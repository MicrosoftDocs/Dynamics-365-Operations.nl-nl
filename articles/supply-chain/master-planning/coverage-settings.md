---
title: Behoefteplanningsinstellingen
description: Dit onderwerp bevat informatie over de instellingen voor behoefteplanning die door de hoofdplanning wordt gebruikt om artikelbehoeften te berekenen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538889"
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

## <a name="additional-resources"></a>Aanvullende bronnen

[Hoofdplannen](master-plans.md)
