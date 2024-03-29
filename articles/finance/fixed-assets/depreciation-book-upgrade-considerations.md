---
title: Overzicht van upgrade van afschrijvingsboeken
description: In dit artikel wordt de huidige boekfunctionaliteit in vaste activa beschreven. Deze nieuwe functionaliteit is gebaseerd de functionaliteit voor waardemodellen, die beschikbaar was in eerdere versies, maar omvat ook alle functionaliteit die voorheen alleen in afschrijvingsboeken beschikbaar was.
author: moaamer
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom:
- "221624"
- intro-internal
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 784ec32ae886ef7ea9342b085f893eeeec761961
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855486"
---
# <a name="depreciation-book-upgrade-overview"></a>Overzicht van upgrade van afschrijvingsboeken

[!include [banner](../includes/banner.md)]

In dit artikel wordt de huidige boekfunctionaliteit in vaste activa beschreven. Deze nieuwe functionaliteit is gebaseerd de functionaliteit voor waardemodellen, die beschikbaar was in eerdere versies, maar omvat ook alle functionaliteit die voorheen alleen in afschrijvingsboeken beschikbaar was. De functionaliteit voor waardemodellen en afschrijvingsboeken zijn samengevoegd tot één concept dat bekend is als een boek. Met de boekfunctionaliteit kunt u één set pagina's, vragen en rapporten gebruiken voor alle vaste-activaprocessen van uw organisatie. In dit artikel komen aan paar onderwerpen aan de orde waar u rekening mee moet houden voordat u de upgrade uitvoert. 

Met het upgradeproces verplaatst u uw bestaande instellingen en alle bestaande transacties naar de nieuwe boekstructuur. De waardemodellen worden in de huidige vorm behouden, in de vorm van een boek dat boekt naar het grootboek. Afschrijvingsboeken worden naar een boek verplaatst waarvoor de optie Boeken naar grootboek is ingesteld op Nee. De journaalnamen van afschrijvingsboeken worden verplaatst naar een grootboekjournaalnaam, waarbij de boekingslaag is ingesteld op Geen. Afschrijvingsboektransacties worden verplaatst naar Vaste-activatransacties.

Voordat u de gegevensupgrade uitvoert, moet u de twee opties begrijpen die beschikbaar zijn om afschrijvingsboekjournaalregels naar transactieboekstukken bij te werken en moet u de nummerreeks begrijpen die voor de boekstuknummering wordt gebruikt.

Optie 1: **Door het systeem gedefinieerde nummerreeks**: dit is de standaardoptie om upgradeprestaties te optimaliseren. Bij de upgrade wordt niet het raamwerk voor nummerreeksen gebruikt, maar in plaats daarvan worden boekstukken toegewezen op basis van sets. Na de upgrade wordt de nieuwe nummerreeks gemaakt waarbij **Volgende nummerset** op de juiste wijze wordt gebaseerd op de bijgewerkte transacties. Standaard is de nummerreeks die wordt gebruikt in de indeling FADBUpgr\#\#\#\#\#\#\#\#\#. Er zijn enkele parameters beschikbaar waarmee u de indeling kunt aanpassen met deze methode:

-   **Nummerreekscode**: de code ter identificatie van de nummerreeks. Deze nummerreekscode kan niet aanwezig zijn, omdat deze met de upgrade wordt gemaakt.
    -   Naam constante: **NumberSequenceDefaultCode**
    -   Standaardwaarde: "FADBUpgr"
-   **Voorvoegsel** – De tekenreekswaarde voor de constante die als voorvoegsel voor de boekstuknummers wordt gebruikt.
    -   Naam constante: **NumberSequenceDefaultParameterPrefix**
    -   Standaardwaarde: "FADBUpgr"
-   **Alfanumerieke lengte** – De lengte van het alfanumerieke segment van de nummerreeks.
    -   Naam constante: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Standaardwaarde: 9
-   **Beginnummer** - Het eerste nummer dat in de nummerreeks moet worden gebruikt.
    -   Naam constante: **NumberSequenceDefaultParameterStartNumber**
    -   Standaardwaarde: 1

