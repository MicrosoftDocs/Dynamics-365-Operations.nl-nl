---
title: Onkostenbeleid definiëren
description: In Microsoft Dynamics 365 for Finance and Operations kunt u een beleid of regels definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisopdrachten.
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840884"
---
# <a name="expense-policies"></a>Onkostenbeleid

[!include [banner](../includes/banner.md)]

U kunt beleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen.         
Door het implementeren van onkostenbeleidsregels kunt u onkosten efficiënt beheren.         

U kunt bijvoorbeeld een beleid instellen dat de onkosten voor een hotelovernachting in New York niet hoger mogen zijn dan USD 250.       
Als een werknemer een onkostennota of een reisaanvraag indient waarin het tarief van de kamer dit bedrag overschrijdt, waarschuwt het systeem de        
de werknemer dat het ingestelde bedrag voor de onkosten is overschreden. U kunt het bericht dat de werknemer ontvangt, configureren bij het        
definiëren van het beleid.      
        
U kunt drie typen beleidsregels definiëren:         
        
- Waarschuwing – De werknemer mag een onkostennota of reisaanvraag indienen maar de onkosten worden gemarkeerd voor alle fiatteurs        
  en latere rapportage.        

- Fout – Vereist dat de werknemer de onkosten herziet om het beleid na te leven alvorens de onkostendeclaratie of reisopdracht wordt ingediend.       
 
 - Verantwoording – Vereist dat de werknemer of een manager van een motivering opgeeft bedrag in het beleid te overschrijden alvorens de onkostennota of reisopdracht kan worden ingediend.        

## <a name="policy-tips"></a>Beleidstips
Hier volgen enkele suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer. 
* Beleid heeft een ingangsdatum en wordt niet van kracht als het beleid wordt gemaakt met een datum na de datum waarop de onkosten zijn gemaakt. Als u bijvoorbeeld vandaag een nieuw beleid maakt om de maximale maaltijdkosten van $ 50 af te dwingen, worden eventuele bestaande onkosten tot en met gisteren die zijn ingevoerd niet gecontroleerd aan de hand van dit beleid.
* Wanneer u een beleid maakt voor een onkostencategorie die kan worden gespecificeerd, kunt u overwegen een voorwaarde toe te voegen voor het type onkostenregel. Sommige beleidsregels, zoals het vereisen van een ontvangstbon, zijn mogelijk niet zinvol voor gespecificeerde regels en mogen alleen worden toegepast op de koptekstregel of een niet-gespecificeerde regel. 

## <a name="when-to-evaluate-policies"></a>Wanneer u beleid moet evalueren

In parameters voor onkostenbeheer is er een optie waarmee u beleid voor onkostenbeheer kunt beoordelen wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend. Als u ervoor kiest om te beoordelen wanneer een regel wordt opgeslagen, zorgt u ervoor dat gebruikers eerder zicht hebben op wat zij moeten doen om hun onkostennota in één keer te voltooien. Anders kunt u beleidsevaluatie uitstellen en tijd besparen als u de validatie uitvoert aan het einde, tijdens de indiening bij de werkstroom.
