---
title: Voorwaardelijke beslissingen configureren in een workflow
description: Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a880d4be461ea9b2caa61b7d038f9b24486a919
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798874"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Voorwaardelijke beslissingen configureren in een workflow

[!include [banner](../includes/banner.md)]

Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.

Een voorwaardelijke beslissing is een punt waarop een workflow in twee takken wordt verdeeld. Om een voorwaardelijke beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de voorwaardelijke beslissing en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.

## <a name="name-a-decision"></a>Een naam geven aan een beslissing

Voer deze stappen uit om een naam op te geven voor een voorwaardelijke beslissing.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Voer in het veld **Naam** een unieke naam voor de voorwaardelijke beslissing in.

## <a name="set-conditions"></a> Voorwaarden instellen

Het systeem bepaalt welke tak wordt gebruikt om het aangeboden document te verwerken door te beoordelen of het document aan de specifieke voorwaarden voldoet.

1. Klik in het linkerdeelvenster op **Basisinstellingen**.
2. Klik op **Voorwaarde toevoegen**.
3. Een voorwaarde invoeren.
4. Geef desgewenst extra voorwaarden op.
5. Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd.

    1. Klik op **Testen** om het formulier **Workflowvoorwaarde testen** te openen.
    2. Selecteer een record in het gebied **Voorwaarde valideren** van het formulier.
    3. Klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.
    4. Klik op **OK** of **Annuleren** om terug te gaan naar het formulier **Eigenschappen**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]