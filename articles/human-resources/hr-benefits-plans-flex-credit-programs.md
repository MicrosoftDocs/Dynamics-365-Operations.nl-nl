---
title: Flex-kredietprogramma's instellen
description: U kunt flex-kredietprogramma's in Microsoft Dynamics 365 Human Resources gebruiken om werknemers in te schrijven voor vergoedingen op basis van een vooraf bepaald aantal flex-kredieten.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ff3bd2c4d39a4411b5a5cb82e4281ff4af98ff0d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336874"
---
# <a name="set-up-flex-credit-programs"></a>Flex-kredietprogramma's instellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt flex-kredietprogramma's in Microsoft Dynamics 365 Human Resources gebruiken om werknemers in te schrijven voor vergoedingen op basis van een vooraf bepaald aantal flex-kredieten. Werknemers kunnen kiezen hoe zij hun flex-kredieten willen toewijzen. Als een werknemer bijvoorbeeld onder het ziektekostenverzekeringsplan van zijn of haar echtgenoot of echtgenote valt, kan deze werknemer de kredieten die hij of zij anders zou hebben gebruikt voor gezondheidszorg, nu gebruiken voor andere vergoedingen. 

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Plannen** de optie **Flex-kredietprogramma's**.

2. Selecteer **Nieuw**.

3. Geef de waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Vergoedingskrediet-id** | De unieke id van het flex-kredietprogramma. |
   | **Beschrijving** | Een omschrijving van het flex-kredietprogramma. | 
   | **Begindatum** | De datum waarop het flex-kredietprogramma actief wordt. |
   | **Einddatum** | De einddatum van het flex-kredietprogramma. U kunt de standaardwaarde (12/31/2154) laten staan om aan te geven dat het Flex-kredietprogramma geen geplande vervaldatum heeft. |
   | **Totale kredietwaarde** | Het aantal kredieten dat iedere werknemer dient te gebruiken voor zijn of haar vergoedingen. |
   | **Omslagregel** | De regel die moet worden gebruikt voor het evenredig verdelen van flex-kredieten wanneer een werknemer in dienst wordt genomen midden in een flex-kredietperiode. </br></br><ul><li>**Geen** – de werknemer ontvangt geen flex-kredieten als deze is aangesteld nadat de periode van het flex-kredietprogramma is gestart.</li><li>**Volledig krediet** – de werknemer ontvangt het volledige aantal flex-kredieten, ongeacht het moment waarop deze is aangesteld.</li><li>**Evenredig** – de werknemer ontvangt een evenredig aantal flex-kredieten op basis van de begindatum.</li></ul> |
   | **Formule voor het berekenen van een evenredig aantal flex-kredieten** | De regel die moet worden gebruikt voor het evenredig verdelen van het aantal flex-kredieten voor werknemers die in dienst wordt genomen midden in een vergoedingsperiode voor het flex-kredietprogramma. Het evenredige aantal flex-kredieten wordt berekend op basis van de begindatum van de aanstelling. Dit veld wordt alleen gebruikt als u **Evenredig** selecteert in het veld **Evenredigheidsregel**. </br></br><ul><li>**Dagelijks** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op dagniveau. Het totale aantal flex-kredieten wordt gedeeld door het aantal dagen in de periode. Als uw vergoedingsperiode bijvoorbeeld 400 dagen is, wordt het totale aantal flex-kredieten door 400 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per dag ontvangen.</li><li>**Huidige maand** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op maandniveau, afgerond op de huidige maand. Het totale aantal flex-kredieten wordt gedeeld door het aantal maanden in de periode. Als uw vergoedingsperiode bijvoorbeeld 15 maanden is, wordt het totale aantal flex-kredieten door 15 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per maand ontvangen.</li><li>**Volgende maand** – het aantal flex-kredieten dat een werknemer ontvangt, wordt evenredig verdeeld op maandniveau, afgerond op de volgende maand. Het totale aantal flex-kredieten wordt gedeeld door het aantal maanden in de periode. Als uw vergoedingsperiode bijvoorbeeld 15 maanden is, wordt het totale aantal flex-kredieten door 15 gedeeld om het aantal flex-kredieten te berekenen dat werknemers per maand ontvangen.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
