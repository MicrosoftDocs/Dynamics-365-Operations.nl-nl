---
title: Attract-gebruikers kunnen niet solliciteren op banen in de vacatureportal
description: In dit onderwerp wordt uitgelegd hoe u een probleem kunt oplossen als Attract-gebruikers niet kunnen solliciteren op vacatures in de carrièreportal.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460771"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Attract-gebruikers kunnen niet solliciteren op banen in de vacatureportal

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Uitgeven

Attract-gebruikers kunnen niet solliciteren op vacatures in de carrièreportal. Wanneer ze solliciteren op een vacature die is gemaakt in Dynamics 365 Talent: Attract, wordt de pagina continu door de browser geladen en wordt de actie niet voltooid.

## <a name="cause"></a>Oorzaak

Dit probleem doet zich voor wanneer het Talent Relationship Team geen Talent-gebruikersrol heeft.

## <a name="resolution"></a>Oplossing

Wijs de Talent-gebruikersrol toe aan het Talent Relationship Team.

1. Meld u bij het [Power Platform beheercentrum](https://admin.powerplatform.microsoft.com) aan met een van de volgende beheerdersreferenties:

   - Dynamics 365 admin
   - Algemeen beheerder
   - Power Platform beheerder

2. Selecteer in het navigatievenster de optie **Omgevingen** en selecteer vervolgens de omgeving waarin u de Talent-gebruikersrol wilt toewijzen aan het Talent Relationship Team.

   ![Omgeving selecteren](./media/attract-troubleshoot-career-portal-select-environment.png)

3. Selecteer in het venster **Omgevingen** de **Omgeving-URL** en meld u aan bij de beheerdersportal van de omgeving (bijvoorbeeld https:<orgname>. crm.dynamics.com).

4. Selecteer **Instellingen**, selecteer **Systeem** en selecteer **Beveiliging**.

   ![Navigeer naar Beveiliging](./media/attract-troubleshoot-career-portal-security.png)

5. Selecteer **Teams**.

   ![Selecteer Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Zoek naar **Talent Relationship Team** in het zoekvak en selecteer vervolgens het team uit de zoekresultaten.

7. Selecteer **ROLLEN BEHEREN** op het lint.

8. Selecteer in het dialoogvenster **Teamrollen beheren** de optie **Talent-gebruiker** in de lijst met beschikbare rollen en selecteer vervolgens **Ok** om de rol toe te passen.

   ![Rol Toepassen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Test de wijzigingen:

   1. Meld u aan bij de carrièreportal in een nieuw browservenster.
   2. Solliciteer op de vacature in de carrièreportal. 