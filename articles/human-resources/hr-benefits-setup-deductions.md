---
title: Inhoudingen configureren
description: Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a865f109379064ae8829532af9253238e203c322
ms.sourcegitcommit: 8592c661b41f9cef8b7ef2863a3b97bf49a4e6f9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/26/2021
ms.locfileid: "7423492"
---
# <a name="configure-deductions"></a>Inhoudingen configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding. Inhoudingen hebben een ingangsdatum, dus kunt u een historisch overzicht van de inhoudingen bijhouden. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Inhoudingen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Aftrek** | Een unieke id die wordt gebruikt om de vergoedingsinhouding te identificeren. |
   | **Beschrijving** | Een omschrijving voor de inhouding. |
   | **Geldig vanaf** | De begindatum. De standaardwaarde is de huidige systeemdatum. |
   | **Vervaldatum** | De einddatum. De standaardwaarde is 12/31/2154, wat 'nooit' betekent. |
   | **Koptekst** | De koptekstcode uit de salarisadministratie die bij deze inhouding wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie. Deze code wordt gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt. |
   | **Verwijzing van werknemer voor salarisinhouding** | De inhoudingscode van de salarisadministratie die in deze inhouding wordt gebruikt voor het werknemergedeelte van de inhouding bij het verwerken van de vergoedingen voor de salarisadministratie. |
   | **Kop voor bedrag** | De koptekstcode uit de salarisadministratie die bij dit inhoudingsbedrag wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie. Deze code wordt gewoonlijk gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt. |
   | **Kan verwijderen** | Hiermee geeft u aan of een geëxporteerde waarde uit Dynamics 365 for Finance and Operations ertoe kan leiden dat de waarde in de salarisadministratie wordt verwijderd. |
   | **Gekoppelde kolommen** | Hiermee geeft u aan of de koptekst en het inhoudingsbedrag in gekoppelde, aangrenzende kolommen naar de salarisadministratie moeten worden geëxporteerd. |
   | **Ingangsdatum wijzigen** | De datum waarop de wijziging van de vergoedingsinhouding van kracht wordt. Op deze datum wordt de vergoedingsinhouding en alle vergoedingsplannen die aan deze inhouding zijn gekoppeld, bijgewerkt zolang u de verwerking **Wijziging van de inhouding** uitvoert. |
   | **Wijziging inhouding voltooid** | Het selectievakje **Wijziging van inhouding voltooid** wordt automatisch ingeschakeld nadat de wijzigingen in de vergoedingsinhouding zijn voltooid door de verwerking van de wijziging van de inhouding. |
   
4. Als u wijzigingen in de instellingen van het vergoedingstarief wilt bijhouden en beheren, selecteert u **Acties** en selecteert u vervolgens **Versies onderhouden**.

5. Selecteer **Opslaan**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
