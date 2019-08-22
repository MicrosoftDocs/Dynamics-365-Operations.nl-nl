---
title: Crediteringen en aanmaningen in Klanten
description: De gegevens van klantaanmaningen worden in één centrale weergave beheerd, namelijk de pagina Microsoft Dynamics 365 for Finance and Operations Aanmaningen. Credit- en incassomanagers kunnen deze centrale weergave gebruiken om aanmaningen te beheren. Incassomedewerkers kunnen het incassoproces starten vanuit klantlijsten die worden gegenereerd met de vooraf gedefinieerde incassocriteria, of vanuit het formulier Klanten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 975988babe2f05adf9179de8d87c8ff216ec59a7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836815"
---
# <a name="credit-and-collections-in-accounts-receivable"></a>Crediteringen en aanmaningen in Klanten

[!include [banner](../includes/banner.md)]

Gegevens van klantincasso's worden beheerd in één centrale weergave, met behulp van de Finance and Operations-pagina Incasso's. Credit- en incassomanagers kunnen deze centrale weergave gebruiken om aanmaningen te beheren. Incassomedewerkers kunnen het incassoproces starten vanuit klantlijsten die worden gegenereerd met de vooraf gedefinieerde incassocriteria, of vanuit het formulier Klanten.

Voordat u aanmaningen gaat instellen of hiermee gaat werken, moet u vertrouwd zijn met de volgende concepten:
-   Ouderdomsmomentopnamen voor klanten bevatten saldogegevens die zijn gerangschikt naar ouderdom
-   Klantverzamelingen voor aanmaningen helpen u uw werk te organiseren
-   Incassomedewerkers kunnen hun eigen klantverzamelingen hebben
-   Met lijstpagina's worden klanten, activiteiten en gevallen voor aanmaningen georganiseerd
-   Alle aanmaningsgegevens voor een klant bevinden zich op één pagina en u kunt vanuit die pagina actie ondernemen
-   Rente en kosten kunnen in één stap worden kwijtgescholden, opnieuw worden ingevoerd of worden teruggedraaid
-   Afschrijvingstransacties kunnen in één stap worden uitgevoerd
-   Betalingen met ontoereikend saldo kunnen in één stap worden verwerkt

In de onderstaande secties wordt elk concept beschreven.

## <a name="customer-aging-snapshots"></a>Ouderdomsmomentopnamen voor klanten 
Een ouderdomsmomentopname bevat de berekende saldi die zijn gerangschikt naar ouderdom, voor een klant op een bepaald tijdstip. Deze informatie wordt weergegeven op de lijstpagina Vervallen saldi en op de pagina Aanmaningen. Een ouderdomsmomentopname moet worden gemaakt, voordat u gegevens op de lijstpagina's Aanmaningen kunt bekijken. 

Een ouderdomsmomentopname bevat voor elke klant een kop voor de ouderdomsmomentopname en detailrecords die overeenkomen met elke ouderdomsperiode in de ouderdomsperiodedefinitie. 

De kop van de ouderdomsmomentopname bevat het totale verschuldigde bedrag, de kredietlimiet, het bedrag van de pakbon, het bedrag van de verkooporder, het aantal geschiltransacties en het totale bedrag van de geschiltransacties voor de klantrekening. Alle transacties voor de klant worden meegenomen bij de berekening van deze bedragen. Het totale verschuldigde bedrag, de kredietlimiet, het bedrag van de pakbon en het bedrag van de verkooporder worden weergegeven in het feitenvak Kredietinformatie op de pagina Aanmaningen. 

Voor elke ouderdomsperiode in de ouderdomsperiodedefinitie wordt een ouderdomsmomentopnamedetailrecord gemaakt. Elke ouderdomsmomentopnamedetailrecord bevat de ouderdomsperiode-ID en het totaalbedrag van de transacties met datums die binnen de ouderdomsperiode vallen. Transacties worden toegewezen aan een ouderdomsperiode, zoals 30 dagen na de vervaldatum. De datum is relatief ten opzichte van de datum Ouderdom vanaf die wordt opgegeven als u de ouderdomsmomentopname maakt. Deze informatie wordt weergegeven op de lijstpagina Vervallen saldi en in het feitenvak Vervallen saldi.

