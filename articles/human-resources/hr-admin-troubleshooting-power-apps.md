---
title: Kan geen omgeving maken in het Power Apps-beheercentrum
description: In dit onderwerp wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft Power Apps-beheercentrum.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e50348515f14b543c392c5f9c8637cec5fa037f2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689601"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan geen omgeving maken in het Power Apps-beheercentrum


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Uitgifte**

- De tenant-/omgevingsbeheerder kan geen omgeving maken in het Microsoft Power Apps-beheercentrum.
- De gebruiker heeft geen licentie die het recht geeft om omgevingen te maken.

**Oplossing**

Zorg ervoor dat de tenantbeheerder een geldige Power Apps P2-licentie heeft toegewezen aan de gebruiker die de omgeving maakt. De volgende Microsoft Dynamics-serviceabonnementen bieden machtigingen voor het maken van omgevingen:

| Algemene product-SKU       | Power Apps P2-serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

Houd er rekening mee dat verschillende Microsoft Office-SKU's ook dit recht verlenen, samen met zelfstandige Power Apps Plan 2-SKU's. Het belangrijkste is dat een van deze SKU's aanwezig moet zijn.

1. Ga naar [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Maak de omgeving door de instructies in [Human Resources inrichten](/dynamics365/unified-operations/talent/provisioning-talent) te volgen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
