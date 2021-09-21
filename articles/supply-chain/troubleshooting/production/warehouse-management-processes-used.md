---
title: Momenteel worden warehouse managementprocessen gebruikt
description: Wanneer u werk reserveert of vrij geeft, ziet u mogelijk een bericht dat momenteel warehouse managementprocessen worden gebruikt. Los het probleem met een van deze stappen op.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475964"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Kan geen werk reserveren of vrijgeven omdat processen momenteel worden gebruikt

## <a name="symptoms"></a>Symptomen

Wanneer u met discrete productie werkt, wordt de volgende foutbericht weergegeven:

> Momenteel worden warehouse managementprocessen gebruikt. Als er nog geen werkregels zijn geregistreerd, kunt u het gemaakte werk en eventuele ladings- of zendingsregels annuleren en doorgaan met het orderverzamel- of verzendproces.

## <a name="cause"></a>Oorzaak

Dit probleem treedt op als u het werk voor een regel wilt reserveren of vrijgeven, maar de voorraadtransactie heeft de status *Opgenomen*. Dit betekent dat het materiaal is verzameld.

## <a name="resolution"></a>Oplossing

Volg een van deze stappen om dit probleem op te lossen.

- Wijzig de status van de productieorder weer in *Geraamd* of *Vrijgegeven*.
- Open de detailspagina voor de desbetreffende productieorder. Selecteer in het actievenster, op het tabblad **Magazijn** in de groep **Stoppen**, **Stoppen en verzameling opheffen** om alle verzamelde transacties op te opheffen. Selecteer vervolgens **Stop verwijderen** om de productieorder te verwerken.

Hier volgt een uitleg van de functies *Opheffen* en *Stoppen*:
  
- **Opheffen**: met deze functie wordt de status omgekeerd van voorraadtransacties voor stuklijstregels en formuleregels die een status hebben van *Opgenomen* tot en met *Op order*. Wanneer het werk voor het orderverzamelen van grondstoffen wordt voltooid, wordt de status van de regels ingesteld op *Opgenomen*. Deze status voorkomt dat de productieorder opnieuw wordt ingesteld op de status *Gemaakt*. In dat geval kunt u de functie *Opheffen* niet gebruiken om de transacties van de status *Opgenomen* terug te zetten en vervolgens de productieorder opnieuw in te stellen op de status *Gemaakt*.
- **Stoppen**: met deze functie stelt u een vlag **Gestopt** op de productieorder in om te voorkomen dat de orderstatus wordt bijgewerkt. U kunt de vlag **Gestopt** vinden op het sneltabblad **Magazijn** van de pagina Details van de productieorder.

> [!NOTE]
>
> - De knoppen zijn alleen zichtbaar wanneer de productieorder wordt gemaakt voor artikelen die zijn ingeschakeld voor magazijnprocessen.
> - De groep **Stoppen** is alleen zichtbaar op het tabblad **Magazijn** in het actievenster van de pagina Details van de productieorder. Het is niet zichtbaar op het sneltabblad **Magazijn** van de lijstpagina **Productieorder**.
