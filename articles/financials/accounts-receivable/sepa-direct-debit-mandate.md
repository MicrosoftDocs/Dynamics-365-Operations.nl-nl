---
title: Mandaag voor automatische afschrijving instellen voor SEPA
description: Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 242d6d3d517ad5190b96ace36bd585a5769ae994
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="set-up-sepa-direct-debit-mandate"></a>Mandaag voor automatische afschrijving instellen voor SEPA

[!include [banner](../includes/banner.md)]

Een automatische SEPA-overschrijving maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend. De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen. Dit onderwerp is opgezet om het proces weer te geven voor het instellen van SEPA-mandaten voor automatische afschrijving.

## <a name="prerequisites"></a>Vereisten
De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

| Categorie       | Vereiste                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/regio | Het primaire adres van de rechtspersoon moet zich in de volgende landen/regio's bevinden: Oostenrijk, België, Duitsland, Spanje, Frankrijk, Italië of Nederland. |

1. Een nummerreeks instellen voor automatische overschrijvingsmandaten Elk mandaat voor automatische afschrijving moet een uniek nummer hebben. Gebruik het formulier **Nummerreeksen** om een nummerreeks voor automatische overschrijvingsmandaten te maken. U wilt deze identificatie gebruiken om de nummerreeks op het automatische overschrijvingsdebetmandaatsysteem op de pagina **Parameters van module Klanten** toe te wijzen.

2. De leveranciersparameters voor mandaten voor automatische afschrijving in stellen Op de pagina **Parameters van module Klanten** stelt u de parameters voor mandaten voor automatische afschrijving in. Als u de parameters wilt instellen, wijzigt u de standaardparameters op het tabblad **Automatische afschrijving**. Werk op het tabblad **Nummerreeksen** het veld **Mandaat-ID voor automatische afschrijving** bij met de eerder ingestelde nummerreeks.

3. Een betalingsmethode voor automatische overschrijvingsmandaten instellen U moet een betalingsmethode voor mandaten voor automatische afschrijving instellen. U gebruikt deze betalingsmethode om facturen op te vragen om automatische afschrijvingen voor te genereren. Gebruik de pagina **Betalingsmethoden** om de betalingsmethode in te stellen. Als u een betalingsmethode voor mandaten voor automatische afschrijving wilt instellen, moet u deze extra stappen voor een betalingsmethode uitvoeren:

-   Selecteer **Elektronische betaling** in het veld **Betalingstype**.
-   Optioneel: Als u verwacht dat al uw klanten meerdere mandaten hebben, selecteert u in het veld **Periode** de waarde **Factuur**. Hierdoor wordt een afzonderlijke betaling voor elke factuur gemaakt, en elke betaling gebruikt het mandaat dat voor de factuur is opgegeven.
-   Selecteer de optie **Mandaat vereisen** om betalingen te maken door mandaten voor automatische afschrijving te gebruiken. De optie **Mandaat vereisen** is alleen beschikbaar als u **Elektronische betaling** in het veld **Betalingstype** selecteert.

Aanvullende resources

[Overzicht automatische overschrijvingen](sepa-direct-debit-overview.md) 

[Een mandaat voor automatische afschrijving maken voor een klant](tasks/create-direct-debit-mandate-customer.md) 


