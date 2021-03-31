---
title: Mobiele factuurgoedkeuringen
description: Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: abf5c2735834537fdc72f2e73fe6a415bd1b67c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227517"
---
# <a name="mobile-invoice-approvals"></a>Mobiele factuurgoedkeuringen

[!include [banner](../includes/banner.md)]

Met de mobiele mogelijkheden kan een zakelijke gebruiker mobiele ervaringen ontwerpen. Voor geavanceerde scenario's kunnen ontwikkelaars met het platform de mogelijkheden desgewenst ook uitbreiden. De meest effectieve manier om een aantal van de nieuwe concepten over mobiele mogelijkheden te leren is het proces voor het ontwerpen van enkele scenario's te doorlopen. Dit onderwerp is bedoeld om een praktische aanpak te verschaffen voor het ontwerpen van mobiele scenario's door factuurgoedkeuringen van leveranciers voor mobiel gebruik als praktijkvoorbeeld te nemen. Aan de hand van dit onderwerp kunt u andere variaties van de scenario's ontwerpen en kunt u de informatie in dit onderwerp ook toepassen op andere scenario's die niet zijn gerelateerd aan facturen van leveranciers.

<a name="prerequisites"></a>Vereisten
-------------

| Vereiste                                                                                            | Omschrijving                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vooraf gelezen mobiel handboek                                                                                |[Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| Dynamics 365 Finance                                                                              | Een omgeving met versie 1611 en Platformupdate 3 (november 2016)                   |
| Installeer hotfix KB 3204341.                                                                              | Taakrecorder kan onterecht twee Sluiten-opdrachten voor vervolgkeuzelijstdialoogvensters registreren. Dit is opgenomen in Platformupdate 3 (update van november 2016). |
| Installeer hotfix KB 3207800.                                                                              | Met deze hotfix kunnen bijlagen worden weergegeven op de mobiele client. Dit is opgenomen in Platformupdate 3 (update van november 2016).           |
| Installeer hotfix KB 3208224.                                                                              | De toepassingscode voor de mobiele toepassing voor leveranciersfactuurgoedkeuring. Dit is opgenomen in versie 7.0.1 (mei 2016).                          |
| Een Android of iOS of een Windows-apparaat waarop de mobiele app is geïnstalleerd. | Zoek naar de app in de juiste store voor mobiele apps.                                                                                                                     |

## <a name="introduction"></a>Inleiding
Voor mobiele goedkeuringen van leveranciersfacturen zijn de drie hotfixes vereist die worden vermeld in de sectie 'Vereisten'. Deze hotfixes verschaffen geen werkgebied voor de factuurgoedkeuringen. Als u wilt weten wat een werkgebied is in de context van mobiel gebruik, leest u het mobiele handboek dat wordt vermeld in de sectie 'Vereisten'. Het werkgebied voor factuurgoedkeuringen moet worden ontworpen. 

Elke organisatie organiseert en definieert bedrijfsprocessen op een andere manier. Voordat u een mobiele ervaring voor leveranciersfactuurgoedkeuringen ontwerpt, moet u rekening houden met de volgende aspecten van het bedrijfsproces. Het idee is om deze gegevenspunten zo veel mogelijk te gebruiken om de gebruikerservaring op het apparaat te optimaliseren.

-   Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?
-   Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?
-   Hoeveel factuurregels bevat een factuur? Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.
-   Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles? Als het antwoord op deze vraag ja is, kunt u de volgende vragen overwegen:
    -   Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, opsplitsingen, enzovoort) zijn er voor een factuurregel? Pas de 80-20-regel opnieuw toe.
    -   Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst? In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?

    > [!NOTE]
    > In dit onderwerp wordt niet uitgelegd hoe boekhoudingsverdelingen kunnen worden bewerkt, omdat deze functionaliteit momenteel niet wordt ondersteund voor mobiele scenario's.

-   Willen gebruikers bijlagen voor de factuur op het apparaat zien?

Het ontwerp van de mobiele ervaring voor factuurgoedkeuringen verschilt, afhankelijk van de antwoorden op deze vragen. Het doel is de gebruikerservaring te optimaliseren voor het bedrijfsproces op mobiele apparaten in een organisatie. In de rest van dit onderwerp bekijken we twee scenariovariaties die zijn gebaseerd op verschillende antwoorden op de voorgaande vragen. 

