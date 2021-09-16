---
title: Standaard financiële dimensies in financiële journalen
description: In dit onderwerp worden de regels beschreven die bepalen hoe waarden van financiële dimensies worden ingesteld in transacties die worden ingevoerd via financiële journalen. Het bevat ook details voor scenario's waarin vaste dimensies worden gebruikt.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 327bc27f068e1f9eefacc6b5defa27044cb1a77e
ms.sourcegitcommit: d420b96d37093c26f0e99c548f036eb49a15ec30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2021
ms.locfileid: "7472527"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Standaard financiële dimensies in financiële journalen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de regels beschreven die bepalen hoe waarden van financiële dimensies worden ingesteld in transacties die worden ingevoerd via financiële journalen (niet via voorraadjournalen of projectjournalen). Het bevat ook details voor scenario's waarin vaste dimensies worden gebruikt.

## <a name="symptom"></a>Symptoom

De waarden van financiële dimensies worden niet, zoals verwacht, ingesteld op de rekening of tegenrekening in een financieel journaal. De volgende scenario's bevatten twee voorbeelden:

Een boekstuk wordt in een algemeen journaal ingevoerd. De rekening is een leverancierrekening en de tegenrekening is een bankrekening. De financiële dimensies van de leverancier worden standaard ingevoerd op de rekening, maar de financiële dimensies van de bank worden niet standaard ingevoerd op de tegenrekening. In plaats daarvan worden de dimensiewaarden van de rekening standaard ingevoerd op de tegenrekening.

Aan een klant zijn standaardwaarden voor financiële dimensies toegewezen en aan een hoofdrekening voor opbrengsten is een vaste dimensiewaarde toegewezen voor de financiële dimensie Afdeling. Een boekstuk wordt in een algemeen journaal ingevoerd.  De rekening is de klant en de tegenrekening is een grootboekrekening, in het bijzonder de opbrengstrekening met de vaste dimensiewaarde. De vaste dimensie wordt niet ingesteld op de tegenrekening voor de hoofdrekening voor opbrengsten. In plaats daarvan wordt de dimensie ingesteld op de dimensiewaarde Afdeling van de rekening, die afkomstig is van de klant.  Na het boeken van het boekstuk wordt de vaste dimensiewaarde gebruikt op de geboekte journaalregel, maar geeft het boekstuk nog de afdelingswaarde weer voor de opbrengstrekening van de klant. 

Welke regels worden gevolgd voor waarden van financiële dimensies die worden ingesteld op boekstukken in een journaal?

## <a name="resolution"></a>Oplossing

De volgende regels worden gevolgd om standaardwaarden van financiële dimensies in te voeren op de regels van een boekstuk in financiële journalen, zoals het algemene journaal of leveranciersfactuurjournaal. 

1. **Journaalkoptekst**

   - De dimensies van de journaalkoptekst worden standaard ingevoerd vanuit de dimensies van de journaalnaam.

2. **Rekening van journaalregel**

   - De rekeningdimensies van de journaalregel worden standaard ingevoerd vanuit de dimensies van de journaalkoptekst.
   - Als financiële dimensies leeg zijn, worden de waarden standaard ingevoerd vanuit klant-, leveranciers-, bank-, vaste activa-, project- of grootboekdimensies.

     - Als het rekeningtype **Grootboek** is, wordt een vaste dimensie op een grootboekrekening behandeld als een standaarddimensie bij het invoeren van transacties.
     - Als het rekeningtype **Klant**, **Leverancier**, **Bank**, **Vaste activa** of **Project** is, kan de hoofdrekening nog niet worden bepaald. Daarom wordt nooit standaard een vaste dimensie voor de rekening ingevoerd.

3. **Tegenrekening van journaalregel**

 - De tegenrekeningdimensies van de journaalregel worden standaard overgenomen vanuit de rekeningdimensies van de journaalregel.

 - Als financiële dimensies leeg zijn, is de volgende standaardinvoer afkomstig uit de standaarddimensies vanuit Klant, Leverancier, Bank, Vaste Activa, Project of Grootboek.
   1. Als het tegenrekeningtype **Grootboek** is, wordt een vaste dimensie op een grootboekrekening behandeld als een standaarddimensie bij het invoeren van transacties. Als er al standaard een dimensiewaarde is ingevoerd via de rekening, wordt de bestaande waarde niet overschreven door de standaard- of vaste dimensiewaarde van de hoofdrekening.
   2. Als het tegenrekeningtype **Klant**, **Leverancier**, **Bank**, **Vaste activa** of **Project** is, is de hoofdrekening voor de tegenrekening nooit standaard voor de tegenrekening.

