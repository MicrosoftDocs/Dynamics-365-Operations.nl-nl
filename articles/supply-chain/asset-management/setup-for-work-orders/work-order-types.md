---
title: Werkordertypen
description: In dit onderwerp wordt uitgelegd hoe u werkordertypen instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 375b18a4bd37ddadecee03a01b3b2125f5cc8d0a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215419"
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
