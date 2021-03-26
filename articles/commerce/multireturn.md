---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Dynamics 365 Commerce beschreven.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4d1be6606793d498d01be91de6205e3a45c6dfdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251254"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikelen voor meerdere klantorders en facturen retourneren

[!include [banner](includes/banner.md)]


In dit artikel worden twee functies beschreven die het retourneren van klantorders voor meerdere facturen optimaliseren. 

## <a name="enable-refunds-over-multiple-captures"></a>Restituties via meerdere registraties inschakelen

Met deze functie worden meerdere gekoppelde terugbetalingen mogelijk voor dezelfde klantorder. 

1. Ga naar het werkgebied **Functiebeheer** en zoek naar **Restituties via meerdere registraties inschakelen**.
2. Selecteer **Restituties via meerdere orders inschakelen** en klik vervolgens op **Inschakelen**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen

Deze functie zorgt ervoor dat wanneer een order wordt geretourneerd met meerdere facturen, de btw uiteindelijk gelijk is aan het oorspronkelijke aangerekende btw-bedrag. 

1. Ga naar het werkgebied **Functiebeheer** en zoek naar **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen**.
2. Selecteer **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen** en klik vervolgens op **Inschakelen**. 


## <a name="process-returns"></a>Retouren verwerken

Wanneer deze functies zijn ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.

Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven. De kassamedewerker kan vervolgens de te retourneren producten selecteren. Er wordt één retourorder gemaakt voor de geselecteerde producten.

Als de order volledig is geretourneerd, is het btw-bedrag dat aan de klant is geretourneerd, gelijk aan het oorspronkelijk aangerekende btw-bedrag.



[!INCLUDE[footer-include](../includes/footer-banner.md)]