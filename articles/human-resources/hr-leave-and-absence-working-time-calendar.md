---
title: Een werktijdkalender maken
description: Definieer een werktijdkalender, feestdagen en vrije tijd in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ccf7901ebbea655b7f795a48944c6f03f9cf210a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115097"
---
# <a name="create-a-working-time-calendar"></a>Een werktijdkalender maken

Een werktijdkalender in Dynamics 365 Human Resources toont de dagen en uren die werknemers in uw organisatie werken. Wanneer een werknemer een verlofaanvraag indient, hoeft hij of zij zich geen zorgen te maken over feestdagen en sluitingen.

Voor het stroomlijnen van verlofaanvragen configureert u deze items voor uw organisatie:

- Werktijdkalender
- Feestdagen en sluitingen
- Vrije tijd

U kunt de laatste twee items toevoegen terwijl u een werktijdkalender instelt. U kunt deze ook afzonderlijk configureren of bijwerken.

## <a name="set-up-a-working-time-calendar"></a>Een werktijdkalender instellen

Stel minimaal één werktijdkalender in waarin uw dagen en werktijden worden weergegeven. Als u locaties hebt in meerdere landen en regio's, kunt u een werktijdkalender instellen voor elk gebied.

1. Selecteer op de pagina **Organisatiebeheer** de optie **Kalenders**.

2. Selecteer **Nieuw** en geef een naam en beschrijving op voor uw kalender.

3. Selecteer onder **Opties voor genereren** de werkdagen voor uw organisatie en geef werktijden op. 
   - Als u een feestdag of sluiting wilt toevoegen, selecteert u de knop **Toevoegen** naast **Feestdagen en sluitingen**.
   - Als u vrije tijd wilt toevoegen, zoals lunchen of pauzes, selecteert u **Toevoegen** onder **VRIJE TIJD** en voert u de naam en het tijdsbereik in.

4. Selecteer onder **Dagen** de optie **Genereren** om de dagen in uw kalender te genereren. Voer het datumbereik voor uw kalender in en selecteer vervolgens **Dagen genereren**.

5. Als u werkschema's wilt toevoegen, selecteert u onder **Werkschema** de optie **Toevoegen** en voert u vervolgens de tijden voor elke werkplanning in.

## <a name="configure-holidays-and-closures"></a>Feestdagen en sluitingen configureren

U kunt vrije dagen en sluitingen apart van een werktijdkalender toevoegen of wijzigen.

1. Selecteer op de pagina **Organisatiebeheer** de optie **Feestdagen en sluitingen**.

2. Selecteer **Nieuw** en geef een naam en datum op voor de feestdag of sluiting.

## <a name="configure-non-work-time"></a>Vrije tijd configureren

U kunt vrije tijd apart van een werktijdkalender toevoegen of wijzigen.

1. Selecteer op de pagina **Organisatiebeheer** de optie **Vrije tijd**.

2. Selecteer **Nieuw** en voer een naam en tijdbereik in voor de vrije tijd.

Als u de preview-functie van Verlof en verzuim voor correcties voor feestdagen hebt ingeschakeld, gebruikt Human Resources feedsdagen en sluitingsdatums om het aantal dagen te bepalen dat moet worden aangepast voor werknemers die zijn ingeschreven in de kalender.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)
