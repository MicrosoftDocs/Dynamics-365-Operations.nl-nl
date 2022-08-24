---
title: Een sandbox-omgeving inrichten voor Dynamics 365 Commerce
description: In dit artikel wordt beschreven hoe u een sandbox-omgeving van Microsoft Dynamics 365 Commerce voor demonstratie- of sandbox-gebruik kunt inrichten met ingebouwde demonstratiegegevens.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283636"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Een sandbox-omgeving inrichten voor Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een sandbox-omgeving van Microsoft Dynamics 365 Commerce voor demonstratiegebruik kunt inrichten met ingebouwde demonstratiegegevens. Het proces voor het instellen van een productieomgeving is vergelijkbaar, maar uitgebreider, omdat veel van de vereisten van de sandbox-omgeving al in de demonstratiegegevens zijn geleverd.

Voordat u begint, kunt u het beste dit artikel snel doorlezen om een idee te krijgen van wat nodig is voor het proces.

Als u een sanbox-omgeving voor Commerce wilt inrichten, moet u een aantal parameters voor de omgeving en CSU (Commerce Scale Unit) opgeven die worden gebruikt wanneer u Commerce later inricht. De instructies in dit artikel beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.

Nadat de inrichting van de omgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de omgeving voor te bereiden. Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt gebruiken. U kunt de optionele stappen altijd later voltooien.

Zie [Een sandbox-omgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw preview-omgeving voor Commerce configureert nadat u deze hebt ingericht. Zie [Optionele functies voor een sandbox-omgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw omgeving van Commerce configureert.

## <a name="prerequisites"></a>Vereisten

Aan de volgende voorwaarden moeten zijn voldaan voordat u uw omgeving van Commerce inricht:

- U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).
- U bent een bestaande Microsoft Dynamics 365-partner of -klant en u hebt al een implementatieproject gemaakt en dat beschikbaar is voor gebruik in LCS.  
- U hebt een Azure Active Directory-beveiligingsgroep (Azure AD) gemaakt om te gebruiken als Commerce-systeembeheerdersgroep en u hebt de id bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand. (Deze beveiligingsgroep kan dezelfde zijn als de Commerce-systeembeheerdersgroep.)
- U hebt een exemplaar van Headquarters in LCS geïmplementeerd. Zie [Een nieuwe omgeving implementeren](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) voor meer informatie.

Deze lijst is niet volledig. Neem contact op met uw Microsoft-partner voor hulp als u problemen ondervindt.

## <a name="provision-your-commerce-environment"></a>Uw omgeving van Commerce inrichten

In de volgende procedures wordt uitgelegd hoe u een omgeving van Commerce inricht. Als u dit hebt gedaan, is de omgeving van Commerce gereed voor configuratie. Alle stappen die hieronder worden beschreven, vinden plaats in de LCS-portal.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit initialiseren (cloud)

Ga als volgt te werk om de CSU te initialiseren.

1. Selecteer in LCS uw omgeving in de lijst.
1. Selecteer **Volledige details** in de weergave **OMGEVINGEN** rechts. De weergave met omgevingsdetails wordt weergegeven.
1. Selecteer **Beheren** in de sectie **Omgeving beheren** onder **OMGEVINGSFUNCTIES**.
1. Selecteer **Initialiseren** op het tabblad **Commerce Scale Units**. De weergave **Schaaleenheid toevoegen** wordt weergegeven.
1. Selecteer in het veld **REGIO** de regio die gelijk is aan of dichtbij de regio waar u de omgeving hebt geïmplementeerd.
1. Selecteer de meest recente versie in de vervolgkeuzelijst **Versie**.
1. Selecteer **Initialiseren**.
1. Selecteer **Ja** in het dialoogvenster met waarschuwingen waarin u wordt gevraagd de initialisatie van Commerce Scale Unit te bevestigen. De CSU is nu in de wachtrij geplaatst voor inrichting.
1. Voordat u verdergaat, moet u controleren of de CSU-status **GELUKT** is. Initialisatie duurt ongeveer twee tot vijf uur.

Als u de koppeling **Beheren** niet kunt vinden in de weergave met omgevingsdetails, neemt u contact op met Microsoft voor hulp.

### <a name="initialize-e-commerce"></a>e-Commerce initialiseren

Ga als volgt te werk om Commerce te initialiseren.

1. Selecteer op het tabblad **e-Commerce** de optie **Instellingen**.
1. Voer een naam in bij **Omgevingsnaam e-Commerce**. Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.
1. Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst. (De lijst moet slechts één optie hebben.)

    Het veld **Geografie van e-Commerce** wordt automatisch ingesteld.

1. Selecteer **Volgende** om door te gaan.
1. Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.
1. Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
1.  Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
1. Laat de optie **Service voor beoordelingen en recensies inschakelen** op **Ja** staan.
1. Selecteer **Initialiseren**. De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd. De initialisatie van e-Commerce is gestart.
1. Voordat u verdergaat, moet u wachten tot de initialisatiestatus van Commerce **GEÏNITIEERD** is.
1. Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:

    * **e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.
    * **Commerce Site Builder**: de koppeling naar het beheerhulpprogramma van de site.

## <a name="next-steps"></a>Volgende stappen

Zie [Een sandbox-omgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw preview-omgeving voor Commerce.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een sandbox-omgeving van Dynamics 365 Commerce configureren](cpe-post-provisioning.md)

[BOPIS configureren in een sandbox-omgeving van Dynamics 365 Commerce](cpe-bopis.md)

[Optionele functies voor een sandbox-omgeving van Dynamics 365 Commerce configureren](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (cloud)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
