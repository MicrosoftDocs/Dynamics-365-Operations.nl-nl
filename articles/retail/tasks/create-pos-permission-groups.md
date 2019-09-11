---
title: POS-machtigingsgroepen maken
description: In dit onderwerp wordt uitgelegd hoe u een POS-machtigingsgroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
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
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914783"
---
# <a name="create-pos-permission-groups"></a>POS-machtigingsgroepen maken

[!include[task guide banner](../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een POS-machtigingsgroep maakt. Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT. Deze taak is bedoeld voor de rol Bedrijfsbeheerder detailhandel.

1. Ga in het navigatievenster naar **Modules > Detailhandel > Medewerkers > Machtigingsgroepen**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **POS-machtigingsgroeps-id**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Ja** in het veld **Registraties tijdklok weergeven**. U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen. Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren. Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.  
6. Selecteer **Ja** in het veld **Order maken toestaan**.
7. Selecteer **Ja** in het veld **Order bewerken toestaan**.
8. Selecteer **Ja** in het veld **Order ophalen toestaan**.
9. Selecteer **Ja** in het veld **Wachtwoordwijziging toestaan**.
10. Selecteer **Ja** in het veld **Blind sluiten toestaan**.
11. Selecteer **Opslaan**. Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen. 
12. Ga in het navigatievenster naar **Modules > Human Resources > Taken > Taken**.
13. Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen. Zoek en selecteer de gewenste record in de lijst.
14. Selecteer **Bewerken**.
15. Vouw de sectie **Taakclassificatie** uit.
16. Typ of selecteer een waarde in het veld POS-machtigingsgroep. Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.  
17. Selecteer **Opslaan**. Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.  

