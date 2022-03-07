---
title: Leaserapporten voor activa
description: In dit onderwerp vindt u een beknopt overzicht van de rapporten die beschikbaar zijn voor de leasing van activa.
author: moaamer
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 085027c5cc823beec99779791ff471dceb4ec8fe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814099"
---
# <a name="asset-leasing-reports"></a>Leaserapporten voor activa

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u een beknopt overzicht van de rapporten die beschikbaar zijn voor de leasing van activa. De meeste rapporten worden weergegeven door het voltooien van deze stappen of stappen die hiermee vergelijkbaar zijn. 

- Als u leaserapporten voor activa wilt weergeven, gaat u naar **Activa leasen > Query's en rapporten > Leaserapporten** en selecteert u een rapport dat u wilt weergeven. Voor de rapporten waarvoor een ander pad is vereist, worden de stappen voor het openen van het rapport opgenomen in de beschrijving van dat rapport. 
- Wanneer u een rapport selecteert om af te drukken, wordt er een pagina met parameters geopend waarmee u de informatie die in het rapport is opgenomen, kunt filteren. Voer filtercriteria in en selecteer **OK** om het rapport te genereren. In het gegenereerde rapport worden gegevens weergegeven die binnen de opgegeven filters vallen.

## <a name="asset-movement"></a>Activummutatie
Het rapport Activamutaties dient als voortschrijdend prognoserapport voor de saldi van de activa met gebruiksrecht voor elke lease. Met dit rapport kunt u de activatransacties van een lease tijdens een opgegeven periode weergeven. Het rapport bevat de volgende velden. 

|     Rapportvelden                  |     Beschrijving                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Begindatum              |     De begindatum van de oudste versie van de lease.                     |   
|     Leasetermijn                     |     De leasetermijn van de oudste versie van de lease.                            |
|     Kortlopende lease               |     Als de lease is geclassificeerd als een lease voor een korte termijn, wordt dit weergegeven als **Ja**.         |
|     Lease met geringe waarde                |     Als de lease is geclassificeerd als een lease met geringe waarde, wordt dit weergegeven als **Ja**.          |
|     Initieel activum met gebruiksrecht     |     De oorspronkelijke waarde van het activum met gebruiksrecht uit de eerste journaalpost voor toerekening.      |
|     Beginsaldo              |     De nettoboekwaarde van het activum met gebruiksrecht vanaf de **Begindatum**.                         |
|     Periodieke afschrijvingskosten    |     Het bedrag aan afschrijvingskosten binnen het datumbereik dat is gedefinieerd voor het rapport.        |
|     Samengevoegde afschrijving       |     Het bedrag van de samengevoegde afschrijving vanaf de **Begindatum**.                               |
|     Waardevermindering                     |     Het bedrag waarmee de waarde van het activum is verminderd binnen het datumbereik dat is gedefinieerd voor het rapport.               |
|     Wijzigingen                  |     Het aantal aanpassingen aan het activum met gebruiksrecht tussen datumparameters.                            |
|     Nettoboekwaarde                 |     De laatste nettoboekwaarde van het activum met gebruiksrecht. Dit is het netto bedrag van de gecumuleerde afschrijving vanaf de **Einddatum**.    |

## <a name="differences-report"></a>Verschillenrapport
In het Verschillenrapport staan de verschillen tussen de gegevens die zijn geladen in het raamwerk voor het importeren van leases en de informatie die zich momenteel in het systeem bevindt. Hiermee kunt u vergelijken wat is aangepast, bijgewerkt of toegevoegd via het raamwerk voor het importeren van leases.  

De waarden in het rapport zijn afhankelijk van de geselecteerde lease. In het rapport worden alleen die velden weergegeven die verschillen van wat zich momenteel in het systeem bevindt en wat zich in de faseringstabellen bevindt. De oude waarde is wat zich momenteel in het systeem bevindt of wat voorheen in het systeem stond, afhankelijk van het feit of het importproces is uitgevoerd. De nieuwe waarde toont de waarde in de faseringstabel waardoor de oude waarde wordt vervangen.

