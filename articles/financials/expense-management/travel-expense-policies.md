---
title: "Onkostenbeleid definiëren"
description: "U kunt onkostenbeleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

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

