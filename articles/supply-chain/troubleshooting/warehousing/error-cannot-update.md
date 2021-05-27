---
title: Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst
description: Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026389"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a>Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst

KB-nummer: 4613106

## <a name="symptoms"></a>Symptomen

Dit probleem treedt op wanneer uw systeem is geconfigureerd voor het automatisch reserveren van verkooporders. Als u de locatie voor een registratieregel van de orderverzamellijst probeert te selecteren, wordt het volgende foutbericht weergegeven wanneer u reserveringsprocessen van magazijnbeheer (WMS) gebruikt:

> Kan hoeveelheid niet bijwerken met nieuwe dimensies

Dit probleem kan optreden omdat u niet voldoende voorhanden voorvoorraad op een opgegeven locatie hebt.

## <a name="resolution"></a>Oplossing

Dit gedrag van het systeem is inherent aan het ontwerp.

In scenario's waarin u het reserveringsproces op magazijnniveau gebruikt, is het aan te raden om het handmatige reserveringsproces te gebruiken voor de orderverzamelregel, als de voorhanden voorraad niet op alle voorraaddimensieniveaus wordt gereserveerd en u niet over voldoende voorhanden voorraad op een bepaalde locatie beschikt. U kunt vervolgens de functie *Partij reserveren* gebruiken om de lagere reserveringen, zoals locatie, voor alle beschikbare voorhanden hoeveelheden te verdelen.
