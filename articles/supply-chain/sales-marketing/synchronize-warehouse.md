---
title: Magazijnen vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>Magazijnen vanuit Finance and Operations synchroniseren naar Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van magazijnen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

**Naam van de sjabloon in Gegevensintegratie:**
- Magazijnen (Finance and Operations naar Field Service)

**Namen van de taken in het project Gegevensintegratie:**
- Magazijn

## <a name="entity-set"></a>Entiteitset
| Field Service    | Finance en Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | Magazijnen                             |

## <a name="entity-flow"></a>Entiteitstroom
Magazijnen die worden gemaakt en beheerd in Finance and Operations kunnen worden gesynchroniseerd met Field Service via een Common Data Service-gegevensintegratieproject (CDS). Met de functie voor geavanceerde query's en projectfilters kunt u bepalen welke magazijnen worden gesynchroniseerd met Field Service. Magazijnen die vanuit Finance and Operations kunnen worden gesynchroniseerd, worden gemaakt in Field Service met het veld Wordt extern onderhouden ingesteld op Ja en de record ingesteld op alleen-lezen.
Field Service CRM-oplossing Ter ondersteuning van de integratie tussen Field Service en Finance and Operations is extra functionaliteit nodig in de CRM-oplossing Field Service. Het oplossing omvat de volgende wijzigingen.
Het veld **Wordt extern beheerd** is toegevoegd aan de entiteit **Magazijn (msdyn_warehouses)**. Op basis van dit veld kunt u zien of het magazijn wordt beheerd vanuit Operations of dat het alleen bestaat in Field Service.
- Ja: het magazijn is afkomstig uit Finance and Operations en kan niet worden bewerkt in Sales.
- Nee: het magazijn is rechtstreeks ingevoerd in Field Service en wordt hier beheerd.

Gebruik het veld **Wordt extern beheerd** om de synchronisatie van voorraadniveaus, -correcties, -overboekingen en -gebruik voor werkorders te beheren. Alleen magazijnen met **Wordt extern beheerd** = Ja kunnen worden gebruikt voor rechtstreekse synchronisatie met hetzelfde magazijn in het andere systeem. 

Opmerking: het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd** = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations. Zie Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations en Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations voor meer informatie.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="in-the-data-integration-project"></a>In het project Gegevensintegratie
Werk voordat u de magazijnen synchroniseert de functie Geavanceerde query en filtering bij zodat alleen de gewenste magazijnen vanuit Finance and Operations worden overgebracht naar Field Service. Houd er rekening mee dat u het magazijn in Field Service nodig hebt om het toe te passen op werkorders, correcties en overboekingen.  

Controleer of de **integratiesleutel** aanwezig is voor **msdyn_warehouses**
1. Ga naar Gegevensintegratie
2. Selecteer het tabblad **Verbindingsset**
3. Selecteer de verbindingsset die wordt gebruikt voor synchronisatie van werksorders
4. Selecteer het tabblad **Integratiesleutel**
5. Zoek msdyn_warehouses en controleer of de sleutel **msdyn_name (naam)** wordt toegevoegd. Als deze niet wordt weergegeven, voegt u deze toe door te klikken op **Sleutel toevoegen** en klikt u op **Opslaan** bovenaan de pagina

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a>Magazijnen (Finance and Operations naar Field Service): Magazijn

[![Sjabloontoewijzing in Gegevensintegratie](./media/Warehouse1.png)](./media/Warehouse1.png)

