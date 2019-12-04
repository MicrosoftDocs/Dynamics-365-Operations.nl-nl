---
title: Activafabrikanten en -modellen
description: In dit onderwerp wordt uitgelegd hoe u activafabrikanten en gerelateerde modellen kunt instellen in Activabeheer.
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
ms.openlocfilehash: b77605070387871335c480e25cbe23af1155d6e8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812163"
---
# <a name="asset-manufacturers-and-models"></a>Activafabrikanten en -modellen

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt uitgelegd hoe u activafabrikanten en gerelateerde modellen kunt instellen in Activabeheer. Modellen kunnen worden gerelateerd aan activatypen.

## <a name="set-up-product-model-relations"></a>Productmodelrelaties instellen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Fabrikant en model**.
2. Selecteer **Nieuw** om een nieuw product te maken.
3. Voer in het veld **Fabrikant** een naam in voor de activafabrikant.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer op het sneltabblad **Modellen** de optie **Toevoegen** om een activamodel te maken dat moet worden gerelateerd aan de activafabrikant.
6. Voer in het veld **Model** een naam in voor de activamodel.
7. Voer in het veld **Beschrijving** een beschrijving in.
8. Selecteer in het veld **Activatype** het activatype waaraan het model van de fabrikant moet zijn gekoppeld.

    > [!NOTE]
    > U kunt ook relaties instellen voor activatypen, -fabrikanten en -modellen in het zoekveld **Activatypen**. Zie [Typen activa](../setup-for-objects/object-types.md) voor meer informatie.

    Op het sneltabblad **Details** geeft het veld **Modellen** het aantal activamodellen weer dat is ingesteld voor de geselecteerde activafabrikant. In het veld **Activa** wordt het aantal activa weergegeven dat de geselecteerde fabrikant gebruikt.
    
    In het veld **Activa** wordt het aantal objecten weergegeven dat het fabrikantmodel gebruikt.

> [!NOTE]
> Een activatype kan geen relaties met modellen van activafabrikanten hebben, kan betrekking hebben op één model van een activafabrikant van activa of kan zijn gerelateerd aan meerdere modellen van activafabrikanten. Als een actiatype is gerelateerd aan ten minste één model van een fabrikant, kunnen alleen de combinaties die zijn ingesteld in de zoekopdracht **Fabrikantmodel** worden geselecteerd op die pagina's van Activabeheer waar een combinatie van een activatype, fabrikant en model kan worden ingesteld. Deze pagina's bevatten **Alle activa**, **Activaserviceniveaus**, **Standaardwaarden voor taaktypen** en **Onderhoudsbudgetregels**. Als sommige activatypen niet zijn gerelateerd aan een fabrikantmodel, worden alleen de activatypen en fabrikantmodellen die ook geen relatie hebben met activatypen op de pagina's weergegeven.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Een fabrikant en model selecteren voor een object

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa**.
2. Selecteer in de kolom **Activum** de koppeling voor het activum. De pagina **Details** wordt weergegeven.
3. Selecteer **Bewerken**.
4. Selecteer op het sneltabblad **Algemeen** waarden in de velden **Fabrikant** en **Model**.
