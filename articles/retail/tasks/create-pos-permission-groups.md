---
title: " POS-machtigingsgroepen maken"
description: Deze procedure laat zien hoe u een POS-machtigingengroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b30c9a1d7fe4598695423ba700ebc88a794a49c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566359"
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

