---
title: Een werknemer inschrijven voor een vaste honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 843db6bc133382a701d4b25b164794e57df152c7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008694"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Een werknemer inschrijven voor een vaste honoreringsregeling

De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren. Bij deze procedure wordt ervan uitgegaan dat een vast plan is gemaakt en actief is, en dat beschikbaarheidregels zijn ingesteld voor het plan. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. U kunt beginnen met de procedure door naar Human resources > Werknemers > Werknemers > Compensatie > Vast plan te gaan

1. Klik op Nieuw.
2. Selecteer in het veld Actie een actie Vaste compensatie van het type Inhuren/opnieuw inhuren om de wijziging in de compensatie van de werknemer te beschrijven.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het veld Positie op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het niveau dat wordt weergegeven is van het Compensatieniveau van de taak op de positie. Het niveau moet worden ingesteld op de taak voordat compensatie kan worden toegewezen aan de werknemer.  
6. Selecteer in het veld Plannen het vastecompensatieplan voor de werknemer. De zoekopdracht voor het plannen wordt gefilterd om alleen de plannen weer te geven waarvoor de werknemer in aanmerking komt op basis van de beschikbaarheidregels.
7. Zoek en selecteer de gewenste record in de lijst.
    * De ingangsdatum en vervaldatum voor de compensatie wordt standaard ingesteld op de begin- en einddatum voor de positietoewijzing van de werknemer. U kunt deze datums indien nodig wijzigen.  
    * Als het Vastecompensatieplan een stappenplan is, selecteert u de stap die het juiste salaristarief voor de werknemer bevat. Als het vastecompensatieplan een schaal- of bandplan is, voert u het salaristarief voor de werknemer in. Het salaristarief wordt gevalideerd op basis van de tolerantie-instellingen voor het plan en de minimale en maximale referentiepunten voor het compensatieniveau van de taak.  
8. Klik op OK.

