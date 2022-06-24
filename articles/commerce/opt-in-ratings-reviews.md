---
title: Aanmelden om beoordelingen en recensies te gebruiken
description: In dit artikel wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.
author: gvrmohanreddy
ms.date: 02/16/2020
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
ms.openlocfilehash: b591799bd5bf00e74e782040bfdc1b678c4c87d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906907"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u zich kunt aanmelden voor beoordelingen en recensies op uw Microsoft Dynamics 365 Commerce-site.

De oplossing voor beoordelingen en recensies is een oplossing voor meerdere kanalen die u beschikbaar kunt maken in Dynamics 365 Commerce met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een beheerportal die door detailhandelaren wordt gebruikt voor het beheren voor hun omgevingen van inrichten tot het uit bedrijf nemen.

Als u de oplossing voor beoordelingen en recensies op uw Commerce-website wilt gebruiken, moet u zich aanmelden voor beoordelingen en recensies tijdens de implementatie van uw e-Commercesite op Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Aanmelden om beoordelingen en recensies te gebruiken

Voer de volgende stappen uit om u aan te melden voor beoordelingen en recensies op uw site.

1. Volg de stappen in [Een nieuwe e-commerce-site implementeren](deploy-ecommerce-site.md).
1. Terwijl u nog bezig bent in LCS, gaat u naar **Implementatie Retail instellen \> Overige instellingen**.
1. Stel de optie **Service voor beoordelingen en recensies inschakelen** in op **Ja**.
1. Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de id in van de Microsoft Azure Active Directory (Azure AD)-beveiligingsgroep die de moderators voor beoordelingen en recensies bevat.

    ![Aanmelden om beoordelingen en recensies te gebruiken.](media/LCS_RnR_Preference_2.png)

1. Voltooi het initialisatieproces voor e-commerce.

> [!NOTE] 
> Als u een bestaande Dynamics 365 Commerce-klant bent die al een e-Commercesite heeft geïmplementeerd zonder zich bij beoordelingen en recensies te hebben aangemeld en nu beoordelingen en recensies uit het Dynamics 365 Commerce-pakket wil gebruiken, moet u een serviceaanvraag indienen. Zie [Proces voor het indienen van serviceaanvragen](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json) voor informatie over het indienen van een serviceaanvraag. 

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht beoordelingen en recensies](ratings-reviews-overview.md)

[Beoordelingen en recensies beheren](manage-reviews.md)

[Beoordelingen en recensies configureren](configure-ratings-reviews.md)

[Productbeoordelingen synchroniseren in Dynamics 365 Commerce](sync-product-ratings.md)

[Handmatig publiceren van beoordelingen en recensies inschakelen door een moderator](manual-publish-rating-reviews.md)

[Beoordelingen en recensies importeren en exporteren](import-export-reviews.md)

[Service-to-Service verificatie configureren](service-to-service-auth.md)

[Veelgestelde vragen over beoordelingen en recensies](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
