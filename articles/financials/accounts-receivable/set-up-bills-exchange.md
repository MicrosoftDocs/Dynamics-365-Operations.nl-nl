---
title: Wissels instellen
description: In dit onderwerp worden de stappen beschreven voor het instellen van wissels.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5ecc30116d6e0c93ca857f4d2a7ed408412c20b9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-bills-of-exchange"></a>Wissels instellen

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de stappen beschreven voor het instellen van wissels.

Een wissel is een geschreven of elektronische order van een klant, waarin wordt aangegeven dat een andere partij, meestal een bank, een opgegeven bedrag aan het bedrijf moet betalen. Wanneer u een wissel als betaling gebruikt voor een verkooporderfactuur of vrije-tekstfactuur, wordt er een bedrag op de klantrekening bijgeschreven. Dit bedrag wordt gedekt door de wissel totdat de klant de wissel betaalt aan de bank. Meestal vereffent u de factuur met de wissel op de vervaldatum. Wanneer u een bericht ontvangt van uw bank dat de wissel is gehonoreerd, kunt u de wissel sluiten. U kunt een wissel trekken via uw bank op een van de volgende momenten:

-   Op de vervaldatum. Deze benadering wordt remise ter incasso genoemd.
-   Vóór de vervaldatum, meestal op de kortingsdatum die is opgegeven in de betalingsvoorwaarden die zijn ingesteld voor de klant. Wanneer u de transactie boekt, wordt het kortingsbedrag geboekt naar een onkostenrekening. Het resterende bedrag is voor uw eigen risico totdat de bank de betaling ontvangt van de klant. Deze benadering wordt discontoremise genoemd.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Boekingsprofielen voor wissels instellen
Op de pagina **Boekingsprofielen van klant** kunt u boekingsprofielen instellen voor gebruik met wissels, geprotesteerde wissels, remises voor incasso en discontoremises. Selecteer in het veld **Totaalrekening** de totaalrekening waarop u wisselbedragen wilt boeken. Deze rekening wordt gedebiteerd of gecrediteerd, afhankelijk van het type wisseltransactie:
-   Voor wissels geldt dat een bedrag van deze rekening wordt afgeschreven wanneer een wissel wordt geboekt. Er wordt een bedrag bijgeschreven wanneer een remise ter incasso of een discontoremise wordt geboekt.
-   Voor geprotesteerde wissels geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een geprotesteerde wissel wordt geboekt.
-   Voor remises ter incasso geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een remise ter incasso wordt geboekt.
-   Voor discontoremises geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een discontoremise wordt geboekt.

Selecteer in het veld **Rekening vereffenen** de kasrekening waarop u wisselbedragen wilt boeken. Van deze rekening wordt een bedrag afgeschreven wanneer een wissel wordt vereffend. Selecteer in het veld **Btw-vooruitbetalingen** de totaalrekening waarop u btw-bedragen wilt boeken wanneer er wissels worden gebruikt voor vooruitbetalingen. Selecteer de rekening waarop u het kortingsbedrag voor discontoremises wilt boeken in het veld **Verplichtingen voor discontorekening**. Op deze rekening wordt een bedrag bijgeschreven wanneer er een discontoremise wordt geboekt.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Parameters van module Klanten instellen voor wissels
De standaardboekingsprofielen worden gedefinieerd op het tabblad **Grootboek en btw** op de pagina **Parameters van module Klanten**. Op het tabblad **Nummerreeksen** kunt u nummerreeksen definiëren. Journaalnamen voor wissels instellen
------------------------------------------

Maak op de pagina **Journaalnamen** minimaal vijf journaalnamen die u kunt gebruiken voor wissels. De volgende journaaltypen zijn beschikbaar:
-   **Door klant getrokken wissel:** Maak een journaalnaam voor het journaal met getrokken wissels.
-   **Door klant geprotesteerde wissel:** Maak een journaalnaam voor het journaal met geprotesteerde wissels.
-   **Door klant hertrokken wissel:** Maak een journaalnaam voor het journaal met hertrokken wissels.
-   **Bankremise van klant:** Maak een journaalnaam voor het remisejournaal.
-   **Door klant afgerekende wissel:** Maak een journaalnaam voor het journaal met afgerekende wissels.

Voer op de journaalboekstukpagina voor elk wisseljournaal informatie over de wissel in op het tabblad **Wissel**. Nadat de wisseljournaalregels zijn geboekt, kunt u deze bekijken op de pagina's **Query op wissel-journalen weergeven** en **Wisselstatistieken**.
Betalingsmethoden voor wissels instellen
-----------------------------------------------

Stel op de pagian **Betalingsmethoden** tenminste één betalingsmethode voor wissels in. Als u zaken doet met meer dan een bank, stelt u een betalingsmethode in die overeenkomt met de remise-indeling die iedere bank vereist voor wissels.
Bijzondere betalingskosten voor wissels instellen
-----------------------------------------

Bijzondere betalingskosten zijn kosten die worden gemaakt bij het innen van betalingen van klanten. Aan alle bijzondere betalingskosten kunnen meerdere instellingsregels voor bijzondere betalingskosten zijn gekoppeld. U kunt door middel van instellingsregels bepalen hoe standaardbedragen voor bijzondere betalingskosten worden berekend. U kunt bijvoorbeeld instellingsregels maken voor betalingsmethoden, betalingsspecificaties, valuta's en perioden. U kunt ook instellingsregels maken voor een percentage of bedrag dat is gebaseerd op dagintervallen. U kunt bijvoorbeeld een rentepercentage instellen gebaseerd op de periode dat een betaling achterstallig is. Als de bank verschillende bedragen rekent voor verschillende remisetypen, zoals **Aanmaning** of **Korting**, moet u voor elk remisetype een afzonderlijke regel voor bijzondere betalingskosten instellen.
Bijzondere remisekosten voor bankremisebestanden instellen
------------------------------------------------

Op de pagina **Bankrekeningen** kunt u bijzondere remisekosten instellen die een bank berekent voor elk remisebestand dat wordt gegenereerd. De bijzondere remisekosten worden geboekt wanneer de remise is bevestigd en de bedragen voor bijzondere kosten bekend zijn. Deze remisekosten verschillen van bijzondere betalingskosten, die worden berekend aan klanten en worden gekoppeld aan journaalregels.
Documentindelingen voor wissels instellen
---------------------------------------------

Klik op de pagina **Bankrekeningen** op **Instellingen**. Geef de documentindeling op die is vereist voor elke bankrekening waarvoor u afgedrukte wisseldocumenten wilt genereren.
Klanten voor wissels instellen
--------------------------------------

Op het tabblad **Standaardwaarden betalingen** op de pagina **Klanten** kunt u een standaardbetalingsmethode instellen voor wissels voor elke klant die akkoord is gegaan met betaling per wissel.





