---
title: Gebruikersrollen voor lease toewijzen
description: In dit onderwerp worden de beveiligingsrollen beschreven die worden gebruikt voor activa-leasing. Ook wordt uitgelegd hoe u gebruikers aan deze rollen toewijst.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1a9e7772448314e0c3fd101576c07a5b6508270f
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711286"
---
# <a name="assign-lease-user-roles"></a>Gebruikersrollen voor lease toewijzen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de beveiligingsrollen beschreven die worden gebruikt voor activa-leasing. Ook wordt uitgelegd hoe u gebruikers aan deze rollen toewijst.

Drie gebruikersrollen geven verschillende toegang tot activa-leasing. Eén rol is geschikt voor het onderhouden van leases, een is geschikt voor het weergeven van leases en een is geschikt voor het uitvoeren van de taken van een leasemedewerker. Elke rol heeft specifieke machtigingen voor alle leasepagina's, en gebruikers kunnen met elk van deze rollen leases weergeven, maken, bewerken of verwijderen op basis van hun functie.

| Rol           | Beschrijving |
|----------------|-------------|
| Lease onderhouden | Gebruikers met deze rol kunnen leases toevoegen, bewerken, verwijderen en weergeven. Deze rol is bedoeld voor dagelijkse gebruikers van wie de taken het maken en boeken van maandelijkse journaalposten en het toevoegen van nieuwe leases omvatten. Deze rol geeft toegang tot alle functies voor activa-leasing. |
| Lease weergeven     | Gebruikers met deze rol kunnen alleen leaserecords, planningen en uitvoeringsrapporten weergeven. Ze kunnen geen nieuwe leases maken, bestaande leases bewerken of journaalposten voor leases maken. De rol is bedoeld voor gebruikers die alleen leases, lease-schema's en transacties voor deze leases hoeven te bekijken. |
| Leasemedewerker    | Gebruikers met deze rol kunnen alleen nieuwe leases maken. Ze kunnen geen bestaande leases bewerken of verwijderen, lease-schema's weergeven of leasing-journaalposten boeken. Deze rol is bedoeld voor gebruikers die gegevens invoeren. |

Volg deze stappen om gebruikers toe te wijzen aan de rollen die worden gebruikt bij de leasing van activa.

1. Ga naar **Systeembeheer \> Beveiliging \> Gebruikers toewijzen aan rollen**.
2. Selecteer de rol **Lease onderhouden**, **Leasemedewerker** of **Lease weergeven** en selecteer vervolgens **Gebruikers handmatig toewijzen / uitsluiten**.
3. Selecteer de gebruiker die u aan de rol wilt toewijzen en selecteer vervolgens **Toewijzen aan rol**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
