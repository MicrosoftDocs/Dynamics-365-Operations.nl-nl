---
title: Verlof- en verzuimplannen toerekenen
description: U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3048f9b6b52a150219067430abb54e5b5bf5c3e4
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197308"
---
# <a name="accrue-leave-and-absence-plans"></a>Verlof- en verzuimplannen toerekenen

U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Verlof en verzuim toerekenen voor meerdere werknemers

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimplannen toerekenen**.

3. Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven. Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Informatie over het toerekeningsproces invoeren.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Verlof en verzuim toerekenen voor een werknemer

1. Selecteer **Verlof** in de record van de werknemer.

2. Selecteer **Verlof en verzuim toerekenen**.

3. Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven. Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Informatie over het toerekeningsproces invoeren.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Verlof- en verzuimtoerekeningen verwijderen voor meerdere werknemers

Opbouwrecords voor een specifiek plan en datumbereik verwijderen. Toerekeningsdatums moeten vandaag of in de toekomst gedateerd zijn.

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimtoerekeningen verwijderen**.

3. Selecteer in het dialoogvenster **Verlof- en verzuimtoerekeningen verwijderen** de optie **Verlofplan**. 

4. Kies **Saldocorrecties verwijderen** als dit van toepassing is.

5. Voer een **Toerekeningsdatum voor verlof** in of selecteer deze. Deze datum moet vandaag zijn of in de toekomst liggen. 

6. Selecteer **OK**. Door het toerekeningsproces worden de toerekeningen met de parameters die u hebt ingesteld, verwijderd. 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Verlof- en verzuimtoerekeningen verwijderen voor één werknemer

1. Selecteer **Verlof** in de record van de werknemer.

2. Selecteer **Verlof- en verzuimtoerekeningen verwijderen**.

3. Selecteer in het dialoogvenster **Verlof- en verzuimtoerekeningen verwijderen** de optie **Verlofplan**. 

4. Kies **Saldocorrecties verwijderen** als dit van toepassing is.

5. Voer een **Toerekeningsdatum voor verlof** in of selecteer deze. Deze datum moet vandaag zijn of in de toekomst liggen. 

6. Selecteer **OK**. Door het toerekeningsproces worden de toerekeningen met de parameters die u hebt ingesteld, verwijderd. 

## <a name="review-leave-accrual-and-deletion-processes"></a>Toerekenings- en verwijderprocessen voor verlof controleren

**Controle van toerekening van verlof** wordt steeds weergegeven als u een toerekening uitvoert of verwijdert voor een of alle werk nemers. De datum en de persoon die de actie heeft uitgevoerd, worden ook weer gegeven.

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Verlof beheren** de optie **Controle van toerekening van verlof verwijderen**.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een plan voor verlof en verzuim maken](hr-leave-and-absence-plans.md)
