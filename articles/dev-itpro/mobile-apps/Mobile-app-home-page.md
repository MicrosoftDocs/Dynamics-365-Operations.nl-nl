---
title: Startpagina voor de mobiele app
description: In dit onderwerp wordt de mobiele app voor Microsoft Dynamics 365 for Unified Operations beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 08dcdf2f5c03de17d50910e617d20e734e6ee31e
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="mobile-app-home-page"></a>Startpagina voor de mobiele app

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt de mobiele app voor Microsoft Dynamics 365 for Unified Operations beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.

> [!NOTE]
> De mobiele toepassing heette voorheen *Microsoft Dynamics 365 for Finance and Operations*.

<a name="overview"></a>Overzicht
--------

De mobiele app stelt uw organisatie in staat de eigen bedrijfsprocessen beschikbaar te maken op mobiele apparaten. Nadat uw IT-beheerder de mobiele werkgebieden voor uw organisatie heeft ingeschakeld, kunnen gebruikers zich aanmelden bij de app en direct beginnen met het uitvoeren van bedrijfsprocessen vanaf hun mobiele apparaten. De mobiele app omvat de volgende functies waarmee de productiviteit kan worden verhoogd:

- Gebruikers kunnen zakelijke gegevens bekijken, bewerken en hierop reageren, zelfs als zij niet voortdurend een netwerkverbinding hebben of als hun mobiele apparaten volledig offline zijn. Wanneer een apparaat een netwerkverbinding herstelt, worden offline gegevensbewerkingen automatisch gesynchroniseerd met Dynamics 365 voor Finance and Operations, Enterprise edition, of met Microsoft Dynamics 365 voor Finance and Operations.
- IT-beheerders of ontwikkelaars kunnen mobiele werkgebieden bouwen en publiceren die zijn op maat zijn gemaakt voor hun organisatie. De app gebruikt uw bestaande code-elementen. Daarom hoeft u uw validatieprocedures, bedrijfslogica of beveiligingsconfiguratie niet opnieuw te implementeren.
- IT-beheerders of ontwikkelaars kunnen op eenvoudige wijze mobiele werkgebieden ontwerpen met behulp van de ontwerper voor werkgebieden, die werkt via aanwijzen en klikken, die deel uitmaakt van de webclient.
- IT-beheerders of ontwikkelaars kunnen desgewenst de offline mogelijkheden van werkgebieden optimaliseren met behulp van het raamwerk voor uitbreiding van bedrijfslogica. Omdat gegevens nog steeds worden verwerkt terwijl een apparaat offline is, blijven uw mobiele scenario's rijk en vloeiend, zelfs als apparaten geen constante netwerkverbinding hebben.

## <a name="elements-of-the-mobile-app"></a>Elementen van de mobiele app
Navigeren in de mobiele app omvat vier basisconcepten: het dashboard, de werkgebieden, de pagina's en de acties. 

[![Navigatieconcepten in de mobiele app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Wanneer u de app start, gaat u naar het **dashboard**.
2. Op het dashboard ziet u een lijst met **werkgebieden** die zijn gepubliceerd.
3. In elk werkgebied ziet u een lijst met **pagina's** die beschikbaar zijn voor dat werkgebied.
4. Nadat u op een pagina bent aangekomen, kunt u verschillende acties uitvoeren. Hieronder vindt u enkele voorbeelden:

    - Gedetailleerde gegevens bekijken.
    - Naar andere pagina's navigeren voor gerelateerde gegevens, zoals entiteitsdetails of regels.
    - Een overzicht van **acties** bekijken, die beschikbaar zijn voor die pagina. Via acties kunt u gegevens maken of bestaande gegevens bewerken.

## <a name="implementation-process"></a>Implementatieproces
In de volgende afbeelding ziet u het proces voor de implementatie van zowel mobiele werkgebieden die door Microsoft worden geleverd als ook aangepaste mobiele werkgebieden. 

![Implementatieproces voor mobiele apps](./media/Mobile-implementation-process-5.png)

De volgende tabel bevat koppelingen naar resources die u kunnen helpen bij de implementatie van zowel mobiele werkgebieden die door Microsoft worden geleverd als ook aangepaste mobiele werkgebieden. De nummers in de eerste kolom komen overeen met de genummerde stappen in de bovenstaande afbeelding.

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
<td>Implementeer Finance and Operations of Finance and Operations in uw organisatie.</td>
<td><ul><li>Als u nog geen versie van Microsoft Dynamics 365 hebt geïmplementeerd, raadpleeg dan <a href="../deployment/deploy-demo-environment.md">Een demo-omgeving implementeren</a>.</li><li>Een lijst met mobiele werkgebieden die u kunt gebruiken, vindt u in <a href="mobile-workspaces-released.md">Recentelijk gepubliceerde mobiele werkgebieden</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systeembeheerder</td>
<td><strong>Als u Microsoft Dynamics 365 for Finance and Operations, versie 1611, gebruikt:</strong> Download en installeer de KB's die de door Microsoft geleverde mobiele werkgebieden inschakelen.</td>
<td>Zie de volgende onderwerpen voor meer informatie:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Mobiel werkgebied voor kostenbeheer</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiel werkgebied voorhanden voorraad</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobiele werkbieden voor verkooporders</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiel werkgebied voor leverancierssamenwerking</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Tijdinvoer voor project voor mobiel werkgebied</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Mobiel werkgebied voor onkostenbeheer</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systeembeheerder</td>
<td>Publiceer de mobiele werkgebieden die worden geleverd door Microsoft.</td>
<td><a href="publish-mobile-workspace.md">Een mobiel werkgebied publiceren</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Ontwikkelaar of onafhankelijke softwareleveranciers (Independent software vendors - ISV's)</td>
<td>Gebruik het mobiele plaftorm om aangepaste mobiele werkgebieden te maken.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobiel platform</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Maak een implementeerbaar pakket met aangepaste mobiele werkgebieden en upload het pakket naar Microsoft Dynamics Lifecycle Services (LCS).</td>
<td><a href="../deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systeembeheerder</td>
<td>Pas het implementeerbare pakket toe met de aangepaste werkbieden die worden geleverd door uw onafhankelijke sofwareleverancier (ISV).</td>
<td><a href="../deployment/apply-deployable-package-system.md">Een implementeerbaar pakket toepassen</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systeembeheerder</td>
<td>Publiceer de aangepaste mobiele werkgebieden die worden geleverd door de ISV.</td>
<td><a href="publish-mobile-workspace.md">Mobiel werkgebied publiceren</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Gebruiker</td>
<td>Download en installeer de mobiele app.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Voor Android-telefoons</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">Voor iPhones</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Gebruiker</td>
<td>Meld u aan en gebruik de mobiele app. De app omvat de mobiele werkgebieden die zijn gepubliceerd door de systeembeheerder.</td>
<td>Een lijst met mobiele werkgebieden die door Microsoft worden geleverd, vindt u in <a href="mobile-workspaces-released.md">Recentelijk gepubliceerde mobiele werkgebieden</a>.
</td>
</tr>
</tbody>
</table>

