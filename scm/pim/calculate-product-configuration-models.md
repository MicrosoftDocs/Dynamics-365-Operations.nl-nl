---
title: 'Berekeningen voor productconfiguratiemodellen: veelgestelde vragen'
description: In dit artikel worden berekeningen voor productconfiguratiemodellen beschreven en wordt uitgelegd hoe u berekeningen samen met beperkingen kunt gebruiken.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 34bebe1f7a324f2d77668d0eb3d6b2303f2544a4
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="calculations-for-product-configuration-models-faq"></a>Berekeningen voor productconfiguratiemodellen: veelgestelde vragen

[!include[banner](../includes/banner.md)]


In dit artikel worden berekeningen voor productconfiguratiemodellen beschreven en wordt uitgelegd hoe u berekeningen samen met beperkingen kunt gebruiken.

Berekeningen kunnen voor rekenkundige of logische bewerkingen worden gebruikt. Deze vullen expressiebeperkingen in productconfiguratiemodellen aan. U kunt berekeningen definiëren op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel** en vervolgens expressies maken voor de berekeningen in de expressie-editor. Raadpleeg Berekeningen maken voor meer informatie.

## <a name="what-is-a-calculation"></a>Wat is een berekening?
Een berekening is een element dat u in een productconfiguratiemodel kunt gebruiken. Berekeningen vullen beperkingen aan door u in staat te stellen decimale getallen te gebruiken om waarden te berekenen wanneer u een product configureert. Bovendien zijn voor de berekeningen een grotere set operators beschikbaar dan voor beperkingen.  

Zoals een beperking, wordt een berekening gekoppeld aan een specifieke component in een model voor productconfiguratie en kan de berekening niet worden hergebruikt of worden gedeeld met een andere component. Een belangrijk verschil tussen berekeningen en beperkingen is dat berekeningen imperatief (één richting) zijn, terwijl beperkingen verklarend (twee richtingen) zijn. Raadpleeg [Expressiebeperkingen en tabelbeperkingen](expression-constraints-table-constraints-product-configuration-models.md) voor meer informatie over beperkingen.  

Een berekening bestaat uit een berekeningsexpressie en een doelkenmerk.

## <a name="what-is-a-target-attribute"></a>Wat is een doelkenmerk?
Een doelkenmerk is een eigenschap die het resultaat van de berekeningsexpressie ontvangt.  

In de volgende expressie, is het doelkenmerk een tafelkleedmeting:  

**Expressie:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]  

**DecimalAttribute1** is de tabellengte en **decimalAttribute2** is de tafelkleedlengte. Deze expressie retourneert de waarde **True** naar het doelkenmerk als **decimalAttribute2** groter dan of gelijk aan **decimalAttribute1** is. Indien dit niet zo is retourneert de expressie de waarde **False**. De tafelkleedmeting is dus acceptabel als de tafelkleedlengte gelijk aan of langer dan de lengte van de tabel is.

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a>Welke kenmerktypen kunnen voor doelkenmerken worden ingesteld?
Alle kenmerktypen die voor de productconfiguratie worden ondersteund kunnen ingesteld worden voor doelkenmerken, behalve tekst zonder vaste lijst.

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a>Kan de waarde voor een doelkenmerk de waarden van de invoerkenmerken in een berekening beperken?
Nee, de waarde voor een doelkenmerk kan de waarden van de invoerkenmerken in een berekening niet beperken omdat berekeningen eenrichtings zijn. Daarom wordt de waarde van het doelkenmerk ingesteld op basis van wijzigingen in de waarde van de invoerkenmerken, maar een wijziging in de waarde van het doel heeft geen invloed op de waarde van de invoerkenmerken. Dit gedrag verschilt van het gedrag voor beperkingen. Beperkingen treden in beide richtingen op.

### <a name="example"></a>Voorbeeld

In de volgende expressie is het doel voor de berekening de lengte een stroomkabel en de invoerwaarde is een kleur:  

**Expressie:** \[If Color == "Groen", 1,5, 1,0\]  

