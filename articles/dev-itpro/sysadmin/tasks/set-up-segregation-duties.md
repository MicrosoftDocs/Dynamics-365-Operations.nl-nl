--- 
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-segregation-of-duties"></a>Scheiding van taken instellen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd. Dit concept wordt scheiding van taken genoemd. Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt. Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren. U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen. Voer de volgende procedure uit om een regel te maken. U moet een systeembeheerder zijn om deze procedure te voltooien. Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT. 

1. Ga naar Systeembeheer > Beveiliging > Scheiding van taken > Regels voor scheiding van taken.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
    * Voer een naam voor de regel in.  
4. Klik in het veld Eerste functie op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de eerste functie die door de regel wordt gecontroleerd.  
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik in het veld Tweede functie op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de tweede functie die door de regel wordt gecontroleerd.  
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Selecteer een optie in het veld Ernst.
    * Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.  
11. Typ een waarde in het veld Beveiligingsrisico.
    * Voer een omschrijving van het beveiligingsrisico in.  
12. Typ een waarde in het veld Risicobeperking beveiliging.
    * Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken. Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.  
13. Klik op Opslaan.


