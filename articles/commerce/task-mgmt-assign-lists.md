---
title: Takenlijsten toewijzen aan winkels of werknemers
description: In dit artikel wordt beschreven hoe u takenlijsten toewijst aan winkels of werknemers in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: faff772051738f624b86fd23fb6bf29173e909ea
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746189"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Takenlijsten toewijzen aan winkels of werknemers

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u takenlijsten toewijst aan winkels of werknemers in Microsoft Dynamics 365 Commerce.

Met taakbeheer in Dynamics 365 Commerce kunt u een takenlijst toewijzen aan meerdere winkels of werknemers, of aan een combinatie van winkels en werknemers. Een regiomanager voor 20 winkels wil bijvoorbeeld de takenlijst **Voorbereiding kerstdagen** toewijzen aan alle 20 winkels.

## <a name="start-the-task-list-assignment-process"></a>Het toewijzingsproces voor takenlijst starten

Voordat u het toewijzen van taken start, moet u eerst een taaklijst maken door de stappen in het artikel [Takenlijsten maken en taken toevoegen](task-mgmt-create-lists.md) te volgen. Ga als volgt te werk om het toewijzingsproces van een takenlijst te starten.

1. Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.
1. Selecteer de takenlijst die u wilt toewijzen.
1. Selecteer **Proces starten**.
1. Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in (bijvoorbeeld **Winkels regio oost**).
1. Geef een datum op in het veld **Doeldatum**.
1. Als u de takenlijst aan winkels wilt toewijzen, gebruikt u op het tabblad **Winkels** het filter **Organisatiehiërarchie** om de winkels te zoeken en te selecteren.

    Om de takenlijst aan werknemers toe te wijzen, zoekt en selecteert u de werkernemers op het tabbald **Medewerkers**.

1. Selecteer **OK** om het proces te starten. De takenlijst wordt toegewezen aan de geselecteerde winkels of werknemers.

In de volgende afbeelding ziet u een voorbeeld van het zoeken naar en selecteren van winkels in het dialoogvenster **Proces starten**.

![Winkels zoeken en selecteren in het dialoogvenster Proces starten.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Takenlijsten op terugkerende basis toewijzen

Een detailhandelaar heeft soms terugkerende taken, zoals een 'controlelijst voor sluiting op donderdag' of een 'controlelijst voor de eerste dag van de maand'. Daarom willen zij misschien de takenlijst op terugkerende basis toewijzen.

1. Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.
1. Selecteer de takenlijst die u wilt toewijzen.
1. Selecteer **Proces starten**.
1. Voer in het dialoogvenster **Proces starten** op het tabblad **Algemeen** in het veld **Procesnaam** een naam in.
1. Stel de optie **Terugkeerpatroon** in op **Ja**.
1. Voer in het veld **Verschuiving van doeldatum naar terugkeerpatroon in dagen** een aantal dagen in. Als u bijvoorbeeld **4** invoert, is de doeldatum de terugkeerdatum plus vier dagen.
1. Selecteer op het tabblad **Uitvoeren op de achtergrond** de optie **Terugkeerpatroon**.
1. Voer in het dialoogvenster **Terugkeerpatroon definiëren** de frequentiecriteria in en selecteer vervolgens **OK**.

In de volgende afbeelding ziet u een voorbeeld van het invoeren van frequentiecriteria in het dialoogvenster **Terugkeerpatroon definiëren**.

![Frequentiecriteria invoeren in het dialoogvenster Terugkeerpatroon definiëren.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Status van takenlijst bijhouden

Als u een regiomanager of winkelmanager bent, wilt u mogelijk de status bijhouden van de takenlijsten die zijn toegewezen aan meerdere winkels of werknemers. U kunt vervolgens opvolgingstaken uitvoeren voor winkels of werknemers die hun toegewezen taken niet op tijd hebben voltooid. Via Commerce Back Office kunt u de status van takenlijsten weergeven, taken opnieuw toewijzen of de status van een taak wijzigen.

Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken.

1. Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.
1. Selecteer het tabblad **Alle takenlijsten** om de status weer te geven van alle takenlijsten die aan verschillende winkels zijn toegewezen.

Voer de volgende stappen uit om de status van een takenlijst bij te houden voor alle taken die aan u zijn toegewezen.

1. Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheerprocessen**.
1. Selecteer het tabblad **Mijn taken** of **Alle taken** om de status van taken weer te geven of bij te werken die aan u zijn toegewezen.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van taakbeheer](task-mgmt-overview.md)

[Taakbeheer configureren](task-mgmt-configure.md)

[Takenlijsten maken en taken toevoegen](task-mgmt-create-lists.md)

[Taakbeheer in POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