## <a name="collections-customer-pools"></a> Klantverzamelingen voor aanmaningen 
Klantverzamelingen zijn query's waarmee een groep klantrecords wordt gedefinieerd die kan worden weergegeven en beheerd voor aanmaningen of ouderdomsrangschikkingprocessen. Met klantverzamelingen kunt u gegevens filteren op de pagina's Vervallen saldi, Incassoactiviteiten en Aanmaningen. U kunt klantverzamelingen ook gebruiken om de klantrekeningen te filteren, die worden opgenomen bij de aanmaak van ouderdomsmomentopnamen.

## <a name="collections-agents"></a>Incassomedewerkers
Gebruikers van Microsoft Dynamics 365 for Finance and Operations kunnen standaard alle klantgegevens op lijstpagina's met aanmaningen weergeven. U kunt incassomedewerkerrecords gebruiken om te bepalen welke klantverzamelingen beschikbaar zijn voor het filteren van gegevens op de lijstpagina's met aanmaningen en op de pagina Aanmaningen. 

Een incassomedewerker is een persoon die met klanten samenwerkt om ervoor te zorgen dat de betalingen op tijd worden geïnd. In Finance and Operations zijn incassomedewerkers werknemers die worden toegewezen aan gebruikers op de pagina Gebruikersinstellingen.

## <a name="collections-list-pages"></a> Lijstpagina's met aanmaningen 
Met de volgende lijstpagina's kunt u gegevens over aanmaningen organiseren.
-   Vervallen saldi – In de kolommen op de lijstpagina worden klantsaldi en op ouderdom gerangschikte bedragen op ouderdomsperiode weergegeven. Deze gegevens worden opgeslagen in een ouderdomsmomentopname. De ouderdomsperioden worden bepaald door de ouderdomsperiodedefinitie die wordt gebruikt. De ouderdomsperiodedefinitie is afkomstig van de klantverzameling, als er één is opgegeven voor de verzamelingquery. Als de klantverzameling geen ouderdomsperiodedefinitie heeft, wordt de standaardouderdomsperiodedefinitie gebruikt die wordt opgegeven op de pagina Parameters van module Klanten. Als geen standaardouderdomsperiodedefinitie is opgegeven, wordt de eerste ouderdomsperiodedefinitie op de pagina Ouderdomsperiodedefinities gebruikt.
-   Incassoactiviteiten – In de kolommen op de lijstpagina worden activiteiten weergegeven die zijn geïdentificeerd als incassoactiviteiten. Deze activiteiten worden gemaakt met de pagina Aanmaningen. Gebruik activiteiten om de werkzaamheden met betrekking tot aanmaningen bij te houden.
-   Incassoaanvragen – In de kolommen op de lijstpagina worden gegevens weergegeven voor gevallen van het type Aanmaningen.

> [!NOTE]
> Een ouderdomsmomentopname moet worden gemaakt, voordat u gegevens op deze lijstpagina's kunt bekijken. Er worden alleen gegevens weergegeven voor klanten voor wie een ouderdomsmomentopname is gemaakt. De records die op de lijstpagina worden weergegeven, kunnen als volgt worden gefilterd:
> <li>Een Finance and Operations-gebruiker heeft standaard toegang tot alle klanten die een ouderdomsmomentopname hebben.</li>
> <li>Als er klantverzamelingen bestaan, moet een gebruiker als incassomedewerker zijn ingesteld om de verzamelingen te gebruiken om gegevens op de lijstpagina's met aanmaningen te filteren. De gegevens zijn beperkt tot de klanten die zijn opgenomen in de geselecteerde klantverzameling.</li>
> <li>Als een gebruiker is ingesteld als incassomedewerker, bevat de lijstpagina alleen de verzamelingen die zijn geselecteerd voor die incassomedewerker. Als de schakeloptie Medewerker toestaan alle klantverzamelingen te bekijken is geselecteerd op de pagina Incassomedewerker voor de incassomedewerker, zijn alle verzamelingen beschikbaar voor die medewerker.</li>


## <a name="collections-page"></a> Pagina Aanmaningen
Gebruik de pagina Aanmaningen om aanmaningsgegevens, activiteiten en gevallen voor een klant te bekijken en te beheren en hiervoor actie te ondernemen. 

