---
title: Kan geen omgeving maken in het Power Apps-beheercentrum
description: In dit artikel wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft Power Apps-beheercentrum.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 68e6dbcbbc9811211570e968047f5faa8a2c8bd0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417957"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan geen omgeving maken in het Power Apps-beheercentrum

**Uitgifte**

- De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft Power Apps-beheercentrum.
- Een licentie die gebruikers het recht geeft de stap voor het maken van de omgeving uit te voeren, is niet direct toegewezen aan de gebruiker die deze stap uitvoert.

**Oplossing**

Zorg ervoor dat de tenantbeheerder een geldige Power Apps P2-licentie heeft toegewezen aan de gebruiker die de stap voor het maken van de omgeving uitvoert. Hier vindt u de Microsoft Dynamics-serviceplannen die dit recht bieden.

| Algemene product-SKU       | Power Apps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige Power Apps Plan 2-SKU's. Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.

1. Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Maak de omgeving door de instructies in [Human Resources inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) te volgen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]