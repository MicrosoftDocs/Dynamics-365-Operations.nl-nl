---
title: Afschrijvingsboeken voor activa instellen (mei 2016)
description: Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566910"
---
# <a name="set-up-depreciation-books-may-2016"></a>Afschrijvingsboeken voor activa instellen (mei 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding maakt een nieuw afschrijvingsboek en koppelt dit aan een vaste-activagroep.  Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.


## <a name="create-a-depreciation-book"></a>Maak een afschrijvingsboek
1. Ga naar Vaste activa > Instellingen > Afschrijvingsboeken.
2. Klik op Nieuw.
3. Typ een waarde in het veld Afschrijvingsboek.
4. Typ een waarde in het veld Omschrijving.
5. Schakel het selectievakje Afschrijving berekenen in of uit.
6. Klik in het veld Afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Zoek en selecteer het gewenste afschrijvingsprofiel in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Klik in het veld Alternatief afschrijvingsprofiel op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Selecteer het gewenste afschrijvingsprofiel in de lijst.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het buitengewone-afschrijvingsprofiel wordt gebruikt voor aanvullende afschrijving van een activum onder ongebruikelijke omstandigheden. U kunt dit bijvoorbeeld gebruiken voor het registreren van afschrijving die het gevolg is van een natuurramp.  
12. Schakel het selectievakje Afschrijvingscorrecties met basiscorrecties maken in of uit.
13. Klik in het veld Kalender op de vervolgkeuzeknop om de zoekopdracht te openen.
14. Klik in de lijst op de koppeling in de geselecteerde rij.

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>Afschrijvingsboeken aan vaste-activagroepen koppelen
1. Klik op Vaste-activagroepen.
2. Klik in het veld Groep vaste activa op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Selecteer in het veld Afschrijvingsconventie een optie.
6. Voer een getal in het veld Levensduur in.
    * Merk op dat de waarde van het veld Afschrijvingsperioden wordt berekend nadat de levensduur is ingesteld.  

