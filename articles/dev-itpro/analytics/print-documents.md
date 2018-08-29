---
title: Documenten afdrukken
description: In Microsoft Dynamics 365 for Finance and Operations kunt u documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5d52568ce49b85f6215ed2835a95e2e016c9c879
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="document-printing"></a>Documenten afdrukken

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics 365 for Finance and Operations kunt u documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. In dit artikel vindt u een overzicht van hoe documenten worden afgedrukt.

<a name="printing-overview"></a>Afdrukoverzicht
-----------------

Microsoft Dynamics 365 for Finance and Operations biedt geïntegreerde services en clienttoepassingen waarmee u eenvoudig documenten kunt genereren, opslaan en distribueren die de bedrijfsactiviteiten ondersteunen. In Finance and Operations kunt u documenten afdrukken met behulp van een lokale printer of een netwerkapparaat. U kunt bovendien de pagina's en rapporten van Finance and Operations rechtstreeks exporteren vanaf de client als PDF-bestanden of Microsoft Office-documenten. Ten slotte zorgt de gedistribueerde werkbelasting dat bedrijfsdocumenten rechtstreeks kunt afdrukken vanaf een mobiel apparaat met behulp van netwerkbronnen. Ook al variëren de afdrukeisen, in alle bedrijfstakken zijn gewoonlijk papieren exemplaren nodig van zakelijke documenten via Finance and Operations. Het afdrukken van documenten op netwerkapparaten via gehoste toepassingen vormt een unieke uitdaging. Hieronder vindt u enkele voorbeelden:

-   Printerstuurprogramma's zijn mogelijk niet beschikbaar op het apparaat van de gebruiker.
-   het apparaat van de gebruiker kan niet worden verbonden met het bedrijfsnetwerk.

Door het toewijzen van een host en het uitvoeren van een paar eenvoudige stappen kunnen systeembeheerders implementaties configureren zodat gebruikers rechtstreeks vanuit bedrijfstoepassingen op netwerkapparaten kunnen afdrukken.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Afdrukscenario's in toepassingen van Finance and Operations

In de volgende tabel worden de drie primaire afdrukscenario's beschreven in toepassingen van Finance and Operations.

| Scenario's                        | Doel                                                      | Oplossing                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| 1. Afdrukken wat u ziet        | De huidige inhoud van de browser afdrukken.             | Een afdrukversie van de webpagina wordt gegenereerd voor de browser.                                             |
| 2. interactief afdrukken         | Een precisiedocument afdrukken op een lokaal aangesloten apparaat. | U kunt een PDF-versie van het rapport exporteren en deze downloaden naar de browser.                                          |
| 3. Afdrukken op een netwerkapparaat | Een precisiedocument verzenden naar een printer voor het domein.     | Een precisiedocument wordt verzonden naar een clienttoepassing die wordt uitgevoerd op een server die wordt gehost in een domein van de klant. |

Omdat de oplossing afhankelijk van het scenario verschilt, bevatten toepassingen van Finance and Operations geïntegreerde services en functies waarmee gebruikers hun doelen kunnen bereiken:

-   **Scenario 1** wordt ondersteund door de weergave in de browser van de HTML5-client.
-   **Scenario 2** maakt gebruik van clienttoepassingen en services van Microsoft Office 365.
-   **Scenario 3** vereist ondersteuning van clienttoepassingen en services die worden gehost in Microsoft Azure.

Naast het platform dat in het Azure-abonnement is geïmplementeerd, bevatten Finance and Operations-toepassingen een geïntegreerde, directe Azure-toepassing waarmee ze makkelijker in het domein gehoste apparaten kunnen gebruiken om documenten af te drukken.

## <a name="service-overview"></a>Serviceoverzicht
Documenten die worden geproduceerd door de gehoste toepassingen en die wachten om te worden afgedrukt op een netwerkapparaat, worden opgeslagen in de Azure-blobopslag. De [Documentrouteringsagent](install-document-routing-agent.md) gebruikt Azure-verificatie om een beveiligde verbinding met de Azure-services tot stand te brengen. **Uitvoeringsreeks**

1.  Het rapport wordt gegenereerd door Microsoft SQL Server Reporting Services (SSRS) en opgeslagen in Azure-blobopslag. Gekoppelde printerinstellingen worden samen met het document opgeslagen.
2.  De Documentrouteringsagent voert een query uit in de Azure Service Bus-wachtrij voor actieve taken.
3.  Het document wordt gedownload door de Documentrouteringsagent en in de netwerkprinterwachtrij geplaatst.

Met de clientoplossing kunnen klanten hun afdrukeisen naar wens beheren. Klanten met een groot volume afdruktaken kunnen veel Documentrouteringsagenten installeren om het aantal gelijktijdige afdrukbewerkingen te vergroten. Andere klanten vereisen mogelijk slechts een paar Documentrouteringsagenten voor het verwerken van hun verwachte afdrukbehoefte.

### <a name="service-components-for-network-printing"></a>Serviceonderdelen voor netwerkafdrukken

Het volgende diagram toont de basisonderdelen voor het ondersteunen van netwerkafdrukfuncties. [![Service-onderdelen-voor-afdrukken via een netwerk\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Houd er rekening mee dat één printer met meerdere documentrouteringagenten kan worden geregistreerd. Om te voldoen aan de printervoorkeuren gebruikt de gehoste service het netwerkpad dat een unieke identificatie is voor elke netwerkprinter. Hierdoor wordt zelfs een printer die door meerdere clients is geregistreerd, als één selectie weergegeven in de lijst met printers die beschikbaar zijn in toepassingen van Finance and Operations.




