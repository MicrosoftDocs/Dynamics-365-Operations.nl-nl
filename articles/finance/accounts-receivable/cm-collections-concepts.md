---
title: Basisbegrippen voor incassobeheer
description: In de onderwerpen worden belangrijke basisbegrippen voor incassobeheer gedefinieerd.
author: mikefalkner
manager: AnnBe
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8bee320beb411a5ee0829a0e3170de0c7f293172
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441929"
---
# <a name="collections-management-key-concepts"></a>Basisbegrippen voor incassobeheer

[!include [banner](../includes/banner.md)]

Voordat u incasso's gaat configureren of gebruiken, moet u vertrouwd zijn met de volgende concepten:

- Ouderdomsmomentopnamen voor klanten bevatten informatie over vervallen saldi op een bepaald moment in de tijd.
- Klantverzamelingen voor incasso's helpen u uw werk te organiseren.
- Incassomedewerkers kunnen hun eigen klantverzamelingen hebben.
- Met lijstpagina's worden klanten, activiteiten en gevallen voor incasso's georganiseerd.
- Alle incassogegevens voor een klant bevinden zich op één pagina en u kunt vanuit die pagina actie ondernemen.
- Rente en kosten kunnen in één stap worden kwijtgescholden, opnieuw worden ingevoerd of worden teruggedraaid.
- Afschrijvingstransacties kunnen in één stap worden gemaakt.
- Betalingen met onvoldoende fondsen kunnen in één stap worden verwerkt.

In dit onderwerp wordt elk concept beschreven.

## <a name="customer-aging-snapshots"></a>Ouderdomsmomentopnamen voor klanten 

Een ouderdomsmomentopname bevat de berekende saldi die zijn gerangschikt naar ouderdom, voor een klant op een specifiek tijdstip. Deze informatie wordt weergegeven op de lijstpagina **Vervallen saldi** en de pagina **Incasso's**. Er moet een ouderdomsmomentopname worden gemaakt voordat u gegevens kunt bekijken op de lijstpagina's met incasso's (**Naar ouderdom gerangschikte saldi**, **Incassoactiviteiten** en **Incassocases**).

Een ouderdomsmomentopname heeft voor elke klant een kop voor de ouderdomsmomentopname en detailrecords die overeenkomen met elke ouderdomsperiode in de ouderdomsperiodedefinitie.

De kop van de ouderdomsmomentopname bevat het totale bedrag dat achterstallig is, de kredietlimiet, het bedrag van de pakbon, het bedrag van de verkooporder, het aantal geschiltransacties en het totale bedrag van de geschiltransacties voor de klantrekening. Alle transacties voor de klant worden meegenomen bij de berekening van deze bedragen. Het totale bedrag dat achterstallig is, de kredietlimiet, het bedrag van de pakbon en het bedrag van de verkooporder worden weergegeven in het feitenvak **Kredietinformatie** op de pagina **Incasso's**.

Voor elke ouderdomsperiode in de ouderdomsperiodedefinitie wordt een detailrecord gemaakt in de ouderdomsmomentopname. Elke detailrecord bevat de id van de ouderdomsperiode en het totaalbedrag van de transacties die datums hebben die binnen de ouderdomsperiode vallen. Transacties worden toegewezen aan een ouderdomsperiode, zoals 30 dagen na de vervaldatum. De datum is relatief ten opzichte van de datum **Ouderdom vanaf** die u opgeeft wanneer u de ouderdomsmomentopname maakt. Deze informatie wordt weergegeven op de lijstpagina **Vervallen saldi** en in het feitenvak **Vervallen saldi** op de pagina **Incasso's**.

## <a name="collections-customer-pools"></a>Klantverzamelingen voor Incasso's

Klantverzamelingen zijn query's waarmee een groep klantrecords wordt gedefinieerd. U kunt deze gegroepeerde records gebruiken om informatie weer te geven over de klantrekeningen die zijn opgenomen en om incasso's of ouderdomsprocessen voor hen te beheren. Met klantverzamelingen kunt u gegevens filteren op de lijstpagina's voor incasso's. U kunt ze ook gebruiken om de klantrekeningen te filteren die zijn opgenomen bij het maken van ouderdomsmomentopnamen.

