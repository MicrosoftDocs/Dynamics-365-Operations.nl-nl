---
title: Projectcontracten en projecten rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations
description: In dit onderwerp worden de sjabloon en de onderliggende taken besproken die worden gebruikt om projectcontracten en projecten rechtstreeks van Microsoft Dynamics 365 for Project Service Automation met Microsoft Dynamics 365 for Finance and Operations te synchroniseren.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561457"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projectcontracten en projecten rechtstreeks vanuit Project Service Automation synchroniseren met Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjabloon en de onderliggende taken besproken die worden gebruikt om projectcontracten en projecten rechtstreeks van Microsoft Dynamics 365 for Project Service Automation met Microsoft Dynamics 365 for Finance and Operations te synchroniseren.

> [!NOTE] 
> Als u Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3.0 gebruikt, moet u KB 4074835 installeren.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Gegevensstroom voor Project Service Automation naar Finance and Operations

> [!NOTE]
> Voordat u de oplossing Project Service Automation-integratie met Finance and Operations kunt gebruiken, moet u bekend zijn met de functie Gegevensintegratie van Microsoft Dynamics 365.

De oplossing Project Service Automation-integratie met Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjabloon die beschikbaar is met de functie voor gegevensintegratie maakt de stroom van projectuurcontracten, projecten, projectcontractregels en projectcontractregelmijlpalen van Project Service Automation naar Finance and Operations mogelijk.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Sjablonen en taken

Selecteer voor toegang tot de beschikbare sjablonen in het Microsoft PowerApps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projectcontracten en projecten vanuit Project Service Automation naar Finance and Operations:

- **Naam van de sjabloon in Gegevensintegratie:** Projecten en contracten (PSA naar Fin and Ops)
- **Naam van de taken in het project:**

    - Projectcontracten PSA naar Fin and Ops
    - Projecten PSA naar Fin and Ops
    - Projectcontractregels PSA naar Fin and Ops
    - Projectcontractregelmijlpalen PSA naar Fin and Ops

Voordat synchronisatie van projectcontracten en projecten kan optreden, moet u rekeningen synchroniseren.

## <a name="entity-set"></a>Entiteitset

| Project Service Automation       | Finance en Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Orders                           | Integratie-entiteit voor projectcontract                |
| Projecten                         | Integratie-entiteit voor project                         |
| Orderregels                      | Integratie-entiteit voor projectcontractregel           |
| Projectcontractregelmijlpalen | Integratie-entiteit voor mijlpaal voor projectcontractregel |

## <a name="entity-flow"></a>Entiteitstroom

Projectcontracten worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectcontracten. Als onderdeel van de integratiesjabloon kunt u de integratiebron instellen in Finance and Operations voor het projectcontract.

Projecten op basis van tijd en materiaal en projecten met vaste prijs worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projecten. Als onderdeel van de sjabloonintegratie kunt u de integratiebron instellen in Finance and Operations voor het project.

Projectcontractregels worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als projectcontractfactureringsregels. Als de factureringsmethode afwijkt van het standaardprojecttype, werkt de synchronisatie het projecttype voor het contractregelproject en de projectgroep bij.

Projectcontractregelmijlpalen worden beheerd in Project Service Automation en worden gesynchroniseerd naar Finance and Operations als mijlpalen voor projectcontractfactureringsregels.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Oplossing Project Service Automation-integratie naar Finance and Operations

Het veld **Projectcontract ID** is beschikbaar op de pagina **Projectcontracten**. Dit veld is tot een natuurlijke en unieke sleutel gemaakt voor de ondersteuning van de integratie.

Wanneer een nieuw projectcontract wordt gemaakt, als een **Projectcontract-ID**-waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **ORD**, gevolgd door een oplopende nummerreeks en vervolgens een achtervoegsel van zes tekens. Dit is een voorbeeld: **ORD-01022-Z4M9Q0**.

Het veld **Projectnummer** is beschikbaar op de pagina **Projecten**. Dit veld is tot een natuurlijke en unieke sleutel gemaakt voor de ondersteuning van de integratie.