4. **Boeking**

    1. Tijdens het boeken wordt de hoofdrekening voor elke journaalregel (voor zowel de rekening als de tegenrekening) geëvalueerd om te bepalen of er een vaste dimensiewaarde is. Als er een vaste dimensie is gedefinieerd, worden bestaande of lege waarden vervangen door die vaste dimensiewaarde.

        De vaste dimensiewaarde wordt na boeking **niet** weergegeven op de journaalregels. In plaats daarvan wordt de waarde weergegeven op de boeking wanneer u het boekstuk bekijkt nadat het is geboekt.

    2. Tijdens het boeken worden er geen andere dimensiewaarden standaard ingevoerd, waaronder extra grootboekrekeningen die tijdens het boeken kunnen worden toegevoegd, zoals afrondingsrekeningen voor afrondingen en intercompany-rekeningen voor betalen of ontvangen. De standaarddimensieboekingen voor extra grootboekrekeningen worden overgenomen van de rekening of tegenrekeningen.

Voor het standaard invoeren van dimensiewaarden kan door het standaard journaalproces niet worden bepaald of een lege dimensiewaarde opzettelijk leeg is gelaten of dat de standaardinvoer niet is gemaakt. Als een dimensiewaarde opzettelijk leeg wordt gelaten, kan nog steeds standaard een waarde worden ingevoerd met de standaardvolgorde die eerder is beschreven. Als een dimensie een lege waarde moet hebben, moet u mogelijk een dimensie met de waarde **0** (nul) of **Leeg** maken, zodat deze kan worden gebruikt in plaats van een lege dimensie.

Bekijk de volgende scenario's voor voorbeelden van de standaardvolgorde van financiële dimensies.

### <a name="scenario-1"></a>Scenario 1

