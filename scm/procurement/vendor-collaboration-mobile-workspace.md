---
title: Mobiel werkgebied voor leverancierssamenwerking voor de app Microsoft Dynamics 365 for Operations
description: Met het mobiele werkgebied voor leverancierssamenwerking kunnen uw leveranciers de inkooporders volgen die aan hen zijn verzonden voor goedkeuring en informatie weergeven over nieuwe en bijgewerkte inkooporders en contactpersonen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: e19fee87dae6e5d425f36dac0db4ea89534a8510
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobiel werkgebied voor leverancierssamenwerking voor de app Microsoft Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]


Met het mobiele werkgebied voor leverancierssamenwerking kunnen uw leveranciers de inkooporders volgen die aan hen zijn verzonden voor goedkeuring en informatie weergeven over nieuwe en bijgewerkte inkooporders en contactpersonen.

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
<td>Meer informatie over het mobiele platform van Microsoft Dynamics 365 for Operations</td>
<td><a href="https://ax.help.dynamics.com/en/wiki/mobile-development-handbook/">Mobiel platform van Dynamics 365 for Operations</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Zorg ervoor dat u een omgeving gebruikt met Microsoft Dynamics 365 for Operations versie 1611 en Microsoft Dynamics for Operations-platform update 3 (november 2016).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000">Mobiel apparaat waarop de Dynamics 365 for Operations-app is geïnstalleerd</span></td>
<td><span style="color: #000000">Download de Dynamics 365 for Operations-app van uw store voor mobiele apps.</span></td>
</tr>
<tr class="even">
<td>Hotfix KB 4013633</td>
<td>Installeer de hotfix om de werkgebieden in te schakelen die beschikbaar zijn in Dynamics 365 for Operations.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000"><span style="color: #000000">Hotfix KB 3216943</span> </span></td>
<td>Installeer de hotfix om het mobiele werkgebied voor leverancierssamenwerking in te schakelen.</td>
</tr>
<tr class="even">
<td>De leveranciersgebruiker moet toegang hebben tot de webinterface voor leverancierssamenwerking in Dynamics 365 for Operations en een gebruiker voor leverancierssamenwerking instellen.</td>
<td>Volg de stappen in de volgende onderwerpen om de webinterface voor leverancierssamenwerking in te stellen en ermee te werken.
<ul>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-external-vendors/">Leverancierssamenwerking voor het werken met externe leveranciers</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/manage-vendor-collaboration-users/">Gebruikers van leverancierssamenwerking beheren</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/set-up-and-maintain-vendor-collaboration/">Samenwerking met leveranciers instellen en onderhouden</a></li>
<li><a href="https://ax.help.dynamics.com/en/wiki/using-vendor-collaboration-to-work-with-customers-in-dynamics-365-for-operations/">Leverancierssamenwerking voor het werken met klanten in Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Overzicht
Het mobiele werkgebied voor leverancierssamenwerking houdt leveranciers op de hoogte van nieuwe inkooporders, zodat ze inkooporders in de Dynamics 365 for Operations-webclient kunnen zien en erop reageren. 

**Opmerking:** Het mobiele werkgebied moet worden gebruikt als aanvulling op de webinterface voor leverancierssamenwerking, niet als vervanging daarvan. 

Met het mobiele werkgebied voor leverancierssamenwerking kunnen uw leveranciers nieuwe inkooporders weergeven die worden verzonden voor goedkeuring. Hierin worden inkoopordergegevens weergegeven, zoals producten, hoeveelheid en verzochte leverdatums. Afhankelijk van de configuratie per leverancier is ook prijsinformatie beschikbaar. 

Wanneer een gebruiker zich als een leverancier aanmeldt, ziet hij op welke inkooporders is gereageerd of welke inkooporders nog wachten op actie van de klant. De leverancier kan een andere leveringsdatum hebben voorgesteld die niet nog door de klant is geaccepteerd, zodat de inkooporder wacht op actie van de klant. De leverancier krijgt ook een overzicht te zien van de inkooporders die bevestigd zijn, maar nog niet zijn geleverd. 