Optie 2: **Bestaande, door gebruiker gedefinieerde nummerreeks**: met deze optie kunt u de nummerreeks definiëren die moet worden gebruikt voor de upgrade. Overweeg deze optie te gebruiken als u geavanceerde nummerreeksconfiguratie nodig hebt. Als u een nummerreeks wilt gebruiken, moet u de upgradeklasse ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans wijzigen met de volgende gegevens:

-   **Nummerreekscode** – De code van de nummerreeks.
    -   Naam constante: **NumberSequenceExistingCode**
    -   Standaardwaarde: geen standaardwaarde, deze moet worden bijgewerkt naar de nummerreekscode.
-   **Gedeelde nummerreeks** - Een booleaanse waarde om het bereik van de nummerreeks te identificeren. Gebruik 'true' voor gedeelde nummerreeksen tussen alle bedrijven en 'false' voor een bedrijfsspecifiek bereik. Wanneer u 'false' gebruikt, moet de nummerreeks met de opgegeven naam bestaan in elk bedrijf dat transacties met afschrijvingsboeken bevat. Gedeelde nummerreeksen bestaan in elke partitie die afschrijvingsboektransacties bevat.
    -   Naam constante: **NumberSequenceExistingIsShared**
    -   Standaardwaarde: true

De parameters bevinden zich aan het begin van de klasse ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans. 

*// Geef een gewenste methode voor toewijzing van boekstukken op* 
 *// true, als u een bestaande nummerreekscode wilt gebruiken* 
 *// false, als u de door het systeem gedefinieerde nummerreeks (standaard) wilt gebruiken* const boolean NumberSequenceUseExistingCode = false;  

*// Als de methode met de door het systeem gedefinieerde nummerreeks wordt gebruikt, geeft u de parameters voor de nummerreeks op.*
 *// Er wordt een nieuwe nummerreeks met deze parameters gemaakt.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Als de methode met de bestaande nummerreeks wordt gebruikt, geeft u de bestaande nummerreekscode op.* 
 *// Toewijzing van boekstukken vindt per rij plaats voor bestaande nummerreeksen.* const str NumberSequenceExistingCode = ''; *// Het bereik van de bestaande nummerreekscode opgeven* 
 *// true, als de opgegeven nummerreeks wordt gedeeld* 
 *// false, als de opgegeven nummerreeks per bedrijf geldt* 
 *// De door het systeem gedefinieerde standaardnummerreeks wordt gebruikt als een nummerreekscode met het opgegeven bereik niet wordt gevonden.* const boolean NumberSequenceExistingIsShared = true; 

Herbouw het project dat de klasse bevat nadat de constanten zijn gewijzigd. 

Wanneer u de methode van de door het systeem gegenereerde nummerreeks gebruikt (optie 1), wordt in de upgrade op sets gebaseerde verwerking gebruikt om de boekstuknummers toe te wijzen zoals opgegeven in de upgradescriptparameters. Hiermee wordt ook een nieuwe nummerreeks met opgegeven parameters na de toewijzing gemaakt. 

Bij gebruik van de door de gebruiker gedefinieerde nummerreeks (optie 2) wordt tijdens de gegevensupgrade gecontroleerd of de nummerreeks met het opgegeven bereik in de database bestaat voor alle partities en bedrijven met afschrijvingsboektransacties. Als deze bestaat, wordt in de upgrade verwerking per rij gebruikt om de boekstuknummers toe te wijzen zoals is opgegeven door de nummerreeks die het nummerreeksraamwerk gebruikt. Als de nummerreeks niet bestaat voor het opgegeven bereik, wordt in de upgrade de methode van de standaard door het systeem gedefinieerde nummerreeks gebruikt voor het toewijzen van de boekstuknummers en wordt een nieuwe nummerreeks met de opgegeven standaardparameters na de toewijzing gemaakt.

Bij beide methoden wordt in het gegevensupgradescript ook de nummerreeks voor het veld **Boekstuknummering** gebruikt voor de nieuwe grootboekjournaalnamen die zijn gemaakt voor de voormalige afschrijvingsboekjournaalnamen.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
