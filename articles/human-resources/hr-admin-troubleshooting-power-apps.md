---
title: Kan geen omgeving maken in het Power Apps-beheercentrum
description: In dit artikel wordt beschreven wat er moet gebeuren als de beheerder geen omgeving kan maken in het Microsoft Power Apps-beheercentrum.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 26a228229a09e74809a048675a3ff90025f2a26c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892222"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Kan geen omgeving maken in het Power Apps-beheercentrum

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