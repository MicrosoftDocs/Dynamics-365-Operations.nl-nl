---
title: Voorbeeldleverancierscheques voor elektronische rapportage
description: Dit onderwerp biedt algemene informatie over het gebruik van de voorbeeldcheque-indelingen voor elektronische rapportage.
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a8ba439ff643fce4811be9224a3edf96b2b9025c
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Voorbeeldcheque-indelingen voor elektronische rapportage

U kunt elektronische rapportage (ER) gebruiken voor het opmaken van cheques voor leveranciers. Veel bankspecifieke en cheque-aanbiedersspecifieke indelingen zijn beschikbaar op de markt. Er zijn voorbeeldcheque-indelingen opgenomen in het betalingschequemodel in de opslagplaats van het ER-hulpprogramma. Deze voorbeeldcheques hebben de naam **Check in the middle (US)** en **Check on top stub below (US)**.

## <a name="what-check-formats-are-currently-supported"></a>Welke cheque-indelingen worden momenteel ondersteund?

U moet altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de huidige lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben. In het volgende gedeelte, 'Wat moet ik instellen?', vindt u een koppeling naar een onderwerp waarin wordt uitgelegd hoe u een LCS-opslagplaats maakt zodat u beschikbare configuraties kunt bekijken en geselecteerde configuraties kunt importeren.

Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition bevat een voorbeeldindeling waarbij de cheque bovenaan staat, gevolgd door twee remisesecties. Het bevat bovendien een voorbeeldindeling waarin de cheque in het midden staat, tussen twee remisesecties. Deze voorbeeldindelingen komen overeen met Deluxe-bedrijfscheque-indelingen.

## <a name="what-do-i-have-to-set-up"></a>Wat moet ik instellen?

- Voordat u cheques kunt afdrukken met ER, moet er ten minste één actieve chequeconfiguratie in uw ER-configuraties worden geïmporteerd. Zie voor instructies het onderwerp [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
- Wanneer u Contanten en bankbeheer-cheques voor de bankrekening configureert, schakelt u het selectievakje **Algemene elektronische exportindeling** in en selecteert u vervolgens de juiste cheque-indeling als een export-indelingsconfiguratie.
- U moet ook het aantal bonregels opgeven dat wordt afgedrukt op de remise. Zorg ervoor dat u de koptekstrijen opneemt als u dit aantal berekent. Het aanbevolen aantal bonregels voor de twee voorbeeldcheque-indelingen is 17. Dit aantal varieert echter, afhankelijk van uw chequevoorraad en uw printerstuurprogramma's.
- Het is raadzaam dat u een testcheque afdrukt om de chequelay-out te controleren. Selecteer de optie **Proefafdruk** om een testcheque af te drukken. De voorbeeldcheque-indelingen werken het beste als **Marges** is ingesteld op **Geen** in de geavanceerde printereigenschappen voor Microsoft Excel. Nadat de testcheque is gegenereerd, schakelt u de bewerking van de Excel-uitvoer in en configureert u de paginalay-out zodanig dat alle marges zijn ingesteld op **0** (nul). Vergelijk de testkopie van de cheques met uw chequevoorraad en pas de instellingen aan totdat u tevreden met de uitlijning bent.
- Wanneer u betalingen genereert voor de geconfigureerde bankrekening in het betalingsjournaal, worden de cheques afgedrukt met behulp van de opgegeven indeling.

Zie [Een indeling voor elektronische aangifte wijzigen](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template) voor meer informatie.
