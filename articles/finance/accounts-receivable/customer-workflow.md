---
title: Klantenworkflow
description: Dit onderwerp bevat informatie over de workflow voor klanten. U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de workflow verzenden voordat ze worden toegevoegd aan de klant.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a74b8ed226c4e13c8684fe86d4dca7236a84040e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012183"
---
# <a name="customer-workflow"></a>Klantenworkflow

[!include [banner](../includes/banner.md)]

De klantenworkflow is toegevoegd aan versie 8.0.4. U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de workflow verzenden voordat ze worden toegevoegd aan de klant.

## <a name="set-up-the-customer-workflow"></a>De klantenworkflow instellen

Voordat u de functie voor klantenworkflow kunt gebruiken, moet u deze inschakelen.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
2. Stel op het tabblad **Algemeen**, op de FastTab **Goedkeuring klant** de optie **Goedkeuringen van klanten inschakelen** in op **Ja** om de functie in te schakelen.
3. In het veld **Gedrag van gegevensentiteit** selecteert u de werking die de gegevensentiteiten moeten gebruiken wanneer gegevens worden geïmporteerd:

    - **Wijzigingen zonder goedkeuring toestaan**: een entiteit kan de klantrecord bijwerken zonder dit via de workflow te verwerken.
    - **Wijzigingen negeren**: de klantrecord kan niet worden gewijzigd. Het importeren mislukt voor de velden die zijn ingeschakeld voor de workflow.
    - **Wijzigingsvoorstellen maken**: alle velden worden gewijzigd behalve de velden die zijn ingeschakeld voor de workflow. De nieuwe waarden voor deze velden worden toegevoegd aan de klant als voorgestelde wijzigingen en de workflow wordt automatisch gestart.

4. Schakel vervolgens in de lijst met klantvelden het selectievakje **Inschakelen** in voor elk veld dat moet worden goedgekeurd voordat de wijzigingen kunnen worden aangebracht.
5. Ga naar **Klanten \> Instellen \> Klantenworkflows**.
6. Selecteer **Nieuw**.
7. Selecteer **Voorgestelde workflow voor klantwijziging**. 
8. Stel de workflow in zodat deze overeenkomt met uw goedkeuringsproces. Door het goedkeuringselement **Workflowgoedkeuring voor voorgestelde klantwijziging** van de workflow worden de wijzigingen toegepast op de klant.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Klantgegevens wijzigen en de wijzigingen in de workflow indienen

Wanneer u een veld wijzigt dat is ingeschakeld voor de workflow, wordt de pagina **Voorgestelde wijzigingen** weergegeven. Deze pagina geeft de oorspronkelijke waarde weer van het veld en de nieuwe waarde die u hebt ingevoerd. Het veld dat u hebt gewijzigd, wordt teruggezet op de oorspronkelijke waarde. Een statusbericht op de pagina meldt dat uw wijzigingen niet zijn ingediend.

Elke keer dat u een veld wijzigt dat is ingeschakeld voor de workflow, wordt dat veld toegevoegd aan de lijst met voorgestelde wijzigingen. Als u de voorgestelde waarde voor een veld wilt verwijderen, gebruikt u de knop **Verwijderen** naast het veld in de lijst. Als u alle wijzigingen wilt verwijderen, gebruikt u de knop **Alle wijzigingen verwijderen** onder aan de pagina. Selecteer **OK** om de pagina te sluiten.

Als u ten minste één voorgestelde wijziging hebt, worden twee extra menu's weergegeven in het Actievenster: **Voorgestelde wijzigingen** en **Workflow**.

1. Selecteer **Voorgestelde wijzigingen** om de pagina **Voorgestelde wijzigingen** te openen en uw wijzigingen te bekijken.
2. Selecteer **Workflow \> Indienen** om de wijzigingen in te dienen bij de workflow.

    De status op de pagina wordt gewijzigd in **Wijzigingen in afwachting van goedkeuring**.

De workflow volgt het standaard workflowproces in de toepassing. De fiatteur wordt doorgestuurd naar de pagina **Klant**, waar de wijzigingen op de pagina **Voorgestelde wijzigingen** kunnen worden gecontroleerd en **Werkstroom \> Goedkeuren** kan worden geselecteerd om de werkstroom goed te keuren. Nadat alle goedkeuringen zijn voltooid, worden de velden bijgewerkt met de voorgestelde waarden.
