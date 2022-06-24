---
title: Basiswijziging in belastingberekeningen van ICMS-DIF voor producten van leveranciers in andere staten
description: In dit artikel wordt de configuratie beschreven voor berekeningen van het ICMS-DIF-belastingtype wanneer een belastingdocument wordt ontvangen in de Braziliaanse staat Rio Grande do Sul (RS) of São Paulo (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868257"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Basiswijziging in belastingberekeningen van ICMS-DIF voor producten van leveranciers in andere staten

In dit artikel wordt de configuratie beschreven voor berekeningen van het **ICMS-DIF**-belastingtype wanneer een belastingdocument wordt ontvangen in de Braziliaanse staat Rio Grande do Sul (RS) of São Paulo (SP).

Volgens de bepalingen van de staatswetten moet voor de geïnde Imposto sobre Circulação de Mercadorias e Serviços (ICMS) deze regel worden gevolgd:

*Te innen ICMS* = ([(*Bewerkingsbedrag* – *ICMS van bron*) ÷ (1 – *ICMS % intern*)] × *ICMS % intern*) – *ICMS-bedrag van bron*

## <a name="example"></a>Voorbeeld

Een Braziliaans bedrijf in de staat RS ontvangt een belastingdocument voor een inkoop van een leverancier in de staat SP. Het bedrijf moet het percentageverschil van ICMS tussen de staat RS (18 procent) en de staat SP (12 procent) innen. De basis moet echter worden berekend volgens de voorgaande regel.

- **Bewerkingsbedrag:** 1.000,00 Braziliaanse real (R$ 1.000,00)
- **ICMS interstate:** R$ 120,00
- **ICMS-percentage in de staat RS:** 18 procent
- **Te innen ICMS in de staat de RS:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Oplossing

Als u het ICMS-verschil (ICMS-DIF) wilt berekenen volgens de regels van de staat RS, moet u btw-codes en een btw-groep als volgt instellen:

1. Maak een btw-code om 12 procent ICMS (voor de andere staat) te ontvangen. Deze code wordt gebruikt om het te ontvangen btw-bedrag van de leverancier te registreren.
2. Maak een btw-code om ICMS-DIF te innen. Deze btw-code moet een percentagebedrag van 18 procent (voor uw eigen staat) hebben om het verschil tussen 18 procent en 12 procent te definiëren. Stel het btw-type in op **ICMS-DIF**. Deze btw-code moet als volgt worden gedefinieerd in de berekeningsparameters:

    - Selecteer in het veld **Oorsprong** de optie **Percentage van brutobedrag**.
    - Selecteer in het veld **Marginale basis** de optie **Nettobedrag per regel** of **Nettobedrag van factuursaldo**.
    - Definieer de belastingcode zodat deze een fiscale waarde van **3** heeft. Op deze manier wordt de correctietransactie automatisch gemaakt wanneer de module **Belastingboeken** wordt ingeschakeld.
    - Selecteer in de configuratie van de btw-groep de optie **Gebruiksbelasting** voor de btw-code **ICMS-DIF**.
