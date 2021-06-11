---
title: Virtuele Dataverse-tabelquery's optimaliseren
description: Prestaties van virtuele Dataverse-tabelquery's optimaliseren en problemen oplossen
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054903"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="0c468-103">Virtuele Dataverse-tabelquery's optimaliseren</span><span class="sxs-lookup"><span data-stu-id="0c468-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="0c468-104">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="0c468-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="0c468-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="0c468-105">Overview</span></span>

<span data-ttu-id="0c468-106">Wanneer u virtuele Dataverse-tabellen gebruikt om integraties en andere gegevensverbindingen met Dynamics 365 Human Resources te ontwikkelen, kunnen er prestatieproblemen optreden met query's voor de virtuele tabellen.</span><span class="sxs-lookup"><span data-stu-id="0c468-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="0c468-107">De uitvoering van de query kan traag zijn op verschillende clients of interfaces.</span><span class="sxs-lookup"><span data-stu-id="0c468-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="0c468-108">U kunt het probleem bijvoorbeeld onder de volgende omstandigheden meemaken:</span><span class="sxs-lookup"><span data-stu-id="0c468-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="0c468-109">Bij het uitvoeren van een query op een virtuele tabel via de Dataverse-web-API</span><span class="sxs-lookup"><span data-stu-id="0c468-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="0c468-110">Bij het maken van een Power-app voor een virtuele tabel</span><span class="sxs-lookup"><span data-stu-id="0c468-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="0c468-111">Bij het maken van een Power BI-rapport in een virtuele tabel</span><span class="sxs-lookup"><span data-stu-id="0c468-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="0c468-112">In al deze interfaces kunnen het prestatieprobleem mogelijk optreden.</span><span class="sxs-lookup"><span data-stu-id="0c468-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="0c468-113">Een van de oorzaak van tragere prestaties bij virtuele Dataverse-tabellen voor Human Resources zijn de kolommen met refererende sleutels van de virtuele tabel die betrekking hebben op de [navigatie-eigenschappen van de tabel](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span><span class="sxs-lookup"><span data-stu-id="0c468-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="0c468-114">Wanneer navigatie-eigenschappen voor een virtuele tabel worden gemaakt, wordt automatisch een kolom met de refererende sleutel aan de tabel toegevoegd, die de waarde van de sleutel voor de sleutelkolom van de gerelateerde virtuele tabel vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="0c468-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="0c468-115">De kolom **_mshr_fk_person_id_value** wordt bijvoorbeeld aan de entiteit **mshr_hcmworkerbaseentity** toegevoegd met de eigenschap van de refererende sleutel van de entiteit **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0c468-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="0c468-116">Vanwege de manier waarop de waarden voor deze kolommen met refererende sleutels worden onderhouden in een tabel, kan het ophalen van de waarden een negatieve invloed hebben op de prestaties van een query ten opzichte van de virtuele tabel.</span><span class="sxs-lookup"><span data-stu-id="0c468-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="0c468-117">Potentiële symptomen</span><span class="sxs-lookup"><span data-stu-id="0c468-117">Potential symptoms</span></span>

