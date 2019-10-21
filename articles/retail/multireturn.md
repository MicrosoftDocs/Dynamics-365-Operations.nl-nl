---
title: Artikelen voor meerdere klantorders en facturen retourneren
description: In dit onderwerp wordt de functionaliteit voor het inschakelen van retouren via meerdere klantorders en facturen in Dynamics 365 Retail beschreven.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017984"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Artikelen voor meerdere klantorders en facturen retourneren

[!include [banner](includes/banner.md)]


Er kunnen retouren worden gemaakt voor meerdere orders en facturen. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retail configureren om retouren voor meerdere klantorders en facturen te ondersteunen

1. Ga naar **Detailhandelparameters \> Klantorders**.
1. Schakel de parameter **Retouren voor meerdere orders inschakelen** in. 

## <a name="process-returns"></a>Retouren verwerken

Wanneer de parameter is ingeschakeld en de wijzigingen zijn gesynchroniseerd met de winkels, kan de kassamedewerker in de winkel meerdere verkooporders voor een klant selecteren voor retour.

Wanneer de orders zijn geselecteerd, wordt een lijst met alle retourneerbare producten voor alle facturen voor de orders weergegeven. De kassamedewerker kan vervolgens de te retourneren producten selecteren. Er wordt één retourorder gemaakt voor de geselecteerde producten.
