---
title: Jaarafsluiting
description: In dit artikel worden de vereiste instellingen en stappen beschreven voor het uitvoeren van het jaarafsluitingsproces van het grootboek.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032c572ec7b29bb6b2823ddde0c4fa76e5f8fcf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883208"
---
# <a name="year-end-close"></a>Jaarafsluiting

[!include [banner](../includes/banner.md)]

In dit artikel worden de vereiste instellingen en stappen beschreven voor het uitvoeren van het jaarafsluitingsproces van het grootboek.

Aan het einde van een boekjaar moet u het jaarafsluitingsproces uitvoeren om beginsaldi naar het nieuwe jaar over te brengen. De meeste organisaties voeren het jaarafsluitingsproces meerdere keren uit. Bij de eerste uitvoering worden de saldi naar het nieuwe fiscale jaar verplaatst. Het proces kan vervolgens opnieuw of zo vaak als nodig is worden uitgevoerd om de saldi van correctieposten naar het nieuwe fiscale jaar te verplaatsen.

Tijdens het jaarafsluitingsproces worden er twee typen mogelijke transacties gemaakt. Er wordt altijd een openingstransactie gegenereerd en deze wordt gebruikt voor het maken van de beginsaldi in het nieuwe boekjaar. De openingstransactie laat de balansgrootboekrekeningsaldi in het nieuwe boekjaar zien en de saldi van de winst- en verliesgrootboekrekeningsaldi in de grootboekrekening voor ingehouden winsten in het nieuwe boekjaar. De afsluittransactie wordt desgewenst gemaakt om de saldi van de winst- en verliesrekeningen op nul te brengen in het boekjaar dat wordt afgesloten.

## <a name="prepare-to-run-the-year-end-close"></a>Voorbereidingen voor het jaarafsluitingsproces

Voordat u het jaarafsluitingsproces uitvoert, moet u de instellingen valideren voor het volgende:

Op de pagina **Hoofdrekening**:

- Controleer of het veld **Hoofdrekeningtype** voor elke hoofdrekening juist is ingesteld. Het hoofdrekeningtype bepaalt of het saldo van de hoofdrekening wordt aangevoerd als een beginsaldo of wordt afgesloten in ingehouden winsten in de openingstransactie.
- Het saldo van de hoofdrekening kan worden overgebracht naar een nieuwe hoofdrekening tijdens de jaarafsluiting. Voer de nieuwe hoofdrekening in het veld **Openingsrekening** in. Meestal wordt dit veld gebruikt voor balanshoofdrekeningen wanneer de hoofdrekening is uitgeschakeld en een nieuwe hoofdrekening wordt gebruikt voor het nieuwe fiscale jaar.

Op de pagina **Grootboekparameters** onder **Afsluiting boekjaar**:

- De optie **Bestaande jaarafsluitingsposten verwijderen bij het opnieuw afsluiten van het jaar** wordt gebruikt om op te geven of de door het systeem gegenereerde openingstransactie uit een vorige jaarafsluiting moet worden verwijderd wanneer de jaarafsluiting opnieuw wordt uitgevoerd. Als deze optie wordt ingesteld op **Ja**, wordem de vorige openings- en optionele afsluittransacties verwijderd en wordt er een nieuwe openings- of afsluittransactie gemaakt op basis van de huidige saldi. Als deze optie is ingesteld op **Nee**, blijft de vorige openings- en optionele afsluittransactie behouden en wordt er een extra openings- of afsluittransactie gemaakt om de saldi te transporteren via correctietransacties die zijn geboekt na de vorige jaarafsluiting.
- De optie **Afsluittransacties tijdens overboeken maken** wordt gebruikt om afsluittransacties te maken in het fiscale jaar dat wordt afgesloten om de saldi van alle hoofdrekeningen op 0 (nul) te brengen. Als deze optie wordt ingesteld op **Ja**, worden zowel de openingstransactie als de afsluittransactie gemaakt. Als deze optie wordt ingesteld op **Nee**, wordt alleen de openingstransactie gemaakt in het volgende fiscale jaar om de saldi over te boeken. De saldi van hoofdrekening blijven aan het einde van het boekjaar.
- De optie **Status boekjaar instellen op definitief afgesloten** wordt gebruikt om het boekjaar in te stellen op een permanent afgesloten status. Gebruik deze optie zorgvuldig, omdat perioden met de status Permanent afgesloten niet opnieuw kunnen worden geopend. Daarom kunnen correcties niet voor het fiscale jaar worden geboekt. U kunt deze optie het beste op **Nee** instellen.
- De optie **Boekstuknummer moet worden ingevuld** is verwijderd. Er is nu een boekstuk vereist wanneer het jaarafsluitingsproces wordt uitgevoerd. Op dat moment wordt het boekstuknummer handmatig ingevoerd.

