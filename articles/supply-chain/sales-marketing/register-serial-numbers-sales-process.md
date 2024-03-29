---
title: Werken met artikelen met serienummers
description: In dit artikel wordt uitgelegd hoe u serienummers op pakbonnen of facturen kunt registreren tijdens het verkoopproces. Deze functionaliteit is nuttig als een bedrijf serienummers wil vastleggen voor service- en garantiedoeleinden, maar geen serienummers in voorraad hoeft bij te houden van ontvangst tot uitgifte.
author: Henrikan
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable, InventSerial
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b89e9ab547d13e68ead88d76f9922d14fde4beb3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901845"
---
# <a name="working-with-serialized-items"></a>Werken met artikelen met serienummers

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u serienummers op pakbonnen of facturen kunt registreren tijdens het verkoopproces. Deze functionaliteit is nuttig als een bedrijf serienummers wil vastleggen voor service- en garantiedoeleinden, maar geen serienummers in voorraad hoeft bij te houden van ontvangst tot uitgifte.

Veel bedrijven wilt alleen serienummers vastleggen voor service en garantiedoeleinden en niet serienummers in voorraad te hoeven bijhouden van ontvangst tot uitgifte. In deze gevallen kunt u met de serienummers op de pakbonnen of de facturen registreren wanneer producten worden verkocht. Als producten later worden geretourneerd, kunt u elk product op een factuur traceren om te bepalen of u het product verkocht hebt en of de service- of garantieverplichtingen geldig zijn.

