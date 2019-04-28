---
title: E-mailsjablonen
description: Dit onderwerp bevat informatie over de e-mailsjablonen die u kunt maken en gebruiken in Microsoft Dynamics 365 for Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: b88ba4386dbf3513d75990acca1c07fa6f0dc9b0
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "857055"
---
# <a name="email-templates"></a>E-mailsjablonen
[!include[banner](../includes/banner.md)]

Met behulp van de e-mailsjabloonbibliotheek kunnen beheerders een uniform thema en merkherkenning maken voor alle e-mails die worden verzonden via Microsoft Dynamics 365 for Talent: Attract. Beheerders kunnen ook een verzameling e-mailinhoudssjablonen samenstellen die andere gebruikers kunnen gebruiken. Het aanstellend team kan deze sjablonen gebruiken in hun werkstroom om e-mails efficiënter te verzenden. Sommige e-mailberichten in Attract zijn geconfigureerd om automatisch te worden verzonden en de beheerder kan de e-mailsjabloonbibliotheek gebruiken om de inhoud van die e-mails aan te passen.

> [!NOTE]
> Als u e-mailsjablonen wilt gebruiken, moet uw organisatie beschikken over Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="global-template-configurations"></a>Globale sjabloonconfiguraties

Als de beheerder consistente merkherkenning voor alle e-mailcommunicatie wil, moet deze eerst de globale kop- en voetteksten voor alle e-mailsjablonen instellen. In het beheercentrum, op het tabblad **Instellingen e-mailsjabloon** in de sectie **Koptekst** kan de beheerder een afbeelding uploaden om te gebruiken als de koptekst of banner voor alle e-mailberichten. De afbeelding kan een bedrijfslogo, een briefhoofd of een andere representatieve afbeelding zijn. Het wordt aangeraden de breedte tussen 25 en 800 pixels te maken en de hoogte tussen 25 en 150 pixels, omdat deze dimensies optimaal zijn voor de meeste e-clients, zoals Microsoft Outlook. De afbeelding moet een JPEG-, JPG-, PNG- of SVG-bestand zijn en de bestandsgrootte moet kleiner dan 1 megabyte (MB) zijn. Nadat een afbeelding is geüpload, wordt een voorbeeld van de koptekst gegenereerd en weergegeven. Als de koptekstafbeelding moet worden verwijderd of vervangen, kan de beheerder de optie **Verwijderen** boven het voorbeeld gebruiken.

In de sectie **Voettekst** kan de beheerder koppelingen verschaffen naar het privacybeleid van het bedrijf voor communicatie, en naar de voorwaarden. Deze koppelingen worden opgenomen in een voettekst die automatisch wordt gegenereerd. Een voorbeeld van deze voettekst wordt vervolgens weergegeven.

Zorg ervoor dat u uw wijzigingen opslaat voordat u het beheercentrum sluit.

> [!NOTE] 
> De koptekst en voettekst zijn algemene instellingen voor alle e-mailberichten. Daarom worden deze weergegeven in alle e-mails die worden verzonden via Attract. Als de instellingen niet zijn geconfigureerd, worden de koptekst en voettekst weggelaten uit alle e-mailberichten.

## <a name="email-template-library"></a>E-mailsjabloonbibliotheek 

Nadat de algemene sjabloonconfiguraties zijn ingesteld, kan de beheerder beginnen sjablonen te maken en samen te stellen voor alle e-mailberichten die worden verzonden vanuit Attract. De e-mailsjabloonbibliotheek is alleen beschikbaar voor beheerders. Als u de bibliotheek wilt openen, klikt u op het hoofdnavigatiemenu en selecteert u het tabblad **E-mailsjablonen**. De bibliotheek wordt gecategoriseerd door de verschillende activiteiten in Attract waarvoor e-mailberichten moeten worden verzonden, zoals planning, beoordeling en het maken van functies. De beheerder kan een categorie selecteren om alle e-mailtypen weer te geven die gekoppeld zijn aan de activiteit. Selecteer bijvoorbeeld **Planning** om de verschillende typen e-mail weer te geven die worden verzonden tijdens het planningsproces en alle sjablonen die beschikbaar zijn voor elke soort e-mail. Elke subsectie in een categorie vertegenwoordigt een soort e-mail.

Sommige typen e-mail kunnen meer dan één ontvanger hebben. Bijvoorbeeld in de categorie **Planning** worden de e-mails die worden verzonden wanneer het overzicht van de sollicitatiegesprekplanning nodig is, zowel aan kandidaten als interviewers verzonden. Elke sectie heeft twee hoofdkolommen: **Sjabloontitel** en **Ontvanger**. Elke rij in een sectie vertegenwoordigt een enkele sjabloon voor een soort e-mail. In eerste instantie verschijnt een vergrendelingssymbool in de rij voor elke sjabloon. Dit symbool geeft aan dat de sjabloon de standaardsjabloon is die wordt geleverd met Attract en dat deze niet kan worden verwijderd. Voor elke sjabloon kan de beheerder de ellipsisknop (**...**) gebruiken om de sjabloon te dupliceren, in te stellen als standaardsjabloon of te verwijderen. Als een sjabloon is ingesteld als een standaardsjabloon kunnen een van twee problemen optreden. Het gedrag wordt aangegeven door de badge of badges die worden weergegeven in de rij voor de sjabloon:

