---
title: Een werktijdkalender maken
description: Definieer een werktijdkalender, feestdagen en vrije tijd in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 163d7caf516d791fa54e2518d19798bdf3d58d3d
ms.sourcegitcommit: 67c4ed957e43d4d60bb609d93921a0be9619e675
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2022
ms.locfileid: "8509607"
---
# <a name="create-a-working-time-calendar"></a>Een werktijdkalender maken


> [!Important]
> De functionaliteit die in dit onderwerp wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

1. Selecteer op de pagina **Organisatiebeheer** de optie **VRIJE TIJD**.

2. Selecteer **Nieuw** en voer een naam en tijdbereik in voor de vrije tijd.

Als u de preview-functie van Verlof en verzuim voor correcties voor feestdagen hebt ingeschakeld, gebruikt Human Resources feedsdagen en sluitingsdatums om het aantal dagen te bepalen dat moet worden aangepast voor werknemers die zijn ingeschreven in de kalender.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)
- [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
