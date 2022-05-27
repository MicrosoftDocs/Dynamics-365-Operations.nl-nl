---
title: Virtuele Dataverse-tabelquery's optimaliseren
description: Prestaties van virtuele Dataverse-tabelquery's optimaliseren en problemen oplossen
author: twheeloc
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f75176781620cd6f845c002876eba6e34d5793e7
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692221"
---
# <a name="optimize-dataverse-virtual-table-queries"></a>Virtuele Dataverse-tabelquery's optimaliseren


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



## <a name="issue"></a>Uitgeven

### <a name="overview"></a>Overzicht

Wanneer u virtuele Dataverse-tabellen gebruikt om integraties en andere gegevensverbindingen met Dynamics 365 Human Resources te ontwikkelen, kunnen er prestatieproblemen optreden met query's voor de virtuele tabellen. De uitvoering van de query kan traag zijn op verschillende clients of interfaces. U kunt het probleem bijvoorbeeld onder de volgende omstandigheden meemaken:

- Bij het uitvoeren van een query op een virtuele tabel via de Dataverse-web-API
- Bij het maken van een Power-app voor een virtuele tabel
- Bij het maken van een Power BI-rapport in een virtuele tabel

In al deze interfaces kunnen het prestatieprobleem mogelijk optreden.

Een van de oorzaak van tragere prestaties bij virtuele Dataverse-tabellen voor Human Resources zijn de kolommen met refererende sleutels van de virtuele tabel die betrekking hebben op de [navigatie-eigenschappen van de tabel](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties). Wanneer navigatie-eigenschappen voor een virtuele tabel worden gemaakt, wordt automatisch een kolom met de refererende sleutel aan de tabel toegevoegd, die de waarde van de sleutel voor de sleutelkolom van de gerelateerde virtuele tabel vertegenwoordigt. De kolom **_mshr_fk_person_id_value** wordt bijvoorbeeld aan de entiteit **mshr_hcmworkerbaseentity** toegevoegd met de eigenschap van de refererende sleutel van de entiteit **mshr_dirpersonentity**. Vanwege de manier waarop de waarden voor deze kolommen met refererende sleutels worden onderhouden in een tabel, kan het ophalen van de waarden een negatieve invloed hebben op de prestaties van een query ten opzichte van de virtuele tabel.

### <a name="potential-symptoms"></a>Potentiële symptomen

Een voorbeeld waar u deze impact kunt zien, is in query's die worden uitvoeren op de entiteit Werknemer (**mshr_hcmworkerentity**) of Basiswerker (**mshr_hcmworkerbaseentity**). Het prestatieprobleem kan op een aantal verschillende manieren zichtbaar zijn:

- **Trage uitvoering van query's**: de query uit de virtuele tabel kan de verwachte resultaten retourneren, maar het duurt langer dan verwacht om de uitvoering van de query te voltooien.
- **Time-out van query**: er treedt een time-out voor de query op en de volgende fout wordt geretourneerd: "Een token is verkregen om Finance and Operations aan te roepen maar Finance and Operations heeft een fout van het type InternalServerError geretourneerd."
- **Onverwachte fout**: de query kan een fouttype 400 retourneren met het volgende bericht: "Er is een onverwachte fout opgetreden."

  ![Fouttype 400 op HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType400.png)

