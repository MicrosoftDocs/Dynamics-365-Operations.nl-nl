---
title: Mobiel werkgebied Goedkeuring van inkooporder
description: In dit onderwerp vindt u informatie over het mobiele werkgebied Goedkeuring van inkooporders waarin u inkooporders kunt weergeven en op ze reageren via acties. U kunt bijvoorbeeld een inkooporder goedkeuren of afwijzen.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26f0dc3b128daf8c7d8a05d6f3cacc5b7de0c756
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909103"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Mobiel werkgebied Goedkeuring van inkooporder

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Goedkeuring van inkooporders**. In deze werkruimte kunt u inkooporders weergeven en op ze reageren via acties. U kunt bijvoorbeeld een inkooporder goedkeuren of afwijzen.
 
## <a name="overview"></a>Overzicht 
Inkooporders die moet worden goedgekeurd doorlopen een goedkeuringswerkstroom. De werkstroom kan verschillende stappen omvatten, waarin één of meer mensen actie moeten ondernemen. Een persoon moet bijvoorbeeld mogelijk een taak uitvoeren of de inkooporder goedkeuren. 

In het mobiele werkgebied **Goedkeuring van inkooporders** kunt u eenvoudig op uw mobiele apparaat inkooporders bekijken en op ze reageren. Hier kunt u ook dezelfde werkstroomacties uitvoeren als vanuit de webclient.

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Supply Chain Management die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Vereisten als u Supply Chain Management gebruikt 
Als Supply Chain Management is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Goedkeuring van inkooporder** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Vereisten als u versie Microsoft Dynamics 365 for Operations 1611 met platformupdate 3 of hoger gebruikt
Als Microsoft Dynamics 365 for Operations versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren. 

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
<td>KB 4017918 implementeren.</td>
<td>Systeembeheerder</td>
<td>KB 4017918 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Goedkeuring van inkooporders</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4017918.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Metagegevens-hotfix downloaden uit Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">De metagegevenshotfix installeren</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Het implementeerbare pakket toepassen</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Publiceer het werkgebied <strong>Goedkeuring van inkooporders</strong>.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren
Download en installeer de mobiele Finance and Operations-app:

- [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
- [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app

1. Start de app op uw mobiele apparaat.
2. Voer uw URL voor Microsoft Dynamics 365 in.
3. De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
4. Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

![Werkgebied Goedkeuring van inkooporders in de lijst van beschikbare werkgebieden](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Orders weergeven die aan u zijn toegewezen
1. Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van inkooporders**.
2. Selecteer **Orders die aan mij zijn toegewezen** om alle inkooporders weer te geven waarvoor u een actie moet uitvoeren in de werkstroom Goedkeuring van inkooporders.
3. Selecteer een order. Op de pagina **Ordergegevens** ziet u de koptekst en de regels van de order. Ook vindt u hier de richtlijnen van de werkstroomtaak.
4. Selecteer **Boekhoudingsverdelingen** en open de pagina **Koptekst boekhoudingsverdeling**.
5. Ga terug naar de pagina **Ordergegevens** en selecteer een regel. Vanuit de orderregelgegevens kunt u ook de boekhoudingsverdelingen voor de specifieke regel bekijken.

## <a name="complete-an-action-on-the-purchase-order"></a>Een actie op de inkooporder uitvoeren
Nadat u de inkooporder die aan u is toegewezen hebt bekeken en de workflowinstructies hebt gelezen, zou u gereed moeten zijn om actie te ondernemen.

1. Selecteer op uw mobiele apparaat het werkgebied **Goedkeuring van inkooporders**.
2. Selecteer **Orders die aan mij zijn toegewezen** om alle inkooporders weer te geven waarvoor u een actie moet uitvoeren in de werkstroom Goedkeuring van inkooporders.
3. Selecteer een order en geef de detailpagina weer.
4. Selecteer **acties** om de beschikbare acties weer te geven. Welke acties beschikbaar zijn, is afhankelijk van de taak die aan u is toegewezen.

    | Taakactie    | Goedkeuringsactie  |
    |----------------|------------------|
    | Volledig       | Goedkeuren          |
    | Retour         | Afwijzen           |
    | Wijziging aanvraag | Wijziging aanvraag   |
    | Machtigen       | Machtigen         |

5. Selecteer de gewenste actie.
6. Voer op de pagina **Taak voltooien** een opmerking in. Houd er rekening mee dat als u de actie **Delegeren** kiest, u een gebruiker moet selecteren aan wie de taak wordt gedelegeerd.
7. Selecteer **Gereed**. Nadat u uw werkruimte hebt vernieuwd, staat de inkooporder niet meer in de lijst. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]