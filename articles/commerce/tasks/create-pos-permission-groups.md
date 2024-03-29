---
title: " POS-machtigingsgroepen maken"
description: In dit artikel wordt uitgelegd hoe u een POS-machtigingsgroep maakt.
author: josaw1
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: RetailPosPermissionGroup, HcmJob
ms.openlocfilehash: 0aa394e5dc6685954c31cdddae7cdc042b80af29
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277955"
---
# <a name="create-pos-permission-groups"></a> POS-machtigingsgroepen maken

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een POS-machtigingsgroep maakt. Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT. Deze taak is bedoeld voor de rol Commerce-bedrijfsbeheerder.

1. Ga in het navigatievenster naar **Modules > Retail en Commerce > Medewerkers > Machtigingsgroepen**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **POS-machtigingsgroeps-id**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Ja** in het veld **Registraties tijdklok weergeven**. U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen. Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren. Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.  
6. Selecteer **Ja** in het veld **Order maken toestaan**.
7. Selecteer **Ja** in het veld **Order bewerken toestaan**.
8. Selecteer **Ja** in het veld **Order ophalen toestaan**.
9. Selecteer **Ja** in het veld **Wachtwoordwijziging toestaan**.
10. Selecteer **Ja** in het veld **Blind sluiten toestaan**.
11. Selecteer **Opslaan**. Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar Commerce te pushen. 
12. Ga in het navigatievenster naar **Modules > Human Resources > Taken > Taken**.
13. Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen. Zoek en selecteer de gewenste record in de lijst.
14. Selecteer **Bewerken**.
15. Vouw de sectie **Taakclassificatie** uit.
16. Typ of selecteer een waarde in het veld POS-machtigingsgroep. Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.  
17. Selecteer **Opslaan**. Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar kanalen te pushen.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
