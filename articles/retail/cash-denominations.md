---
title: Contante denominaties voor POS configureren
description: Contante denominaties voor bankbiljetten en munten kunnen worden gedefinieerd in de backoffice voor gebruik in het POS door kassiers, verkoopmedewerkers en managers in de winkel.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: afe7c359f284fde10ada377fb19add9819a8dd21
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="configure-cash-denominations-for-pos"></a>Contante denominaties voor POS configureren

[!include [banner](includes/banner.md)]

Contante denominaties voor bankbiljetten en munten kunnen worden gedefinieerd in de backoffice voor gebruik in het POS door kassiers, verkoopmedewerkers en managers in de winkel. Deze denominaties kunnen worden gebruikt om te helpen bij het tellen van contant geld bij kascontroles aan het einde van de dag of voor snelle offertes.

## <a name="define-denominations"></a>Denominaties definiëren
De denominaties worden per winkel ingesteld op de pagina **Instellen** > **Optie contantdeclaratie van de winkeleigenschappen**. 

![contante denominaties](./media/image1-denomination.png)

Denominaties definiëren:
1. Klik op **Nieuw**.
1. Geef het type op (munt of biljet).
1. Geef het bedrag op (waarde).

![contante denominaties](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Het functionaliteitsprofiel configureren
Bij de betaling met contant geld in POS kan de gebruiker kan de denominaties gebruiken om snel het bedrag in te voeren dat is betaald door de klant. U kunt de twee opties voor het weergeven van de denominatie in het POS configureren in het functionaliteitsprofiel.

**Groter of gelijk aan het verschuldigde bedrag**: standaard worden door het POS alleen denominaties weergegeven die groter zijn dan het verschuldigde bedrag, wat one-touch offertes mogelijk maakt. Als het verschuldigde bedrag bijvoorbeeld $7,50 is, geeft het POS de volgende denominaties weer: $10, $20, $50 en $100. Als een van deze bedragen wordt aangeraakt, wordt de verkoop automatisch aangeboden voor dat bedrag. De biljetten van $1 en $5 worden niet weergegeven omdat deze bedragen kleiner dan het te betalen bedrag.

**Alle denominaties**: selecteer deze optie om altijd alle denominaties in POS weer te geven, ongeacht het betaalde bedrag. Dit betekent dat de gebruiker een combinatie van biljetten kan gebruiken voor het verschuldigde bedrag. Als het verschuldigde bedrag bijvoorbeeld $25,00 is, kan de gebruiker $20 en $5 kiezen voor het voltooien van de verkoop.

