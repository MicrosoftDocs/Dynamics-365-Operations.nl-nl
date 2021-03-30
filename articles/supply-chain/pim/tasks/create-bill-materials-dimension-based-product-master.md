---
title: Een stuklijst maken voor een op dimensies gebaseerd productmodel
description: Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799479c4b4cdf5b61b1f55a61454823558b9013b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237419"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Een stuklijst maken voor een op dimensies gebaseerd productmodel

[!include [banner](../../includes/banner.md)]

Voor deze procedure moet u de vorige 4 guides in deze reeks van acht registraties hebben voltooid. Met de eerste 4 registraties zijn gegevens ingesteld die nodig zijn om deze procedure te voltooien. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze taak wordt doorgaans afgehandeld door de productontwerper.


## <a name="select-the-product"></a>Het product selecteren
1. Klik op Vrijgegeven productonderhoud.
2. Klik op Vrijgegeven producten.
3. Markeer in de lijst de geselecteerde rij.
    * Zoek het vrijgegeven productmodel met op dimensies gebaseerde configuratietechnologie die u in de eerste taakbegeleider in deze reeks hebt gemaakt.  
4. Klik op Technicus in het actievenster.
5. Klik op Stuklijstversies.

## <a name="create-new-bom-and-bom-version"></a>Een nieuwe stuklijst en stuklijstversie maken
1. Klik op Nieuw.
2. Klik op Stuklijst en stuklijstversie.
3. Typ een waarde in het veld Naam.
    * Een vestiging instellen  
    * In deze procedure wordt geen specifieke vestiging voor de stuklijst ingesteld.  
4. Klik op OK.
5. Klik op Nieuw.
    * In deze procedure worden vier regels aan de stuklijst toegevoegd. Twee regels staan voor kabelopties en twee regels staan voor behuizingsopties.  
6. Markeer in de lijst de geselecteerde rij.
7. Typ of selecteer een waarde in het veld Artikelnummer.
    * Selecteer artikelnummer A0001, HDMI 6' kabels.  
8. Typ of selecteer een waarde in het veld Configuratiegroep.
    * Selecteer de kabelconfiguratiegroep die is gemaakt in guide 4 in deze reeks.  
9. Klik op Nieuw.
    * Selecteer artikelnummer A0002, HDMI 12' kabels.  
10. Markeer in de lijst de geselecteerde rij.
11. Typ of selecteer een waarde in het veld Artikelnummer.
12. Typ of selecteer een waarde in het veld Configuratiegroep.
    * Selecteer de kabelconfiguratiegroep nogmaals.  
13. Klik op Nieuw.
14. Markeer in de lijst de geselecteerde rij.
15. Typ of selecteer een waarde in het veld Artikelnummer.
    * Selecteer artikelnummer D0002 behuizing  
16. Typ of selecteer een waarde in het veld Configuratiegroep.
    * Selecteer de behuizingsconfiguratiegroep voor deze stuklijstregel.  
17. Klik op Nieuw.
18. Markeer in de lijst de geselecteerde rij.
19. Typ of selecteer een waarde in het veld Artikelnummer.
    * Selecteer artikelnummer M0007 standaardbehuizing als de laatste stuklijstregel.  
20. Typ of selecteer een waarde in het veld Configuratiegroep.
    * Selecteer de behuizingsconfiguratiegroep voor de laatste stuklijstregel.  

## <a name="approve-and-activate"></a>Goedkeuren en activeren
1. Sluit de pagina.
2. Klik op Goedkeuren.
3. Typ of selecteer een waarde in het veld Goedgekeurd door.
4. Selecteer Ja in het veld Wilt u ook de stuklijst goedkeuren?
5. Klik op OK.
6. Klik op Activeren.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]