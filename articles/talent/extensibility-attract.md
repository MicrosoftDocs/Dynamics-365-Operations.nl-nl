---
title: Uitbreidbaarheid in Attract
description: In dit onderwerp wordt beschreven hoe de toepassing Microsoft Dynamics 365 for Talent - Attract kan worden uitgebreid met behulp van het Microsoft Power Platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/12/2019
ms.locfileid: "949961"
---
# <a name="extensibility-in-attract"></a>Uitbreidbaarheid in Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent is ontwikkeld op het  Common Data Service-platform en kan op verschillende manieren worden uitgebreid met behulp van het Microsoft Power Platform en de mogelijkheden die Common Data Service biedt. Daarom kunt u het systeem configureren en aanpassen met behulp van Microsoft PowerApps en Microsoft Flow. U kunt ook extra analyses over personen krijgen met behulp van Microsoft Power BI. Bovendien maken nieuwe aangepaste activiteiten, zoals de PowerApps en webcontentactiviteiten (iFrame) het aanstellingsproces flexibeler dan ooit. Met deze activiteiten kunt u het aanstellingsproces aanpassen aan uw zakelijke behoeften en processen, en zorgen dat zowel het aanstellingsteam als de kandidaten een naadloze, aangepaste ervaring krijgen.

## <a name="extending-option-sets-in-attract"></a>Optiesets uitbreiden in Attract

