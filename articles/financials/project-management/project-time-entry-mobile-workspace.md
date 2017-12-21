---
title: Tijdinvoer voor project voor mobiel werkgebied
description: Dit onderwerp biedt informatie over het mobiele werkgebied voor invoer van projecturen. In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: c04ffccdcbf104b1d5db30a41116663fcedd4e1d
ms.contentlocale: nl-nl
ms.lasthandoff: 12/01/2017

---

# <a name="project-time-entry-mobile-workspace"></a>Tijdinvoer voor project voor mobiel werkgebied

[!include[banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Projecttijdinvoer**. In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.

Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Overzicht
Als onderdeel van hun dagelijkse werkzaamheden zijn projectresources vaak on-site of onderweg. Het mobiele werkgebied **Invoer van projecturen** stelt gebruikers in staat hun factureerbaar of niet-factureerbare tijd voor een project in te voeren op het mobiele apparaat van hun keuze. Daarom kunnen projectresources altijd en overal tijdinvoer vastleggen. Zij kunnen ook tijdinvloer bekijken die al is geregistreerd. 

Specifiek kunnen gebruikers in het mobiele werkgebied **Projecttijdinvoer** deze taken uitvoeren:

-   Voer voor elke geselecteerde datum het aantal uren in dat u hebt besteed aan een bepaalde taak.
-   Zoek op projectnaam of klant om het project te vinden waarvoor u tijd wilt invoeren.
-   Geef de categorie en de activiteit op voor de tijd die u hebt besteed.
-   Leg de tijd vast als factureerbaar of niet-factureerbaar voor het project.
-   Voer desgewenst externe of interne opmerkingen toe.

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Vereisten als u Microsoft Dynamics 365 for Finance and Operations, Enterprise edition gebruikt
Als Microsoft Dynamics 365 for Finance and Operations, Enterprise edition is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Projecttijdinvoer** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Vereisten als u Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger gebruikt.
Als Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder aan de volgende vereisten voldoen. 

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

<td>KB 4018050 implementeren.</td>
<td>Systeembeheerder</td>
<td>KB 4018050 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Invoer van projecturen</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4018050.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">De metagegevenshotfix van Microsoft Dynamics Lifecycle Services (LCS) downloaden</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Maak een implementeerbaar pakket</a> dat de <strong>ApplicationSuite</strong> en <strong>ProjectMobile</strong>-modellen bevat en upload het implementeerbare pakket vervolgens naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Het mobiele werkgebied <strong>Projecttijdinvoer</strong> publiceren.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Dynamics 365 for Unified Operations:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1.  Start de app op uw mobiele apparaat.
2.  Voer uw Dynamics 365-URL in.
3.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
4.  Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Tijd invoeren met behulp van het mobiele werkgebied Invoer van projecturen
1.  Selecteer op uw mobiele apparaat het werkgebied **Invoer van projecturen**.
2.  Selecteer **Tijdinvoer**. De kalenderdatums voor de huidige week worden weergegeven.
3.  Selecteer voor een geselecteerde datum **Acties** &gt; **Nieuwe invoer**.
4.  Voer het aantal uren te registreren uren in.
5.  Selecteer het project voor de tijdinvoer. In een lijst ziet u de projecten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Als uw project niet in de lijst staat, selecteert u **Zoeken**. Zoek op naam of schakel over naar zoeken op projectnaam of klant.
7.  Een categorie selecteren. In een lijst ziet u de categorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Als uw categorie niet in de lijst staat, selecteert u **Zoeken**. Zoek op categorie of schakel over naar zoeken op categorienaam.
9.  Een activiteit selecteren. In een lijst ziet u de activiteiten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie voor meer informatie [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Als uw activiteit niet in de lijst staat, selecteert u **Zoeken**. Zoeken op activiteitnummer of schakel over als u wilt zoeken op doel.

11. Selecteer de regeleigenschap.
12. Optioneel: voer eventueel externe en interne opmerkingen toe.
13. Selecteer **Gereed**.