Zorg er als algemene richtlijn voor dat u tijdens het werken met de mobiele ontwerper de wijzigingen ´publiceert´ om te voorkomen dat de updates verloren gaan.

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a>Een eenvoudig factuurgoedkeuringsscenario ontwerpen voor Contoso
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
<td>Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</td>
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
<td>Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Inkoopcategorie</li>
<li>Hoeveelheid</li>
<li>Eenheidsprijs</li>
<li>Nettobedrag per regel</li>
<li>1099-bedrag</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hoeveel factuurregels bevat een factuur? Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</td>
<td>1</td>
</tr>
<tr class="even">
<td>Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel? Pas de 80-20-regel opnieuw toe.</td>
<td>Totaalprijs: 2 btw: 0 toeslagen: 0</td>
</tr>
<tr class="even">
<td>Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst? In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</td>
<td>Niet gebruikt</td>
</tr>
<tr class="odd">
<td>Willen gebruikers bijlagen voor de factuur op het apparaat zien?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a>Het werkgebied maken

1.  In een browser en meld u aan bij de-toepassing.
2.  Nadat u bent aangemeld, voegt u **&mode=mobile** toe aan de URL, zoals weergegeven in het volgende voorbeeld, en vernieuwt u de pagina: https://&lt;yoururl&gt;/? cmp=usmf&mi=DefaultDashboard **&mode=mobile**
3.  Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**. De ontwerper van de mobiele app moet worden weergegeven meteen wanneer de taakrecorder verschijnt.
4.  Klik op **Toevoegen** om een nieuw werkgebied te maken. Geef voor dit voorbeeld het werkgebied de naam **Mijn goedkeuringen**.
5.  Voer een omschrijving in.
6.  Selecteer een werkgebiedkleur. De kleur van het werkgebied wordt gebruikt voor de algemene stijl van de mobiele ervaring voor dit werkgebied.
7.  Selecteer een pictogram voor het werkgebied.
8.  Klik op **Gereed**.
9.  Klik op **Werkgebied publiceren** om de wijzigingen op te slaan.

### <a name="vendor-invoices-assigned-to-me"></a>Leveranciersfacturen die aan mij zijn toegewezen

De eerste mobiele pagina die u moet ontwerpen, is de lijst met facturen die ter beoordeling zijn toegewezen aan de gebruiker. Als u deze mobiele pagina wilt ontwerpen, gebruikt u de pagina **VendMobileInvoiceAssignedToMeListPage**. Voordat u deze procedure voltooit, controleert u of er ten minste één leveranciersfactuur ter beoordeling aan u is toegewezen en of de factuurregel twee verdelingen heeft. Deze instelling voldoet aan de vereisten voor dit scenario.

