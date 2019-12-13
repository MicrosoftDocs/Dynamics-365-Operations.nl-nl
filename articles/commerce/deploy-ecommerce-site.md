---
title: Een nieuwe e-commerce-tenant implementeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-tenant implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697446"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Een nieuwe e-commerce-tenant implementeren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuwe e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).

## <a name="overview"></a>Overzicht
    
Microsoft Dynamics Lifecycle Services (LCS) is een cloudwerkgebied dat door partners en klanten wordt gebruikt voor het beheer van hun projecten en omgevingen, het weergeven van de meest recente informatie over producten en functies van Microsoft Dynamics en het maken, volgen en zoeken van ondersteuningsaanvragen. Beheerfuncties voor e-commerce zijn in LCS geïntegreerd.

Zie de [gebruikershandleiding van Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) voor meer informatie over LCS.
    
## <a name="get-started"></a>Aan de slag

Voordat u e-commerce kunt initialiseren, moet u een project, een omgeving en een Retail Cloud Scale Unit (RCSU) initialiseren. Als u de initialisatie wilt uitvoeren in LCS, moet u machtigingen hebben voor de rol projecteigenaar of omgevingsbeheerder. De topologieën productie en sandbox-omgeving worden ondersteund.

Zie [Omgevingsplanning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) voor meer informatie over omgevingen. Zie [Retail Cloud Scale Unit initialiseren](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)voor meer informatie over RCSU.

## <a name="initialize-e-commerce"></a>e-Commerce initialiseren

Gebruik deze procedure om de e-commerce-functie in een bestaande omgeving te initialiseren.

Voordat u begint, moet u controleren of u de volgende vereiste informatie hebt:

- De RCSU die wordt gebruikt
- De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor e-commerce-systeembeheerders.
- De Microsoft Azure Active Directory-beveiligings groep die wordt gebruikt voor moderators van beoordelingen en recensies.
- De domeinen die aan de omgeving worden gekoppeld.

Bovendien kunt u de volgende optionele informatie verzamelen:

- Informatie over Azure AD business-to-consumer (B2C):

    - Naam tenant.
    - Client-id.
    - Aangepast domein voor aanmelding.
    - Antwoord-URL.
    - Beleids-id voor aanmelden registreren.
    - Beleid-id voor wachtwoord opnieuw instellen.
    - Profielbeleid-id bewerken.

[!NOTE]
Deze informatie kan later worden toegevoegd via een serviceaanvraag.

Nadat u de vereiste informatie hebt verzameld, voert u de volgende stappen uit om e-commerce te initialiseren.

1. Meld u aan bij [LCS](https://lcs.dynamics.com).
1. Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.
1. Selecteer de omgeving in de sectie **Omgevingen**.
1. Selecteer de koppeling **Retail beheren** onder **Omgevingsfuncties**.
1. Selecteer op het tabblad **e-Commerce** de optie **Instellingen**. Er wordt een dialoogvenster weergegeven, waarin u de vereiste gegevens voor de inrichting moet invoeren.
1. Vul de vereiste informatie in en ga naar de volgende pagina.
1. Vul de vereiste informatie in op de volgende pagina en verzend het formulier. U keert terug naar het tabblad **e-Commerce** en u ziet dat de initialisatie is gestart.
1. Als u de initialisatiestatus wilt weergeven, kiest u **Vernieuwen** of keert u later terug naar het tabblad **e-Commerce**.
    
Wanneer e-Commerce via LCS wordt geïnitialiseerd, worden verscheidene onderdelen ingesteld die nodig zijn voor e-commerce en die aan de omgeving worden gekoppeld. Nadat de inrichting is voltooid, wordt het tabblad **e-Commerce** op de pagina **Beheer detailhandel** bijgewerkt om de inrichting weer te geven. Op de pagina worden de nieuwste implementaties van aanpassingen en de status van andere lopende implementaties weergegeven. De pagina bevat ook koppelingen naar de e-commerce-site en het hulpprogramma voor e-commerce-sitebeheer (het ontwerpgereedschap).

## <a name="access-the-authoring-environment"></a>Toegang tot de ontwerpomgeving

Ga naar het tabblad **e-Commerce** op de pagina **Detailhandelbeheer** om de ontwerpomgeving te openen. Hier vindt u koppelingen naar uw e-commerce-site en het hulpprogramma voor sitebeheer.

## <a name="additional-resources"></a>Aanvullende resources

[Online winkeloverzicht](online-store-overview.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een online-site koppelen aan een kanaal](associate-site-online-store.md)

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)
