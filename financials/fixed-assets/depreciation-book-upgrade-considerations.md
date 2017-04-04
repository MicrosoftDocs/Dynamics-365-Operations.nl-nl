---
title: Afschrijving boek upgrade, overzicht
description: "In eerdere versies zijn er twee waardering concepten voor vaste activa - waardemodellen en afschrijvingsboeken. In versie 1611 van Microsoft Dynamics 365 for Operations zijn functionaliteiten van waardemodellen en afschrijvingsboeken samengevoegd in één concept dat de naam boek draagt. Dit onderwerp bevat enkele overwegingen voor de upgrade."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Afschrijving boek upgrade, overzicht

In eerdere versies zijn er twee waardering concepten voor vaste activa - waardemodellen en afschrijvingsboeken. In versie 1611 van Microsoft Dynamics 365 for Operations zijn functionaliteiten van waardemodellen en afschrijvingsboeken samengevoegd in één concept dat de naam boek draagt. Dit onderwerp bevat enkele overwegingen voor de upgrade. 

Met het upgradeproces verplaatst u uw bestaande instellingen en alle bestaande transacties naar de nieuwe boekstructuur. De waardemodellen worden in de huidige vorm behouden, in de vorm van een boek dat boekt naar het grootboek. Afschrijvingsboeken worden naar een boek verplaatst waarvoor de optie **Boeken naar grootboek** is ingesteld op **Nee**. Afschrijvingsboekjournaalnamen wordt verplaatst naar de naam van een grootboek-journaal met de boekingslaag die zijn ingesteld op **geen**. Transacties met afschrijvingsboeken worden aan vaste-activatransacties verplaatst. 

Voordat u de gegevensupgrade uitvoert, moet u de twee opties begrijpen die beschikbaar zijn om afschrijvingsboekjournaalregels naar transactieboekstukken bij te werken en moet u de nummerreeks begrijpen die voor de boekstuknummering wordt gebruikt. 

Optie 1: **Door het systeem gedefinieerde nummerreeks** - Dit is de standaardoptie om upgradeprestaties te optimaliseren. Bij de upgrade wordt niet het raamwerk voor nummerreeksen gebruikt, maar in plaats daarvan worden boekstukken toegewezen op basis van sets. Na de upgrade de nieuwe nummerreeks worden gemaakt met de **volgende ingesteld** op de juiste wijze op basis van de bijgewerkte transacties. Standaard is de nummerreeks die wordt gebruikt in de FADBUpgr\#\#\#\#\#\#\#\#\# indeling. Er zijn enkele parameters beschikbaar voor u de indeling aanpassen bij het gebruik van deze benadering:

-   **Nummerreekscode** – de code voor de nummerreeks. Deze nummerreekscode kan niet bestaan, omdat deze met de upgrade worden gemaakt.
    -   Naam constante: **NumberSequenceDefaultCode**
    -   Standaardwaarde: "FADBUpgr"
-   **Voorvoegsel** – De tekenreekswaarde voor de constante die als voorvoegsel voor de boekstuknummers wordt gebruikt.
    -   Naam constante: **NumberSequenceDefaultParameterPrefix**
    -   Standaardwaarde: "FADBUpgr"
-   **Alfanumerieke lengte** – De lengte van het alfanumerieke segment van de nummerreeks.
    -   Naam constante: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Standaardwaarde: 9
-   **Beginnummer** - Het eerste nummer dat in de nummerreeks moet worden gebruikt.
    -   Naam constante: ** NumberSequenceDefaultParameterStartNumber **
    -   Standaardwaarde: 1

Optie 2: **bestaande aangepaste nummerreeks** -met deze optie kunt u de nummerreeks moet worden gebruikt voor de upgrade te definiëren. Overweeg het gebruik van deze optie als u geavanceerde nummerreeksconfiguratie nodig. Als u wilt een nummerreeks gebruiken, moet u de upgrade ReleaseUpdateDB70-klasse wijzigen\_FixedAssetJournalDepBookRemovalDepBookJournalTrans met de volgende gegevens:

