---
title: Nummerplaat ontvangen via de mobiele app Warehouse Management
description: In dit artikel wordt uitgelegd hoe u de mobiele app Magazijnbeheer kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: fe083f16bd47b3f7bdfd366ae4b0fe4a02f49185
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906995"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>Nummerplaat ontvangen via de mobiele app Warehouse Management

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de mobiele app Magazijnbeheer kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.

Met deze functie kunt u snel de ontvangst van de inkomende voorraad vastleggen die is gerelateerd aan een voorschotbericht (advance shipping notice, ASN). Het systeem maakt automatisch een ASN wanneer magazijnbeheerprocessen worden gebruikt om een overboekingsorder te verzenden. Voor het inkooporderproces kan een ASN handmatig worden vastgelegd of kan deze automatisch worden geïmporteerd met behulp van een inkomend ASN-gegevensentiteitproces.

De ASN-gegevens worden gekoppeld aan ladingen en zendingen via *de verpakkingsstructuren*, waarbij pallets (bovenliggende nummerplaten) dozen kunnen bevatten (geneste nummerplaten).

> [!NOTE]
> Om het aantal voorraadtransacties te verminderen wanneer de verpakkingsstructuren met geneste nummerplaten worden gebruikt, registreert het systeem de fysieke voorhanden voorraad op de bovenliggende nummerplaat. Om de verplaatsing van de fysieke voorhanden voorraad van de bovenliggende nummerplaat naar de geneste nummerplaat te activeren, op basis van de verpakkingsstructuurgegevens, moet het mobiele apparaat een menuopdracht geven die is gebaseerd op het werkaanmaakproces *Verpakken naar geneste nummerplaten*.

## <a name="warehousing-mobile-device-app-processing"></a>Verwerking van app Magazijnbeheer voor mobiele apparaten

Wanneer een werknemer een binnenkomende nummerplaat-id scant, initialiseert het systeem een ontvangstproces voor de nummerplaat. Op basis van deze informatie wordt de inhoud van de nummerplaat (gegevens afkomstig van de ASN) fysiek geregistreerd op de inbound dock-locatie. Welke stromen volgen, is afhankelijk van uw bedrijfsprocesbehoeften.

## <a name="work-policies"></a>Werkbeleidsregels

Net als met (bijvoorbeeld) het proces voor de menuopdracht voor mobiele apparaten *Gereedmelden*, ondersteunt het proces voor nummerplaatontvangst verschillende workflows op basis van de gedefinieerde instellingen.

### <a name="work-policies-with-work-creation"></a>Werkbeleid waarbij werk wordt gemaakt

Wanneer u binnenkomende artikelen registreert via een werkbeleid waarmee werk wordt gemaakt, worden voor elke registratie werkrecords voor wegzetten gegenereerd en opgeslagen. Als u het werkproces *Ontvangen en wegzetten van nummerplaat* gebruikt, worden registratie en wegzetten als één bewerking behandeld met één menuopdracht voor mobiele apparaten. Als u het proces *Ontvangen van nummerplaat* gebruikt, worden de processen voor ontvangen en wegzetten afgehandeld als twee verschillende magazijnbewerkingen, elk met een eigen menuopdracht voor mobiele apparaten.

### <a name="work-policies-without-work-creation"></a>Werkbeleid zonder dat er werk wordt gemaakt

U kunt het proces voor nummerplaatontvangst gebruiken zonder werk te maken. Als u werkbeleid definieert met een werkorder van het type *Ontvangst van overboekingsorder* en/of *Inkooporders* en u het proces *Ontvangen en wegzetten van nummerplaat* gebruikt, wordt met de volgende twee processen van de mobiele app voor Magazijnbeheer geen werk gemaakt. In plaats daarvan registreren ze de inkomende fysieke voorraad op de nummerplaat plaat bij het dock voor binnenkomende ontvangsten.

- *Ontvangen van nummerplaat*
- *Ontvangen en wegzetten van nummerplaat*

> [!NOTE]
> - U moet ten minste één locatie voor een werkbeleid definiëren in de sectie **Voorraadlocaties**. U kunt niet dezelfde locatie opgeven voor meerdere werkbeleidsregels.
> - Met de optie **Etiket afdrukken** voor Magazijnbeheer wordt met menuopties op mobiele apparaten geen nummerplaatlabel afhgedrukt zonder dat er werk wordt gemaakt.

Als u deze functionaliteit op uw systeem beschikbaar wilt maken, moet u de functie *Verbeteringen voor nummerplaat ontvangen* in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Voorraad ontvangen op een locatie die geen nummerplaten bijhoudt

