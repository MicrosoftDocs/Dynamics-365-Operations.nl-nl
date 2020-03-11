---
title: Overzicht van twee keer wegschrijven
description: Dit onderwerp biedt een overzicht van twee keer wegschrijven. Twee keer wegschrijven is een infrastructuur die vrijwel-realtime interactie biedt tussen modelgestuurde Microsoft Dynamics 365-apps en Finance and Operations-apps.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075978"
---
# <a name="dual-write-overview"></a>Overzicht van twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Wat is twee keer wegschrijven?

Twee keer wegschrijven is een kant-en-klare infrastructuur die vrijwel-realtime interactie biedt tussen modelgestuurde apps in Microsoft Dynamics 365 en Finance and Operations-apps. Wanneer gegevens over klanten, producten, personen en bewerkingen over de grenzen van toepassingen heen stromen, zijn alle afdelingen in een organisatie gemachtigd.

Twee keer wegschrijven biedt nauw gekoppelde, bidirectionele integratie tussen Finance and Operations-apps en Common Data Service. Alle gegevenswijzigingen in Finance and Operations-apps leiden tot schrijfbewerkingen naar Common Data Service en alle gegevenswijzigingen in Common Data Service resulteren in schrijfbewerkingen naar Finance and Operations-apps. Deze geautomatiseerde gegevensstroom biedt een geïntegreerde gebruikerservaring over de apps heen.

![Gegevensrelatie tussen apps](media/dual-write-overview.jpg)

Twee keer wegschrijven heeft twee aspecten: een *infrastructuuraspect* en een *toepassingsaspect*.

### <a name="infrastructure"></a>Infrastructuur

De infrastructuur voor twee keer wegschrijven is uitbreidbaar en betrouwbaar en bevat de volgende hoofdfuncties:

+ Synchrone en bidirectionele gegevensstroom tussen toepassingen
+ Synchronisatie, samen met de modi voor afspelen, onderbreken en inhalen, om het systeem te ondersteunen tijdens online en offline/asynchrone modi.
+ Mogelijkheid om initiële gegevens tussen de toepassingen te synchroniseren
+ Geconsolideerde weergave van activiteiten- en foutlogbestanden voor gegevensbeheerders
+ Mogelijkheid om aangepaste waarschuwingen en drempels te configureren en om zich te abonneren op meldingen
+ Intuïtieve gebruikersinterface (UI) voor filtering en transformaties
+ Mogelijkheid om afhankelijkheden en relaties tussen entiteiten in te stellen en weer te geven
+ Uitbreidbaarheid voor zowel standaard als aangepaste entiteiten en kaarten
+ Betrouwbaar levenscyclusbeheer voor toepassingen
+ Kant-en-klare instelling voor nieuwe klanten

### <a name="application"></a>Aanvraag

Met twee keer wegschrijven worden concepten in Finance and Operations-apps gekoppeld aan concepten in modelgestuurde apps in Dynamics 365. Deze integratie ondersteunt de volgende scenario's:

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

+ Met twee keer wegschrijven beschikt u over een strak gekoppelde, bijna realtime en bidirectionele integratie tussen Finance and Operations-apps en modelgestuurde apps in Dynamics 365. Door deze integratie is Microsoft Dynamics 365 de plek voor al uw zakelijke oplossingen. Klanten die gebruikmaken van Dynamics 365 Finance en Dynamics 365 Supply Chain Management, maar die niet-Microsoft-oplossingen voor Customer Relationship Management (CRM) gebruiken, stappen over op Dynamics 365 vanwege de ondersteuning voor twee keer wegschrijven.
+ Gegevens van klanten, producten, transacties, projecten en het Internet of Things (IoT) stromen automatisch naar Common Data Service via twee keer wegschrijven. Deze verbinding is heel nuttig voor bedrijven die geïnteresseerd zijn in Microsoft Power Platform-uitbreidingen.
+ De infrastructuur voor twee keer wegschrijven volgt het principe van geen code/weinig code. Er is minimale technische inspanning vereist om de standaardtoewijzingen van tabel naar tabel uit te breiden en aangepaste toewijzingen op te nemen.
+ Twee keer wegschrijven ondersteunt zowel de online modus als de offline modus. Microsoft is het enige bedrijf dat ondersteuning biedt voor online en offline modi.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Wat betekent twee keer wegschrijven voor gebruikers en architecten van CRM-producten?

Met twee keer wegschrijven wordt de gegevensstroom tussen Finance and Operations-apps en Common Data Service geautomatiseerd. In toekomstige releases worden concepten in modelgestuurde apps in Dynamics 365 (zoals klant, contactpersoon, prijsopgave en order) geschaald naar klanten in de middenmarkt en hogere middenmarkt.

In de eerste release wordt de meeste automatisering verzorgd door oplossingen voor twee keer wegschrijven. In toekomstige releases worden deze oplossingen onderdeel van Common Data Service. Door de aanstaande wijzigingen in Common Data Service te begrijpen, kunt u uw inspanningen op lange termijn beperken. Hier volgen enkele van de belangrijke wijzigingen:

+ Common Data Service krijgt nieuwe concepten, zoals bedrijf en partij. Deze concepten zijn van invloed op alle apps die op Common Data Service zijn gebouwd, zoals Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service en Dynamics 365 Field Service.
+ Activiteiten en notities worden gecombineerd en uitgebreid om zowel C1's (gebruikers van het systeem) als C2's (klanten van het systeem) te ondersteunen.
+ Hier volgen enkele van de komende wijzigingen in Common Data Service:

    - Het gegevenstype decimaal vervangt het gegevenstype geld.
    - Datumeffectiviteit biedt ondersteuning voor vroegere, huidige en toekomstige datums op dezelfde locatie.
    - Er wordt meer ondersteuning geboden voor valuta en wisselkoersen en API (Application Programming Interface) voor **Wisselkoers** wordt herzien.
    - Eenheidsomrekeningen worden ondersteund.

Zie [Gegevens in Common Data Service – fase 1 en 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap) voor meer informatie over aanstaande wijzigingen.
