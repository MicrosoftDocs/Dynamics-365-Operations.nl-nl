---
title: Behoefteplanningsinstellingen
description: Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.
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
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "322554"
---
# <a name="coverage-settings"></a>Behoefteplanningsinstellingen

[!include [banner](../includes/banner.md)]

Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen. 

U kunt behoefteplanningsinstellingen op verschillende manieren instellen:

-   Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op. U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep. Klik op **Hoofdplanning &gt; Instellen &gt; Behoefteplanning &gt; Dekking Behoefteplanning** om een behoefteplanningsgroep te maken. U kunt een behoefteplanningsgroep koppelen aan een product. Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**. Als de koppeling generisch is, ongeacht de productdimensies, gebruikt u **Behoefteplanningsgroep** op het sneltabblad **Plannen** op de pagina **Productgegevens**. Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning gebruik van de **Algemene behoefteplanningsgroep** die is als standaard is opgegeven op de pagina **Parameters hoofdplanning**.

-   Geef behoefteplanningsinstellingen op voor een product. U kunt behoefteplanningsinstellingen maken voor een bepaald product. Klik op **Productgegevensbeheer &gt; Producten &gt; Vrijgegeven producten**. Selecteer het product in het **Actievenster** en klik op het tabblad **Plannen** in de **Behoefteplanningsgroep** op **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen. Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken. De behoefteplanningsinstellingen op de pagina **Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.

<!-- -->

-   Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard. De wizard is een stapsgewijze ondersteuning bij het instellen van de primaire artikelbehoefteplanningsparameters. Klik op de pagina **Artikelbehoefteplanning** op **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.

<!-- -->

- Geef behoefteplanningsinstellingen op voor een dimensiegroep. Klik op **Productgegevensbeheer &gt; Algemeen &gt; Vrijgegeven producten**. Klik op de pagina **Vrijgegeven productdetail** op het tabblad **Algemeen** in de groep **Beheer** op de koppeling **Opslagdimensiegroep**. Selecteer op de pagina **Opslagdimensiegroep** het veld **In behoefteplan opnemen volgens dimensie** om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken. Alle productdimensies, zoals configuratie, kleur, grootte, stijl, moeten het veld **In behoefteplan opnemen volgens dimensie** hebben geselecteerd.



<a name="additional-resources"></a>Aanvullende resources
--------

[Hoofdplannen](master-plans.md)



