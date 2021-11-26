---
title: Overzicht van twee keer wegschrijven
description: Dit onderwerp biedt een overzicht van twee keer wegschrijven wat een near-realtime interactie biedt tussen Customer Engagement- en Finance and Operations-apps.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.custom: intro-internal
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 69abd2b6d4026ef1b5b85d52c561bb060cf82123
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781459"
---
# <a name="dual-write-overview"></a>Overzicht van twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a>Wat is twee keer wegschrijven?

Twee keer wegschrijven is een kant-en-klare infrastructuur die near-realtime interactie biedt tussen Customer Engagement- en Finance and Operations-apps. Wanneer gegevens over klanten, producten, personen en bewerkingen over de grenzen van toepassingen heen stromen, zijn alle afdelingen in een organisatie gemachtigd.

Twee keer wegschrijven biedt nauw gekoppelde, bidirectionele integratie tussen Finance and Operations-apps en Dataverse. Alle gegevenswijzigingen in Finance and Operations-apps leiden tot schrijfbewerkingen naar Dataverse en alle gegevenswijzigingen in Dataverse resulteren in schrijfbewerkingen naar Finance and Operations-apps. Deze geautomatiseerde gegevensstroom biedt een geïntegreerde gebruikerservaring over de apps heen.

![Gegevensrelatie tussen apps.](media/dual-write-overview.jpg)

Twee keer wegschrijven heeft twee aspecten: een *infrastructuuraspect* en een *toepassingsaspect*.

### <a name="infrastructure"></a>Infrastructuur

De infrastructuur voor twee keer wegschrijven is uitbreidbaar en betrouwbaar en bevat de volgende hoofdfuncties:

+ Synchrone en bidirectionele gegevensstroom tussen toepassingen
+ Synchronisatie, samen met de modi voor afspelen, onderbreken en inhalen, om het systeem te ondersteunen tijdens online en offline/asynchrone modi.
+ Mogelijkheid om initiële gegevens tussen de toepassingen te synchroniseren
+ Gecombineerde weergave van activiteiten- en foutlogbestanden voor gegevensbeheerders
+ Mogelijkheid om aangepaste waarschuwingen en drempels te configureren en om zich te abonneren op meldingen
+ Intuïtieve gebruikersinterface (UI) voor filtering en transformaties
+ Mogelijkheid om afhankelijkheden en relaties tussen tabellen in te stellen en weer te geven
+ Uitbreidbaarheid voor zowel standaard als aangepaste tabellen en kaarten
+ Betrouwbaar levenscyclusbeheer voor toepassingen
+ Kant-en-klare instelling voor nieuwe klanten

### <a name="application"></a>Aanvraag

Met twee keer wegschrijven worden concepten in Finance and Operations-apps gekoppeld aan concepten in Customer Engagement-apps. Deze integratie ondersteunt de volgende scenario's:

+ Model voor geïntegreerde klanten
+ Toegang tot loyaliteitskaarten en beloningspunten van klanten
+ Uniform gebruik van productmodellen
+ Kennis van organisatiehiërarchie
+ Model voor geïntegreerde leveranciers
+ Toegang tot referentiegegevens voor financiën en belastingen
+ Beschikbaarheid van prijsengine op aanvraag
+ Geïntegreerde ervaring van prospect naar contant geld
+ Mogelijkheid om zowel interne activa als klantactiva te bedienen via veldmedewerkers
+ Geïntegreerd proces van inkopen tot betalen
+ Geïntegreerde activiteiten en notities voor klantgegevens en -documenten
+ Mogelijkheid om de beschikbaarheid van voorhanden voorraad en details op te zoeken
+ Ervaring van project naar contant geld
+ Mogelijkheid om meerdere adressen en rollen te verwerken via het partijconcept
+ Een enkel bronbeheer voor gebruikers
+ Geïntegreerde kanalen voor detailhandel en marketing
+ Zicht op acties en kortingen
+ Functies voor aanvragen van service
+ Gestroomlijnde servicebewerkingen

## <a name="top-reasons-to-use-dual-write"></a>Belangrijkste redenen voor het gebruik van twee keer wegschrijven

Twee keer wegschrijven biedt gegevensintegratie tussen Microsoft Dynamics 365-toepassingen. Dit robuuste raamwerk koppelt omgevingen en zorgen ervoor dat verschillende bedrijfstoepassingen samenwerken. Dit zijn de belangrijkste redenen voor het gebruik van twee keer wegschrijven:

