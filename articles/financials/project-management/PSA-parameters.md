---
title: Parameters van Project Service Automation-integratie
description: In dit onderwerp wordt uitgelegd hoe u kunt configureren hoe standaardgegevens worden ingevoerd bij integratie van Microsoft Dynamics 365 for Project Service Automation met Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation-integration-parameters"></a>Parameters van Project Service Automation-integratie

[!include[banner](../includes/banner.md)]

Op de pagina **Project Service Automation-integratieparameters** kunt u configureren hoe standaardgegevens worden ingevoerd bij integratie van Microsoft Dynamics 365 for Project Service Automation met Microsoft Dynamics 365 for Finance and Operations. Als u projecten met succes wilt synchroniseren vanuit Project Service Automation met Finance and Operations, moet u de volgende velden instellen.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in Microsoft Dynamics 365 for Finance and Operations, versie 8.0.
> - Integratie van werkelijke waarden is beschikbaar in Microsoft Dynamics 365 for Finance and Operations versie 8.01 of hoger.
> - Als u Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, 7.3.0 gebruikt, kunt u nadat u KB 4132657 en KB 4132660 hebt geïnstalleerd, de sjablonen gebruiken om projecttaken, onkostentransactiecategorieën, geraamde uren, geraamde onkosten en werkelijke waarden te integreren en om functionaliteitvergrendeling te configureren. Als u de boekhoudingsverdelingen opnieuw instellen moet, wordt u aangeraden ook KB 4131710 te installeren.

| Tabblad                    | Veld                | Omschrijving |
|------------------------|----------------------|-------------|
| Algemeen                | Standaardprojecttype | Selecteer het standaardprojecttype. Wanneer projecten worden gesynchroniseerd vanuit Project Service Automation, wordt deze waarde gebruikt als u geen standaardwaarde hebt verstrekt in de integratiesjabloon. Tijdens de synchronisatie wordt het veld **Projecttype** van nieuwe projecten ingesteld op deze waarde. De waarde kan echter worden bijgewerkt wanneer de projectcontractregels worden gesynchroniseerd vanuit Project Service Automation. |
|                        | Tijdcategorie        | Selecteer de standaardtijdcategorie. Deze waarde wordt gebruikt wanneer uurramingen worden gesynchroniseerd vanuit Project Service Automation. Wanneer de uurramingen en werkelijke uurwaarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** van nieuwe projectuurramingen in Finance and Operations ingesteld op deze waarde. |
|                        | Categorie bijzondere kosten         | Selecteer de standaardkostencategorie. Deze waarde wordt gebruikt wanneer werkelijke kosten worden gesynchroniseerd vanuit Project Service Automation. Wanneer de werkelijke kostenwaarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** van nieuwe kostentransacties in Finance and Operations ingesteld op deze waarde. |
| Standaardinstellingen voor projectgroep | Projecttype         | Klik op **Nieuw** om een rij toe te voegen waarin u het projecttype kunt selecteren waarvoor de standaardprojectgroep moet worden ingesteld. Een bepaald projecttype kan slechts één keer worden geselecteerd in de configuratie. |
|                        | Projectgroep        | Selecteer de standaardprojectgroep voor het geselecteerde projecttype. Wanneer nieuwe projecten worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Projectgroep** ingesteld op de standaardwaarde voor het projecttype als u geen standaardwaarde hebt verschaft in de integratiesjabloon. |
| Standaardwaarden voor factureringstype  | Factureringstype         | Klik op **Nieuw** om een rij toe te voegen waarin u het factureringstype kunt selecteren waarvoor de standaardregeleigenschap wordt ingesteld. Een bepaald factureringstype kan slechts één keer worden geselecteerd in de configuratie. |
|                        | Regeleigenschap        | Selecteer de standaardregeleigenschap voor het geselecteerde factureringstype. Wanneer nieuwe uurramingen, nieuwe onkostenramingen of nieuwe werkelijke waarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Regeleigenschap** ingesteld op de standaardwaarde voor het factureringstype. |
| Functionaliteit vergrendelen  | Niet van toepassing       | Selecteer de uit te schakelen functionaliteit in Finance and Operations voor projecten en contracten die afkomstig zijn uit Project Service Automation. U kunt bijvoorbeeld de mogelijkheid uitschakelen om contracten en projecten te bewerken, structuren voor werkspecificaties te maken en urenstaten in te voeren in Finance and Operations. Boekhoudinggerelateerde velden blijven ingeschakeld, zelfs als ze niet beschikbaar zijn gemaakt met de parameterinstelling. Standaard zijn alle functies ingeschakeld. |

