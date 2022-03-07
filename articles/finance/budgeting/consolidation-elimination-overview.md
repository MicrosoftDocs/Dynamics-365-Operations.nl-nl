---
title: Overzicht van consolidatie en schrapping
description: Dit onderwerp geeft algemene informatie over het consolidatie- en schrappingsproces. Het bevat antwoorden op enkele veelgestelde vragen.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "13151"
- intro-internal
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3134c55458d09e2f9ec3aca3ce5c20afdbdf1d3
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883434"
---
# <a name="consolidation-and-elimination-overview"></a>Overzicht van consolidatie en schrapping

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft algemene informatie over het consolidatie- en schrappingsproces. Het bevat antwoorden op enkele veelgestelde vragen.

Wanneer u gegevens consolideert, worden de financiële resultaten van meerdere dochterbedrijven gecombineerd in de resultaten voor één geconsolideerd bedrijf. De dochtermaatschappijen gebruiken mogelijk verschillende versies of systemen, ze zijn mogelijk niet volledig in eigendom en ze gebruiken misschien andere valuta's. Er zijn meerdere opties voor het consolideren van gegevens:

-   **Online consolideren**: met deze optie worden dagelijkse saldi geconsolideerd op basis van de geselecteerde rekeningen en dimensies, en deze worden in een consolidatiebedrijf opgeslagen.
-   **Financiële rapportage**: met deze optie is consolidatie van transacties en saldi mogelijk en deze rapportage kan op elk moment worden gegenereerd. Meerdere niveaus van hiërarchieën kunnen worden gemaakt en meerdere aangiftevaluta kunnen worden weergegeven.
-   **Consolidatie met import**: met deze optie worden saldi in een consolidatiebedrijf geïmporteerd.
-   **Bedrijfssaldi exporteren**: deze optie verschaft een exportbestand van bedrijfssaldi. Het bestand kan vervolgens in andere exemplaren of systemen worden geïmporteerd. Financiële rapportage kan ook worden gebruikt om de saldi naar een Microsoft Excel-bestand te exporteren.

Schrappingen kunnen op meerdere manieren worden gerapporteerd:

-  De schrappingsregels kunnen in het systeem worden ingesteld en vervolgens tijdens het consolidatieproces of via een schrappingsvoorstel worden verwerkt. De regels kunnen naar elk bedrijf worden geboekt waarvoor **Gebruiken voor proces voor financiële schrapping** in de instellingen van de rechtspersoon is geselecteerd.
-   Een afzonderlijk bedrijf kan worden gemaakt en gebruikt om schrappingstransacties handmatig te definiëren en te boeken. Dit bedrijf kan in het consolidatieproces of in de financiële rapportage worden gebruikt.
-  De rekeningen en financiële dimensies die worden gebruikt om activiteiten tussen bedrijven vast te stellen, kunnen in financiële rapportage op een rijdefinitie of kolomdefinitie worden gefilterd en de volledige inzoommogelijkheden kunnen worden gebruikt. Een berekende kolom of rij kan vervolgens worden gebruikt om de rekeningen en financiële dimensies uit het geconsolideerde totaal te verwijderen.

Er bestaan veel consolidatiescenario's en met elke methode kunnen de scenario's op verschillende manieren worden afgehandeld.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
1. Ik verkies schrappingen in een database te boeken. Wat zijn mijn opties?

U hebt meerdere opties. U kunt de optie **Consolidatie online** gebruiken en schrappingen tijdens het proces of als een voorstel opnemen. De transacties worden in het consolidatiebedrijf geboekt. U kunt ook een afzonderlijk bedrijf hebben waarin u de schrappingen handmatig maakt en vervolgens dat bedrijf in de financiële rapportage of in het consolidatieproces gebruiken.

2.  We hebben onze geconsolideerde resultaten in meerdere aangiftevaluta´s nodig.

De optie **Financiële rapportage** heeft onbeperkte aangiftevaluta´s. De gegevens worden vertaald tijdens het genereren van rapporten op basis van het wisselkoerstype en de omrekeningsmethode voor valuta´s, die in de hoofdrekening worden ingesteld. Omdat de optie **Consolidatie online** slechts één aangiftevaluta heeft, is een geconsolideerd bedrijf vereist voor elke aangiftevaluta als u deze optie gebruikt. De optie **Financiële rapportage** is de aanbevolen methode.

