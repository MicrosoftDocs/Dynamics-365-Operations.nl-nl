---
title: Een workflow voor regelartikelen configureren
description: In dit onderwerp wordt uitgelegd hoe u een workflowelement voor regelartikelen configureert.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2781a0344f1de5caf0031d7c3d5b88678be153a4
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="configure-a-line-item-workflow"></a>Een workflow voor regelartikelen configureren

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u een workflowelement voor regelartikelen configureert.

Om een element in een workflow voor regelartikelen te configureren, klikt u in de workfloweditor met de rechtermuisknop op het goedkeuringselement en klikt u vervolgens op **Eigenschappen** om de pagina **Eigenschappen** te openen. Met behulp van de volgende procedures kunt dan u de eigenschappen van het element in een workflow voor regelartikelen configureren.

## <a name="name-the-lineitem-workflow-element"></a>Een naam opgeven voor het element in een workflow voor regelartikelen
Voer deze stappen uit om een naam op te geven voor het element in een workflow voor regelartikelen.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Geef in het veld **Naam** een unieke naam voor het element in een workflow voor regelartikelen op.

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a>Geef op of dezelfde workflow wordt gebruikt om alle regelartikelen te verwerken
Volg deze stappen om op te geven of dezelfde workflow wordt gebruikt om alle regelartikelen in een document te verwerken.

1.  Klik in het linkerdeelvenster op **Basisinstellingen**.
2.  Als dezelfde workflow alle regelartikelen in een document moet verwerken, klikt u op **Eén workflow aanroepen voor alle regelartikelen**. Selecteer vervolgens de workflow om te gebruiken voor het verwerken van de regelartikelen.
3.  Als een specifieke workflow de regelartikelen moet verwerken die aan een specifieke set voorwaarden voldoen, klikt u op **Eén workflow aanroepen voor elk regelartikel**. Voer deze stappen uit om de set voorwaarden te definiëren:
    1.  Klik op **Toevoegen**.
    2.  Selecteer ide voorwaarde in de tabel.
    3.  Geef in het tabblad **Voorwaardenaam** een naam op voor de set voorwaarden die u definieert.
    4.  Klik op **Voorwaarde toevoegen** om een voorwaarde in te voeren.
    5.  Geef desgewenst vereiste extra voorwaarden op.
    6.  Klik op **Testen** om te controleren of de door u ingevoerde set voorwaarden correct is ingesteld. Seelecteer op de pagina **Workflowvoorwaarde testen** in het gebied **Voorwaarde valideren** een record en klik op **Testen**. Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd. Klik op **OK** of **Annuleren** om terug te gaan naar de pagina **Eigenschappen**.

    Selecteer op het tabblad **Workflow** de workflow die u wilt gebruiken om regelartikelen te verwerken die aan de set voorwaarden voldoen die u hebt gedefinieerd.





