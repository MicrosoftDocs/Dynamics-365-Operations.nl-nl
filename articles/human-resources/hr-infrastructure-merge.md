---
title: Overzicht van infrastructuursamenvoeging voor Dynamics 365 Human Resources
description: In dit artikel wordt de samenvoeging van de Microsoft Dynamics 365 Human Resources-infrastructuur beschreven.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f79ef3ed5db7583eb44b99e49c010778ce8524d1
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733451"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Samenvoeging van Dynamics 365 Human Resources-infrastructuur 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources biedt hulpprogramma's waarmee HR-teams de organisatorische flexibiliteit kunnen vergroten, de werknemerservaring kunnen transformeren en HR-programma's kunnen optimaliseren om een werkplek te creëren die goed is voor mensen en het bedrijf. Zie voor meer informatie over Dynamics 365 Human Resources [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **De werknemerservaring transformeren.** Houd de prestaties op hoog niveau door managers en werknemers meer mogelijkheden te bieden via verbonden selfservice-ervaringen die zorgen voor meer betrokkenheid en groei.
- **HR-programma's optimaliseren.** Verlaag de operationele kosten en maak programma's voor op mensen gebaseerd beheer van verlof en verzuim, tijd, vergoedingen en compensatie.
- **Organisatorische flexibiliteit vergroten.** Stel HR in staat om te werken met de behendigheid die het bedrijf nodig heeft door Dataverse en Microsoft Power Platform te gebruiken om gegevens van personen te centraliseren en Dynamics 365 Human Resources eenvoudig uit te breiden.
- **Inzichten in personeel verkrijgen.** Neem gegevensgestuurde beslissingen via de mogelijkheid om gegevens over personen te analyseren en te visualiseren op uitgebreide dashboards die op elk apparaat beschikbaar zijn.

## <a name="human-resources-infrastructure-merge"></a>Samenvoegen van Human Resources-infrastructuur

Dynamics 365 Human Resources is een zelfstandige toepassing die momenteel een andere infrastructuur gebruikt dan andere apps voor financiën en bedrijfsactiviteiten, zoals Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Door de infrastructuursamenvoeging krijgt Dynamics 365 Human Resources dezelfde infrastructuur als andere apps voor financiële en bedrijfsactiviteiten.

Zie [Samenvoeging van HR-aanbod](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/) voor meer informatie over de samenvoeging van de Human Resources-infrastructuur. Zie [Veelgestelde vragen over samenvoegen van Human Resources-infrastructuur](./hr-infrastructure-merge-faq.md) voor antwoorden op veelgestelde vragen.

## <a name="customer-migration-vs-customer-merge"></a>Klantmigratie en klantsamenvoeging

Als onderdeel van de infrastructuursamenvoeging zijn alle mogelijkheden van de Human Resources-toepassing beschikbaar gemaakt in omgevingen voor financiën en bedrijfsactiviteiten. Klanten kunnen hun Human Resources-omgevingen migreren met de migratieprogramma's die beschikbaar zijn in Microsoft Dynamics Lifecycle Services. Ze kunnen hun gegevens desgewenst ook samenvoegen met de bestaande omgeving voor financiën en bedrijfsactiviteiten. 

Klantenmigraties en klantensamenvoegingen verschillen als volgt van elkaar:

- **Klantmigratie**: het hulpprogramma voor geautomatiseerde migratie wordt gebruikt om een lift-and-shift-migratie (verplaatsing) van de klantendatabase van de Human Resources-infrastructuur naar de infrastructuur voor financiën en bedrijfsactiviteiten uit te voeren. Het resultaat is een nieuwe omgeving voor apps voor financiën en bedrijfsactiviteiten waarin de Human Resources-database van de klant wordt gebruikt. 
- **Klantsamenvoeging**: deze extra stap is niet vereist door Microsoft. Het wordt gedaan naar eigen inzicht en op de eigen tijdlijn van de klant. Tijdens deze stap worden klantgegevens verplaatst naar een bestaande omgeving, zoals een omgeving voor financiën en bedrijfsactiviteiten. Dit is meestal een handmatig proces dat kan worden uitgevoerd met DMF-gegevensentiteiten (Data Management Framework). 

## <a name="planning-a-human-resources-environment-migration"></a>De migratie van een Human Resources-omgeving plannen

Als onderdeel van de samenvoeging van de infrastructuur moeten alle klanten hun bestaande Human Resources-omgevingen migreren vanuit de zelfstandige infrastructuur. Voor dit proces is het raadzaam om de hulpmiddelen voor automatische migratie in Lifecycle Services te gebruiken om uw huidige omgevingen naar de nieuwe infrastructuur te verplaatsen. 

De volgende secties bieden meer details over het gebruik van de Lifecycle Services-hulpprogramma's om een zelfstandige Human Resources-omgeving te migreren. 

Klanten die een migratie plannen, kunnen de volgende verwachtingen hebben:

