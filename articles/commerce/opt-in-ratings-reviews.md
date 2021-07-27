---
title: Aanmelden om beoordelingen en recensies te gebruiken
description: In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cce8cb6ef9e0cc74abf90f16ed0ee481b8274a03
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352983"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.

## <a name="overview"></a>Overzicht

De oplossing voor beoordelingen en recensies is een oplossing voor meerdere kanalen die u beschikbaar kunt maken in Dynamics 365 Commerce met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een beheerportal die door detailhandelaren wordt gebruikt voor het beheren voor hun omgevingen van inrichten tot het uit bedrijf nemen.

Als u de oplossing voor beoordelingen en recensies op uw Commerce-website wilt gebruiken, moet u zich aanmelden voor beoordelingen en recensies tijdens de implementatie van uw e-Commercesite op Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

Voer de volgende stappen uit om u aan te melden voor beoordelingen en recensies op uw site.

1. Volg de stappen in [Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md).
1. Terwijl u nog bezig bent in LCS, gaat u naar **Implementatie Retail instellen \> Overige instellingen**.
1. Stel de optie **Service voor beoordelingen en recensies inschakelen** in op **Ja**.
1. Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies (beveiligingsgroepsobject-id)** de id in van de Microsoft Azure Active Directory (Azure AD)-beveiligingsgroep die de moderators voor beoordelingen en recensies bevat.

    ![Aanmelden om beoordelingen en recensies te gebruiken.](media/LCS_RnR_Preference.png)

1. Voltooi het initialisatieproces voor e-commerce.

> [!NOTE] 
> Als u een bestaande Dynamics 365 Commerce-klant bent die al een e-Commercesite heeft geïmplementeerd zonder zich bij beoordelingen en recensies te hebben aangemeld en nu beoordelingen en recensies uit het Dynamics 365 Commerce-pakket wil gebruiken, moet u een serviceaanvraag indienen. Zie [Proces voor het indienen van serviceaanvragen](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json) voor informatie over het indienen van een serviceaanvraag. 

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Commerce](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]