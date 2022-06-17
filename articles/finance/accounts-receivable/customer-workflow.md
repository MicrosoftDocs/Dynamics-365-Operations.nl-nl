---
title: Klantenwerkstroom
description: Dit artikel bevat informatie over de werkstroom voor klanten. U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de werkstroom verzenden voordat ze worden toegevoegd aan de klant.
author: abruer
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 883e77b5480a52201673e58a641c7180009a129c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864420"
---
# <a name="customer-workflow"></a>Klantenwerkstroom

[!include [banner](../includes/banner.md)]

De klantenwerkstroom is toegevoegd aan versie 8.0.4. U kunt specifieke velden voor een klant wijzigen en deze wijzigingen ter goedkeuring via de werkstroom verzenden voordat ze worden toegevoegd aan de klant.

## <a name="set-up-the-customer-workflow"></a>De klantenwerkstroom instellen

Voordat u de functie voor klantenwerkstroom kunt gebruiken, moet u deze inschakelen.

1. Ga naar **Klanten \> Instellen \> Parameters van module Klanten**.
2. Stel op het tabblad **Algemeen**, op de FastTab **Goedkeuring klant** de optie **Goedkeuringen van klanten inschakelen** in op **Ja** om de functie in te schakelen.
3. In het veld **Gedrag van gegevensentiteit** selecteert u de werking die de gegevensentiteiten moeten gebruiken wanneer gegevens worden geïmporteerd:

    - **Wijzigingen zonder goedkeuring toestaan**: een entiteit kan de klantrecord bijwerken zonder dit via de werkstroom te verwerken.
    - **Wijzigingen negeren**: de klantrecord kan niet worden gewijzigd. Het importeren mislukt voor de velden die zijn ingeschakeld voor de werkstroom.
    - **Wijzigingsvoorstellen maken**: alle velden worden gewijzigd behalve de velden die zijn ingeschakeld voor de werkstroom. De nieuwe waarden voor deze velden worden toegevoegd aan de klant als voorgestelde wijzigingen en de werkstroom wordt automatisch gestart.

4. Schakel vervolgens in de lijst met klantvelden het selectievakje **Inschakelen** in voor elk veld dat moet worden goedgekeurd voordat de wijzigingen kunnen worden aangebracht.
5. Ga naar **Klanten \> Instellen \> Klantenwerkstromen**.
6. Selecteer **Nieuw**.
7. Selecteer **Voorgestelde werkstroom voor klantwijziging**. 
8. Stel de werkstroom in zodat deze overeenkomt met uw goedkeuringsproces. Door het goedkeuringselement **Werkstroomgoedkeuring voor voorgestelde klantwijziging** van de werkstroom worden de wijzigingen toegepast op de klant.

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a>Klantgegevens wijzigen en de wijzigingen in de werkstroom indienen

Wanneer u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt de pagina **Voorgestelde wijzigingen** weergegeven. Deze pagina geeft de oorspronkelijke waarde weer van het veld en de nieuwe waarde die u hebt ingevoerd. Het veld dat u hebt gewijzigd, wordt teruggezet op de oorspronkelijke waarde. Een statusbericht op de pagina meldt dat uw wijzigingen niet zijn ingediend.

Elke keer dat u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt dat veld toegevoegd aan de lijst met voorgestelde wijzigingen. Als u de voorgestelde waarde voor een veld wilt verwijderen, gebruikt u de knop **Verwijderen** naast het veld in de lijst. Als u alle wijzigingen wilt verwijderen, gebruikt u de knop **Alle wijzigingen verwijderen** onder aan de pagina. Selecteer **OK** om de pagina te sluiten.

Als u ten minste één voorgestelde wijziging hebt, worden twee extra menu's weergegeven in het Actievenster: **Voorgestelde wijzigingen** en **Werkstroom**.

1. Selecteer **Voorgestelde wijzigingen** om de pagina **Voorgestelde wijzigingen** te openen en uw wijzigingen te bekijken.
2. Selecteer **Werkstroom \> Indienen** om de wijzigingen in te dienen bij de werkstroom.

    De status op de pagina wordt gewijzigd in **Wijzigingen in afwachting van goedkeuring**.

De werkstroom volgt het standaard werkstroomproces in de toepassing. De fiatteur wordt doorgestuurd naar de pagina **Klant**, waar de wijzigingen op de pagina **Voorgestelde wijzigingen** kunnen worden gecontroleerd en **Werkstroom \> Goedkeuren** kan worden geselecteerd om de werkstroom goed te keuren. Nadat alle goedkeuringen zijn voltooid, worden de velden bijgewerkt met de voorgestelde waarden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
