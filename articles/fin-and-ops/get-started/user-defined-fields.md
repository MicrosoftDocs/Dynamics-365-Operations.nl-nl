---
title: Maken en werken met aangepaste velden
description: Dit onderwerp beschrijft hoe sommige gebruikers met Microsoft Dynamics 365 for Finance and Operations aangepaste velden kunnen maken om de toepassing aan te passen aan hun bedrijf.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18402579789c17de7b46dd7a013b3b6327ea5d4f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348015"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="fff0b-103">Maken en werken met aangepaste velden</span><span class="sxs-lookup"><span data-stu-id="fff0b-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fff0b-104">Microsoft Dynamics 365 for Finance and Operations biedt een uitgebreide reeks kant-en-klare velden voor het beheren van een breed scala van bedrijfsprocessen, maar soms is er behoefte in een bedrijf om aanvullende informatie bij te houden in het systeem.</span><span class="sxs-lookup"><span data-stu-id="fff0b-104">While Microsoft Dynamics 365 for Finance and Operations provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="fff0b-105">Voor deze behoefte kunt u met Finance and Operations aangepaste velden maken om de toepassing aan te passen aan uw bedrijf, als u machtigingen hebt voor de functie.</span><span class="sxs-lookup"><span data-stu-id="fff0b-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="fff0b-106">De mogelijkheid om aangepaste velden toe te voegen, is beschikbaar in platformupdate 13 en hoger.</span><span class="sxs-lookup"><span data-stu-id="fff0b-106">The ability to add custom fields is available in platform update 13 and later.</span></span>

