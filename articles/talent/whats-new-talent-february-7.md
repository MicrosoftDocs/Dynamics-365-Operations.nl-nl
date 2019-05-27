---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (7 februari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b89fc15130755a80b56f26cf7c61674a26f43e36
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517682"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (7 februari 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="interview-scheduling-enhancements"></a>Verbeteringen voor het plannen van sollicitatiegesprekken
Er zijn verbeteringen aangebracht in de planning van end-to-end sollicitatiegesprekken. U kunt nu de beschikbaarheid van de kalender van een interne kandidaat zien en deze kalender voor planningsaanbevelingen gebruiken. Zie voor meer informatie [Plannen van sollicitatiegesprekken en feedback](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Publicatie van vacatures naar LinkedIn: probleem met verkeerde bedrijfsnaam is opgelost
Het probleem is opgelost waarbij vacatures die worden gepubliceerd naar LinkedIn vanuit Attract, onder de verkeerde bedrijfsnaam worden weergegeven. Zie voor meer informatie [Vacatures maken, goedkeuren en publiceren in Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>De URL van de vacaturesite weergegeven in Beheerinstellingen
De startpagina-URL van de vacaturesite wordt nu weergegeven in **Beheerinstellingen** onder **Beheer van vacaturesite**.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

**Build 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Meerdere compensatieniveaus ondersteund voor functies
Dankzij deze wijziging kunnen meerdere compensatieniveaus worden gedefinieerd voor een functie, waardoor bereiken mogelijk zijn van vaste compensaties voor werknemers die tussen plannen kunnen verschillen wanneer dezelfde functie wordt gebruikt. 

Bijvoorbeeld:    
*Functie* - Accountmanager *Gekoppelde compensatieniveaus:* B1 en B2 - elk niveau heeft een gedefinieerd bereik van waarden. B1 = min. 50.000, midden 60.000, max. 75.000 en B2 = min. 65.000, midden 74.000, max. 85.000. Bij het maken van vaste compensaties voor werknemers op basis van de gedefinieerde geschiktheidsregels kan elk vast plan nu verwijzen naar dezelfde functie en naar verschillende niveaus voor de functie. Zo kunnen plannen worden gedefinieerd in verschillende regio's/bedrijven en verwijzen naar dezelfde functie, maar verschillende bereiken zonder functies te dupliceren voor deze verschillen.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Het veld Compensatieniveau is toegevoegd aan de entiteit Vaste compensatie voor werknemer 
Met deze update wordt de entiteit Vaste compensatie voor werknemer bijgewerkt om het veld **Compensatieniveau** op te nemen. Door deze toevoeging kunnen vaste compensatieplannen voor werknemers gemakkelijker worden bijgewerkt. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Functiegroep bijwerken bij het bijwerken en maken van nieuwe posities
Bij het wijzigen van de functie voor een positie wordt **Functiegroep** nu standaard ingesteld op basis van de geselecteerde functie.

### <a name="performance-improvements-when-rendering-workspaces"></a>Betere prestaties bij het weergeven van werkgebieden
Analysetabbladen in werkgebieden worden voortaan alleen geladen wanneer toegang wordt verkregen tot deze pagina's. Een indicator wordt weergegeven tijdens de eerste weergave van de pagina in de linkerbovenhoek van de pagina.
