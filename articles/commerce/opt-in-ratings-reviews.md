---
title: Aanmelden om beoordelingen en recensies te gebruiken
description: In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697975"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.

## <a name="overview"></a>Overzicht

De oplossing voor beoordelingen en recensies is een omnichannel-oplossing die u beschikbaar kunt maken in Dynamics 365 Commerce met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een beheerportal die door detailhandelaren wordt gebruikt voor het beheren voor hun omgevingen van inrichten tot het uit bedrijf nemen.

Als u de oplossing voor beoordelingen en recensies op uw commerce-website wilt gebruiken, moet u zich eerst aanmelden.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

Voer de volgende stappen uit om u aan te melden voor beoordelingen en recensies op uw site.

1. Volg de stappen in [Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md).
1. Terwijl u nog bezig bent in LCS, gaat u naar **Implementatie Retail instellen \> Overige instellingen**.
1. Stel de optie **Service voor beoordelingen en recensies inschakelen** in op **Ja**.
1. Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies (beveiligingsgroepsobject-id)** de id in van de Microsoft Azure Active Directory (Azure AD)-beveiligingsgroep die de moderators voor beoordelingen en recensies bevat.

    ![Aanmelden om beoordelingen en recensies te gebruiken](media/LCS_RnR_Preference.png)

1. Voltooi het initialisatieproces voor e-commerce.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Retail](sync-product-ratings.md)