<span data-ttu-id="fff0b-107">In deze video wordt getoond hoe gemakkelijk het is een aangepast veld toe te voegen aan een pagina: [Aangepaste velden toevoegen in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="fff0b-107">This video shows how easy it is to add a custom field to a page: [Adding custom fields in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="fff0b-108">Aangepaste velden maken</span><span class="sxs-lookup"><span data-stu-id="fff0b-108">Creating custom fields</span></span>

<span data-ttu-id="fff0b-109">Nadat u extra informatie hebt aangegeven die u wilt bijhouden in de toepassing, kunt u het aangepaste veld in de juiste tabel maken en weergeven op een pagina.</span><span class="sxs-lookup"><span data-stu-id="fff0b-109">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="fff0b-110">De volgende stappen beschrijven het proces voor het maken van een aangepast veld en dat veld plaatsen op een formulier.</span><span class="sxs-lookup"><span data-stu-id="fff0b-110">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="fff0b-111">Ga naar het formulier waar het nieuwe veld is vereist.</span><span class="sxs-lookup"><span data-stu-id="fff0b-111">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="fff0b-112">Aangezien het einddoel is het aangepaste veld op een formulier weer te geven, bestaat het ingangspunt voor het maken van aangepaste velden in de persoonlijke ervaring.</span><span class="sxs-lookup"><span data-stu-id="fff0b-112">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="fff0b-113">Open de aanpassingswerkbalk door **Opties** en vervolgens **Dit formulier aanpassen** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="fff0b-113">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="fff0b-114">Klik op **invoegen** en vervolgens op **Veld**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-114">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="fff0b-115">Selecteer het gebied van het formulier waar u het nieuwe veld wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-115">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="fff0b-116">Na selectie bevat het dialoogvenster **Velden invoegen** een lijst met bestaande velden die kunnen worden ingevoegd in het geselecteerde gebied van het formulier.</span><span class="sxs-lookup"><span data-stu-id="fff0b-116">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="fff0b-117">Controleer dat het veld waarin u geïnteresseerd bent nog niet in de lijst staat.</span><span class="sxs-lookup"><span data-stu-id="fff0b-117">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="fff0b-118">Als dit wel het geval is, selecteert u gewoon dat veld in de lijst en klikt u op **Invoegen**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-118">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="fff0b-119">Klik op de knop **Nieuw veld maken** boven de lijst om het proces te starten om een aangepast veld te maken.</span><span class="sxs-lookup"><span data-stu-id="fff0b-119">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="fff0b-120">Hiermee opent u het dialoogvenster **Nieuw veld maken**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-120">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="fff0b-121">Als u de knop **Nieuw veld maken** niet ziet, hebt u niet de benodigde machtigingen om deze functie te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fff0b-121">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="fff0b-122">Voer in het dialoogvenster **Nieuw veld maken** de volgende informatie in.</span><span class="sxs-lookup"><span data-stu-id="fff0b-122">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="fff0b-123">Selecteer de databasetabel waar dit veld moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="fff0b-123">Select the database table where this field should be added.</span></span> <span data-ttu-id="fff0b-124">Houd er rekening mee dat alleen de tabellen die ondersteuning bieden voor aangepaste velden, in de vervolgkeuzelijst worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-124">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="fff0b-125">Zie de sectie hieronder voor meer technische informatie over ondersteunde tabellen.</span><span class="sxs-lookup"><span data-stu-id="fff0b-125">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="fff0b-126">Selecteer het gegevenstype voor het nieuwe veld</span><span class="sxs-lookup"><span data-stu-id="fff0b-126">Select the data type for the new field.</span></span> <span data-ttu-id="fff0b-127">De beschikbare gegevenstypen zijn selectievakje, datum, datum/tijd, decimaal, nummer, selectielijst en tekst.</span><span class="sxs-lookup"><span data-stu-id="fff0b-127">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="fff0b-128">Als u het tekstgegevenstype kiest, kunt u ook de maximale lengte van de tekst die kan worden ingevoerd in dit veld opgeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-128">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="fff0b-129">Als u het gegevenstype selectielijst kiest, kunt u ook de set geldige waarden voor het veld selecteren.</span><span class="sxs-lookup"><span data-stu-id="fff0b-129">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="fff0b-130">Geef een naam, label en help-tekst voor het veld op.</span><span class="sxs-lookup"><span data-stu-id="fff0b-130">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="fff0b-131">De naam komt overeen met de fysieke veldnaam in de database, terwijl het label en de help-tekst de tekst zijn die wordt gebruikt voor het weergeven van dit veld in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="fff0b-131">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="fff0b-132">Als dit het enige veld dat u wilt maken voor dit formulier, klikt u op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-132">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="fff0b-133">Als u extra velden moet maken, klikt u op **Opslaan en nieuw** en gaat u terug naar stap 7.</span><span class="sxs-lookup"><span data-stu-id="fff0b-133">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="fff0b-134">Er is momenteel een limiet van **20 aangepaste velden per tabel**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-134">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="fff0b-135">Als u het dialoogvenster **Nieuw veld maken** verlaat, keert u terug naar het dialoogvenster **Velden invoegen**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-135">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="fff0b-136">Eventuele aangepaste velden die zojuist zijn toegevoegd, worden automatisch gemarkeerd in de lijst met velden die in het formulier moeten worden ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="fff0b-136">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="fff0b-137">Klik op **Invoegen** voor het invoegen van de gemarkeerde velden in het geselecteerde gedeelte van het formulier.</span><span class="sxs-lookup"><span data-stu-id="fff0b-137">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="fff0b-138">**Optioneel:** schakel de modus **Verplaatsen** op de aanpassingswerkbalk in om de nieuwe velden naar de gewenste locatie in het geselecteerde gebied te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="fff0b-138">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="fff0b-139">Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het gebruik van de verschillende mogelijkheden voor aanpassing van een formulier aan uw persoonlijke gebruik.</span><span class="sxs-lookup"><span data-stu-id="fff0b-139">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="fff0b-140">Aangepaste velden delen met andere gebruikers</span><span class="sxs-lookup"><span data-stu-id="fff0b-140">Sharing custom fields with other users</span></span>

<span data-ttu-id="fff0b-141">Nadat u een aangepast veld hebt gemaakt en het op een formulier wordt weergegeven, wilt u wellicht deze bijgewerkte paginaweergave met het nieuwe veld aan andere gebruikers in het systeem bieden.</span><span class="sxs-lookup"><span data-stu-id="fff0b-141">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="fff0b-142">Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:</span><span class="sxs-lookup"><span data-stu-id="fff0b-142">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="fff0b-143">De aanbevolen route is via de systeembeheerder, die een aanpassing aan alle gebruikers of een subset van gebruikers kan doorgeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-143">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="fff0b-144">Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fff0b-144">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="fff0b-145">U kunt ook uw wijzigingen (*aanpassingen* genoemd) exporteren, Stuur ze naar een of meer gebruikers en laat elk van deze gebruikers uw wijzigingen importeren.</span><span class="sxs-lookup"><span data-stu-id="fff0b-145">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="fff0b-146">Met de optie **Beheren** op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.</span><span class="sxs-lookup"><span data-stu-id="fff0b-146">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="fff0b-147">Aangepaste velden beheren</span><span class="sxs-lookup"><span data-stu-id="fff0b-147">Managing custom fields</span></span>

<span data-ttu-id="fff0b-148">Beheer van de aangepaste velden in het systeem kan worden uitgevoerd via de pagina **Aangepaste velden** in de module Systeembeheer.</span><span class="sxs-lookup"><span data-stu-id="fff0b-148">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="fff0b-149">Op deze pagina kunnen gebruikers toegang tot veel mogelijkheden krijgen, zoals:</span><span class="sxs-lookup"><span data-stu-id="fff0b-149">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="fff0b-150">Een lijst weergeven met alle aangepaste velden in het systeem.</span><span class="sxs-lookup"><span data-stu-id="fff0b-150">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="fff0b-151">Beperkt bewerken van bestaande aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="fff0b-151">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="fff0b-152">Aangepaste velden verwijderen.</span><span class="sxs-lookup"><span data-stu-id="fff0b-152">Deleting custom fields.</span></span>
- <span data-ttu-id="fff0b-153">Aangepaste velden in gegevensentiteiten weergeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-153">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="fff0b-154">Vertalingen van labels van aangepaste velden en help-tekst bieden.</span><span class="sxs-lookup"><span data-stu-id="fff0b-154">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="fff0b-155">Alle aangepaste velden weergeven</span><span class="sxs-lookup"><span data-stu-id="fff0b-155">Viewing all custom fields</span></span>

<span data-ttu-id="fff0b-156">De pagina **Aangepaste velden** biedt inzicht in alle aangepaste velden die zijn gedefinieerd in het systeem.</span><span class="sxs-lookup"><span data-stu-id="fff0b-156">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="fff0b-157">Selecteer gewoon de tabel waarin u geïnteresseerd bent en de pagina wordt bijgewerkt met een lijst met aangepaste velden die zijn gekoppeld aan die tabel.</span><span class="sxs-lookup"><span data-stu-id="fff0b-157">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="fff0b-158">Als u een aangepast veld kiest uit de lijst, kunt u alle details weergeven over het veld.</span><span class="sxs-lookup"><span data-stu-id="fff0b-158">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="fff0b-159">Aangepaste velden bewerken</span><span class="sxs-lookup"><span data-stu-id="fff0b-159">Editing custom fields</span></span>

<span data-ttu-id="fff0b-160">Nadat u een aangepast veld hebt gemaakt, kunnen alleen bepaalde delen van informatie over het aangepaste veld worden gewijzigd op de pagina **Aangepaste velden**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-160">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="fff0b-161">U *kunt* deze kenmerken wijzigen:</span><span class="sxs-lookup"><span data-stu-id="fff0b-161">You *can* modify these attributes:</span></span>

- <span data-ttu-id="fff0b-162">Label</span><span class="sxs-lookup"><span data-stu-id="fff0b-162">Label</span></span>
- <span data-ttu-id="fff0b-163">Help-tekst</span><span class="sxs-lookup"><span data-stu-id="fff0b-163">Help text</span></span>
- <span data-ttu-id="fff0b-164">Lengte voor tekstvelden</span><span class="sxs-lookup"><span data-stu-id="fff0b-164">Length, for Text fields</span></span>

<span data-ttu-id="fff0b-165">U kunt de volgende kenmerken *niet* bewerken:</span><span class="sxs-lookup"><span data-stu-id="fff0b-165">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="fff0b-166">Veldnaam</span><span class="sxs-lookup"><span data-stu-id="fff0b-166">Field name</span></span>
- <span data-ttu-id="fff0b-167">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="fff0b-167">Data type</span></span>

<span data-ttu-id="fff0b-168">Daarnaast kan voor selectielijstvelden, de lijst geldige waarden voor het aangepaste veld opnieuw worden geordend en kunnen nieuwe waarden worden toegevoegd. Bestaande waarden voor het selectielijstveld kunnen echter niet worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="fff0b-168">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="fff0b-169">Vergeet niet op **Wijzigingen toepassen** te klikken wanneer u klaar bent met bewerken van velden voor een bepaalde tabel, zodat de wijzigingen worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="fff0b-169">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="fff0b-170">Aangepaste velden in gegevensentiteiten weergeven</span><span class="sxs-lookup"><span data-stu-id="fff0b-170">Exposing custom fields on data entities</span></span>

<span data-ttu-id="fff0b-171">Het is belangrijk toe te staan dat aangepaste velden zichtbaar zijn in gegevensentiteiten.</span><span class="sxs-lookup"><span data-stu-id="fff0b-171">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="fff0b-172">Gegevensentiteiten worden gebruikt in de functie [Openen in Office](../../dev-itpro/office-integration/office-integration.md) en voor scenario's voor het importeren/exporteren van gegevens.</span><span class="sxs-lookup"><span data-stu-id="fff0b-172">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="fff0b-173">Ga als volgt te werk om een aangepast veld in een gegevensentiteit weer te geven:</span><span class="sxs-lookup"><span data-stu-id="fff0b-173">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="fff0b-174">Selecteer het aangepaste veld op het formulier **Aangepaste velden**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-174">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="fff0b-175">Vouw de sectie **Entiteiten** uit om de set relevante entiteiten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-175">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="fff0b-176">Klik op de knop **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-176">Click the **Edit** button.</span></span>
4. <span data-ttu-id="fff0b-177">Selecteer het veld **Ingeschakeld** voor elke entiteit die dit veld moet weergeven.</span><span class="sxs-lookup"><span data-stu-id="fff0b-177">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="fff0b-178">Klik op **Wijzigingen toepassen** om uw selecties op te slaan.</span><span class="sxs-lookup"><span data-stu-id="fff0b-178">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="fff0b-179">Toestaan dat aangepaste velden worden weergegeven in andere talen</span><span class="sxs-lookup"><span data-stu-id="fff0b-179">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="fff0b-180">Omdat gebruikers in allerlei talen toegang moeten kunnen hebben tot aangepaste velden, bevat de pagina **Aangepaste velden** een mechanisme waarmee het label en de help-tekst van een aangepast veld kan worden vertaald in andere talen.</span><span class="sxs-lookup"><span data-stu-id="fff0b-180">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="fff0b-181">De volgende stappen beschrijven het proces voor het omzetten van aangepaste velden in andere talen:</span><span class="sxs-lookup"><span data-stu-id="fff0b-181">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="fff0b-182">Selecteer het aangepaste veld op de pagina **Aangepaste velden**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-182">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="fff0b-183">Selecteer de knop **Vertalingen** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="fff0b-183">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="fff0b-184">Hiermee opent u een vervolgkeuzelijst met bestaande vertalingen voor dit veld.</span><span class="sxs-lookup"><span data-stu-id="fff0b-184">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="fff0b-185">De vervolgkeuzelijst **Taal** toont de set talen waarvoor reeds vertalingen zijn verschaft.</span><span class="sxs-lookup"><span data-stu-id="fff0b-185">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="fff0b-186">Als u een bestaande vertaling wilt bewerken, selecteert u de gewenste taal in het menu en wijzigt u de waarden voor het label en de help-tekst.</span><span class="sxs-lookup"><span data-stu-id="fff0b-186">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="fff0b-187">Klik anders op de knop **Taal toevoegen**, selecteer de gewenste taal in het menu, en geef vertaalde waarden op voor het label en de help-tekst.</span><span class="sxs-lookup"><span data-stu-id="fff0b-187">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="fff0b-188">Wanneer u klaar bent, klikt u op **OK**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-188">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="fff0b-189">Aangepaste velden verwijderen</span><span class="sxs-lookup"><span data-stu-id="fff0b-189">Deleting custom fields</span></span>

<span data-ttu-id="fff0b-190">In sommige zeldzame gevallen kunt u bepalen dat een aangepast veld niet meer nodig is.</span><span class="sxs-lookup"><span data-stu-id="fff0b-190">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="fff0b-191">Als dit gebeurt kan een systeembeheerder het veld verwijderen van de pagina **Aangepaste velden**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-191">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="fff0b-192">Hiertoe selecteert u het juiste veld, klikt u op **Verwijderen**, klikt u op **Ja** om de verwijdering te bevestigen en klikt u ten slotte op **Wijzigingen toe passen**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-192">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="fff0b-193">Deze actie kan niet ongedaan worden gemaakt en leidt ertoe dat de gegevens die zijn gekoppeld aan het veld, permanent worden verwijderd uit de database.</span><span class="sxs-lookup"><span data-stu-id="fff0b-193">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="fff0b-194">Bijlage</span><span class="sxs-lookup"><span data-stu-id="fff0b-194">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="fff0b-195">Wie kan aangepaste velden maken?</span><span class="sxs-lookup"><span data-stu-id="fff0b-195">Who can create custom fields?</span></span>

<span data-ttu-id="fff0b-196">Als beveiliging voor het systeem kunnen alleen systeembeheerders standaard aangepaste velden maken.</span><span class="sxs-lookup"><span data-stu-id="fff0b-196">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="fff0b-197">Hoofdgebruikers van wie de organisatie dat nodig vindt, kunnen echter door systeembeheerders rechten worden gegeven om aangepaste velden te maken met de beveiligingsrol **Runtimeaanpassing hoofdgebruiker**.</span><span class="sxs-lookup"><span data-stu-id="fff0b-197">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="fff0b-198">Gebruikers zonder deze beveiligingsrol kunnen geen aangepaste velden maken, maar kunnen aangepaste velden die door andere gebruikers in het systeem zijn gemaakt, wel zien en gebruiken.</span><span class="sxs-lookup"><span data-stu-id="fff0b-198">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="fff0b-199">Welke tabellen ondersteunen aangepaste velden?</span><span class="sxs-lookup"><span data-stu-id="fff0b-199">What tables support custom fields?</span></span>

<span data-ttu-id="fff0b-200">Omwille van prestaties en technische redenen kunnen momenteel alleen aangepaste velden worden toegevoegd aan tabellen die voldoen aan de volgende voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="fff0b-200">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="fff0b-201">De tabel moet zijn gemarkeerd als een van deze groepen:</span><span class="sxs-lookup"><span data-stu-id="fff0b-201">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="fff0b-202">Groep</span><span class="sxs-lookup"><span data-stu-id="fff0b-202">Group</span></span>
    - <span data-ttu-id="fff0b-203">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="fff0b-203">WorksheetHeader</span></span>
    - <span data-ttu-id="fff0b-204">Hoofdonderdeel</span><span class="sxs-lookup"><span data-stu-id="fff0b-204">Main</span></span>
    - <span data-ttu-id="fff0b-205">Diversen</span><span class="sxs-lookup"><span data-stu-id="fff0b-205">Miscellaneous</span></span>
    - <span data-ttu-id="fff0b-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="fff0b-206">Parameter</span></span>
    - <span data-ttu-id="fff0b-207">Verwijzing</span><span class="sxs-lookup"><span data-stu-id="fff0b-207">Reference</span></span>
    - <span data-ttu-id="fff0b-208">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="fff0b-208">TransactionHeader</span></span>

- <span data-ttu-id="fff0b-209">De tabel kan niet een andere tabel uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="fff0b-209">The table cannot extend another table.</span></span>
- <span data-ttu-id="fff0b-210">De tabel kan niet zijn gemarkeerd als een systeemtabel.</span><span class="sxs-lookup"><span data-stu-id="fff0b-210">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="fff0b-211">De tabel kan geen tijdelijke tabel zijn.</span><span class="sxs-lookup"><span data-stu-id="fff0b-211">The table cannot be a temporary table.</span></span>
