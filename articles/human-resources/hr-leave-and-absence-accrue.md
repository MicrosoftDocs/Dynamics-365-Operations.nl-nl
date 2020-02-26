---
title: Verlof- en verzuimplannen toerekenen
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 28b7d843d9dd652e45c24af09d0414530c06c4ac
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008603"
---
# <a name="accrue-leave-and-absence-plans"></a>Verlof- en verzuimplannen toerekenen

U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Verlof en verzuim toerekenen voor meerdere werknemers

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimplannen toerekenen**.

3. Selecteer in het dialoogvenster **Verlof- en verzuimplannen toerekenen**, in **Toerekenen vanaf** de optie **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Informatie over het toerekeningsproces invoeren.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.

## <a name="accrue-leave-and-absence-for-an-employee"></a>Verlof en verzuim toerekenen voor een werknemer

1. Selecteer **Verlof** in de record van de werknemer.

2. Selecteer **Verlof en verzuim toerekenen**.

3. Selecteer in het dialoogvenster **Verlof- en verzuimplannen toerekenen**, in **Toerekenen vanaf** de optie **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

   1. Informatie over het toerekeningsproces invoeren.

   2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u **OK**.

   3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.

   4. Selecteer **OK**. Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt.

## <a name="preview-features-for-leave-and-absence"></a>Preview-functies voor Verlof en verzuim

[!include [banner](includes/preview-feature-leave-absence.md)]

U kunt de volgende preview-functies inschakelen voor Verlof en verlof:

- **Verlof- en verzuimtoerekeningen verwijderen**. Opbouwrecords voor een specifiek plan en datumbereik verwijderen. Toerekeningsdatums moeten vandaag of in de toekomst gedateerd zijn.

- **Controle van toerekening van verlof**. Hiermee wordt elke keer weergegeven dat iemand een toerekening uitvoert of verwijdert voor een of alle werknemers, samen met de datum en de persoon die de actie heeft uitgevoerd.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Een verlof- en verzuimplan maken](hr-leave-and-absence-plans.md)