---
title: Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service
description: In dit artikel worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8b86b6a59344299a7a2d277543c3186ed2b8cee4
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103228"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a>Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service

[!include[banner](../includes/banner.md)]



In dit artikel worden de sjablonen en onderliggende taken besproken die worden gebruikt om magazijnen van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service.](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van magazijnen vanuit Supply Chain Management naar Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Magazijnen (Supply Chain Management naar Field Service)

**Taak in het project Gegevensintegratie**
- Magazijn

## <a name="table-set"></a>Tabelset
| Field Service    | Supply Chain Management                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Magazijnen                             |

## <a name="table-flow"></a>Tabelstroom
Magazijnen die worden gemaakt en beheerd in Supply Chain Management, kunnen worden gesynchroniseerd met Field Service via een Microsoft Dataverse-gegevensintegratieproject (CDS). Met de functie voor geavanceerde query's en projectfilters kunnen de magazijnen die u wilt synchroniseren met Field Service worden beheerd. Magazijnen die vanuit Supply Chain Management worden gesynchroniseerd, worden gemaakt in Field Service met de kolom **Wordt extern beheerd** ingesteld op **Ja** en de record ingesteld op alleen-lezen.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
Ter ondersteuning van de integratie tussen Field Service en Supply Chain Management is extra functionaliteit nodig in de CRM-oplossing Field Service. In de oplossing is de kolom **Wordt extern beheerd** toegevoegd aan de tabel **Magazijn (msdyn_warehouses)**. Op basis van deze kolom kunt u zien of het magazijn wordt beheerd vanuit Supply Chain Management of dat het alleen bestaat in Field Service. De instellingen voor deze kolom zijn:
- **Ja** – het product is afkomstig uit Supply Chain Management en kan niet worden bewerkt in Sales.
- **Nee**: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.

Gebruik de kolom **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren. Alleen magazijnen met **Wordt extern beheerd** = **Ja** kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem. 

> [!NOTE]
> Het is mogelijk om meerdere magazijnen in Field Service te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn, met de functies voor geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates naar Supply Chain Management verzendt. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Supply Chain Management. Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="data-integration-project"></a>Gegevensintegratieproject
Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Supply Chain Management worden overgebracht naar Field Service. Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.  

Om te controleren of de **Integratiesleutel** aanwezig is voor **msdyn_warehouses**:
1. Ga naar Gegevensintegratie.
2. Selecteer het tabblad **Verbindingsset**.
3. Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werkorders.
4. Selecteer het tabblad **Integratiesleutel**.
5. Zoek msdyn_warehouses en bevestig dat de sleutel **msdyn_name (naam)** is toegevoegd. Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeelding ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a>Magazijnen (Supply Chain Management naar Field Service): Warehouse

[![Sjabloontoewijzing in Gegevensintegratie.](./media/Warehouse1.png)](./media/Warehouse1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