## <a name="five-years-undiscounted-payment-forecast"></a>Niet-verdisconteerde betalingsprognose voor vijf jaar
Het rapport met de niet-verdisconteerde betalingsprognose voor vijf jaar geeft de verwachte niet-verdisconteerde betalingen die de volgende vijf jaar moeten worden betaald vanaf de datum die is opgegeven in de rapportparameters. Het rapport bevat de volgende velden. 

|     Rapportvelden         |     Beschrijving                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Leasebeschrijving     |     De leasebeschrijving uit de leasekoptekst.                                                      |
|     Lease-id              |     De unieke lease-ID.                                                                              |
|     Boek                  |     Het leaseboek dat is gekoppeld aan de boek-id.                                                         |
|     Classificatie        |     De classificatie van de lease.                                                                  |
|     Boekingslaag         |     De laag waarop deze lease wordt geboekt.                                                         |
|     Valuta              |     De valuta van de lease.                                                                        |
|     Huidig               |     De som van alle leasebetalingen die binnen de komende 12 maanden na de rapporteringsdatum verschuldigd zijn.          |
|     13 - 24 maanden          |     De som van alle leasebetalingen die binnen de komende 13 tot 24 maanden na de rapporteringsdatum verschuldigd zijn.           |
|     25 - 36 maanden          |     De som van alle leasebetalingen die binnen de komende 25 tot 36 maanden na de rapporteringsdatum verschuldigd zijn.           |
|     37 - 48 maanden          |     De som van alle leasebetalingen die binnen de komende 37 tot 48 maanden na de rapporteringsdatum verschuldigd zijn.           |
|     49 - 60 maanden          |     De som van alle leasebetalingen die binnen de komende 49 tot 60 maanden na de rapporteringsdatum verschuldigd zijn.           |
|     Later            |     De som van alle leasebetalingen die binnen of na 61 maanden na de rapporteringsdatum verschuldigd zijn.              |

## <a name="gaap-cash-flows-report"></a>GAAP-cashflowrapport
Het GAAP-rapport voldoet aan de Amerikaanse GAAP-openbaarmakingsplicht die is gespecificeerd in 842-20-50-4(g)(1). Als u dit rapport wilt weergeven, gaat u naar **Activa leasen > Query's en rapporten > Openbaarmakingen > GAAP – kasstromen**. 

|     Rapportvelden                                 |     Beschrijving                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Begindatum <br> Einddatum                        |     Definieert een datumbereik dat wordt gebruikt om de informatie in het rapport te beperken.      |
|     Rechtspersoon                                  |     De rechtspersoon die aan de leases is gebonden.                                      |
|     Leasetype                                    |     De classificatie van de lease als financieel of operationeel.           |
|     Lease-id                                      |     De unieke lease-ID.                                                      |
|     Leasebeschrijving                             |     De leasebeschrijving uit de leasekoptekst.                              |
|     Leaseboek                                    |     Het leaseboek waarnaar de regel verwijst.                        |
|     Boekingslaag                                 |     Elk boek dat is gekoppeld aan vaste activa, is ingesteld voor een bepaalde boekingslaag met een algemeen afschrijvingsdoel.                          |
|     Leasegroep                                   |     De groep waaraan de lease is gekoppeld.                                     |
|     Valuta                                      |     De afkorting voor de gebruikte transactievaluta. Alle rapporten converteren de transactievaluta naar de aangiftevaluta.                      |
|     Financiële leases – operationele kasstromen         |     De som van de totale geboekte variabele betalingen en de totale rentebetalingen die zijn geboekt uit het aflossingsschema tussen de datumparameters.        |
|     Financiële leases – financiële kasstromen           |     De som van de totale betalingen voor de hoofdsom uit het aflossingsschema tussen de datumparameters.       |
|     Operationele leases – operationele kasstromen       |     De som van alle geboekte leasebetalingen en geboekte variabele betalingen tussen de datumparameters.            |

## <a name="lease-balances-forecast"></a>Prognose van leasesaldi
De prognoses voor de leasesaldi worden rechtstreeks opgehaald uit het afschrijvingsschema voor leaseverplichtingen en het afschrijvingsschema voor activa. In het rapport worden de geraamde bedragen van de geprojecteerde leaseverplichtingen en de activa met gebruiksrecht gedurende een bepaalde periode weergegeven, inclusief alle verwachte onkosten voor deze leases. Het rapport bevat de volgende velden.

