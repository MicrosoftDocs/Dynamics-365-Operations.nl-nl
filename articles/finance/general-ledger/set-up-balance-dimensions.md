---
title: Hoe stel ik financiële dimensies salderen in?
description: In dit onderwerp worden de opties beschreven voor het instellen en gebruiken van de functie Financiële dimensies salderen.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: cb3033a615200a358c1b28b0991bae4b84470ae0
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720106"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Hoe stel ik financiële dimensies salderen in?

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de opties beschreven voor het instellen en gebruiken van de functie Financiële dimensies salderen.

## <a name="symptom"></a>Symptoom

Er zijn twee opties voor het instellen van de saldering van financiële dimensies. De eerste optie is het gebruik van het veld **Financiële dimensie salderen**  op de pagina **grootboekinstelling**  (**Grootboek \> Instelling grootboek \> Grootboek**). De tweede optie is om het veld **Vereisen dat de dimensie gesaldeerd is** te gebruiken op de pagina **Financiële dimensies** (**Grootboek > Rekeningschema \> Dimensies \> Financiële dimensiesets**). In dit onderwerp wordt het verschil tussen deze twee opties uitgelegd.

## <a name="resolution"></a>Oplossing

Organisaties maken meestal gebruik van salderingsdimenssie om een balans te genereren die op het niveau van de financiële dimensies in balans is. Als u een van deze functies inschakelen, worden geboekte niet-gesaldeerde dimensies niet in balans gebracht. U moet eerst handmatig aanpassingsposten invoeren om de balans in balans te brengen voordat u een van deze functies inschakelen.

Deze twee opties sluiten elkaar uit. De optie die in uw organisatie wordt gebruikt, moet zijn gebaseerd op uw bedrijfsbehoeften. We hebben vaak te maken met klanten die de salderingsdimensie definiëren in de grootboekinstellingen en de financiële dimensie-instellingen en vervolgens enkele of alle aanvullende instellingen die nodig zijn voltooien. Ze kunnen echter nog steeds niet worden geboekt vanwege een onevenwicht op het niveau van de financiële dimensie.

In de volgende secties worden de twee opties beschreven en uitgelegd hoe u deze in moet stellen.

### <a name="ledger--balancing-financial-dimension"></a>Grootboek - Een salderende financiële dimensie gebruiken

De salderende dimensie op de **grootboekinstellingspagina** wordt gebruikt om interunit-boekhouding in te stellen. Volg deze stappen om de functionaliteit in te schakelen.

1. Bepaal welke financiële dimensie de salderende dimensie is.

    - Met deze functionaliteit kunt u slechts één financiële dimensie selecteren als de salderende dimensie.
    - De dimensie moet nog niet worden geselecteerd op de pagina **Grootboekinstellingen**.
    - Zorg ervoor dat uw balans al gesaldeerd is voor de geselecteerde financiële dimensie.

2. Werk de rekeningstructuur voor de salderende financiële dimensie bij.

    - De salderende financiële dimensie moet worden opgenomen in alle rekeningstructuren die aan het grootboek zijn toegewezen.
    - De financiële dimensie mag geen lege plekken in de rekeningstructuur toestaan. Deze beperking zorgt ervoor dat elke boeking in de boekhouding die naar het grootboek wordt geboekt, een financiële dimensiewaarde bevat. Een lege dimensie is niet geldig wanneer salderende dimensies worden gebruikt.

3. Definieer op de pagina **Rekeningen voor automatische transacties** (**Grootboek \> Boekingsinstellingen \> Rekeningen voor automatische transacties**) de interunit debet- en krediethoofdrekeningen.
4. Selecteer op de instellingenpagina **Grootboek** (**Grootboek \> Grootboekinstellingen \> Grootboek**) in het veld **Financiële dimensie** balanceren een financiële dimensie die u wilt gebruiken voor de saldering.

Als de geselecteerde financiële dimensie niet gesaldeerd is wanneer transacties worden ingevoerd en geboekt, worden de debet- of kredietboekingen die nodig zijn om de boeking te salderen te brengen tijdens het boeken automatisch toegevoegd. De debet- en krediet-grootboekrekeningen voor de interunittransactie worden weergegeven op het geboekte boekstuk in het grootboek. Deze worden echter niet weergegeven in de journalen of brondocumenten waar de boekingen in de boekhouding voor zijn geboekt.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Financiële dimensies – Vereisen dat de dimensie gesaldeerd is