Het is mogelijk om een magazijnlocatie te gebruiken die aan een locatieprofiel is toegewezen, zelfs als **Bijhouden nummerplaat gebruiken** niet is ingeschakeld. U kunt dus bij het ontvangen van voorraad de voorhanden voorraad rechtstreeks registreren op een locatie zonder dat u werk hoeft te maken.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Menuopdrachten voor mobiele apparaten toevoegen voor elke ontvangende locatie in een magazijn

Met de functie *Verbeteringen voor nummerplaat ontvangen* kunt u op elke locatie in een magazijn ontvangen door menu-items voor locatiespecifieke nummerplaatontvangst (en wegzetten) toe te voegen aan de mobiele app voor Magazijnbeheer. Voorheen bood het systeem alleen ondersteuning voor ontvangst op de standaardlocatie die voor elk magazijn is gedefinieerd. Wanneer deze functie echter is ingeschakeld, bieden de menuopdrachten voor mobiele apparaten voor nummerplaatontvangst (en wegzetten) nu de optie **Standaardgegevens gebruiken**. Hiermee kunt u een aangepaste doellocatie selecteren voor elke menuopdracht. (Deze optie was al beschikbaar voor enkele andere typen menuopdrachten.)

Als u deze functionaliteit op uw systeem beschikbaar wilt maken, moet u de functie *Verbeteringen voor nummerplaat ontvangen* in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) inschakelen.

## <a name="show-or-skip-the-receiving-summary-page"></a>De pagina met het ontvangstoverzicht weergeven of overslaan

U kunt de functie *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten* gebruiken om te profiteren van de extra gedetailleerde stroom van de mobiele app Magazijnbeheer als onderdeel van het nummerplaatontvangstproces.

Als deze functie is ingeschakeld, bevatten de menuopdrachten van het mobiele apparaat voor het ontvangen en opslaan van nummerplaten de instelling **Pagina met het ontvangstoverzicht weergeven**. Deze instelling heeft de volgende opties:

- **Een gedetailleerd overzicht weergeven**: tijdens het ontvangen van een nummerplaat krijgen de werknemers een extra pagina te zien waarop de volledige ASN-informatie wordt weergegeven.
- **Het overzicht overslaan**: werknemers kunnen de volledige ASN-informatie niet zien. Magazijnmedewerkers kunnen ook geen beschikkingscode instellen of uitzonderingen toevoegen tijdens het ontvangstproces.

Om deze functionaliteit beschikbaar te maken, moet de functie *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten* zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Bepalen of u een ontvangstoverzichtspagina wilt weergeven op mobiele apparaten* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Verhinderen dat met overboekingsorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn

Een ontvangstproces voor een nummerplaat kan niet worden gebruikt als een ASN een nummerplaat-id bevat die al bestaat en fysieke voorraadgegevens bevat op een magazijnlocatie anders dan de magazijnlocatie waar de nummerplaatregistratie wordt uitgevoerd.

Voor overboekingsorderscenario's waarbij het transitmagazijn geen nummerplaten volgt (en dus ook geen fysieke voorhanden voorraad per nummerplaat bijhoudt), kunt u de functie *Verhinderen dat met overboekingsorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* gebruiken om fysieke voorraadupdates te voorkomen in nummerplaten in transit. Als u deze functionaliteit op uw systeem beschikbaar wilt maken, moet u de functie *Verhinderen dat met overboekingsorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* inschakelen voor uw systeem. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functie in- of uitschakelen door ernaar te zoeken in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Voer de volgende stappen uit om de functionaliteit te beheren wanneer deze functie beschikbaar is.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Algemeen** op het sneltabblad **Nummerplaten** het veld **Beleid voor nummerplaten transitmagazijn** in op een van de volgende waarden:

    - **Hergebruik toestaan van niet-getraceerde nummerplaat**: het systeem werkt op dezelfde manier als wanneer functie de *Verhinderen dat met overboekingsorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* niet beschikbaar is. Deze waarde is de standaardinstelling wanneer u de functie voor het eerst activeert.
    - **Hergebruik verhinderen van niet-getraceerde nummerplaat**: alleen voorhanden updates die zijn gerelateerd aan een geleverde nummerplaat worden toegestaan in het doelmagazijn totdat de overboekingsorder is ontvangen.

## <a name="more-information"></a>Meer informatie

Zie [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md) voor meer informatie over menuopties voor mobiele apparaten.

Zie [Overzicht van Werkbeleid magazijn](warehouse-work-policies.md) voor meer informatie over het productiescenario *Gereedmelden*.

Zie [Magazijnverwerking van inkomende ladingen voor inkooporders](inbound-load-handling.md) voor meer informatie over het beheer van inkomende ladingen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]