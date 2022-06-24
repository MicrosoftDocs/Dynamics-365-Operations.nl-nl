---
title: Parameters voor het beheer van technische wijzigingen
description: In dit artikel wordt uitgelegd hoe u functies van technisch wijzigingsbeheer voor Microsoft Dynamics 365 Supply Chain Management configureert.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6ef4113077c538ca1a54009aacbdeaf2ccbd0232
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875505"
---
# <a name="engineering-change-management-parameters"></a>Parameters voor het beheer van technische wijzigingen

[!include [banner](../includes/banner.md)]

De pagina **Parameters voor technisch wijzigingsbeheer** bevat instellingsparameters waarmee het standaardgedrag wordt gewijzigd dat is gerelateerd aan de processen voor het vrijgeven van de productstructuur en het beheer van technische wijzigingen.

## <a name="open-the-engineering-change-management-parameters-page"></a>De pagina Parameters voor technisch wijzigingsbeheer openen

U opent de pagina **Parameters voor technisch wijzigingsbeheer** door te gaan naar **Technisch wijzigingsbeheer \> Instellingen \> Parameters voor technisch wijzigingsbeheer**. U kunt de velden vervolgens instellen zoals is beschreven in de overige secties van dit artikel.

## <a name="release-control-tab"></a>Het tabblad Vrijgavebeheer

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Vrijgavebeheer** van de pagina **Parameters voor technisch wijzigingsbeheer**. Deze velden zijn van invloed op het vrijgaveproductstructuurproces.

| Veld | Beschrijving |
|---|---|
| Artikelnummerregel | Selecteer hoe het artikelnummer moet worden gedefinieerd wanneer het product aan een rechtspersoon wordt vrijgegeven. Selecteer *Nummer technisch product* als het productnummer in de ontvangende rechtspersoon moet overeenkomen met het productnummer in het technisch bedrijf. Selecteer *Nummerreeks lokaal artikel* als het product het volgende nummer in de nummerreeks voor productnummers in de ontvangende rechtspersoon moet krijgen. |
| Regel voor stuklijstnaam | Geef op hoe de naam van de stuklijst wordt gedefinieerd wanneer het product wordt ontvangen (vrijgegeven) in een rechtspersoon. Selecteer *Technische naam* of het *Ontvangend artikelnummer*. |
| Regel voor routenaam | Geef op hoe de routenaam wordt gedefinieerd wanneer de route van het product wordt ontvangen (vrijgegeven) in een rechtspersoon. Selecteer *Technische naam* of het *Ontvangend artikelnummer*. |
| Stuklijstcontrole uitvoeren | Geef op of er een stuklijstcontrole wordt uitgevoerd wanneer het product wordt ontvangen (vrijgegeven) in een rechtspersoon. |
| Gedrag bij vrijgave van inactieve stuklijst | Geef op of een product kan worden vrijgegeven als het een inactieve stuklijst heeft. Selecteer *Accepteren*, *Alleen waarschuwing* of *Niet toegestaan*. |
| Gedrag bij vrijgave van inactieve route | Geef op of een product kan worden vrijgegeven als het een inactieve route heeft. Selecteer *Accepteren*, *Alleen waarschuwing* of *Niet toegestaan*.|
| Productacceptatie | Geef op of een aanvullende stap voor acceptatie vereist is voordat het product in de rechtspersoon kan worden vrijgegeven. Selecteer *Handmatig* om de acceptatiestap toe te voegen. In dit geval worden de producten weergegeven op de pagina **Openstaande productreleases**. Selecteer *Automatisch* om het product direct op de pagina **Vrijgegeven producten** weer te geven in de doelrechtspersoon nadat het product is vrijgegeven in combinatie met de productstructuur van de vrijgave. |

## <a name="engineering-change-management-tab"></a>Het tabblad Technisch wijzigingsbeheer

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Technisch wijzigingsbeheer** van de pagina **Parameters voor technisch wijzigingsbeheer**. Deze instellingen zijn van invloed op het proces van het beheer van technische wijzigingen.

| Veld | Beschrijving |
|---|---|
| Categorie | De standaardcategorie die wordt gebruikt wanneer een aanvraag voor een technische wijziging wordt gemaakt. |
| Prioriteit | De standaardprioriteit die wordt gebruikt wanneer een aanvraag voor een technische wijziging wordt gemaakt. |
| Regel voor ernstcategorie | Geef op hoe de ernst van een order voor een technische wijziging moet worden vastgesteld. Selecteer *Handmatig* als de gebruiker een waarde moet invoeren in het veld **Ernst**. Selecteer *Berekenen* als u wilt dat de waarde van het veld **Ernst** wordt berekend wanneer u **Ernst berekenen** selecteert in het actievenster van de order voor technische wijzigingen. In dit geval worden de prioriteitsregels gebruikt die zijn gedefinieerd op de pagina **Regelset voor ernst**. Selecteer *Automatisch berekenen* als u de waarde van het veld **Ernst** automatisch wilt laten berekenen en invullen op basis van de regelsets voor de ernst. |
| Betrokken producten opnieuw vrijgeven | Dit veld is van toepassing wanneer u producten opnieuw vrijgeeft via een order voor technische wijzigingen. U kunt opgeven of alle producten of alleen de getroffen producten moeten worden voorgesteld in het dialoogvenster **Releases**. |
| Vrij te geven stuklijstniveaus | De diepte van het stuklijstniveau dat moet worden vrijgegeven. Als de stuklijst meer niveaus heeft (dieper is) dan de waarde die hier is opgegeven, worden alleen de niveaus vrijgegeven die tot aan de opgegeven waarde zijn doorgegeven. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]