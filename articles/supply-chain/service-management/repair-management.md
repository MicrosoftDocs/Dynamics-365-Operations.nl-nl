---
title: Reparatiebeheer
description: U kunt problemen systematisch groeperen, zodat oplossingen worden voorgesteld die bij eerdere problemen hebben gewerkt.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAConditionTable, SMASymptomArea, SMADiagnosisArea, SMAResolutionTable, SMARepairStage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 265709f298d9310d5d647eaa029ece778d2e226e
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470636"
---
# <a name="repair-management"></a>Reparatiebeheer       

[!include [banner](../includes/banner.md)]


Bij reparatiebeheer kunt u problemen systematisch groeperen. Hierdoor worden oplossingen voorgesteld die bij eerdere problemen hebben gewerkt.

U geeft instellingen voor de symptomen, diagnose en oplossing op. Deze instellingen kunnen later worden toegepast wanneer u een vergelijkbaar artikel ontvangt voor reparatie. U kunt ook reparatiefasen instellen, zodat u de voortgang van een reparatie kunt volgen.

## <a name="setting-up-repair-management"></a>Reparatiebeheer instellen

Met de volgende instellingsformulieren kunt u gegevens invoeren waarmee de symptomen, diagnose en oplossing voor de reparatie worden ingesteld.

- **Servicebeheer** \> **Instellen** \> **Repareren** \> **Voorwaarden**.
- **Servicebeheer** \> **Instellen** \> **Repareren** \> **Symptoomgebieden**.
-  **Servicebeheer** \> **Instellen** \> **Repareren** \> **Diagnosegebieden**.
- **Servicebeheer** \> **Instellen** \> **Repareren** \> **Oplossingen**.
- **Servicebeheer** \> **Instellen** \> **Repareren** \> **Reparatiefasen**.

## <a name="symptoms-and-conditions"></a>Symptomen en voorwaarden

Symptomen zijn de manier waarop de klant het probleem beschrijft. Symptomen omvatten de opmerkingen van de klant waarmee wordt aangegeven dat het artikel moet worden gerepareerd.

U kunt symptoomgebieden, symptoomcodes en voorwaarden instellen. Het symptoomgebied geeft het gebied van het defect aan en met de symptoomcode wordt het defectsymptoom aangeduid. De voorwaarde geeft de situatie of de omgeving aan die aanwezig is wanneer het probleem optreedt.

**Voorbeeld**

Een computer wordt teruggebracht voor reparatie omdat de vaste schijf telkens vastloopt na langdurig gebruik. Als de vaste schijf vastloopt, verschijnt er een blauw scherm. De technisch medewerker die de computer ontvangt, voert de volgende symptomen en voorwaarden in:

1.  Het symptoomgebied is de vaste schijf

2.  De symptoomcode is de fout met het blauwe scherm

3.  De voorwaarde is dat de vaste schijf vastloop na langdurig gebruik

## <a name="diagnosis-and-resolutions"></a>Diagnose en oplossingen

De diagnose- en oplossingsvelden zijn verklaringen vanuit reparatieperspectief. Dit zijn de stappen die zijn uitgevoerd door een technische werknemer om het probleem te onderzoeken.

Het diagnosegebied bestaat uit de bewerking die moet worden uitgevoerd om het probleem op te lossen. Met de diagnosecode wordt aangegeven hoe het probleem is afgehandeld en de oplossing kan zijn dat het artikel is gerepareerd, vervangen of dat de order is geannuleerd door de klant. Als de computer bijvoorbeeld is gerepareerd, kan het diagnosegebied 'defect onderdeel' zijn, de diagnosecode 'nieuwe videokaart geïnstalleerd' en de oplossing 'vervangen'.

## <a name="repair-stages"></a>Reparatiefasen

Met reparatiefasen wordt de voortgang van het reparatieproces aangegeven. De reparatiefase heeft de afmeldingsparameter **Voltooid**, waarmee wordt aangegeven dat de reparatieregel is voltooid en de voltooiingsdatum en -tijd zijn vastgelegd.

## <a name="applying-repair-management"></a>Reparatiebeheer toepassen

Als u reparatiebeheer wilt toepassen op een artikel, moet het artikel op een serviceorder worden ingesteld met een serviceobjectrelatie. Via de serviceorder kunt u vervolgens een reparatieregel maken met informatie over het huidige probleem. Op de reparatieregel definieert u het serviceobject dat moet worden gerepareerd en informatie over symptomen, de diagnose en uitvoering. U kunt ook een notitie maken voor de reparatieregel.

U kunt voor elke stap in het reparatieproces reparatieregels maken.

## <a name="create-a-repair-line-on-a-service-order"></a>Een reparatieregel maken in een serviceorder

1.  Ga naar **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Selecteer de serviceorder met het serviceobject dat moet worden gerepareerd.

3.  Selecteer **Repareren** \> **Reparatieregels** om het formulier **Reparatieregels** te openen.

4.  Selecteer **Nieuw** om een nieuwe regel te maken.

5.  Selecteer een serviceobject. U kunt elk serviceobject selecteren dat op de serviceorder is ingesteld met een objectrelatie.

6.  Selecteer op de reparatieregel de vooraf ingestelde waarden voor de symptomen, diagnose en uitvoering die relevant zijn en selecteer zo nodig het tabblad **Opmerking** om een notitie te maken voor de reparatieregel.

7.  Selecteer **Opslaan** om de nieuwe reparatieregel op te slaan. Het veld **Aanmaakdatum en -tijd** op het tabblad **Algemeen** van het formulier **Reparatieregels** wordt bijgewerkt met het tijdstip waarop de regel is opgeslagen.

## <a name="tracking-progress-and-resolving-a-repair-issue"></a>De voortgang bijhouden en een reparatieprobleem oplossen

U kunt de reparatiefasen van een reparatieregel zo instellen dat de voortgang van de reparatie wordt bijgehouden.

Als een reparatieprobleem is opgelost, kunt u de reparatieregel afsluiten. Stel de reparatiefase in op een fase waarvoor de eigenschap **Voltooid** is ingeschakeld. De huidige datum en tijd worden op de regel vastgelegd als de voltooiingstijd.

## <a name="close-a-repair-line-for-a-resolved-issue"></a>Een reparatieregel voor een opgelost probleem afsluiten

1.  Open het formulier **Reparatieregels**. Volg de procedure voor het maken van een reparatieregel die eerder in dit onderwerp is beschreven.

2.  Selecteer de reparatieregel met de reparatie die u wilt afsluiten.

3.  Selecteer in het veld **Reparatiefase** een fase waarvoor de eigenschap **Voltooid** is ingeschakeld.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]