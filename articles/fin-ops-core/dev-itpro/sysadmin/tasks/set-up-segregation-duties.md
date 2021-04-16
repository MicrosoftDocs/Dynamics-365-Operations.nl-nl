---
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745736"
---
# <a name="set-up-segregation-of-duties"></a>Scheiding van taken instellen

[!include [banner](../../includes/banner.md)]

U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd. Dit concept wordt scheiding van taken genoemd. Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt. Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren. U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen. Voer de volgende procedure uit om een regel te maken. U moet een systeembeheerder zijn om deze procedure te voltooien.

1. Ga naar **Systeembeheer** > **Beveiliging** > **Scheiding van taken** > **Regels voor scheiding van taken**.
2. Klik op **Nieuw**.
3. Typ een waarde voor de regel in het veld **Naam**.
4. Klik in het veld **Eerste functie** op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Zoek en selecteer de gewenste record in de lijst. Selecteer de eerste functie die door de regel wordt gecontroleerd.
6. Klik in het veld **Tweede functie** op de vervolgkeuzeknop om de zoekopdracht te openen. 
7. Zoek en selecteer de gewenste record in de lijst. Selecteer de tweede functie die door de regel wordt gecontroleerd.
10. Selecteer een optie in het veld **Ernst**. Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.  
11. Typ een waarde in het veld **Beveiligingsrisico**. Voer een omschrijving van het beveiligingsrisico in.  
12. Typ een waarde in het veld **Risicobeperking beveiliging**. Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken. Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.     
13. Klik op **Opslaan**.

> [!IMPORTANT] 
> Wanneer u een regel maakt, wordt niet gecontroleerd of de regels voor de scheiding van taken worden nageleefd. U kunt een regel maken die een conflict veroorzaakt voor bestaande rollen. Bestaande gebruikersroltoewijzingen kunnen ook in conflict zijn met de nieuwe regel. U moet de conformiteit valideren nadat u een regel hebt gemaakt of gewijzigd. Zie [Conflicten bij scheiding van taken identificeren en oplossen](identify-resolve-conflicts-segregation-duties.md) voor meer informatie.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]