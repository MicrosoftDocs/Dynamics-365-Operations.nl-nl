---
title: Informatiecodes en informatiecodegroepen
description: Dit artikel geeft een overzicht over infocodes, de groepen infocodes, en hoe ze worden gebruikt.
author: mugunthanm
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailInfocodeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 22761
ms.assetid: 99877dba-a6e3-4d88-ba0a-ee5913aea17e
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d4ab9b8546ee5b13edcb86b3e09004130eaeec07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797015"
---
# <a name="info-codes-and-info-code-groups"></a>Informatiecodes en informatiecodegroepen

[!include [banner](includes/banner.md)]

Dit artikel geeft een overzicht over infocodes, de groepen infocodes, en hoe ze worden gebruikt.

Informatiecodes zijn een manier om gegevens te registreren in een kassa in een verkooppunt (POS). U kunt informatiecodes gebruiken om de kassier te vragen om informatie in te voeren tijdens verschillende acties op de POS, zoals artikelverkopen, artikelretouren of bij het selecteren van klanten. Kassiers kunnen informatie selecteren uit een lijst of deze invoeren als code, nummer, datum of tekst. U kunt informatiecodes toewijzen aan vooraf gedefinieerde winkelacties, detailhandelartikelen, betalingsmethoden, klanten en bepaalde POS-activiteiten. U kunt informatiecodes gebruiken om het volgende te doen:

- Aanvullende informatie vastleggen die nodig is op het moment van de transactie, zoals een vluchtnummer of de reden voor een retour.
- De kassamedewerker vragen een lijstprijs te selecteren voor specifieke producten.
- Koppel een subcode aan een informatiecode om de kassamedewerker om invoer te vragen wanneer hij of zij een bepaalde activiteit uitvoert. Wanneer een klant bijvoorbeeld een product retourneert, kunt u de kassier vragen waarom het product wordt geretourneerd. Vervolgens kunt u subcodes gebruiken om een lijst met redenen weer te geven waaruit de kassier kan kiezen.
- Een product verkopen als een normaal geprijsd product, een product met korting of een gratis product.
- Vraag de kassamedewerker een waarde in te voeren of een selectie te maken in een lijst subcodes als de kassalade wordt geopend zonder een verkoopactie uit te voeren.

## <a name="info-codes-group"></a>Infocodegroep

In Commerce kunt u groepen informatiecodes maken. Informatiecodegroepen bieden flexibiliteit doordat u minder informatiecodes moet definiëren maar deze wel op veelzijdigere manieren kunt gebruiken. U kunt informatiecodegroepen op de volgende manieren gebruiken:

- Definieer minder informatiecodes en gebruik deze gemakkelijk opnieuw. De informatiecodes die zijn opgenomen in informatiecodegroepen, hebben geen vooraf gedefinieerde afhankelijkheden van andere informatiecodes. U kunt dezelfde informatiecode opnemen in meerdere informatiecodegroepen en vervolgens prioriteiten gebruiken om dezelfde informatiecodes in de order te gebruiken volgens specifieke situaties.
- Koppel informatiecodes aan andere informatiecodes of informatiecodegroepen om informatie te verzamelen over een product of transactie zonder daarvoor een afzonderlijke informatiecode of bijbehorende informatiecode te moeten definiëren voor elk scenario.

## <a name="info-code-examples"></a>Voorbeelden van informatiecodes

**Voorbeeld 1: Informatiecodes hergebruiken**

U kunt informatiecodes koppelen zodat bij activering van een informatiecode onmiddellijk ook een andere informatiecode wordt geactiveerd. Als u bijvoorbeeld bepaalde producten verkoopt, kunt u de kassier vragen om de klant te vragen of ze batterijen en een productgarantie willen kopen. Bij andere producten kunt u de kassier laten vragen of de klant batterijen wil kopen en zijn/haar postcode wil geven. Als u gekoppelde informatiecodes maakt voor deze scenario's, moet u elke variatie van de informatiecode zo instellen dat de kassier wordt gevraagd om de juiste informatie te vragen. Als u informatiecodegroepen gebruikt, kunnen algemene informatiecodes zoals het vragen om batterijen, eenmalig worden ingesteld en vervolgens opnieuw worden gebruikt in meerdere informatiecodegroepen. U kunt ook prioriteiten instellen voor de informatiecodegroepen om de volgorde te bepalen waarin de vragen worden weergegeven.

**Voorbeeld 2: Informatiecodes koppelen aan informatiecodegroepen**

Als u bepaalde producten verkoopt, bijvoorbeeld mobiele apparaten, wilt u altijd specifieke informatie verzamelen, zoals een telefoonnummer, mobiele uitrustingsidentificatie (MEID) en serienummer. U wilt echter ook andere informatie verzamelen voor een tablet dan bij een mobiele telefoon. U kunt een informatiecodegroep instellen die vragen bevat voor het telefoonnummer, MEID en het serienummer en vervolgens de informatiecodegroep koppelen aan een afzonderlijke informatiecode. Wanneer de productspecifieke informatiecode wordt geactiveerd, kan de informatiecodegroep vervolgens worden geactiveerd zodat u de gemeenschappelijke gegevens kunt verzamelen zonder daarvoor meerdere sets gekoppelde informatiecodes te definiëren voor elk apparaat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]