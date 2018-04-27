---
title: Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van overeenkomstfacturen in Microsoft Dynamics 365 for Field Service met vrije-tekstfacturen in Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: nl-nl
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van overeenkomstfacturen in Microsoft Dynamics 365 for Field Service met vrije-tekstfacturen in Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Sjablonen en taken

De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van overeenkomstfacturen in Field Service met vrije-tekstfacturen in Finance and Operations.

**Naam van de sjabloon in Gegevensintegratie:**

- Overeenkomstfacturen (Field Service met Finance and Operations)

**Namen van de taken in het project Gegevensintegratie:**

- Factuurkopteksten
- Factuurregels

De volgende synchronisatietaak is vereist voordat de synchronisatie van de overeenkomstfacturen kan plaatsvinden:

- Rekeningen (Sales naar Fin and Ops) - Direct

## <a name="entity-set"></a>Entiteitset

| Field Service  | Finance en Operations                 |
|----------------|----------------------------------------|
| facturen       | Kopteksten voor vrije-tekstfacturen van CDS-klanten |
| factuurdetails | Regels voor vrije-tekstfacturen van CDS-klanten   |

## <a name="entity-flow"></a>Entiteitstroom

Facturen die zijn gemaakt op basis van een overeenkomst in Field Service kunnen worden gesynchroniseerd met Finance and Operations via een Common Data Service-gegevensintegratieproject (CDS). Updates voor deze facturen worden gesynchroniseerd met de vrije-tekstfacturen in Finance and Operations als de boekhoudstatus van de vrije-tekstfacturen **onderhanden** is. Nadat de vrije-tekstfacturen zijn geboekt in Finance and Operations en de boekhoudstatus is bijgewerkt naar **voltooid**, kunt u de updates van Field Service niet meer synchroniseren.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing

Het veld **Heeft regels met oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuur**. Dit veld zorgt ervoor dat alleen facturen die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd. De waarde is **true** als de factuur ten minste één factuurregel bevat die afkomstig is van een overeenkomst.

Het veld **Heeft oorsprong overeenkomst** is toegevoegd aan de entiteit **Factuurregel**. Dit veld zorgt ervoor dat alleen factuurregels die zijn gemaakt op basis van een overeenkomst, worden gesynchroniseerd. De waarde **true** als de factuurregel afkomstig is uit een overeenkomst.

**Factuurdatum** is een verplicht veld in Finance and Operations. Het veld moet daarom een waarde in Field Service hebben voordat de synchronisatie wordt uitgevoerd. Om te voldoen aan deze vereiste wordt de volgende logica toegevoegd:

- Als het veld **Factuurdatum** leeg is op de entiteit **Factuur** (dat wil zeggen er is geen waarde), wordt deze ingesteld op de huidige datum wanneer een factuurregel afkomstig uit een overeenkomst wordt toegevoegd.
- De gebruiker kan het veld **Factuurdatum** wijzigen. Wanneer de gebruiker een factuur wil opslaan die afkomstig is uit een overeenkomst, verschijnt een bedrijfsprocesfout als het veld **Factuurdatum** leeg is op de factuur.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="in-finance-and-operations"></a>In Finance and Operations

De oorsprong van een factuur moet worden ingesteld voor de integratie om vrije-tekstfacturen te herkennen in Finance and Operations die zijn gemaakt op basis van overeenkomstfacturen in Field Service. Wanneer een factuur een factuuroorsprong heeft van het type **Factuurintegratie van overeenkomst**, wordt het veld **Extern factuurnummer** weergegeven in de koptekst van de **verkoopfactuur**.

Behalve op de factuurkop worden de gegvevens van het **externe factuurnummer** gebruikt om te garanderen dat facturen die zijn gemaakt op basis van Field Service-overeenkomstfacturen, eruit worden gefilterd tijdens de factuursynchronisatie tussen Finance and Operations en Field Service.

1. Ga naar **Klanten** \> **Instellen** \> **Oorsprongcodes voor factuur**.
2. Selecteer **Nieuw** om een nieuwe factuuroorsprong te maken.
3. Voer in het veld **Factuuroorsprong** een naam in voor de factuuroorsprong, zoals **FS**.
4. Voer in het veld **Omschrijving** een omschrijving in zoals **Field Service-overeenkomstfactuur**.
5. Schakel het selectievakje **Toewijzing van oorsprongtype** in.
6. Stel het veld **Type factuuroorsprong** in op **Factuurintegratie van overeenkomst**.
7. Selecteer **Opslaan**.

### <a name="in-the-data-integration-project"></a>In het project Gegevensintegratie

Taak: **Factuurregels**  

Zorg dat de standaardwaarde voor het veld **Weergegeven waarde hoofdrekening** in Finance and Operations wordt bijgewerkt naar de gewenste waarde.

De standaardsjabloonwaarde is **401100**.
