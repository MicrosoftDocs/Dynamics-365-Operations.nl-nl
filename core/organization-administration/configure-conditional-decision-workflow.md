---
title: Een voorwaardelijke beslissing configureren in een workflow
description: Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c21c8e33ab3a88e1b93ca81d6f0770f1c77fe139
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Een voorwaardelijke beslissing configureren in een workflow

[!include[banner](../includes/banner.md)]


Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.

Een voorwaardelijke beslissing is een punt waarop een workflow in twee takken wordt verdeeld. Om een voorwaardelijke beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de voorwaardelijke beslissing en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.

## <a name="name-a-decision"></a>Een naam geven aan een beslissing
Voer deze stappen uit om een naam op te geven voor een voorwaardelijke beslissing.
1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Voer in het veld **Naam** een unieke naam voor de voorwaardelijke beslissing in.

## <a name="set-conditions"></a> Voorwaarden instellen
Het systeem bepaalt welke tak wordt gebruikt om het aangeboden document te verwerken door te beoordelen of het document aan de specifieke voorwaarden voldoet.
1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Klik op **Voorwaarde toevoegen**.
3.  Een voorwaarde invoeren.
4.  Geef desgewenst extra voorwaarden op.
5.  Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd.
    1.  Klik op **Testen** om het formulier **Workflowvoorwaarde testen** te openen.
    2.  Selecteer een record in het gebied **Voorwaarde valideren** van het formulier.
    3.  Klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.
    4.  Klik op **OK** of **Annuleren** om terug te gaan naar het formulier **Eigenschappen**.






