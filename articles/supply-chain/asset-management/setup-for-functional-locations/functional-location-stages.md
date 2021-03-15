---
title: Levenscyclusstatussen van functionele locatie
description: In dit onderwerp wordt beschreven hoe u statussen van functionele locaties en levenscyclusmodellen instelt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f119e68319b901b052fa4aa659260f386f44bcf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021265"
---
# <a name="functional-location-lifecycle-states"></a>Levenscyclusstatussen van functionele locatie

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp wordt beschreven hoe u levenscyclusstatussen van functionele locaties en levenscyclusmodellen instelt in Activabeheer. Levenscyclusstatussen van functionele locaties definiëren de statussen die een functionele locatie kan doorlopen, bijvoorbeeld gemaakt, actief en beëindigd. U kunt alle functionele locaties weergeven, ongeacht hun levenscyclusstatus, op de lijstpagina **Alle functionele locaties**. U kunt de status van een functionele locatie wijzigen door deze te selecteren op de lijstpagina **Alle functionele locaties** en **Status van functionele locatie bijwerken** te selecteren.

## <a name="set-up-functional-location-lifecycle-states"></a>Levenscyclusstatussen van functionele locatie instellen

1. Selecteer **Activabeheer** > **Instellingen** > **Functionele locaties** > **Levenscyclusstatussen**.
2. Selecteer **Nieuw** om een nieuwe status voor een functionele locatie te maken.
3. Voeg de status-id in het veld **Levenscyclusstatus** in en geef een naam op voor de status van de functionele locatie in het veld **Naam**. In het veld **Levenscyclusmodellen** kunt u het aantal levenscyclusmodellen voor functionele locatie zien dat gebruikmaakt van de status van de functionele locatie.
4. Selecteer op het sneltabblad **Algemeen** de optie 'Ja' op de wisselknop **Actief** als de functionele locatie bij deze status actief moet zijn.
5. Selecteer 'Ja' op de wisselknop **Activa maken** als het mogelijk moet zijn om automatisch een activum met dezelfde naam te maken als de functionele locatie en dit bij deze status te installeren op de functionele locatie.  
>[!NOTE]
>Deze wisselknop heeft betrekking op het veld **Activatype** op het sneltabblad **Algemeen** in het formulier **Typen functionele locatie** (**Activabeheer** > **Instellingen** > **Functionele locaties** > **Typen functionele locatie**).
6. Selecteer 'Ja' op de wisselknop **Locatie hernoemen** als het mogelijk moet zijn om de naam van de functionele locatie bij deze status te wijzigen.
7. Selecteer 'Ja' op de wisselknop **Nieuwe sublocaties** als het mogelijk moet zijn om nieuwe sublocaties toe te voegen aan de functionele locatie bij deze status.
8. Selecteer 'Ja' op de wisselknop **Activa installeren** als het mogelijk moet zijn om activa te installeren op de functionele locatie bij deze status.
9. Selecteer 'Ja' op de wisselknop **Functionele locatie verwijderen** als het mogelijk moet zijn om de functionele locatie te verwijderen bij deze status.
10. Selecteer een activastatus in het veld **Levenscyclusstatus** als u wilt dat de levenscyclusstatus van het activum automatisch wordt bijgewerkt bij deze status voor alle activa die op de functionele locatie zijn geïnstalleerd. Voorbeeld: als u een functionele locatie sluit en de levenscyclusstatus van de functionele locatie instelt op 'Beëindigd', wilt u mogelijk automatisch de levenscyclusstatus van de activa die op die functionele locatie zijn geïnstalleerd wijzigen in 'Niet in gebruik'.


>[!NOTE]
>Levenscyclusstatussen van functionele locaties, levenscyclusmodellen voor functionele locaties en typen functionele locaties zijn gerelateerd en worden op dezelfde manier gebruikt als levenscyclusstatussen van werkorders, levenscyclusmodellen voor werkorders en typen werkorders. 

## <a name="set-up-functional-location-lifecycle-models"></a>Levenscyclusmodellen voor functionele locaties instellen

Wanneer u de levenscyclusstatussen hebt gemaakt die zijn vereist voor uw functionele locaties, kunnen deze worden onderverdeeld in groepen. Dit wordt gedaan om de levenscyclusmodelstroom te maken die kan worden gebruikt voor verschillende typen functionele locaties. Er moet minimaal één standaard levenscyclusmodel voor functionele locaties worden gemaakt.

1. Selecteer **Activabeheer** > **Instellingen** > **Functionele locaties** > **Levenscyclusmodellen**.
2. Selecteer **Nieuw** om een nieuw levenscyclusmodel te maken.
3. Voeg de levenscyclusmodel-id in het veld **Levenscyclusmodel** in en geef een naam op voor het levenscyclusmodel in het veld **Naam**. In de velden **Typen functionele locatie** en **Levenscyclusstatussen** kunt u het aantal typen functionele locatie zien dat gebruikmaakt van het levenscyclusmodel en het aantal statussen dat is geselecteerd in het levenscyclusmodel.
4. Selecteer op het sneltabblad **Levenscyclusstatussen** de statussen die in het model moeten worden opgenomen. Dit wordt gedaan door op een status te klikken in de sectie **Resterende levenscyclusstatussen** en op de knop ![pijl naar voren](media/02-setup-for-functional-locations.png) te klikken.
5. Als u alle beschikbare statussen voor een model wilt selecteren, klikt u op de knop ![Alle beschikbare fasen selecteren](media/03-setup-for-functional-locations.png). Alle statussen worden overgebracht naar de sectie **Geselecteerde levenscyclusstatussen**.
6. Als u een geselecteerde status uit het model wilt verwijderen, selecteert u de status in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop ![pijl terug](media/04-setup-for-functional-locations.png).
7. Selecteer **Updates van levenscyclusstatussen** om te definiëren welke levenscyclusstatussen een geselecteerde status kunnen volgen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]