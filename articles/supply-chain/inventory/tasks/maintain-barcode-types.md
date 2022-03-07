---
title: Typen streepjescodes onderhouden
description: Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van de orderverzamellijst.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4102f8036c0aede7c8a2adcaa9b8799a71ac7ada
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441284"
---
# <a name="maintain-bar-code-types"></a>Typen streepjescodes onderhouden

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u een nieuwe definitie van streepjescodes instelt die u vervolgens kunt gebruiken als onderdeel van het rapport van de orderverzamellijst. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven. Deze taken worden meestal uitgevoerd door een magazijnmanager.

1. Ga naar **Streepjescodes**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Streepjescode instellen** in.
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer een optie in het veld **Streepjescodetype**.
    * Als u USMF gebruikt, kunt u 'Code 39' selecteren.
1. Geef in het veld **Masker-id** de streepjescodemasker-id op. Streepjescodemaskers worden gebruikt om streepjescodes te maken en snel streepjescodes te identificeren die in het POS-systeem worden gescand. Zie [Streepjescodemaskers instellen](../../../commerce/set-up-bar-code-masks.md) voor meer informatie.
1. Voer in het veld **Grootte** een nummer in.
1. Voer in het veld **Maximumlengte** een getal in.
1. Selecteer **Opslaan**.
1. Sluit de pagina.
1. Ga naar **Parameters voor voorraad- en magazijnbeheer**.
1. Typ of selecteer een waarde in het veld **Streepjescode instellen**.
    * Selecteer de instelling van streepjescodes die u eerder hebt gemaakt, maar houd er rekening mee dat de indeling van streepjescodes moet overeenkomen met de indeling van de unieke identificatie van het registratietype die in het proces wordt gebruikt. Voor orderverzamelroutes moet de indeling van streepjescodes bijvoorbeeld overeenkomen met de indeling van de verwijzing van de orderverzamelroute, die meestal een nummerreeks is.  
1. Selecteer **Opslaan**.
1. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
