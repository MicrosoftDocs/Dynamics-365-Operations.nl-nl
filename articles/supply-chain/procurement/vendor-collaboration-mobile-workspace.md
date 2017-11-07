---
title: Mobiel werkgebied Leverancierssamenwerking
description: In dit onderwerp vindt u informatie over het mobiele werkgebied Leverancierssamenwerking. Met dit werkgebied kunnen uw leveranciers op de hoogte blijven van de inkooporders die aan hen zijn verzonden voor goedkeuring. Ze zien hier ook informatie over nieuwe en bijgewerkte inkooporders en contactpersonen.
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: d9dfd987aa81b9537bc05715eb85b5285b61b5cf
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-collaboration-mobile-workspace"></a>Mobiel werkgebied Leverancierssamenwerking

[!include[banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over het mobiele werkgebied **Leverancierssamenwerking**. Met dit werkgebied kunnen uw leveranciers op de hoogte blijven van de inkooporders die aan hen zijn verzonden voor goedkeuring. Ze zien hier ook informatie over nieuwe en bijgewerkte inkooporders en contactpersonen.

Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Overzicht 
Het mobiele werkgebied **Leverancierssamenwerking** informeert leveranciers over nieuwe inkooporders, zodat ze inkooporders kunnen zien en erop reageren in de webclient van Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. 

>[!NOTE]
> Het mobiele werkgebied moet worden gebruikt als aanvulling op de webinterface voor leverancierssamenwerking, niet als vervanging daarvan. 

Uw leveranciers kunnen het mobiele werkgebied **Leverancierssamenwerking** nieuwe inkooporders weergeven die naar hen worden verzonden voor goedkeuring. Hierin worden inkoopordergegevens weergegeven, zoals producten, hoeveelheden en aangevraagde leverdatums. Afhankelijk van de configuratie van de leverancier is ook prijsinformatie beschikbaar. 

Wanneer een gebruiker zich als een leverancier aanmeldt, ziet hij op welke inkooporders is gereageerd en welke inkooporders nog wachten op actie van de klant. Een inkooporder kan bijvoorbeeld nog wachten op actie door de klant, omdat de leverancier een andere leveringsdatum heeft voorgesteld die niet nog door de klant is geaccepteerd. De leverancier krijgt ook een overzicht te zien van de inkooporders die zijn bevestigd, maar nog niet zijn geleverd. 

Om te reageren op een inkooporder moet de leverancier de webinterface voor leverancierssamenwerking gebruiken die beschikbaar is in de webclient. Daar vindt de leverancier ook meer informatie over de order, zoals documentbijlagen, het afleveradres per regel en toeslagen die gerelateerd zijn aan de leverancier. 

Leveranciers met een speciale beveiligingsrol kunnen zien welke contactpersonen zijn geregistreerd voor een leveranciersaccount. Met dezelfde beveiligingsrol kan de leverancier ook de status zien van alle gebruikersaanvragen die zijn ingediend. 

De webinterface voor leverancierssamenwerking in de webclient moet worden gebruikt om nieuwe contactpersonen aan te maken en aanvragen voor nieuwe gebruikers in te dienen. 

In het werkgebied **Leverancierssamenwerking** kan een leverancier deze taken uitvoeren:

-   Nieuwe inkooporders bekijken die aan de leverancier zijn verzonden.
-   Inkooporders weergeven waarop de leverancier heeft gereageerd op en die wachten op actie van de klant.
-   Inkooporders weergeven die zijn bevestigd maar nog niet volledig zijn ontvangen.
-   Informatie weergeven over contactpersonen die zijn geregistreerd voor de leveranciersaccount. (Deze taak vereist een aanvullende beveiligingsrol)
-   Informatie weergeven voor en de status volgen van een gebruikersaanvraag die is ingediend door de leverancier. (Deze taak vereist een aanvullende beveiligingsrol)

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 for Finance and Operations die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Vereisten als u Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) gebruikt 
Als Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Leverancierssamenwerking** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Vereisten voor gebruik van Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger.
Als Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren. 

<table>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 3216943 moet worden geïmplementeerd als u platformupdate 3 gebruikt.</td>
<td>Systeembeheerder</td>
<td>KB 3216943 is een binaire update die is vereist als u platformupdate 3 gebruikt. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van deze KB.
<ol>
<li>KB 3216943 downloaden van Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>De binaire update installeren, die als een implementeerbaar pakket is geleverd. Zie voor informatie over het toepassen van een implementeerbaar pakket <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Een implementeerbaar pakket toepassen</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>KB 4013633 moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>KB 4013633 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Voorhanden voorraad</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">De metagegevens-hotfix downloaden vanuit LCS</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>
</ol></td>
</tr>
<tr class="odd">
<td>Het mobiele werkgebied <strong>Leverancierssamenwerking</strong> moet worden gepubliceerd.</td><td>Systeembeheerder</td>
<td>Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
<tr class="even">
<td>De leveranciersgebruiker moet toegang hebben tot de webinterface voor leverancierssamenwerking in de webclient en een gebruiker voor leverancierssamenwerking instellen.</td><td>Inkopers en de systeembeheerder</td>
<td>Volg de stappen in de volgende onderwerpen om de webinterface voor leverancierssamenwerking in te stellen en ermee te werken.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Leverancierssamenwerking voor het werken met externe leveranciers</a></li>
<li><a href="manage-vendor-collaboration-users.md">Gebruikers van leverancierssamenwerking beheren</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Samenwerking met leveranciers instellen en onderhouden</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Leverancierssamenwerking voor het werken met klanten in Finance and Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Dynamics 365 for Unified Operations:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1.  Start de app op uw mobiele apparaat.
2.  Voer uw Microsoft Dynamics 365-URL in.
4.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
5.  Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

    [![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Het mobiele werkgebied Leverancierssamenwerking gebruiken
Wanneer u het werkgebied **Leverancierssamenwerking** selecteert, ziet u de volgende opties.

![Mobiel werkgebied Leverancierssamenwerking](./media/vendor-collaboration-mobile-app.png)

Het werkgebied **Leverancierssamenwerking** bevat de volgende pagina's.

### <a name="contacts"></a>Contacten
Op de pagina **Contactpersonen** ziet u alle contactpersonen die zijn ingesteld voor de leveranciersaccount. Hier ziet u de naam, het primaire e-mailadres van de contactpersoon en diens gebruikersalias, als de contactpersoon een alias heeft. Op deze pagina wordt ook aangegeven of de gebruikersaccount van de contactpersoon actief is. Wanneer u een contactpersoon selecteert, ziet u contactgegevens zoals de rechtspersonen waarvoor de persoon dient als contactpersoon. U ziet ook contactgegevens, zoals een telefoonnummer of een alternatief e-mailadres.

### <a name="user-requests"></a>Gebruikersaanvragen
Op de pagina **Gebruikersaanvragen** kunt u alle gebruikersaanvragen zien die u hebt ingediend via de webinterface voor leverancierssamenwerking en de status ervan volgen. U kunt ook de status van die aanvragen volgen. Wanneer u een gebruikersaanvraag selecteert, ziet u wat is aangevraagd, een gebruiker toevoegen of deactiveren, de beveiliging wijzigen en zien welke beveiligingsrollen zijn aangevraagd voor de gebruiker.

### <a name="purchase-orders-ready-for-review"></a>Inkooporders ter beoordeling
Op de pagina **Inkooporders ter beoordeling** kunt u alle inkooporders zien die zijn verzonden door de klant en waarop nog niet is gereageerd. U kunt geselecteerde informatie weergeven over de verkooporder, zoals welke producten zijn aangevraagd en wanneer deze producten moeten worden geleverd. Afhankelijk van de configuratie van de leverancier is ook prijsinformatie beschikbaar.

U kunt ook zien of de inkooporder notities of bijlagen heeft. Om notities en bijlagen te openen, moet u echter de webinterface voor leverancierssamenwerking in de webclient gebruiken. Selecteer **Inkooporderregel** om alle regels samen met details weer te geven. Bij elke regel geeft een indicator aan of er notities of bijlagen zijn, of dat het afleveradres afwijkt van het adres dat in de koptekst wordt weergegeven.

Om te reageren op de inkooporder moet u de webinterface voor leverancierssamenwerking in de webclient gebruiken.

### <a name="awaiting-customer-action"></a>In afwachting van actie van klant
Op de pagina **In afwachting van actie van klant** kunt u zoeken naar inkoopopdrachten waarop u of iemand anders in uw bedrijf met toegang tot leverancierssamenwerking heeft gereageerd. De inkooporders zijn alleen zichtbaar in deze lijst als de klant een van de volgende acties moet uitvoeren op de inkooporder:

-   Als de inkooporder is afgewezen, moet de klant de oorspronkelijke order bijwerken of annuleren en deze dan opnieuw verzenden. Nadat de inkooporder opnieuw is verzonden, is hij niet meer zichtbaar op de pagina **In afwachting van actie van klant**.
-   Als de inkooporder is geaccepteerd met wijzigingen, moet de klant de oorspronkelijke order bijwerken en opnieuw verzenden ter beoordeling, of de order bijwerken op basis van de aangevraagde wijzigingen en onmiddellijk bevestigen. In beide gevallen wordt de inkooporder verwijderd van de pagina **In afwachting van actie van klant**.
-   Als de inkooporder is geaccepteerd en nog steeds wordt weergegeven op de pagina **In afwachting van actie van klant**, komt dat doordat de inkooporder niet automatisch werd bevestigd bij acceptatie. Hij wacht nu erop dat een inkoper de orderstatus wijzigt in **Bevestigd**. Normaal gesproken wordt de inkooporder beschouwd als een overeenkomst tussen de klant en de leverancier, zodra de leverancier de order accepteert. Daarom is de update naar de status **Bevestigd** meestal alleen een formaliteit.

Als u een inkooporder selecteert, worden aanvullende gegevens voor de reactie weergegeven. U kunt de regeldetails en het antwoord voor elke regel bekijken. De regelstatus geeft aan welke van de volgende antwoorden is gegeven:

-   Geaccepteerd
-   Afgewezen
-   Geaccepteerd met wijzigingen
-   Vervangen/Vervanging
-   Opsplitsen tot planning/Planningsregel

Houd er rekening mee dat het veld **Leveren** is ingesteld op **Ja** of **Nee** om aan te geven of de regels worden geleverd. Een regel kan om de volgende redenen niet worden geleverd:

- De regel is afgewezen.
- Een product is vervangen en de oorspronkelijke regel wordt niet verwacht te worden geleverd, zoals gevraagd in de ontvangen order.
- De regel is opgesplitst in meerdere schemaregels en de oorspronkelijke regel wordt naar verwachting niet geleverd, zoals gevraagd in de ontvangen order.

Alle wijzigingen die zijn aangebracht in de orderregelreactie worden hier weergegeven. Geüploade notities en bijlagen worden echter niet weergegeven. Om notities en bijlagen weer te geven moet u echter de webinterface voor leverancierssamenwerking in de webclient gebruiken.

### <a name="open-confirmed-orders"></a>Openstaande bevestigde orders
Wanneer de inkooporder is bevestigd door de klant (wat inhoudt dat de inkooporder is gewijzigd naar de status **Bevestigd**) wordt hij weergegeven als openstaande bevestigde order. Hij blijft in de lijst staan, totdat hij wordt geregistreerd als ontvangen door de klant.

