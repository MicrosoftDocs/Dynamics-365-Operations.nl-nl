---
title: Een boekstuknummer van een productontvangstbon wordt verbruikt, zelfs wanneer er geen boekstuk wordt gegenereerd
description: Er wordt een boekstuknummer voor de productontvangstbon verbruikt, zelfs als er tijdens de productontvangst geen financieel boekstuk is gegenereerd
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0556969950c45e80d177a0e96096c4157d690ae3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476006"
---
# <a name="a-product-receipt-voucher-number-is-consumed-even-when-not-generating-a-voucher"></a>Een boekstuknummer van een productontvangstbon wordt verbruikt, zelfs wanneer er geen boekstuk wordt gegenereerd

## <a name="symptoms"></a>Symptomen

Er wordt een boekstuknummer voor de productontvangstbon verbruikt, zelfs als er tijdens de productontvangst geen financieel boekstuk is gegenereerd.

## <a name="resolution"></a>Oplossing

Als de optie **Toerekening van aansprakelijkheid bij productontvangstbon** is ingesteld op *Nee* voor de artikelmodelgroep, worden er geen boekingen naar het grootboek uitgevoerd. Er wordt echter een fysieke gebeurtenis voor de boekhouding in een subadministratie geregistreerd en voor die gebeurtenis is een boekstuknummer vereist. Dit boekstuknummer is het boekstuknummer waarnaar in de voorraadtransacties wordt verwezen.

Het is raadzaam om de optie **Toerekening van aansprakelijkheid bij productontvangstbon** in te stellen op *Ja*, zoals wordt beschreven in het volgende blogbericht: [Diverse toeslagen boeken op het moment van ontvangst van het product](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