Om te reageren op een inkooporder moet de leverancier de webinterface voor leverancierssamenwerking gebruiken die beschikbaar is in de Dynamics 365 for Operations-webclient. Hier vindt de leverancier ook meer informatie over de order, zoals documentbijlagen, afleveradres per regel en toeslagen die zijn gekoppeld aan de leverancier. 

Met een speciale beveiligingsrol kan de leverancier zien welke personen zijn geregistreerd voor een leveranciersaccount. Met dezelfde beveiligingsrol kan de leverancier de status zien van alle gebruikersaanvragen die zijn ingediend. 

Het maken van nieuwe contactpersonen en het indienen van nieuwe gebruikersaanvragen moeten worden uitgevoerd in de interface voor leverancierssamenwerking in de Dynamics 365 for Operations-webclient. 

Met het mobiele werkgebied kan uw leverancier onder meer de volgende handelingen uitvoeren:

-   Nieuwe inkooporders bekijken die aan de leverancier zijn verzonden.
-   Inkooporders weergeven waarop de leverancier heeft gereageerd op en die wachten op actie van de klant.
-   Inkooporders weergeven die in een bevestigde status hebben en niet volledig zijn ontvangen.
-   Gegevens voor contactpersonen weergeven, die zijn geregistreerd voor de leveranciersaccount (aanvullende beveiligingsrol vereist).
-   Informatie weergeven voor en de status volgen van een aanvraag die is ingediend door de leverancier (aanvullende beveiligingsrol vereist).

## <a name="get-started"></a>Aan de slag
Aan de slag op uw mobiele telefoon:

1.  Download en installeer de app Microsoft Dynamics 365 for Operations via uw store voor mobiele apps.
2.  Start de app op uw apparaat.
3.  Voer uw Dynamics 365-URL in.
4.  Voer het bedrijf in waarbij u zich wilt aanmelden. Voer bijvoorbeeld **USMF** in.
5.  De eerste keer dat u zich aanmeldt, wordt u gevraagd om de gebruikersnaam en het wachtwoord voor uw Microsoft Dynamics 365 for Operations-account.

Nadat u zich in de app hebt aangemeld, worden geen werkgebieden weergegeven. Als u werkgebieden op uw mobiele app wilt bekijken, moet u eerst de gewenste werkgebieden publiceren naar de Dynamics 365 for Operations-app. U hebt systeembeheerrechten nodig om het werkgebied te publiceren.

