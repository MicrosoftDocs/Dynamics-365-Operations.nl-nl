---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: c36fe4c8376ad0364516c0268965c798e20436c6
ms.sourcegitcommit: 3a9599e9b9458434c0e44d295eabd2304c5650be
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334420"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikelen voor meerdere klantorders en facturen retourneren

[!include [banner](includes/banner.md)]


Er kunnen retouren worden gemaakt voor meerdere orders en facturen. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Commerce configureren om retouren voor meerdere klantorders en facturen te ondersteunen

1. Ga naar **Commerce-parameters \> Klantorders**.
1. Schakel de parameter **Retouren voor meerdere orders inschakelen** in. 

## <a name="process-returns"></a>Retouren verwerken

Wanneer de parameter is ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.

Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven. De kassamedewerker kan vervolgens de te retourneren producten selecteren. Er wordt één retourorder gemaakt voor de geselecteerde producten.
