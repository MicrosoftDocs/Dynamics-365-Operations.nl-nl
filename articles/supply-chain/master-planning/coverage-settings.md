---
title: Behoefteplanningsinstellingen
description: Dit artikel bevat informatie over de instellingen voor behoefteplanning die door de hoofdplanning wordt gebruikt om artikelbehoeften te berekenen.
author: t-benebo
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1218c447a18f79f9a44bfa413a0414d6926d7499
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871944"
---
# <a name="coverage-settings"></a>Behoefteplanningsinstellingen

[!include [banner](../includes/banner.md)]

Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.

U kunt behoefteplanningsinstellingen op verschillende manieren instellen:

- Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op.

    U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep. Ga naar **Hoofdplanning &gt; Instellen &gt; Behoefteplanning &gt; Behoefteplanningsgroepen** om een behoefteplanningsgroep te maken. U kunt een behoefteplanningsgroep koppelen aan een product. Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**. Als de koppeling algemeen is, ongeacht de productdimensies, gebruikt u het veld **Behoefteplanningsgroep** op het sneltabblad **Plannen** van de pagina **Productgegevens**. Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning standaard gebruik van de algemene behoefteplanningsgroep die is opgegeven op de pagina **Parameters hoofdplanning**.

- Geef behoefteplanningsinstellingen op voor een product.

    U kunt behoefteplanningsinstellingen maken voor een bepaald product. Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het product en selecteer vervolgens in het actievenster op het tabblad **Plannen** in de groep **Behoefteplanning** de optie **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen. Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken. De behoefteplanningsinstellingen op de pagina **Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.

- Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard.

    De wizard leidt u stapsgewijs door het proces van het instellen van de parameters voor de primaire artikelbehoefteplanning. Selecteer op de pagina **Artikelbehoefteplanning** in het actievenster de optie **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.

- Geef behoefteplanningsinstellingen op voor een dimensiegroep.

    Ga naar **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer op de pagina **Vrijgegeven productdetails** op het sneltabblad **Algemeen** in de sectie **Beheer** de koppeling in het veld **Opslagdimensiegroep**. Schakel op de pagina **Opslagdimensiegroepen** het selectievakje **In behoefteplan opnemen volgens dimensie** in om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken. Het veld **In behoefteplan opnemen volgens dimensie** moet worden geselecteerd voor alle productdimensies, zoals configuratie, kleur, grootte en stijl.


## <a name="coverage-codes"></a>Dekkingscodes

Hoofdplanning kan worden geconfigureerd om verschillende aanvullingsmethoden te gebruiken. De aanvullingsmethoden of methoden voor het wijzigen van de lotgrootte zijn de technieken die door het systeem worden gebruikt om de batchgrootte voor ingekochte of geproduceerde artikelen te bepalen. 

Aan elke aanvullingsmethode is een van de volgende dekkingscodes toegewezen:

- **Handmatig**: de methode voor het bepalen van de partijgrootte waarbij het systeem geen inkoop-, overboekings- of productieorders voor het artikel voorstelt. De planner voor het artikel zal verantwoordelijk zijn voor het maken van de vereiste orders voor de aanvulling van het artikel.
- **Per vereiste**: de methode voor het bepalen van de partijgrootte waarbij het systeem een geplande inkoop-, overdrachts- of productieorder per behoefte voor het artikel maakt. Deze wordt over het algemeen gebruikt voor dure artikelen met periodieke vraag.  
- **Per periode**: de methode voor het bepalen van de partijgrootte waarmee alle vraag voor een periode in één order voor het artikel wordt gecombineerd. De order wordt gepland voor de eerste dag van de periode en de hoeveelheid voldoet aan de nettobehoeften gedurende de vastgestelde periode. De periode begint met de eerste vraag van het artikel en dekt de gedefinieerde lengte in de tijd. De volgende periode begint met de volgende vereisten van het artikel.
- **Min/max**: de methode voor het bepalen van partijgrootte die de aanvulling van de voorraad bevat tot een bepaald niveau wanneer de voorhanden voorraad onder een drempel valt. De aanvullingshoeveelheid is het verschil tussen het maximumniveau en het voorspelde voorhanden niveau.


## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Hoofdplannen](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]