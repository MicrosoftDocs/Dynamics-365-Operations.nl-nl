---
title: Streepjescodes instellen
description: In dit artikel wordt beschreven hoe u barcodes in Dynamics 365 Commerce gebruikt.
author: josaw1
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.industry: Retail
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
ms.openlocfilehash: 5771ada4a9bba92fb32155ae425f08d6429b46e6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271791"
---
# <a name="set-up-bar-codes"></a>Streepjescodes instellen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u barcodes in Dynamics 365 Commerce gebruikt.

U kunt streepjescodes gebruiken voor het kopen en verkopen van producten, om productvarianten bij te houden en om klanten en werknemers in te stellen. U kunt streepjescodes gebruiken om kortingbonnen, cadeaubonnen en creditnota's uit te geven en te verwerken. U kunt producten instellen met standaardstreepjescodes of met op maat gemaakte, interne streepjescodes. Producten kunnen meer dan één streepjescode hebben. Een product kan bijvoorbeeld meerdere streepjescodes hebben indien het afkomstig is van verschillende fabrikanten of indien er varianten zijn op basis van grootte, stijl of kleur. Streepjescodes kunnen het gewicht of de prijs van het product bevatten. Streepjescodemaskers zijn sjablonen die worden gebruikt voor het maken van streepjescodes.

> [!NOTE]
> Als u aan elke variantcombinatie een unieke streepjescode toewijst, kunt u de streepjescode van het artikel bij de kassa scannen en het programma laten bepalen welke variant van het product wordt verkocht. Op die manier kunt u ook verkoopstatistieken op basis van varianten verzamelen en weergeven. Aan elke grootte-, kleur- en stijlgroep kan een uniek nummer worden toegewezen dat die groep in de streepjescode identificeert. Commerce gebruikt het streepjescodemasker om automatisch voor elke variantcombinatie streepjescodes te genereren. Deze functionaliteit kan nuttig zijn als er veel maten, kleuren en stijlen zijn, aangezien het aantal combinaties aanzienlijk kan oplopen met elke extra toegevoegde variantcode. Als deze functie niet wordt gebruikt, moeten streepjescodes handmatig worden toegewezen aan elke combinatie die een productvariant representeert.

U kunt de streepjescodes handmatig of automatisch maken. Om streepjescodes te maken, voert u de volgende taken uit in de volgorde waarin ze zijn vermeld.

1. [Stel tekens van streepjescodemaskers in](set-up-bar-code-masks.md).
2. [Stel streepjescodemaskers in](set-up-bar-code-masks.md).
3. Stel de instellingen voor streepjescodes in.
4. [Maak streepjescodes voor producten](../supply-chain/pim/tasks/create-bar-code-product.md).

## <a name="additional-resources"></a>Aanvullende resources

[Streepjescodemaskers instellen](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
