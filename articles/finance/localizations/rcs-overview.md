---
title: Regulatory Configuration Service
description: In dit onderwerp wordt een overzicht gegeven van de functies van RCS (Regulatory Configuration Service) en wordt uitgelegd hoe u toegang krijgt tot de service.
author: JaneA07
ms.date: 06/04/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 816b1bf9da9acdd5999320f39fb68fb6deda197c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983462"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) is een zelfstandige ontwerpfunctie en lifecyclebeheerservice voor globalisatiefunctionaliteit zonder code/met weinig code. Met RCS kunnen globalisatiepartijen belangrijke globalisatiegebieden van belasting, e-facturering, wettelijke rapportage, bankdocumenten en bedrijfsdocumenten uitbreiden en aanpassen zonder ontwikkelaars. Door deze globalisatie zonder code/met weinig code wordt globalisatie eenvoudiger, sneller en effectiever om te maken of uit te breiden.

RCS biedt de volgende mogelijkheden:

- Ondersteuning voor alle functionaliteit die wordt geleverd door Elektronische rapportage (ER).
- Een vereiste voor het configureren van nieuwe microservices voor globalisatie.
- Ondersteuning voor Elektronische facturering. Zie [Elektronische facturering](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) voor meer informatie.
- Ondersteunt Belastingberekening. Zie voor meer informatie [Belastingservice](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).
- Ondersteuning voor nieuwe functionaliteit voor globalisatiefuncties die het levenscyclusbeheer van meerdere componentfuncties vereenvoudigt en extra mogelijkheden biedt voor het configureren van acties en het instellen van functieparameters. Zie [Regulatory Configuration Service – vereenvoudigd globalisatiefunctiebeheer voor globalisatieservices](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)  voor meer informatie.
- Ondersteuning voor gecentraliseerde publicatie, opslag en het delen van aangepaste configuraties in de Algemene opslagplaats om configuratiebeheer te vereenvoudigen zonder dat Microsoft Dynamics Lifecycle Services moet worden gebruikt.

## <a name="access-rcs"></a>Toegang tot RCS

U kunt zich registreren voor RCS of u aanmelden via de pagina [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

![Registreren/aanmelden bij RCS.](media/202103_RCS%20Marketing%20page_updated_1.jpg)

Controleer op de pagina **Regulatory Configuration Service** de aanvullende algemene voorwaarden voor gebruik van de service. Accepteer deze en selecteer een van de volgende knoppen:

- **Registreren** als u een nieuwe gebruiker van de service bent en u een bedrijfse-mailadres gebruikt om uw organisatie een serviceomgeving in te richten
- **Aanmelden** als u zich eerder hebt aangemeld voor de service en u toegang wilt krijgen tot uw organisatieomgeving

> [!NOTE] 
> Nadat u zich hebt aangemeld, is het raadzaam om een extra SysAdmin-gebruiker toe te voegen aan de RCS-omgeving. Deze gebruiker wordt ingericht als co-beheerder voor de omgeving. Dit helpt om de toegang tot de RCS-omgeving te stabiliseren, aangezien de rol SysAdmin het beheren van gebruikers voor die omgeving is. U kunt gebruikers toevoegen met behulp van **RCS-werkgebied > Systeembeheer**.

## <a name="regional-availability"></a>Regionale beschikbaarheid

RCS is algemeen beschikbaar in de volgende regio's:

- Verenigde Staten
- India
- Frankrijk
- Europa

Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/dynamics_365_international_availability_deck) voor een volledige lijst met regio's.

## <a name="rcs-default-company"></a>RCS-standaardbedrijf

Ontwerptijdfunctionaliteit die wordt gebruikt in RCS, wordt gedeeld door alle bedrijven. Er is geen bedrijfsspecifieke functionaliteit. Daarom is het raadzaam dat u één bedrijf, **DAT**, gebruikt voor uw RCS-omgeving.

In sommige scenario's wilt u echter dat ER-indelingen gebruikmaken van parameters die aan een bepaalde rechtspersoon zijn gerelateerd. Uitsluitend in deze scenario's moet u de standaardbedrijfsschakelknop gebruiken. Zie [ER-indelingen configureren om parameters te gebruiken die per rechtspersoon worden opgegeven](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md) voor een voorbeeld.

## <a name="related-rcs-documentation"></a>Gerelateerde RCS-documentatie

Zie de volgende onderwerpen voor meer informatie over gerelateerde onderdelen:

- **RCS:**

    - [ER-configuraties maken in RCS en ze uploaden naar de algemene opslagplaats](rcs-global-repo-upload.md)

- **Algemene opslagplaats:**

    - [ER-configuratie maken en uploaden naar algemene opslagplaats](rcs-global-repo-upload.md)
    - [Configuratie delen in algemene opslagplaats](rcs-global-repo-share-configuration.md)
    - [Verbeterde filters in algemene opslagplaats](enhanced-filtering-global-repo.md)
    - [ER-configuraties downloaden uit de algemene opslagplaats](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [Configuraties stopzetten in de algemene opslagplaats](discontinuing-configurations-rcs-global-repo.md)
    - [Afschaffing Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage](rcs-lcs-repo-dep-faq.md)

- **Globalisatiefunctie:**

    - [Regulatory Configuration Service (RCS) - globalisatiefunctie](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a>Problemen met RCS-registratie oplossen

Wanneer u zich via de servicepagina bij RCS aanmeldt, kunt u een probleem aantreffen dat betrekking heeft op Azure Active Directory (Azure AD). Het foutbericht dat u ontvangt, geeft aan dat de aanmelding bij RCS momenteel is uitgeschakeld en moet worden ingeschakeld voordat u het aanmeldingsproces kunt voltooien.

![Foutbericht voor RCS-registratie.](media/01_RCSSignUpError.jpg)

Het probleem treedt op omdat u bent geblokkeerd voor het aanmelden voor ad-hoc abonnementen en de eigenschap `AllowAdHocSubscriptions` moet zijn ingeschakeld in uw tenant. 

- Als uw IT-afdeling de Azure-tenants van uw organisatie beheert, neem dan contact op met die afdeling om het probleem te melden.
- Als u verantwoordelijk bent voor het beheer van uw Azure-tenants, kunt u de problemen oplossen door de stappen in [Wat is selfserviceaanmelding voor Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings) uit te voeren.
