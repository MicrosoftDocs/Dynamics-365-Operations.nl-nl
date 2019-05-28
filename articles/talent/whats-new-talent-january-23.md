---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (23 januari 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
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
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f27698c257301f52e5c77eaa8a04ca13a0315825
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517681"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent Core HR (23 januari 2019)

[!include [banner](includes/banner.md)]

**Build 8.1.2121**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="changes"></a>Wijzigingen

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a>Import van vaste compensatie van werknemers werkt niet bij het maken van nieuwe records voor vaste compensatie
Er is een wijziging aangebracht in de entiteit voor vaste compensatie van werknemers om het compensatieniveau tijdens het importeren op te halen. Vóór deze release werd een bericht weergegeven dat het niveau vereist was.

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a>Het veld Minimumsaldo is verwijderd uit het dialoogvenster voor verlofaanvragen
Het veld **Minimumsaldo** is verwijderd uit het dialoogvenster **Verlofaanvraag**. Deze wijziging geldt voor alle gebieden waarin verlof kan worden aangevraagd.

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a>Gegevensupgrade voor compensatieniveaus wordt niet in alle scenario's bijgewerkt
Er is een wijziging aangebracht om het compensatieniveau in plannen voor vaste compensatie bij te werken. Met deze wijziging wordt het compensatieniveau voor vaste plannen ingevuld voor de functie die is toegewezen aan de werknemer.

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a>Salarisinformatie op de pagina Wijzigingen beheren is alleen beschikbaar wanneer is aangemeld als systeembeheerder
Met deze wijziging kunnen werknemers met de rol Salarisadministrateur toegang krijgen tot de salarisgegevens op de pagina **Tijdlijn van wijzigingen > Wijzigingen beheren** voor de functie.

### <a name="job-fields-default-to-positions"></a>Functievelden worden standaard ingesteld op posities
Bij het wijzigen van de functie voor een positie worden functievelden standaard ingesteld op de positie. Een waarschuwingsbericht wordt weergegeven waarin een optie wordt gegeven om de standaardwaarden te accepteren of de bestaande waarden voor deze velden te behouden.

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a>Proeftijd en kalender worden niet weergegeven voor werknemers die voor de toekomst zijn aangenomen.
Met deze wijziging zijn de velden **Proeftijd** en **Kalender** toegevoegd aan de pagina **Wijzigingen beheren** zodat gegevens voor toekomstige en eerdere werknemers kunnen worden ingevoerd.

### <a name="platform-update-23"></a>Platformupdate 23
Kleine correcties zijn opgenomen als onderdeel van platformupdate 23. Zie voor meer informatie [Wat is nieuw of gewijzigd in Dynamics 365 for Finance and Operations platformupdate 23 (januari 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23). 
