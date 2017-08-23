--- 
title: " POS-machtigingsgroepen maken"
description: Deze procedure laat zien hoe u een POS-machtigingengroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b0c930e3722d1d0b1fff8efad7a785a153436b6d
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="create-pos-permission-groups"></a> POS-machtigingsgroepen maken

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een POS-machtigingengroep maakt. Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT. Deze taak is bedoeld voor de rol Bedrijfsbeheerder detailhandel.

1. Ga naar Machtigingsgroepen.
2. Klik op Nieuw.
3. Typ een waarde in het veld POS-machtigingsgroeps-id.
4. Typ een waarde in het veld Omschrijving.
5. Selecteer Ja in het veld Registraties tijdklok weergeven.
    * U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen. Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren.  Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.  
6. Selecteer Ja in het veld Order maken toestaan.
7. Selecteer Ja in het veld Order bewerken toestaan.
8. Selecteer Ja in het veld Order ophalen toestaan.
9. Selecteer Ja in het veld Wachtwoordwijziging toestaan.
10. Selecteer Ja in het veld Blind sluiten toestaan.
11. Klik op Opslaan.
    * Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.  
12. Sluit de pagina.
13. Ga naar Taken.
    * Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen.  
14. Zoek en selecteer de gewenste record in de lijst.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
16. Klik op Bewerken.
17. Vouw de sectie Taakclassificatie uit.
18. Typ of selecteer een waarde in het veld POS-machtigingsgroep.
    * Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.  
19. Klik op Opslaan.
    * Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.  