|     Rapportvelden                 |     Beschrijving                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Beginsaldo             |     Het beginsaldo in het aflossingsschema van de lease voor de periode die de begindatum van het rapport omvat.            |
|     Initiële toerekening           |     Als de begindatum van de lease binnen het datumbereik valt dat is gedefinieerd voor het rapport, wordt in deze kolom de waarde van de passivarekening van de eerste journaalpost voor toerekening weergegeven.      |
|     Betalingen                      |     De som van de leasebetalingen die binnen het datumbereik vallen dat is gedefinieerd voor het rapport.                               |
|     Interesse                      |     De som van de rentelasten voor de lease die binnen het datumbereik vallen dat is gedefinieerd voor het rapport.                    |
|     Eindsaldo                |     De leaseverplichtingen vanaf de **Einddatum**.                                                             |
|     Kortlopende betalingsverplichting          |     Het bedrag van de kortlopende aansprakelijkheid in het afschrijvingsschema van de lease vanaf de **Einddatum**.                           |
|     Langetermijnverplichtingen           |     Het bedrag van de langlopende aansprakelijkheid in het afschrijvingsschema van de lease vanaf de **Einddatum**.                            |
|     Nettoboekwaarde bij aanvang      |     De Nettoboekwaarde bij aanvang in het afschrijvingsschema van de lease voor de periode die de begindatum van het rapport omvat      |
|     Initiële toerekening           |     Als de begindatum van de lease binnen de datumparameters valt dat is gedefinieerd voor het rapport, wordt in deze kolom de waarde van de activarekening van de eerste journaalpost voor toerekening weergegeven.            |
|     Afschrijvingskosten          |     De som van de afschrijvingskosten voor de lease die binnen het datumbereik vallen dat is gedefinieerd voor het rapport.                  |
|     Eindsaldo                |     Het activumsaldo van de lease vanaf de **Einddatum**.                                                              |
|     Correctie eigen vermogen             |     Het beginsaldo min de nettoboekwaarde bij aanvang.                                                             |

## <a name="lease-commencements-report"></a>Rapport met begonnen leases
Het rapport met begonnen leases bevat alle leases die binnen een opgegeven datumbereik zijn begonnen, met het beginsaldo voor verplichtingen en het saldo voor activum met gebruiksrecht. Het rapport bevat de volgende velden. 

|     Rapportvelden                 |     Beschrijving                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Begindatum             |     De datum van de eerste journaalpost voor toerekening die voor die leaseversie is geboekt.         |
|     Initieel leasebedrag      |     Het verplichtingenbedrag van de eerste journaalpost voor toerekening.                                  |
|     Initieel activumbedrag          |     Het activumbedrag van de eerste journaalpost voor toerekening.                                      |

## <a name="lease-modification-report"></a>Rapport met leasewijzigingen
Het rapport met leasewijzigingen geeft alle leases weer die binnen een opgegeven datumbereik zijn gewijzigd. In het rapport wordt ook de gebruiker weergegeven die de lease heeft aangepast en het totale bedrag van de gewijzigde verplichtingen. Het rapport bevat de volgende velden. 

|     Rapportvelden                 |     Beschrijving           |
|---------------------------------  |-------------------------  |
|     Gecorrigeerd door                   |     De gebruikersnaam van de persoon die de lease heeft gewijzigd.                                |
|     Correctiedatum               |     De datum weer waarop de correctiejournaalpost is geboekt.                        |
|     Correcties                   |     Het bedrag voor een correctiejournaalpost die is geboekt op de passivarekening van de lease tussen de datumparameters. Credit wordt als positief weergegeven en debet als negatief.       |
|     Winst-/verliesbedrag            |     Het bedrag voor een correctiejournaalpost die is geboekt op de winst-/verliesrekening van de lease tussen de datumparameters. Credit wordt als positief weergegeven en debet als negatief.       |
|     Ingehouden winst             |     Het bedrag voor een correctiejournaalpost die is geboekt op de rekening met ingehouden winst van de lease tussen de datumparameters.      |
|     Eindsaldo van leaseverplichtingen      |     De resulterende leaseverplichtingen vanaf de correctiedatum van de lease.           |