Op de pagina **Fiscale kalender**:

- Het volgende fiscale jaar moet aanwezig zijn voordat de jaarafsluiting wordt uitgevoerd. Anders kunnen de openingssaldi niet worden gemaakt in de openingsperiode.

Op de pagina **Grootboekkalender**:

- Optioneel: elke boekperiode voor het fiscale jaar dat wordt afgesloten, kan worden ingesteld op **In wachtstand** om te voorkomen dat nieuwe transacties worden ingevoerd. Wanneer correctiegegevens worden geïdentificeerd, worden de geblokkeerde perioden heropend zodat correctieposten kunnen worden geboekt, zelfs als het jaarafsluitingsproces al is uitgevoerd.

Op de pagina **Configuratie van de jaarafsluitingssjabloon**:

- Wanneer de functie **Verbeteringen voor jaarultimoverwerking van grootboek** is ingeschakeld, wordt het instellen van de jaarafsluitingssjabloon gescheiden van het proces voor het uitvoeren van de jaarafsluiting. De sjabloon kan worden gedefinieerd op de pagina **Configuratie van de jaarafsluitingssjabloon** (**Grootboek \> Grootboekinstellingen \> Configuratie van de jaarafsluitingssjabloon**) of kan deze worden geopend vanuit het jaarafsluitingsproces.

## <a name="define-year-end-close-templates"></a>Sjablonen voor jaarafsluiting definiëren

Nadat het systeem is geconfigureerd, kan het jaarafsluitingsproces worden uitgevoerd. Op de pagina **Configuratie van de jaarafsluitingssjabloon** kan een sjabloon worden gedefinieerd voor de groep rechtspersonen waarvoor het jaarafsluitingsproces wordt uitgevoerd. De sjabloon wordt bij elke jaarafsluiting opnieuw gebruikt, maar kan worden gewijzigd als uw organisatie verandert.

Stel eerst het veld **Groepsnaam** voor de sjabloon in en selecteer de fiscale kalender. Met de groepsnaam moet de groep van inbegrepen rechtspersonen worden geïdentificeerd. Wanneer u de groepen rechtspersonen bepaalt, moet u onthouden dat rechtspersonen alleen in dezelfde groep kunnen worden opgenomen als dezelfde fiscale kalender voor hen is geselecteerd. De sjablonen kunnen bijvoorbeeld worden ingesteld op basis van geografie, terwijl aparte groepen kunnen worden gemaakt voor Noord-Amerikaanse rechtspersonen, EMEA-rechtspersonen (Europa, het Midden-Oosten en Afrika) en APAC-rechtspersonen (Azië/Pacific).

Vervolgens kunnen de rechtspersonen worden toegevoegd aan de sjabloon. Rechtspersonen kunnen worden toegevoegd door een organisatiehiërarchie te selecteren of door de rechtspersonen te selecteren. Als een organisatiehiërarchie wordt geselecteerd, worden alleen rechtspersonen binnen de hiërarchie waarin de geselecteerde fiscale kalender wordt gebruikt, toegevoegd aan de sjabloon. Als u rechtspersonen wilt toevoegen aan de sjabloon, kunnen alleen rechtspersonen met dezelfde fiscale kalender worden toegevoegd. Dezelfde fiscale kalender is vereist, omdat de jaarafsluiting boekjaar wordt uitgevoerd door een boekjaar te selecteren, die per kalender kan variëren.

Nadat de rechtspersonen zijn toegevoegd, definieert u de hoofdrekeningen voor ingehouden winsten voor elke rechtspersoon.

Het tabblad **Financiële dimensie** wordt gebruikt om te definiëren welke financiële dimensies worden gebruikt in de openingstransactie. Houd er rekening mee dat de instellingen op dit tabblad alleen gelden voor de rechtspersoon die is geselecteerd in het raster **Rechtspersonen**. U moet de instelling voor elke rechtspersoon in het raster herhalen.

