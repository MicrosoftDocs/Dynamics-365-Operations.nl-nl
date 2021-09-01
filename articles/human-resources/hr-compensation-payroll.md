---
title: Gereed voor betaling
description: In dit onderwerp wordt weergegeven hoe u een werknemer als gereed voor betaling kunt markeren in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732412"
---
# <a name="ready-to-pay"></a>Gereed voor betaling

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Als u een werknemer als gereed voor betaling wilt markeren, moet u eerst de functionaliteit **(Preview) Integratie van salarisadministratie** in functiebeheer inschakelen. Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).

Met deze functie kunnen HR-prefessionals inzicht krijgen in welke werknemers gereed zijn voor salarisverwerking en voor wie actie vereist is voordat ze door een externe salarisverlener worden verwerkt.

## <a name="mark-employee-as-ready-to-pay"></a>Werknemer markeren als gereed voor betaling

Het verzamelen en valideren van werknemersgegevens kan tijdrovend en foutgevoelig zijn. Door HR-professionals in staat te stellen om werknemersgegevens te controleren en eenvoudig bij te werken, helpt Dynamics 365 Human Resources u de tijd beperken die wordt besteed aan het verwerken van salarissen.

Een werknemer markeren als gereed voor betaling:

1. Open **Compensatiebeheer**. De werkruimte bevat twee tegels. 
    - **Werknemers die gereed zijn voor betaling**
    - **Werknemers die gereed zijn voor betaling**
    ![Werkruimte Compensatiebeheer.](./media/hr-ready-to-pay-1-workspace.png)

2. Selecteer de tegel **Werknemers die gereed zijn voor betaling**.

3. Selecteer de werknemers die moeten worden gevalideerd. Selecteer **Valideren** op het tabblad **Salaris** in de groep **Gereed voor betaling**.
    ![Valideer werknemers.](./media/hr-ready-to-pay-2-validate.png)

4. Als u de resultaten wilt bekijken, selecteert u **Resultaten** op het tabblad **Salaris** in de groep **Gereed voor betaling**.

## <a name="validation"></a>Validatie

Voordat een werknemer wordt gemarkeerd als gereed voor betaling, wordt er een basisvalidatie uitgevoerd op volledigheid van het profiel.

![Valideer resultaten.](./media/hr-ready-to-pay-3-results.png)

De volgende tabel bevat meer informatie over elk van de validaties die worden uitgevoerd. 

| Validatie | Gegevens |
| --- | --- |
| Parameter van adresdoel | Valideert of de parameter **Doel adressen salarisadministratie gebruiken** is ingeschakeld. |
| Adres salarisadministratie | Valideert of het werknemerprofiel ten minste één adres heeft met het doel 'Salarisplaats' of 'Salariswerklocatie' en er slechts één adres per doel is. |
| Dienstverband | Controleer of de werknemer ten minste één dienstverband heeft (huidig, vorig of toekomstig). |
| Identificatienummer | Valideert of de parameter 'Identificatietypen gebruiken in salarisverwerking' ja is en of het identificatietype dat is aangegeven in de parameter is ingevuld in het werknemersprofiel. |
| Voornaam en achternaam | Controleer of het werknemerprofiel geldig is en controleer of de velden **Naam** en **Achternaam** zijn ingevuld.|
| Locatie | Controleer of de werknemer een positie heeft toegewezen. |
| Geboortedatum | Valideert of het werknemerprofiel geldig is en controleert of het veld **Verjaardag** is ingevuld. |
| Compensatie | Controleer of de werknemer bij een plan voor vaste compensatie is ingeschreven. |

Als een van deze validaties mislukt, kunt u de werknemer niet als gereed voor betaling markeren.

Als het veld **Gereed voor betaling** de waarde **Nee** heeft, geeft dit aan dat u een actie moet uitvoeren om ervoor te zorgen dat het werknemerprofiel is voltooid. Hiermee wordt niet voorkomen dat de gegevens beschikbaar worden gemaakt in een gegevensentiteit. 

## <a name="known-issues"></a>Bekende problemen

- U moet de functie **Gestroomlijnde invoer voor werknemers** in functiebeheer uitschakelen. De tegels in de werkruimte voor compensatiebeheer werken niet goed als u deze functie gebruikt.
- In het formulier Werknemer op het tabblad **Salaris** is de groep **Gereed voor betaling** beschikbaar voor elke gebruikersrol. 

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
