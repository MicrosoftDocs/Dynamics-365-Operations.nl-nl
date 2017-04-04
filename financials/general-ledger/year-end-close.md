---
title: Jaarafsluiting
description: Dit onderwerp beschrijft de vereiste instellingen en de stappen voor het uitvoeren van het grootboek afsluiten jaarultimoproces.
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

Dit onderwerp beschrijft de vereiste instellingen en de stappen voor het uitvoeren van het grootboek afsluiten jaarultimoproces. 

Aan het einde van een boekjaar moet u het jaarultimoproces sluiten om beginsaldi overboeken naar het nieuwe jaar uitvoeren. De meeste organisaties wordt het jaarultimoproces Sluit meerdere keren uitvoeren. De eerste keer wordt het saldo in het nieuwe boekjaar geplaatst. Sluit het jaareinde kan vervolgens opnieuw worden uitgevoerd als vaak zijn vereist om de saldi van wijzigingsposten naar het nieuwe fiscaal jaar. 

Sluit tijdens het jaareinde verwerken, er zijn twee typen van eventuele transacties die zijn gemaakt. Een openingstransactie wordt altijd gegenereerd en wordt gebruikt voor het maken van de openingssaldi in het nieuwe boekjaar. De openingstransactie ziet u de balans grootboekrekeningsaldi in het nieuwe boekjaar en saldi van de winst en verlies grootboekrekeningsaldi in de ingehouden winsten grootboekrekening in het nieuwe boekjaar. De afsluittransactie desgewenst gemaakt om de saldi van de winst- en verliesrekeningen op nul in het boekjaar wordt afgesloten.

## <a name="prepare-to-run-the-year-end-close"></a>Voorbereidingen voor het jaareinde afsluit
Voordat u het jaarultimoproces sluiten uitvoert, moet u de instellingen voor de volgende valideren: 

Op de pagina **Hoofdrekening**:

-   Valideer de **hoofdtabel rekeningtype** juist is gedefinieerd voor elke hoofdrekening. Het rekeningtype van de hoofdtabel wordt gebruikt om te bepalen of het saldo van de belangrijkste rekening worden gebracht naar voren als een beginsaldo of afgesloten in ingehouden winsten in de transactie openen.
-   De **openingsrekening** veld kan worden gebruikt voor het saldo van de hoofdrekening overboeken naar een nieuwe hoofdrekening tijdens de afsluiting boekjaar afsluiten. De nieuwe hoofdrekening is ingevoerd in de **openingsrekening** veld. Meestal wordt dit gebruikt voor hoofdrekeningen balans wanneer de hoofdrekening is uitgeschakeld en een nieuwe hoofdrekening wordt gebruikt voor het nieuwe boekjaar.

Op de **grootboekparameters** pagina onder **afsluiting boekjaar**:

-   De **verwijderen sluiten van transacties voor jaar** optie wordt gebruikt om op te geven of het systeem gegenereerde openingstransactie uit een vorige afsluiting boekjaar afsluiten moeten worden verwijderd wanneer de afsluiting boekjaar afsluiten opnieuw wordt uitgevoerd. Als deze optie is ingesteld op **Ja**, de vorige openingstransactie verwijderd en wordt een nieuwe openen-transactie is gemaakt op basis van de huidige saldi. Als deze optie is ingesteld op **Nee**, de vorige openingstransactie blijft en een extra openingstransactie wordt gemaakt als u wilt verplaatsen van de saldi vooruit vanaf het corrigeren van transacties die zijn geboekt na het afsluiten van het vorige jaareinde.
-   De **Afsluittransacties tijdens overboeken maken** optie wordt gebruikt om afsluittransacties te maken van het fiscale jaar wordt afgesloten om de saldi van de winst- en verliesrekeningen op nul te brengen. Als deze optie is ingesteld op **Ja**, de openingstransactie en de afsluittransactie is gemaakt. Als deze optie is ingesteld op **Nee**, alleen de openingstransactie wordt gemaakt in het volgende boekjaar de saldi moeten worden overgeboekt. De verlies- en rekeningsaldo's blijven aan het einde van het fiscale jaar.
-   De **permanent afgesloten boekjaar status instellen op** optie wordt gebruikt om het fiscale jaar permanent afgesloten status ingesteld. Gebruik deze instelling voorzichtig mee, omdat alle perioden met de status van een permanent afgesloten kunnen niet worden heropend, correcties worden geboekt naar het boekjaar te blokkeren. Het is raadzaam deze optie instellen op **Nee**.
-   De **boekstuknummer moet worden ingevuld** optie wordt gebruikt om te definiëren of een boekstuknummer vereist is als u het jaarultimoproces sluiten. Het is raadzaam een boekstuknummer vereist om te kunnen herkennen de openingstransactie.