De optie **Balansdimensies overboeken** wordt gebruikt om op te geven of de financiële dimensies voor transacties die zijn geboekt naar balansrekeningen, moeten worden ingesteld in de openingstransactie. U kunt deze optie het beste op **Ja** instellen. De instelling voor de balansdimensies heeft geen invloed op bestaande saldi in de grootboekrekeningen voor ingehouden winst. Deze saldi worden bepaald door de winst- en verliesdimensies die in de volgende sectie zijn gedefinieerd. Fiscaal jaar 2019 was bijvoorbeeld het eerste jaar dat werd afgesloten en de optie **Alles sluiten** werd gebruikt om de dimensies **Afdeling** en **Kostenplaats** voor afsluiting te selecteren. In dit geval is er een afzonderlijke winstrekening voor de ingehouden winst gemaakt voor elke combinatie van een afdeling en een kostenplaats. Wanneer de jaarafschrijving wordt uitgevoerd voor fiscaal jaar 2020, blijven de ingehouden opbrengsten van het vorige jaar precies zoals ze zijn geboekt, zelfs als **Balansdimensies overboeken** is ingesteld op **Nee**. Saldi die worden geboekt op ingehouden winst van vorige jaarafsluitingen worden nooit gewijzigd.

De sectie **Verlies- en winstdimensies overboeken** wordt gebruikt om op te geven welke financiële dimensies voor transacties die zijn geboekt naar winst- en verliesrekeningen, worden overgeboekt naar de hoofdrekening van ingehouden winsten. Geef eerst de financiële dimensies aan die relevant zijn voor de geselecteerde rechtspersoon. Deze financiële dimensies omvatten elke financiële dimensie die is geboekt gedurende het jaar, zelfs als de financiële dimensie geen deel uitmaakt van een actieve rekeningstructuur. Definieer vervolgens elke dimensie als **Eén sluiten** of **Alles sluiten**. De standaardoptie is **Alles sluiten**. Met deze optie worden de oorspronkelijke waarden voor financiële dimensies van geboekte transacties behouden en gebruikt voor het maken van de beginsaldi voor de rekening ingehouden winsten. Afzonderlijke beginsaldi voor ingehouden winsten worden gemaakt voor elke unieke combinatie van waarden voor financiële dimensies. Als **Eén sluiten** is geselecteerd, worden alle geboekte transacties die deze financiële dimensie hebben, samengevat in een beginsaldo voor ingehouden winsten voor de dimensiewaarde die is ingevoerd in het veld dat wordt weergegeven na **Eén sluiten**. Stel bijvoorbeeld dat alle transacties voor het fiscale jaar zijn geboekt met de rekeningstructuur **Hoofdrekening - afdeling**. Voor de financiële dimensie **Afdeling** in de sjabloon is **Eén sluiten** geselecteerd en is **100** ingevoerd als dimensiewaarde. Als de totale inkomsten van alle transacties die zijn geboekt naar afdelingen 200, 300 en 400 100.000 zijn, wordt één beginsaldo gemaakt voor **Ingehouden winsten - 100**. Als u **Eén sluiten** selecteert, maar de waarde voor de financiële dimensie leeg laat, worden alle transacties geboekt naar ingehouden winsten en is de dimensiewaarde leeg.

## <a name="run-the-year-end-close-process"></a>Het jaarafsluitingsproces uitvoeren

Nadat de jaarafsluitingssjablonen zijn gemaakt, kunt u het jaarafsluitingsproces starten op de pagina **Jaarafsluiting** (**Grootboek \> Afgesloten periode \> Jaarafsluiting**). Voordat u de jaarafsluiting uitvoert, kunt u nieuwe jaarafsluitingssjablonen toevoegen of bestaande sjablonen wijzigen door **Configuratie van de jaarafsluitingssjabloon** te selecteren om de instellingspagina voor de sjablonen te openen.

Selecteer de jaarafsluitingssjabloon en selecteer vervolgens in het actievenster de optie **Jaarafsluiting uitvoeren**. Selecteer alle rechtspersonen of een subset ervan in de sjabloon waarvoor u de jaarafsluiting uitvoert. Als u de jaarafsluiting voor de eerste keer in een fiscaal jaar uitvoert, selecteert u waarschijnlijk alle rechtspersonen om beginsaldi voor alle rechtspersonen te maken. Als u de jaarafsluiting eerder hebt uitgevoerd, kunt u ervoor kiezen deze alleen opnieuw uit te voeren voor de rechtspersonen waarvoor correctieposten zijn geboekt.

Selecteer vervolgens het fiscale jaar waarvoor u het jaarafsluitingsproces wilt uitvoeren. Als er meerdere afsluitingsperioden bestaan voor de laatste periode van het fiscale jaar, komt het veld **Periodenaam** beschikbaar. U kunt vervolgens de afsluitperiode selecteren die moet worden gebruikt om de afsluittransactie te maken, als de instellingen zijn gedefinieerd voor het maken van de afsluittransactie.