Hoewel de salderende dimensie op de pagina **Financiële dimensies** meestal wordt gebruikt door bedrijven uit de publieke sector, is de functionaliteit niet gekoppeld aan een configuratiesleutel voor de publieke sector. Aangezien het systeem geen beperking heeft, kunt u deze functionaliteit gebruiken, zelfs als uw organisatie geen entiteit uit de publieke sector is.

Deze functionaliteit wordt meestal gebruikt in het klantenbestand voor de publieke sector, omdat boekingsdefinities moeten worden gebruikt om elke transactie automatisch in balans te brengen. Het gebruikt niet de debet- en kredietrekeningen voor interunit die zijn gedefinieerd op de pagina  **Rekeningen voor automatische transacties** om de boekingen in de boekhouding automatisch te salderen. Als een boekhoudpost niet gesaldeerd is op dimensieniveau nadat de boekdefinities zijn toegepast, wordt de transactie niet geboekt, ook niet als de debet- en kredietrekeningen voor interunit zijn gedefinieerd.

We hebben vaak te maken met klanten die de salderingsdimensie definiëren in de instellingen van het grootboek en de financiële dimensie. In dit geval gebruikt het systeem de functionaliteit voor financiële dimensies. De instellingen voor het salderen van dimensies op het niveau van financiële dimensies hebben prioriteit tijdens het boeken. Het boeken mislukt als de boekdefinitie geen gesaldeerde boekhoudingspost maakt op het niveau van financiële dimensies.

Volg deze stappen om het gebruik van een gesaldeerde dimensie op het niveau van financiële dimensies in te schakelen.

1. Bepaal welke financiële dimensies de salderende dimensies zijn.

    - U kunt meer dan één financiële dimensie instellen als salderende dimensie.
    - Stel de financiële dimensies die nodig zijn om een transactie te salderen nog niet in op de pagina **Financiële dimensies**.

2. Definieer de boekingsdefinities voor elk type journaal of brondocument dat door uw organisatie wordt gebruikt. Bij boekingsdefinities worden de grootboekrekeningen uit een niet-boekingsjournaal of brondocument gebruikt als 'matchcriteria'. De boekdefinitie retourneert vervolgens de 'gegenereerde vermeldingen' die de boeking in de boekhouding worden. Als de boekdefinitie juist is ingesteld, bevat de gegenereerde vermelding de matchcriteria in het grootboek, plus extra rekeningen om de boeking in de boekhouding op dimensieniveau te salderen. Zie voor meer informatie [Boekingsdefinities](posting-definitions.md). 
   
   Boekingsdefinities worden niet ondersteund voor elk type transactie. Boekingsdefinities kunnen bijvoorbeeld niet worden gedefinieerd voor transacties die worden ingevoerd via het algemeen journaal of het vaste-activajournaal. Als een boekingsdefinitie niet kan worden gedefinieerd voor een journaal of brondocument, moet de transactie handmatig gesaldeerd zijn tegen de waarde van financiële dimensie. Als er bijvoorbeeld een algemene journaalboeking wordt gemaakt en de afdelingsdimensie de salderende dimensie is, moet u ervoor zorgen dat elke afdelingswaarde in balans is.  Als de dimensie niet voor elke afdelingswaarde gesaldeerd is, wordt het boekstuk pas gecorrigeerd als het onevenwicht is gecorrigeerd door handmatig een debet- of kredietwissel voor interunit aan het boekstuk toe te voegen. 

    > [!IMPORTANT]
    > Als een te groot aantal transacties handmatig moet worden gesaldeerd, mag u de salderende dimensiefunctionaliteit **niet** gebruiken op de pagina **Financiële dimensies**. Gebruik in plaats daarvan de salderende dimensiefunctionaliteit op de instellingspagina voor **Grootboek**.

3. Nadat boekingsdefinities zijn gedefinieerd, kunnen de financiële dimensies worden gemarkeerd als vereist voor saldering.

Tijdens het boeken worden de boekdefinities tijdens het boeken aangeroepen om de boekingen in de boekhouding te bepalen. Als de financiële dimensies gesaldeerd zijn, vindt validatie plaats nadat de boekhoudregels zijn bepaald. Als de financiële dimensies niet gesaldeerd zijn, wordt de transactie niet geboekt en ontvangt u een bericht waarin wordt melding gemaakt dat de debetbetalingen niet gelijk zijn aan het krediet voor een bepaalde dimensie.
