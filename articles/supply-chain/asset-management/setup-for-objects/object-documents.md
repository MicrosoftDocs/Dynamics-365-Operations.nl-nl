---
title: Activadocumenten
description: In dit onderwerp worden activadocumenten in Activabeheer uitgelegd.
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
ms.openlocfilehash: d1c90788da7ad536fb9978db18160ccf6c158033
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783169"
---
# <a name="asset-documents"></a>Activadocumenten

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In dit onderwerp worden activadocumenten in Activabeheer uitgelegd.

In Activabeheer kunt u documenten zo instellen dat deze automatisch worden gekoppeld aan bijvoorbeeld taaktypen, activafabrikanten, activatypen of activa. Deze functionaliteit is handig wanneer bijgewerkte documentversies worden vrijgegeven. In dat geval hoeft u alleen het bijgewerkte document op de standaardlocatie te plaatsen die u voor uw Microsoft Dynamics 365 for Finance and Operations-documenten gebruikt en het document te koppelen aan de activadocumentrecord die u hebt gemaakt. Het bijgewerkte document kan vervolgens worden geopend vanuit de menuopties **Alle activa**, **Actieve activa**, **Mijn actieve activa**, **Alle werkorders** en **Actieve werkordertaken**. Bij het proces voor het koppelen van documenten aan een activadocumentrecord wordt gebruikgemaakt van het standaardsysteem voor documentverwerking in Finance and Operations.

**Voorbeeld 1:** een document dat is gerelateerd aan een taaktype kan een procedure voor dat taaktype beschrijven.

**Voorbeeld 2:** een document dat is gerelateerd aan een combinatie van een activatype, fabrikant en model kan de standaardhandleiding zijn voor het geselecteerde model van de activafabrikant.

## <a name="create-asset-document-relation"></a>Activadocumentrelatie maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activadocumenten**.
2. Selecteer **Nieuw** om een activadocumentrecord te maken.
3. Afhankelijk van hoe specifiek u de documentrelatie witl maken, voert u relevante selecties uit in een of meer van de volgende velden: **Activatype**, **Fabrikant**, **Model**, **Activum**, **Categorie van taaktype**, **Taaktype**, **Variant van taaktype** en **Taakbehoefte**. De opties die beschikbaar zijn in de velden **Variant van taaktype** en **Taakbehoefte** zijn afhankelijk van uw selectie in het veld **Taaktype**.

    > [!NOTE]
    > Wanneer het systeem zoekt naar documenten die gerelateerd moeten zijn aan een activum of een werkorder, doorloopt Activabeheer alle activadocumentrecords om te controleren op een mogelijke overeenkomst. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Met andere woorden, Activabeheer controleert eerst op een overeenkomst voor het veld **Taakbehoefte**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Variant van taaktype**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Taaktype** enzovoort. Zoals u kunt zien in de indeling van de pagina **Activadocumenten**, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden. Verschillende documenten zijn mogelijk gerelateerd aan een activum of een werkorder. U kunt het serviceniveau voor een onderhoudsaanvraag of een werkorder naar behoefte bewerken.

4. Selecteer **Bijlagen**. De standaardpagina **Documentverwerking** in Finance and Operations wordt weergegeven.
5. Stel de documenten of notities in die aan de activadocumentrecord moeten worden gekoppeld. Nadat u documenten hebt gekoppeld, wordt in het veld **Bijlagen** het aantal documenten weergegeven dat aan de record is gerelateerd.