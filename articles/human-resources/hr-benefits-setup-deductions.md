---
title: Inhoudingen configureren
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008640"
---
# <a name="configure-deductions"></a>Inhoudingen configureren

[!include [banner](includes/preview-feature.md)]

Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding. Inhoudingen hebben een ingangsdatum, dus kunt u een historisch overzicht van de inhoudingen bijhouden. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Inhoudingen**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | Aftrek | Een unieke id die wordt gebruikt om de vergoedingsinhouding te identificeren. |
   | Beschrijving | Een omschrijving voor de inhouding. |
   | Geldig vanaf | De begindatum. De standaardwaarde is de huidige systeemdatum. |
   | Vervaldatum | De einddatum. De standaardwaarde is 12/31/2154, wat 'nooit' betekent. |
   | Koptekst | De koptekstcode uit de salarisadministratie die bij deze inhouding wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie. Deze code wordt gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt. |
   | Verwijzing van werknemer voor salarisinhouding | De inhoudingscode van de salarisadministratie die in deze inhouding wordt gebruikt voor het werknemergedeelte van de inhouding bij het verwerken van de vergoedingen voor de salarisadministratie. |
   | Kop voor bedrag | De koptekstcode uit de salarisadministratie die bij dit inhoudingsbedrag wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie. Deze code wordt gewoonlijk gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt. |
   | Kan verwijderen | Hiermee geeft u aan of een geëxporteerde waarde uit Dynamics 365 for Finance and Operations ertoe kan leiden dat de waarde in de salarisadministratie wordt verwijderd. |
   | Gekoppelde kolommen | Hiermee geeft u aan of de koptekst en het inhoudingsbedrag in gekoppelde, aangrenzende kolommen naar de salarisadministratie moeten worden geëxporteerd. |
   | Ingangsdatum wijzigen | De datum waarop de wijziging van de vergoedingsinhouding van kracht wordt. Op deze datum wordt de vergoedingsinhouding automatisch door het systeem gewijzigd en worden alle vergoedingsplannen die aan deze inhouding zijn gekoppeld, bijgewerkt zolang u de verwerking van de wijziging van de inhouding uitvoert. |
   | Wijziging inhouding voltooid | Het selectievakje 'Wijziging van inhouding voltooid' wordt automatisch ingeschakeld nadat de wijzigingen in de vergoedingsinhouding zijn voltooid door de verwerking van de wijziging van de inhouding. |
   
4. Als u wijzigingen in de instellingen van het vergoedingstarief wilt bijhouden en beheren, selecteert u **Acties** en selecteert u vervolgens **Versies onderhouden**.

5. Selecteer **Opslaan**. 
