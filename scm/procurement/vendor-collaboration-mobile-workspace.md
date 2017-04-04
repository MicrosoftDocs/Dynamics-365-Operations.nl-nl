---
title: Leverancier mobiele werkruimte voor samenwerking voor Microsoft Dynamics 365 voor bewerkingen app
description: Met de leverancier mobiele werkruimte voor samenwerking, kunnen uw leveranciers bijhouden voor de inkooporders die aan hen zijn verzonden voor goedkeuring en informatie over nieuwe en bijgewerkte inkooporders en contactpersonen weergeven.
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Leverancier mobiele werkruimte voor samenwerking voor Microsoft Dynamics 365 voor bewerkingen app

Met de leverancier mobiele werkruimte voor samenwerking, kunnen uw leveranciers bijhouden voor de inkooporders die aan hen zijn verzonden voor goedkeuring en informatie over nieuwe en bijgewerkte inkooporders en contactpersonen weergeven.

<a name="prerequisites"></a>Vereisten
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Meer informatie over de Microsoft Dynamics 365 voor bewerkingen mobiel platform</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 voor bewerkingen mobiel platform</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Zorg ervoor dat u gebruikt een omgeving met Microsoft Dynamics 365 voor bewerkingen versie 1611 en Microsoft Dynamics voor bewerkingen platform 3 (November 2016) bijwerken.</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobiel apparaat met de Dynamics 365 for Operations app geïnstalleerd</span></td>
<td><span style="color: #000000;">De Dynamics 365 for Operations app downloaden van uw winkel mobiele app.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 3215650</td>
<td>Installeer de hotfix zodat de werkruimten die beschikbaar zijn in Dynamics 365 voor bewerkingen.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Hotfix KB 3216943</span> </span></td>
<td>Installeer de hotfix zodat leverancier mobiele de werkruimte voor samenwerking.</td>
</tr>
<tr class="even">
<td>De leveranciersgebruiker moet toegang hebben tot de webinterface voor samenwerking van leverancier in Dynamics 365 voor bewerkingen en een leveranciersgebruiker samenwerking instellen.</td>
<td>Volg de stappen in de volgende onderwerpen instellen en werken met de webinterface voor samenwerking van leverancier.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Leverancier samenwerking gebruiken om te werken met externe leveranciers</a></li>
<li><a href="manage-vendor-collaboration-users.md">Gebruikers van leverancierssamenwerking beheren</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Samenwerking met leveranciers instellen en onderhouden</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Leverancier samenwerking gebruiken om te werken met klanten in Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Overzicht
Leverancier mobiele de werkruimte voor samenwerking houdt leveranciers op de hoogte van nieuwe inkooporders zodat ze kunnen zien en reageren op inkooporders in de Dynamics 365 voor bewerkingen-webclient.  

**opmerking:** de mobiele werkruimte moet worden gebruikt als een aanvulling op de webinterface voor samenwerking van leverancier, maar niet als vervanging.  

Uw leveranciers kunnen aan de leverancier mobiele werkruimte voor samenwerking, nieuwe inkooporders die worden verzonden voor goedkeuring weergeven. Inkoopordergegevens, zoals producten, hoeveelheid en verzochte leverdatums wordt weergegeven. Prijsinformatie is beschikbaar, afhankelijk van de configuratie voor elke leverancier.  

Wanneer een gebruiker zich als een leverancier aanmeldt, zien ze welke inkooporders is beantwoord of welke inkooporders worden nog steeds wacht op actie van de klant. De leverancier kan hebt voorgesteld een andere leveringsdatum die niet nog aan de klant overeengekomen is zodat de inkooporder op actie van de klant wacht. De leverancier wordt ook een overzicht van de inkooporders die bevestigd zijn, maar nog niet zijn geleverd.  

