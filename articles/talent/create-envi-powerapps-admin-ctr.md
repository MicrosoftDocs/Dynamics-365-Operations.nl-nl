---
title: Kan geen omgeving maken in het PowerApps-beheercentrum
description: In dit onderwerp wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft PowerApps-beheercentrum.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96119ca869cbbb15ed8d8d5d0fe3b0f94b5f36cc
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742837"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Kan geen omgeving maken in het PowerApps-beheercentrum

[!include [banner](includes/banner.md)]

**Probleem**

- De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft PowerApps-beheercentrum.
- Een licentie die gebruikers het recht geeft de stap voor het maken van de omgeving uit te voeren, is niet direct toegewezen aan de gebruiker die deze stap uitvoert.

**Oplossing**

Zorg ervoor dat de tenantbeheerder een geldige PowerApps P2-licentie heeft toegewezen aan de gebruiker die de stap voor het maken van de omgeving uitvoert. Hier vindt u de Microsoft Dynamics-serviceplannen die dit recht bieden.

| Algemene product-SKU       | PowerApps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps for Dynamics 365 |

Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige PowerApps Plan 2-SKU's. Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.

1. Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Maak de omgeving door de instructies in [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) te volgen.