Op de **fiscale kalender** pagina:

-   Het volgende boekjaar moet bestaan voordat u de afsluiting boekjaar afsluiten. Het volgende boekjaar is vereist voor de beginsaldi maken in de openingsperiode.

Op de **grootboekkalender** pagina:

-   Optioneel: Elk fiscaal jaar voor het boekjaar wordt afgesloten kan worden ingesteld op **in de wachtstand** om te voorkomen dat nieuwe transacties worden ingevoerd. Wanneer correctiegegevens worden geïdentificeerd, de blokkering op perioden kunnen worden opnieuw geopend boeken correctiegegevens, zelfs als het jaarultimoproces afsluiten al is uitgevoerd.

## <a name="define-year-end-close-templates"></a>Jaareinde sluiten sjablonen definiëren
Nadat het systeem is geconfigureerd, kan het jaarultimoproces sluiten worden uitgevoerd. Op de **Jaarultimoafsluiting** pagina een sjabloon kan worden gedefinieerd voor de groep van de rechtspersonen waarvoor de sluiting einde van het proces wordt uitgevoerd. De sjabloon zal opnieuw worden gebruikt bij elke afsluiting boekjaar afsluiten, maar kan worden gewijzigd als uw organisatie is gewijzigd. 

Eerste stap definieert het **groepsnaam** voor de sjabloon en selecteer de fiscale kalender. De groepsnaam moet de groepcriteria rechtspersonen opgenomen.  Bijvoorbeeld kunnen de sjablonen worden ingesteld op basis van geografische, met aparte groepen gemaakt voor Noord-Amerikaanse rechtspersonen, EMEA rechtspersonen en APAC rechtspersonen. 

De rechtspersonen kunnen vervolgens worden toegevoegd aan de sjabloon. Rechtspersonen kunnen worden toegevoegd door een organisatiehiërarchie selecteren of door de rechtspersonen te selecteren. Als een organisatiehiërarchie is ingeschakeld, worden alleen rechtspersonen binnen de hiërarchie waarin de geselecteerde fiscale kalender wordt toegevoegd aan de sjabloon. Als u wilt toevoegen aan de sjabloon rechtspersonen, kunnen alleen rechtspersonen met dezelfde fiscale kalender worden toegevoegd. Dezelfde fiscale kalender is vereist, omdat de afsluiting boekjaar afsluiten wordt uitgevoerd door een boekjaar, die, kalender kalender variëren kan selecteren. 

Nadat de rechtspersonen worden toegevoegd, definieert u de hoofdrekeningen voor ingehouden winst voor elke rechtspersoon. De **datum van laatste jaareinde sluiten** veld wordt bijgewerkt telkens als het jaareinde afsluiten wordt uitgevoerd voor de rechtspersoon. 

De **financiële dimensie** tab wordt gebruikt om te definiëren welke financiële dimensies worden gebruikt voor de transactie openen. Houd er rekening mee dat de instellingen die u definieert alleen de rechtspersoon die zijn geselecteerd betreffen in de **rechtspersonen** raster. U kunt de instellingen wordt herhaald voor elke rechtspersoon in het raster. 

De **balans dimensies overbrengen** wordt gebruikt om te definiëren of de financiële dimensies voor transacties die zijn geboekt naar balansrekeningen moeten worden ingesteld op de transactie openen. Het is raadzaam deze optie instellen op **Ja**. De **overbrengen van winst en verlies dimensies** wordt gebruikt om te bepalen welke financiële dimensies op transacties die zijn geboekt naar winst en verlies-rekening overgemaakt naar de hoofdrekening van ingehouden winsten. Bepaal eerst de financiële dimensies die relevant zijn voor de geselecteerde rechtspersoon. Dit kan de financiële dimensies geboekt tegen gedurende het jaar omvatten, zelfs als de financiële dimensie geen deel uit van een actieve rekeningstructuur maakt. Definieer vervolgens elke dimensie als **Sluit één** of **sluit u alle**.  De standaardwaarde is **sluit u alle**, die de oorspronkelijke financiële dimensie onderhoudt waarden van geboekte transacties en deze worden gebruikt voor het maken van de saldi voor de rekening ingehouden winsten. Afzonderlijke ingehouden beginsaldi gemaakt voor elke unieke combinatie van financiële dimensiewaarden. Als **Sluit één** is ingeschakeld, worden alle transacties die zijn geboekt met die financiële dimensie in een beginsaldo voor de dimensiewaarde die is ingevoerd in het veld na ingehouden samengevat **Sluit één**. Stel bijvoorbeeld dat alle transacties voor het boekjaar zijn geboekt met de rekeningstructuur van de hoofdrekening - afdeling. Op de financiële dimensie Afdeling op de sjabloon **Sluit één** is ingeschakeld en de ingevoerde waarde is 100. Als de totale inkomsten van alle transacties die zijn geboekt naar afdelingen 200, 300 en 400 $100,000 is, wordt een beginsaldo voor winst Retained - 100 worden gemaakt. Als u **Sluit één** en de financiële dimensiewaarde leeg laat, wordt alle transacties worden geboekt naar ingehouden winsten aan die dimensiewaarde wordt leeg. 