Om te reageren op een inkooporder, heeft de leverancier de leverancier samenwerking webinterface die beschikbaar is in de Dynamics 365 voor bewerkingen webclient gebruiken. Dit is ook waar de leverancier krijgt meer informatie over de order, zoals documentbijlagen, afleveradres per regel en toeslagen die zijn gekoppeld aan de leverancier.  

Met een speciale beveiligingsrol weergeven de leverancier welke personen zijn geregistreerd voor een leveranciersrekening contact. Met dezelfde beveiligingsrol, kunt de leverancier weergeven van de status van alle aanvragen voor de gebruiker die is ingediend.  

Nieuwe contactpersonen maken en indienen van nieuwe gebruikersaanvragen moeten worden uitgevoerd in de interface van de leverancier samenwerking die beschikbaar is in de Dynamics 365 voor bewerkingen webclient.  

Met de mobiele werkruimte uw leverancier kunt doen:

-   Nieuwe inkooporders die zijn verzonden naar de leverancier weergeven.
-   Inkooporders weergeven dat de leverancier heeft gereageerd op en wachten op klant-actie.
-   Inkooporders weergeven die in een bevestigde staat en niet volledig zijn ontvangen.
-   Contactpersoon weergeven die zijn geregistreerd voor de leverancierrekening (de rol van een extra beveiliging vereist).
-   Informatie weergeven en volgt u de status van een aanvraag ingediend door de leverancier (de rol van een extra beveiliging vereist).

## <a name="get-started"></a>Aan de slag
Aan de slag op je mobiele telefoon:

1.  In uw winkel mobiele app downloaden en installeren van de Microsoft Dynamics 365 voor bewerkingen app.
2.  Start de toepassing op het apparaat.
3.  De URL van uw Dynamics 365 invoeren.
4.  Voer in het bedrijf aan te melden. Voer bijvoorbeeld **USMF**.
5.  De eerste keer dat u zich aanmeldt, u gevraagd om de gebruikersnaam en wachtwoord voor uw Microsoft Dynamics 365 voor rekening van de bewerkingen. 

Nadat u zich in de app, worden geen werkruimten weergegeven. Om werkruimten op uw mobiele app bekijkt, moet u eerst de gewenste werkruimten publiceren naar de Dynamics 365 voor bewerkingen app. U moet de systeem-beheer-toestemming voor het publiceren van de werkruimte.

1.  Start de Dynamics 365 voor bewerkingen.
2.  Ga naar **Systeembeheer**&gt;**Setup**&gt;**systeemparameters**.
3.  Selecteer **mobiele app beheren**.
4.  Selecteer de werkruimte **leverancier samenwerking** publiceren naar het mobiele platform.
5.  Selecteer **publiceren werkruimte**.
6.  Het apparaat om te zien van de gepubliceerde werkruimten vernieuwen.
7.  Selecteer de **leverancier samenwerking** werkruimte. U moet de volgende pagina.