Voer vervolgens een boekstuknummer in. Hetzelfde boekstuknummer wordt gebruikt voor alle rechtspersonen die u hebt geselecteerd voor het jaarafsluitingsproces. Het boekstuknummer wordt niet gegenereerd met behulp van een nummerreeks.

Het jaarafsluitingsproces wordt standaard in de batchmodus uitgevoerd. Nadat u het project hebt gestart, kunt u daarom terugkeren naar andere activiteiten.

Aangezien rekeningstructuren gedurende een fiscaal jaar kunnen veranderen, kan de relevante rekeningstructuur niet altijd worden geïdentificeerd. Daarom worden bij het jaarafsluitingsproces geen rekeningstructuren aangehouden. Wanneer openingstransacties worden gemaakt, worden de saldi aangevoerd met financiële dimensies, zoals is gedefinieerd in de jaarafsluitingssjabloon. De beginsaldiposten kunnen financiële dimensies bevatten die niet meer in de huidige rekeningstructuur voorkomen en segmentcombinaties die niet meer geldig zijn in de huidige rekeningstructuur. Als uw organisatie een financiële dimensie wil uitsluiten voor het beginsaldo van ingehouden winst, definieert u de financiële dimensie als **Eén sluiten** en laat u de dimensiewaarde leeg.

Nadat het proces is voltooid, wordt een record gemaakt voor elke combinatie van een rechtspersoon en een fiscaal jaar. U krijgt alleen records voor rechtspersonen te zien waartoe u toegang hebt. Elke record bevat de systeemdatum en -tijd waarop het proces is uitgevoerd, en een directe koppeling naar de boekstukken die voor de jaarafsluiting zijn gemaakt.

[![Records die zijn gemaakt op het sneltabblad Historie jaarafsluiting van de pagina Jaarafsluiting](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Als u de jaarafsluiting opnieuw uitvoert, ziet u voor elke combinatie van een rechtspersoon en een fiscaal jaar een of meer records, afhankelijk van de instelling van de optie **Bestaande jaarafsluitingsposten verwijderen bij het opnieuw afsluiten van het jaar** op de pagina **Grootboekparameters**:

- Als de optie is ingesteld op **Ja**, wordt het boekstuk voor de vorige jaarafsluiting verwijderd. De record is gemarkeerd als **Omgekeerd** en wordt aangegeven met de datum en tijd waarop de omkering is uitgevoerd. Bovendien wordt de koppeling naar het boekstuknummer verwijderd. Wanneer de jaarafsluiting is voltooid, wordt er een nieuwe record gemaakt voor het nieuwe boekstuk dat wordt gemaakt.
- Als de optie op **Nee** is ingesteld, blijft de record voor de vorige jaarafsluiting behouden, samen met de koppeling naar het boekstuk. Telkens als de jaarafsluiting opnieuw wordt uitgevoerd, wordt een nieuwe record gemaakt, samen met een koppeling naar de nieuwe boekstukken.

## <a name="reverse-the-year-end-close-process"></a>Het jaarafsluitingsproces omkeren

Op de pagina **Jaarafsluiting** kunt u een jaarafsluiting omkeren. Selecteer de record voor de combinatie van een rechtspersoon en een fiscaal jaar die moet worden omgekeerd en selecteer vervolgens **Jaarafsluiting omkeren**. Het omkeringsproces verwijdert alle openings- en afsluitingsboekstukken die zijn gemaakt voor het fiscale jaar. De record is gemarkeerd als **Omgekeerd** en wordt aangegeven met de datum en tijd waarop de omkering is uitgevoerd. Bovendien wordt de koppeling naar het boekstuknummer verwijderd. Net als het jaarafsluitingsproces wordt de omkering in de batchmodus uitgevoerd.

Met een selectievakje **Omgekeerd weergeven** dat boven het raster beschikbaar is, kunt u de records voor omgekeerde jaarafsluitingsprocessen verbergen of weergeven. Wanneer u het proces **Jaarafsluiting omkeren** hebt uitgevoerd, moet u mogelijk het selectievakje **Omgekeerd weergeven** inschakelen om de record weer te geven. U kunt extra filters instellen om andere informatie weer te geven.

[![Het selectievakje Omgekeerd weergeven gebruiken om records voor omgekeerde jaarafsluitingsprocessen te bekijken op de pagina Jaarafsluiting](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Zie [Het grootboek aan het einde van de periode afsluiten](close-general-ledger-at-period-end.md) en [Het boekjaar afsluiten](tasks/close-fiscal-year.md) voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
