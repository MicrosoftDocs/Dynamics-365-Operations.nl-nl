---
title: Leverancierswerkstroom
description: Wijzig leveranciergegevens en gebruik de werkstroom om deze goed te keuren.
author: sunfzam
ms.date: 11/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: cfc255265df48e4a47aee4f13016356fb4775aa7
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799459"
---
# <a name="vendor-workflow"></a>Leverancierswerkstroom

[!include [banner](../includes/banner.md)]

Wanneer de leverancierswerkstroom wordt gebruikt, worden wijzigingen die zijn aangebracht in specifieke velden verzonden naar de werkstroom voordat ze worden toegevoegd aan de leverancier.

## <a name="set-up-the-vendor-workflow"></a>De leverancierswerkstroom instellen

Voordat u de werkstroomfunctie kunt gebruiken, moet u deze inschakelen.

1. Ga naar **Leveranciers \> Instellen \> Parameters van Leveranciers**.
2. Stel op het tabblad **Algemeen** op het sneltabblad **Goedkeuring van leverancier** de optie **Goedkeuringen van leveranciers inschakelen** in op **Ja**.
3. Geef in het veld **Gedrag van gegevensentiteit** aan hoe gegevens moeten worden geïmporteerd:

    - **Wijzigingen zonder goedkeuring toestaan**: de gegevensentiteit kan de leveranciersrecord bijwerken zonder deze via de werkstroom te verwerken.
    - **Wijzigingen afwijzen**: de leveranciersrecord kan niet worden gewijzigd. Het importeren mislukt voor de velden die zijn ingeschakeld voor de werkstroom.
    - **Wijzigingsvoorstellen maken**: alle velden worden gewijzigd behalve de velden die zijn ingeschakeld voor de werkstroom. De nieuwe waarden voor deze velden worden toegevoegd aan de leverancier als voorgestelde wijzigingen en de werkstroom wordt automatisch gestart.

4. Schakel vervolgens in de lijst met leveranciersvelden het selectievakje **Inschakelen** in voor elk veld dat moet worden goedgekeurd voordat de wijzigingen kunnen worden aangebracht.
5. Ga naar **Leveranciers \> Instellen \> Leverancierswerkstromen**.
6. Selecteer **Nieuw**.
7. Selecteer **Werkstroom van voorgestelde leverancierswijzigingen**. 
8. Stel de werkstroom in zodat deze overeenkomt met uw goedkeuringsproces. Door het goedkeuringselement **Werkstroomgoedkeuring voor voorgestelde leverancierswijziging** van de werkstroom worden de wijzigingen toegepast op de leverancier.

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a>Leveranciersgegevens wijzigen en de wijzigingen in de werkstroom indienen

Wanneer u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt de pagina **Voorgestelde wijzigingen** weergegeven. Deze pagina geeft de oorspronkelijke waarde weer van het veld en de nieuwe waarde die u hebt ingevoerd. Het veld dat u hebt gewijzigd, wordt teruggezet op de oorspronkelijke waarde. Ook een statusbericht op de pagina meldt dat uw wijzigingen niet zijn ingediend. 

Elke keer dat u een veld wijzigt dat is ingeschakeld voor de werkstroom, wordt dat veld toegevoegd aan de lijst op de pagina **Voorgestelde wijzigingen**. Als u de voorgestelde waarde voor een veld wilt verwijderen, gebruikt u de knop **Verwijderen** naast het veld in de lijst. Als u alle wijzigingen wilt verwijderen, gebruikt u de knop **Alle wijzigingen verwijderen** onder aan de pagina. Selecteer **OK** om de pagina te sluiten.

Als u ten minste één voorgestelde wijziging hebt, worden twee extra tabbladen weergegeven in het Actievenster: **Voorgestelde wijzigingen** en **Werkstroom**.

1. Selecteer **Voorgestelde wijzigingen** om de pagina **Voorgestelde wijzigingen** te openen en uw wijzigingen te bekijken.
2. Selecteer **Werkstroom \> Indienen** om de wijzigingen in te dienen bij de werkstroom.

    De status op de pagina wordt gewijzigd in **Wijzigingen in afwachting van goedkeuring**.

De werkstroom volgt het standaard werkstroomproces. De fiatteur wordt doorgestuurd naar de pagina **Leverancier**, waar de wijzigingen op de pagina **Voorgestelde wijzigingen** kunnen worden gecontroleerd en **Werkstroom \> Goedkeuren** kan worden geselecteerd om de werkstroom goed te keuren. Nadat alle goedkeuringen zijn voltooid, worden de velden bijgewerkt met de voorgestelde waarden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
