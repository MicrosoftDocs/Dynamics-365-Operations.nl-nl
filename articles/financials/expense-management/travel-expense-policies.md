---
title: "Onkostenbeleid definiëren"
description: "U kunt onkostenbeleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="expense-policies"></a>Onkostenbeleid

[!include[banner](../includes/banner.md)]

U kunt beleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen. Door het implementeren van onkostenbeleidsregels kunt u onkosten efficiënt beheren. 

U kunt bijvoorbeeld een beleid instellen dat de onkosten voor een hotelovernachting in New York niet hoger mogen zijn dan USD 250. Een werknemer die een onkostennota of reisaanvraag met een hotelovernachting boven dit bedrag indient, wordt door het systeem gewaarschuwd dat het in het beleid ingestelde maximumbedrag wordt overschreden. U kunt het bericht dat de werknemer ontvangt, configureren bij het definiëren van het beleid. 

U kunt drie typen beleidsregels definiëren: 

 - Waarschuwing – De werknemer mag een onkostennota of reisaanvraag indienen maar de onkosten worden gemarkeerd voor alle fiatteurs  
 en latere rapportage. 
 - Fout – Vereist dat de werknemer de onkosten herziet om het beleid na te leven alvorens de onkostendeclaratie of reisopdracht wordt ingediend. 
 - Verantwoording – Vereist dat de werknemer of een manager van een motivering opgeeft bedrag in het beleid te overschrijden alvorens de onkostennota of reisopdracht kan worden ingediend. 

Het is ook mogelijk om te definiëren gedurende welk datumbereik de onkostenbeleidsregels geldig zijn. Tijdens de piekperiode in de zomervakantie gelden bijvoorbeeld mogelijk hogere tarieven voor vluchten tussen Denemarken en New York. U kunt een regel definiëren dat voor ticketkosten naar New York een limiet van DKK 5000 geldt en u kunt opgeven dat deze regel geldt van 15 mei tot 15 september. 

