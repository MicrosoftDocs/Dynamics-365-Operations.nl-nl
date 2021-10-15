---
title: Voorraadtraceringsinformatie corrigeren
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om voorraadtraceringsinformatie te corrigeren.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69921651ecd0969e9cdd3cdd3740db212a1953e1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573796"
---
# <a name="correct-inventory-tracking-information"></a>Voorraadtraceringsinformatie corrigeren

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om voorraadtraceringsinformatie te corrigeren. In dit voorbeeld werken we de informatie van een batchartikel bij door een verkeerd geregistreerde batch in een andere batch te wijzigen. U kunt deze procedure met het demobedrijf USPI uitvoeren of uw eigen gegevens gebruiken. Als u uw eigen gegevens gebruikt, moet u een artikel hebben dat voor batchverwerking ingesteld is en mag de locatie niet worden gecontroleerd. U moet ook een voorraadjournaalnaam hebben ingesteld voor voorraadoverboekingen. Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.


## <a name="create-an-inventory-transfer-journal"></a>Een voorraadoverboekingsjournaal maken
1. Ga naar Overboeken.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Naam.
4. Klik op OK.

## <a name="create-journal-lines"></a>Journaalregels maken
1. Klik op Nieuw.
2. Typ of selecteer een waarde in het veld Artikelnummer.
    * Als u USPI gebruikt, selecteert u artikel M5003.  
3. Voer in het veld Hoeveelheid een getal in.
4. Klik op het tabblad Voorraaddimensies.
5. Typ of selecteer een waarde in het veld Batchnummer.
6. Typ of selecteer een waarde in het veld Locatie.
7. Typ of selecteer een waarde in het veld Magazijn.
8. Typ of selecteer een waarde in het veld Batchnummer.

## <a name="post-the-journal"></a>Het journaal boeken
1. Klik op Boeken.
2. Klik op OK.

## <a name="check-tracing-information"></a>Traceringsinformatie controleren
1. Klik op Voorraad.
2. Klik op Traceren.
3. Klik op OK.
    * Met deze traceringinformatie kunt u terug traceren van welke batch u voorraad corrigeerde.  U kunt de pagina Traceren artikel ook gebruiken om deze informatie te bekijken.  
4. Sluit de pagina.

## <a name="check-inventory-transactions"></a>Voorraadtransacties controleren
1. Klik op Voorraad.
2. Klik op Transacties.
    * Hier ziet u de transacties die werden gemaakt toen u uw journaal boekte.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]