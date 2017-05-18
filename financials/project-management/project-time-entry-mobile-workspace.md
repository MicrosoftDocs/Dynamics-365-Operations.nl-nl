---
title: Mobiel werkgebied voor invoer van projecturen voor de app Microsoft Dynamics 365 for Operations
description: Dit onderwerp biedt informatie over het mobiele werkgebied voor invoer van projecturen. In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Mobiel werkgebied voor invoer van projecturen

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dit onderwerp biedt informatie over het mobiele werkgebied Invoer van projecturen, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. In dit werkgebied kunnen gebruikers tijd invoeren en opslaan voor een project met behulp van hun mobiele apparaat.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Overzicht van het mobiele werkgebied Invoer van projecturen
---------------------------------------------------

Als onderdeel van hun dagelijkse werkzaamheden zijn projectresources vaak on-site of onderweg. Het mobiele werkgebied **Invoer van projecturen** stelt gebruikers in staat hun factureerbaar of niet-factureerbare tijd voor een project in te voeren op het mobiele apparaat van hun keuze. Daarom kunnen projectresources altijd en overal tijdinvoer vastleggen. Zij kunnen ook tijdinvloer bekijken die al is geregistreerd. 

Het mobiele werkgebied **Invoer van projecturen** biedt vooral de volgende functies:

-   Voer voor elke geselecteerde datum het aantal uren in dat u hebt besteed aan een bepaalde taak.
-   Zoek op projectnaam of klant om het project te vinden waarvoor u tijd wilt invoeren.
-   Geef de categorie en de activiteit op voor de tijd die u hebt besteed.
-   Leg de tijd vast als factureerbaar of niet-factureerbaar voor het project.
-   Voer desgewenst externe of interne opmerkingen toe.

Voor het implementeren van het mobiele werkgebied **Invoer van projecturen** bekijkt u de volgende secties in dit onderwerp.

## <a name="prerequisites"></a>Vereisten
Voordat u het mobiele werkgebied **Invoer van projecturen** kunt gebruiken, controleert u of de systeembeheerder de volgende vereisten heeft geregeld.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations versie 1611 met platformupdate 3 of hoger moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>Als u Dynamics 365 for Operations nog niet hebt geïmplementeerd in uw organisatie, dient uw systeembeheerder <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Een Microsoft Dynamics 365 for Operations demo-omgeving implementeren</a> te raadplegen.</td>
</tr>
<tr class="even">
<td>KB 4018050 moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>KB 4018050 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Invoer van projecturen</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4018050.
<ol>
<li>Download KB 4018050 van Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installeer de metagegevenshotfix</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Maak een implementeerbaar pakket</a> dat de <strong>ApplicationSuite</strong> en <strong>ProjectMobile</strong>-modellen bevat en upload het implementeerbare pakket vervolgens naar LCS.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a> op uw Microsoft Dynamics 365 for Operations-systeem.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het mobiele werkgebied <strong>Invoer van projecturen</strong> moet worden gepubliceerd naar de mobiele app voor Dynamics 365 for Operations.</td>
<td>Systeembeheerder</td>
<td><ol>
<li>Start Dynamics 365 for Operations in uw browser.</li>
<li>Selecteer op de pagina <strong>Systeemparameters</strong>, op het tabblad <strong>Mobiele werkgebieden beheren</strong>, het werkgebied <strong>Invoer van projecturen</strong>.</li>
<li>Klik op <strong>Mobiel werkgebied publiceren</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>De mobiele app voor Dynamics 365 for Operations downloaden en installeren
Download en installeer de mobiele app van Microsoft Dynamics 365 for Operations vanuit uw store voor mobiele apps.

-   Voor Android: [Dynamics 365 for Operations in de Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Voor iPhone: [Dynamics 365 for Operations in de iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Meld u aan bij de mobiele app voor Dynamics 365 for Operations
1.  Start de app op uw mobiele apparaat.
2.  Voer uw Dynamics 365 for Operations-URL in.
3.  Voer het bedrijf in waarbij u zich wilt aanmelden. Voer bijvoorbeeld **USMF** in.
4.  De eerste keer dat u zich aanmeldt, wordt u gevraagd om de gebruikersnaam en het wachtwoord voor uw Dynamics 365 for Operations-account. Voer uw referenties in.
5.  Nadat u zich hebt aangemeld, ziet u de beschikbare werkgebieden voor uw bedrijf. Houd er rekening mee dat als uw systeembeheerder een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden kunt opvragen om te vernieuwen.

[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Tijd invoeren met behulp van het mobiele werkgebied Invoer van projecturen
1.  Selecteer op uw mobiele apparaat het werkgebied **Invoer van projecturen**.
2.  Selecteer **Tijdinvoer**. U ziet de kalenderdatums voor de huidige week.
3.  Selecteer voor een geselecteerde datum **Acties** &gt; **Nieuwe invoer**.
4.  Voer het aantal uren te registreren uren in.
5.  Selecteer het project voor de tijdinvoer. U ziet een lijst van de projecten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) raadplegen.
6.  Als uw project niet in de lijst staat, selecteert u **Zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op naam of schakel over naar zoeken op projectnaam of klant.
7.  Een categorie selecteren. U ziet een lijst van de categorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) raadplegen.
8.  Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op categorie of schakel over naar zoeken op categorienaam.
9.  Een activiteit selecteren. U ziet een lijst van de activiteiten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) raadplegen.
10. Als uw activiteit niet in de lijst staat, selecteert u **Zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoeken op activiteitnummer of schakel over als u wilt zoeken op doel.
11. Selecteer de regeleigenschap.
12. Optioneel: voer eventueel externe en interne opmerkingen toe.
13. Selecteer **Gereed**.






