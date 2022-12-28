---
title: Preview van Dynamics 365 Commerce 10.0.30 (November 2022)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics 365 Commerce 10.0.30 nieuw of gewijzigd zijn.
author: josaw1
ms.date: 12/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: a449c7eff21c059555f9659ea932705858d26275
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831742"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Preview van Dynamics 365 Commerce 10.0.30 (November 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Microsoft Dynamics 365 Commerce previewversie 10.0.30. Deze versie heeft het buildnummer 10.0.1362 en is beschikbaar volgens de onderstaande planning:

- **Preview-versie:** september 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** oktober 2022
- **Algemene beschikbaarheid van versie (automatische update):** november 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit artikel.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door |
|---------|------------------|----------------|--------------| 
| Klantondersteuning   | Chat op een e-commercesite met een Power Virtual Agents-bot. | Via deze functie kunnen gebruikers van de e-commercesite een Power Virtual Agents-chatbot gebruiken voor ondersteuningsaanvragen. | Ingeschakeld door beheerder/makers voor eindgebruikers |
| Inzichten  |  Geef operationele inzichten van het verkooppunt (POS) door naar uw Application Insights-account. | [Toegang tot logboeken in Application Insights](../dev-itpro/operational-insights.md#enable-diagnostic-events-in-application-insights)   |  Aanmelden voor IT-pro/ontwikkelaar   |
|  Betalingen  | Ondersteuning voor PayPal-order na de autorisatieperiode van 29 dagen. | De maximum autorisatieperiode voor PayPal is 29 dagen, waarna een nieuwe autorisatie- en order-id moet worden gegenereerd. In plaats daarvan biedt PayPal een optie waarmee naar een PayPal-order kan worden verwezen als een algemene order, waarbij meerdere autorisaties zijn verleend en op basis van dezelfde order-id mogen worden vastgeslagen en niet binnen 29 dagen een nieuwe autorisatie- en order-id kan worden gegenereerd. | Bij het configureren van de PayPal-betalingsconnector in Commerce Headquarters is het veld **OrderIntent** toegevoegd en kan het twee waarden hebben:<p><p>- **Autoriseren**: deze configuratie is de standaardconfiguratie (als u dit veld leeg laat, is **Autoriseren** de standaardwaarde). De configuratie van **OrderIntent** met **Autoriseren** is gekoppeld aan de PayPal-waarde voor **processing_instruction** van **NO_INSTRUCTION**. De order wordt geautoriseerd met PayPal en de autorisatie kan niet worden gewijzigd wanneer deze waarde wordt gebruikt.<p>- **Opslaan**: wanneer de waarde **OrderIntent** wordt ingesteld op **Opslaan**, is dit gekoppeld aan de PayPal-waarde voor **processing_instruction** van **ORDER_SAVED_EXPLICITLY**. Orderverwijzingen worden opgeslagen in de PayPal-service wanneer deze waarde wordt gebruikt.  |
| Aanmelden bij POS  | [Diagnosemogelijkheden voor selfservice inschakelen voor aanmelding bij POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Deze functie biedt selfservice-diagnosemogelijkheden op het POS en in Commerce Headquarters om winkelmedewerkers en managers te helpen snel de hoofdoorzaken van POS-aanmeldingsproblemen te identificeren en op te lossen.<p><p>- De foutberichten die op het POS-aanmeldingsscherm worden weergegeven, zijn verbeterd, zodat er informatie wordt weergegeven over de hoofdoorzaak. Winkelmedewerkers kunnen sneller begrijpen wat er is misgegaan, zodat ze de noodzakelijke acties kunnen uitvoeren om het probleem op te lossen.<p>- Er is een functie **Testaanmelding** op de pagina **Werknemers** in Commerce Headquarters, zodat winkelmanagers die POS-apparaten instellen, POS-aanmeldingen kunnen simuleren. In het geval van een aanmeldingsstoring, helpt deze functie bij het oplossen van problemen, zodat managers relevante configuraties kunnen controleren, problemen kunnen corrigeren en de oplossingen kunnen valideren.  | Standaard ingeschakeld |


## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Dynamics 365 Finance 10.0.30 bevat platformupdates. Zie voor meer informatie [Platformupdates voor versie 10.0.30 van apps voor financiën en bedrijfsactiviteiten](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van versie 10.0.30, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022](/dynamics365-release-plan/2022wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-features"></a>Verwijderde en afgeschafte functies

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) worden functies beschreven die zijn verwijderd of afgeschaft voor Commerce.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Commerce](removed-deprecated-features-commerce.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
