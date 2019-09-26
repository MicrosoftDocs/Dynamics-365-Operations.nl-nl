---
title: Statussen van levenscyclus voor onderhoudsverzoeken
description: In dit onderwerp wordt beschreven hoe u levenscyclusstatussen van onderhoudsverzoeken instelt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f68e11a1cd14bc35282b957a4262cbecdd627b3b
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790482"
---
# <a name="maintenance-request-states"></a>Statussen van onderhoudsverzoeken

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Levenscyclusstatussen van onderhoudsverzoeken bepalen de fasen die een verzoek kan doorlopen. Voorbeelden zijn **Gemaakt**, **Actief** en **Beëindigd**. Wanneer een onderhoudsverzoek wordt geconverteerd naar een werkorder, moet de levenscyclusstatus van het onderhoudsverzoek worden bijgewerkt naar **Beëindigd** of **Gesloten** om aan te geven dat het onderhoudsverzoek niet langer actief is. Op de pagina **Alle onderhoudsverzoeken** worden alle onderhoudsverzoeken weergegeven, ongeacht de levenscyclusstatus.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Levenscyclusstatussen van onderhoudsverzoek instellen

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Levenscyclusstatussen**.
2. Selecteer **Nieuw** om een levenscyclusstatus van een onderhoudsverzoek te maken.
3. Voer in het veld **Levenscyclusstatus** een id voor de levenscyclusstatus in.
4. Voer in het veld **Naam** een naam in.

    Op het sneltabblad **Details** wordt in het veld **Levenscyclusmodellen** het aantal levencyclusmodellen van onderhoudsverzoeken weergegeven die deze levenscyclusstatus gebruiken.

5. Stel op het sneltabblad **Algemeen** de optie **Actief** in op **Ja** als een onderhoudsverzoek actief moet zijn terwijl deze zich in deze levenscyclusstatus bevindt.
6. Stel de optie **Werkelijk einde instellen** in op **Ja** als een werkelijke einddatum en -tijd automatisch moeten worden ingevoerd op een onderhoudsverzoek dat zich in deze levenscyclusstatus bevindt.
7. Stel de optie **Werkorder maken** in op **Ja** als een werkorder kan worden gemaakt op basis van een onderhoudsverzoek dat zich in deze levenscyclusstatus bevindt.
8. Stel de optie **Verwijderen** in op **Ja** als een onderhoudsverzoek kan worden verwijderd terwijl deze zich in deze levenscyclusstatus bevindt.
9. Op het sneltabblad **Bijwerken** zijn de opties **Inkomend** en **Uitgaand** in de sectie **Activa** relevant als u depotreparatie gebruikt. Stel de juiste optie in op **Ja** als de levenscyclusstatus van activa die zijn geselecteerd op een onderhoudsverzoek automatisch moeten worden bijgewerkt naar **Inkomend** of **Uitgaand** wanneer de levenscyclusstatus van dat onderhoudsverzoek is ingesteld op **Inkomend** of **Uitgaand**.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Levenscyclusstatussen van onderhoudsverzoeken**.

![Figuur 1](media/02-setup-for-requests.png)

> [!NOTE]
> Levenscyclusstatussen, levenscyclusstatusgroepen en -typen van onderhoudsverzoeken zijn gerelateerd aan en worden op dezelfde manier gebruikt als levenscyclusstatussen, levenscyclusstatusgroepen en -typen van werkorders. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Levenscyclusmodellen van onderhoudsverzoeken instellen

Nadat u de levenscyclusstatussen hebt gemaakt die vereist zijn voor uw onderhoudsverzoeken, kunnen deze worden onderverdeeld in levenscyclusstatusgroepen of levenscyclusmodellen. Levenscyclusmodellen van onderhoudsverzoeken worden gebruikt voor het maken van de stroom die kan worden gebruikt voor verschillende typen onderhoudsverzoeken. Er moet minimaal één standaardlevenscyclusmodel voor onderhoudsverzoeken worden gemaakt.

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudsverzoeken** \> **Levenscyclusmodellen**.
2. Selecteer **Nieuw** om een levenscyclusmodel voor onderhoudsverzoeken te maken.
3. Voer in het veld **Levenscyclusmodel** de id van het levenscyclusmodel in.
4. Voer in het veld **Naam** een naam in.

    Het veld **Levenscyclusstatussen** op het sneltabblad **Details** bevat het aantal levencyclusstatussen die in dit levenscyclusmodel zijn geselecteerd. Het veld **Typen onderhoudsverzoeken** bevat het aantal typen onderhoudsverzoeken dat gebruikmaakt van dit levenscyclusmodel.

5. Ga naar het sneltabblad **Levenscyclusstatussen** en selecteer de levencyclusstatussen die moet worden opgenomen in het levenscyclusmodel:

    - Als u een levenscyclusstatus wilt opnemen in het levenscyclusmodel, selecteert u deze in de sectie **Resterende levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-rechts ![Pijl-rechts](media/03-setup-for-requests.png) om deze te verplaatsen naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u alle beschikbare levenscyclusstatussen in het levenscyclusmodel wilt opnemen, selecteert u de knop **Alle beschikbare statussen selecteren** ![Alle beschikbare statussen selecteren](media/04-setup-for-requests.png). Alle levenscyclusstatussen worden verplaatst naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u een levenscyclusstatus uit het levenscyclusmodel wilt verwijderen, selecteert u deze in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-links ![Pijl-links](media/05-setup-for-requests.png) om deze te verplaatsen naar de sectie **Resterende levenscyclusstatussen**.

6. Op het sneltabblad **Algemeen** zijn de velden in de sectie **Updates** relevant als u depotreparatie gebruikt.

    - Selecteer in het veld **Levenscyclusstatus voor ontvangen activum** de levenscyclusstatus waarnaar activa die zijn geselecteerd op een onderhoudsverzoek automatisch moeten worden bijgewerkt wanneer ze worden ontvangen voor depotreparatie.
    - Selecteer in het veld **Levenscyclusstatus voor geleverd activum** de levenscyclusstatus waarnaar activa die zijn geselecteerd op een onderhoudsverzoek automatisch moeten worden bijgewerkt wanneer ze worden geretourneerd na reparatie.

In de volgende afbeelding ziet u een voorbeeld van de pagina **Levenscyclusmodellen van onderhoudsverzoeken**.

![Figuur 2](media/06-setup-for-requests.png)