[![leverancier-samenwerking-mobiele-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Contacten
De **contactpersonen** pagina kunt u alle contactpersonen die zijn ingesteld voor de leveranciersrekening. Hier worden de contactpersoon naam, primair e- en de gebruikersalias voor de, indien beschikbaar. U ziet ook of de gebruikersaccount van de contactpersoon actief is. Wanneer u een contactpersoon selecteert, kunt u contactgegevens, zoals welke rechtspersonen is voor de persoon een contactpersoon, Zie en contactinformatie zoals telefoonnummer of een ander e-mailadres.

## <a name="user-requests"></a>Gebruikersaanvragen
De **gebruikersaanvragen** pagina kunt u zien dat de gebruiker vraagt die u hebt ingediend via de webinterface voor samenwerking van leverancier en de status volgen. Wanneer u een gebruikersaanvraag, kunt u zien wat is aangevraagd, toevoegen of een gebruiker deactiveren beveiliging wijzigen en zien welke beveiligingsrollen zijn aangevraagd voor de gebruiker.

## <a name="purchase-orders-ready-for-review"></a>Inkooporders gereed voor revisie
De **inkooporders klaar voor controle** pagina kunt u zien dat alle de inkooporders die zijn verzonden door de klant en nog niet zijn beantwoord. U kunt geselecteerde informatie weergeven over de verkooporder, zoals welke producten zijn aangevraagd en wanneer leveren. Prijsinformatie is alleen beschikbaar als deze is geconfigureerd voor de leverancier.  

U kunt zien of de inkooporder notities of bijlagen heeft. U mailbijlagen kunt openen, moet u de samenwerking van de leverancier in de-webclient gebruiken. Selecteer **inkooporderregel** om alle regels met details weer te geven. Houd er rekening mee dat voor elke regel een indicator geeft aan of er notities of bijlagen zijn of als een afleveradres die wijkt af van wat er in de koptekst wordt weergegeven.  

Om te reageren op de inkooporder, moet u de leverancier samenwerking-webclient gebruiken.

## <a name="awaiting-customer-action"></a>In afwachting van actie van klant
De **moet nog actie van de klant** pagina kunt u zoeken naar opdrachten tot inkoop die u of iemand in uw bedrijf die ook toegang tot samenwerking van de leverancier heeft, hebben gereageerd op. De inkooporders zijn alleen zichtbaar in deze lijst als de klant moet een van de volgende acties uitvoeren op de inkooporder.

-   Als de inkooporder is afgewezen, zou de klant hetzij moet bijwerken van de order verzonden en opnieuw verzenden of de order annuleren en opnieuw verzenden. Wanneer de inkooporder opnieuw wordt verzonden, wordt de taak verwijderd uit de **moet nog actie van de klant** pagina.
-   Als de inkooporder is geaccepteerd met wijzigingen, moet de klant bijwerken van de oorspronkelijke order opnieuw verzenden voor beoordeling, of deze bijwerken op basis van de wijzigingen en onmiddellijk bevestigen. In beide gevallen wordt de inkooporder verdwijnen uit de **moet nog actie van de klant** pagina.
-   Als de inkooporder is geaccepteerd en wordt weergegeven in de **moet nog actie van de klant** pagina is omdat de inkooporder is niet automatisch bevestigd wanneer de acceptatie is uitgevoerd. Er wordt gewacht tot een inkoper de volgorde te wijzigen in bevestigd. Normaal gesproken zou de inkooporder worden beschouwd als een overeenkomst tussen de klant en leverancier, zodra de leverancier de order accepteert. De inkooporder te verplaatsen naar de status bevestigd, zou een formaliteit zijn.

Als u de inkooporder, weergegeven extra informatie over het antwoord. U kunt de details van de regels en het antwoord voor elke regel zien. De regel status wordt aangegeven welke van de volgende antwoorden heeft gekregen.

-   Geaccepteerd
-   Afgewezen
-   Geaccepteerd met wijzigingen
-   Vervangen/vervanging
-   In schema of schema regel splitsen

Notitie waarin een indicator **leveren**= Ja/Nee, dat wordt gebruikt om aan te geven dat de regels niet worden geleverd. Het is mogelijk dat de regel is afgewezen of vervangen waar de oorspronkelijke regels worden niet naar verwachting wordt geleverd, of een regel die is gesplitst in meerdere regels en de oorspronkelijke regel niet naar verwachting worden geleverd, zoals opgegeven in de ontvangen order.  

Eventuele wijzigingen in het antwoord van de regel order worden weergegeven, met uitzondering van de geüploade notities en bijlagen die u zien kunt met behulp van de webinterface voor samenwerking van leverancier.

## <a name="open-confirmed-orders"></a>Bevestigde orders openen
Wanneer de inkooporder wordt bevestigd door de klant, wordt wat betekent dat de inkooporder gewijzigd naar de status bevestigd wordt weergegeven in de open bestelling is bevestigd. Het veld in de lijst blijft totdat deze is geregistreerd als ontvangen door de klant.


