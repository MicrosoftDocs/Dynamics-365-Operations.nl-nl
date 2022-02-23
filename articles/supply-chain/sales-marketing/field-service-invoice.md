---
title: Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Supply Chain Management
description: Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van overeenkomstfacturen in Dynamics 365 Field Service voor vrije-tekstfacturen in Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c2d0f671d4b824cb5d38a5d11c4b06b2e97bd0c8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528240"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bespreekt de sjablonen en onderliggende taken die worden gebruikt voor het synchroniseren van facturen in Dynamics 365 Field Service voor vrije-tekstfacturen in Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Sjablonen en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van overeenkomstfacturen in Field Service met vrije-tekstfacturen in Supply Chain Management.

**Naam van de sjabloon in Gegevensintegratie**

- Overeenkomstfacturen (Field Service naar Supply Chain Management)

**Namen van de taken in het project Gegevensintegratie**

- Factuurkopteksten
- Factuurregels

De volgende synchronisatietaak is vereist voordat de synchronisatie van de overeenkomstfacturen kan plaatsvinden:

- Accounts (Sales naar Supply Chain Management) - Direct

## <a name="entity-set"></a>Entiteitset

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| facturen       | Kopteksten voor vrije-tekstfacturen van CDS-klanten |
| factuurdetails | Regels voor vrije-tekstfacturen van CDS-klanten   |

## <a name="entity-flow"></a>Entiteitstroom

Facturen die zijn gemaakt op basis van een overeenkomst in Field Service kunnen worden gesynchroniseerd met Supply Chain Management via een Common Data Service-gegevensintegratieproject. Updates voor deze facturen worden gesynchroniseerd met de vrije-tekstfacturen in Supply Chain Management als de boekhoudstatus van de vrije-tekstfacturen **Onderhanden** is. Nadat de vrije-tekstfacturen zijn geboekt in Supply Chain Management en de boekhoudstatus is bijgewerkt naar **Voltooid**, kunt u de updates van Field Service niet meer synchroniseren.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing

Het veld **Heeft regels met oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuur**. Dit veld zorgt ervoor dat alleen facturen die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd. De waarde is **true** als de factuur ten minste één factuurregel bevat die afkomstig is van een overeenkomst.

Het veld **Heeft oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuurregel**. Dit veld zorgt ervoor dat alleen factuurregels die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd. De waarde **true** als de factuurregel afkomstig is uit een overeenkomst.

**Factuurdatum** is een verplicht veld in Supply Chain Management. Het veld moet daarom een waarde in Field Service hebben voordat de synchronisatie wordt uitgevoerd. Om te voldoen aan deze vereiste wordt de volgende logica toegevoegd:

- Als het veld **Factuurdatum** leeg is op de entiteit **Factuur** (dat wil zeggen er is geen waarde), wordt deze ingesteld op de huidige datum wanneer een factuurregel afkomstig uit een overeenkomst wordt toegevoegd.
- De gebruiker kan het veld **Factuurdatum** wijzigen. Wanneer de gebruiker een factuur wil opslaan die afkomstig is uit een overeenkomst, verschijnt een bedrijfsprocesfout als het veld **Factuurdatum** leeg is op de factuur.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="in-supply-chain-management"></a>In Supply Chain Management

De oorsprong van een factuur moet worden ingesteld voor de integratie om vrije-tekstfacturen te herkennen in Supply Chain Management die zijn gemaakt op basis van overeenkomstfacturen in Field Service. Wanneer een factuur een factuuroorsprong heeft van het type **Factuurintegratie van overeenkomst**, wordt het veld **Extern factuurnummer** weergegeven in de koptekst van de **verkoopfactuur**.

Behalve op de factuurkop worden de gegevens van het **Externe factuurnummer** gebruikt om te garanderen dat facturen die zijn gemaakt op basis van Field Service-overeenkomstfacturen, eruit worden gefilterd tijdens de factuursynchronisatie tussen Supply Chain Management en Field Service.

1. Ga naar **Klanten** \> **Instellen** \> **Oorsprongcodes voor factuur**.
2. Selecteer **Nieuw** om een nieuwe factuuroorsprong te maken.
3. Voer in het veld **Factuuroorsprong** een naam in voor de factuuroorsprong, zoals **FS**.
4. Voer in het veld **Omschrijving** een omschrijving in zoals **Field Service-overeenkomstfactuur**.
5. Schakel het selectievakje **Toewijzing van oorsprongtype** in.
6. Stel het veld **Type factuuroorsprong** in op **Factuurintegratie van overeenkomst**.
7. Selecteer **Opslaan**.

### <a name="in-the-data-integration-project"></a>In het project Gegevensintegratie

Taak: **Factuurregels**  

Zorg dat de standaardwaarde voor het veld **Weergegeven waarde hoofdrekening** in Supply Chain Management wordt bijgewerkt naar de gewenste waarde.

De standaardsjabloonwaarde is **401100**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Overeenkomstfacturen (Field Service naar Supply Chain Management): Factuurkopteksten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Overeenkomstfacturen (Field Service naar Supply Chain Management): Factuurregels

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
