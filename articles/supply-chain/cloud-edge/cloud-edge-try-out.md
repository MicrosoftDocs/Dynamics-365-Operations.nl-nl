---
title: Schaaleenheden in een gedistribueerde hybride topologie uitproberen
description: Dit onderwerp geeft informatie over het werken met schaaleenheden voor Cloud en Edge voor workloads voor productie en magazijnbeheer.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 658948d94cd012b95812a786433967f5cadc3a15
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711881"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Schaaleenheden in een gedistribueerde hybride topologie uitproberen

[!include [banner](../includes/banner.md)]

Het proces voor de gedistribueerde, hybride topologie is eenvoudig. Tijdens de eerste fase moet u aanpassingen valideren om ervoor te zorgen dat ze werken in de gedistribueerde topologie. U hebt twee opties.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Optie 1: Aanpassingen in ontwikkelomgevingen evalueren

Voordat u uw sandbox-omgevingen gaat opnemen, is het raadzaam om schaaleenheden te onderzoeken in een ontwikkelopstelling, zoals een omgeving met één vak (ook wel een tier-1-omgeving genoemd), zodat u processen, aanpassingen en oplossingen kunt valideren. In deze fase worden gegevens en aanpassingen toegepast op de omgevingen met één vak. U kunt in één omgeving werken met de rol van ondernemingsknooppunt en schaaleenheid. U kunt ook twee ontwikkelomgevingen hebben, waarvan de ene de rol van knooppunt heeft en de andere de rol van een schaaleenheid. Deze opzet biedt de beste manier om problemen op te lossen. U kunt ook de nieuwste [preview-build](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) gebruiken om deze fase te voltooien.

U moet de [implementatieprogramma's voor schaaleenheden gebruiken voor ontwikkelomgevingen met één vak](https://github.com/microsoft/SCMScaleUnitDevTools) om de omgevingen te installeren en te onderhouden. Met deze hulpprogramma's kunt u hub- en schaaleenheden configureren in een of twee omgevingen met één vak. De hulpprogramma's worden geleverd als binaire versie en in broncode op GitHub. Bestudeer de project-wiki die een [stapsgewijze gebruikshandleiding](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) bevat hoe u de hulpmiddelen gebruikt. Als u [edge-schaaleenheden implementeert op aangepaste hardware via lokale bedrijfsgegevens (LBD)](cloud-edge-edge-scale-units-lbd.md), moet u een ander proces volgen.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Optie 2: invoegvoegingen verkrijgen en implementeren in uw sandbox-omgevingen

Als u de gedistribueerde hybride topologie wilt proberen, moet u twee sandbox-omgevingen (tier 2) hebben, waarvan de ene uw gegevens (ondernemingshub) heeft en de andere voor de schaaleenheid is met 'lege gegevens'.

U moet invoegtoepassingen verkrijgen voor minimaal één cloud- of edge scale-eenheid. Overeenkomstige project- en omgevingsslots worden vervolgens toegekend in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), zodat de omgevingen van schaaleenheden kunnen worden geïmplementeerd met de [portal voor Scale Unit Manager](https://aka.ms/SCMSUM).

Neem contact op met Microsoft Support met het verzoek om de sandbox-omgevingen in te schakelen.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
