---
title: Jaarafsluiting
description: In dit onderwerp worden de vereiste instellingen en stappen beschreven voor het uitvoeren van het jaarafsluitingsproces van het grootboek.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerClosingSheet
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 22233cfa1df79076c8ea42f75ea309bac990d574
ms.lasthandoff: 03/31/2017


---

# <a name="year-end-close"></a>Jaarafsluiting

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de vereiste instellingen en stappen beschreven voor het uitvoeren van het jaarafsluitingsproces van het grootboek. 

Aan het einde van een boekjaar moet u het jaarafsluitingsproces uitvoeren om beginsaldi naar het nieuwe jaar over te brengen. De meeste organisaties voeren het jaarafsluitingsproces meerdere keren uit. De eerste keer worden de saldi naar het nieuwe boekjaar verplaatst. Het jaarafsluitingsproces kan vervolgens nogmaals of zo vaak als nodig is, worden uitgevoerd om de saldi van correctieposten naar het nieuwe boekjaar te verplaatsen. 

Tijdens het jaarafsluitingsproces worden er twee typen mogelijke transacties gemaakt. Er wordt altijd een openingstransactie gegenereerd en deze wordt gebruikt voor het maken van de beginsaldi in het nieuwe boekjaar. De openingstransactie laat de balansgrootboekrekeningsaldi in het nieuwe boekjaar zien en de saldi van de winst- en verliesgrootboekrekeningsaldi in de grootboekrekening voor ingehouden winsten in het nieuwe boekjaar. De afsluittransactie wordt desgewenst gemaakt om de saldi van de winst- en verliesrekeningen op nul te brengen in het boekjaar dat wordt afgesloten.

## <a name="prepare-to-run-the-year-end-close"></a>Voorbereidingen voor het jaarafsluitingsproces
Voordat u het jaarafsluitingsproces uitvoert, moet u de instellingen valideren voor het volgende: 

Op de pagina **Hoofdrekening**:

-   Valideer of het **Hoofdrekeningtype** juist is gedefinieerd voor elke hoofdrekening. Het hoofdrekeningtype wordt gebruikt om te bepalen of het saldo van de hoofdrekening wordt aangevoerd als een beginsaldo of wordt afgesloten in ingehouden winsten in de openingstransactie.
-   Het veld **Openingsrekening** kan worden gebruikt om het saldo van de hoofdrekening over te brengen naar een nieuwe hoofdrekening tijdens de jaarafsluiting. De nieuwe hoofdrekening wordt ingevoerd in het veld **Openingsrekening**. Meestal wordt dit gebruikt voor balanshoofdrekeningen wanneer de hoofdrekening is uitgeschakeld en een nieuwe hoofdrekening wordt gebruikt voor het nieuwe boekjaar.

Op de pagina **Grootboekparameters** onder **Afsluiting boekjaar**:

-   De optie **Jaareindetransacties verwijderen** wordt gebruikt om op te geven of de door het systeem gegenereerde openingstransactie uit een vorige jaarafsluiting moet worden verwijderd wanneer de jaarafsluiting opnieuw wordt uitgevoerd. Als deze optie wordt ingesteld op **Ja**, wordt de vorige openingstransactie verwijderd en wordt er een nieuwe openingstransactie gemaakt op basis van de huidige saldi. Als deze optie is ingesteld op **Nee**, blijft de vorige openingstransactie aanwezig en wordt er een extra openingstransactie gemaakt om de saldi te transporteren via correctietransacties die zijn geboekt na de vorige jaarafsluiting.
-   De optie **Afsluittransacties tijdens overboeken maken** wordt gebruikt om afsluittransacties te maken in het boekjaar dat wordt afgesloten om de saldi van de winst- en verliesrekeningen op nul te brengen. Als deze optie wordt ingesteld op **Ja**, worden zowel de openingstransactie als de afsluittransactie gemaakt. Als deze optie wordt ingesteld op **Nee**, wordt alleen de openingstransactie gemaakt in het volgende boekjaar om de saldi over te boeken. De saldi van winst- en verliesrekening blijven aan het einde van het boekjaar.
-   De optie **Status boekjaar instellen op definitief afgesloten** wordt gebruikt om het boekjaar in te stellen op een permanent afgesloten status. Ga voorzichtig met deze instelling om, omdat alle perioden met een permanent afgesloten status niet kunnen worden heropend, waardoor correcties niet naar het boekjaar kunnen worden geboekt. U kunt deze instelling het beste op **Nee** instellen.
-   De optie **Boekstuknummer moet worden ingevuld** wordt gebruikt om te definiëren of een boekstuknummer vereist is als u het jaarafsluitingsproces uitvoert. Het is raadzaam een boekstuknummer te vereisen zodat u de openingstransactie gemakkelijk kunt identificeren.