## <a name="collections-agents"></a>Incassomedewerkers

Gebruikers kunnen standaard alle klantgegevens op de lijstpagina's met incasso's weergeven. Met incassomedewerkerrecords kunt u bepalen welke klantverzamelingen kunnen worden gebruikt voor het filteren van gegevens op de lijstpagina's met incasso's en de pagina **Incasso's**.

Incassomedewerkers werken samen met klanten om ervoor te zorgen dat betalingen op tijd worden geïnd. Het zijn medewerkers die aan gebruikers worden toegewezen op de pagina **Gebruikersinstellingen**.

## <a name="collections-list-pages"></a>Lijstpagina's met incasso's

De volgende lijstpagina's helpen u om gegevens over incasso's te organiseren:

- **Vervallen saldi**: in de kolommen op deze lijstpagina ziet u klantsaldi en op ouderdom gerangschikte bedragen op ouderdomsperiode. Deze gegevens worden opgeslagen in een ouderdomsmomentopname. De ouderdomsperioden worden bepaald door de ouderdomsperiodedefinitie die wordt gebruikt. De ouderdomsperiodedefinitie is afkomstig uit de klantverzameling, als er een klantverzameling voor de verzamelingquery is opgegeven. Als de klantverzameling geen ouderdomsperiodedefinitie heeft, wordt de standaardouderdomsperiodedefinitie gebruikt die is opgegeven op de pagina **Parameters van module Klanten**. Als geen standaardouderdomsperiodedefinitie is opgegeven, wordt de eerste ouderdomsperiodedefinitie op de pagina **Ouderdomsperiodedefinities** gebruikt.
- **Incassoactiviteiten**: in de kolommen op deze lijstpagina worden activiteiten weergegeven die zijn geïdentificeerd als incassoactiviteiten. Deze activiteiten worden gemaakt op de pagina **Incasso's**. U gebruikt activiteiten om het incasso-gerelateerde werk dat u doet, bij te houden.
- **Incassocases**: in de kolommen op deze lijstpagina wordt informatie weergegeven die behoort tot een casecategorie met het casetype **Incasso's**.

### <a name="aging-snapshots"></a>Ouderdomsmomentopnamen

Een ouderdomsmomentopname moet worden gemaakt voordat u gegevens op de lijstpagina's met incasso's kunt bekijken. Er worden alleen gegevens weergegeven voor klanten voor wie een ouderdomsmomentopname is gemaakt. De records die op de lijstpagina worden weergegeven, kunnen verder als volgt worden gefilterd:

- Gebruikers hebben standaard toegang tot alle klanten die een ouderdomsmomentopname hebben.
- Als er klantverzamelingen bestaan, moet een gebruiker als incassomedewerker zijn ingesteld om de verzamelingen te gebruiken om gegevens op de lijstpagina's met incasso's te filteren. De gegevens zijn beperkt tot de klanten die zijn opgenomen in de geselecteerde klantverzameling.
- Als een gebruiker is ingesteld als incassomedewerker, zijn alleen de groepen die voor die incassomedewerker zijn geselecteerd, beschikbaar op de incassolijstpagina's. Als de optie **Medewerker toestaan alle klantverzamelingen te bekijken** op de pagina **Incassomedewerker** voor de incassomedewerker is geselecteerd, zijn alle verzamelingen beschikbaar voor die medewerker.

## <a name="collections-page"></a>Pagina Incasso's

U kunt de pagina **Incasso's** gebruiken om incassogegevens, activiteiten en cases voor een klant te bekijken en te beheren en hiervoor actie te ondernemen.

De bovenste sectie van de pagina bevat cases voor de geselecteerde klant, de middelste sectie bevat transacties voor de klant en het onderste sectie bevat activiteiten voor de klant. U kunt incassogevallen maken om incassogegevens bij te houden voor een of meer transacties en activiteiten. De informatie in de bovenste en onderste sectie kan worden gefilterd op case.

Feitenblokken tonen vervallen saldi en kredietlimietgegevens voor de geselecteerde klant. Deze gegevens worden opgeslagen in de ouderdomsmomentopname. Indien nodig, kunt u de ouderdomsmomentopname bijwerken met actuele gegevens.

