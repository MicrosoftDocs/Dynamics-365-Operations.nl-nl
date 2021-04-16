---
title: Een evaluatieomgeving voor Dynamics 365 Commerce inrichten
description: In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19cedf01d1b916de785454d55448f41d1f5db1df
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792286"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Een evaluatieomgeving voor Dynamics 365 Commerce inrichten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een evaluatieomgeving van Microsoft Dynamics 365 Commerce inricht.

Voordat u begint, kunt u het beste dit onderwerp snel doorlezen om een idee te krijgen van wat nodig is voor het proces.

> [!NOTE]
> Commerce-evaluatieomgevingen zijn doorgaans niet beschikbaar en worden aan partners en klanten op aanvraag ter beschikking gesteld. Neem contact op met uw Microsoft-partner voor meer informatie.

Als u uw evaluatieomgeving van Commerce wilt inrichten, moet u een project maken met een specifieke productnaam en een specifiek producttype. De omgeving en Commerce Scale Unit (CSU) beschikken ook over specifieke parameters die u moet gebruiken wanneer u e-Commerce later wilt inrichten. De instructies in dit onderwerp beschrijven alle vereiste stappen voor het voltooien van de inrichting en de parameters die u moet gebruiken.

Nadat de inrichting van de evaluatieomgeving van Commerce is voltooid, moet u een aantal stappen uitvoeren om de preview-omgeving voor te bereiden. Sommige stappen zijn optioneel, afhankelijk van de aspecten van het systeem die u wilt evalueren. U kunt de optionele stappen altijd later voltooien.

Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) voor meer informatie over hoe u uw evaluatieomgeving voor Commerce configureert nadat u deze hebt ingericht. Zie [Optionele functies voor een evaluatieomgeving van Commerce configureren](cpe-optional-features.md) voor meer informatie over hoe u optionele functies voor uw evaluatieomgeving van Commerce configureert.

## <a name="prerequisites"></a>Vereisten

Aan de volgende voorwaarden moeten zijn voldaan voordat u uw evaluatieomgeving van Commerce inricht:

- U bent geregistreerd voor het evaluatieprogramma en hebt capaciteit gekregen voor een evaluatieomgeving.
- U hebt toegang tot de Microsoft Dynamics Lifecycle Services-portal (LCS).
- U bent een bestaande Microsoft Dynamics 365-partner of -klant en kunt een Dynamics 365 Commerce-project maken.
- U hebt beheerderstoegang tot uw Microsoft Azure-abonnement of u bent in contact met een abonnementsbeheerder die u kan helpen als dat nodig is.
- U hebt uw Azure Active Directory-tenant-id (Azure AD) bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als e-Commerce-systeembeheerdersgroep en u hebt de id bij de hand.
- U hebt een Azure AD-beveiligingsgroep gemaakt om te gebruiken als moderatorgroep voor beoordelingen en recensies en u hebt de id bij de hand. (Deze beveiligingsgroep kan dezelfde zijn als de systeembeheerdersgroep van e-Commerce.)

Deze lijst is niet volledig. Neem contact op met uw Microsoft-partner voor hulp als u problemen ondervindt.

## <a name="provision-your-commerce-evaluation-environment"></a>Uw evaluatieomgeving van Commerce inrichten

In deze procedures wordt uitgelegd hoe u een evaluatieomgeving van Commerce inricht. Als u dit hebt gedaan, is de evaluatieomgeving van Commerce gereed voor configuratie. Alle activiteiten die hier worden beschreven, vinden plaats in de LCS-portal.

### <a name="create-a-new-project"></a>Een nieuw project maken

Ga als volgt te werk om een nieuw project te maken in LCS.

1. Selecteer op de LCS-startpagina het plusteken (**+**) om een project te maken.
1. Volg een van de volgende stappen uit in het rechterdeelvenster:

    - Als u een partner bent, selecteert u **Migreren, oplossingen maken en informatie over**.
    - Als u een klant bent, selecteert u **Potentiële presales**.

