---
title: Typen kritieke eigenschappen van activa
description: In het onderwerp wordt uitgelegd hoe u typen kritieke eigenschappen van activa maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 660038060826ade9301e50143e49b53ba3fcd3ab
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783185"
---
# <a name="asset-criticalities"></a>Kritieke eigenschappen van activa

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In het onderwerp wordt uitgelegd hoe u typen kritieke eigenschappen van activa maakt in Activabeheer. Kritieke eigenschappen van activa zijn gerelateerd aan activa en worden overgebracht naar werkorders. Zij kunnen niet worden gewijzigd in een werkorder. Kritieke eigenschappen van activa worden gebruikt voor het berekenen van kritieke eigenschappen van een werkorder tijdens de planning van de werkorder. Met andere woorden, zij worden gebruikt om te berekenen in hoeverre een onderhoudstaak voor een activum van invloed is op het productieschema en de productiviteit in uw bedrijf. Zie [Parameters voor activabeheer](../setup-for-objects/enterprise-asset-management-parameters.md) voor meer informatie over de instellingen die zijn gerelateerd aan de berekening van beoordelingsscores voor de planning van werkorders.

Als u kritieke eigenschappen wilt instellen, maakt u eerst de typen kritieke eigenschappen die moeten worden gebruikt in de activa-instellingen. Vervolgens stelt u kritieke eigenschappen van activa in.

## <a name="set-up-criticality-types"></a>Typen kritieke eigenschappen instellen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Typen kritieke eigenschappen**.
2. Selecteer **Nieuw** om een record te maken.
3. Voer in het veld **Kritieke eigenschappen** een getal in dat de kritieke eigenschappen aangeeft.
4. Voer in het veld **Naam** een naam voor het type kritieke eigenschappen in.
5. Voer in het veld **Factor** een factor in. Deze factor wordt gebruikt tijdens de berekening van de werkorderplanning om de record voor kritieke eigenschappen te bepalen die moet worden gebruikt. (Er wordt altijd gebruikgemaakt van de record met de hoogste factor.) Deze instelling is relevant als, zoals wordt weergegeven in de volgende afbeelding, regels voor kritieke eigenschappen worden gemaakt met dezelfde waarde voor kritieke eigenschappen.

    ![Figuur 1](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Kritieke eigenschappen van activa instellen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Kritieke eigenschappen van activa**.
2. Selecteer **Nieuw** om een record te maken.
3. Afhankelijk van het vereiste detailniveau voor kritieke eigenschappen van activa moet u relevante selecties maken in de velden **Functionele locatie**, **Activatype**, **Fabrikant**, **Model**, **Activum**, **Categorie van taaktype**, **Taaktype**, **Variant van taaktype** en **Taakbehoefte**.

    > [!NOTE]
    > Wanneer de kritieke eigenschappen van een activum zijn geselecteerd, doorloopt Activabeheer alle records voor kritieke eigenschappen van activa om te controleren op een mogelijke overeenkomst. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Met andere woorden, Activabeheer controleert eerst **Taakbehoefte**. Als er geen overeenkomst wordt gevonden, wordt **Variant van taaktype** gecontroleerd. Als er geen overeenkomst wordt gevonden, wordt **Taaktype** gecontroleerd, enzovoort. Zoals u zien in de lay-out van de pagina, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden. Als er geen overeenkomst wordt gevonden, wordt de 'standaardrecord' zonder selecties gebruikt.

4. Selecteer in het veld **Kritieke eigenschappen** een van de waarden voor kritieke eigenschappen die u in de vorige procedure hebt gemaakt.

### <a name="notes-about-criticality-setup"></a>Opmerkingen over de instelling van kritieke eigenschappen

- Als u de kritieke eigenschappen van een activum in deze instellingen wijzigt nadat u deze al hebt gebruikt op een werkorder, worden de kritieke eigenschappen van de werkorder niet dienovereenkomstig bijgewerkt.
- De kritieke eigenschappen van een werkorder worden telkens opnieuw berekend wanneer een werkorderregel wordt toegevoegd aan of verwijderd uit de werkorder.
- Als een werkorder meerdere werkordertaken bevat, wordt voor de werkorder altijd gebruikgemaakt van de hoogste kritieke eigenschappen, volgens het veld **Factor** op de pagina **Typen kritieke eigenschappen**.
- Over het algemeen kunnen kritieke eigenschappen van activa veranderen gedurende een periode. Kritieke eigenschappen kunnen worden beïnvloed door de aanschaf van nieuwe apparatuur, verbouwingen, enzovoort. Overweeg om de kritieke eigenschappen van uw activa op regelmatige tijdstippen opnieuw te evalueren (bijvoorbeeld één keer per jaar of om het andere jaar) om ervoor te zorgen dat uw definities voor kritieke eigenschappen overeenkomen met uw huidige productie-instellingen.
