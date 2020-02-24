---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (7 januari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974425"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (7 januari 2020)

In dit artikel worden de functies beschreven die in Dynamics 365 Talent nieuw of gewijzigd zijn.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2697. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Kan werknemers zonder dienstverbandrecord niet verwijderen - (386157)

Deze wijziging voegt een optie voor verwijderen toe aan het formulier **Medewerkers zonder dienstverband**. Medewerkers worden weergegeven in dit formulier wanneer er geen dienstverband voor de werknemer bestaat voor het verleden, het heden of de toekomst. In deze versie kunnen alleen systeembeheerders deze medewerkers verwijderen. In de versie van de volgende week wordt de beveiliging echter bijgewerkt, zodat alle gebruikers met de rol van HR-assistent medewerkers zonder dienstverband kunnen verwijderen. U kunt deze wijzigingen ook handmatig doorvoeren met de volgende stappen.

1. Ga naar **Beveiligingsconfiguratie**.
2. Filter op het tabblad **Bevoegdheden** de lijst **Bevoegdheden** op **Medewerkers onderhouden**.
3. Selecteer in de kolom **Verwijzingen** de optie **Opdrachten in weergavemenu**.
4. Selecteer onder **Opdrachten in weergavemenu** de optie **HcmWOrkersWithoutEmployment**.
5. Stel de machtiging **Verwijderen** in op Toewijzen.
6. Selecteer het tabblad **Niet-gepubliceerde objecten**.
7. Selecteer **Alles publiceren**.