<span data-ttu-id="0c468-118">Een voorbeeld waar u deze impact kunt zien, is in query's die worden uitvoeren op de entiteit Werknemer (**mshr_hcmworkerentity**) of Basiswerker (**mshr_hcmworkerbaseentity**).</span><span class="sxs-lookup"><span data-stu-id="0c468-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="0c468-119">Het prestatieprobleem kan op een aantal verschillende manieren zichtbaar zijn:</span><span class="sxs-lookup"><span data-stu-id="0c468-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="0c468-120">**Trage uitvoering van query's**: de query uit de virtuele tabel kan de verwachte resultaten retourneren, maar het duurt langer dan verwacht om de uitvoering van de query te voltooien.</span><span class="sxs-lookup"><span data-stu-id="0c468-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="0c468-121">**Time-out van query**: de query krijgt een time-out en geeft de volgende fout: "Een token is verkregen om Finance and Operations aan te roepen maar Finance and Operations heeft een fout van het type InternalServerError geretourneerd."</span><span class="sxs-lookup"><span data-stu-id="0c468-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="0c468-122">**Onverwachte fout**: de query kan een fouttype 400 retourneren met het volgende bericht: "Er is een onverwachte fout opgetreden."</span><span class="sxs-lookup"><span data-stu-id="0c468-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![Fouttype 400 op HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="0c468-124">**Aanvraagbeperking**: de query gebruikt mogelijk te veel serverbronnen waardoor aanvraagbeperking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="0c468-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="0c468-125">In dit geval geeft de query de volgende fout: "Er is een token verkregen om Finance and Operations aan te roepen maar Finance and Operations heeft een fout van het type 429 geretourneerd."</span><span class="sxs-lookup"><span data-stu-id="0c468-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="0c468-126">Meer informatie over aanvraagbeperking in Human Resources vindt u in [Veelgestelde vragen over aanvraagbeperking](./hr-admin-integration-throttling-faq.md).</span><span class="sxs-lookup"><span data-stu-id="0c468-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![Fouttype 429 op HcmWorkerBaseEntity](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="0c468-128">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0c468-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="0c468-129">Het aantal kolommen in de gegevensquery beperken</span><span class="sxs-lookup"><span data-stu-id="0c468-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="0c468-130">Met virtuele tabellen is een van de meest geslaagde methoden om queryprestaties te verbeteren, het beperken van het aantal kolommen dat in de query wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="0c468-131">De algemene richtlijnen voor optimalisatie van queryprestaties zijn om de kolommen die in de query worden geretourneerd, te beperken tot de eigenschappen die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="0c468-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="0c468-132">Dit geldt met name voor de kolommen met de refererende sleutel in virtuele tabellen.</span><span class="sxs-lookup"><span data-stu-id="0c468-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="0c468-133">Als u de waarden in de kolommen met de refererende sleutel niet nodig hebt voor uw integratie of rapport, structureert u de query zo dat u alleen de kolommen selecteert die u nodig hebt, met uitzondering van de kolommen met de refererende sleutel.</span><span class="sxs-lookup"><span data-stu-id="0c468-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="0c468-134">Kolommen selecteren in een OData-query</span><span class="sxs-lookup"><span data-stu-id="0c468-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="0c468-135">Wanneer u een query uitvoert op een virtuele tabel via de Dataverse-web-API, kunt u het aantal kolommen in de query beperken met de **$select**-optie voor de systeemquery en de kolommen definiëren waarvoor resultaten moeten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="0c468-136">Om de prestaties te maximaliseren sluit u kolommen met een refererende sleutel (met prefix **_mshr_FK_**) uit van de query.</span><span class="sxs-lookup"><span data-stu-id="0c468-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="0c468-137">De volgende query voor de entiteit **mshr_hcmworkerbaseentity** bevat bijvoorbeeld alleen de kolommen in de clausule van de **$select**-queryoptie, exclusief waarden van refererende sleutels.</span><span class="sxs-lookup"><span data-stu-id="0c468-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="0c468-138">Hiermee worden de prestaties aanzienlijk verbeterd van een query die alle tabelkolommen bevat.</span><span class="sxs-lookup"><span data-stu-id="0c468-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="0c468-139">De aanbeveling om het aantal geselecteerde kolommen te beperken, is ook van toepassing wanneer u de **$expand**-queryoptie gebruikt om de query uit te breiden naar verwante virtuele tabellen via navigatie-eigenschappen.</span><span class="sxs-lookup"><span data-stu-id="0c468-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="0c468-140">De volgende query bevat bijvoorbeeld kolommen van de entiteit **mshr_hcmworkerbaseentity** met uitgebreide kolommen van de entiteit **mshr_dirpersonentity**.</span><span class="sxs-lookup"><span data-stu-id="0c468-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="0c468-141">De **$select**-queryoptie is ook opgenomen in de clausule van de **$expand**-queryoptie.</span><span class="sxs-lookup"><span data-stu-id="0c468-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="0c468-142">Wanneer u deze methode gebruikt voor het ophalen van gegevens met de **$select**-queryoptie in de clausule van de **$expand**-queryoptie, zijn er meestal betere prestatieverbeteringen wanneer de navigatie-eigenschap tussen de entiteiten een veel-op-één-relatie is.</span><span class="sxs-lookup"><span data-stu-id="0c468-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="0c468-143">Bij het uitbreiden van een één-op-veel-relatie wordt mogelijk niet dezelfde afname in de uitvoering van de query opgemerkt.</span><span class="sxs-lookup"><span data-stu-id="0c468-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="0c468-144">Zie [Tabelrelaties](/powerapps/maker/data-platform/create-edit-entity-relationships) voor meer informatie over de relatiedefinitie voor virtuele Dataverse-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0c468-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="0c468-145">Zie [Gerelateerde entiteitsrecords ophalen met een query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query) voor meer informatie over het gebruik van de systeemqueryopties **$select** en **$expand** in de Dataverse-web-API.</span><span class="sxs-lookup"><span data-stu-id="0c468-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="0c468-146">Kolommen selecteren in Power BI</span><span class="sxs-lookup"><span data-stu-id="0c468-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="0c468-147">Als u tijdens het maken van een Power BI-rapport met een virtuele Dataverse-tabel merkt dat de prestaties trager zijn, kunt u de prestaties verbeteren door kolommen met een refererende sleutel uit te sluiten uit de kolommen die u voor het rapport uit de tabel hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="0c468-148">Als u bijvoorbeeld met Power BI Desktop een rapport maakt op basis van de entiteit **mshr_hcmworkerbaseentity**, kunt u de volgende stappen uitvoeren om de kolommen te selecteren die u in de rapportquery wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="0c468-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="0c468-149">Selecteer in Power BI Desktop **Meer...** in de vervolgkeuzelijst **Gegevens ophalen** op het actielint.</span><span class="sxs-lookup"><span data-stu-id="0c468-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="0c468-150">Voer in het venster **Gegevens ophalen** in het zoekvak **Common Data Service** in, selecteer de **Common Data Service**-connector en selecteer **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="0c468-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="0c468-151">Voer in het veld **Server-URL** van het Common Data Service-venster de organisatie-URI voor uw Dataverse-omgeving in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c468-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Geef de URI in voor de Dataverse-omgeving](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="0c468-153">Vouw het knooppunt **Entiteiten** uit in het navigatievenster.</span><span class="sxs-lookup"><span data-stu-id="0c468-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="0c468-154">Voer in het zoekvak **mshr_hcmworkerbaseentity** en selecteer de entiteit.</span><span class="sxs-lookup"><span data-stu-id="0c468-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="0c468-155">Selecteer **Gegevens transformeren**.</span><span class="sxs-lookup"><span data-stu-id="0c468-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="0c468-156">Selecteer Geavanceerde editor in het venster **Power Query-editor**.</span><span class="sxs-lookup"><span data-stu-id="0c468-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="0c468-157">Werk de query bij in het venster **Geavanceerde editor** zodat deze er als hieronder uitziet en voeg zo nodig kolommen aan de matrix toe of verwijder deze.</span><span class="sxs-lookup"><span data-stu-id="0c468-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![De query bijwerken in Geavanceerde editor voor Power Query-editor](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="0c468-159">Selecteer **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="0c468-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="0c468-160">Als u eerder een fout van het type 429 hebt ontvangen van de query voordat u de query bijwerkt, moet u mogelijk wachten tot de periode voor een nieuwe poging voorbij is voordat de query wordt vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="0c468-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="0c468-161">Klik op **Sluiten en toepassen** in het actielint van de Power Query-editor.</span><span class="sxs-lookup"><span data-stu-id="0c468-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="0c468-162">Vervolgens kunt u beginnen met het maken van het Power BI-rapport aan de hand van de kolommen die in de virtuele tabel zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="0c468-163">Kolommen selecteren in Power Apps</span><span class="sxs-lookup"><span data-stu-id="0c468-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="0c468-164">Net zoals bij query's in Dataverse-web-API en Power BI kunt u queryprestaties verbeteren voor Power Apps op basis van virtuele Dataverse-tabellen door kolommen van gerelateerde tabellen uit te sluiten van de app.</span><span class="sxs-lookup"><span data-stu-id="0c468-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="0c468-165">Als kolommen uit een gerelateerde tabel zijn opgenomen op een pagina, bevat de aanvraag-URL die is gemaakt om de gegevens op te halen eigenschappen van de gerelateerde tabel.</span><span class="sxs-lookup"><span data-stu-id="0c468-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="0c468-166">Hierdoor worden de prestaties beperkt, zoals in de voorbeelden van [Kolommen selecteren in een bovenstaande OData-query](#selecting-columns-in-power-apps), omdat extra zoekopdrachten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="0c468-167">Als u dit probleem wilt verhelpen, kunt u controleren of er geen gegevensvelden uit gerelateerde tabellen zijn opgenomen in een gegevensformulier van uw Power App.</span><span class="sxs-lookup"><span data-stu-id="0c468-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="0c468-168">Selecteer in het deelvenster Structuurweergave het gegevensformulier voor het scherm.</span><span class="sxs-lookup"><span data-stu-id="0c468-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="0c468-169">Selecteer **Bewerken** in het **eigenschappenvenster** voor de eigenschap **Velden**.</span><span class="sxs-lookup"><span data-stu-id="0c468-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="0c468-170">Controleer in het deelvenster **Gegevens** of geen van de geselecteerde velden deel uitmaken van de virtuele tabel van de gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="0c468-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="0c468-171">Als een van de gegevensvelden op een pagina in de app bijvoorbeeld verwijst naar een andere tabel, zoals **ThisItem.Worker.Name**, waarbij **Werknemer** de gerelateerde tabel is, kunnen de prestaties bij het ophalen van de gegevens worden verlaagd.</span><span class="sxs-lookup"><span data-stu-id="0c468-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="0c468-172">Gebruik de [Power Apps-monitor](/powerapps/maker/monitor-overview) om ervoor te zorgen dat alleen de kolommen die u nodig hebt in de query worden opgenomen om de gegevens voor de Power App op te halen.</span><span class="sxs-lookup"><span data-stu-id="0c468-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="0c468-173">U kunt de URL van de getRows-bewerking weergeven, zodat de geselecteerde kolommen voor de app optimaal zijn om de gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="0c468-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Met Power Apps-monitor kunt u de getData-bewerking analyseren.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="0c468-175">De gegevensquery filteren</span><span class="sxs-lookup"><span data-stu-id="0c468-175">Filtering the data query</span></span>

<span data-ttu-id="0c468-176">Een andere methode voor het verbeteren van de prestaties voor het uitvoeren van query's is het beperken van het aantal records dat in de queryresultaten wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0c468-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="0c468-177">U kunt dit doen door de resultaten te filteren, zodat u alleen de records ontvangt die u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="0c468-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="0c468-178">Zie [Filterresultaten](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) voor meer informatie over het filteren van querygegevens.</span><span class="sxs-lookup"><span data-stu-id="0c468-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="0c468-179">De paginagrootte van de query beperken</span><span class="sxs-lookup"><span data-stu-id="0c468-179">Limiting the page size of the query</span></span>

<span data-ttu-id="0c468-180">Als u met grote gegevenssets werkt, kunt u queryresultaten op meerdere pagina's verdelen door de koptekst `odata.maxpagesize` toe te voegen aan gegevensquery's.</span><span class="sxs-lookup"><span data-stu-id="0c468-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="0c468-181">Zie [Het aantal entiteiten opgeven dat op een pagina moet worden geretourneerd](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page) voor meer informatie over paginering.</span><span class="sxs-lookup"><span data-stu-id="0c468-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="0c468-182">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0c468-182">See also</span></span>

- [<span data-ttu-id="0c468-183">Virtuele Dataverse-entiteiten configureren</span><span class="sxs-lookup"><span data-stu-id="0c468-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="0c468-184">Veelgestelde vragen over virtuele tabellen in Human Resources</span><span class="sxs-lookup"><span data-stu-id="0c468-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="0c468-185">Veelgestelde vragen over aanvraagbeperking</span><span class="sxs-lookup"><span data-stu-id="0c468-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]