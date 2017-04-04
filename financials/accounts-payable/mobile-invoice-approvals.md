---
title: Mobiele goed te keuren
description: Mobiele mogelijkheden in Microsoft Dynamics 365 for Operations kunnen een zakelijke gebruiker mobiele ervaringen ontwerpen. Voor geavanceerde scenario&quot;s, het platform we ook ontwikkelaars van de mogelijkheden als ze nodig hebt. De meest effectieve manier om te leren enkele van de nieuwe concepten van mobiele is het proces van het ontwerpen van een paar scenario&quot;s doorlopen. In dit onderwerp is bedoeld om een praktische aanpak voor het ontwerpen van mobiele scenario&quot;s door middel van leverancier goed te keuren voor mobiel gebruik kist bevatten. In dit onderwerp kunt u andere variaties van de scenario&quot;s ontwerpen en kan ook worden toegepast op andere scenario&quot;s die niet zijn gerelateerd aan facturen van leveranciers.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 30229c0d24aed0bd927993b9af76b32d9bb073ee
ms.lasthandoff: 03/31/2017


---

# <a name="mobile-invoice-approvals"></a>Mobiele goed te keuren

Mobiele mogelijkheden in Microsoft Dynamics 365 for Operations kunnen een zakelijke gebruiker mobiele ervaringen ontwerpen. Voor geavanceerde scenario's, het platform we ook ontwikkelaars van de mogelijkheden als ze nodig hebt. De meest effectieve manier om te leren enkele van de nieuwe concepten van mobiele is het proces van het ontwerpen van een paar scenario's doorlopen. In dit onderwerp is bedoeld om een praktische aanpak voor het ontwerpen van mobiele scenario's door middel van leverancier goed te keuren voor mobiel gebruik kist bevatten. In dit onderwerp kunt u andere variaties van de scenario's ontwerpen en kan ook worden toegepast op andere scenario's die niet zijn gerelateerd aan facturen van leveranciers.

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                                                            | Omschrijving                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mobiele handbook vooraf gelezen                                                                                |(/ dynamics365/bewerkingen/dev-itpro/mobile-apps / mobile-platform.md)                                                                                                  |
| Dynamics 365 for Operations                                                                             | Een omgeving met Microsoft Dynamics 365 voor bewerkingen versie 1611 en Microsoft Dynamics voor bewerkingen platform bijwerken (November 2016) 3                   |
| Installeer hotfix KB 3204341.                                                                              | Taakregistratie kunt twee sluiten opdrachten voor vervolgkeuzelijst dialoogvensters die dit in Dynamics 365 voor bewerking platformupdate 3 (update November 2016 opgenomen) ten onrechte registreren |
| Installeer hotfix KB 3207800.                                                                              | Deze hotfix kunt bijlagen moeten worden weergegeven op de mobiele client die deze is opgenomen in Dynamics 365 voor bewerking platformupdate 3 (November 2016 update).           |
| Installeer hotfix KB 3208224.                                                                              | De toepassingscode voor de mobiele leverancier factuur aanvraag om goedkeuring die deze oplossing is opgenomen in Microsoft Dynamics AX application 7.0.1 (mei 2016).                          |
| Een Android of iOS of een Windows-apparaat met de mobiele toepassing geïnstalleerd voor Dynamics 365 for Operations | De app in de juiste app winkel zoekt.                                                                                                                     |

## <a name="introduction"></a>Introductie
Mobiele goedkeuringen voor leveranciersfacturen moeten de drie hotfixes die worden vermeld in de sectie 'Voorwaarden'. Deze hotfixes voorzien niet van een werkruimte voor het goed te keuren. Als u wilt weten wat een werkruimte is in de context van mobiele, lezen het mobiele handbook dat wordt vermeld in de sectie 'Vereisten'. De werkruimte van de goedkeuringen factuur moet zijn ontworpen. 

Elke organisatie orchestrates en zijn bedrijfsproces voor leveranciersfacturen anders definieert. Voordat u een mobiele ervaring voor leverancier goed te keuren ontwerpt, moet u rekening houden met de volgende aspecten van het bedrijfsproces. Het idee is om te gebruiken deze gegevenspunten zo veel mogelijk optimaliseren van de gebruikerservaring op het apparaat.

