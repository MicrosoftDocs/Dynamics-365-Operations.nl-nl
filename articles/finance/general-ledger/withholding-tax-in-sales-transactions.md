---
title: Bronbelasting in verkooptransacties
description: Dit onderwerp bevat de stappen voor het voorkomen van de berekening van bronbelasting voor geselecteerde klanten. Voor klanten die bronbelasting opgeven in hun betalingen aan u, kunt u de standaard bronbelastinggroep toewijzen.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060721"
---
# <a name="withholding-tax-in-sales-transactions"></a>Bronbelasting in verkooptransacties

Dit onderwerp bevat de stappen voor het voorkomen van de berekening van bronbelasting voor geselecteerde klanten. Voor klanten die bronbelasting opgeven in hun betalingen aan u, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Klanten**. 

1. Ga in het navigatiedeelvenster naar **Modules > Klanten > Klanten > Alle klanten**.

2. Klik op de betreffende klantrekening en klik op **Bewerken**.

3. Stel op het tabblad **Factuur en levering** het veld **Bronbelasting berekenen** in op **Ja**.

   > [!NOTE] 
   > Bronbelasting wordt niet berekend als **Bronbelasting berekenen** voor deze klant niet wordt ingeschakeld in de hoofdgegevens.

4. Selecteer een bronbelastinggroep in **Bronbelastinggroep**.

5. Klik op **Opslaan**.

Voor artikelen/services waarvoor bronbelasting moet worden betaald, kunt u de standaard **artikelbronbelastinggroep** toewijzen in **Vrijgegeven producten**.

1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.

2. Klik op het betreffende artikelnummer en klik op **Bewerken**.

3. Klik op het tabblad **Verkopen** op **Bronbelasting berekenen**.

   > [!NOTE] 
   > Bronbelasting wordt niet berekend als **Bronbelasting berekenen** niet op **Ja** is ingesteld voor dit artikel op het tabblad **Verkopen** op de pagina **Vrijgegeven product**.

4. Selecteer een artikelbronbelastinggroep in de lijst **Artikelbronbelastinggroep**.

5. Klik op **Opslaan**.

Bronbelastinggroepen en artikelbronbelastinggroepen kunnen worden toegewezen via de pagina **Verkooporder**. 

De standaard bronbelastinggroep en artikelbronbelastinggroep worden als standaardwaarden gebruikt op verkooporderregels wanneer u een nieuwe verkooporder maakt.

Bronbelasting wordt berekend en geboekt met **Journaal met betalingen van klant**. U kunt de toepasselijke bronbelastingcode en het werkelijke bronbelastingbedrag handmatig aanpassen op het tabblad **Bronbelasting** op de pagina **Transacties vereffenen**.

Het berekende bronbelastingbedrag wordt afgetrokken van de klantbetaling en geboekt op de **tegenrekening voor bronbelasting** in een gerelateerd boekstuk.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]