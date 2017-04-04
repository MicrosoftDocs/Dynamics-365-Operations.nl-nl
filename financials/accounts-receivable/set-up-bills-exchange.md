---
title: Wissels instellen
description: In dit onderwerp beschrijft de stappen voor het instellen van wissels.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Wissels instellen

In dit onderwerp beschrijft de stappen voor het instellen van wissels.

Een wissel is een geschreven of elektronische order van een klant die aangeeft dat een andere partij, meestal een bank, een opgegeven bedrag aan het bedrijf moet betalen. Wanneer u een wissel als betaling gebruikt voor een verkooporderfactuur of vrije-tekstfactuur, wordt er een bedrag op de klantrekening bijgeschreven. Dit bedrag wordt gedekt door de wissel totdat de klant de wissel betaalt aan de bank. Meestal vereffent u de factuur met de wissel op de vervaldatum. Wanneer u een bericht ontvangt van uw bank dat de wissel is gehonoreerd, kunt u de wissel sluiten. U kunt een wissel trekken via uw bank op een van de volgende momenten:

-   Op de vervaldatum. Deze aanpak wordt aangeduid als remise ter incasso.
-   Vóór de vervaldatum, meestal op de datum die is opgegeven in de geselecteerde betalingstermijn die zijn ingesteld voor de klant. Wanneer u de transactie boekt, wordt het kortingsbedrag geboekt naar een onkostenrekening. Het resterende bedrag is voor uw eigen risico totdat de bank de betaling ontvangt van de klant. Deze benadering wordt de rekening Discontoremise korting genoemd.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Boekingsprofielen voor wissels instellen
Gebruik de **boekingsprofielen van klant** pagina die u met wissels, geprotesteerde wissels, remises ter incasso en discontoremises gebruiken kunt boekingsprofielen instellen. In de **totaalrekening** veld, selecteert u de totaalrekening wisselbedragen wilt boeken. Deze rekening wordt gedebiteerd of gecrediteerd, afhankelijk van het type wisseltransactie:
-   Voor wissels, worden deze rekening wordt gedebiteerd wanneer een wissel wordt geboekt en gecrediteerd wanneer een discontoremise of een remise ter incasso wordt geboekt.
-   Voor geprotesteerde wissels geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een geprotesteerde wissel wordt geboekt.
-   Voor remises ter incasso geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een remise ter incasso wordt geboekt.
-   Voor discontoremises geldt dat er van deze rekening een bedrag wordt afgeschreven wanneer een discontoremise wordt geboekt.

In de **rekening vereffenen** veld, selecteer de kasrekening wisselbedragen wilt boeken. Van deze rekening wordt een bedrag afgeschreven wanneer een wissel wordt vereffend. In de **btw-vooruitbetalingen** veld, selecteert u de totaalrekening voor het boeken van btw-bedragen wanneer er wissels worden gebruikt voor vooruitbetalingen. In de **verplichtingen voor discontorekening** veld, de rekening waarnaar het kortingsbedrag voor discontoremises te selecteren. Op deze rekening wordt een bedrag bijgeschreven wanneer er een discontoremise wordt geboekt.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Accounts receivable parameters voor wissels instellen
Op de **parameters van module klanten** pagina standaard boekingsprofielen voor wissels worden ingevoerd op de **grootboek en omzetbelasting** tabblad. Nummerreeksen zijn gedefinieerd op de **nummerreeksen** tabblad.
Journaalnamen voor wissels instellen
------------------------------------------

Op de **journaalnamen** pagina, minimaal vijf journaalnamen voor wissels maken. Hier volgen de journaaltypen:
-   **Door klant getrokken wissel** : Maak een journaalnaam voor het journaal met getrokken wissels.
-   **Door klant geprotesteerde wissel** : Maak een journaalnaam voor het journaal met geprotesteerde wissels.
-   **Door klant hertrokken wissel** : Maak een journaalnaam voor het journaal met hertrokken wissels.
-   **Bankremise van klant** : Maak een journaalnaam voor het remisejournaal.
-   **Door klant afgerekende wissel** : Maak een journaalnaam voor het journaal met afgerekende wissels.

Klik op de pagina journaal boekstuk voor elk wisseljournaal informatie invoeren over de wissel op de **wissel** tabblad. Nadat de wissel-journaalregels zijn geboekt, kunt u deze bekijken op de **wissel journaal query** pagina en de **Wisselstatistieken** pagina.
Betalingsmethoden voor wissels instellen
-----------------------------------------------

Op de **betalingsmethoden** pagina ten minste één betalingsmethode voor wissels instellen. Als u zaken met meer dan een bank doet, stelt u een betalingsmethode die overeenkomt met de indeling die elke bank voor wissels vereist.
Bijzondere betalingskosten voor wissels instellen
-----------------------------------------

Bijzondere betalingskosten zijn kosten die worden gemaakt bij het innen van betalingen van klanten. Meerdere instelling voor betalingskosten regels kunnen worden alle bijzondere betalingskosten die zijn gekoppeld. U kunt regels gebruiken om te bepalen hoe standaardbedragen voor betalingskosten worden berekend. U kunt bijvoorbeeld instellingsregels maken voor betalingsmethoden, betalingsspecificaties, valuta's en perioden. U kunt ook instellingsregels maken voor een percentage of bedrag dat is gebaseerd op dagintervallen. U kunt bijvoorbeeld een rentepercentage op basis van hoe lang die een betaling al achterstallig is instellen. Als de bank verschillende bedragen voor verschillende remisetypen, zoals rekent **verzameling** of **korting**, een afzonderlijke regel van de bijzondere kosten voor elk remisetype instellen.
Bijzondere remisekosten voor bankremisebestanden instellen
------------------------------------------------

Op de **bankrekeningen** pagina, u kunt bijzondere remisekosten instellen dat een bank berekent voor elk remisebestand dat wordt gegenereerd. De bijzondere remisekosten worden geboekt wanneer de remise is bevestigd en de bedragen voor bijzondere kosten bekend zijn. Bijzondere remisekosten verschillen van betalingskosten, die worden verzameld van klanten en gekoppeld aan journaalregels.
Documentindelingen voor wissels instellen
---------------------------------------------

Op de **bankrekeningen** pagina, klikt u op **instellen**, en geef de documentlay-out die is vereist voor elke bankrekening dat u afgedrukte wissels wilt genereren voor documenten.
Klanten voor wissels instellen
--------------------------------------

Op de **klanten**, voor elke klant die is overeengekomen te betalen met behulp van een wissel, kunt u een standaardbetalingsmethode voor wissels ingesteld op de **wanbetalingen** tabblad.




