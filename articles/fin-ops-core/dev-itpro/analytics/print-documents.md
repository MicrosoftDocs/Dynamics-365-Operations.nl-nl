---
title: Overzicht van Documenten afdrukken
description: U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.
author: RichdiMSFT
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.custom:
- "69161"
- intro-internal
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b9105ef39e411ac33043f1941d4e1dd32b758e5
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984903"
---
# <a name="document-printing-overview"></a>Overzicht van Documenten afdrukken

[!include [banner](../includes/banner.md)]

U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.

## <a name="printing-overview"></a>Afdrukoverzicht

De toepassing biedt geïntegreerde services en clienttoepassingen die het gemakkelijk maken om documenten die bedrijfsactiviteit ondersteunen, te genereren, op te slaan en te distribueren. U kunt documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. U kunt bovendien de pagina's en rapporten rechtstreeks exporteren vanaf de client als PDF-bestanden of Microsoft Office-documenten. Ten slotte zorgt de gedistribueerde werkbelasting dat bedrijfsdocumenten rechtstreeks kunt afdrukken vanaf een mobiel apparaat met behulp van netwerkbronnen. Ook al variëren de afdrukeisen, in alle bedrijfstakken zijn gewoonlijk papieren exemplaren nodig van zakelijke documenten via de toepassing. Het afdrukken van documenten op netwerkapparaten via gehoste toepassingen vormt een unieke uitdaging. Hieronder vindt u enkele voorbeelden:

- Printerstuurprogramma's zijn mogelijk niet beschikbaar op het apparaat van de gebruiker.
- Het apparaat van de gebruiker kan niet worden verbonden met het bedrijfsnetwerk.

Door het toewijzen van een host en het uitvoeren van een paar eenvoudige stappen kunnen systeembeheerders implementaties configureren zodat gebruikers rechtstreeks vanuit bedrijfstoepassingen op netwerkapparaten kunnen afdrukken.

### <a name="application-printing-scenarios"></a>Afdrukscenario's voor toepassingen 

In de volgende tabel worden de drie primaire afdrukscenario's beschreven.

| Scenario                        | Doelstelling                                                      | Oplossing |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Afdrukken wat u ziet        | De huidige inhoud van de browser afdrukken.             | Een afdrukversie van de webpagina wordt gegenereerd voor de browser. |
| 2. interactief afdrukken         | Een precisiedocument afdrukken op een lokaal aangesloten apparaat. | U kunt een PDF-versie van het rapport exporteren en deze downloaden naar de browser. |
| 3. Afdrukken op een netwerkapparaat | Een precisiedocument verzenden naar een printer voor het domein.     | Een precisiedocument wordt verzonden naar een clienttoepassing die wordt uitgevoerd op een server die wordt gehost in een domein van de klant. |

Omdat de oplossing afhankelijk van het scenario verschilt, bevatten toepassingen van Finance geïntegreerde services en functies waarmee gebruikers hun doelen kunnen bereiken:

- **Scenario 1** wordt ondersteund door de weergave in de browser van de HTML5-client.
- **Scenario 2** maakt gebruik van clienttoepassingen en services van Microsoft 365.
- **Scenario 3** vereist ondersteuning van clienttoepassingen en services die worden gehost in Microsoft Azure.

Naast het platform dat in het Azure-abonnement is geïmplementeerd, bevatten Finance and Operations-toepassingen een geïntegreerde, directe Azure-toepassing waarmee ze makkelijker in het domein gehoste apparaten kunnen gebruiken om documenten af te drukken.

## <a name="service-overview"></a>Serviceoverzicht
Documenten die worden geproduceerd door de gehoste toepassingen en die wachten om te worden afgedrukt op een netwerkapparaat, worden opgeslagen in de Azure-blobopslag. [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](install-document-routing-agent.md) gebruikt Azure-verificatie om een beveiligde verbinding met de Azure-services tot stand te brengen.

**Uitvoeringsreeks**

1. Het rapport wordt gegenereerd door Microsoft SQL Server Reporting Services (SSRS) en opgeslagen in Azure-blobopslag. Gekoppelde printerinstellingen worden samen met het document opgeslagen.
2. De Documentrouteringsagent voert een query uit in de Azure Service Bus-wachtrij voor actieve taken.
3. Het document wordt gedownload door de Documentrouteringsagent en in de netwerkprinterwachtrij geplaatst.

Met de clientoplossing kunnen klanten hun afdrukeisen naar wens beheren. Klanten met een groot volume afdruktaken kunnen veel Documentrouteringsagenten installeren om het aantal gelijktijdige afdrukbewerkingen te vergroten. Andere klanten vereisen mogelijk slechts een paar Documentrouteringsagenten voor het verwerken van hun verwachte afdrukbehoefte.

### <a name="service-components-for-network-printing"></a>Serviceonderdelen voor netwerkafdrukken

Het volgende diagram toont de basisonderdelen voor het ondersteunen van netwerkafdrukfuncties.

[![service-components-for-network-printing\_2016.](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Houd er rekening mee dat één printer kan worden geregistreerd met meerdere documentrouteringsagents. Om te voldoen aan de printervoorkeuren gebruikt de gehoste service het netwerkpad dat een unieke identificatie is voor elke netwerkprinter. Hierdoor wordt zelfs een printer die door meerdere clients is geregistreerd, als één selectie weergegeven in de lijst met printers die beschikbaar zijn in toepassingen van Finance.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]