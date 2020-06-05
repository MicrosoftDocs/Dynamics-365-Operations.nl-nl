---
title: Voorbeeldleverancierscheques voor elektronische rapportage
description: Dit onderwerp biedt algemene informatie over het gebruik van de voorbeeldcheque-indelingen voor elektronische rapportage.
author: ShylaThompson
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4ce9c9d5b5def386f159df581c87d48f3e0b0ad9
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367310"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Voorbeeldleverancierscheques voor elektronische rapportage

[!include [banner](../includes/banner.md)]

U kunt elektronische rapportage (ER) gebruiken voor het opmaken van cheques voor leveranciers. Veel bankspecifieke en cheque-aanbiedersspecifieke indelingen zijn beschikbaar op de markt. Er zijn voorbeeldcheque-indelingen opgenomen in het betalingschequemodel in de opslagplaats van het ER-hulpprogramma. Deze voorbeeldcheques hebben de naam **Check in the middle (US)** en **Check on top stub below (US)**.

## <a name="what-check-formats-are-currently-supported"></a>Welke cheque-indelingen worden momenteel ondersteund?

U moet altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de huidige lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben. In het volgende gedeelte, 'Wat moet ik instellen?', vindt u een koppeling naar een onderwerp waarin wordt uitgelegd hoe u een LCS-opslagplaats maakt zodat u beschikbare configuraties kunt bekijken en geselecteerde configuraties kunt importeren.

Microsoft Dynamics 365 Finance bevat bovendien een voorbeeldindeling waarin de cheque bovenaan staat, gevolgd door twee remisesecties. Het bevat bovendien een voorbeeldindeling waarin de cheque in het midden staat, tussen twee remisesecties. Deze voorbeeldindelingen komen overeen met Deluxe-bedrijfscheque-indelingen.

## <a name="what-do-i-have-to-set-up"></a>Wat moet ik instellen?

- Voordat u cheques kunt afdrukken met ER, moet er ten minste één actieve chequeconfiguratie in uw ER-configuraties worden geïmporteerd. Zie voor instructies het onderwerp [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Wanneer u Contanten en bankbeheer-cheques voor de bankrekening configureert, schakelt u het selectievakje **Algemene elektronische exportindeling** in en selecteert u vervolgens de juiste cheque-indeling als een export-indelingsconfiguratie.
- U moet ook het aantal bonregels opgeven dat wordt afgedrukt op de remise. Zorg ervoor dat u de koptekstrijen opneemt als u dit aantal berekent. Het aanbevolen aantal bonregels voor de twee voorbeeldcheque-indelingen is 17. Dit aantal varieert echter, afhankelijk van uw chequevoorraad en uw printerstuurprogramma's.
- Het is raadzaam dat u een testcheque afdrukt om de chequelay-out te controleren. Selecteer de optie **Proefafdruk** om een testcheque af te drukken. De voorbeeldcheque-indelingen werken het beste als **Marges** is ingesteld op **Geen** in de geavanceerde printereigenschappen voor Microsoft Excel. Nadat de testcheque is gegenereerd, schakelt u de bewerking van de Excel-uitvoer in en configureert u de paginalay-out zodanig dat alle marges zijn ingesteld op **0** (nul). Vergelijk de testkopie van de cheques met uw chequevoorraad en pas de instellingen aan totdat u tevreden met de uitlijning bent.
- Wanneer u betalingen genereert voor de geconfigureerde bankrekening in het betalingsjournaal, worden de cheques afgedrukt met behulp van de opgegeven indeling.

Zie [Een indeling voor elektronische aangifte wijzigen](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md) voor meer informatie.