1.  Vervang in de URL de naam van de menuoptie door **VendMobileInvoiceAssignedToMeListPage** om de mobiele versie van de lijstpagina **Aan mij toegewezen leveranciersfacturen in behandeling** in de module **Leveranciers** te openen. Afhankelijk van het aantal facturen dat in uw systeem aan u is toegewezen, worden op deze pagina deze facturen weergegeven. Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken. Voor dit voorbeeld is echter geen specifieke factuur vereist. Er moet alleen een bepaalde factuur aan u zijn toegewezen op basis waarvan u de mobiele pagina kunt ontwerpen. De nieuwe pagina's die beschikbaar zijn, zijn specifiek ontworpen voor het ontwikkelen van mobiele scenario's voor leveranciersfacturen. Daarom moet u deze pagina's gebruiken. De URL moet lijken op de volgende URL en nadat u deze hebt ingevoerd, moet de pagina die wordt weergegeven in de afbeelding verschijnen: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile 

    [![Pagina Aan mij toegewezen leveranciersfacturen in behandeling](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)
    
2.  Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.
3.  Selecteer uw werkgebied en klik op **Bewerken**
4.  Klik op **Pagina toevoegen** voor het maken van de eerste mobiele pagina.
5.  Voer een naam in, zoals **Mijn leveranciersfacturen**, en een omschrijving, zoals **Ter controle aan mij toegewezen leveranciersfacturen**.
6.  Klik op **Gereed**.
7.  Klik in de mobiele ontwerper op het tabblad **Velden** op **Velden selecteren**. De kolommen op de lijstpagina moeten lijken op de volgende afbeelding. 

    [![Kolommen op de pagina In behandeling zijnde leveranciersfacturen die aan mij zijn toegewezen](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)
    
8.  Voeg de vereiste kolommen toe vanuit de lijstpagina die moet worden weergegeven voor de gebruikers op de mobiele pagina. De volgorde waarin u toevoegt, is de volgorde waarin de velden worden weergegeven voor de eindgebruiker. De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren. Op basis van de vereisten voor dit scenario zijn de volgende acht velden vereist. Sommige gebruikers vinden mogelijk dat acht velden te veel informatie is voor een mobiel apparaat. Daarom laten we alleen de belangrijkste velden in de mobiele lijstweergave zien. De resterende velden worden weergegeven in de detailweergave die wij later ontwerpen. Op dit moment voegen we de volgende velden toe. Klik op het plusteken (**+**) in deze kolommen om aan de mobiele pagina toe te voegen.
    - Leveranciernaam
    - Factuurtotaal
    - Te factureren rekening
    - Factuurnummer
    - Factuurdatum

    Nadat u de velden zijn toegevoegd, moet de mobiele pagina lijken op de volgende afbeelding. 
    
    [![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)

9.  U moet de volgende kolommen nu ook toevoegen, zodat we workflowacties later kunnen inschakelen.
    - Voltooide taak weergeven
    - Gedelegeerde taak weergeven
    - Teruggeroepen taak weergeven
    - Geweigerde taak weergeven
    - Voltooiingstaak aanvraag weergeven
    - Herindieningstaak weergeven

10. Klik op **Gereed** om de bewerkingsmodus af te sluiten.
11. Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten
12. Klik op **Werkgebied publiceren** om uw werk op te slaan.
13. Schakel **Factuurtotaal in lijst met in behandeling zijnde leveranciersfacturen weergeven** in het formulier voor leveranciersparameterformulier in onder **Factuur**. Houd er rekening mee dat alleen door het inschakelen van deze parameter factuurtotalen worden berekend voor weergave op de lijstpagina met in behandeling zijnde leveranciersfacturen. Dit is een nieuwe mogelijkheid als onderdeel van de vereiste hotfix 3208224.

### <a name="vendor-invoice-details"></a>Details leveranciersfactuur

Als u de pagina met factuurdetails wilt inschakelen voor mobiele apparaten, gebruikt u de pagina **VendMobileInvoiceHeaderDetails**. Houd er rekening mee dat, afhankelijk van het aantal facturen dat u in uw systeem hebt, op deze pagina de oudste factuur (de factuur die het eerst is gemaakt) wordt weergegeven. Als u op zoek bent naar een specifieke factuur, kunt u het filter aan de linkerkant gebruiken. Voor dit voorbeeld is echter geen specifieke factuur vereist. We hebben slechts enkele factuurgegevens nodig zodat we de mobiele pagina kunnen ontwerpen. 

[![Pagina Workflow](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)

1. Vervang in de URL de naam van de menuoptie met **VendMobileInvoiceHeaderDetails** om het formulier te openen

2. Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).

3. Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.

4. Selecteer de pagina **Mijn leveranciersfacturen** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.

5. Klik op het tabblad **Velden** op de kolomkop **Raster**.

6. Klik op **Eigenschappen &gt; Pagina toevoegen**. **Opmerking:** wanneer u klikt op de kop **Raster** en een pagina toevoegt, wordt de relatie met de detailpagina automatisch ingesteld.

7. Voer een paginatitel in, zoals **Factuurdetails**, en een omschrijving, zoals **Koptekst- en regeldetails factuur weergeven**.

8. Klik op **Velden selecteren**. Houd er rekening mee dat de volgorde waarin u toevoegt, de volgorde is waarin de velden worden weergegeven voor de eindgebruiker. De enige manier om de volgorde van de velden te wijzigen is door alle velden opnieuw te selecteren. 

9. Op basis van de vereisten voor dit scenario voegt u de volgende velden uit de koptekst toe:
   - Leveranciernaam
   - Factuurtotaal
   - Te factureren rekening
   - Factuurnummer
   - Factuurdatum
   - Factuuromschrijving
   - Vervaldatum
   - Factuurvaluta

10. Voeg de volgende velden uit het regelraster op de pagina toe:
    - Inkoopcategorie
    - Hoeveelheid
    - Eenheidsprijs
    - Nettobedrag per regel
    - 1099-bedrag

11. Nadat alle velden uit de vorige twee stappen zijn toegevoegd, klikt u op **Gereed**. De pagina moet lijken op de volgende afbeelding.
    
    [![Pagina nadat velden zijn toegevoegd.](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)

12. Klik op **Gereed** om de bewerkingsmodus af te sluiten.

13. Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten

14. Klik op **Werkgebied publiceren** om uw werk op te slaan.

### <a name="workflow-actions"></a>Workflowacties

Voeg workflowacties toe met de pagina **VendMobileInvoiceHeaderDetails**. Als u deze pagina wilt openen, vervangt u de naam van de menuoptie in de URL, zoals u eerder hebt gedaan. Open de mobiele ontwerper vervolgens met de knop **Instellingen** (tandwiel). Voer de volgende stappen uit om workflowacties op de detailpagina toe te voegen. Er moeten dus facturen aan u zijn toegewezen die de correcte status hebben, zodat de workflowacties beschikbaar voor u kunnen worden gemaakt waarvoor u een ontwerp gaat ontwikkelen.

#### <a name="record-workflow-actions"></a>Workflowacties opnemen
1.  Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.
2.  Selecteer de pagina **Factuurdetails** die u eerder hebt gemaakt en klik vervolgens op **Bewerken**.
3.  Klik op het tabblad **Acties** op **Actie toevoegen**.
4.  Voer een actietitel in, zoals **Goedkeuren**, en een omschrijving, zoals **Factuur goedkeuren**. Houd er rekening mee dat de titel van de actie die u hier invoert, de naam wordt van de actie die wordt weergegeven aan de gebruiker in de mobiele toepassing.
5.  Klik op **Gereed**.
6.  Klik op **Velden selecteren**.
7.  Doorloop het workflowproces op de pagina **VendMobileInvoiceHeaderDetails** en voer de actie uit die u wilt registreren. Zorg dat u workflowopmerkingen tijdens dit proces invoert, zodat er ook een veld met opmerkingen in de mobiele ervaring wordt opgenomen.
8.  Nadat de workflowactie is uitgevoerd, klikt u op **Gereed** om de taak Velden selecteren te voltooien.
9.  Klik op **Gereed** om de bewerkingsmodus af te sluiten.
10. Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten
11. Klik op **Werkgebied publiceren** om uw werk op te slaan.
12. Herhaal de vorige stappen om alle vereiste workflowacties te registreren. 

#### <a name="create-a-js-file"></a>Een js-bestand maken.
1. Open Kladblok of Microsoft Visual Studio en plak de volgende code. Sla het rapport als een .js-bestand op. Deze code voert het volgende uit:
    - De extra workflowgerelateerde kolommen worden verborgen die we eerder op de mobiele lijstpagina hebben toegevoegd. We hebben deze kolommen toegevoegd zodat de app die informatie in context heeft en de volgende stap kan worden uitgevoerd.
    - Op basis van de workflowstap die actief is, wordt deze logica toegepast om slechts twee acties weer te geven.

    > [!NOTE]
    > De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```

2.  Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren
3.  Klik op **Gereed** om de bewerkingsmodus af te sluiten.
4.  Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten
5.  Klik op **Werkgebied publiceren** om uw werk op te slaan.

### <a name="vendor-invoice-attachments"></a>Leveranciersfactuurbijlagen

1. Klik op de knop **Instellingen** (tandwiel) in de rechterbovenhoek van de pagina en klik op **Mobiele app**.

2. Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten.

3. Selecteer de pagina <strong>Factuurdetails** die u eerder hebt gemaakt en klik vervolgens op **Bewerken</strong>.

4. Stel de optie **Documentbeheer** in op **Ja** zoals hieronder wordt weergegeven. **Opmerking:** als er geen vereisten zijn om bijlagen weer te geven op het mobiele apparaat, kunt u deze optie ingesteld laten op **Nee**. Dit is de standaardinstelling.
   
   ![Documentbeheer](./media/docmanagement-216x300.png)

5. Klik op **Gereed** om de bewerkingsmodus af te sluiten.

6. Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten

7. Klik op **Werkgebied publiceren** om uw werk op te slaan.

### <a name="vendor-invoice-line-distributions"></a>Leveranciersfactuurregelverdelingen

Met vereisten voor dit scenario wordt bevestigd dat er alleen verdelingen op regelniveau zijn en dat een factuur altijd slechts één regel heeft. Omdat dit scenario eenvoudig is, moet de gebruikerservaring op het mobiele apparaat ook zo eenvoudig zijn dat de gebruiker geen detailanalyse hoeft uit te voeren op verschillende niveaus om de verdelingen weer te geven. Leveranciersfacturen hebben ook de optie om alle verdelingen uit de factuurkoptekst weer te geven. Deze ervaring is wat we nodig hebben voor het mobiele scenario. Daarom gebruiken we de pagina **VendMobileInvoiceAllDistributionTree** om dit deel van het mobiele scenario te ontwerpen. 

> [!NOTE] 
> Op basis van de vereisten kunnen we bepalen welke specifieke pagina moet worden gebruikt en hoe de mobiele ervaring exact moet worden geoptimaliseerd voor de gebruiker bij het ontwerp van het scenario. In het tweede scenario gebruiken we een andere pagina om de verdelingen weer te geven, omdat de vereisten voor dat scenario verschillen.

1.  Vervang in de URL de naam van de menuoptie, zoals u eerder hebt gedaan. De pagina die verschijnt, moet lijken op de volgende afbeelding.

    [![Pagina Alle verdelingen](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)

2.  Open de mobiele ontwerper met de knop **Instellingen** (tandwiel).

3.  Klik op de knop **Bewerken** om de bewerkingsmodus in het werkgebied te starten. **Opmerking:** u ziet dat er automatisch twee nieuwe pagina's zijn gemaakt. Omdat u documentbeheer in het vorige gedeelte hebt ingeschakeld, worden deze pagina's gemaakt. U kunt deze nieuwe pagina's negeren.

4.  Klik op **Pagina toevoegen**.

5.  Voer een paginatitel in, zoals **Boekhouding weergeven**, en een omschrijving, zoals **Boekhouding weergeven voor de factuur**.

6.  Klik op **Gereed**.

7.  Selecteer op het tabblad **Velden** **Velden selecteren**, selecteer de volgende velden op de pagina Verdelingen en klik op **Gereed**:
    1.  Bedrag
    2.  Valuta
    3.  Grootboekrekening

    > [!NOTE] 
    > We hebben de kolom **Omschrijving** uit het raster Verdelingen niet geselecteerd, omdat de vereisten voor dit scenario hebben bevestigd dat de totaalprijs het enige bedrag is waarvoor er verdelingen zijn. De gebruiker heeft daarom geen ander veld nodig om het bedragtype te bepalen waarvoor de verdeling is bestemd. In het volgende scenario gebruiken we echter deze gegevens **wel**, omdat de vereisten voor dat scenario aangeven dat andere bedragtypen verdelingen hebben (bijvoorbeeld btw).

8.  Klik op **Gereed** om de bewerkingsmodus af te sluiten.

9.  Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten

10. Klik op **Werkgebied publiceren** om uw werk op te slaan.

#### <a name="adding-navigation-to-view-accounting-page"></a>Navigatie toevoegen aan de pagina 'Boekhouding weergeven'

De mobiele pagina **Boekhouding weergeven** is nu nog niet gekoppeld aan een van de mobiele pagina's die we tot nu toe hebben ontworpen. Omdat de gebruiker moet kunnen navigeren naar de pagina **Boekhouding weergeven** van de pagina **Factuurdetails** op het mobiele apparaat, moeten wij navigatie verschaffen vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**. We stellen deze navigatie in met behulp van aanvullende logica via JavaScript.

1.  Open het .js-bestand dat u eerder hebt gemaakt en voeg de regels toe die in de volgende code zijn gemarkeerd. Deze code doet twee dingen:
    1.  Dit helpt te garanderen dat gebruikers niet rechtstreeks van het werkgebied naar de pagina **Boekhouding weergeven** kunnen navigeren.
    2.  Er wordt een navigatiebesturingselement ingesteld vanaf de pagina **Factuurdetails** naar de pagina **Boekhouding weergeven**.

    > [!NOTE] 
    > De namen van pagina's en andere besturingselementen in de code moet hetzelfde zijn als de namen in het werkgebied.

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

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
    ```
    
2.  Het codebestand uploaden naar het werkgebied door het tabblad **Logica** te selecteren om de vorige code te overschrijven
3.  Klik op **Gereed** om de bewerkingsmodus af te sluiten.
4.  Klik op **Terug** en vervolgens op **Gereed** om het werkgebied af te sluiten
5.  Klik op **Werkgebied publiceren** om uw werk op te slaan.

### <a name="validation"></a>Validatie

Open op uw mobiele apparaat de app en maak verbinding met uw exemplaar. Zorg ervoor dat u zich aanmeldt bij het bedrijf waar leveranciersfacturen ter controle aan u zijn toegewezen. U moet de volgende acties kunnen uitvoeren:

-   Zie het werkgebied **Mijn goedkeuringen**.
-   Zoom in op het werkgebied **Mijn goedkeuringen** en bekijk de pagina **Mijn leveranciersfacturen**.
-   Zoom in op de pagina **Mijn leveranciersfacturen** en bekijk de lijst met facturen die aan u zijn toegewezen.
-   Zoom in op een van de facturen en bekijk de factuurkoptekstdetails en de factuurregeldetails.
-   Bekijk op de detailpagina een koppeling naar bijlagen en gebruik deze koppeling om naar de lijst met bijlagen te navigeren en de bijlagen weer te geven.
-   Bekijk op de detailpagina een koppeling naar de pagina **Boekhouding weergeven** en gebruik deze koppeling om naar de pagina met verdelingen te navigeren en geef de verdelingen weer.
-   Klik op de detailpagina op het menu **Acties** onderaan en voer workflowacties uit die van toepassing op de workflowstap zijn.

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a>Een complex factuurgoedkeuringsscenario ontwerpen voor Fabrikam
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
<td>Welke velden uit de factuurkoptekst wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</td>
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
<td>Welke velden uit de factuurregels wil de gebruiker zien in de mobiele ervaring en in welke volgorde?</td>
<td><ol>
<li>Inkoopcategorie</li>
<li>Hoeveelheid</li>
<li>Eenheidsprijs</li>
<li>Nettobedrag per regel</li>
<li>1099-bedrag</li>
</ol></td>
</tr>
<tr class="odd">
<td>Hoeveel factuurregels bevat een factuur? Pas hier de 80-20-regel toe en optimaliseer voor 80 procent.</td>
<td>5</td>
</tr>
<tr class="even">
<td>Willen gebruikers boekhoudingsverdelingen (factuurcodering) op het mobiele apparaat zien tijdens controles?</td>
<td>Ja</td>
</tr>
<tr class="odd">
<td>Hoeveel boekhoudingsverdelingen (totaalprijs, btw, toeslagen, toeslagen, enzovoort) zijn er voor een factuurregel? Pas de 80-20-regel opnieuw toe.</td>
<td>Totaalprijs: 2 btw: 2 toeslagen: 2</td>
</tr>
<tr class="even">
<td>Bevatten de facturen ook boekhoudingsverdelingen in de factuurkoptekst? In dat geval moeten deze boekhoudingsverdelingen dan beschikbaar zijn op het apparaat?</td>
<td>Niet gebruikt</td>
</tr>
<tr class="odd">
<td>Willen gebruikers bijlagen voor de factuur op het apparaat zien?</td>
<td>Ja</td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a>Volgende stappen

De volgende variaties kunnen worden uitgevoerd voor scenario 1, op basis van de vereisten voor scenario 2. U kunt deze sectie gebruiken om de ervaring in uw mobiele app te verbeteren.

1.  Omdat er meer factuurregels worden verwacht in scenario 2, helpen de volgende wijzigingen in het ontwerp de gebruikerservaring op het mobiele apparaat te optimaliseren:
    1.  In plaats van factuurregels weer te geven op de detailpagina (zoals in scenario 1), kunnen gebruikers ervoor kiezen regels op een aparte mobiele pagina weer te geven.
    2.  Omdat meer dan één factuurregel wordt verwacht in dit scenario als de pagina **VendMobileInvoiceAllDistributionTree** wordt gebruikt voor het ontwerpen van de pagina Verdelingen voor mobiele apparaten (zoals in scenario 1), kan dat verwarrend zijn voor de gebruiker om regels te relateren aan verdelingen. Gebruik daarom de pagina **VendMobileInvoiceLineDistributionTree** om de pagina Verdelingen te ontwerpen.
    3.  In het ideale geval moeten de verdelingen worden weergegeven in de context van een factuurregel in dit scenario. Zorg er daarom voor dat de gebruiker kan inzoomen op een regel om de pagina Verdelingen te bekijken. Gebruik de paginakoppelingmogelijkheid om het inzoomen in te stellen, net als u voor de koptekst en detailpagina's in scenario 1 hebt gedaan.

2.  Omdat meer dan één bedragtype wordt verwacht voor de verdelingen in scenario 2 (btw, toeslagen, enzovoort), is het nuttig om de omschrijving van het bedragtype weer te geven. (We hebben deze informatie in scenario 1 weggelaten.)






[!INCLUDE[footer-include](../../includes/footer-banner.md)]