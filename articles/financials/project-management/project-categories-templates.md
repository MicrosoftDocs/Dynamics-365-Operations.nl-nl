---
title: "Projectonkostencategorieën vanuit Project Service Automation synchroniseren"
description: "In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën te synchroniseren tussen Microsoft Dynamics 365 for Project Service Automation en Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren

In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën te synchroniseren tussen Microsoft Dynamics 365 for Project Service Automation en Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Gegevensstroom voor Project Service Automation en Finance and Operations

De integratieoplossing voor Project Service Automation en Finance and Operations gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance and Operations. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over categorieën projectonkostentransacties tussen Project Service Automation en Finance and Operations mogelijk.

Als de projectonkostencategorieën worden gemaakt in Finance and Operations, is de stroom van de integratie van Finance and Operations naar Project Service Automation en vervolgens worden de integratie-ID's van projectonkostencategorieën bijgewerkt doordat wordt gesynchroniseerd van Project Service Automation naar Finance and Operations.

Als de projectonkostencategorieën worden gemaakt in Project Service Automation, is de stroom van de integratie eerst van Project Service Automation naar Finance and Operations. De projectcategorieën moeten in Finance and Operations zijn geconfigureerd al vóór de synchronisatie van Project Service Automation. Synchroniseer vervolgens van Finance and Operations terug naar Project Service Automation en vervolgens van Project Service Automation naar Finance and Operations. Hierdoor worden de categorieën gekoppeld en worden geen duplicaten gemaakt.

> [!NOTE]
> Meestal worden de projectonkostencategorieën gemaakt in Finance and Operations. Als dat niet uw situatie is of als u al onkostencategorieën hebt gemaakt in Project Service Automation, moet u eerst synchroniseren met behulp van de categorieën projectonkostentransacties (PSA naar Fin and Ops) en vervolgens synchroniseren met categorieën projectonkostentransacties (Fin and Ops naar PSA). Vervolgens voert u de synchronisatie nog een keer uit van PSA naar Fin and Ops.

> Als u eerst synchroniseert vanuit Project Service Automation, moeten de projectcategorieën al zijn ingesteld in Finance and Operations en moeten alle projectcategorieën die moeten worden gesynchroniseerd met de Project Service Automation-transactiecategorieën, zijn ingesteld als **Actief in journalen**.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance and Operations.

[![Gegevensstroom voor Project Service Automation-integratie met Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Sjablonen en taken

Selecteer voor toegang tot beschikbare sjablonen in het Microsoft PowerApps Beheercentrum **Projecten** en selecteer vervolgens in de rechterbovenhoek **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Finance and Operations naar Project Service Automation:

-  **Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (Fin and Ops naar PSA)
-  **Naam van de taak in het project:** Categorieën synchroniseren naar PSA

## <a name="entity-set"></a>Entiteitset

| Finance en Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Integratie-entiteit voor categorieën    | Transactiecategorieën        |

## <a name="entity-flow"></a>Entiteitstroom

Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.

## <a name="power-query"></a>Power Query

U moet Microsoft Power Query gebruiken om het type facturering in te stellen voor de transactiecategorie wanneer u synchroniseert naar Project Service Automation. De sjabloon Categorieën projectkostentransacties (Fin and Ops naar PSA) heeft al een standaardkolom en -toewijzing. Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query.
- Open het formulier Geavanceerde filtering en query vanuit de toewijzing van de projectkostencategorieëntaak.
- Selecteer **Voorwaardelijke kolom toevoegen**.
- Geef de nieuwe kolom een naam, zoals Factureringstype.
- Voer de volgende voorwaarde: als **CATEGORYID niet gelijk aan null dan 19235001, anders null**.
- Klik op **OK** in de kolom.
- Zorg ervoor dat deze nieuwe kolom wordt toegewezen op de toewijzingspagina.

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance and Operations naar Project Service Automation worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Project Service Automation naar Finance and Operations:

-**Naam van de sjabloon in gegevensintegratie:** Categorieën projectkostentransacties (PSA naar Fin and Ops) -**Naam van de taak in het project:** Categorieën synchroniseren naar Fin Ops

## <a name="entity-set"></a>Entiteitset

| Project Service Automation      | Finance en Operations             |
|---------------------------------|------------------------------------|
| Transactiecategorieën          | Integratie-entiteit voor categorieën  | 

## <a name="entity-flow"></a>Entiteitstroom

Projectkostencategorieën worden beheerd in Finance and Operations en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën. De synchronisatie terug naar Finance and Operations werkt de integratie-id bij vanuit Project Service Automation in de Finance and Operations-projectcategorie.

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance and Operations worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

