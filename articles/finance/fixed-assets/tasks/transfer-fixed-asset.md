---
title: Een vast activum overboeken
description: Deze taakbegeleiding boekt de financiële gegevens voor het vaste-activaboek over van een set financiële dimensies naar een nieuwe set financiële dimensies.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c307568ab1cc064c27fa8d3e24756f564947e4716aaed1c280019c1283da1c93
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765687"
---
# <a name="transfer-a-fixed-asset"></a>Een vast activum overboeken

[!include [banner](../../includes/banner.md)]

Deze taakbegeleiding boekt de financiële gegevens voor het vaste-activaboek over van een set financiële dimensies naar een nieuwe set financiële dimensies.  Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.

1. Ga in het navigatievenster naar **Modules > Vaste activa > Vaste activa > Vaste activa**.
2. Zoek en selecteer in de lijst het vaste activum om over te boeken.
3. Klik in het actievenster op **Vaste activa**.
4. Klik op **Vaste activa overboeken**.
5. Voer een datum in het veld **Overdrachtsdatum** in.
6. Voer een opmerking in om de overboeking te beschrijven.
    
    Deze lijst bevat alle boeken voor de vaste activa.  
7. Markeer de boeken die u naar een nieuwe set financiële dimensies wilt overboeken.
    * Deze lijst toont de bestaande financiële dimensiewaarden voor het geselecteerde boek.  
    * Selecteer de financiële dimensie die u voor het geselecteerde vaste activumboek wilt bijwerken.  
8. Klik in het veld **Financiële dimensie** op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Stel andere financiële dimensiewaarden in.  
    * Alle financiële dimensiewaarden wijzigen wanneer een overboeking plaatsvindt, ongeacht of een waarde is ingevoerd of niet. Bijvoorbeeld, als u een waarde voor de BusinessUnit hebt ingevoerd en de financiële dimensies CostCenter en Department leeg laat. Als uw rekeningstructuur lege waarden toestaat voor CostCenter en Department, resulteert de overboeking in elk waardemodel met de nieuwe waarde voor BusinessUnit en een lege waarde voor CostCenter en Department.  
9. Klik op **Bijwerken**.
    * U kunt de wijzigingen bekijken voordat de overboeking wordt voltooid.  
    * Controleer resultaten voordat de vaste-activumboeken worden overgeboekt.  
10. Klik op **Overboeken**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]