Op de pagina **Fiscale kalender**:

-   Het volgende boekjaar moet aanwezig zijn voordat u de jaarafsluiting kunt uitvoeren. Het volgende boekjaar is vereist om de beginsaldi in de openingsperiode te maken.

Op de pagina **Grootboekkalender**:

-   Optioneel: elke boekperiode voor het boekjaar dat wordt afgesloten, kan worden ingesteld op **In wachtstand** om te voorkomen dat nieuwe transacties worden ingevoerd. Wanneer correctiegegevens worden geïdentificeerd, worden de geblokkeerde perioden heropend om correctiegegevens te boeken, zelfs als het jaarafsluitingsproces al is uitgevoerd.

## <a name="define-year-end-close-templates"></a>Sjablonen voor jaarafsluiting definiëren
Nadat het systeem is geconfigureerd, kan het jaarafsluitingsproces worden uitgevoerd. Op de pagina **Jaarafsluiting** kan een sjabloon worden gedefinieerd voor de groep rechtspersonen waarvoor het jaarafsluitingsproces wordt uitgevoerd. De sjabloon wordt bij elke jaarafsluiting opnieuw gebruikt, maar kan worden gewijzigd als uw organisatie verandert. 

Definieer eerst de **Groepsnaam** voor de sjabloon en selecteer de fiscale kalender. Met de groepsnaam moet de groep rechtspersonen worden geïdentificeerd.  De sjablonen kunnen bijvoorbeeld worden ingesteld op basis van geografie, waarbij aparte groepen worden gemaakt voor Noord-Amerikaanse rechtspersonen, EMEA-rechtspersonen en APAC-rechtspersonen. 

Vervolgens kunnen de rechtspersonen worden toegevoegd aan de sjabloon. Rechtspersonen kunnen worden toegevoegd door een organisatiehiërarchie te selecteren of door de rechtspersonen te selecteren. Als een organisatiehiërarchie wordt geselecteerd, worden alleen rechtspersonen binnen de hiërarchie waarin de geselecteerde fiscale kalender wordt gebruikt, toegevoegd aan de sjabloon. Als u rechtspersonen wilt toevoegen aan de sjabloon, kunnen alleen rechtspersonen met dezelfde fiscale kalender worden toegevoegd. Dezelfde fiscale kalender is vereist, omdat de jaarafsluiting boekjaar wordt uitgevoerd door een boekjaar te selecteren, die per kalender kan variëren. 

Nadat de rechtspersonen zijn toegevoegd, definieert u de hoofdrekeningen voor ingehouden winsten voor elke rechtspersoon. Het veld **Datum van laatste jaarafsluiting** wordt bijgewerkt elke keer als de jaarafsluiting wordt uitgevoerd voor de rechtspersoon. 

Het tabblad **Financiële dimensie** wordt gebruikt om te definiëren welke financiële dimensies worden gebruikt in de openingstransactie. Houd er rekening mee dat de instellingen die u definieert alleen relevant zijn voor de rechtspersoon die is geselecteerd in het raster **Rechtspersonen**. U herhaalt de instelling voor elke rechtspersoon in het raster. 

**Balansdimensies overboeken** wordt gebruikt om te definiëren of de financiële dimensies voor transacties die zijn geboekt naar balansrekeningen, moeten worden ingesteld in de openingstransactie. U kunt deze optie het beste instellen op **Ja**. **Verlies- en winstdimensies overboeken** wordt gebruikt om te bepalen welke financiële dimensies voor transacties die zijn geboekt naar de winst- en verliesrekening, worden overgeboekt naar de hoofdrekening van ingehouden winsten. Geef eerst de financiële dimensies aan die relevant zijn voor de geselecteerde rechtspersoon. Dit kan alle financiële dimensies omvatten waarvoor is geboekt gedurende het jaar, zelfs als de financiële dimensie geen deel uitmaakt van een actieve rekeningstructuur. Definieer vervolgens elke dimensie als **Eén sluiten** of **Alles sluiten**.  De standaardwaarde is **Alles sluiten**, waarmee de oorspronkelijke waarden voor financiële dimensies van geboekte transacties worden behouden en worden gebruikt voor het maken van de beginsaldi voor de rekening ingehouden winsten. Afzonderlijke beginsaldi voor ingehouden winsten worden gemaakt voor elke unieke combinatie van waarden voor financiële dimensies. Als **Eén sluiten** is geselecteerd, worden alle transacties die zijn geboekt met die financiële dimensie, samengevat in een beginsaldo voor ingehouden winsten voor de dimensiewaarde die is ingevoerd in het veld na **Eén sluiten**. Stel bijvoorbeeld dat alle transacties voor het boekjaar zijn geboekt met de rekeningstructuur van hoofdrekening - afdeling. Op de financiële dimensie Afdeling in de sjabloon is **Eén sluiten** geselecteerd en is 100 de ingevoerde waarde. Als de totale inkomsten van alle transacties die zijn geboekt naar afdelingen 200, 300 en 400 100.000 zijn, wordt één beginsaldo gemaakt voor Ingehouden winsten - 100. Als u **Eén sluiten** selecteert en de waarde voor de financiële dimensie leeg laat, worden alle transacties geboekt naar ingehouden winsten waarbij die dimensiewaarde leeg is. 