- **Aanvraagbeperking**: de query gebruikt mogelijk te veel serverbronnen waardoor aanvraagbeperking wordt toegepast. In dit geval geeft de query de volgende fout: "Er is een token verkregen om Finance and Operations aan te roepen maar Finance and Operations heeft een fout van het type 429 geretourneerd." Meer informatie over aanvraagbeperking in Human Resources vindt u in [Veelgestelde vragen over aanvraagbeperking](./hr-admin-integration-throttling-faq.md).

  ![Fouttype 429 op HcmWorkerBaseEntity.](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a>Oplossing

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a>Het aantal kolommen in de gegevensquery beperken

Met virtuele tabellen is een van de meest geslaagde methoden om queryprestaties te verbeteren, het beperken van het aantal kolommen dat in de query wordt geselecteerd. De algemene richtlijnen voor optimalisatie van queryprestaties zijn om de kolommen die in de query worden geretourneerd, te beperken tot de eigenschappen die u nodig hebt. Dit geldt met name voor de kolommen met de refererende sleutel in virtuele tabellen. Als u de waarden in de kolommen met de refererende sleutel niet nodig hebt voor uw integratie of rapport, structureert u de query zo dat u alleen de kolommen selecteert die u nodig hebt, met uitzondering van de kolommen met de refererende sleutel.

#### <a name="selecting-columns-in-an-odata-query"></a>Kolommen selecteren in een OData-query

Wanneer u een query uitvoert op een virtuele tabel via de Dataverse-web-API, kunt u het aantal kolommen in de query beperken met de **$select**-optie voor de systeemquery en de kolommen definiëren waarvoor resultaten moeten worden geretourneerd. Om de prestaties te maximaliseren sluit u kolommen met een refererende sleutel (met prefix **_mshr_FK_**) uit van de query.

De volgende query voor de entiteit **mshr_hcmworkerbaseentity** bevat bijvoorbeeld alleen de kolommen in de clausule van de **$select**-queryoptie, exclusief waarden van refererende sleutels. Hiermee worden de prestaties aanzienlijk verbeterd van een query die alle tabelkolommen bevat.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

De aanbeveling om het aantal geselecteerde kolommen te beperken, is ook van toepassing wanneer u de **$expand**-queryoptie gebruikt om de query uit te breiden naar verwante virtuele tabellen via navigatie-eigenschappen. De volgende query bevat bijvoorbeeld kolommen van de entiteit **mshr_hcmworkerbaseentity** met uitgebreide kolommen van de entiteit **mshr_dirpersonentity**. De **$select**-queryoptie is ook opgenomen in de clausule van de **$expand**-queryoptie.

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

Wanneer u deze methode gebruikt voor het ophalen van gegevens met de **$select**-queryoptie in de clausule van de **$expand**-queryoptie, zijn er meestal betere prestatieverbeteringen wanneer de navigatie-eigenschap tussen de entiteiten een veel-op-één-relatie is. Bij het uitbreiden van een één-op-veel-relatie wordt mogelijk niet dezelfde afname in de uitvoering van de query opgemerkt. Zie [Tabelrelaties](/powerapps/maker/data-platform/create-edit-entity-relationships) voor meer informatie over de relatiedefinitie voor virtuele Dataverse-tabellen.

Zie [Gerelateerde entiteitsrecords ophalen met een query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query) voor meer informatie over het gebruik van de systeemqueryopties **$select** en **$expand** in de Dataverse-web-API.

#### <a name="selecting-columns-in-power-bi"></a>Kolommen selecteren in Power BI

Als u tijdens het maken van een Power BI-rapport met een virtuele Dataverse-tabel merkt dat de prestaties trager zijn, kunt u de prestaties verbeteren door kolommen met een refererende sleutel uit te sluiten uit de kolommen die u voor het rapport uit de tabel hebt geselecteerd. Als u bijvoorbeeld met Power BI Desktop een rapport maakt op basis van de entiteit **mshr_hcmworkerbaseentity**, kunt u de volgende stappen uitvoeren om de kolommen te selecteren die u in de rapportquery wilt opnemen.

1. Selecteer in Power BI Desktop **Meer...** in de vervolgkeuzelijst **Gegevens ophalen** op het actielint.
2. Voer in het venster **Gegevens ophalen** in het zoekvak **Common Data Service** in, selecteer de **Common Data Service**-connector en selecteer **Verbinden**.
3. Voer in het veld **Server-URL** van het Common Data Service-venster de organisatie-URI voor uw Dataverse-omgeving in en selecteer **OK**.
  
   ![Geef de URI in voor de Dataverse-omgeving.](./media/PowerBIDataverseURLSetup.png)
  
4. Vouw het knooppunt **Entiteiten** uit in het navigatievenster.
5. Voer in het zoekvak **mshr_hcmworkerbaseentity** en selecteer de entiteit.
6. Selecteer **Gegevens transformeren**.
7. Selecteer **Geavanceerde editor** in het venster Power Query-editor.
8. Werk de query bij in het venster **Geavanceerde editor** zodat deze er als hieronder uitziet en voeg zo nodig kolommen aan de matrix toe of verwijder deze.

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![De query bijwerken in de Geavanceerde editor voor Power Query-editor.](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. Selecteer **Gereed**.

   > [!NOTE]
   > Als u eerder een fout van het type 429 hebt ontvangen van de query voordat u de query bijwerkt, moet u mogelijk wachten tot de periode voor een nieuwe poging voorbij is voordat de query wordt vernieuwd.

10. Klik op **Sluiten en toepassen** in het actielint van de Power Query-editor.

Vervolgens kunt u beginnen met het maken van het Power BI-rapport aan de hand van de kolommen die in de virtuele tabel zijn geselecteerd.

#### <a name="selecting-columns-in-power-apps"></a>Kolommen selecteren in Power Apps

Net zoals bij query's in Dataverse-web-API en Power BI kunt u queryprestaties verbeteren voor Power Apps op basis van virtuele Dataverse-tabellen door kolommen van gerelateerde tabellen uit te sluiten van de app. Als kolommen uit een gerelateerde tabel zijn opgenomen op een pagina, bevat de aanvraag-URL die is gemaakt om de gegevens op te halen eigenschappen van de gerelateerde tabel. Hierdoor worden de prestaties beperkt, zoals in de voorbeelden van [Kolommen selecteren in een bovenstaande OData-query](#selecting-columns-in-power-apps), omdat extra zoekopdrachten worden uitgevoerd.

Als u dit probleem wilt verhelpen, kunt u controleren of er geen gegevensvelden uit gerelateerde tabellen zijn opgenomen in een gegevensformulier van uw Power App.

1. Selecteer in het deelvenster Structuurweergave het gegevensformulier voor het scherm.
2. Selecteer **Bewerken** in het **eigenschappenvenster** voor de eigenschap **Velden**.
3. Controleer in het deelvenster **Gegevens** of geen van de geselecteerde velden deel uitmaken van de virtuele tabel van de gegevensbron.

Als een van de gegevensvelden op een pagina in de app bijvoorbeeld verwijst naar een andere tabel, zoals **ThisItem.Worker.Name**, waarbij **Werknemer** de gerelateerde tabel is, kunnen de prestaties bij het ophalen van de gegevens worden verlaagd.

Gebruik de [Power Apps-monitor](/powerapps/maker/monitor-overview) om ervoor te zorgen dat alleen de kolommen die u nodig hebt in de query worden opgenomen om de gegevens voor de Power App op te halen. U kunt de URL van de getRows-bewerking weergeven, zodat de geselecteerde kolommen voor de app optimaal zijn om de gegevens op te halen.

![Met Power Apps-monitor kunt u de getData-bewerking analyseren.](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a>De gegevensquery filteren

Een andere methode voor het verbeteren van de prestaties voor het uitvoeren van query's is het beperken van het aantal records dat in de queryresultaten wordt geretourneerd. U kunt dit doen door de resultaten te filteren, zodat u alleen de records ontvangt die u nodig hebt.

Zie [Filterresultaten](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) voor meer informatie over het filteren van querygegevens.

### <a name="limiting-the-page-size-of-the-query"></a>De paginagrootte van de query beperken

Als u met grote gegevenssets werkt, kunt u queryresultaten op meerdere pagina's verdelen door de koptekst `odata.maxpagesize` toe te voegen aan gegevensquery's.

Zie [Het aantal entiteiten opgeven dat op een pagina moet worden geretourneerd](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page) voor meer informatie over paginering.

## <a name="see-also"></a>Zie ook

- [Virtuele Dataverse-entiteiten configureren](hr-admin-integration-common-data-service-virtual-entities.md)
- [Veelgestelde vragen over virtuele tabellen in Human Resources](hr-admin-virtual-entity-faq.md)
- [Veelgestelde vragen over aanvraagbeperking](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
