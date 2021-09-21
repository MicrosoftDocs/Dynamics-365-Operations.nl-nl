---
title: Order verzamelen geblokkeerd vanwege onvoltooid aanvullingswerk
description: Verzamelwerk kan geblokkeerd worden vanwege afhankelijk aanvullingswerk. Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476058"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Order verzamelen kan niet worden gedeblokkeerd vanwege onvoltooid aanvullingswerk

## <a name="symptoms"></a>Symptomen

Bij gebruik van aanvulling van wave-aanvragen kan orderverzamelwerk worden geblokkeerd vanwege afhankelijk aanvullingswerk. Als er een verzamellocatie moet worden aangevuld om aan de bronordervraag te voldoen, wordt zowel het aanvullings- als het verzamelwerk aangemaakt door het systeem. Dit blokkeert echter het orderverzamelwerk totdat het aanvullingswerk is voltooid en u het volgende foutbericht ontvangt:

> Werk %1 kan niet worden gedeblokkeerd vanwege onvoltooid aanvullingswerk.

## <a name="resolution"></a>Oplossing

Dit gebeurt met opzet, omdat de verzamellocatie onvoldoende voorraad heeft, tenzij het aanvullingswerk is voltooid. Voltooi het aanvullingswerk en verwerk vervolgens het verzamelwerk.
