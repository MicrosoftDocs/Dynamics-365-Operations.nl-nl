---
title: Bekende problemen met de infrastructuursamenvoeging voor Dynamics 365 Human Resources
description: Dit artikel geeft een overzicht van problemen die kunnen optreden tijdens de samenvoeging van de Microsoft Dynamics 365 Human Resources-infrastructuur.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752685"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Bekende problemen met de infrastructuursamenvoeging voor Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Gedeelde Dataverse-omgevingen

Het framework voor twee keer wegschrijven biedt geen ondersteuning voor het koppelen van twee omgevingen van de app voor financiën en bedrijfsactiviteiten aan dezelfde Dataverse-omgeving. Als u een Dataverse-omgeving hebt die met beide volgende items wordt gedeeld, moet u de Dataverse-omgeving dupliceren of opsplitsen:

- Een app voor financiën en bedrijfsactiviteiten
- Een huidige Human Resources-omgeving

## <a name="environment-type-requirements"></a>Vereisten voor omgevingstype

De volgende omgevingstypen zijn vereist voordat u de migratie kunt doen:

- Als u geen sandbox-omgevingen hebt, moet u een omgeving maken om de migratie te valideren.
- Als u meerdere zelfstandige productieomgevingen hebt, kan een van deze omgevingen worden gemigreerd. Neem contact op met Microsoft Ondersteuning met het verzoek om de andere omgevingen als sandboxes te markeren.

## <a name="teams-integration"></a>Teams-integratie

De bestaande Human Resources-app in Teams wordt momenteel verplaatst naar een Microsoft Power Platform-oplossing. Zie [Human resources-app in Teams](hr-admin-teams-leave-app.md) voor meer informatie.

