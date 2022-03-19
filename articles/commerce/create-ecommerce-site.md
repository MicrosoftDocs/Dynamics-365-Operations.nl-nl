---
title: Een e-commerce-site maken
description: In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.
author: bicyclingfool
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e451b1c95c3e26d1292e7b8300b62af43c81f2f
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388206"
---
# <a name="create-an-e-commerce-site"></a>Een e-commerce-site maken

[!include [banner](includes/banner.md)]

In dit onderwerp worden de stappen en informatie beschreven die nodig zijn om een nieuwe e-Commerce-site in Dynamics 365 Commerce site builder te maken.

Wanneer u een licentie neemt voor de functies voor Dynamics 365 Commerce, wordt site builder ingericht met een startsite die u kunt gebruiken als basis voor uw eigen site. Als u echter zelf wilt beginnen of als u een tweede site wilt maken, moet u een nieuwe site maken in de site-ontwerpomgeving. 

## <a name="site-creation-prerequisites"></a>Vereisten voor het maken van een site

Een site builder-gebruiker moet een gebruikersaccount voor Microsoft Azure Active Directory (Azure AD) hebben in de Azure AD-beveiligingsgroep die is toegewezen aan de beheerders van het e-commercesysteem. Zie [Een nieuwe e-commercetenant implementeren](deploy-ecommerce-site.md) voor meer informatie.

> [!NOTE]
> Azure AD-gastgebruikers hebben mogelijk verschillende toegangsrechten in uw Azure AD-tenant. Zelfs als deze is opgenomen in de Azure AD-beveiligingsgroep die is toegewezen aan de e-commercesysteembeheerders, zijn voor een gastgebruiker in Azure AD mogelijk de machtigingsinstellingen **Externe gebruikers** nodig om een e-commercesite in Commerce te maken. 

Volg deze stappen om Azure AD-instellingen van **externe gebruikers** aan te passen.

1. Navigeer in de Azure-portal naar uw Azure AD-tenant.
1. Ga naar **Gebruikersinstellingen \> Externe gebruikers** en selecteer de koppeling **Externe samenwerkingsinstellingen beheren**. Hiermee opent u de pagina **Externe samenwerkingsinstellingen** waar toegang voor gastgebruikers, instellingen voor gastuitnodigingen en beperkingen voor samenwerking kunnen worden ingesteld. 
1. Pas de instellingen voor externe samenwerking aan conform het beveiligingsbeleid van uw bedrijf. 

## <a name="set-up-your-site"></a>Uw site instellen

Ga als volgt te werk als u uw site wilt instellen.

1. Open de site builder-omgeving. U vindt een koppeling naar de site builder in Microsoft Lifecycle Services (LCS) op de pagina omgevingsfuncties voor Commerce.
1. Selecteer **Nieuwe site** op de startpagina voor de ontwerpomgeving voor sites.
1. Geef in het dialoogvenster **Nieuwe site** de volgende informatie op.

| Veld                               | Beschrijving |
|-------------------------------------|-------------|
| Sitenaam                           | Voer de weergavenaam in die moet worden gebruikt voor uw site in de ontwerpomgeving. Deze naam is alleen zichtbaar in de ontwerpomgeving en wordt niet weergegeven voor klanten. |
| Beveiligingsgroep van de sitebeheerder | Geef de beveiligingsgroep voor Microsoft Azure Active Directory (Azure AD) op waarmee gebruikers met de rol van sitebeheerder op deze site worden beheerd. |
| Standaardkanaal (nummer operationele eenheid) | Selecteer de online winkel waarvoor deze site als webwinkel zal dienen. Als u wilt dat uw e-commerce-site meerdere online winkels ondersteunt, moet u de winkels aan uw site koppelen in de **Site-instellingen** nadat de site is ingesteld. |
| Standaardtaal                            | Geef de standaardtaal op voor deze online winkel en markt. Een online winkel kan meerdere talen ondersteunen. Als u meerdere talen wilt ondersteunen voor deze online winkel of een andere online winkel, kunt u dat configureren in **Site-instellingen** nadat de site is ingesteld.  |
| Domein                              | Selecteer een domein dat als domein zal dienen voor deze online winkel. Als u geen domeinen in LCS hebt geconfigureerd, kunt u dit veld leeg laten. Nadat uw domein in LCS is geconfigureerd, moet u dit aan uw online winkel toevoegen in de **Site-instellingen**.  |
| Pad                              | Wanneer uw site meerdere talen ondersteunt voor een bepaalde domeinnaam, gebruikt u het padveld om een unieke site-URL te maken voor die domein- en taalcombinatie. Als de taal die u hebt opgegeven in het veld **Standaardtaal** de enige taal is die u voor dit domein wilt gebruiken of de standaardtaal blijft nadat u uw site hebt gelokaliseerd in extra talen, wordt u aangeraden dit veld leeg te laten. |

Nadat de site is gemaakt, kunt u controleren of deze is gekoppeld aan uw online winkel door het tabblad **Producten** te selecteren. Het assortiment met producten dat aan de online winkel is toegewezen, wordt weergeven. U kunt ook het vervolgkeuzemenu in de linkerbovenhoek van de pagina gebruiken om toegang te krijgen tot de toegewezen producten per categorie.

## <a name="rename-your-site"></a>Naam van uw site wijzigen

Voer de volgende stappen uit om de naam van uw site te wijzigen in Site Builder.

1. Als u de lijstweergave met sites wilt openen, selecteert u **Sites wisselen** in de rechterbovenhoek en selecteert u vervolgens **Sites beheren**. 
1. Schakel het selectievakje in naast de site waarvan u de naam wilt wijzigen en selecteer vervolgens **Naam wijzigen** op de opdrachtbalk.
1. Voer in het dialoogvenster **Nieuwe sitenaam** de nieuwe sitenaam in en selecteer vervolgens **OK**. De sitelijst wordt bijgewerkt om de nieuwe naam van de site weer te geven.

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-B2C-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-B2C-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
