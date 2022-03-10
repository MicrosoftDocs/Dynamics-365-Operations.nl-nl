---
title: Gereed voor betaling
description: In dit onderwerp wordt weergegeven hoe u een werknemer als gereed voor betaling kunt markeren in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 08/25/2021
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
ms.openlocfilehash: 825aa327cc1530675fad57be6fc1b4313f0cf998
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068965"
---
# <a name="ready-to-pay"></a>Gereed voor betaling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Als u een werknemer als gereed voor betaling wilt markeren, moet u eerst de functionaliteit **(Preview) Integratie van salarisadministratie** in functiebeheer inschakelen. Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).

Met deze functie kunnen HR-prefessionals inzicht krijgen in welke werknemers gereed zijn voor salarisverwerking en voor wie actie vereist is voordat ze door een externe salarisverlener worden verwerkt.

## <a name="mark-employee-as-ready-to-pay"></a>Werknemer markeren als gereed voor betaling

Het verzamelen en valideren van werknemersgegevens kan tijdrovend en foutgevoelig zijn. Door HR-professionals in staat te stellen om werknemersgegevens te controleren en eenvoudig bij te werken, helpt Dynamics 365 Human Resources u de tijd beperken die wordt besteed aan het verwerken van salarissen.

Een werknemer markeren als gereed voor betaling:

1. Open **Compensatiebeheer**. De werkruimte bevat twee tegels: 
    - **Werknemers die gereed zijn voor betaling**
    - **Werknemers die gereed zijn voor betaling**
    ![Werkruimte Compensatiebeheer.](./media/hr-ready-to-pay-1-workspace.png)

2. Selecteer de tegel **Werknemers die gereed zijn voor betaling**.

3. Selecteer de werknemers die moeten worden gevalideerd. Selecteer **Valideren** op het tabblad **Salaris** in de groep **Gereed voor betaling**.
    ![Valideer werknemers.](./media/hr-ready-to-pay-2-validate.png)

4. Als u de resultaten wilt bekijken, selecteert u **Resultaten** op het tabblad **Salaris** in de groep **Gereed voor betaling**.

## <a name="validation"></a>Validatie

Voordat een werknemer wordt gemarkeerd als gereed voor betaling, wordt het profiel van de medewerker gevalideerd op volledigheid.

![Valideer resultaten.](./media/hr-ready-to-pay-3-results.png)

| Validatie | Gegevens |
| --- | --- |
| **Parameter van adresdoel** | Bevestigt dat de parameter **Doel adressen salarisadministratie gebruiken** is geselecteerd. |
| **Adres salarisadministratie** | Bevestigt dat het werknemerprofiel ten minste één adres heeft met het doel **Salarisplaats** of **Salariswerklocatie** en er slechts één adres per doel is. |
| **Dienstverband** | Bevestigt dat de werknemer ten minste één dienstverband heeft (huidig, vorig of toekomstig). |
| **Identificatienummer** | Bevestigt dat het veld **Identificatietypen gebruiken in salarisverwerking** is ingesteld op **Ja** op de pagina **Human Resources-parameters**, en dat het identificatietype dat is aangegeven in de parameter, is ingevuld in het werknemersprofiel. |
| **Voornaam en achternaam** | Bevestigt dat de velden **Naam** en **Achternaam** zijn ingevuld.|
| **Locatie** | Bevestigt dat aan de werknemer een positie is toegewezen. |
| **Geboortedatum** | Bevestigt dat het veld **Verjaardag** is ingevuld. |
| **Compensatie** | Bevestigt dat de werknemer bij een plan voor vaste compensatie is ingeschreven. |

Als een van deze validaties mislukt, kunt u de werknemer niet als gereed voor betaling markeren.

Als het veld **Gereed voor betaling** de waarde **Nee** heeft, geeft dit aan dat u een actie moet uitvoeren om ervoor te zorgen dat het werknemerprofiel is voltooid. Hiermee wordt niet voorkomen dat de gegevens beschikbaar worden gemaakt in een gegevensentiteit. 

## <a name="process-automation"></a>Procesautomatisering

U kunt de validatie van alle werknemers automatiseren door [Procesautomatisering](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation) te gebruiken. Ga in de werkruimte **Compensatiebeheer** naar **Koppelingen** \> **Parameters** \> **Procesautomatiseringen**.

## <a name="see-also"></a>Zie ook

[Inleiding bij API voor integratie van salarisadministratie](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
