--- 
title: " POS-machtigingsgroepen maken"
description: Deze procedure laat zien hoe u een POS-machtigingengroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a> POS-machtigingsgroepen maken

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

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