## <a name="lease-movement-report"></a>Rapport Leasemutaties
Het rapport Leasemutaties dient als voortschrijdend prognoserapport voor de saldi van de leaseverplichtingen voor elke lease. Met dit rapport kan de gebruiker de verplichtingentransacties van een lease tijdens een opgegeven periode weergeven.

|     Rapportvelden             |     Beschrijving                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Begindatum         |     De begindatum van de oudste versie van de lease.    |
|     Leasetermijn                |     De leasetermijn van de oudste versie van de lease.           |
|     Resterende betalingen        |     Het aantal betalingen dat nog niet is geboekt voor de lease.                       |
|     Beginsaldo         |     De som van alle transacties die van invloed zijn op de leaseverplichtingen die hebben plaatsgevonden voor de begindatum van het rapport.             |
|     Initiële toerekening       |     Het bedrag van de eerste toerekeningstransactie voor de lease die is geboekt binnen het datumbereik dat is gedefinieerd voor het rapport.     |
|     Betalingen                  |     De som van de betalingstransacties voor de lease die zijn geboekt binnen het datumbereik dat is gedefinieerd voor het rapport. De waarden in deze kolom worden als negatieve bedragen weergegeven wanneer de betalingen het verplichtingensaldo van de lease verminderen.  |
|     Interesse                  |     De som van de rentetoerekeningen die zijn geboekt voor de lease binnen het datumbereik dat is gedefinieerd voor het rapport.            |
|     Correcties               |     De som van de geboekte correctietransacties voor de lease die binnen het datumbereik vallen dat is gedefinieerd voor het rapport.                               |
|     Eindsaldo            |     Het saldo van alle transacties voor leaseverplichtingen die zijn geboekt vanaf de **Einddatum** van het rapport.                  |

## <a name="lease-transactions-report"></a>Rapport Leasetransacties
Met de query Leasetransacties worden alle journaalposten weergegeven die zijn gegenereerd door Activa leasen. Elke journaalboeking wordt gekoppeld aan de boek-id waaruit de boeking afkomstig is. Hierdoor kunt u de journaalboeking eenvoudig aan de overeenkomstige lease koppelen. De query Leasetransacties werkt op een manier die vergelijkbaar is met de pagina **Boekstuktransacties** in het grootboek.

## <a name="weighted-average-discount-rate-report"></a>Rapport Gewogen gemiddelde kortingspercentage
Het rapport Gewogen gemiddelde kortingspercentage voldoet aan de Amerikaanse GAAP-vereiste voor openbaarmaking die is opgegeven in ASC 842-20-50-4(g)(4) voor gewogen gemiddelde kortingspercentage. Als u dit rapport wilt weergeven, gaat u naar **Activa leasen > Query's en rapporten > Gewogen gemiddelde kortingspercentage**. Het rapport bevat de volgende velden. 

|     Rapportvelden                     |     Beschrijving                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Begindatum                        |     In dit rapport worden alle leases opgenomen die zijn begonnen op of vóór de parameter **Begindatum**. Dit rapport moet worden uitgevoerd vanaf de laatste dag van de periode die openbaar moet worden gemaakt.      |
|     Rechtspersoon                      |     De rechtspersoon die aan de lease is gebonden.                           |
|     Lease-id                          |     De unieke lease-ID.                                                  |
|     Leasebeschrijving                 |     De leasebeschrijving uit de leasekoptekst.                          |
|     Boek                              |     Het specifieke boektype van de weergegeven lease.                                                                                                                                            |
|     Boekingslaag                     |     Elk boek dat is gekoppeld aan vaste activa, is ingesteld voor een bepaalde boekingslaag met een algemeen afschrijvingsdoel.      |
|     Leasegroep                       |     De groep waartoe de lease behoort.                                 |
|     Kortingspercentage                     |     Het tarief dat wordt gebruikt voor kortingen van leasebetalingen.                             |
|     Valuta                          |     De afkorting voor de gebruikte transactievaluta. Alle rapporten converteren de transactievaluta naar de aangiftevaluta.  |
|     Resterende leasebetalingen          |     Het totale bedrag aan onbetaalde leasebetalingen uit het betalingsschema dat resteert vanaf de **Begindatum**.            |
|     Gewogen resterende betalingen       |     De resterende leasebetalingen vermenigvuldigd met het gebruikte kortingspercentage.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]