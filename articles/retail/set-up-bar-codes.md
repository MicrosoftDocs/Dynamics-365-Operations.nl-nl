---
title: Streepjescodes instellen
description: In dit artikel wordt beschreven hoe u barcodes in Microsoft Dynamics 365 for Retail gebruikt.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "347348"
---
# <a name="set-up-bar-codes"></a>Streepjescodes instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u barcodes in Microsoft Dynamics 365 for Retail gebruikt.

U kunt streepjescodes gebruiken voor het kopen en verkopen van producten, om productvarianten bij te houden en om klanten en werknemers in te stellen. U kunt streepjescodes gebruiken om kortingbonnen, cadeaubonnen en creditnota's uit te geven en te verwerken. U kunt detailhandelproducten instellen met standaardstreepjescodes of met op maat gemaakte, interne streepjescodes. Producten kunnen meer dan één streepjescode hebben. Een product kan bijvoorbeeld meerdere streepjescodes hebben indien het afkomstig is van verschillende fabrikanten of indien er varianten zijn op basis van grootte, stijl of kleur. Streepjescodes kunnen het gewicht of de prijs van het product bevatten. Streepjescodemaskers zijn sjablonen die worden gebruikt voor het maken van streepjescodes.

> [!NOTE]
> Als u aan elke variantcombinatie een unieke streepjescode toewijst, kunt u de streepjescode van het artikel bij de kassa scannen en het programma laten bepalen welke variant van het product wordt verkocht. Op die manier kunt u ook verkoopstatistieken op basis van varianten verzamelen en weergeven. Aan elke grootte-, kleur- en stijlgroep kan een uniek nummer worden toegewezen dat die groep in de streepjescode identificeert. Dynamics 365 for Retail gebruikt het streepjescodemasker om automatisch voor elke variantcombinatie streepjescodes te genereren. Deze functionaliteit kan nuttig zijn als er veel maten, kleuren en stijlen zijn, aangezien het aantal combinaties aanzienlijk kan oplopen met elke extra toegevoegde variantcode. Als deze functie niet wordt gebruikt, moeten streepjescodes handmatig worden toegewezen aan elke combinatie die een productvariant representeert.

U kunt de streepjescodes handmatig of automatisch maken. Om streepjescodes te maken, voert u de volgende taken uit in de volgorde waarin ze zijn vermeld.

1. [Stel tekens van streepjescodemaskers in](set-up-bar-code-masks.md).
2. [Stel streepjescodemaskers in](set-up-bar-code-masks.md).
3. Stel de instellingen voor streepjescodes in.
4. Maak streepjescodes voor producten.

## <a name="additional-resources"></a>Aanvullende resources

[Streepjescodemaskers instellen](set-up-bar-code-masks.md)
