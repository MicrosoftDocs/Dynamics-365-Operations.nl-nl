---
title: Een werknemer inschrijven voor een vaste honoreringsregeling
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc8373a4a39a1a212ab445b2b300fbddfe0e4a39
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112087"
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

