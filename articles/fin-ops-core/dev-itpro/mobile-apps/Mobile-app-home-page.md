---
title: Startpagina mobiele app
description: In dit onderwerp wordt de mobiele app voor Finance and Operations (Dynamics 365) beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 469b03151f3113f44d932a2d6f4bf3fcfa059133
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188405"
---
# <a name="mobile-app-home-page"></a>Startpagina mobiele app

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de mobiele app voor **Finance and Operations (Dynamics 365)** beschreven en worden koppelingen verstrekt naar bronnen die u kunnen helpen deze toe te passen in uw organisatie.

## <a name="overview"></a>Overzicht

De mobiele app stelt uw organisatie in staat de eigen bedrijfsprocessen beschikbaar te maken op mobiele apparaten. Nadat uw IT-beheerder de mobiele werkgebieden voor uw organisatie heeft ingeschakeld, kunnen gebruikers zich aanmelden bij de app en direct beginnen met het uitvoeren van bedrijfsprocessen vanaf hun mobiele apparaten. De mobiele app omvat de volgende functies waarmee de productiviteit kan worden verhoogd:

- Gebruikers kunnen zakelijke gegevens bekijken, bewerken en hierop reageren, zelfs als zij niet voortdurend een netwerkverbinding hebben of als hun mobiele apparaten volledig offline zijn. Als een apparaat de netwerkverbinding herstelt, worden offline gegevensbewerkingen automatisch gesynchroniseerd.
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

[![Implementatieproces voor mobiele apps](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

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
<td>Implementeer de Finance and Operations-app in uw organisatie.</td>
<td><ul><li>Als u nog geen versie van Microsoft Dynamics 365 hebt geïmplementeerd, raadpleeg dan <a href="../deployment/deploy-demo-environment.md">Een demo-omgeving implementeren</a>.</li><li>Een lijst met mobiele werkgebieden die u kunt gebruiken, vindt u in <a href="mobile-workspaces-released.md">Recentelijk gepubliceerde mobiele werkgebieden</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systeembeheerder</td>
<td><strong>Als u Microsoft Dynamics 365 for Operations versie 1611 gebruikt:</strong> Download en installeer KB's waarmee de mobiele werkgebieden die door Microsoft worden geleverd worden ingeschakeld.</td>
<td>Zie de volgende onderwerpen voor meer informatie:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobiel werkgebied voor kostenbeheer</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiel werkgebied voorhanden voorraad</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Mobiele werkbieden voor verkooporders</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiel werkgebied voor leverancierssamenwerking</a></li>
<li><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Tijdinvoer voor project voor mobiel werkgebied</a></li>
<li><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Mobiel werkgebied voor onkostenbeheer</a></li>

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
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations-app voor Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations-app voor iOS</a><BR/>
(Windows Phone wordt niet ondersteund)
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

## <a name="troubleshooting"></a>Problemen oplossen
[Resources voor mobiel platform](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]