In het bovenste deelvenster worden aanvragen voor de geselecteerde klant weergegeven. In het middelste deelvenster worden transacties voor de klant weergegeven. In het onderste deelvenster worden activiteiten voor de klant weergegeven. U kunt aanmaningsgevallen maken om aanmaningsgegevens bij te houden voor een of meer transacties en activiteiten. De gegevens in het bovenste en onderste deelvenster kunnen op geval worden gefilterd. 

In feitenblokken worden vervallen saldi en kredietlimietgegevens voor de geselecteerde klant weergegeven. Deze gegevens worden opgeslagen in de ouderdomsmomentopname. U kunt de ouderdomsmomentopname zo nodig bijwerken met actuele gegevens. 

Het actiedeelvenster bevat knoppen waarmee u verwante informatie voor de geselecteerde klant, geval, transactie of activiteit kunt weergeven. Ook kunt u algemene acties uitvoeren, zoals de incassostatus van een transactie wijzigen, e-mails versturen door de integratie met uw e-mailprovider, klanten terugbetalen, betalingen met ontoereikend saldo verwerken en saldi afschrijven die niet kunnen worden geïnd.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Rente en bijzondere kosten kwijtschelden, opnieuw invoeren of omkeren 
U kunt rentenota's, of kosten en de transactierente die deel uitmaken van rentenota's kwijtschelden, opnieuw invoeren of terugdraaien. U kunt dit doen vanaf het tabblad Incasso in het actievenster op de lijstpagina Alle klanten door op Rentenota, Transactierente of Bijzondere kosten te klikken. 

Deze correcties zijn alleen van invloed op rentenota's en de bijbehorende rente en kosten. Gebruik de stappen in de sectie 'Afschrijvingstransacties kunnen in één stap worden gemaakt' om alle kosten van een klant af te schrijven.

Zie voor meer informatie [Een rentecode met een bereik maken](tasks/create-interest-code-range.md) en [Rente verwerken](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Afschrijvingstransacties maken
U kunt oninbare schulden afschrijven door te klikken op Afschrijven in het formulier Aanmaningen en op de lijstpagina's Vervallen saldi, Klanten en Openstaande klantfacturen. 

Wanneer u transacties voor een klant afschrijft, worden alle transacties voor de klant automatisch voor vereffening gemarkeerd. Welk bedrag wordt afgeschreven, is afhankelijk van het nettobedrag van de gemarkeerde transacties. De afschrijvingstransactie wordt gemaakt in een algemeen journaal en kan maximaal drie typen journaalregels bevatten.

-   Het eerste type journaalregel bevat de afschrijvingsvermelding van de klant. Als de gemarkeerde transacties meerdere combinaties van valutacode, dimensie en boekingsprofiel bevatten, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt.
-   Het tweede type journaalregel bevat de afschrijvingsvermelding van het grootboek. Als de gemarkeerde transacties meerdere combinaties van valutacode, dimensie en boekingsprofiel bevatten, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt.
-   Het derde type journaalregel bevat de grootboekafschrijvingsgegevens voor btw. Deze journaalregel wordt alleen gemaakt als de schakeloptie Btw apart is ingeschakeld op de pagina Parameters van module Klanten. Als de gemarkeerde transacties meerdere combinaties bevat van rekening voor te betalen btw, dimensie en btw-code, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt.

De afschrijvingstransactie wordt gemaakt in de transactievaluta.

Zie voor meer informatie [Een afschrijvingsjournaal voor een klant maken](tasks/create-write-off-journal-customer.md).

<a name="process-not-sufficient-funds-nsf-payments"></a>Betalingen met ontoereikend saldo verwerken  
--------------------------------------------

U kunt betalingen met ontoereikend saldo verwerken door op Betaling met ontoereikend saldo op de pagina Aanmaningen te klikken. Wanneer u op deze knop klikt, wordt de betaling geannuleerd. Als er kosten voor een betaling met ontoereikend saldo voor de klant van toepassing zijn, wordt een toeslagentransactie gemaakt in een betalingsjournaal. Het bedrag van de kosten is gebaseerd op de instellingen voor de automatische toeslagen. De automatische toeslagen die van toepassing zijn voor betalingen met ontoereikend saldo, zijn opgegeven bij de groep toeslagen die is geselecteerd op de pagina Bankrekeningen voor de betreffende bankrekening.





