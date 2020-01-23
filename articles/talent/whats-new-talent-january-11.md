---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (11 januari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899169"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent - Core HR (11 januari 2019)

**Build 8.1.2100**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="changes"></a>Wijzigingen

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>Verlofaanvragen valideren door het beschikbare saldo te voorspellen
Met wijzigingen die in deze versie zijn aangebracht, kunnen werknemers toekomstig verlof aanvragen zonder dat dit van hun huidige saldo wordt afgetrokken. Standaardwerkstromen worden gebruikt voor alle toekomstige aanvragen. Zie voor meer informatie [Verlof toerekenen op basis van gewerkte uren](leave-accrue-hours-worked.md).

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>Verwacht verlofsaldo in Selfservice werknemer en Mensen weergeven
Met deze functie kunnen saldi voor toekomstige verlofperioden door HR, managers en werknemers worden weergegeven. Werknemers kunnen toekomstige saldi bekijken in het werkgebied **Selfservice werknemer** en HR heeft toegang tot dezelfde informatie met het werkgebied **Mensen**.

### <a name="notifications-for-changing-leave-balances"></a>Meldingen voor het wijzigen van verlofsaldi
Verlofsaldi geven het huidige saldo van de werknemers weer. Toekomstige saldi zijn beschikbaar in de werkgebieden **Selfservice werknemer** en **Mensen** door een 'vanaf datum' in te voeren om het verwachte saldo te berekenen.

Er is navigatie toegevoegd om de verwachte saldi weer te geven in de volgende gebieden:
  - **Verlof**-kaart in het werkgebied **Selfservice werknemer**.
  - **Verlof en verzuim**-kaart in het werkgebied **Selfservice manager**.
  - **Verlof en verzuim**-pagina in het werkgebied **Mensen**.

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>Decimalen voor variabele compensatieplannen (plannen contant geld) toestaan
Variabele toekenningen en plannen voor contant geld hebben nu extra flexibiliteit voor bedragen en overschrijvingen voor waarden met decimale bedragen.

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>De datums in variabele compensatie-inschrijvingen kunnen niet worden gewijzigd nadat het plan is opgeslagen
Door deze wijziging kan de einddatum van het plan worden bijgewerkt (verlengen of op verlopen instellen) nadat het plan is opgeslagen. U kunt plannen nog steeds activeren of deactiveren onafhankelijk van de begin- en einddatums.

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>Salarisinformatie beschikbaar wanneer de beveiligingsrol Salarisadministrateur is toegewezen
De rol Salarisadministrateur is bijgewerkt zodat deze rol toegang geeft tot de salarisgegevens tijdens het aanvraagproces.

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Selfservice werknemer | Bovenliggend knooppunt kan niet vanuit tegel worden opgehaald bij inzoomen op positiehiërarchie
Er zijn wijzigingen aangebracht zodat een fout is opgelost die optrad bij het toevoegen van de positiehiërarchie aan nieuwe werkgebieden en bij het navigeren binnen de organisatiestructuur.

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>Nieuw validatiebericht wanneer nummerreeks van personeel in gebruik is
Er is een wijziging aangebracht om duidelijk te maken wat het probleem is wanneer u een werknemer in dienst neemt en het volgende personeelsnummer in gebruik is.

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>Werkgebied Selfservice werknemer geselecteerd als eerste opstartpagina
Wanneer het werkgebied **Selfservice werknemer** is geselecteerd als de eerste opstartpagina voor een gebruiker en die gebruiker is niet aan de werknemersrol toegewezen, wordt omgeleid naar het standaarddashboard.

### <a name="termination-reason-code-updates-position-assignment-record"></a>Met redencode voor ontslag wordt de positietoewijzingsrecord bijgewerkt
Met de redencode voor ontslag wordt de positietoewijzing nu bijgewerkt wanneer de aanstelling van een werknemer en de positie worden beëindigd. 