Het jaarultimoproces sluiten voldoen niet aan de rekeningstructuren. Dit komt doordat rekeningstructuren gedurende een boekjaar veranderen kunnen en het is niet altijd mogelijk om aan te duiden de relevante rekeningstructuur vanwege deze wijzigingen.  Wanneer openingstransacties worden gemaakt, worden de saldi vervroegd met financiële dimensies zoals is gedefinieerd in het jaar einde sluiten (sjabloon). Items in de saldi begin kunnen niet meer financiële dimensies bevatten in de huidige rekening structuur segment combinaties en die niet langer geldig in de structuur van de huidige rekening zijn. Als uw organisatie wil uitsluiten van een financiële dimensie voor de financiële dimensie moet worden ingehouden verdienen beginsaldo, ingesteld **Sluit één** en de waarde van de dimensie leeg laten.

## <a name="run-the-year-end-close-process"></a>Het jaarultimoproces sluiten uitvoert
Nadat de jaarultimo sluiten sjablonen zijn gemaakt, wordt opgehaald uit het jaarultimoproces sluiten kiezen **uitvoeren van fiscaal jaar** in het actievenster te klikken. Selecteer alle of een subset van juridische entiteiten uit de sjabloon waarop de afsluiting boekjaar afsluit. Wanneer het jaareinde uitgevoerd voor de eerste keer in een boekjaar afsluit, wordt u waarschijnlijk alle rechtspersonen beginsaldi voor alle rechtspersonen maken. Als u het jaareinde afsluiten opnieuw, kunt u de historie van bijwerkacties voor alleen rechtspersonen waarvoor de correctiepost posten zijn geboekt. 

Selecteer het boekjaar dat u wilt uitvoeren van het jaar afsluiten proces aan het einde ten opzichte van. Als er meer dan een afsluitperiode bestaat voor de laatste periode van het boekjaar, het **periodenaam** veld zijn binnenkort beschikbaar zodat u welke afsluitperiode waarnaar de transactie afsluiting selecteren kunt als is ingesteld voor het maken van de transactie afsluiting. 

Een boekstuk invoeren nummeren, die al dan niet vereist, afhankelijk van de instellingen in het algemeen grootboekparameters. Het boekstuknummer dat wordt gebruikt voor alle rechtspersonen die geselecteerd voor het proces voor het afsluiten van jaar-einde. Het boekstuknummer wordt niet gegenereerd met behulp van een nummerreeks. Het is raadzaam om in te voeren een boekstuknummer toegewezen zelfs als dit is niet vereist. Een boekstuknummer invoeren gemakkelijker zoeken naar de openingstransactie in het nieuwe boekjaar. Als een boekstuknummer niet is ingevoerd, is het boekstuk is leeg voor de transactie openen. 

Als u omkeren bij het afsluiten een einde van het vorige jaar voor het geselecteerde fiscaal jaar wilt, stelt u **sluit vorige ongedaan** naar **Ja**. Sluit het jaareinde worden omgekeerd, maar het proces opnieuw op elk gewenst moment kan worden uitgevoerd. Als het omkeren van een afsluiting boekjaar afsluiten, de **datum van laatste jaareinde sluiten** is niet beschikbaar. 

Het jaarultimoproces sluit de standaardinstelling in batchmodus uitgevoerd. Het is raadzaam om uit te voeren van het proces in de batchmodus, zodat de gebruiker teruggaan naar de andere activiteiten. Nadat het jaareinde sluiten-proces voltooid is, de **datum van laatste jaareinde sluiten** wordt bijgewerkt met de sessiedatum.

Zie voor meer informatie [het grootboek aan het einde van de periode](close-general-ledger-at-period-end.md).


