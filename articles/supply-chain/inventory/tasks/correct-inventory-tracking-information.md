---
title: Voorraadtraceringsinformatie corrigeren
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadoverboekingjournaal om voorraadtraceringsinformatie te corrigeren.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204189"
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

