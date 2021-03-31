---
title: Automatische fiattering met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u automatische fiattering gebruikt met Planningsoptimalisatie.
author: ChristianRytt
manager: tfehr
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 9106137fe6dd097beea9914cdde541e581946f46
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227789"
---
# <a name="autofirming-with-planning-optimization"></a>Automatische fiattering met Planningsoptimalisatie

[!include [banner](../../includes/banner.md)]

Met automatische fiattering kunt u geplande orders fiatteren (vrijgeven) als onderdeel van het hoofdplanningsproces. Wanneer geplande orders worden gefiatteerd, worden deze omgezet in werkelijke inkooporders, transferorders of productie orders. Wanneer Planningsoptimalisatie wordt gebruikt, worden geplande orders gefiatteerd tijdens de uitvoering van een hoofdplanning wanneer de orderdatum (dat wil zeggen de begindatum) binnen de time fence voor fiattering valt.

> [!NOTE]
> Een geplande inkooporder kan alleen automatisch automatisch worden gefiatteerd als het artikel is gekoppeld aan een leverancier.

## <a name="turn-on-autofirming"></a>Automatische fiattering inschakelen

Voer de volgende stappen uit om automatische fiattering in te schakelen.

1. Selecteer **Automatisch fiatteren voor Planningsoptimalisatie** in de lijst op het tabblad **Nieuw** van het werkgebied **Functiebeheer**. Als de functie niet wordt weergegeven op het tabblad **Nieuw**, kijkt u op de tabbladen **Niet ingeschakeld** en **Alle**.
1. Selecteer **Nu inschakelen**. U kunt ook **Planning** selecteren en vervolgens het tijdstip selecteren waarop u de functie wilt inschakelen.

## <a name="set-up-the-firming-time-fence"></a>De time fence voor fiatteren instellen

De time fence voor fiattering wordt vooruit vanaf de datum van hoofdplanningsuitvoering berekend. Deze wordt gedefinieerd op basis van het aantal dagen dat u invoert. U kunt de time fence voor fiatteren op de volgende manieren beheren:

- Als u de standaard time fence voor fiattering voor een behoefteplanningsgroep wilt definiëren, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Behoefteplanning** \> **Behoefteplanningsgroepen** en selecteert u een behoefteplanningsgroep. Voer vervolgens op het sneltabblad **Overige** in het veld **Time fence automatische fiattering (dagen)** het aantal dagen in.
- Als u de gedefinieerde time fence voor de behoefteplanningsgroep voor een specifiek artikel wilt overschrijven, gaat u naar **Productgegevensbeheer** \> **Vrijgegeven producten** en selecteert u vervolgens in het actievenster **Planning** en **Artikelbehoefteplanning**. Selecteer vervolgens op het tabblad **Algemeen** de optie **Time fence overschrijven** en voer in het **Time fence automatische fiattering (dagen)** het aantal dagen in.
- Als u de gedefinieerde time fence voor fiattering voor de behoefteplanningsgroep en artikelbehoefteplanning voor een specifiek hoofdplan wilt overschrijven, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Hoofdplannen** en selecteert u een hoofdplan. Stel vervolgens op het sneltabblad **Time fence in dagen** de optie **Fiattering** in op **Ja** om het aantal dagen in te voeren.

Als automatische fiattering is ingeschakeld voor een uitvoering van de hoofdplanning waarbij wordt gebruikgemaakt van Planningsoptimalisatie, wordt het proces voor automatische fiattering uitgevoerd volgens de instellingen voor automatische fiattering. Als automatische fiattering niet is ingeschakeld of als planning wordt gestart vanaf de pagina **Nettobehoeften**, wordt het proces voor automatisch fiatteren overgeslagen.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Planningsoptimalisatie vs. de ingebouwde planningsengine voor Supply Chain Management

Zowel Planningsoptimalisatie als de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management kan worden gebruikt voor het automatisch fiatteren van geplande orders. Er zijn echter enkele belangrijke verschillen. Terwijl Planningsoptimalisatie bijvoorbeeld de orderdatum (de begindatum) gebruikt om te bepalen welke geplande orders moeten worden gefiatteerd, gebruikt de ingebouwde planningsengine voor Supply Chain Management de behoeftedatum (dat wil zeggen de einddatum). Hier volgt een overzicht van de verschillen.

**Planningsoptimalisatie**

- Automatische fiattering is gebaseerd op de orderdatum (begindatum).
- Omdat de orderdatum (begindatum) de fiattering activeert, hoeft u geen rekening te houden met de doorlooptijd als onderdeel van de time fence voor fiattering.
- Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering één week zijn.

**Ingebouwde planningsengine voor Supply Chain Management**

- Automatische fiattering is gebaseerd op de behoeftedatum (einddatum).
- Om te garanderen dat orders tijdig worden gefiatteerd, moet de time fence voor fiattering langer zijn dan de levertijd.
- Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering de levertijd plus één week zijn.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]