1. Voer een naam, beschrijving en branche in.
1. Selecteer **Dynamics 365 Commerce** in het veld **Productnaam**.
1. Selecteer **Dynamics 365 Commerce** in het veld **Productversie**.
1. Selecteer **Implementatiemethodologie voor Dynamics Retail** in het veld **Methodologie**.
1. Optioneel: u kunt rollen en gebruikers importeren uit bestaand project.
1. Selecteer **Maken**. De projectweergave wordt weergegeven.

### <a name="add-the-azure-connector"></a>De Azure-connector toevoegen

Om de Azure-connector aan uw LCS-project toe te voegen volgt u de stappen in de procedure voor [het voltooien van het onboardingproces van Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).

### <a name="deploy-the-environment"></a>De omgeving implementeren

Ga als volgt te werk om de omgeving te implementeren.

> [!NOTE]
> Het is mogelijk dat u de stappen 6, 7 en/of 8 niet hoeft te voltooien, omdat pagina's met één optie worden overgeslagen. Controleer in de weergave **Omgevingsparameters** of u de tekst **Dynamics 365 Commerce - Demo (10.0.* x* met Platform update *xx*)** direct boven het veld **Omgevingsnaam** ziet. Zie de afbeelding die na stap 8 wordt weergegeven voor nadere details.

1. Selecteer in het bovenste menu de optie **Cloudomgevingen**.
1. Selecteer **Toevoegen** om een omgeving toe te voegen.
1. Selecteer in het veld **Toepassingsversie** de meest recente versie. Als u specifiek een andere toepassingsversie dan de meest recente versie wilt selecteren, moet u geen eerdere versie dan **10.0.14** selecteren.
1. Gebruik in het veld **Platformversie** de platform versie die automatisch wordt gekozen voor de toepassingsversie die u hebt geselecteerd. 

    ![Toepassings- en platformversies selecteren](./media/project1.png)

1. Selecteer **Volgende**.
1. Selecteer **Demo** als de omgevingstopologie.

    ![De omgevingstopologie 1 selecteren](./media/project2.png)

1. Voer op de pagina **Omgeving implementeren** een omgevingsnaam in. Laat geavanceerde instellingen ongewijzigd.

    ![De pagina Omgeving implementeren](./media/project4.png)

1. Pas de VM-grootte naar wens aan. (We raden VM-voorraadeenheid \[SKU\] **D13 v2** aan.)
1. Controleer de prijs- en licentievoorwaarden en schakel vervolgens het selectievakje in om aan te geven dat u ermee instemt.
1. Selecteer **Volgende**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Implementeren**. U keert terug naar de weergave in **Cloudomgevingen** en uw omgeving wordt weergegeven in de lijst.

    Uw aangevraagde omgeving wordt weergegeven in de wachtrij en vervolgens geïmplementeerd. Het duurt even voordat de werkstromen van de omgeving zijn voltooid. Controleer dit daarom na ongeveer zes tot negen uur.

1. Voordat u verdergaat, moet u controleren of de omgevingsstatus **Geïmplementeerd** is.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit initialiseren (cloud)

Ga als volgt te werk om de CSU te initialiseren.

1. Selecteer in de weergave **Cloudomgevingen** uw omgeving in de lijst.
1. Klik op **Volledige details** in de omgevingsweergave rechts. De weergave met omgevingsdetails wordt weergegeven.
1. Selecteer **Beheren** onder **Omgevingsfuncties**.
1. Selecteer **Initialiseren** op het tabblad **Commerce**. De weergave CSU-initialisatieparameters wordt weergegeven.
1. Selecteer in het veld **Regio** de regio die gelijk is aan of dichtbij de regio waar u de omgeving hebt geïmplementeerd.
1. Laat het veld **Versie** ongewijzigd.
1. Selecteer **Initialiseren**.
1. Controleer op de bevestigingspagina voor de implementatie of de details juist zijn en klik op **Ja**. De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **Commerce** is geselecteerd. Uw CSU is in de wachtrij geplaatst voor inrichting.
1. Voordat u verdergaat, moet u controleren of de CSU-status **Gelukt** is. Initialisatie duurt ongeveer twee tot vijf uur.