1.  Start Dynamics 365 for Operations.
2.  Ga naar **Systeembeheer** &gt; **Instellen** &gt; **Systeemparameters**.
3.  Selecteer **Mobiele app beheren**.
4.  Selecteer het werkgebied **Leverancierssamenwerking** voor publicatie naar het mobiele platform.
5.  Selecteer **Werkgebied publiceren**.
6.  Vernieuw uw apparaat om de gepubliceerde werkgebieden te zien.
7.  Selecteer het werkgebied **Leverancierssamenwerking**. De volgende pagina wordt geopend.

    [![leverancierssamenwerking-mobiele-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Contacten
Op de pagina **Contactpersonen** ziet u alle contactpersonen die zijn ingesteld voor de leveranciersaccount. De weergegeven gegevens zijn de naam, het primaire e-mailadres en de gebruikersalias van de contactpersoon, indien beschikbaar. Hier wordt ook aangegeven of de gebruikersaccount van de contactpersoon actief is. Wanneer u een contactpersoon selecteert, ziet u verschillende gegevens, zoals voor welke rechtspersonen de persoon een contactpersoon is en contactgegevens zoals telefoonnummer of een ander e-mailadres.

## <a name="user-requests"></a>Gebruikersaanvragen
Op de pagina **Gebruikersaanvragen** kunt u alle gebruikersaanvragen zien die u hebt ingediend via de webinterface voor leverancierssamenwerking en de status ervan volgen. Wanneer u een gebruikersaanvraag selecteert, ziet u wat is aangevraagd, een gebruiker toevoegen of deactiveren, de beveiliging wijzigen en zien welke beveiligingsrollen zijn aangevraagd voor de gebruiker.

## <a name="purchase-orders-ready-for-review"></a>Inkooporders ter beoordeling
Op de pagina **Inkooporders ter beoordeling** kunt u zien alle inkooporders zien die zijn verzonden door de klant en nog niet zijn beantwoord. U kunt geselecteerde informatie weergeven over de verkooporder, zoals welke producten zijn aangevraagd en wanneer deze moeten worden geleverd. Prijsinformatie is alleen beschikbaar als dit is geconfigureerd voor de leverancier. U kunt zien of de inkooporder notities of bijlagen heeft. Om bijlagen te openen, moet u de leverancierssamenwerking in de webclient gebruiken. Selecteer **Inkooporderregel** om alle regels met details weer te geven. Merk op dat een indicator bij elke regel aangeeft of er notities of bijlagen zijn, of dat het afleveradres afwijkt van wat in de koptekst wordt weergegeven. Om te reageren op de inkooporder moet u de webclient voor leverancierssamenwerking gebruiken.

## <a name="awaiting-customer-action"></a>In afwachting van actie van klant
Op de pagina **In afwachting van actie van klant** kunt u zoeken naar inkoopopdrachten waarop u of iemand in uw bedrijf met toegang tot leverancierssamenwerking heeft gereageerd. De inkooporders zijn alleen zichtbaar in deze lijst als de klant een van de volgende acties heeft uitgevoerd op de inkooporder.

-   Als de inkooporder is afgewezen, moet de klant de verzonden order bijwerken en opnieuw verzenden of deze annuleren en opnieuw verzenden. Nadat de inkooporder opnieuw is verzonden, wordt hij verwijderd uit de pagina **In afwachting van actie van klant**.
-   Als de inkooporder is geaccepteerd met wijzigingen, moet de klant de oorspronkelijke order bijwerken en opnieuw verzenden ter beoordeling, of deze bijwerken op basis van de wijzigingen en onmiddellijk bevestigen. In beide gevallen wordt de inkooporder verwijderd uit de pagina **In afwachting van actie van klant** nadat hij opnieuw is verzonden.
-   Als de inkooporder is geaccepteerd en nog steeds wordt weergegeven op de pagina **In afwachting van actie van klant**, komt dat doordat de inkooporder niet automatisch is bevestigd bij acceptatie. De order wacht op een inkoper die de status moet wijzigen in Bevestigd. Normaal gesproken wordt de inkooporder beschouwd als een overeenkomst tussen de klant en leverancier, zodra de leverancier de order accepteert. Het verplaatsen van de inkooporder naar de status Bevestigd is een formaliteit.

Als u de inkooporder selecteert, worden aanvullende gegevens voor het antwoord weergegeven. U kunt de regeldetails en het antwoord voor elke regel bekijken. De regelstatus geeft aan welke van de volgende antwoorden is gegeven.

-   Geaccepteerd
-   Afgewezen
-   Geaccepteerd met wijzigingen
-   Vervangen/Vervanging
-   Opsplitsen tot planning/Planningsregel

Merk op dat een indicator aangeeft: **Leveren**= Ja/Nee, waarmee wordt aangegeven dat de regels niet worden geleverd. Dit kan zijn omdat de regel is afgewezen, of vervangen waarbij de oorspronkelijke regels naar verwachting niet zouden worden geleverd, of een regel is gesplitst in meerdere regels waarbij de oorspronkelijke regel naar verwachting niet zou worden geleverd, zoals opgegeven in de ontvangen order. Eventuele wijzigingen in het antwoord op de orderregel worden weergegeven, met uitzondering van de geüploade notities en bijlagen die u zien kunt met de webinterface voor leverancierssamenwerking.

## <a name="open-confirmed-orders"></a>Openstaande bevestigde orders
Wanneer de inkooporder is bevestigd door de klant (wat inhoudt dat de inkooporder is gewijzigd naar de status Bevestigd) wordt hij weergegeven als openstaande bevestigde order. Hij blijft in de lijst staan, totdat hij wordt geregistreerd als ontvangen door de klant.