-   Welke velden uit de factuurkoptekst wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?
-   Welke velden op de factuurregels wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?
-   Het aantal factuurregels zijn er een factuur? Hier de 80-20-regel wordt toegepast en geoptimaliseerd voor de 80 procent.
-   Zal gebruikers wilt zien boekhoudingsverdelingen (factuur standaardproces) op het mobiele apparaat tijdens revisies? Als het antwoord op deze vraag Ja is, kunt u de volgende vragen:
    -   Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, worden opgesplitst, enzovoort) zijn er voor een factuurregel? De 80-20-regel opnieuw toepassen.
    -   De facturen ook hebt boekhoudingsverdelingen op de factuurkop? In dat geval moeten deze boekhoudingsverdelingen zijn beschikbaar op het apparaat?

> [!NOTE]
> In dit onderwerp hoe niet e boekhoudingsverdelingen bewerken omdat deze functie momenteel niet wordt ondersteund voor mobiele scenario's.

-   Gebruikers wilt Zie bijlagen voor de factuur op het apparaat?

Het ontwerp van de mobiele ervaring voor de goedkeuring van de factuur verschillen, afhankelijk van de antwoorden op deze vragen. Het doel is het optimaliseren van de gebruikerservaring voor het bedrijfsproces op mobile in een organisatie. In de rest van dit onderwerp, gaan we twee scenario variaties die zijn gebaseerd op verschillende antwoorden op de voorgaande vragen. 

Zorg dat u de wijzigingen verloren van de updates publiceren als een algemene richtlijn bij het werken met de ontwerper van de mobiele.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Een eenvoudige factuur goedkeuring scenario ontwerpen voor Contoso
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenariokenmerk</th>
<th>Beantwoorden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Welke velden uit de factuurkoptekst wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Leveranciernaam</li>
<li>Factuurtotaal</li>
<li>Te factureren rekening</li>
<li>Factuurnummer</li>
<li>Factuurdatum</li>
<li>Factuuromschrijving</li>
<li>Vervaldatum</li>
<li>Factuurvaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Welke velden op de factuurregels wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Inkoopcategorie</li>
<li>Hoeveelheid</li>
<li>Eenheidsprijs</li>
<li>Nettobedrag per regel</li>
<li>1099-bedrag</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het aantal factuurregels zijn er een factuur? Hier de 80-20-regel wordt toegepast en geoptimaliseerd voor de 80 procent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Zal gebruikers wilt zien boekhoudingsverdelingen (factuur standaardproces) op het mobiele apparaat tijdens revisies?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, enzovoort) zijn er voor een factuurregel? De 80-20-regel opnieuw toepassen.</td>
<td>Totaalprijs: 2 btw: toeslagen 0: 0</td>
</tr>
<tr class="even">
<td>De facturen ook hebt boekhoudingsverdelingen op de factuurkop? In dat geval moeten deze boekhoudingsverdelingen zijn beschikbaar op het apparaat?</td>
<td>Niet gebruikt</td>
</tr>
<tr class="odd">
<td>Gebruikers wilt Zie bijlagen voor de factuur op het apparaat?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>De werkruimte maken

1.  In een browser Dynamics 365 for Operations openen en inloggen.
2.  Nadat u bent aangemeld, toevoegen **& modus = mobiele** naar de URL, zoals weergegeven in het volgende voorbeeld en vernieuwt u de pagina: https://&lt;yoururl&gt;/? cmp = usmf & mi = DefaultDashboard**& modus = mobiele**
3.  Klik op de **instellingen** (versnelling)-knop in de rechterbovenhoek van de pagina en klik op **mobiele app**. De ontwerper van de mobiele app moet weergegeven.Net als taak recorder wordt weergegeven.
4.  Klik op **Add** om een nieuwe werkruimte te maken. De werkruimte voor dit voorbeeld de naam **Mijn goedkeuringen**.
5.  Voer een omschrijving in.
6.  Selecteer een kleur voor de werkruimte. De kleur van de werkruimte wordt gebruikt voor de algehele stijl van de mobiele ervaring voor deze werkruimte.
7.  Selecteer een pictogram voor de werkruimte.
8.  Klik op **uitgevoerd**
9.  Klik op **publiceren werkruimte** de wijzigingen wilt opslaan