Als u de koppeling **Beheren** niet kunt vinden in de weergave met omgevingsdetails, neemt u contact op met Microsoft voor hulp.

Mogelijk wordt het volgende foutbericht weergegeven tijdens het implementatieproces:

> Voor evaluatieomgevingen (demo/test) moet de connectortoepassing voor schaaleenheden \<application ID\> in Headquarters worden geregistreerd.

Als de CSU-initialisatie mislukt en u dit foutbericht ontvangt, noteert u de toepassings-id (een GUID) en volg vervolgens de stappen in de volgende sectie om de CSU-implementatietoepassing in Commerce Headquarters te registreren.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>De CSU-implementatietoepassing in Commerce Headquarters registreren (indien nodig)

Voer de volgende stappen uit om de CSU-implementatietoepassing in Commerce Headquarters te registreren.

1. Ga in Commerce Headquarters naar **Systeembeheer \> Instellen \> Azure Active Directory-toepassingen**.
1. Voer in de kolom **Client-id** de toepassings-id uit het foutbericht voor CSU-initialisatie in dat u hebt ontvangen.
1. Voer in de kolom **Naam** een beschrijvende tekst in (bijvoorbeeld **CSU-eval**).
1. Voer in de kolom **Gebruikers-id** de tekst **RetailServiceAccount** in.
1. Probeer de CSU-initialisatie en -implementatie opnieuw uit te voeren vanuit LCS.

### <a name="initialize-e-commerce"></a>e-Commerce initialiseren

Ga als volgt te werk om e-Commerce te initialiseren.

1. Controleer op het tabblad **e-Commerce** de toestemming voor de evaluatie en selecteer vervolgens **Instellen**.
1. Voer een naam in bij **Omgevingsnaam e-Commerce**. Houd er rekening mee dat deze naam wordt weergegeven in sommige URL's die naar uw e-Commerce-exemplaar verwijzen.
1. Selecteer in het veld **Naam Commerce Scale Unit** uw CSU in de lijst. (De lijst moet slechts één optie hebben.)

    Het veld **Geografie van e-Commerce** wordt automatisch ingesteld.

1. Selecteer **Volgende** om door te gaan.
1. Voer in het veld **Ondersteunde hostnamen** een geldig domein in, bijvoorbeeld `www.fabrikam.com`.
1. Voer in het veld **AAD-beveiligingsgroep voor systeembeheer** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
1.  Voer in het veld **AAD-beveiligingsgroep voor moderator van beoordelingen en recensies** de eerste paar letters van de naam van de beveiligingsgroep in die u wilt gebruiken en selecteer vervolgens het vergrootglassymbool om de zoekresultaten weer te geven. Selecteer de juiste beveiligingsgroep in de lijst.
1. Laat de optie **Service voor beoordelingen en recensies inschakelen** op **Ja** staan.
1. Selecteer **Initialiseren**. De weergave **Commerce-beheer** wordt opnieuw weergegeven, waarbij het tabblad **e-Commerce** is geselecteerd. De initialisatie van e-Commerce is gestart.
1. Voordat u verdergaat, moet u wachten tot de initialisatiestatus van e-Commerce **Geïnitieerd** is.
1. Let onder **Koppeling** in de rechterbenedenhoek op de URL's voor de volgende koppelingen en noteer deze:

    * **e-Commerce-site**: de koppeling naar de hoofdmap van uw e-Commerce-site.
    * **Commerce Site Builder**: de koppeling naar het beheerhulpprogramma van de site.

## <a name="next-steps"></a>Volgende stappen

Zie [Een evaluatieomgeving van Commerce configureren](cpe-post-provisioning.md) om door te gaan met het inrichten en configureren van uw evaluatieomgeving voor Commerce.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce](cpe-overview.md)

[Een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-post-provisioning.md)

[BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving](cpe-bopis.md)

[Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-optional-features.md)

[Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (cloud)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