Wanneer u het artikel configureert, wordt de lengte van de stroomkabel ingesteld op **1,5** als u als kleurenkenmerk **Groen** opgeeft. Als u een andere kleur opgeeft, is de lengte ingesteld op **1,0**. Echter, omdat berekeningen eenrichtings zijn, wordt in de berekening niet de waarde van het kleurenkenmerk op **Groen** ingesteld wanneer u een lengte van **1,5** opgeeft.

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a>Wat gebeurt er als een berekening een doelkenmerk van het gehele getaltype heeft maar een berekening een decimaal getal genereert?
Als een doelkenmerk van het type geheel getal is, maar een berekening genereert een decimaal getal, wordt alleen het geheel getaldeel van het berekende resultaat geretourneerd. Het decimale deel wordt verwijderd en het resultaat wordt niet afgerond. Een resultaat van 12,70 wordt bijvoorbeeld weergegeven als 12.

## <a name="when-do-calculations-occur"></a>Wanneer komen de berekeningen voor?
De berekeningen komen voor wanneer een waarde voor alle invoerkenmerken is opgegeven.

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a>Kan ik een waarde overschrijven die voor het doelkenmerk wordt berekend?
U kunt de waarde overschrijven die voor het doelkenmerk wordt berekend, tenzij het doelkenmerk is ingesteld als verborgen of alleen-lezen.

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a>Hoe kan ik een doelkenmerk instellen als verborgen of alleen-lezen?
Om een kenmerk in te stellen als verborgen of alleen-lezen, volgt u deze stappen.

1.  Klik op **Productgegevensbeheer** &gt; **Algemeen** &gt; **Productconfiguratiemodellen**.
2.  Selecteer een productconfiguratiemodel en klik vervolgens in het Actievenster op **Bewerken**.
3.  Selecteer op de pagina **Details van op beperkingen gebaseerd productconfiguratiemodel** het kenmerk dat u als doelkenmerk wilt gebruiken.
4.  Selecteer op het sneltabblad **Kenmerken** de optie **Verborgen** of **Alleen-lezen**.

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a>Kan een berekening de waarden die ik instel overschrijven?
Nr. De waarden die u instelt wanneer u een product configureert, zijn de waarden die worden gebruikt. De berekening die gemaakt wordt wanneer de invoerwaarden in een berekening worden gewijzigd kan de waarden niet overschrijven die u voor een specifiek kenmerk opgeeft.

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a>Wat gebeurt er als ik een invoerwaarde in een berekening verwijder?
Als u een invoerwaarde in een berekening verwijdert, wordt de waarde van het doelkenmerk ook verwijderd.

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a>Waarom krijg ik een foutbericht dat zegt dat mijn model in tegenspraak is?
Dit bericht verschijnt wanneer een berekening een fout bevat of wanneer er een tegenspraak aanwezig is in een of meerdere beperkingen. Raadpleeg [Expressiebeperkingen en tabelbeperkingen](expression-constraints-table-constraints-product-configuration-models.md) voor meer informatie over tegenspraak. Hier volgen enkele situaties waarin er fouten in berekeningen kunnen optreden:

-   Een waarde wordt gedeeld door 0 (nul).
-   Een conflict bestaat tussen deze volgende twee elementen:
    -   De waarden die voor een kenmerk beschikbaar zijn en die door een beperking worden beperkt
    -   Een waarde die door een berekening wordt gegenereerd
-   De waarden die in de berekening worden geretourneerd zijn buiten het domein van het kenmerk. Een voorbeeld is een geheel getal van \[[1..10]\] dat wordt berekend als 0.

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a>Waarom krijg ik een foutbericht hoewel ik succesvol mijn productmodel hebt gevalideerd?
De berekeningen zijn niet opgenomen in de validatie. U moet het productconfiguratiemodel testen om fouten in berekeningen te zoeken. Om een productconfiguratiemodel te testen, voert u deze stappen uit.

1.  Klik op **Productgegevensbeheer** &gt; **Algemeen** &gt; **Productconfiguratiemodellen**.
2.  Selecteer een productconfiguratiemodel en klik vervolgens in het Actievenster in de groep **Uitvoeren** op **Testen**.





