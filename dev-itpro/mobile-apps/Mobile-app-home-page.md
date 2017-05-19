---
title: Startpagina voor mobiele app van Dynamics 365 for Operations
description: In dit onderwerp wordt de mobiele app voor Microsoft Dynamics 365 for Operations beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Startpagina voor mobiele app van Dynamics 365 for Operations

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt de mobiele app voor Microsoft Dynamics 365 for Operations beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.

<a name="overview"></a>Overzicht
--------

De mobiele app voor Microsoft Dynamics 365 for Operations stelt uw organisatie in staat de eigen bedrijfsprocessen beschikbaar te maken op mobiele apparaten. Nadat uw IT-beheerder de functie voor mobiele werkgebieden voor uw organisatie heeft ingeschakeld, kunnen gebruikers zich aanmelden bij de app en direct beginnen met het uitvoeren van bedrijfsprocessen vanaf hun mobiele apparaten. De mobiele app voor Dynamics 365 for Operations omvat de volgende functies waarmee de productiviteit kan worden verhoogd:

-   Gebruikers kunnen zakelijke gegevens bekijken, bewerken en hierop reageren, zelfs als zij niet voortdurend een netwerkverbinding hebben of als hun mobiele apparaten volledig offline zijn. Als een apparaat de netwerkverbinding herstelt, worden offline gegevensbewerkingen automatisch gesynchroniseerd met Dynamics 365 for Operations.
-   IT-beheerders of ontwikkelaars kunnen mobiele werkgebieden bouwen en publiceren die zijn op maat zijn gemaakt voor hun organisatie. De app gebruikt uw bestaande code-elementen. Daarom hoeft u uw validatieprocedures, bedrijfslogica of beveiligingsconfiguratie niet opnieuw te implementeren.
-   IT-beheerders of ontwikkelaars kunnen op eenvoudige wijze mobiele werkgebieden ontwerpen met behulp van de ontwerper voor werkgebieden, die werkt via aanwijzen en klikken, die deel uitmaakt van de Dynamics 365 for Operations-webclient.
-   IT-beheerders of ontwikkelaars kunnen desgewenst de offline mogelijkheden van werkgebieden optimaliseren met behulp van het raamwerk voor uitbreiding van bedrijfslogica. Omdat gegevens nog steeds worden verwerkt terwijl een apparaat offline is, blijven uw mobiele scenario's rijk en vloeiend, zelfs als apparaten geen constante netwerkverbinding hebben.

## <a name="elements-of-the-mobile-app"></a>Elementen van de mobiele app
Navigeren in de mobiele app bestaat uit vier eenvoudige concepten: het dashboard, werkgebieden, pagina's en acties. 

[![Navigatieconcepten in de mobiele app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Wanneer u de app start, gaat u naar het **dashboard**.
-   Op het dashboard ziet u een lijst met **werkgebieden** die in uw Dynamics 365 for Operations-omgeving worden gepubliceerd.
-   In elk werkgebied ziet u een lijst met **pagina's** die beschikbaar zijn voor dat werkgebied.
-   Op een pagina kunt u gegevens bekijken die zijn verzameld van een of meer pagina's van Dynamics 365 for Operations.
-   Vanaf een pagina kunt u navigeren naar andere pagina's voor gerelateerde gegevens, zoals entiteitsdetails of regels.
-   Op een pagina kunt u ook een lijst met **acties** bekijken die beschikbaar zijn voor die pagina.
-   Via acties kunt u gegevens maken of bestaande gegevens bewerken.

## <a name="implementation-process"></a>Implementatieproces
De volgende afbeelding toont het proces voor het implementeren van de mobiele app voor Dynamics 365 for Operations in uw organisatie. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

De volgende tabel bevat koppelingen naar bronnen die u kunnen helpen de mobiele app voor Dynamics 365 for Operations te implementeren in uw organisatie. De nummers in de eerste kolom komen overeen met de genummerde stappen in de bovenstaande afbeelding.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Stap</th>
<th>Rol</th>
<th>Actie</th>
<th>Bronnen die u helpen de actie te voltooien</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Systeembeheerder</td>
<td>Implementeer Dynamics 365 for Operations voor de organisatie.</td>
<td>Als u Dynamics 365 for Operations nog niet hebt geïmplementeerd in uw organisatie, raadpleegt u <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Een Microsoft Dynamics 365 for Operations demo-omgeving implementeren</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Systeembeheerder</td>
<td>Download en installeer KB's waarmee de mobiele werkgebieden die door Microsoft worden geleverd worden ingeschakeld.</td>
<td>Zie de sectie &quot;Vereisten&quot; in het onderwerp over het mobiele werkgebied dat uw organisatie wil gebruiken:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobiel werkgebied voor kostenbeheer</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiel werkgebied voorhanden voorraad</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobiele werkbieden voor verkooporders</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobiel werkgebied voor leverancierssamenwerking</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Tijdinvoer voor project voor mobiel werkgebied</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systeembeheerder</td>
<td>Publiceer de mobiele werkgebieden die worden geleverd door Microsoft.</td>
<td>Zie de sectie &quot;Vereisten&quot; in het onderwerp over het mobiele werkgebied dat uw organisatie wil gebruiken:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobiel werkgebied voor kostenbeheer</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiel werkgebied voorhanden voorraad</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobiele werkbieden voor verkooporders</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobiel werkgebied voor leverancierssamenwerking</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Tijdinvoer voor project voor mobiel werkgebied</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Ontwikkelaar of onafhankelijke softwareleveranciers (Independent software vendors - ISV's)</td>
<td>Gebruik het mobiele framework voor Dynamics 365 for Operations om aangepaste mobiele werkgebieden te maken.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Mobiel framework voor Dynamics 365 for Operations</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Werkgebied X++ API's voor Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Maak een implementeerbaar pakket met aangepaste mobiele werkgebieden en upload het pakket naar Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Een implementeerbaar pakket genereren</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systeembeheerder</td>
<td>Pas het implementeerbare pakket toe met de aangepaste werkbieden die worden geleverd door de ISV.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Een implementeerbaar pakket toepassen op een Microsoft Dynamics 365 for Operations-systeem</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systeembeheerder</td>
<td>Publiceer de aangepaste mobiele werkgebieden die worden geleverd door de ISV.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Een mobiel werkgebied publiceren</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Gebruiker</td>
<td>Download en installeer de mobiele app voor Dynamics 365 for Operations.</td>
<td><ul>
<li>Voor Android: <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations in de Google Play Store</a></li>
<li>Voor iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations in de iTunes apps store</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Gebruiker</td>
<td>Meld u aan en gebruik de mobiele app voor Dynamics 365 for Operations. De app omvat de mobiele werkgebieden die zijn gepubliceerd.</td>
<td>Microsoft heeft de volgende mobiele werkgebieden geleverd:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobiel werkgebied voor kostenbeheer</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Mobiel werkgebied voorhanden voorraad</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Mobiele werkbieden voor verkooporders</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobiel werkgebied voor leverancierssamenwerking</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Tijdinvoer voor project voor mobiel werkgebied</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Zie ook
--------

[Mobiele werkgebieden die onlangs zijn vrijgegeven voor de mobiele app voor Dynamics 365 for Operations](mobile-workspaces-released.md)





