---
title: Levenscyclusstatussen van activa
description: In dit onderwerp worden levenscyclusstatussen van activa en levenscyclusmodellen in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1752298ce726b904defb1c826a1e2d5014286e1f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216523"
---
# <a name="asset-lifecycle-states"></a>Levenscyclusstatussen van activa

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp worden levenscyclusstatussen van activa en levenscyclusmodellen in Activabeheer uitgelegd. Levenscyclusstatussen van activa worden gebruikt om te definiëren of een activum actief of inactief is. U kunt bijvoorbeeld de levenscyclusstatussen van activa instellen op **Gemaakt**, **Actief** en **Beëindigd**.

> [!NOTE]
> - Aanvragen voor levenscyclusstatussen zijn gekoppeld aan levenscyclusstatussen van activa. Daarom krijgt, wanneer een aanvraag wordt gewijzigd in een nieuwe aanvraag voor levenscyclusstatus, het activum dat is gekoppeld aan de aanvraag een nieuwe van de levenscyclusstatus van activa. Als bijvoorbeeld de levenscyclusstatus van een aanvraag wordt gewijzigd in **Inkomend**, wordt de levenscyclusstatus van het gekoppelde activum gewijzigd in de levenscyclusstatus die is geselecteerd in het veld **Inkomende levenscyclusstatus** op het sneltabblad **Levenscyclusstatus van activa** van de pagina **Modellen voor levenscyclusstatussen van activa**. 


Levenscyclusstatussen van activa kunnen worden ingesteld in levenscyclusmodellen van activa, waar u de vereiste levenscyclusstatussen voor verschillende typen activa kunt definiëren. U stelt eerst levenscyclusstatussen in. Vervolgens maakt u een levenscyclusmodel en selecteert u levenscyclusstatussen hiervoor.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Levenscyclusstatussen**.
2. Selecteer **Nieuw** om een nieuwe levenscyclusstatus van activa te maken.
3. Voer in het veld **Levenscyclusstatus** de id van de levenscyclusstatus in.
4. Voer in het veld **Naam** een beschrijving in.

    Het veld **Levenscyclusmodellen** bevat het aantal levencyclusmodellen van activa dat gebruikmaakt van de levenscyclusstatus van activa.

5. Stel de optie **Actief** in op **Ja** als deze levenscyclusstatus een actieve levenscyclusstatus moet zijn (met andere woorden, als werkorders kunnen worden gemaakt voor activa die zich in deze levenscyclusstatus bevinden).
6. Stel de optie **Openstaande kalenderregels verwijderen** in op **Ja** als openstaande activakalenderregels die de levenscyclusstatus **Gemaakt** van activa hebben, moeten worden verwijderd wanneer ze zich in deze levenscyclusstatus bevinden. Deze instelling is handig als u alle open onderhoudsschema's wilt opschonen die niet langer relevant zijn voor het activum (bijvoorbeeld als het activum niet meer actief is).

> [!NOTE]
> Levencyclusstatussen van activa, levenscyclusmodellen van activa en activatypen zijn gerelateerd. Ze worden op dezelfde manier gebruikt als levenscyclusstatussen van werkorders, levenscyclusmodellen van werkorders en typen werkorders. 


Nadat u de vereiste levenscyclusstatussen van activa hebt gemaakt, kunt u levenscyclusstatussen instellen in levenscyclusmodellen van activa.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Activa** \> **Levenscyclusmodellen**.
2. Selecteer **Nieuw** om een nieuw levenscyclusmodel van activa te maken.
3. Voer in het veld **Levenscyclusmodel** de id van het levenscyclusmodel in.
4. Voer in het veld **Naam** een beschrijving in.

    Het veld **Levenscyclusstatussen** bevat het aantal levencyclusstatussen activa die zijn geselecteerd in het levenscyclusmodel van activa. Het veld **Activatypen** bevat het aantal activatypen dat gebruikmaakt van het levenscyclusmodel.

5. Selecteer op het sneltabblad **Levenscyclusstatussen** het aantal levencyclusstatussen van activa dat moet worden opgenomen in het levenscyclusmodel van activa.

    - Als u een levenscyclusstatus voor het model wilt gebruiken, selecteert u deze in de sectie **Resterende levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-rechts ![Pijl-rechts](media/15-setup-for-objects.png) om deze te verplaatsen naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u alle beschikbare levenscyclusstatussen voor het model wilt gebruiken, selecteert u de knop **Alle beschikbare levenscyclusstatussen** ![Alle beschikbare levenscyclusstatussen](media/20-setup-for-objects.png). Alle levenscyclusstatussen worden overgebracht naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u een levenscyclusstatus uit het model wilt verwijderen, selecteert u deze in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-links ![Pijl-links](media/16-setup-for-objects.png) om deze te verplaatsen naar de sectie **Resterende levenscyclusstatussen**.

6. Selecteer **Updates van levenscyclusstatussen** om de levenscyclusstatussen van activa te definiëren die een geselecteerde levenscyclusstatus kunnen volgen.
7. U gebruikt het sneltabblad **Activastatus** als u activa verwerkt die u voor reparatie ontvangt. In de sectie **Inkomend/uitgaand** kunt u levenscyclusstatussen van activa selecteren om de werkstroom aan te geven van een activum dat u voor reparatie ontvangt. Als u leenactiva aanbiedt aan klanten of afdelingen, kunt u in de sectie **Loan** levenscyclusstatussen selecteren voor leenactiva.