Ga naar **Grootboek \> Journaalinstellingen \> Journaalnamen** en selecteer de journaalnaam **GenJrn**. Definieer vervolgens op het sneltabblad **Financiële dimensies** de volgende waarden voor de standaard financiële dimensies:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Pagina Journaalnamen](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Ga naar **Grootboek \> Journaalregels \> Algemeen journaal** en maak een nieuw algemeen journaal met de naam **GenJrn**. De dimensies worden standaard vanuit de journaalnaam (tabel LedgerJournalName) ingevoerd in de journaalkoptekst (tabel LedgerJournalTable), zoals weergegeven op het tabblad **Financiële dimensies**.

[![Tabblad Financiële dimensies op de pagina Algemene journalen](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Ga naar de **Regels**. Selecteer **Grootboek** in het veld **Rekeningtype** en voer vervolgens **170150** in het veld **Rekening** in. Ga vervolgens met de **Tab**-toets uit het veld. De dimensies worden standaard ingevoerd vanuit de journaalkoptekst. Daarom wordt de **rekening** waarde weergegeven als **170150-001-024**.

[![Journaalregels voor een algemeen journaal op de pagina Journaalboekstuk](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Wijzig de **rekening** waarde in **170150-001-023**. Voer een debetbedrag of een creditbedrag in. Selecteer **Grootboek** in het veld **Tegenrekeningtype** en voer vervolgens **600150** in het veld **Tegenrekening** in. De dimensiewaarden worden standaard ingevoerd vanuit de rekening. Daarom wordt de waarden van de **tegenrekening** weergegeven als **600150-001-023**.

### <a name="scenario-2"></a>Scenario 2

Gebruik dezelfde financiële dimensies die u voor de journaalnaam in scenario 1 hebt gedefinieerd. Ga vervolgens naar **Klanten \> Klanten \> Alle klanten** en definieer de standaardwaarden voor financiële dimensies voor klant US-001. Selecteer de klant om de klantgegevens te openen. Laat op het tabblad **Financiële dimensies** de standaardwaarde voor de dimensie **BUSINESSUNIT** (**001**) staan. Voeg de dimensie **COSTCENTER** toe en voer **007** als de waarde in.

Maak een nieuw algemeen journaal dat de journaalnaam **GenJrn** gebruikt. Wijzig op het tabblad **Financiële dimensies** de standaardwaarde **BUSINESSUNIT** van **001** in **002**.

Ga naar de **Regels**. Selecteer **Klant** in het veld **Rekeningtype** en voer vervolgens **US-001** in het veld **Rekening** in. Als u de financiële dimensies voor niet-grootboekrekeningtypen wilt weergeven, selecteert u **Financiële dimensies \> Rekening**. De volgende standaardwaarden voor de waarden van financiële dimensies worden ingevoerd:

- **BUSINESSUNIT:** 002: de standaardboeking wordt overgenomen uit de journaalkoptekst. De waarde **001** wordt niet standaard overgenomen van klant US-001, omdat er al een standaardwaarde was ingevoerd.
- **COSTCENTER:** 007: de standaardinvoer wordt overgenomen uit de instellingen van klant US-001.
- **DEPARTMENT:** 024: de standaardboeking wordt overgenomen uit de journaalkoptekst.

Selecteer in de regel **Grootboek** in het veld **Tegenrekeningtype** en voer vervolgens **600150** in het veld **Tegenrekening** in. De volgende standaardwaarden voor de waarden van financiële dimensies worden op de regel ingevoerd:

- **BUSINESSUNIT:** 002: de standaardinvoer wordt overgenomen uit de financiële dimensies van de rekening. (De gegevens werden standaard ingevoerd vanuit de journaalkoptekst.)
- **DEPARTMENT:** 024: de standaardinvoer wordt overgenomen uit de financiële dimensies van de rekening. (De gegevens werden standaard ingevoerd vanuit de journaalkoptekst.)
- **COSTCENTER:** 007: de standaardinvoer wordt overgenomen uit de financiële dimensies van de rekening. (De gegevens werden standaard ingevoerd vanuit de klant.)

### <a name="scenario-3"></a>Scenario 3

Voeg een nieuwe regel toe in hetzelfde journaal dat u voor scenario 2 hebt gebruikt. Selecteer **Grootboek** in het veld **Rekeningtype** en voer vervolgens **170150** in het veld **Rekening** in. Wis de standaarddimensiewaarden zodat alleen hoofdrekeninggegevens 170150 blijven staan. Selecteer **Klant** in het veld **Tegenrekeningtype** en voer vervolgens **US-001** in het veld **Tegenrekening** in. De volgende standaardwaarden voor de waarden van financiële dimensies worden ingevoerd:

- **BUSINESSUNIT:** 002: de standaardboeking wordt overgenomen uit de journaalkoptekst, omdat de waarde van de rekeningdimensie leeg is. De waarde **001** wordt niet standaard overgenomen van klant US-001, omdat er al een standaardwaarde is overgenomen uit de journaalkoptekst. Als de waarde **BUSINESSUNIT** opzettelijk leeg is gelaten, moet u ook de financiële dimensie uit de tegenrekening verwijderen.
- **COSTCENTER:** 007: de standaardinvoer wordt overgenomen van klant US-001, omdat de dimensiewaarde voor de rekening en de journaalkoptekst leeg zijn. Als de waarde **COSTCENTER** opzettelijk leeg is gelaten, moet u ook de financiële dimensie uit de tegenrekening verwijderen.
- **DEPARTMENT:** 024: de standaardboeking wordt overgenomen uit de journaalkoptekst, omdat de waarde van de rekeningdimensie leeg is. Als de waarde **DEPARTMENT** opzettelijk leeg is gelaten, moet u ook de financiële dimensie uit de tegenrekening verwijderen.

### <a name="scenario-4"></a>Scenario 4

Gebruik dezelfde standaardwaarden voor financiële dimensies die u voor de journaalnaam en klant hebt gedefinieerd in scenario 1 en 2. Definieer vervolgens een vaste dimensiewaarde voor de dimensie **BUSINESSUNIT** in hoofdrekening 170150. Ga naar **Grootboek \> Rekeningschema \> Rekeningen \> Hoofdrekeningen**. Selecteer **170150** in het veld **Hoofdrekening** en selecteer vervolgens **Toevoegen** op het tabblad **Overschrijvingen van rechtspersoon**. Selecteer **USMF** als de rechtspersoon en selecteer **Toevoegen**. Selecteer die record en selecteer vervolgens **Standaarddimensies**. Wijzig de dimensie **BUSINESSUNIT** in **Vaste waarde** en voer **003** in als de waarde.

Maak een nieuw algemeen journaal dat de journaalnaam **GenJrn** gebruikt. Verwijder alle standaarddimensiewaarden op het tabblad **Financiële dimensies**.

Ga naar de **Regels**. Selecteer **Grootboek** in het veld **Rekeningtype** en voer vervolgens **170150** in het veld **Rekening** in. Ga vervolgens met de **Tab**-toets uit het veld. De dimensiewaarden worden standaard ingevoerd vanuit de instellingen van de hoofdrekening voor rekening 170150. Daarom wordt de **rekening** waarde weergegeven als **170150-003-**.

Wijzig de **rekening** waarde in **170150-004-**. **De journaalfunctionaliteit voorkomt echter niet dat een vaste dimensiewaarde wordt gewijzigd.** Voer een debetbedrag of een creditbedrag in. Selecteer **Grootboek** in het veld **Tegenrekeningtype** en voer vervolgens **170250** in het veld **Tegenrekening** in. De financiële dimensiewaarde 004 wordt standaard ingevoerd vanuit de rekening. Vervolgens kunt u het document boeken. Selecteer **Boekstuk** in het journaal. Tijdens het boeken wordt de waarde **BUSINESSUNIT** teruggezet op de vaste dimensiewaarde **003**.

Wanneer u teruggaat naar het boekstuk in het journaal, wordt bij de dimensie **BUSINESSUNIT** **niet** de vaste dimensiewaarde weergegeven. Deze heeft altijd de waarde die vóór het boeken op het scherm werd weergegeven. Tijdens het boekingsproces wordt niets gewijzigd dat op het boekstuk wordt ingevoerd. Alleen de journaalregel in de boekhouding wordt tijdens het boeken gewijzigd.

## <a name="developer-notes"></a>Notities voor ontwikkelaars

Als u een ontwikkelaar bent en zoekt naar code voor het standaardproces, controleert u de volgende methoden:

- **LedgerJournalEngine.accountModified()**: deze methode is het hoofdinvoerpunt voor het standaardproces voor de primaire rekeningdimensie dat standaard is voor alle journalen (en wordt overgenomen door een aantal journaaltypen).
- **LedgerJournalEngine.offsetAccountModified()**: deze methode is het hoofdinvoerpunt voor het standaardproces voor de dimensie voor tegenrekening.