Wanneer een nieuw project wordt gemaakt, als een **Projectnummer**-waarde nog niet bestaat, wordt deze automatisch gegenereerd met behulp van een nummerreeks. De waarde bestaat uit **PRJ**, gevolgd door een oplopende nummerreeks en vervolgens een achtervoegsel van zes tekens. Dit is een voorbeeld: **PRJ-01049-CCNID0**.

Wanneer de oplossing Project Service Automation-integratie naar Finance and Operations wordt toegepast<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, stelt een upgradescript het veld **Projectcontract-ID** in voor bestaande projectcontracten en het veld **Projectnummer** voor bestaande projecten in Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

- Voordat synchronisatie van projectcontracten en projecten kan optreden, moet u rekeningen synchroniseren.
- Voeg in uw verbindingsset een toewijzing van een integratiesleutelveld toe voor **msdyn\_organizationalunits** naar **msdyn\_name \[name\]**. Mogelijk moet u eerst een project toevoegen aan de verbindingsset. Zie voor meer informatie [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- Voeg in uw verbindingsset een toewijzing van een integratiesleutelveld toe voor **msdyn\_projects** naar **msdynce\_projectnumber \[Project Number\]**. Mogelijk moet u eerst een project toevoegen aan de verbindingsset. Zie voor meer informatie [Gegevens integreren in Common Data Service voor Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- **SourceDataID** voor projectcontracten en projecten kan worden bijgewerkt naar een andere waarde of verwijderd uit de toewijzing. De standaardsjabloonwaarde is **Project Service Automation**.
- De toewijzing **Betalingsvoorwaarden** moet worden bijgewerkt zodat deze geldige betalingsvoorwaarden in Finance and Operations reflecteert. U kunt ook de toewijzing uit de projecttaak verwijderen. De standaardwaardetoewijzing heeft standaardwaarden voor demonstratiegegevens. De volgende tabel bevat de waarden in Project Service Automation.

    | Waarde | Omschrijving   |
    |-------|---------------|
    | 1     | Netto 30        |
    | 2     | 2% 10, Net 30 |
    | 3     | Netto 45        |
    | 4     | Netto 60        |

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query voor Excel gebruiken om gegevens te filteren als aan de volgende voorwaarden wordt voldaan:

- U hebt verkooporders in Microsoft Dynamics 365 for Sales.
- U hebt meerdere organisatie-eenheden in Project Service Automation en deze organisatie-eenheden worden toegewezen aan meerdere rechtspersonen in Finance and Operations.

Als u Power Query moet gebruiken, volgt u deze richtlijnen:

- De sjabloon Projecten en contracten (PSA naar Fin and Ops) heeft een standaardfilter dat alleen verkooporders bevat van het type **Werkitem (msdyn\_ordertype = 192350001)**. Dit filter helpt waarborgen dat geen projectcontracten worden gemaakt voor verkooporders in Finance and Operations. Als u uw eigen sjabloon maakt, moet u dit filter toevoegen.
- U moet een Power Query-filter maken dat alleen de contractorganisaties bevat die moeten worden gesynchroniseerd naar de rechtspersoon van de integratieverbindingsset. Projectcontracten die u hebt met de contractorganisatie-eenheid Contoso US moeten bijvoorbeeld worden gesynchroniseerd met de rechtspersoon USSI, maar projectcontracten die u hebt met de contractorganisatie-eenheid Contoso Global moeten worden gesynchroniseerd met de rechtspersoon USMF. Als u dit filter niet aan uw taaktoewijzing toevoegt, worden alle projectcontracten gesynchroniseerd met de rechtspersoon die is gedefinieerd voor de verbindingsset, ongeacht de organisatie-eenheid van het contract.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

> [!NOTE] 
> De velden **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** en **AddressZipCode** worden niet opgenomen in de standaardtoewijzing voor projectcontracten. U kunt de toewijzingen toevoegen als u nodig hebt dat deze gegevens worden gesynchroniseerd voor projectcontracten.
>
> De velden **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** en **ProjectType** worden niet opgenomen in de standaardtoewijzing voor projecten. U kunt de toewijzingen toevoegen als u nodig hebt dat deze gegevens worden gesynchroniseerd voor projecten.

In de volgende afbeeldingen ziet u voorbeelden van de sjabloontaaktoewijzingen in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Sjabloontoewijzing](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Sjabloontoewijzing](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Sjabloontoewijzing](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)
