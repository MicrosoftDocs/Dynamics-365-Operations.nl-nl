---
title: Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie
description: Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020727"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>Kan een beveiligingsgroep voor Commerce Site Builder niet configureren tijdens de initiële implementatie

[!include [banner](../../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor het oplossen van problemen die kunnen helpen wanneer de Microsoft Azure Active Directory (Azure AD) beveiligingsgroep voor Commerce Site Builder niet als optie wordt weergegeven wanneer u e-commerce-onderdelen maakt in Microsoft Dynamics Lifecycle Services (LCS) tijdens de initiële implementatie van een nieuwe e-commerce-tenant.

## <a name="description"></a>Beschrijving

Wanneer u de e-commerce-onderdelen maakt als onderdeel van het proces voor de implementatie van een nieuwe e-commerce-tenant die het onderdeel Commerce Site Builder bevat, wordt de Azure AD-beveiligingsgroep niet weergegeven als een optie in het dialoogvenster.

## <a name="resolution"></a>Oplossing

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>De e-commercesite inrichten met een gebruiker in de juiste tenant

1. Ga naar de [Azure-portal](https://portal.azure.com/).
1. Volg onder de tenant waarvoor het LCS-project voor uw e-commercesite is ingericht de instructies in [Een basisgroep maken en leden toevoegen via Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).
1. Ga naar [LCS](https://lcs.dynamics.com/) en meld u aan met een account die dezelfde tenant heeft als de Azure AD-beveiligingsgroep die u zojuist hebt gemaakt. De account moet toegang hebben om de Azure AD-beveiligingsgroep weer te geven.
1. Voltooi de instellingsstappen om de e-commercesite te configureren. Bij de levering van de e-commerce-onderdelen moet de beveiligingsgroep nu als een optie in het dialoogvenster worden weergegeven.

> [!NOTE]
> Als u ervoor wilt zorgen dat het veld in het dialoogvenster wordt gevuld met de lijst met beveiligingsgroepen, moet u **Enter** selecteren nadat u de naam hebt ingevuld van de Azure AD-beveiligingsgroep die u hebt gemaakt. In de zoekresultaten worden alle Azure AD-beveiligingsgroepen weergegeven die beginnen met de zoektekst en waartoe de gebruiker toegang heeft. U kunt een kortere zoekterm gebruiken voor bredere zoekresultaten.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een basisgroep maken en leden toevoegen met Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[Een nieuwe e-commercetenant implementeren](../deploy-ecommerce-site.md)