Een **Optieset** (selectielijst) is een type veld dat kan worden opgenomen in een entiteit. Met een optieset wordt een set opties gedefinieerd. Als een optieset in een formulier wordt weergegeven, wordt een besturingselement voor een vervolgkeuzelijst gebruikt.  Attract bevat meerdere velden die optiesets zijn.  We zijn begonnen met het introduceren van de mogelijkheid om de optiesets uit te breiden, te beginnen met het veld Reden voor afwijzing, het veld Type dienstverband en het veld Type anciënniteit.   U kunt ook gelokaliseerde weergavelabels toevoegen voor de opties die u toevoegt. Zie voor meer informatie [Optiesetlabels aanpassen](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> De functionaliteit voor publicatie van vacatures naar LinkedIn vereist het gebruik van het veld **Type dienstverband** en **Type anciënniteit** op de pagina **Functiedetails**. De standaardwaarden in deze velden worden ondersteund door LinkedIn en worden weergegeven wanneer de vacature wordt gepubliceerd. Dus als u vacatures naar LinkedIn publiceert en de bestaande optiesetwaarden voor deze velden wijzigt, wordt de vacature wel gepubliceerd, maar worden op LinkedIn de aangepaste waarden voor **Type dienstverband** en **Type anciënniteit** niet weergegeven.  

Hieronder ziet u de stappen voor het bijwerken van het veld **Reden voor afwijzing** met waarden die specifiek voor uw bedrijf gelden.  

1. Als u de optieset **Reden voor afwijzing** wilt uitbreiden, gaat u naar de [PowerApps-beheer-website.](https://admin.powerapps.com)
2. Mogelijk wordt u gevraagd u aan te melden bij uw account. Geef uw gebruikers-ID- en wachtwoordreferenties op die u gebruikt voor aanmelding bij Dynamics365 en/of Office365. Klik vervolgens op **Volgende**.
3. Selecteer op het tabblad **Omgevingen** de omgeving die u wilt beheren, en dubbelklik erop om het tabblad **Details** te openen.
4. Selecteer op het tabblad **Details** **Dynamics 365-beheercentrum**.
5. Selecteer het exemplaar dat u wilt wijzigen en selecteer **Openen**.
6. Ga naar **Instellingen** en vervolgens **Aanpassingen** en kies **Het systeem aanpassen**.
7. Zoek de entiteit waarvoor u de optieset wilt uitvouwen door **Entiteiten** te selecteren en de groep uit te vouwen. In dit voorbeeld is dit de **entiteit Sollicitatie**.
8. Ga naar het veld waarvoor u de optieset wilt uitbreiden door de optie **Velden** te selecteren. In dit voorbeeld is dit **msdyn_rejectionreason**. Dubbelklik op het veld.
9. Kies in het veld **Optieset** **Bewerken**.
10. Selecteer het pictogram **+**.
11. Voer een **Label** in.  (Dit moet een unieke waarde zijn. Duplicaten zijn niet toegestaan).
12. Selecteer **Opslaan**.
13. Selecteer **Publiceren** boven aan de pagina.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Profiteren van het Microsoft Power Platform 

Omdat alle gegevens uit Attract zich bevinden in Common Data Service, kunt u hulpprogramma's van het Microsoft Power Platform gebruiken om uw unieke bedrijfsbehoeften op te nemen in Attract.

### <a name="powerapps"></a>PowerApps

U kunt PowerApps gebruiken om eenvoudig apps te maken die uw Attract-gegevens verbinden, en die expressies gebruiken zoals de expressies in Microsoft Excel om logica toe te voegen. Apps die u maakt met behulp van PowerApps, kunnen worden uitgevoerd op het web en op Apple iOS- en Google Android-apparaten.

U kunt bijvoorbeeld vacaturebeurzen eenvoudiger voor wervers maken door een lichtgewicht app te ontwikkelen waarmee ze cv's kunnen scannen en kandidaten kunnen voorstellen voor een positie in Attract. U kunt ook een app maken die helpt voldoen aan de behoeften aan conformiteit van uw organisatie. Zie voor meer informatie over PowerApps en hoe u deze gebruikt om apps te bouwen [Gegevens integreren in Common Data Service](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

U kunt Microsoft Flow gebruiken om geautomatiseerde werkstromen te maken die op Attract-gegevens worden uitgevoerd. U kunt eenvoudig verbinding maken met tal van populaire apps en services zonder code te schrijven. Door stromen te maken die interactie hebben met de Attract-entiteiten Functie, Kandidaat en Sollicitatie in Common Data Service, kunt u verschillende acties automatiseren. Wanneer een kandidaat bijvoorbeeld een aanbieding accepteert, kan een melding worden verzonden aan een onboardingteam of kan het nieuws worden aangekondigd op Twitter. Zie de  [Documentatie van Microsoft Flow](https://docs.microsoft.com/en-us/flow/) voor meer informatie over stromen.

### <a name="power-bi"></a>Power BI

Met Power BI BI kunt u aangepaste rapporten en dashboards maken en weergeven die u meer inzicht geven in uw Attract-gegevens. Zie voor meer informatie over Power BI en het bouwen van interactieve rapporten en dashboards de [Power BI-documentatie](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Aangepaste activiteiten 

U kunt aangepaste activiteiten, zoals de PowerApps-apps en webinhoudactiviteiten (iframe), toevoegen op het niveau van het taaksjabloonproces of terwijl u een nieuwe functie maakt. Met deze activiteiten kunt u het aanstellingsproces aanpassen en bedrijfslogica introduceren die uniek is voor uw organisatie in Attract.

#### <a name="powerapps-activity"></a>Activiteit PowerApps 

Met de activiteit PowerApps kan de maker van een functie of functieprocessjabloon een PowerApps-app insluiten in de aanstellingsstroom. Nadat u de app hebt gemaakt en gepubliceerd, kunt u de app-id ervan invoeren in de activiteitconfiguraties. Met behulp van een PowerApps-app kunt u gegevens lezen en schrijven in Common Data Service. U kunt de app zelfs koppelen aan een stroom. U hebt bijvoorbeeld een app die wervers gebruiken om een formulier in te vullen terwijl ze telefonische sollicitatiegesprekken houden. In dit geval kunt u de app koppelen aan een stroom die bepaalt of een sollicitant verder kan gaan in het sollicitatieproces. Dit type activiteit kan alleen worden bekeken door leden van het aanstellend team. Zie voor meer informatie over het configureren van de activiteit PowerApps [Activiteiten in Attract](./activities-attract.md).

> [!NOTE]
> De activiteit PowerApps is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

#### <a name="web-content-iframe-activity"></a>Activiteit Webinhoud (iframe)

Met de activiteit Web-inhoud (iframe) kunt u een aangepaste weboplossing insluiten die u hebt gemaakt in het aanstellingsproces of de kandidaatportal. U kunt gegevens direct lezen en schrijven uit Common Data Service. U kunt ook de oplossing aanpassen zodat deze stromen activeert of gebruikmaakt van functies van Microsoft Azure. Zie voor meer informatie over het configureren van de activiteit Webinhoud [Activiteiten in Attract](./activities-attract.md).

> [!NOTE]
> De activiteit Webinhoud is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.