+ Met twee keer wegschrijven beschikt u over een strak gekoppelde, bijna realtime en bidirectionele integratie tussen Finance and Operations-apps en apps voor klantbetrokkenheid. Door deze integratie is Microsoft Dynamics 365 de plek voor al uw zakelijke oplossingen. Klanten die gebruikmaken van Dynamics 365 Finance en Dynamics 365 Supply Chain Management, maar die niet-Microsoft-oplossingen voor Customer Relationship Management (CRM) gebruiken, stappen over op Dynamics 365 vanwege de ondersteuning voor twee keer wegschrijven.
+ Gegevens van klanten, producten, transacties, projecten en het Internet of Things (IoT) stromen automatisch naar Dataverse via twee keer wegschrijven. Deze verbinding is nuttig voor bedrijven die geïnteresseerd zijn in Power Platform-uitbreidingen.
+ De infrastructuur voor twee keer wegschrijven volgt het principe van geen code/weinig code. Er is minimale technische inspanning vereist om de standaardtoewijzingen van tabel naar tabel uit te breiden en aangepaste toewijzingen op te nemen.
+ Twee keer wegschrijven ondersteunt zowel de online modus als de offline modus. Microsoft is het enige bedrijf dat ondersteuning biedt voor online en offline modi.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Wat houdt Twee keer wegschrijven in voor ontwikkelaars en architecten van Customer Engagement-apps?

Met Twee keer wegschrijven wordt de gegevensstroom tussen Finance and Operations-apps en Customer Engagement-apps geautomatiseerd. Twee keer wegschrijven bestaat uit twee AppSource-oplossingen die in Dataverse worden geïnstalleerd. De oplossingen vergroten het tabelschema, invoegtoepassingen en workflows in Dataverse, zodat deze kunnen worden aangepast aan de ERP-grootte. Voor een succesvolle implementatie moeten ontwikkelaars en architecten van Customer Engagement-apps deze wijzigingen begrijpen en samenwerken met hun tegenhangers in Finance and Operations-apps.

Om pariteit met Finance and Operations-toepassingen tot stand te brengen, brengt Twee keer wegschrijven een aantal belangrijke wijzigingen in het Dataverse-schema aan. Als u het plan begrijpt, kunt u voorkomen dat u ontwerp- en ontwikkelingsproblemen in de toekomst voorkomen.

+ Wanneer het AppSource-pakket voor Twee keer wegschrijven is geïnstalleerd, bevat Dataverse nieuwe concepten, zoals een bedrijf en partij. Met deze concepten kunnen toepassingen gebouwd op Dataverse, zoals Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service en Dynamics 365 Field Service, naadloos met Finance and Operations-apps communiceren.

+ Activiteiten en notities worden gecombineerd en uitgebreid om zowel C1's (gebruikers van het systeem) als C2's (klanten van het systeem) te ondersteunen.

+ Als u gegevensverlies tijdens de valutaoverdracht tussen Finance and Operations-apps en Dataverse wilt voorkomen, kunt u het aantal decimalen in het valutagegevenstype van Customer Engagement-apps uitbreiden. Met deze functie worden bestaande rijen automatisch omgezet in de nieuwe uitgebreide status in de metagegevenslaag. Tijdens deze procedure wordt de valutawaarde omgezet in decimale gegevens in plaats van geldgegevens en de valutawaarde ondersteunt 10 decimalen. Deze functie is optioneel en organisaties die niet meer dan vier decimalen nodig hebben, hoeven zich niet aan te melden. Zie [Migratie van valutagegevenstype voor twee keer wegschrijven](currrency-decimal-places.md) voormeer informatie.

+ [Ingangsdatum](../../dev-tools/date-effectivity.md) wordt toegevoegd aan Dataverse. Hiermee wordt ondersteuning geboden voor vroegere, huidige en toekomstige gegevens in dezelfde tabel.

+ [Omrekeningen van producteenheden](../../../../supply-chain/pim/tasks/manage-unit-measure.md) worden ondersteund voor producten, offertes, orders en facturen.

Zie [Nieuwe of gewijzigde functies in twee keer wegschrijven](whats-new-dual-write.md) voor meer informatie over aanstaande wijzigingen.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]