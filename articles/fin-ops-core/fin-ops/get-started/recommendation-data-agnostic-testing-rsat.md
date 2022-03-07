---
title: Gegevensagnostisch testen met de Regression Suite Automation Tool
description: In dit onderwerp worden de aanbevelingen besproken voor gegevensagnostisch testen met behulp van de Regression Suite Automation Tool.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d9a5bce1cc56dfdf66b2ce58c2e740b7c4b3bdfc7f4e75396fe5dc7cb931b6d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763405"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Gegevensagnostisch testen met de Regression Suite Automation Tool

[!include [banner](../includes/banner.md)]

Hoewel de functionele validatie van een ERP-toepassing niet volledig gegevensagnostisch kan zijn, zijn er meerdere fasen en benaderingen voor het testen. Deze testfasen zijn onder andere:  

- SysTest kader
- ATL kader
- Regression Suite Automation Tool (RSAT)

[![Piramide met testclassificatie.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Overzicht
-   **SysTest-kader** – het SysTest-kader is betrouwbaar voor het schrijven van tests. Aangezien de eenheidstesten in het algemeen een methode of functie testen, moeten deze altijd gegevensagnostisch zijn en alleen afhankelijk van de invoergegevens die als onderdeel van de test worden geleverd.
-   **ATL-kader** – Microsoft heeft een ATL-kader dat een abstracte structuur is op het SysTest-kader en het werken met tests veel eenvoudiger en betrouwbaarder maakt. Dit kader moet worden gebruikt voor het schrijven van onderdeeltests of eenvoudige integratietests.
-   **RSAT** – de RSAT wordt gebruikt voor integratietests en bedrijfscyclustests. De bedrijfscyclustests, ook wel regressievalidatietests genoemd, zijn afhankelijk van bestaande gegevens. Deze tests kunnen echter gegevensagnostisch worden als u extra factoren in acht neemt. 

    - o Waar eenheidstests en onderdeeltests van laag niveau zijn en volledig gegevensagnostisch kunnen zijn (niet afhankelijk van bestaande gegevenssets), zijn de bedrijfscyclus- of regressievalidatietests afhankelijk van enkele bestaande gegevens. Deze gegevens omvatten instellingen, configuratie-instellingen (parameters) en hoofdgegevens (klant, leveranciers, artikelen, enzovoort), maar nooit transactiegegevens. Zorg ervoor dat tijdens de test een of meer van deze wijzigingen worden teruggedraaid als onderdeel van de eindtest.
    - Selecteer hoofdgegevens op basis van bepaalde criteria in plaats van een bepaalde record te selecteren. Als u bijvoorbeeld een artikel wilt selecteren op basis van de dimensiewaarden en de voorraadbeschikbaarheid, filtert u de productlijst met deze waarden, selecteert u het eerste artikel en kopieert u het nummer dat u wilt gebruiken voor toekomstige tests. Als het een eenvoudige hoofdgegevens-regel is, zoals klant, leverancier of artikel, kan deze worden gemaakt als onderdeel van de automatisering en in toekomstige tests worden gebruikt via kettingen. 
    - o Geef de unieke id's, zoals factuurnummers, op via de nummer reeks of met behulp Microsoft Excel-functies zoals =TEXT(NOW(),"yyyymmddhhmm"). Deze functie geeft elke minuut een uniek nummer, waarmee u kunt bijhouden wanneer de actie heeft plaatsgevonden. Deze kan worden gebruikt voor variabelen zoals productontvangstbonnen en factuurnummers van leveranciers. Deze tests blijven opnieuw en in dezelfde database werken, zonder dat er een herstelbewerking hoeft worden uitgevoerd.
    - Steld de **Bewerkingsmodus** van de omgeving altijd in op **Lezen** of **Bewerken** als eerste testaanvraag, omdat de standaardoptie **Automatisch** is. De **Automatische**-opties gebruiken altijd de vorige instelling en kunnen onbetrouwbare tests tot gevolg hebben. 
 
    [![Pagina Opties, tabblad Prestaties.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Valideer alleen nadat u op een bepaalde transactie hebt gefilterd in plaats van algemene validatie. Filter bijvoorbeeld voor het aantal records op het transactienummer of de transactiedatum, zodat alle overige transacties worden uitgesloten. 
    - Als u een klantsaldo of een budgetcontrole controleert, slaat u eerst de waarde op en voegt u vervolgens uw transactiewaarde toe om het verwachte resultaat te valideren, in plaats van een vaste verwachte waarde te valideren. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]