Het actievenster bevat knoppen waarmee u verwante informatie voor de geselecteerde klant, case, transactie of activiteit kunt weergeven. Ook kunt u algemene acties uitvoeren, zoals de incassostatus van een transactie wijzigen, e-mails versturen door de integratie met uw e-mailprovider, klanten terugbetalen, betalingen met ontoereikend saldo verwerken en saldi afschrijven die niet kunnen worden geïnd.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Rente en bijzondere kosten kwijtschelden, opnieuw invoeren of omkeren

U kunt rentenota's, of de kosten en de transactierente die deel uitmaken van rentenota's, kwijtschelden, opnieuw invoeren of terugdraaien. Ga naar het tabblad **Incasso** in het actievenster van de lijstpagina **Alle klanten** en selecteer **Rentenota**, **Transactierente** of **Bijzondere kosten**.

Deze correcties zijn alleen van invloed op rentenota's en de bijbehorende rente en kosten. Zie de sectie [Afschrijvingstransacties maken](#creating-write-off-transactions) van dit onderwerp voor informatie over het afschrijven van alle kosten die een klant verschuldigd is.

Zie voor meer informatie Een rentecode met een bereik maken en Rente verwerken.

## <a name="creating-write-off-transactions"></a>Afschrijvingstransacties maken

U kunt de oninbare vorderingen afschrijven door **Afschrijven** te selecteren op de pagina **Incasso's** en de incassolijstpagina's.

Wanneer u transacties voor een klant afschrijft, worden alle transacties voor die klant automatisch voor vereffening gemarkeerd. Welk bedrag wordt afgeschreven, is afhankelijk van het nettobedrag van de gemarkeerde transacties. De afschrijvingstransactie wordt gemaakt in een algemeen journaal en kan maximaal drie typen journaalregels bevatten:

- Het eerste type journaalregel bevat de afschrijvingsvermelding van de klant. Als de gemarkeerde transacties meerdere combinaties van valutacodes, dimensies en boekingsprofielen bevatten, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt.
- Het tweede type journaalregel bevat de afschrijvingsvermelding van het grootboek. Als de gemarkeerde transacties meerdere combinaties van valutacodes, dimensies en boekingsprofielen bevatten, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt.
- Het derde type journaalregel bevat de grootboekafschrijvingsgegevens voor btw. Deze journaalregel wordt alleen gemaakt als de **Btw apart** is ingeschakeld op de pagina **Parameters van module Klanten**. Als de gemarkeerde transacties meerdere combinaties bevatten van rekeningen voor te betalen btw, dimensies en btw-codes, wordt voor elke combinatie een afzonderlijke journaalregel gemaakt. De afschrijvingstransactie wordt gemaakt in de transactievaluta. Zie voor meer informatie Een afschrijvingsjournaal voor een klant maken.

## <a name="process-nsf-payments"></a>Betalingen met ontoereikend saldo verwerken

U kunt betalingen met ontoereikend saldo verwerken door **Betaling met ontoereikend saldo** te selecteren op de pagina **Incasso's**. Wanneer u deze knop selecteert, wordt de betaling geannuleerd. Als er kosten voor een betaling met ontoereikend saldo voor de klant van toepassing zijn, wordt een toeslagentransactie gemaakt in een betalingsjournaal. Het bedrag van de kosten is gebaseerd op de instellingen voor de automatische toeslagen. De automatische toeslagen die van toepassing zijn op betalingen met ontoereikend saldo, zijn opgegeven bij de groep toeslagen die is geselecteerd op de pagina **Bankrekeningen** voor de betreffende bankrekening.

## <a name="additional-resources"></a>Aanvullende resources

[Parameters voor klantkredietbeheer instellen](./cm-credit-mgmt-setup.md)

[Informatie over het instellen van klantkredietbeheer](./cm-setup-information.md)

[Informatie over kredietbeheer voor een klant toevoegen](./cm-add-credit-mgmt-information-customer.md)

[Kredietgroepen van klant](./cm-customer-credit-groups.md)

[Kredietlimietcorrecties voor klant](./cm-credit-limit-adjustments.md)

[Kredietblokkeringen voor verkooporders](./cm-sales-order-credit-holds.md)

[Periodieke taken voor klantkredietbeheer](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]