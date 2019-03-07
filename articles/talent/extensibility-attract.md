---
title: Uitbreidbaarheid in Attract
description: In dit onderwerp wordt beschreven hoe de toepassing Microsoft Dynamics 365 for Talent - Attract kan worden uitgebreid met behulp van het Microsoft Power Platform.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303871"
---
# <a name="extensibility-in-attract"></a>Uitbreidbaarheid in Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent is ontwikkeld op het Common Data Service (CDS) voor Apps-platform en kan op verschillende manieren worden uitgebreid met behulp van het Microsoft Power Platform en de mogelijkheden die Common Data Service voor Apps biedt. Daarom kunt u het systeem configureren en aanpassen met behulp van Microsoft PowerApps en Microsoft Flow. U kunt ook extra analyses over personen krijgen met behulp van Microsoft Power BI. Bovendien maken nieuwe aangepaste activiteiten, zoals de PowerApps en webcontentactiviteiten (iFrame) het aanstellingsproces flexibeler dan ooit. Met deze activiteiten kunt u het aanstellingsproces aanpassen aan uw zakelijke behoeften en processen, en zorgen dat zowel het aanstellingsteam als de kandidaten een naadloze, aangepaste ervaring krijgen.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Profiteren van het Microsoft Power Platform 

Omdat alle gegevens uit Attract zich bevinden in Common Data Service voor Apps, kunt u hulpprogramma's van het Microsoft Power Platform gebruiken om uw unieke bedrijfsbehoeften op te nemen in Attract.

### <a name="powerapps"></a>PowerApps

U kunt PowerApps gebruiken om eenvoudig apps te maken die uw Attract-gegevens verbinden, en die expressies gebruiken zoals de expressies in Microsoft Excel om logica toe te voegen. Apps die u maakt met behulp van PowerApps, kunnen worden uitgevoerd op het web en op Apple iOS- en Google Android-apparaten.

U kunt bijvoorbeeld vacaturebeurzen eenvoudiger voor wervers maken door een lichtgewicht app te ontwikkelen waarmee ze cv's kunnen scannen en kandidaten kunnen voorstellen voor een positie in Attract. U kunt ook een app maken die helpt voldoen aan de behoeften aan conformiteit van uw organisatie. Zie voor meer informatie over PowerApps en hoe u deze gebruikt om apps te bouwen [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

U kunt Microsoft Flow gebruiken om geautomatiseerde werkstromen te maken die op Attract-gegevens worden uitgevoerd. U kunt eenvoudig verbinding maken met tal van populaire apps en services zonder code te schrijven. Door stromen te maken die interactie hebben met de Attract-entiteiten Functie, Kandidaat en Sollicitatie in Common Data Service voor Apps, kunt u verschillende acties automatiseren. Wanneer een kandidaat bijvoorbeeld een aanbieding accepteert, kan een melding worden verzonden aan een onboardingteam of kan het nieuws worden aangekondigd op Twitter. Zie de  [Documentatie van Microsoft Flow](https://docs.microsoft.com/en-us/flow/) voor meer informatie over stromen.

### <a name="power-bi"></a>Power BI

Met Power BI BI kunt u aangepaste rapporten en dashboards maken en weergeven die u meer inzicht geven in uw Attract-gegevens. Zie voor meer informatie over Power BI en het bouwen van interactieve rapporten en dashboards de [Power BI-documentatie](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Aangepaste activiteiten 

U kunt aangepaste activiteiten, zoals de PowerApps-apps en webinhoudactiviteiten (iframe), toevoegen op het niveau van het taaksjabloonproces of terwijl u een nieuwe functie maakt. Met deze activiteiten kunt u het aanstellingsproces aanpassen en bedrijfslogica introduceren die uniek is voor uw organisatie in Attract.

#### <a name="powerapps-activity"></a>Activiteit PowerApps 

Met de activiteit PowerApps kan de maker van een functie of functieprocessjabloon een PowerApps-app insluiten in de aanstellingsstroom. Nadat u de app hebt gemaakt en gepubliceerd, kunt u de app-id ervan invoeren in de activiteitconfiguraties. Met behulp van een PowerApps-app kunt u gegevens lezen en schrijven in Common Data Service voor Apps. U kunt de app zelfs koppelen aan een stroom. U hebt bijvoorbeeld een app die wervers gebruiken om een formulier in te vullen terwijl ze telefonische sollicitatiegesprekken houden. In dit geval kunt u de app koppelen aan een stroom die bepaalt of een sollicitant verder kan gaan in het sollicitatieproces. Dit type activiteit kan alleen worden bekeken door leden van het aanstellend team. Zie voor meer informatie over het configureren van de activiteit PowerApps [Activiteiten in Attract](./activities-attract.md).

> [!NOTE]
> De activiteit PowerApps is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.

#### <a name="web-content-iframe-activity"></a>Activiteit Webinhoud (iframe)

Met de activiteit Web-inhoud (iframe) kunt u een aangepaste weboplossing insluiten die u hebt gemaakt in het aanstellingsproces of de kandidaatportal. U kunt gegevens direct lezen en schrijven uit Common Data Service voor Apps. U kunt ook de oplossing aanpassen zodat deze stromen activeert of gebruikmaakt van functies van Microsoft Azure. Zie voor meer informatie over het configureren van de activiteit Webinhoud [Activiteiten in Attract](./activities-attract.md).

> [!NOTE]
> De activiteit Webinhoud is alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen.
