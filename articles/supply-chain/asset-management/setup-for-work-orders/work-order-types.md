---
title: Werkordertypen
description: In dit onderwerp wordt uitgelegd hoe u werkordertypen instelt in Activabeheer.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderType
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6bdc9d226d8e1aa6960cac38b95b0245e46ee1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825585"
---
# <a name="work-order-types"></a>Werkordertypen

[!include [banner](../../includes/banner.md)]

 

Werkordertypen worden gebruikt om werkorders te categoriseren. Zo kunnen er typen werkorders zijn die betrekking hebben op preventief onderhoud of op correctief onderhoud.

Een werkordertype definieert een aansluiting met een levenscyclusmodel van een werkorder. Met een levenscyclusmodel voor werkorders worden de statuswaarden voor levenscyclusmodellen voor werkorders gedefinieerd. (Voorbeelden van statuswaarden voor werkorders zijn **Gemaakt**, **Onderhanden** en **Voltooid**.)

Zie [Levenscyclusstatussen van werkorder](work-order-lifecycle-states.md)voor meer informatie over levenscyclusstatussen van werkorders en projectfasen.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Werkordertypen**.
2. Selecteer **Nieuw** om een levenscyclustype te maken.
3. Voer in het veld **Werkordertype** een id in voor het werkordertype.
4. Voer in het veld **Naam** een naam in.
5. Selecteer in het veld **Levenscyclusmodel van werkorder** een model voor de levenscyclus.
5. Stel de optie **Eén onderhoudsmedewerker** in op **Ja** als alle werkordertaken die zijn gerelateerd aan een werkorder van dit type, moeten worden gepland voor dezelfde onderhoudsmedewerker.
6. Selecteer in het veld **Kostentype** uit **Corrigerend**, **Preventief** of **Investering**. Alle werkordertaken op een werkorder moeten hetzelfde kostentype hebben.
7. Stel in de sectie **Verplicht** de relevante opties in op **Ja** om aan te geven welke fout- of uitvaltijd-gerelateerde informatie wordt toegevoegd aan een werkorder van dit type.

    > [!NOTE]
    > De opties in de sectie **Verplicht** zijn gerelateerd aan de opties op het sneltabblad **Valideren** van de pagina **Levenscyclusstatus van werkorder** (**Activabeheer** \> **Instellen** \> **Werkorders** \> **Levenscyclusstatussen**).

8. Selecteer **Opslaan**.

![Werkordertypen](media/16-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]