-   **Nummerreekscode** – De code van de nummerreeks.
    -   Naam constante: ** NumberSequenceExistingCode **
    -   Standaardwaarde: geen standaardwaarde, deze moet worden bijgewerkt naar de nummerreekscode.
-   **Gedeelde nummerreeks** - Een booleaanse waarde om het bereik van de nummerreeks te identificeren. Gebruik 'true' voor gedeelde nummerreeksen tussen alle bedrijven en 'false' voor een bedrijfsspecifiek bereik. Wanneer u 'false', wordt de nummerreeks met de opgegeven naam moet bestaan in elk bedrijf dat transacties met afschrijvingsboeken bevat. Gedeelde nummerreeksen bestaan in elke partitie waarop afschrijvingsboektransacties.
    -   Naam constante: ** NumberSequenceExistingIsShared **
    -   Standaardwaarde: true

De parameters zijn aan het begin van de ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans-klasse. 

*Geef een oplopende benadering van toewijzing van boekstukken*<ph id="t1">
</ph>*/ / klopt, maar als u wilt gebruiken van een bestaande nummerreekscode*<ph id="t2">
</ph>*/ / false, als u wilt gebruiken van het systeem gedefinieerde nummerreeks (standaard)* const boolean NumberSequenceUseExistingCode = ONWAAR;  

*Als de methode met numerieke volgorde systeem gedefinieerde, de parameters voor de nummerreeks opgeven. *<ph id="t3">
</ph>*/ / Een nieuwe nummerreeks met deze parameters wordt gemaakt.* Const str NumberSequenceDefaultCode = 'FADBUpgr'; Const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; int Const NumberSequenceDefaultParameterAlpanumericLength = 9; int Const NumberSequenceDefaultParameterStartNumber = 1;   

*Als met de bestaande numerieke volgorde aanpak geeft u de bestaande nummerreekscode. *<ph id="t4">
</ph>*/ / Toewijzing van boekstukken per rij gaat voor bestaande nummerreeksen.* Const str NumberSequenceExistingCode = ''; */ / Het bereik van de bestaande nummerreekscode opgeven*<ph id="t5">
</ph>*/ / true als de opgegeven nummerreeks wordt gedeeld*<ph id="t6">
</ph>*/ / false als de opgegeven nummerreeks per bedrijf*<ph id="t7">
</ph>*/ / het systeem gedefinieerde standaardnummerreeks wordt gebruikt als een nummerreekscode met het opgegeven bereik is niet gevonden.* const boolean NumberSequenceExistingIsShared = true; 

Herbouw het project dat de klasse bevat nadat de constanten zijn gewijzigd. 

Wanneer u met behulp van het systeem gegenereerde nummer volgorde aanpak (optie 1), wordt de upgrade sets gebaseerde verwerking via de boekstuknummers die is opgegeven in de parameters upgradescript toewijzen. Het maakt ook een nieuwe nummerreeks met opgegeven parameters na de toewijzing. 

Bij gebruik van de door de gebruiker gedefinieerde nummerreeks (optie 2) wordt tijdens de gegevensupgrade gecontroleerd of de nummerreeks met het opgegeven bereik in de database bestaat voor alle partities en bedrijven met afschrijvingsboektransacties. Als deze bestaat, wordt de upgrade per rij verwerking gebruikt de boekstuknummers zoals opgegeven door de nummerreeks die met behulp van het raamwerk voor nummerreeks toewijzen. Als de nummerreeks aan het opgegeven bereik niet bestaat, wordt de upgrade de standaard systeem gedefinieerde numerieke volgorde methode gebruikt voor het toewijzen van de boekstuknummers en maakt u een nieuwe nummerreeks met de opgegeven standaardparameters na de toewijzing.

Bij beide methoden wordt in het gegevensupgradescript ook de nummerreeks voor het veld **Boekstuknummering** gebruikt voor de nieuwe grootboekjournaalnamen die zijn gemaakt voor de voormalige afschrijvingsboekjournaalnamen.