- Alle klanten moeten een migratie naar een sandbox-omgeving maken voordat de productieomgeving kan worden gemigreerd. 
- Met migratieprogramma's kunt u alleen migraties tussen sandbox-omgevingen en tussen productieomgevingen uitvoeren. Daarom bepaalt uw omgevingstype welke omgeving op de juiste manier kan worden gemigreerd. 
- Klanten kunnen zoveel sandboxes migreren als nodig is voordat ze hun productieomgeving migreren, mits er een doelruimte voor de sandbox beschikbaar is. Klanten kunnen een gemigreerde sandbox ook verwijderen en meerdere keren opnieuw migreren. 
- Als de migratie van een sandbox mislukt of als u opnieuw wilt beginnen, kunt u een omgeving in de infrastructuur voor financiën en bedrijfsactiviteiten verwijderen en dezelfde omgeving opnieuw migreren.
- De URL van uw Human Resources-omgeving is na de migratie anders.
- Plan de juiste hoeveelheid uitvaltijd voor de migratie van uw productieomgeving. De geschatte periode voor voltooiing van het automatische migratieproces is drie tot vier uur. De periode varieert, afhankelijk van de gegevens van uw organisatie. U moet de hoeveelheid tijd valideren die nodig is tijdens de migratie van uw sandbox-omgevingen en tijd vrijmaken voor de extra handmatige taken die moeten worden uitgevoerd.

> [!IMPORTANT] 
> Wanneer een productieomgeving wordt gemigreerd naar de infrastructuur voor financiën en bedrijfsactiviteiten, wordt de zelfstandige bronproductieomgeving automatisch verwijderd. U moet de gemigreerde productieomgeving niet verwijderen. 

Het migratieproces verloopt merendeels automatisch. Uw zakelijke gebruikers moeten echter enkele handmatige stappen uitvoeren en valideren na de migratie.

De volgende handmatige stappen moeten worden voltooid:

- Een nieuw Lifecycle Services-project maken voor de migratie.
- Eventuele integraties in uw oude omgeving naar de nieuwe omgeving reviseren door de integratie naar de nieuwe URL/eindpunten te wijzen, gebaseerd op elke integratieconfiguratie.
- De gegevensopslag vernieuwen voor ingesloten Power BI-rapporten.
- De lijst met gegevensentiteiten vernieuwen vanuit de DMF-werkruimte.
- Een koppeling naar Lifecycle Services opnemen voor ondersteuning.
- Fiscale kalenders maken.

Tijdens het automatische proces worden de volgende acties voltooid en moeten ze worden gevalideerd:

- Gegevens:

    - Configuraties
    - Beveiligingsrollen (inclusief aangepaste rollen)
    - Werkstromen
    - Persoonlijke instellingen en opgeslagen weergaven
    - Transacties
    - Aangepaste velden
    - Bijlagen

- Gegevensbeheer: uw eigen database gebruiken (BYOD).
- Functiebeheer: in-/uitgeschakelde functies.
- Ingesloten Power Apps.
- Aan het Power Platform-beheercentrum gekoppelde omgeving (alleen productie).
- Batchtaken.
- Voor elke rechtspersoon wordt een leeg grootboek gemaakt. Het standaard wisselkoerstype en de valuta voor boekhouding voor elk grootboek zijn ingesteld.
- Er wordt automatisch een nieuw rekeningschema gemaakt en dit wordt gekoppeld aan de pagina **Grootboek** in elke rechtspersoon. De financiële dimensies die in uw Human Resources-omgeving zijn geconfigureerd, worden automatisch toegevoegd aan een nieuwe rekeningstructuur en aan het grootboek gekoppeld. 

> [!NOTE]
> Als onderdeel van het Dynamics 365 Finance-product is een grootboek vereist voor de infrastructuur voor financiën en bedrijfsactiviteiten. De controller voor aangepaste dimensies die in de zelfstandige Dynamics 365 Human Resources-toepassing bestond, is niet beschikbaar. De samengevoegde infrastructuur voor Human Resources is afhankelijk van de logica van Finance om financiële dimensies weer te geven in de module **Human Resources**. [Hier](../finance/general-ledger/plan-chart-of-accounts.md) vindt u meer informatie over het rekeningschema en financiële dimensies. 

## <a name="considerations"></a>Overwegingen

- Migratie naar omgevingen wordt altijd opgenomen in de meest recente algemeen beschikbare (GA) versie. Afhankelijk van uw migratie en testplan is het raadzaam om een sandbox-migratie te valideren op dezelfde versie als uw productieomgeving als uw migratievalidatie voor sandbox-omgevingen op een andere versie is uitgevoerd. 
- Tijdens de migratie worden de gemigreerde omgevingen in dezelfde regio geplaatst als de zelfstandige Human Resources-bronomgevingen.

## <a name="licensing"></a>Licenties

Er zijn geen wijzigingen in licenties voor Dynamics 365 Human Resources op de volgende gebieden: 

- **Vereiste voor aanschaf van minimum aantal licenties**
- **Licenties voor een productieomgeving en een sandbox-omgeving**: als u bestaande zelfstandige Human Resources-licenties hebt voor één productieomgeving en één sandbox-omgeving, is hetzelfde aantal licenties zonder extra kosten beschikbaar voor de infrastructuur voor financiën en bedrijfsactiviteiten.
- **Extra sandbox-licenties**: als u extra sandbox-licenties hebt aangeschaft voor de zelfstandig Human Resources-toepassing, is hetzelfde aantal sandbox-licenties zonder extra kosten beschikbaar voor een sandbox-omgeving (standaardacceptatietest) in de infrastructuur voor financiën en bedrijfsactiviteiten. 
