---
title: Proces van tijd- en aanwezigheidsregistratie inschakelen
description: Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2df4695b796b4e96e01fe5dac538b344cb76b910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146716"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Proces van tijd- en aanwezigheidsregistratie inschakelen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u het salarisproces voor tijd en aanwezigheid kunt inschakelen. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Een salaristype maken met een gerelateerd salaristarief
1. Tijd en aanwezigheid > Instellingen > Salarisadministratie > Salaristypen
2. Klik op Nieuw.
3. Typ een waarde in het veld Salaristype.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Opslaan.
6. Klik op Tarieven.
    * Tarieven voor salaristypen worden ingesteld voor bepaalde tijdsintervallen en er kunnen afzonderlijke tarieven voor werknemers worden ingesteld. Het is niet altijd nodig om tarieven te maken voor salaristypen in tijd en aanwezigheid. Deze gegevens zijn mogelijk al aanwezig in het salarissysteem dat wordt gebruikt om de salarissen te genereren.  
7. Klik op Nieuw.
8. Markeer in de lijst de geselecteerde rij.
9. Voer een nummer in het veld Tarief in.
10. Klik op Opslaan.

## <a name="create-a-pay-agreement"></a>Een salarisovereenkomst maken
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Salarisovereenkomsten.
    * Tijd en aanwezigheid > Instellingen > Salarisovereenkomsten  
4. Klik op Nieuw.
5. Typ een waarde in het veld Salarisovereenkomst.
6. Typ een waarde in het veld Omschrijving.
7. Klik op Opslaan.
8. Klik op Overeenkomstregels.
9. Klik op Nieuw.
10. Markeer in de lijst de geselecteerde rij.
11. Typ of selecteer een waarde in het veld Profieltype.
12. Typ of selecteer een waarde in het veld Salaristype.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Salarisovereenkomst voor tijd- en registratiewerknemer instellen
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Tijdregistratiewerknemers.
    * Tijd en aanwezigheid > Instellingen > Tijdregistratiewerknemers  
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik op het tabblad Aanstelling.
6. Vouw de sectie Tijdregistratie uit.
7. Klik op Bewerken.
8. Typ of selecteer een waarde in het veld Salarisovereenkomst.

