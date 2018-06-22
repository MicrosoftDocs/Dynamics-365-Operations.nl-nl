---
title: Parameters van Project Service Automation-integratie
description: U kunt configureren hoe gegevens standaard moet worden werken bij het integreren van Project Service Automation met Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: nl-nl
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Parameters van Project Service Automation-integratie

Op de pagina **Parameters van Project Service Automation-integratie** kunt u configureren hoe gegevens standaard moeten werken wanneer Project Service Automation wordt geïntegreerd met Finance and Operations. Het volgende moet worden ingesteld voor projecten om met succes te worden gesynchroniseerd vanuit Project Service Automation in Finance and Operations.

> [!NOTE]
> Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling is beschikbaar in Dynamics 365 for Finance and Operations, versie 8.0.




| **Tabblad**                      | **Veld**                          | **Beschrijving**                    |
|------------------------------|------------------------------------|--------------------------------|
| **Algemeen**                  | **Standaardprojecttype**               | Selecteer de standaard voor **Projecttype**, namelijk wanneer projecten worden gesynchroniseerd vanuit Project Service Automation, als u geen standaardwaarde hebt verstrekt in de integratiesjabloon. Tijdens de synchronisatie wordt het **Projecttype** van nieuwe projecten op deze waarde ingesteld en kan het worden bijgewerkt wanneer de projectcontractregels worden gesynchroniseerd vanuit Project Service Automation.               |
| **Algemeen**                  | **Tijdcategorie**                      | Selecteer de standaard voor **Tijdcategorie**, dat is wanneer uurramingen worden gesynchroniseerd vanuit Project Service Automation. Tijdens de synchronisatie krijgen nieuwe projectuurramingen in Finance and Operations de **categorie** ingesteld op deze waarde wanneer de uurramingen en werkelijke uurwaarden worden gesynchroniseerd vanuit Project Service Automation.   |
| **Algemeen**                  | **Categorie bijzondere kosten**                       | Selecteer de standaard voor **Categorie bijzondere kosten**, dat is wanneer werkelijke kosten worden gesynchroniseerd vanuit Project Service Automation. Tijdens de synchronisatie krijgen nieuwe kostentransacties in Finance and Operations de **categorie** ingesteld op deze waarde wanneer de werkelijke kostenwaarden worden gesynchroniseerd vanuit Project Service Automation.          |
| **Standaardinstellingen voor projectgroep**   | **Projecttype** | Klik op **Nieuw** om een rij toe te voegen waarin u het projecttype kunt selecteren waarvoor de standaardprojectgroep moet worden ingesteld. Een bepaald projecttype kan slechts één keer worden geselecteerd in de configuratie.              
|                              | **Projectgroep**          | Selecteer de standaardprojectgroep voor het opgegeven projecttype. Wanneer nieuwe projecten worden gesynchroniseerd vanuit Project Service Automation, wordt de **Projectgroep** de standaard op basis van het projecttype als u geen standaardwaarde hebt verschaft in de integratiesjabloon.  |
| **Standaardwaarden voor factureringstype**    | **Factureringstype** | Klik op **Nieuw** om een rij toe te voegen waarin u het factureringstype kunt selecteren waarvoor de standaardregeleigenschap wordt ingesteld. Een bepaald factureringstype kan slechts één keer worden geselecteerd in de configuratie.          |
|                              | **Regeleigenschap**| Selecteer de standaardregeleigenschap voor het opgegeven factureringstype. Wanneer nieuwe uurramingen, nieuwe onkostenramingen of nieuwe werkelijke waarden worden gesynchroniseerd vanuit Project Service Automation, wordt de **Regeleigenschap** de standaard op basis van het factureringstype.          |
| **Functionaliteit vergrendelen**    |                   | Selecteer de uit te schakelen functionaliteit in Finance and Operations voor projecten en contracten die afkomstig zijn uit Project Service Automation. U kunt bijvoorbeeld de mogelijkheid uitschakelen om contracten en projecten te bewerken, structuren voor werkspecificaties te maken en urenstaten in te voeren in Finance and Operations. Boekhoudinggerelateerde velden blijven ingeschakeld, zelfs als ze niet beschikbaar zijn gemaakt met de parameterinstelling. Standaard worden alle functies ingeschakeld.           |

