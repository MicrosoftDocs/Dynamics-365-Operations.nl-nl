---
title: Een verlof voor onbepaalde tijd maken
description: In dit artikel wordt uitgelegd hoe u een verlof voor onbepaalde tijd maakt in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 08231d4139209387c3c76923fafdd2061fceb280
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805337"
---
# <a name="create-an-open-ended-leave-of-absence"></a>Een verlof voor onbepaalde tijd maken

> [!IMPORTANT]
> De functionaliteit die in dit artikel wordt beschreven zal beschikbaar zijn in de Finance-infrastructuur als onderdeel van een toekomstige versie na Microsoft Dynamics 365 Finance versie 10.0.31.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt aanvragen indienen voor verlof voor onbepaalde tijd en de status van uw verlofaanvragen bekijken in Dynamics 365 Human Resources.

## <a name="prerequisites"></a>Vereisten

1. Zorg er onder **Functiebeheer** voor dat de functie **Verlof voor onbepaalde tijd** is ingeschakeld.

    > [!IMPORTANT]
    > Deze functie kan niet meer worden uitgeschakeld wanneer deze eenmaal is ingeschakeld.

2. Maak een verloftype.
3. Voer de gegevens in, zoals het verloftype, de beschrijving en de werkstroom-id.
4. Selecteer **Verlof** in het veld **Aanvraagtype**.
5. Stel in het detailgedeelte voor verlof voor onbepaalde tijd de optie **Voor onbepaalde tijd** in op **Ja**.
6. Stel de optie **Weer aan het werk-melding** in op **Ja** of **Nee**.
7. Mogelijk is een weer aan het werk-melding vereist voor aanvragen voor verlof voor onbepaalde duur.

> [!NOTE]
> Nadat deze functie is ingeschakeld, is de functie **Bijlage vereist** ingeschakeld.

## <a name="request-an-open-ended-leave-of-absence"></a>Een verlof voor onbepaalde tijd aanvragen

1. Selecteer in de werkuimte **Selfservice werknemer** de optie **Meer** (...) op de tegel **Verlofsaldi**.
2. Selecteer **Verlof aanvragen** als u een verlofaanvraag wilt indienen.
3. Geef informatie op in de velden **Verloftype** en **Begindatum**. Voer in het veld **Einddatum** een voorlopige einddatum in.
4. Selecteer **Uploaden** onder **Bijlagen** als u ondersteunende documenten moet indienen.
5. Selecteer **Indienen** wanneer u gereed bent om uw aanvraag in te dienen. Selecteer anders **Concept opslaan**.
6. Als u een verlofaanvraag voor een verlof voor onbepaalde tijd wilt bijwerken, selecteert u de aanvraag, voert u een einddatum in het veld **Einddatum**, stelt u de optie **Einddatum bevestigen** in op **Ja** en uploadt u documentatie.
7. Als de optie **Weer aan het werk-melding** is ingesteld op **Ja**, selecteer ut **Uploaden** en schakelt u vervolgens het selectievakje in om te bevestigen dat een geldige melding voor terugkeer op het werk is geüpload.
8. Wanneer alle gegevens zijn ingevoerd, selecteert u **Indienen**.
