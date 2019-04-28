---
title: Magazijnen vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Microsoft Dynamics 365 for Finance and Operations te synchroniseren met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/14/2019
ms.locfileid: "842528"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Magazijnen van Finance and Operations synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Microsoft Dynamics 365 for Finance and Operations te synchroniseren met Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt om magazijnen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Magazijnen (Fin and Ops naar Field Service)

**Taak in het project Gegevensintegratie**
- Magazijn

## <a name="entity-set"></a>Entiteitset
| Field Service    | Finance en Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Magazijnen                             |

## <a name="entity-flow"></a>Entiteitstroom
Magazijnen die worden gemaakt en beheerd in Finance and Operations kunnen worden gesynchroniseerd met Field Service via een Common Data Service-gegevensintegratieproject (CDS). Met de functie voor geavanceerde query's en projectfilters kunnen de magazijnen die u wilt synchroniseren met Field Service worden beheerd. Magazijnen die vanuit Finance and Operations kunnen worden gesynchroniseerd, worden gemaakt in Field Service met het veld **Wordt extern onderhouden** ingesteld op **Ja** en de record ingesteld op alleen-lezen.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
Ter ondersteuning van de integratie tussen Field Service en Finance and Operations is extra functionaliteit nodig in de CRM-oplossing Field Service. In de oplossing is het veld **Wordt extern beheerd** toegevoegd aan de entiteit **Magazijn (msdyn_warehouses)**. Op basis van dit veld kunt u zien of het magazijn wordt beheerd vanuit Finance and Operations of dat het alleen bestaat in Field Service. De instellingen voor deze velden zijn:
- **Ja**: het magazijn is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.
- **Nee**: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.

Gebruik het veld **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren. Alleen magazijnen met **Wordt extern beheerd** = **Ja** kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem. 

> [!NOTE]
> Het is mogelijk om meerdere magazijnen in Field Service te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations. Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="data-integration-project"></a>Gegevensintegratieproject
Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Finance and Operations worden overgebracht naar Field Service. Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.  

Om te controleren of de **Integratiesleutel** aanwezig is voor **msdyn_warehouses**:
1. Ga naar Gegevensintegratie.
2. Selecteer het tabblad **Verbindingsset**.
3. Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werkorders.
4. Selecteer het tabblad **Integratiesleutel**.
5. Zoek msdyn_warehouses en bevestig dat de sleutel **msdyn_name (naam)** is toegevoegd. Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>Magazijnen (Fin and Ops naar Field Service): Magazijn

[![Sjabloontoewijzing in Gegevensintegratie](./media/Warehouse1.png)](./media/Warehouse1.png)
