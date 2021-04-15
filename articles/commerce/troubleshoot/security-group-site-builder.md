---
title: Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801502"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.

## <a name="description"></a>Beschrijving

Wanneer u de e-commerce-onderdelen maakt als onderdeel van het proces voor de implementatie van een nieuwe e-commerce-tenant die het onderdeel Commerce Site Builder bevat, wordt de Azure AD-beveiligingsgroep niet weergegeven als een optie in het dialoogvenster.

## <a name="resolution"></a>Oplossing

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>De e-commercesite inrichten met een gebruiker in de juiste tenant

1. Ga naar de [Azure-portal](https://portal.azure.com/).
1. Volg onder de tenant waarvoor het LCS-project voor uw e-commercesite is ingericht de instructies in [Een basisgroep maken en leden toevoegen via Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Ga naar [LCS](https://lcs.dynamics.com/) en meld u aan met een account die dezelfde tenant heeft als de Azure AD-beveiligingsgroep die u zojuist hebt gemaakt. De account moet toegang hebben om de Azure AD-beveiligingsgroep weer te geven.
1. Voltooi de instellingsstappen om de e-commercesite te configureren. Bij de levering van de e-commerce-onderdelen moet de beveiligingsgroep nu als een optie in het dialoogvenster worden weergegeven.

> [!NOTE]
> Als u ervoor wilt zorgen dat het veld in het dialoogvenster wordt gevuld met de lijst met beveiligingsgroepen, moet u **Enter** selecteren nadat u de naam hebt ingevuld van de Azure AD-beveiligingsgroep die u hebt gemaakt. In de zoekresultaten worden alle Azure AD-beveiligingsgroepen weergegeven die beginnen met de zoektekst en waartoe de gebruiker toegang heeft. U kunt een kortere zoekterm gebruiken voor bredere zoekresultaten.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een basisgroep maken en leden toevoegen met Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Een nieuwe e-commercetenant implementeren](../deploy-ecommerce-site.md)