U moet serienummers inschakelen voor het verkoopproces door de optie **Actief in verkoopproces** te selecteren op de pagina **Traceringsdimensiegroepen**. De volgende gebeurtenissen treden vervolgens op in Supply Chain Management:
-   Op het sneltabblad **Serienummers** wordt de optie **Serienummercontrole** geselecteerd. Als deze optie is geselecteerd, moet u één serienummer registreren voor elk artikel op de pakbon of factuur.
-   Alle selecties op traceringsdimensiegroep voor serienummers worden gewist, behalve de optie **Lege uitgifte is toegestaan**. U kunt de optie **Lege uitgifte is toegestaan** selecteren om serienummerbeheer te negeren en toe te staan dat producten worden verpakt of gefactureerd zonder serienummers te registreren.

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a>Wanneer registreer ik serienummers tijdens het verkoopproces?
U kunt serienummers registreren op de pakbon of factuur voor een verkooporder of op de factuur. Wanneer u een factuur voorbereidt voor een artikel met serienummer dat samen met een pakbon is verzonden, kunt u selecteren welke serienummers op de pakbon u wilt factureren. De hoeveelheid geregistreerde serienummers mag niet groter zijn dan de hoeveelheid verzonden artikelen. Als u een gedeeltelijke factuur maakt, kunt u minder artikelen met serienummer selecteren dan het aantal dat op de pakbon is geregistreerd. Wanneer u een pakbon of factuur afdrukt, worden de geregistreerde serienummers opgenomen.

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a>Kan ik serienummers toevoegen door deze te scannen, of moet ik deze typen?
U kunt serienummers scannen of typen. Als u een scanner gebruikt, bepaalt de scanmodus of de serienummers worden toegevoegd aan of verwijderd uit de lijst met serienummers op de factuur of de pakbon. Als u serienummers wilt scannen, bijvoorbeeld door een draagbare streepjescodescanner te gebruiken, moet u de scanner configureren om een Enter- of TAB-opdracht te verzenden na het serienummer. Deze opdracht geeft het einde van de gegevensstroom aan. Anders moet u op Enter of op de tabtoets op het toetsenbord drukken nadat u elk serienummer hebt gescand.

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a>Als ik serienummers inschakel voor het verkoopproces, moet ik dan alle serienummers voor alle artikelen registreren?
De instelling van de traceringsdimensiegroep die is toegewezen aan het product bepaalt of serienummers moeten worden geregistreerd voor alle artikelen op een pakbon of factuur. Wanneer u serienummers voor het verkoopproces inschakelt, wordt de optie **Serienummercontrole** automatisch geselecteerd. U moet dan één serienummer registreren, of een lege registratie voor een onleesbaar nummer maken, voor elk artikel op de pakbon of factuur. Als u geen serienummer voor elk artikel verplicht wilt stellen, selecteert u de optie **Lege uitgifte is toegestaan** voor de traceringsdimensiegroep die aan het artikel is toegewezen. U kunt vervolgens minder serienummers registreren dan de hoeveelheid artikelen die wordt verzonden. Als u meer serienummers registreert dan de hoeveelheid artikelen die worden verzonden, kunt u de pakbon of de factuur niet boeken.

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a>Mag ik serienummers registreren voor gedeeltelijke facturen en gedeeltelijke zendingen?
U kunt gedeeltelijk facturen en pakbonnen maken voor verkooporders, en alleen de serienummers registreren voor de artikelen die deze facturen en pakbonnen bevatten. Als u een gedeeltelijke factuur wilt maken en u meerdere pakbonnen voor de verkooporder hebt, kunt u serienummers van meer dan één pakbon opnemen. Er kan echter maar één pakbon zijn die niet alle serienummers bevat. Stel, u hebt drie pakbonnen en elke omvat twee artikelen met serienummers. U kunt dan geen gedeeltelijke factuur maken voor een artikel van elke pakbon.

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a>Wat doe ik wanneer een serienummer niet leesbaar is?
Als een serienummer niet kan worden gelezen of worden gescand, kunt u een lege regel voor het artikel maken door op **Niet leesbaar** op de pagina **Serienummers** te klikken. Als het serienummer later beschikbaar wordt, kunt u de factuur of de pakbon bijwerken. Zie voor meer informatie de volgende sectie "Kan ik de serienummers die ik heb geregistreerd voor een verkooporder corrigeren of wijzigen?"

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a>Kan ik de serienummers die ik heb geregistreerd voor een verkooporder corrigeren of wijzigen?
Ja, u kunt serienummers corrigeren als aan de volgende voorwaarden wordt voldaan:
-   **Facturen**: u kunt de serienummers wijzigen voor artikelen die u nog niet hebt gefactureerd. De pakbon wordt dan eveneens bijgewerkt. Echter, als een verkooporderregel is gecorrigeerd door een negatieve hoeveelheid te registreren, kunt u geen serienummers wijzigen voor de verkooporderregel.
-   **Pakbonnen**: u kunt geen pakbonregel gedeeltelijk corrigeren die artikelen met serienummers bevat. U moet de volledige hoeveelheid voor de regel omkeren. Als een pakbon is geannuleerd of gecorrigeerd, moet u de teruggeboekte serienummers niet opnieuw registreren wanneer u een nieuwe pakbon voor dezelfde artikelen met serienummer maakt. De nummers die zijn geregistreerd, worden gebruikt.

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a>Kan ik de serienummers bekijken die samen met een specifieke pakbon zijn verzonden of die in een factuur zijn opgenomen?
Ja, u kunt een zoekopdracht uitvoeren op de pakbonjournaalregel of de factuurjournaalregel om een lijst van alle serienummers te bekijken die in het document zijn opgenomen.

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a>Kan ik de artikelen met serienummer zien die ik beschikbaar heb?
Nee, u kunt de artikelen met serienummer die u in voorraad hebt niet bekijken omdat de serienummers niet worden geregistreerd voor artikelen tot de artikelen worden verkocht.

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a>Ik kan serienummers voor artikelen met variabel gewicht registreren?
Nee, u kunt geen serienummers voor catch weight-artikelen registreren in het verkoopproces. Bovendien geldt dat als een product is ingesteld als een catch weight-artikel, u het product niet kunt toewijzen aan een traceringsdimensiegroep die is ingesteld om serienummers alleen tijdens het verkoopproces te gebruiken.

## <a name="can-i-register-serial-numbers-at-the-retail-pos"></a>Kan ik serienummers registreren op het detailhandel-POS?

Ja, het verkooppunt voor detailhandel (POS) vraagt de gebruiker om een serienummer in te voeren wanneer de gebruiker een artikel verkoopt waaraan een traceringsdimensiegroep is toegewezen die is ingesteld om alleen serienummers te gebruiken tijdens het verkoopproces.

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a>Welke beveiligingsrollen zijn vereist voor het registreren van serienummers tijdens het verkoopproces?
Deze functionaliteit is beschikbaar voor alle rollen die verkooppakbonnen en verkoopfacturen kunnen beheren. Met de volgende taken kunnen werknemers serienummers corrigeren en lege invoeren registreren voor serienummers die niet kunnen worden gelezen of worden gescand:
-   Correcties van serienummers beheren
-   Registraties van onleesbare serienummers onderhouden







[!INCLUDE[footer-include](../../includes/footer-banner.md)]