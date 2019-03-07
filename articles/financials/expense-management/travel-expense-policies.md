---
title: Onkostenbeleid definiëren
description: In Microsoft Dynamics 365 for Finance and Operations kunt u een beleid of regels definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisopdrachten.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "342426"
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
 
  Het is ook mogelijk om te definiëren gedurende welk datumbereik de onkostenbeleidsregels geldig zijn. Tijdens de piekperiode in de zomervakantie gelden bijvoorbeeld      
  mogelijk hogere tarieven voor vluchten tussen Denemarken en New York. U kunt een regel definiëren dat voor ticketkosten naar New York een limiet      
  van DKK 5000 geldt en u kunt opgeven dat deze regel geldt van 15 mei      
  tot 15 september.
