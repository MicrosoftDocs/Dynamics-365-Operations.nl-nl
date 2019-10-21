---
title: Parameters van Project Service Automation-integratie
description: In dit onderwerp wordt uitgelegd hoe u kunt configureren hoe standaardgegevens worden ingevoerd wanneer u Microsoft Dynamics 365 for Project Service Automation met Microsoft Dynamics 365 Finance integreert.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174813"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation-integratieparameters

[!include[banner](../includes/banner.md)]

Op de pagina **Integratieparameters Project Service Automation** kunt u configureren hoe standaardgegevens worden ingevoerd wanneer u Dynamics 365 Project Service Automation integreert met Dynamics 365 Finance. Als u projecten met succes wilt synchroniseren vanuit Project Service Automation met Finance, moet u de volgende velden instellen.

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurramingen, onkostenramingen en functionaliteitvergrendeling zijn beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is mogelijk in versie 8.0.1 of hoger.


| Tab                    | Veld                | Beschrijving |
|------------------------|----------------------|-------------|
| Algemeen                | Standaardprojecttype | Selecteer het standaardprojecttype. Wanneer projecten worden gesynchroniseerd vanuit Project Service Automation, wordt deze waarde gebruikt als u geen standaardwaarde hebt verstrekt in de integratiesjabloon. Tijdens de synchronisatie wordt het veld **Projecttype** van nieuwe projecten ingesteld op deze waarde. De waarde kan echter worden bijgewerkt wanneer de projectcontractregels worden gesynchroniseerd vanuit Project Service Automation. |
|                        | Tijdcategorie        | Selecteer de standaardtijdcategorie. Deze waarde wordt gebruikt wanneer uurramingen worden gesynchroniseerd vanuit Project Service Automation. Wanneer de uurramingen en werkelijke uurwaarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** van nieuwe projectuurramingen in Finance ingesteld op deze waarde. |
|                        | Categorie bijzondere kosten         | Selecteer de standaardkostencategorie. Deze waarde wordt gebruikt wanneer werkelijke kosten worden gesynchroniseerd vanuit Project Service Automation. Wanneer de werkelijke kostenwaarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** van nieuwe kostentransacties in Finance ingesteld op deze waarde. |
| Standaardinstellingen voor projectgroep | Projecttype         | Klik op **Nieuw** om een rij toe te voegen waarin u het projecttype kunt selecteren waarvoor de standaardprojectgroep moet worden ingesteld. Een bepaald projecttype kan slechts één keer worden geselecteerd in de configuratie. |
|                        | Projectgroep        | Selecteer de standaardprojectgroep voor het geselecteerde projecttype. Wanneer nieuwe projecten worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Projectgroep** ingesteld op de standaardwaarde voor het projecttype als u geen standaardwaarde hebt verschaft in de integratiesjabloon. |
| Standaardwaarden voor factureringstype  | Factureringstype         | Klik op **Nieuw** om een rij toe te voegen waarin u het factureringstype kunt selecteren waarvoor de standaardregeleigenschap wordt ingesteld. Een bepaald factureringstype kan slechts één keer worden geselecteerd in de configuratie. |
|                        | Regeleigenschap        | Selecteer de standaardregeleigenschap voor het geselecteerde factureringstype. Wanneer nieuwe uurramingen, nieuwe onkostenramingen of nieuwe werkelijke waarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Regeleigenschap** ingesteld op de standaardwaarde voor het factureringstype. |
| Functionaliteit vergrendelen  | Niet van toepassing       | Selecteer de uit te schakelen functionaliteit in Finance voor projecten en contracten die afkomstig zijn uit Project Service Automation. U kunt bijvoorbeeld de mogelijkheid uitschakelen om contracten en projecten te bewerken, structuren voor werkspecificaties te maken en urenstaten in te voeren in Finance. Boekhoudinggerelateerde velden blijven ingeschakeld, zelfs als ze niet beschikbaar zijn gemaakt met de parameterinstelling. Standaard zijn alle functies ingeschakeld. |
