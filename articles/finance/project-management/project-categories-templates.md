---
title: Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren
description: In dit onderwerp worden de sjablonen en onderliggende taken beschreven die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Microsoft Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770307"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projectonkostencategorieën tussen Finance and Operations en Project Service Automation synchroniseren

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om projectonkostencategorieën rechtstreeks tussen Dynamics 365 Finance en Dynamics 365 Project Service Automation te synchroniseren.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is mogelijk in versie 8.0.1 of hoger.
> - Als u Enterprise edition 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Gegevensstroom voor Project Service Automation en Finance

De integratieoplossing voor Project Service Automation en Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Project Service Automation en Finance. De integratiesjablonen die beschikbaar zijn met de functie voor gegevensintegratie maken de stroom van gegevens over categorieën projectonkostentransacties tussen Finance en Project Service Automation mogelijk.

Als de projectonkostencategorieën worden gemaakt in Finance, is de stroom van de integratie eerst van Finance naar Project Service Automation. De integratie-id's van de onkostencategorieën voor projecten worden dan bijgewerkt via synchronisatie vanuit Project Service Automation naar Finance.

Als de projectonkostencategorieën worden gemaakt in Project Service Automation, is de stroom van de integratie eerst van Project Service Automation naar Finance. De projectcategorieën moeten al in Finance zijn geconfigureerd vóór de synchronisatie vanuit Project Service Automation. Synchroniseer vervolgens van Finance terug naar Project Service Automation en vervolgens van Project Service Automation naar Finance. Op deze manier helpt u garanderen dat de categorieën zijn gekoppeld en dat er geen dubbele waarden worden gemaakt.

> [!NOTE]
> Meestal worden de projectonkostencategorieën gemaakt in Finance. Echter, als ze niet worden gemaakt in Finance, of als al onkostencategorieën zijn gemaakt in Project Service Automation, moet u eerst synchroniseren met de Project-sjabloon voor onkostentransactiecategorieën (PSA naar Fin and Ops). Synchroniseer vervolgens via de Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA). Daarna moet u nog één keer de synchronisatie uitvoeren van Project Service Automation naar Finance.
>
> Als u eerst vanuit Project Service Automation synchroniseert, moet aan de volgende vereisten worden voldaan in Finance voordat de synchronisatie wordt uitgevoerd:
>
> - De gedeelde categorie die overeenkomt met de projectcategorie die is ingesteld in Project Service Automation moet bestaan en moet worden ingesteld voor zowel **Project** als **Onkosten**.
> - Voor elke rechtspersoon in Finance waarmee moet volgende geïntegreerd, moeten de volgende projectcategorieën bestaan:
>
>     - **Projectcategorie** bestaat. 
>     - **Gebruiken in Onkosten** is ingeschakeld.
>     - **Actief in journaal** is ingeschakeld.
>     - **Transactietype** is ingesteld op **Onkosten**.

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd tussen Project Service Automation en Finance.

[![Gegevensstroom voor Project Service Automation-integratie met Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronisatie van projectonkostencategorieën van Finance naar Project Service Automation

### <a name="template-and-task"></a>Sjabloon en taak

Selecteer voor toegang tot de sjabloon in het Microsoft Power Apps-beheercentrum de optie **Projecten** en selecteer vervolgens in de rechterbovenhoek de optie **Nieuw project** om openbare sjablonen te selecteren.

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Finance naar Project Service Automation:

- **Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (Fin and Ops naar PSA)
- **Naam van de taak in het project:** Categorieën synchroniseren naar PSA

### <a name="entity-set"></a>Entiteitset

| Financiën                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integratie-entiteit voor categorieën | Transactiecategorieën     |

### <a name="entity-flow"></a>Entiteitstroom

Projectkostencategorieën worden beheerd in Finance en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën.

### <a name="power-query"></a>Power Query

Wanneer u synchroniseert naar Project Service Automation, moet u Microsoft Power Query voor Excel gebruiken om het factureringstype in te stellen voor de transactiecategorie. De Project-sjabloon voor kostentransactiecategorieën (Fin and Ops naar PSA) biedt een standaardkolom en -toewijzing. Als u uw eigen sjabloon maakt, moet u een voorwaardelijke kolom toevoegen in Power Query. Volg deze stappen.

1. Klik op de pijl om de toewijzing te openen van de taak voor projectonkostencategorieën in de Project-sjabloon voor kostentransactiecategorieën (Fin en Ops voor PSA).
2. Klik op de koppeling **Geavanceerde query en filtering** om Power Query te openen.
2. Selecteer **Voorwaardelijke kolom toevoegen**.
3. Voer naam in voor de nieuwe kolom, zoals **Factureringstype**.
4. Voer de volgende voorwaarde in: **als CATEGORYID niet gelijk aan null dan 19235001, anders null**.
5. Klik op **OK** in de kolom.
6. Zorg ervoor dat deze nieuwe kolom wordt toegewezen op de toewijzingspagina.

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie. Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Finance naar Project Service Automation worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronisatie van projectonkostencategorieën van Project Service Automation naar Finance

### <a name="template-and-task"></a>Sjabloon en taak

De volgende sjabloon en onderliggende taak worden gebruikt voor het synchroniseren van projectkostencategorieën vanuit Project Service Automation naar Finance:

- **Naam van de sjabloon in Gegevensintegratie:** Categorieën projectkostentransacties (PSA naar Fin and Ops)
- **Naam van de taak in het project:** Categorieën synchroniseren naar Fin and Ops

### <a name="entity-set"></a>Entiteitset

| Project Service Automation | Financiën                           |
|----------------------------|-----------------------------------|
| Transactiecategorieën     | Integratie-entiteit voor categorieën |

### <a name="entity-flow"></a>Entiteitstroom

Projectkostencategorieën worden beheerd in Finance en worden gesynchroniseerd naar Project Service Automation als transactiecategorieën. De synchronisatie terug naar Finance werkt de projectcategorie in Finance bij met de integratie-id vanuit Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u een voorbeeld van sjabloontaaktoewijzing in Gegevensintegratie.

> [!NOTE]
> Aan de hand van de toewijzing kunt u zien welke veldgegevens vanuit Project Service Automation naar Finance worden gesynchroniseerd.

[![Sjabloontoewijzing](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