- **Standaard**: deze badge geeft aan dat de sjabloon de standaardsjabloon is voor e-mail die wordt verzonden en dat er informatie in wordt ingevoerd als een gebruiker e-mail verzendt van dat specifieke type.
- **Standaard** + **Automatisch verzonden**: deze combinatie van badges geeft aan dat de sjabloon de actieve sjabloon voor door het systeem gegenereerde e-mail is die automatisch wordt verzonden.

Als u een sjabloon wilt bewerken, selecteert u de rij en brengt u wijzigingen aan in de sjabloon.

> [!NOTE]
> Elke geadresseerde van een bepaald type e-mail heeft een standaardsjabloon. Alle standaard-Attract-sjablonen worden ingesteld als standaardsjablonen totdat de beheerder een nieuwe sjabloon voor een bepaald type e-mail maakt en instelt als de standaardsjabloon.

## <a name="create-a-template"></a>Een sjabloon maken

Als u een sjabloon wilt maken, selecteert u in de rechterbovenhoek van de e-mailsjabloonbibliotheek **+ Nieuwe sjabloon**. Selecteer het type e-mailadres waarvoor u de sjabloon maakt, selecteer de ontvanger, het proces en de gebeurtenis waarvoor de e-mail moet worden verzonden. Selecteer vervolgens **Maken**.

De sjabloon wordt geopend in de bewerkingsweergave en u kunt de sjabloon een naam geven. Bijvoorbeeld: als de sjabloon is bedoeld voor kandidaten aan een Amerikaanse universiteit, maar de inhoud in het Frans is geschreven, kunt u **University\_US\_Français** als titel invoeren. De titel, de onderwerpregel en de inhoud van de hoofdtekst voor een sjabloon kunnen talen naast Engels ondersteunen.

Het veld **Naar** voor een sjabloon kan niet worden bewerkt, omdat u de ontvanger al hebt geselecteerd toen u de sjabloon maakte.

U kunt persoonlijkheden zoals **Werver** of **Aanstellend manager** toevoegen aan de regel Cc (carbon copy). Wanneer de e-mail wordt verzonden, worden deze rollen automatisch vervangen door de desbetreffende gebruikers op basis van de context van de functie.

De onderwerpregel en hoofdtekst ondersteunen tijdelijke aanduidingen. U kunt tijdelijke aanduidingen invoegen door **\#** te typen en vervolgens de desbetreffende tijdelijke aanduiding te selecteren in de automatisch aangevulde vervolgkeuzelijst. De lijst met beschikbare tijdelijke aanduidingen wordt weergegeven aan de rechterkant van de pagina. Wanneer de e-mail wordt verzonden, worden de tijdelijke aanduidingen automatisch vervangen, op basis van de context van de functie en de ontvanger. Een sjabloon voor een e-mail die wordt verzonden naar kandidaten, bevat bijvoorbeeld de tijdelijke aanduiding \#{Naam\_kandidaat}. Wanneer de e-mail wordt verzonden aan een kandidaat die Cameron heet, wordt deze tijdelijke aanduiding vervangen door de naam Cameron.

De hoofdteksteditor is een uitgebreide teksteditor waarmee u tekst een stijl en opmaak kunt geven. U kunt er ook hyperlinks en ankers mee invoegen.

Nadat een sjabloon is gemaakt voor een bepaald type e-mail, selecteert u de ellipsisknop (**...**) in de rij voor de sjabloon en stelt u deze in als de standaardsjabloon.

## <a name="consume-templates"></a>Sjablonen gebruiken

Wanneer het aanstellend team een e-mailbericht verzendt, kan het gebruikmaken van de sjablonen die de beheerder heeft gemaakt. Als er meerdere sjablonen zijn gemaakt voor het e-mailbericht dat een gebruiker verzendt, verschijnt een vervolgkeuzelijst in de werkstroom voor e-samenstelling. De standaardsjabloon wordt automatisch ingevoerd, maar de gebruiker kan een andere sjabloon selecteren.

> [!NOTE] 
> Voor e-mailberichten die automatisch worden verzonden, kunnen meerdere sjablonen worden gemaakt. Slechts één sjabloon kan echter worden ingesteld als de actieve sjabloon. Omdat dit proces wordt geactiveerd door gebeurtenissen, kan alleen de beheerder bepalen welke sjabloon moet worden gebruikt, op basis van de combinatie van badges **Standaard** en **Automatisch verzonden** in de sjabloonbibliotheek.