3. Ik wil gegevens op transactieniveau voor elk bedrijf zien.

De optie **Financiële rapportage** is de oplossing, omdat gegevens op transactieniveau voor zoveel bedrijven kan worden weergegeven als in de rapportagestructuurdefinitie zijn opgenomen.

4. We gebruiken budgetplanning of budgetbeheer en dit moet worden geconsolideerd.

De optie **Financiële rapportage** is de oplossing om budgetplannings- of budgetbeheergegevens samen te voegen.

5. Onze dochterondernemingen zitten over de hele wereld verspreid en we hebben meerdere rekeningschema's. Wat is de beste methode om onze gegevens te consolideren?

U hebt meerdere opties wanneer u meerdere rekeningschema's moet verwerken. U kunt de optie **Consolidatie online** gebruiken en er vervolgens voor kiezen om de consolidatierekening te gebruiken die in de hoofdrekening of een consolidatierekeninggroep is gedefinieerd. U kunt ook de optie **Financiële rapportage** gebruiken, meerdere koppelingen naar de financiële dimensies in de rijdefinitie opnemen en de rekeningen toewijzen.

6. We hebben meerdere consolidatieniveaus nodig. Met andere woorden, we consolideren eerst onze Europese dochtermaatschappijen in de Britse pond (GBP). Vervolgens nemen we die gegevens en rekenen het geconsolideerde bedrag om in Amerikaanse dollars. Hoe kunnen we dit doen?

Als meerdere consolidatieniveaus zijn vereist en andere valuta´s op elk niveau worden gebruikt, moet u de optie **Consolidatie online** gebruiken. Er moeten meerdere consolidatiebedrijven worden gemaakt waarvan de boekhoudings- en aangiftevaluta´s verschillen. De consolidatie moet vervolgens meerdere keren worden uitgevoerd. Met de optie **Financiële rapportage** vindt omrekening altijd plaats van de valuta voor boekhouding van elk bronbedrijf naar de geselecteerde valuta.

7. We hebben dochtermaatschappijen die een ander systeem gebruiken. Hoe kunnen we deze consolideren?

Gebruik de optie **Consolidatie met import** om de saldi in een consolidatiebedrijf te importeren.

8. Sommige van onze dochterondernemingen zijn niet volledig in eigendom. Wat is de beste methode om deze ondernemingen te consolideren?

U hebt meerdere opties voor ondernemingen die gedeeltelijk in eigendom zijn. Als u de optie **Financiële rapportage** gebruikt, kunt u een rapportagestructuurdefinitie en het eigendom definiëren. U kunt ook een berekende rij of kolom gebruiken om het bedrag gedeeltelijk in eigendom voor te stellen. U kunt zelfs het minderheidsbelang als een eigen rij in een rapport weergeven. U kunt ook de optie **Consolidatie online** gebruiken. Het tabblad **Rechtspersonen** heeft de kolom **Eigendom**, waarin u het percentage kunt definiëren dat in bezit is van het moederbedrijf.

9. Onze organisatie moet consolidaties per bedrijfseenheid weergeven of wil de organisatiehiërarchieën gebruiken.

De optie **Financiële rapportage** is de oplossing. Over organisatiehiërarchieën die rechtspersonen of financiële dimensies bevatten, kan in Financiële rapportage worden gerapporteerd. U kunt ook uw eigen hiërarchieën op meerdere niveaus maken met behulp van een rapportagestructuurdefinitie die een combinatie van rechtspersonen en dimensiewaarden heeft.

10. We hebben meer dan één exemplaar van het systeem.

Als u de optie **Bedrijfssaldi exporteren** gebruikt om vanuit één exemplaar te exporteren en vervolgens de optie **Consolidatie met import** in het andere exemplaar gebruikt, kunt u de gegevens consolideren.

11. Kan ik een consolidatie maken met mijn budget in de status **CONCEPT**? 
            
U kunt uw budgetten niet verwerken of voltooien in het consolidatiebedrijf. Het is raadzaam Financial Reporting te gebruiken om conceptbudgetten te consolideren.

Zie [Herwaardering van valuta in een consolidatiebedrijf](../general-ledger/currency-revaluation-consolidation-company.md) voor meer informatie.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
