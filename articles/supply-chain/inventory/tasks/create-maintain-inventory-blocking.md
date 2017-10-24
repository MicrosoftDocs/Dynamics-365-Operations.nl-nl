---
title: Voorraadblokkering maken en beheren
description: Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering.
author: perlynne
manager: AnnBe
ms.date: 12/02/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7272349cf16b9459823a752b8d3df915f42606ef
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-maintain-inventory-blocking"></a>Voorraadblokkering maken en beheren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering. U kunt de procedure uitvoeren in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven. U moet een artikel met fysieke beschikbare voorhanden voorraad hebben voordat u deze procedure start.


## <a name="create-an-inventory-blocking"></a>Een voorraadblokkering maken
1. Ga naar Voorraadbeheer > Periodieke taken > Voorraadblokkering.
2. Klik op Nieuw.
3. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer in de lijst het artikel dat u wilt kiezen.
    * Selecteer een artikelnummer met fysieke voorhanden voorraad die u wilt blokkeren. Als u USMF gebruikt, kunt u artikel M9201 selecteren.  
5. Voer in het veld Hoeveelheid een getal in.
    * Als u artikel M9201 gebruikt, moet u minder dan 200 selecteren.  
6. Schakel de uitbreiding van de sectie Voorraaddimensies om.
7. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer de gewenste record in de lijst.
    * Als u artikel M9201 gebruikt, kunt u magazijn 51 selecteren.  
9. Klik op Opslaan.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>De voorwaarden van de voorraadblokkering bijwerken
1. Voer in het veld Hoeveelheid een getal in.
    * Werk het veld van de voorraadhoeveelheid bij om de te blokkeren hoeveelheid aan te geven.  
2. Voer in het veld Verwachte datum een datum in.
    * U kunt bijvoorbeeld aangeven wanneer de geblokkeerde voorraad naar verwachting beschikbaar komt voor reservering door een verwachte datum toe te wijzen. Als de optie Verwachte ontvangsten is geselecteerd voor de voorraadblokkering, zoals standaard het geval is wanneer u handmatig een blokkering uitvoert, wordt deze datum op de verwachte transactie weergegeven.  
3. Klik op Opslaan.

## <a name="remove-the-inventory-blocking"></a>De voorraadblokkering verwijderen
1. Klik op Verwijderen.
2. Klik op Ja.
3. Sluit de pagina.

