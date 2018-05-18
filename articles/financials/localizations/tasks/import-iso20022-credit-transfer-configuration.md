--- 
title: Configuratie van ISO20022-kredietoverdracht importeren
description: In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van leveranciersbetalingen importeert.
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 71c0175178203006e297466c4a37cd3e6319b6ea
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="import-iso20022-credit-transfer-configuration"></a>Configuratie van ISO20022-kredietoverdracht importeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van leveranciersbetalingen importeert. De Duitse kredietoverdrachtindeling ISO 20022 wordt hier als voorbeeld gebruikt. Deze procedure kan worden gebruikt voor andere beschikbare indelingen voor elektronische rapportage. 

Deze taak is gemaakt met het demobedrijf DEMF, maar u kunt elk bedrijf uit de demogegevens gebruiken om deze taak uit te voeren.

Dit is de eerste van vijf taken die samen het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Selecteer in de lijst met beschikbare configuratieproviders de waarde Microsoft.
3. Klik op Instellingen als actief.
4. Klik op Opslagplaatsen.
5. Klik op Openen.
6. Klik op Filters weergeven.
7. Pas de volgende filter toe: voer in het veld "Configuratienaam" de waarde "ISO20022 Kredietoverdracht (DE)" in met de filteroperator "begint met".
    * Of zoek de configuratie in de lijst, selecteer deze en verplaats de configuratie naar de taak Importeren.  
8. Klik op Importeren.
    * Als de knop Importeren niet beschikbaar is, betekent dit dat deze configuratie al is geïmporteerd.  
9. Klik op Ja.


