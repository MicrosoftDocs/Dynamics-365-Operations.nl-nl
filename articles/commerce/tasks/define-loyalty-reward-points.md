---
title: " Beloningspunten voor loyaliteit definiëren"
description: Deze procedure doorloopt het definiëren van loyaliteitsbeloningspunten.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyRewardPoints
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e40ebcbf3ab1befc641ae34571a8b974bd0425a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140871"
---
# <a name="define-loyalty-reward-points"></a> Beloningspunten voor loyaliteit definiëren

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het definiëren van loyaliteitsbeloningspunten. U moet loyaliteitsbeloningspunten instellen voordat u een loyaliteitsprogramma instelt. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Retail en Commerce > Klanten > Loyaliteit > Beloningspunten voor loyaliteit.
2. Klik op Nieuw.
3. Typ een waarde in het veld Beloningspunt-id.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer een optie in het veld Type beloningspunt.
    * Selecteer Hoeveelheid als u wilt dat de beloningspunten worden afgerond op het dichtstbijzijnde gehele getal. Selecteer Bedrag als u wilt dat de beloningspunten worden afgerond volgens de valuta-afrondingsregels. Als u Hoeveelheid selecteert, slaat u de volgende stap van deze procedure over.  
6. Typ een waarde in het veld Valuta.
    * Voor beloningspunten van het type Bedrag hebben alle uitgegeven punten de geselecteerde valuta. Voor beloningspunten van het type Hoeveelheid is dit veld niet van toepassing. Sla deze stap dan over.  
7. Schakel het selectievakje Inwisselbaar in of uit.
8. Voer een getal in het veld Positie inwisselen in.
    * Positie inwisselen wordt gebruikt wanneer twee of meer inwisselbare beloningspunten kunnen worden gebruikt om voor producten te betalen. Als de twee beloningspunten dezelfde inwisselpositie hebben, wordt het punt gebruikt dat het kleinste aantal punten nodig heeft.  
9. Voer een getal in het veld Waarde vervaltijd in.
    * De beloningspunten vervallen na het opgegeven aantal dagen, maanden of jaren nadat de punten zijn uitgegeven. Een waarde van '0' betekent dat de beloningspunten nooit vervallen.  
10. Selecteer een optie in het veld Eenheid vervaltijd.
11. Klik op Opslaan.