### <a name="vendor-invoices-assigned-to-me"></a>Leveranciersfacturen die aan mij zijn toegewezen

De eerste mobile-pagina die u moet ontwerpen, is de lijst met facturen die zijn toegewezen aan de gebruiker voor beoordeling. Als u wilt deze mobiele pagina ontwerpt, gebruikt u de **VendMobileInvoiceAssignedToMeListPage** pagina in Dynamics 365 for Operations. Voordat u deze procedure hebt voltooid, controleert u of die ten minste één leveranciersfactuur ter beoordeling, aan u is toegewezen en dat de factuurregel twee verdelingen heeft. Deze instelling voldoet aan de vereisten voor dit scenario.

1.  Vervang in de Dynamics 365 voor bewerkingen URL, de naam van het menu-item met **VendMobileInvoiceAssignedToMeListPage** voor het openen van de mobiele versie van de **in behandeling zijnde leveranciersfacturen die aan mij toegewezen** lijstpagina in de **leveranciers** module. Afhankelijk van het aantal facturen die u hebt in uw systeem aan u toegewezen, wordt deze pagina voor de facturen weergeven. Ga voor een specifieke factuur, kunt u het filter aan de linkerkant. Echter niet een specifieke factuur is vereist voor dit voorbeeld. Sommige aan u toegewezen factuur zal kunt u de mobiele pagina is alleen vereist. De nieuwe pagina's die beschikbaar zijn zijn specifiek voor het ontwikkelen van mobiele scenario's voor leveranciersfactuur ontworpen. Daarom moet u deze pagina's gebruiken. De URL moet lijken op de volgende URL en nadat u deze hebt ingevoerd, de pagina die wordt weergegeven in de afbeelding moet worden weergegeven: https://&lt;yourURL&gt;/? cmp = usmf & mi =**VendMobileInvoiceAssignedToMeListPage**& modus = mobiele [![in behandeling zijnde leveranciersfacturen die aan mij toegewezen pagina](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
2.  Klik op de **instellingen** (versnelling)-knop in de rechterbovenhoek van de pagina en klik op **mobiele app**
3.  Selecteer uw werkruimte en klik op **bewerken**
4.  Klik op **pagina toevoegen** voor het maken van de eerste mobiele pagina.
5.  Voer een naam, zoals **mijn leveranciersfacturen**, en een omschrijving, zoals **ter controle aan mij toegewezen leveranciersfacturen**.
6.  Click **Done**.
7.  In de mobiele ontwerper van de **velden** en klik op **velden selecteren**. De kolommen op de lijstpagina moeten lijken op de volgende afbeelding. [![De pagina aan mij toegewezen kolommen op de in behandeling zijnde leveranciersfacturen](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
8.  De vereiste kolommen toevoegen vanuit de lijstpagina die moet worden weergegeven voor gebruikers in de mobiele pagina. De volgorde waarin u toevoegt, is de volgorde waarin de velden worden weergegeven voor de eindgebruiker. De enige manier om de volgorde van de velden wijzigen worden door alle velden te selecteren. Op basis van de vereisten voor dit scenario wordt zijn de volgende acht velden vereist. Echter, sommige gebruikers overwegen acht velden te veel informatie op een mobiel apparaat. Daarom zien we alleen de belangrijkste velden in de mobiele lijstweergave. De resterende velden worden weergegeven in de weergave van gegevens die wij later ontwikkelen. Op dit moment zullen we de volgende velden toevoegen. Klik op het plusteken (**+**) in deze kolommen toevoegen aan de mobiele pagina.
    1.  Leveranciernaam
    2.  Factuurtotaal
    3.  Te factureren rekening
    4.  Factuurnummer
    5.  Factuurdatum

    Nadat u de velden hebt toegevoegd, moet de volgende afbeelding lijkt op de mobiele pagina. [![Pagina nadat u velden hebt toegevoegd.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)
9.  U moet de volgende kolommen ook nu toevoegen, zodat we workflowacties later kunt inschakelen.
    1.  Taak voltooid weergeven
    2.  Gedelegeerde taak weergeven
    3.  Terughalen taak weergeven
    4.  Taak weigeren weergeven
    5.  Voltooiingstaak aanvraag weergeven
    6.  De taak opnieuw indienen weergeven

10. Klik op **doen** om af te sluiten van de bewerkingsmodus.
11. Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
12. Klik op **publiceren werkruimte** uw werk op te slaan.
13. Inschakelen **weergave factuurtotaal van in behandeling zijnde facturen lijst** in leveranciers parameterformulier onder **factuur**. Houd er rekening mee dat alleen door het inschakelen van deze parameter factuurtotalen wordt berekend op de lijstpagina met leveranciersfacturen in behandeling leverancier wordt weergegeven. Dit is een nieuwe mogelijkheid als onderdeel van de vooraf vereiste hotfix 3208224.

### <a name="vendor-invoice-details"></a>Factuurdetails van leverancier

Als u wilt de detailspagina voor de factuur voor mobiele ontwerpen, gebruiken de **VendMobileInvoiceHeaderDetails** pagina in Dynamics 365 voor bewerkingen. Houd er rekening mee dat, afhankelijk van het aantal facturen die u in uw systeem hebt, deze pagina ziet u de oudste factuur (de factuur die het eerst is gemaakt). Ga voor een specifieke factuur, kunt u het filter aan de linkerkant. Echter niet een specifieke factuur is vereist voor dit voorbeeld. Sommige factuurgegevens is alleen vereist zodat we de mobile-pagina kunt ontwerpen. [![Werkstroompagina](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1.  Vervang in de Dynamics 365 voor bewerkingen URL, de naam van het menu-item met **VendMobileInvoiceHeaderDetails** het formulier te openen
2.  Open de mobiele ontwerper van de **instellingen** knop (versnelling).
3.  Klik op de **bewerken** om de bewerkingsmodus start in de werkruimte.
4.  Selecteer de ** mijn leveranciersfacturen ** pagina dat u eerder hebt gemaakt en klik vervolgens op **bewerken**.
5.  Op de **velden** en klik op de **raster** kolomkop.
6.  Klik op **eigenschappen**&gt;**pagina toevoegen**. **opmerking:** wanneer u klikt op de **raster** voor koptekst en het toevoegen van een pagina, wordt de relatie met de details van de pagina wordt automatisch vastgesteld.
7.  Voer de titel van een pagina, zoals **factuurdetails**, en een omschrijving, zoals **koptekst en regeldetails weergeven**.
8.  Klik op **velden selecteren**. Houd er rekening mee dat de volgorde waarin u toevoegt is de volgorde waarin de velden worden weergegeven voor de eindgebruiker. De enige manier om de volgorde van de velden wijzigen worden door alle velden te selecteren.
9.  De volgende velden toevoegen vanuit de koptekst, op basis van de vereisten voor dit scenario:
    1.  Leveranciernaam
    2.  Factuurtotaal
    3.  Te factureren rekening
    4.  Factuurnummer
    5.  Factuurdatum
    6.  Factuuromschrijving
    7.  Vervaldatum
    8.  Factuurvaluta

10. De volgende velden uit het raster regels op de pagina toevoegen:
    1.  Inkoopcategorie
    2.  Hoeveelheid
    3.  Eenheidsprijs
    4.  Nettobedrag per regel
    5.  1099-bedrag

11. Nadat u alle velden uit de vorige twee stappen zijn toegevoegd, klikt u op **doen**. De pagina moet lijken op de volgende afbeelding. [![Pagina nadat u velden hebt toegevoegd.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)
12. Klik op **doen** om af te sluiten van de bewerkingsmodus.
13. Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
14. Klik op **publiceren werkruimte** uw werk op te slaan

### <a name="workflow-actions"></a>Workflowacties

Als workflowacties wilt toevoegen, gebruikt u de **VendMobileInvoiceHeaderDetails** pagina in Dynamics 365 voor bewerkingen. U opent deze pagina, vervangt u de naam van het menu-item in de URL, zoals u eerder hebt gedaan. Open vervolgens de mobiele ontwerper van de **instellingen** knop (versnelling). Volg deze stappen uit om workflowacties op de detailpagina.

1.  Klik op de **bewerken** om de bewerkingsmodus start in de werkruimte.
2.  Selecteer de **factuurdetails** up dat u eerder hebt gemaakt en klik op **bewerken**.
3.  Op de **acties** en klik op **actie toevoegen**.
4.  Voer de titel van een actie, zoals **goedkeuren**, en een omschrijving, zoals **goedkeuren factuur**. Houd er rekening mee dat de titel van de actie die u hier invoert, wordt de naam van de actie die wordt weergegeven aan de gebruiker in de mobiele toepassing.
5.  Click **Done**.
6.  Klik op **velden selecteren**.
7.  Het workflowproces doorlopen op de **VendMobileInvoiceHeaderDetails** pagina en vult u de actie die u wilt opnemen. Zorg dat u workflow opmerkingen tijdens dit proces invoeren, zodat een opmerkingenveld ook in de mobiele ervaring opgenomen is.
8.  Nadat u de workflowactie wordt uitgevoerd, klikt u op **doen** om de velden selecteren taak te voltooien.
9.  Klik op **doen** om af te sluiten van de bewerkingsmodus.
10. Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
11. Klik op **publiceren werkruimte** uw werk op te slaan
12. Herhaal de stappen 3 tot en met 11 om vast te leggen van de vereiste workflowacties. Houd er rekening mee dat een behoefte aan u toegewezen facturen die in staat om de workflowacties beschikbaar te maken die u ontwerpen wilt voor mogelijk is.
13. Open Kladblok of Microsoft Visual Studio en plak de volgende code. Sla het bestand als een JS-bestand. Deze code gebeuren twee dingen:
    1.  Hiermee knop verbergt u de extra workflow-gerelateerde kolommen die we eerder op de pagina mobiele lijst toegevoegd. We hebben deze kolommen toegevoegd zodat de toepassing die informatie in de context heeft en de volgende stap kunt doen.
    2.  Op basis van de werkstroomstap die actief is, deze logica voor het weergeven van alleen acties van toepassing.

Houd er rekening mee dat de naam van de pagina's en andere besturingselementen in de code JS hetzelfde uit de werkruimte moeten.

1.  Belangrijkste functie (metadataService, dataService, cacheService, $q) {retourneren {appInit: functie (appMetadata) {/ / verbergen van besturingselementen moeten metadataService.configureControl aanwezig, maar niet zichtbaar zijn (' Mijn--leveranciersfacturen, 'ShowAccept' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowApprove' {verborgen: true}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowReject' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowDelegate' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowRequestChange' {verborgen: true}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowRecall' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowComplete' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowResubmit' { verborgen: true}); }, pageInit: functie (pageMetadata, parameters) {als (pageMetadata.Name == factuur-details) {/ / workflowacties weergeven/verbergen op basis van workflow stap metadataService.configureAction ('Accepteren' {zichtbaar: waar}); metadataService.configureAction ('Goedkeuren' {zichtbaar: waar}); metadataService.configureAction ('Afwijzen' {zichtbaar: waar}); metadataService.configureAction ('Gemachtigde' {zichtbaar: true}); metadataService.configureAction (' wijziging aanvragen ', {zichtbaar: true}); metadataService.configureAction ('Intrekken' {zichtbaar: true}); metadataService.configureAction ('Volledig' {zichtbaar: true}); metadataService.configureAction ('Opnieuw indienen', {zichtbaar: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  De codebestand uploaden naar de werkruimte door te selecteren de **logica** tabblad
3.  Klik op **doen** om af te sluiten van de bewerkingsmodus.
4.  Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
5.  Klik op **publiceren werkruimte** uw werk op te slaan

### <a name="vendor-invoice-attachments"></a>Leverancier factuur bijlagen

1.  Klik op de **instellingen** (versnelling)-knop in de rechterbovenhoek van de pagina en klik op **mobiele app**
2.  Klik op de **bewerken** om de bewerkingsmodus start in de werkruimte.
3.  Selecteer de ** factuurdetails ** pagina dat u eerder hebt gemaakt en klik vervolgens op **bewerken**.
4.  Stel de **documentbeheer** optie aan **Ja** zoals hieronder wordt weergegeven. **opmerking:** als er geen vereisten moeten worden bijlagen weergegeven op het mobiele apparaat, kunt u deze optie instelt op **Nee**, de standaardinstelling.
5.  [![docmanagement](./media/docmanagement-216x300.png)](./media/docmanagement.png)
6.  Klik op **doen** om af te sluiten van de bewerkingsmodus.
7.  Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
8.  Klik op **publiceren werkruimte** uw werk op te slaan

### <a name="vendor-invoice-line-distributions"></a>Regel leveranciersfactuurverdelingen

De vereisten voor dit scenario bevestigen dat er worden alleen op regelniveau verdelingen en een factuur hebben altijd slechts één regel. Omdat dit scenario eenvoudig is, moet de gebruikerservaring op het mobiele apparaat ook zo eenvoudig is dat de gebruiker geen detailanalyse uitvoeren op verschillende niveaus voor de boekhoudingsverdelingen weergeven. Leveranciersfacturen in Dynamics 365 for Operations omvatten aangeven dat alle verdelingen uit de factuurkoptekst. Deze ervaring is wat we nodig hebben voor het mobiele scenario. Daarom gebruiken we de **VendMobileInvoiceAllDistributionTree** pagina voor het ontwerpen van dit deel van het mobiele scenario. 

> [!NOTE] 
> De vereisten weten helpt ons bepalen welke specifieke pagina wilt gebruiken en hoe helemaal gelijk aan het optimaliseren van de mobiele ervaring voor de gebruiker bij het ontwerp van het scenario. In het tweede scenario we gebruiken een andere pagina om weer te geven van de verdelingen, omdat de vereisten voor dat scenario verschillen.

1.  Vervang in de URL de naam van het menu-item als u hiervoor hebt gedaan. De volgende afbeelding ziet er dan de pagina die wordt weergegeven. [![Pagina voor alle verdelingen](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)
2.  Open de mobiele ontwerper van de **instellingen** knop (versnelling).
3.  Klik op de **bewerken** om de bewerkingsmodus start in de werkruimte. **opmerking:** ziet u dat twee nieuwe pagina's automatisch zijn gemaakt. Omdat u documentbeheer in de vorige sectie hebt ingeschakeld, maakt het systeem deze pagina's. Deze nieuwe pagina's, kunt u negeren.
4.  Klik op **pagina toevoegen**.
5.  Voer de titel van een pagina, zoals **weergave boekhouding**, en een omschrijving, zoals **boekhouding weergeven voor de factuur**.
6.  Click **Done**.
7.  Op de **velden** en klik op **velden selecteren**, selecteert u de volgende velden op de verdelingen-pagina en klik op **doen**:
    1.  Bedrag
    2.  Valuta
    3.  Grootboekrekening

> [!NOTE] 
> We hebt geselecteerd de **omschrijving** kolom uit het raster verdelingen omdat de vereisten voor dit scenario wordt bevestigd dat de totaalprijs is het enige bedrag dat zal er verdelingen voor. De gebruiker won't daarom een ander veld om te bepalen van het bedragsoort dat de verdeling is vereist. Echter, in het volgende scenario we **wordt** deze gegevens gebruiken, omdat de vereisten voor dat scenario opgeven dat andere typen bedrag verdelingen (bijvoorbeeld btw).
8.  Klik op **doen** om af te sluiten van de bewerkingsmodus.
9.  Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
10. Klik op **publiceren werkruimte** uw werk op te slaan

**opmerking:** de **weergave boekhouding** mobiele pagina momenteel niet is gekoppeld aan een van de mobiele pagina's die we tot nu toe hebt ontworpen. Omdat de gebruiker moet mogelijk zijn om te navigeren naar de **weergave boekhouding** pagina van de **factuurdetails** pagina op het mobiele apparaat moeten wij u navigatie in de **factuurdetails** pagina aan de **boekhouding weergeven** pagina. We maken deze navigatie met behulp van extra logica via JavaScript.

1.  Open het JS-bestand dat u eerder hebt gemaakt en de regels die zijn gemarkeerd in de volgende code toevoegen. Deze code gebeuren twee dingen:
    1.  Het helpt te garanderen dat gebruikers kunnen niet navigeren rechtstreeks vanuit de werkruimte aan de **weergave boekhouding** pagina.
    2.  Het vaststelt dat een navigatiebesturingselement van de **factuurdetails** pagina aan de **weergave boekhouding** pagina.

> [!NOTE] 
> De naam van de pagina's en andere besturingselementen in de code JS moeten hetzelfde uit de werkruimte.

1.  Belangrijkste functie (metadataService, dataService, cacheService, $q) {retourneren {appInit: functie (appMetadata) {/ / verbergen van besturingselementen moeten metadataService.configureControl aanwezig, maar niet zichtbaar zijn (' Mijn--leveranciersfacturen, 'ShowAccept' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowApprove' {verborgen: true}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowReject' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowDelegate' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowRequestChange' {verborgen: true}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowRecall' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowComplete' {verborgen: waar}); metadataService.configureControl (' Mijn--leveranciersfacturen, 'ShowResubmit' { verborgen: true}); Pagina's niet van toepassing voor hoofdmap navigatie metadataService.hideNavigation('View-accounting'); verbergen Koppeling naar metadataService.addLink voor boekhouding weergeven ('-factuurdetails, ' weergave boekhouding ', '-boekhouding-nav-weergavebesturingselement ","Boekhoudkundige weergeven", true); }, pageInit: functie (pageMetadata, parameters) {als (pageMetadata.Name == factuur-details) {/ / workflowacties weergeven/verbergen op basis van workflow stap metadataService.configureAction ('Accepteren' {zichtbaar: waar}); metadataService.configureAction ('Goedkeuren' {zichtbaar: waar}); metadataService.configureAction ('Afwijzen' {zichtbaar: waar}); metadataService.configureAction ('Gemachtigde' {zichtbaar: true}); metadataService.configureAction (' wijziging aanvragen ', {zichtbaar: true}); metadataService.configureAction ('Intrekken' {zichtbaar: true}); metadataService.configureAction ('Volledig' {zichtbaar: true}); metadataService.configureAction ('Opnieuw indienen', {zichtbaar: true});

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  De codebestand uploaden naar de werkruimte door te selecteren de **logica** tabblad kunt u de voorgaande code overschrijven
3.  Klik op **doen** om af te sluiten van de bewerkingsmodus.
4.  Klik op **terug** en vervolgens **doen** om af te sluiten van de werkruimte
5.  Klik op **publiceren werkruimte** uw werk op te slaan

### <a name="validation"></a>Validatie

Vanaf je mobiele telefoon, de app openen en verbinding maken met uw Dynamics 365 voor bewerkingen exemplaar. Zorg ervoor dat u zich aanmeldt op het bedrijf waar leveranciersfacturen ter controle aan u zijn toegewezen. U moet mogelijk zijn de volgende handelingen uitvoeren:

-   Zie de **Mijn goedkeuringen** werkruimte.
-   Inzoomen op de **Mijn goedkeuringen** voor samenwerking en Zie de **mijn leveranciersfacturen** pagina.
-   Inzoomen op de **mijn leveranciersfacturen** pagina en de lijst met facturen die aan u zijn toegewezen.
-   Inzoomen op een van de facturen en de factuurdetails koptekst en regeldetails bekijken.
-   Een koppeling naar de bijlagen op de detailpagina en gebruik van deze koppeling naar de lijst van bijlagen en de bijlagen weergeven.
-   Klik op de detailpagina ziet u een koppeling naar de **boekhouding weergeven** pagina en gebruik van deze koppeling om te navigeren naar de pagina verdelingen en de boekhoudingsverdelingen weergeven.
-   Klik op de detailpagina op de **acties** menu onder aan het en workflowacties uitvoeren die van toepassing op de werkstroomstap zijn.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Een scenario van de goedkeuring complexe factuur ontwerpen voor Fabrikam
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenariokenmerk</th>
<th>Beantwoorden</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Welke velden uit de factuurkoptekst wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Leveranciernaam</li>
<li>Factuurbedrag</li>
<li>Te factureren rekening</li>
<li>Factuurnummer</li>
<li>Factuurdatum</li>
<li>Factuuromschrijving</li>
<li>Vervaldatum</li>
<li>Factuurvaluta</li>
</ol></td>
</tr>
<tr class="even">
<td>Welke velden op de factuurregels wordt de gebruiker wilt zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Inkoopcategorie</li>
<li>Hoeveelheid</li>
<li>Eenheidsprijs</li>
<li>Nettobedrag per regel</li>
<li>1099-bedrag</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het aantal factuurregels zijn er een factuur? Hier de 80-20-regel wordt toegepast en geoptimaliseerd voor de 80 procent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Zal gebruikers wilt zien boekhoudingsverdelingen (factuur standaardproces) op het mobiele apparaat tijdens revisies?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, enzovoort) zijn er voor een factuurregel? De 80-20-regel opnieuw toepassen.</td>
<td>Totaalprijs: 2 btw: 2 toeslagen: 2</td>
</tr>
<tr class="even">
<td>De facturen ook hebt boekhoudingsverdelingen op de factuurkop? In dat geval moeten deze boekhoudingsverdelingen zijn beschikbaar op het apparaat?</td>
<td>Niet gebruikt</td>
</tr>
<tr class="odd">
<td>Gebruikers wilt Zie bijlagen voor de factuur op het apparaat?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="exercise"></a>Oefening

De volgende variaties kunnen worden uitgevoerd voor scenario 1, op basis van de vereisten voor scenario 2. Gebruik deze sectie als oefening die u kunt uitvoeren voor leermateriaal.

1.  Omdat u meer factuurregels worden verwacht in scenario 2, wordt de volgende wijzigingen in het ontwerp optimalisatie van de gebruikerservaring op het mobiele apparaat:
    1.  In plaats van factuurregels weergeven op de detailpagina (zoals in scenario 1), kunnen gebruikers kiezen regels wilt weergeven op een aparte mobiele pagina.
    2.  Omdat meer dan één factuurregel wordt verwacht in dit scenario is als de **VendMobileInvoiceAllDistributionTree** pagina wordt gebruikt voor het ontwerpen van de pagina verdelingen voor mobiele telefoons (zoals in scenario 1), kan dat verwarrend zijn voor de gebruiker om te relateren regels verdelingen. Gebruik daarom de **VendMobileInvoiceLineDistributionTree** pagina om de pagina verdelingen te ontwerpen.
    3.  In het ideale geval moeten de verdelingen worden weergegeven in de context van een factuurregel in dit scenario. Zorg er daarom voor dat de gebruiker een regel voor een overzicht van de pagina verdelingen kunt inzoomen. Gebruik de pagina koppeling mogelijkheid vast te stellen de detailanalyse,.Net als voor de kop- en pagina's in scenario 1.

2.  Omdat meer dan één bedragtype wordt verwacht voor de verdelingen in scenario 2 (btw, toeslagen, enzovoort), wordt het nuttig om weer te geven van de omschrijving van het bedragtype zijn. (We weggelaten deze informatie in scenario 1.)

## <a name="conclusion"></a>Conclusie
Het mobiele platform en de toepassingsmogelijkheden kunnen u mobiele scenario's die zijn geoptimaliseerd voor een gebruiker in een organisatie base ontwerpen. Op basis van de voorbeelden die in dit onderwerp worden geleverd, kunt u proberen andere varianten en maken van verschillende ervaringen die voldoen aan een specifieke behoefte.


