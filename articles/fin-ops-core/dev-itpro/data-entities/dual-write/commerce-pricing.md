---
title: De Dynamics 365 Commerce-prijsengine gebruiken met Dynamics 365 Sales
description: In dit artikel wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Commerce gebruikt om verkoopoffertes te maken in Dynamics 365 Sales.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881389"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>De Dynamics 365 Commerce-prijsengine gebruiken met Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u de prijsengine in Microsoft Dynamics 365 Commerce gebruikt om verkoopoffertes te maken in Dynamics 365 Sales.

De Dynamics 365 Commerce-prijsengine ondersteunt de meeste B2C-prijsscenario's (Business-to-consumer), zoals prijzen op winkelniveau, prijzen op basis van relatie en loyaliteit, combinatiekortingen, kwantumkortingen en drempelkortingen. De prijsengine gebruikt complexe regels om de beste prijs voor een bepaalde offerte of order te bepalen.

Wanneer u [twee keer wegschrijven](./dual-write-overview.md) gebruikt, hebt u drie opties voor uw prijsbehoeften. U kunt de statische prijzen gebruiken die afkomstig zijn van de prijslijst in Dynamics 365 Sales, de prijsengine in Dynamics 365 Supply Chain Management of de prijsengine in Dynamics 365 Commerce. Onder deze opties is de Commerce-prijsengine het meest geschikt voor B2C-scenario's.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>De Commerce-prijsengine gebruiken in Sales

> [!NOTE]
> Op dit moment kan de Commerce-prijsengine alleen worden gebruikt voor het maken van offertes in Sales. Integratie van verkooporders met de Commerce-prijsengine is nog niet beschikbaar.

Wanneer gebruikers een offerte in Sales starten, kopieert het raamwerk voor twee keer wegschrijven de offertegegevens naar Commerce. Eventuele wijzigingen in bestaande offerteregels of nieuw toegevoegde offerteregels in Sales worden naar Commerce gekopieerd. Wanneer gebruikers de Commerce-prijsengine willen gebruiken voor de prijscalculatie, kunnen zij **Prijsopgave** selecteren om de prijzen van de offerte bij te werken op basis van de Commerce-prijsengine. Prijzen worden vervolgens automatisch bijgewerkt in Sales en Commerce.

## <a name="prerequisites"></a>Vereisten

- Voordat u de Commerce-prijsengine in Sales kunt gebruiken, moet u de stappen in [Prospect naar contant geld in twee keer wegschrijven](./dual-write-prospect-to-cash.md) volgen.
- U moet evaluatie van handelsovereenkomst uitschakelen door de volgende stappen uit te voeren:

    1. Ga in uw Commerce-omgeving naar **Klanten \> Instellen \> Parameters van module Klanten**.
    1. Schakel op het tabblad **Prijzen** op het sneltabblad **Evaluatie van handelsovereenkomst** het selectievakje **Handmatige invoer** uit.

## <a name="additional-resources"></a>Aanvullende bronnen

[Prospect naar contant geld in twee keer wegschrijven](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]