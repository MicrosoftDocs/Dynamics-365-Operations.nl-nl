---
title: Magazijnvoorraadcorrectie
description: Dit onderwerp bevat informatie over het Magazijnvoorraadcorrectiejournaal en de verwerking wanneer u schaaleenheden gebruikt.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938221"
---
# <a name="warehouse-inventory-adjustment"></a>Magazijnvoorraadcorrectie

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

De functie Magazijnvoorraadcorrectie wordt gebruikt wanner u cloud- en randschaaleenheden gebruikt voor [productieworkloads](cloud-edge-workload-manufacturing.md) en [magazijnbeheerworkloads](cloud-edge-workload-warehousing.md).

Wanneer een werknemer een voorraadcorrectie uitvoert met de magazijnapp op een magazijnbeheerworkload met schaaleenheden, moet de update van de fysieke voorhanden voorraad worden verwerkt door de batchtaak **Magazijnvoorraadcorrectiejournaal**, die u uitvoert en inplant via **Magazijnbeheer > Periodieke taken > Magazijnvoorraadcorrectiejournaal**.

In de volgende magazijnapp-werkprocessen wordt momenteel het **Magazijnvoorraadcorrectiejournaal** gebruikt voor workloads met schaaleenheden:

- Correctie in/uit
- Cyclustelling
- Nummerplaatlading

Tijdens het voorraadcorrectieproces worden verschillende voorraadtransacties gemaakt als onderdeel van cloud en edge, omdat de implementaties van hub en schaaleenheden de voorraadrecords delen.

## <a name="inventory-adjustment-example"></a>Voorbeeld van voorraadcorrectie

In dit voorbeeld heeft een magazijnmedewerker de magazijnapp gebruikt om het toevoegen van de voorhanden voorraad te registreren.

Als eerste wordt door de schaaleenheidworkload een voorraadcorrectietransactie voor het magazijn gemaakt voor de positieve fysieke correctie, die vervolgens wordt gesynchroniseerd naar de hub en resulteert in een toename van de voorhanden voorraad in de hub.

| Type                                    | Schaaleenheid | Richting | Hub |
|-----------------------------------------|------------|-----------|-----|
| Magazijnvoorraadcorrectie          | +1         | ->        | +1  |

De hub verwerkt vervolgens een tellingsjournaalboeking, die wordt ontvangen via [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md). Hiermee wordt de extra voorhanden voorraad bijgewerkt. Om te voorkomen dat er dubbele voorraad voorhanden is, wordt door de hub een tegenboekingstransactie gemaakt als onderdeel van dit proces en wordt de eerder geregistreerde voorhanden voorraad verwijderd die is gerelateerd aan de correctie van de magazijnvoorraad.

| Type                                    | Schaaleenheid | Richting | Hub |
|-----------------------------------------|------------|-----------|-----|
| Tellen                                | +1         | <-        | +1  |
| Magazijnvoorraadcorrectie (tegenboeking) | -1         | <-        | -1  |

Nadat met een schaaleenheid een **magazijnvoorraadcorrectiejournaal** is gemaakt op de hub, kunt u zowel het **Tellingsjournaal** als het **Tegenboekingsjournaal** controleren, die door de hub worden gemaakt als onderdeel van het correctieproces.

U kunt elk van deze journaalposten en -transacties controleren in Supply Chain Management door de volgende stappen uit te voeren:

1. Meld u aan bij de schaaleenheid.
1. Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.
1. Zoek op de pagina **Magazijnvoorraadcorrectiejournaal** het journaal waarin de wijziging in de voorhanden voorraad is vastgelegd en open het. In de sectie **Journaalregels** ziet u elke correctie die door dit journaal is geregistreerd.
1. Meld u aan bij de hub.
1. Ga naar **Magazijnbeheer \> Periodieke taken \> Magazijnvoorraadcorrectiejournaal**.
1. Op de pagina **Magazijnvoorraadcorrectiejournaal** moet hetzelfde journaal worden weergegeven, als de hub en de schaaleenheid zijn gesynchroniseerd.
1. Open het journaal. Als de [berichten van berichtenverwerker](cloud-edge-message-processor-messages.md) zijn verwerkt, ziet u koppelingen naar het **Tellingsjournaal** en het **Tegenboekingsjournaal** in de koptekst.
    - In het **Tellingjournaal** moeten dezelfde dimensiewaarden worden staan als in de journaalregels.
    - In het **Tegenboekingsjournaal** moet de tegenboeking zijn opgenomen, waarmee de dubbele voorraadcorrectie wordt verwijderd.
    > [!NOTE]
    > Wanneer de synchronisatie en verwerking helemaal zijn voltooid, worden het **Tellingjournaal** en het **Tegenboekjournaal** teruggesynchroniseerd naar de schaaleenheid. Deze kunt u ook weergeven op de relevante pagina **Magazijnvoorraadcorrectiejournaal**.
