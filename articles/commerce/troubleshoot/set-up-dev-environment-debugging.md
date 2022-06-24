---
title: Een ontwikkelomgeving voor e-commerce instellen voor foutopsporing op een virtuele machine van Tier 1 Retail Server
description: In dit artikel wordt uitgelegd hoe u een ontwikkelomgeving voor e-commerce kunt instellen voor foutopsporing op een virtuele machine (VM) van Tier 1 Retail Server.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7cc6c936c67bc82da1a237341ac07fb69d4ac233
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855697"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>Een ontwikkelomgeving voor e-commerce instellen voor foutopsporing op een virtuele machine van Tier 1 Retail Server

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een ontwikkelomgeving voor e-commerce kunt instellen voor foutopsporing op een virtuele machine (VM) van Tier 1 Retail Server.

## <a name="description"></a>Beschrijving

Microsoft Dynamics 365 Commerce Tier 1-omgevingen worden meestal geïmplementeerd voor Commerce runtime (CRT) en POS-uitbreidingsontwikkeling (Point of Sale). Dit zijn zelfstandige omgevingen. Vanwege de SaaS-aard (Software as a Service) van de architectuur, zijn geen e-commerce-onderdelen inbegrepen.

In sommige scenario's wilt u mogelijk aanroepen voor uitbreidingen in een Tier 1-omgeving testen, zodat u foutopsporing kunt uitvoeren vanuit e-commerce-onderdelen. Zie [Foutopsporing voor een Tier 1-ontwikkelomgeving voor Commerce](../e-commerce-extensibility/debug-tier-1.md) voor algemene instructies.

Wanneer u fouten opspoort in een Tier 1-omgeving, omdat de site nu een andere Retail Server aanroept, kunnen cross-serveroproepen verschillende fouten veroorzaken met betrekking tot het beleid voor inhoudsbeveiliging.

In de volgende afbeelding ziet u een voorbeeld van een fout die kan optreden wanneer een variant wordt geselecteerd op een productdetailpagina.

![Fout bij het selecteren van een variant op een productdetailpagina.](media/unhandled-rejection-error.jpg)

In de volgende afbeelding ziet u een voorbeeld van een vergelijkbare fout in de foutopsporingstools van een browser (F12 Developer Tools). In het foutbericht wordt gesproken over overtreding van de richtlijn voor inhoudsbeveiliging.

![Fout in programma's voor foutopsporing.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>Oplossing

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>Het beleid voor inhoudsbeveiliging uitschakelen voor de site in Commerce Site Builder

1. Selecteer de site waaraan u werkt.
1. Selecteer **Instellingen** en selecteer vervolgens **Uitbreidingen**.
1. Selecteer op het tabblad **Beveiligingsbeleid voor inhoud** de optie **Beleid voor inhoudsbeveiliging uitschakelen**.
1. Selecteer **Opslaan en publiceren**.

> [!NOTE]
> Aanmelden met B2C (Business-to-consumer) werkt niet in een lokale ontwikkelomgeving. U kunt echter als gast uitchecken gebruiken of dummypagina's bouwen om waar nodig het aanmelden van gebruikers te simuleren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Aan de slag met ontwikkeling van online uitbreiding van e-commerce](../e-commerce-extensibility/sdk-getting-started.md)

[Beleid voor inhoudsbeveiliging (CSP) op de e-commercesite beheren](../manage-csp.md)
