---
title: Behoefteplanningsinstellingen
description: Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c1c5654afa6b592e178af052e3e4a7e246a94c9f
ms.lasthandoff: 03/31/2017


---

# <a name="coverage-settings"></a>Behoefteplanningsinstellingen

Voor de hoofdplanning wordt gebruikgemaakt van behoefteplanningsinstellingen om artikelbehoeften te berekenen. 

U kunt behoefteplanningsinstellingen op verschillende manieren instellen:

-   Geef de behoefteplanningsinstellingen voor een behoefteplanningsgroep op. U kunt een behoefteplanningsgroep maken die instellingen bevat voor alle producten die zijn gekoppeld aan de behoefteplanningsgroep. Klik op **hoofdplanning &gt;Setup &gt;dekking &gt;Behoefteplanningsgroepen** om een behoefteplanningsgroep te maken. U kunt een behoefteplanningsgroep koppelen aan een product. Als de koppeling specifiek is voor een locatie, magazijn of productdimensie, gebruikt u het veld **Behoefteplanningsgroep** op de pagina **Artikelbehoefteplanning**. Als de koppeling generisch is, ongeacht de productdimensies, gebruikt u **Behoefteplanningsgroep** op het sneltabblad **Plannen** op de pagina **Productgegevens**. Als u geen behoefteplanningsgroep aan een product koppelt, maakt de hoofdplanning gebruik van de **Algemene behoefteplanningsgroep** die is als standaard is opgegeven op de pagina **Parameters hoofdplanning**.

-   Geef behoefteplanningsinstellingen op voor een product. U kunt behoefteplanningsinstellingen maken voor een bepaald product. Klik op **productgegevensbeheer &gt;producten &gt;vrijgegeven producten**. Selecteer het product op de **actievenster**op de **plannen** tabblad de **behoefteplanningsgroep**, klikt u op **artikelbehoefteplanning** te openen de **artikelbehoefteplanning** pagina. Als het product al aan een behoefteplanningsgroep is gekoppeld, kunt u de behoefteplanningsgroepsinstellingen negeren door het veld **Overschrijven** te gebruiken. De behoefteplanningsinstellingen op de pagina** Artikelbehoefteplanning** hebben voorrang op de instellingen op de pagina **Behoefteplanningsgroep**.

<!-- -->

-   Geef behoefteplanningsinstellingen voor een product op met behulp van een wizard. De wizard is een stapsgewijze ondersteuning bij het instellen van de primaire artikelbehoefteplanningsparameters. Klik op de pagina **Artikelbehoefteplanning** op **Wizard** om de **Wizard Artikelbehoefteplanning** te openen.

<!-- -->

-   Geef behoefteplanningsinstellingen op voor een dimensiegroep. Klik op **productgegevensbeheer &gt;veelgebruikte &gt;vrijgegeven producten**. Op de ** vrijgegeven productdetails ** pagina op de **algemeen** tabblad in het **beheer** groep, klikt u op de **opslagdimensiegroep** koppeling. Selecteer op de pagina **Opslagdimensiegroep** het veld **In behoefteplan opnemen volgens dimensie** om de behoefteplanningsinstellingen voor een dimensie in de opslagdimensiegroep te maken. Alle dimensies, zoals configuratie, kleur, grootte, stijl, beschikt over de **behoefteplan opnemen volgens dimensie** is ingeschakeld.



<a name="see-also"></a>Zie ook
--------

[Master plans](master-plans.md)


