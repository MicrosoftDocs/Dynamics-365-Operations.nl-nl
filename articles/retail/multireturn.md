---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Microsoft Dynamics 365 for Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517037"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikelen voor meerdere klantorders en facturen retourneren

[!include [banner](includes/banner.md)]


In Dynamics 365 for Finance and Operations versie 10.0 kunnen retouren voor meerdere orders en facturen worden gemaakt terwijl in eerdere versies dan 10.0 retouren slechts op basis van één factuur tegelijk konden worden verwerkt. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retail configureren om retouren voor meerdere klantorders en facturen te ondersteunen

1. Ga naar **Detailhandelparameters \> Klantorders**.
1. Schakel de parameter **Retouren voor meerdere orders inschakelen** in. 

## <a name="process-returns"></a>Retouren verwerken

Wanneer de parameter is ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.

Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven. De kassamedewerker kan vervolgens de te retourneren producten selecteren. Er wordt één retourorder gemaakt voor de geselecteerde producten.
