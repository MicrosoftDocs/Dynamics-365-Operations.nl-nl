---
title: Een nieuwe e-commerce-tenant implementeren
description: In dit onderwerp wordt beschreven hoe u een nieuwe Dynamics 365 Commerce e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d31e3e7248809a00ad51183b80205d1351567ab3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477871"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>Een nieuwe e-commerce-tenant implementeren

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuwe Dynamics 365 Commerce e-commerce-site implementeert met behulp van Microsoft Dynamics Lifecycle Services (LCS).

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

> [!NOTE]
> Deze informatie kan later worden toegevoegd via een serviceaanvraag.

Nadat u de vereiste informatie hebt verzameld, voert u de volgende stappen uit om e-commerce te initialiseren.

1. Meld u aan bij [LCS](https://lcs.dynamics.com).
1. Open het project dat de omgeving bevat waarin u e-commerce wilt initialiseren.
1. Selecteer de omgeving in de sectie **Omgevingen**.
1. Selecteer de koppeling **Retail beheren** onder **Omgevingsfuncties**.
1. Selecteer op het tabblad **e-Commerce** de optie **Instellingen**. Er wordt een dialoogvenster weergegeven, waarin u de vereiste gegevens voor de inrichting moet invoeren.
1. Vul de vereiste informatie in en ga naar de volgende pagina.
1. Vul de vereiste informatie in op de volgende pagina en verzend het formulier. U keert terug naar het tabblad **e-Commerce** en u ziet dat de initialisatie is gestart.
1. Als u de initialisatiestatus wilt weergeven, kiest u **Vernieuwen** of keert u later terug naar het tabblad **e-Commerce**.
    
Wanneer e-Commerce via LCS wordt geïnitialiseerd, worden verscheidene onderdelen ingesteld die nodig zijn voor e-commerce en die aan de omgeving worden gekoppeld. Nadat de inrichting is voltooid, wordt het tabblad **e-Commerce** op de pagina **Retail-beheer** bijgewerkt om de inrichting weer te geven. Op de pagina worden de nieuwste implementaties van aanpassingen en de status van andere lopende implementaties weergegeven. De pagina bevat ook koppelingen naar de e-Commerce-site en de site builder voor de e-Commerce-site waar sites worden geschreven.

## <a name="access-commerce-site-builder"></a>Commerce-site builder openen

Ga naar het tabblad **e-Commerce** op de pagina **Retail-beheer** in LCS en selecteer de koppeling **Beheerhulpprogramma van de e-Commerce-site** om toegang te krijgen tot site builder. De landingspagina voor site builder is een weergave op tenantniveau. Op deze pagina kunt u het volgende doen:

- Instellingen op tenantniveau wijzigen.
- Naar een site gaan die u hebt gemaakt en waarvoor u weergavemachtiging hebt. 
- Toegang verkrijgen tot beoordelingsfuncties, zoals moderator en rapportage.
- Maak een nieuwe site. Zie [Een e-Commerce-site maken](create-ecommerce-site.md) voor meer informatie over het maken van een nieuwe site. 

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een e-commerce-site maken](create-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
