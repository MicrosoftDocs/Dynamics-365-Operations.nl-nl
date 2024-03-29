---
title: Verlof- en verzuimplannen toerekenen
description: U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.
author: twheeloc
ms.date: 09/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aac35177ca120b1ae1b4759b98278fafadc3e033
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702114"
---
# <a name="accrue-leave-and-absence-plans"></a>Verlof- en verzuimplannen toerekenen

>[!Important]
>De functionaliteit die in dit artikel wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt verlof en verzuim toerekenen in Dynamics 365 Human Resources voor meerdere werknemers of voor een individu.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Verlof en verzuim toerekenen voor meerdere werknemers

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Verlof beheren** de optie **Verlof- en verzuimplannen toerekenen**.

3. Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven. Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u transitorische posten voor alle bedrijven wilt uitvoeren, selecteert u **Alle bedrijven**. Als u transitorische posten voor één verlofplan wilt verwerken, selecteert u **Nee** voor **Alle plannen** en selecteert u vervolgens een **Verlofplan**. Als u alle bedrijven selecteert, kunt u geen afzonderlijk verlofplan selecteren.

5. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

    1. Informatie over het toerekeningsproces invoeren.
    2. Als u een terugkerende taak wilt instellen, selecteert u **Terugkeerpatroon**, voert u de terugkeergegevens in en selecteert u vervolgens **OK**.
    3. Als u een taakwaarschuwing wilt instellen, selecteert u **Waarschuwingen**, selecteert u de waarschuwingen die u wilt ontvangen en selecteert u vervolgens **OK**.
    4. Selecteer **OK**. Het toerekeningsproces wordt uitgevoerd met de parameters die u instelt. 

## <a name="accrue-leave-and-absence-for-an-employee"></a>Verlof en verzuim toerekenen voor een werknemer

1. Selecteer **Verlof** in de record van de werknemer.

2. Selecteer **Verlof en verzuim toerekenen**.

3. Het dialoogvenster **Verlof- en verzuimplannen toerekenen** wordt weergegeven. Selecteer bij **Toerekenen vanaf** **Datum van vandaag** of **Aangepaste datum** en voer een aangepaste datum in.

4. Als u transitorische posten voor alle bedrijven wilt uitvoeren, selecteert u **Alle bedrijven**. Als u transitorische posten voor één verlofplan wilt verwerken, selecteert u **Nee** voor **Alle plannen** en selecteert u vervolgens een **Verlofplan**. Als u alle bedrijven selecteert, kunt u geen afzonderlijk verlofplan selecteren.

5. Als u het toerekeningsprocedure op de achtergrond wilt uitvoeren, selecteert u **Uitvoeren op de achtergrond** en voert u de volgende taken uit:

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

## <a name="leave-accrual-rounding"></a>Afronding voor verloftoerekening
Wanneer een werknemer wordt geregistreerd of uitgeschreven, wordt de afronding van de verloftoerekening omgeslagen. Eerder was afronding alleen toegestaan wanneer een verlofplan werd ingesteld op verdeling naar rato, en een werknemer tijdens een periode werd in- of uitgeschreven. Verloftoerekeningen worden nu afgerond, ongeacht de in-/uitschrijving die in het midden of aan het begin van een periode plaatsvindt.

## <a name="leave-accrual-transaction-auditing"></a>Controleren van toerekeningstransacties voor verlof

Met deze functie begrijpen verzuim- en verlofmanagers de toerekeningstransacties voor verlof en verzuim die betrekking hebben op de verlofsaldi van een werknemer voor een bepaald verloftype.

Transactiedetails weergeven:

1. Selecteer **Verlof** in de record van de werknemer.

2. Selecteer **Verlof weergeven** en selecteer vervolgens het tabblad **Saldi**.

Als u de toerekeningstransacties wilt weergeven die zijn gerelateerd aan een bepaald type verlof, selecteert u de numerieke waarde in de kolom **Huidig saldo**.

Als u de transactiedetails voor een specifiek toerekeningsbedrag wilt weergeven, selecteert u een toerekeningsrij, opent u het venster **Verwante informatie** aan de rechterkant en opent u vervolgens de sectie **Transactiedetails**. In de sectie Transactiedetails wordt het volgende weergegeven:

- Wijzigingen in het saldo van het verloftype van de werknemer
- Details van het dienstverband voor de opgegeven toerekeningsperiode.
- Details over de toerekeningsperiode en -tarieven
- Eventuele wijzigingen in de verlofplanconfiguraties

![Controle van toerekeningstransacties voor verlof weergeven.](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>Zie ook

[Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)</br>
[Een plan voor verlof en verzuim maken](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
