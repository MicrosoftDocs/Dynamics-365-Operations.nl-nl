---
title: Een transactie uitstellen en hervatten in het verkooppunt (POS)
description: In dit onderwerp wordt beschreven hoe gebruikers transacties in uitvoering kunnen uitstellen en later of op een andere kassa kunnen hervatten met Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022182"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Een transactie uitstellen en hervatten in het verkooppunt (POS)

[!include [banner](includes/banner.md)]


POS-gebruikers kunnen transacties in uitvoering uitstellen en deze later of op een andere kassa hervatten. Transacties worden vaak uitgesteld om snel een kassa vrij te maken voor een andere taak zonder de voortgang van de huidige transactie te verliezen. Stel, een winkelmedewerker begint de transactie van een klant te verwerken op een mobiel apparaat, maar moet de transactie voltooien op een kassa met een kassalade. In dat geval kan de winkelmedewerker de transactie uitstellen op het mobiele apparaat en vervolgens ophalen en hervatten op een kassa.

## <a name="configure-suspend-and-resume-functionality"></a>Functie voor onderbreken en hervatten configureren

### <a name="pos-operations"></a>POS-bewerkingen

Met twee [POS-bewerkingen](pos-operations.md) kan het POS ondersteuning bieden voor uitstel- en hervatscenario's. U kunt deze bewerkingen toewijzen aan [knoppenrasters](pos-screen-layouts.md) op de transactie- of welkomstpagina.

- 503: Transactie uitstellen
- 504: Transactie intrekken (ophalen)

### <a name="receipt-template"></a>Ontvangstsjabloon

Het POS kan zo worden geconfigureerd dat er een afgedrukte pakbon wordt gegenereerd wanneer een transactie wordt uitgesteld. Die pakbon kan vervolgens worden gebruikt om de transactie later snel te identificeren en op te halen.

Als u het POS in staat wilt stellen een pakbon af te drukken, moet u de ontvangstbewijsindeling **Uitgestelde transactie** toevoegen aan het ontvangstbewijsprofiel van de de winkel. U kunt de ontvangstbewijsindeling zo ontwerpen dat deze specifieke details over de transactie bevat of uitsluit. De indeling kan bijvoorbeeld een streepjescode omvatten om scannen te ondersteunen.

### <a name="receipt-numbering"></a>Ontvangstbewijsnummering

Zoals voor andere POS-transactietypen die een afgedrukt ontvangstbewijs genereren, kunt u een nummerreeks voor uitgestelde transacties opgeven in de sectie **Ontvangstbewijsnummering** van het functionaliteitsprofiel van de winkel.

### <a name="void-when-closing-shift"></a>Ongeldig maken bij sluiten van dienst

U kunt de optie **Ongeldig maken bij sluiten van dienst** gebruiken om te vereisen dat gebruikers uitgestelde transacties voltooien of ongeldig maken voordat ze hun dienst sluiten. Tijdens de bewerking **Ploeg sluiten** moeten gebruikers aangeven of ze eventueel openstaande uitgestelde transacties willen annuleren of weergeven.

## <a name="suspend-and-resume-a-transaction"></a>Een transacties uitstellen en hervatten

### <a name="suspend-a-transaction"></a>Een transactie uitstellen

Gebruikers die over voldoende bevoegdheden beschikken en een schermindeling met de bewerking **Transactie uitstellen** gebruiken, kunnen een transactie uitstellen zodat deze later of op een andere kassa kan worden opgehaald.

Transacties kunnen alleen worden uitgesteld als deze **niet** de volgende soorten regels bevatten:

- Actieve betalingsregels
- Geschenkbonregels (om een geschenkbon uit te geven of toe te voegen aan het geschenkbonsaldo)

Een uitgestelde transactie heeft geen invloed op verkoopgegevens of voorraadbeschikbaarheidsgegevens voor de winkel.

### <a name="resume-a-suspended-transaction"></a>Een uitgestelde transactie hervatten

Uitgestelde transacties kunnen worden opgehaald en hervat op dezelfde locatie door elke gebruiker die over voldoende bevoegdheden beschikt en een indeling met de bewerking **Transactie intrekken** gebruikt.

Scan de streepjescode op de afgedrukte pakbon terwijl u de lijst met transacties vanuit de bewerking **Transactie intrekken** bekijkt om snel en eenvoudig een uitgestelde transactie op te halen.

### <a name="considerations-for-offline-mode"></a>Overwegingen voor offlinemodus

- Een transactie die wordt uitgesteld terwijl het POS online is, kan niet worden hervat in de offlinemodus omdat de gegevens niet zijn gesynchroniseerd met de offlinedatabase.
- Als u een transactie uitstelt terwijl het POS offline is, kunt u deze ophalen in de offlinemodus, mits het POS niet online is gezet sinds u de transactie hebt uitgesteld. Zodra het POS weer online is, worden gegevens over uitgestelde transacties verplaatst naar de onlinedatabase en uit de offlinedatabase verwijderd. De transacties kunnen daarom alleen in de onlinemodus worden hervat. Als u de offlinemodus weer inschakelt voor het POS, kunt u deze uitgestelde transactie niet hervatten omdat ze al zijn verwijderd uit de offlinedatabase.

### <a name="void-a-suspended-transaction"></a>Een uitgestelde transactie ongeldig maken

U kunt een uitgestelde transactie ongeldig maken door de transactie op te halen en vervolgens de bewerking **Ongeldig gemaakte transactie** uit te voeren of door de transactie te selecteren in de lijst **Transactie intrekken** en **Annuleren** te selecteren op de appbalk. De winkel kan ook zo worden geconfigureerd dat gebruikers wordt gevraagd om uitgestelde transacties ongeldig te maken wanneer ze hun dienst sluiten.