Bij het jaarafsluitingsproces worden geen rekeningstructuren aangehouden. Dit komt doordat rekeningstructuren gedurende een boekjaar kunnen veranderen en vanwege deze wijzigingen is het niet altijd mogelijk om de relevante rekeningstructuur aan te duiden.  Wanneer openingstransacties worden gemaakt, worden de saldi aangevoerd met financiële dimensies, zoals is gedefinieerd in de jaarafsluitingssjabloon. De beginsaldiposten kunnen financiële dimensies bevatten die niet meer in de huidige rekeningstructuur voorkomen en segmentcombinaties die niet meer geldig zijn in de huidige rekeningstructuur. Als uw organisatie een financiële dimensie wil uitsluiten voor het beginsaldo van ingehouden winsten, stelt u de financiële dimensie in op **Eén sluiten** en laat u de dimensiewaarde leeg.

## <a name="run-the-year-end-close-process"></a>Het jaarafsluitingsproces uitvoeren
Nadat de sjablonen voor het jaarafsluitingsproces zijn gemaakt, wordt het jaarafsluitingsproces gestart door **Boekjaar uitvoeren** te kiezen in het actievenster. Selecteer alle rechtspersonen of een subset ervan in de sjabloon waarvoor de jaarafsluiting moet worden uitgevoerd. Wanneer de jaarafsluiting voor de eerste keer in een boekjaar wordt uitgevoerd, kiest u waarschijnlijk alle rechtspersonen om beginsaldi voor alle rechtspersonen te maken. Als u de jaarafsluiting opnieuw uitvoert, kunt u ervoor kiezen het proces uit te voeren voor alleen de rechtspersonen waarvoor correctieposten zijn geboekt. 

Selecteer het boekjaar waarvoor u het jaarafsluitingsproces wilt uitvoeren. Als er meer dan één afsluitperiode bestaat voor de laatste periode van het boekjaar, wordt het veld **Periodenaam** beschikbaar zodat u kunt aangeven naar welke afsluitperiode de afsluittransactie moet worden geboekt als de instelling is gedefinieerd om de afsluittransactie te maken. 

Voer een boekstuknummer in dat al dan niet vereist is. Dit hangt af van de instelling in de grootboekparameters. Hetzelfde boekstuknummer wordt gebruikt voor alle rechtspersonen die zijn geselecteerd voor het jaarafsluitingsproces. Het boekstuknummer wordt niet gegenereerd met een nummerreeks. Het is raadzaam om een boekstuknummer in te voeren, zelfs als dit niet vereist is. Als u een boekstuknummer invoert, kunt u gemakkelijker zoeken naar de openingstransactie in het nieuwe boekjaar. Als een boekstuknummer niet wordt ingevoerd, is het boekstuk leeg voor de openingstransactie. 

Als u een vorige jaarafsluiting voor het geselecteerde boekjaar ongedaan wilt maken, stelt u **Vorige afsluiting ongedaan maken** in op **Ja**. De jaarafsluiting wordt ongedaan gemaakt, maar het proces kan op elk gewenst moment opnieuw worden uitgevoerd. Als u een jaarafsluiting ongedaan maakt, is **Datum van laatste jaarafsluiting** niet beschikbaar. 

Het jaarafsluitingsproces wordt standaard in de batchmodus uitgevoerd. Het is raadzaam om het proces in de batchmodus uit te voeren, zodat de gebruiker kan teruggaan naar de andere activiteiten. Het veld **Datum van laatste jaarafsluiting** wordt bijgewerkt met de sessiedatum nadat het jaarafsluitingsproces is voltooid.

Zie [Het grootboek aan het einde van de periode afsluiten](close-general-ledger-at-period-end.md) voor meer informatie.




