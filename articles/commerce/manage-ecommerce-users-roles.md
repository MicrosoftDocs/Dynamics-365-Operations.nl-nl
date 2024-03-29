---
title: e-Commerce-gebruikers en -rollen beheren
description: In dit artikel wordt uitgelegd hoe u gebruikerstoegang verleent voor de ontwerpomgeving voor uw Microsoft Dynamics 365 Commerce-site.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 180fc5c0a9c9e247d5bd6ec7f469f313463526df
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279497"
---
# <a name="manage-e-commerce-users-and-roles"></a>e-Commerce-gebruikers en -rollen beheren


[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u gebruikerstoegang verleent voor de ontwerpomgeving voor uw Microsoft Dynamics 365 Commerce-site.

De ontwerpomgeving voor websites maakt gebruik van beveiligingsgroepen die u maakt in Microsoft Azure Active Directory (Azure AD) om gebruikerstoegang te beheren en aan gebruikers toestemming te verlenen om specifieke taken uit te voeren. U wijst eerst een nieuwe of bestaande beveiligingsgroep uit Azure AD toe aan elke rol in de ontwerpomgeving. Vervolgens kunt u machtigingen verlenen of intrekken voor afzonderlijke gebruikers door deze gebruikers aan een geschikte beveiligingsgroep toe te voegen of ze uit een beveiligingsgroep te verwijderen.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Overzicht van rollen in de ontwerpomgeving

De Dynamics 365 for Commerce-ontwerpomgeving ondersteunt de volgende rollen.

| Rol                 | Beschrijving |
|----------------------|-------------|
| Systeembeheerder | Gebruikers die deze rol hebben, hebben alle bevoegdheden voor alle hulpprogramma's en voor alle beoordelingen en recensies. Ze kunnen ook sites maken. |
| Beheerder   | Gebruikers die deze rol hebben, hebben alle bevoegdheden voor alle hulpprogramma's, en beoordelingen en recensies in een bepaalde sitestructuur. |
| Webproducer         | Gebruikers die deze rol hebben, kunnen pagina's, fragmenten en sjablonen maken, assets uploaden en beheren, en producten en categorieën uitbreiden. |
| Lezer               | Gebruikers met deze rol kunnen pagina's, sjablonen, assets, fragmenten, indelingen en instellingen weergeven, maar kunnen geen wijzigingen aanbrengen. |
| RnR-moderator        | Gebruikers die deze rol hebben, kunnen productbeoordelingen verwerken. |

## <a name="system-administrator-role"></a>Systeembeheerdersrol

Wanneer u Dynamics 365 Commerce inricht in de Microsoft Dynamics Lifecycle Services-omgeving (LCS), wordt u gevraagd een beveiligingsgroep voor de rol van **systeembeheerder** op te geven. Deze rol wordt vervolgens automatisch toegepast op alle sites die u maakt in de omgeving die u configureert. De beveiligingsgroep voor deze rol kan alleen worden bijgewerkt in LCS. Op de pagina **Sitebeheer** voor alle sites wordt dit weergegeven als alleen-lezen en alleen ter informatie.

## <a name="administrator-role"></a>Beheerdersrol

Wanneer u een nieuwe site maakt in Commerce, wordt u gevraagd een beveiligingsgroep voor de rol **Beheerder** op te geven. Zie de tabel eerder in dit artikel voor een overzicht van de machtigingen die door deze rol worden verleend.

## <a name="add-or-update-security-groups"></a>Beveiligingsgroepen toevoegen of bijwerken

Nadat de site is gemaakt, hebben alleen gebruikers in de beveiligingsgroepen die zijn gekoppeld aan de rollen **Systeembeheerder** en **Beheerder**, toegang tot de ontwerpomgeving voor die site. Als u gebruikers wilt toewijzen aan de rollen **Webproducer**, **RnR-moderator** en **Lezer**, moet u beveiligingsgroepen toewijzen aan deze rollen. Voer de volgende stappen uit om een beveiligingsgroep aan een rol toe te voegen of om een beveiligingsgroep bij te werken die momenteel aan een rol is toegewezen.

1. Ga naar de site die u wilt bijwerken.
1. Open de pagina **Beveiliging** in **Sitebeheer**.
1. Selecteer de rol die u wilt wijzigen.
1. Voeg beveiligingsgroepen aan rollen toe of verwijder beveiligingsgroepen van rollen.

## <a name="additional-resources"></a>Aanvullende resources

[Scriptcode toevoegen aan sitepagina's voor ondersteuning van telemetrie](add-telemetry.md)

[Overwegingen bij SEO (Search Engine Optimization) voor uw site](search-engine-optimization-considerations.md)

[Beveiligingsbeleid voor inhoud (CSP) beheren](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
