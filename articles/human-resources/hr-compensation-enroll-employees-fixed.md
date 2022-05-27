---
title: Een werknemer inschrijven voor een vast compensatieplan
description: De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688736"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Een werknemer inschrijven voor een vaste honoreringsregeling


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

De manager Compensatie en emolumenten kan werknemers toewijzen aan vaste compensatieplannen om hun basissalaris te beheren. Bij deze procedure wordt ervan uitgegaan dat een vast plan is gemaakt en actief is, en dat beschikbaarheidregels zijn ingesteld voor het plan. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. U kunt beginnen met de procedure door naar **Human resources** > **Werknemers** > **Werknemers** > **Compensatie** > **Vast plan** te gaan.

1. Klik op **Nieuw**.
2. Selecteer in het veld **Actie** een actie Vaste compensatie van het type **Inhuren/opnieuw inhuren** om de wijziging in de compensatie van de werknemer te beschrijven.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Klik in het veld **Positie** op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Het niveau dat wordt weergegeven is van het sneltabblad **Compensatie** > **Niveau** van de **Taak** die is toegewezen aan de **Positie**. Het niveau moet worden ingesteld op de taak voordat compensatie kan worden toegewezen aan de werknemer.  
6. Selecteer in het veld **Plan** het vaste compensatieplan voor de werknemer. De zoekopdracht **Plan** wordt gefilterd om alleen de plannen weer te geven waarvoor de werknemer in aanmerking komt op basis van de **Geschiktheidsregels**.
7. Zoek en selecteer de gewenste record in de lijst.
    * De **ingangsdatum** en de **vervaldatum** voor de compensatie worden standaard ingesteld op de begin- en einddatum voor de positietoewijzing van de werknemer. U kunt deze datums indien nodig wijzigen.  
    * Als het Vastecompensatieplan een stappenplan is, selecteert u de stap die het juiste salaristarief voor de werknemer bevat. Als het vastecompensatieplan een schaal- of bandplan is, voert u het salaristarief voor de werknemer in. Het salaristarief wordt gevalideerd op basis van de tolerantie-instellingen voor het plan en de minimale en maximale referentiepunten voor het compensatieniveau van de taak.  
8. Klik op **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
