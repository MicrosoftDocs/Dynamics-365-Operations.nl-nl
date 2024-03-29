---
title: Locaties in een WMS-magazijn configureren
description: Deze guide toont hoe u de locatie-instelling configureert voor een nieuw WMS-magazijn (een magazijn dat magazijnbeheerprocessen (WMS) gebruikt).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cce7ea0c06938d2ce038853a262f843ec76fe4c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219653"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Locaties in een WMS-magazijn configureren

[!include [banner](../../includes/banner.md)]

Deze guide toont hoe u de locatie-instelling configureert voor een nieuw WMS-magazijn (een magazijn dat magazijnbeheerprocessen (WMS) gebruikt). Het proces wordt gewoonlijk uitgevoerd door een magazijnmanager. U kunt deze begeleiding uitvoeren in het demobedrijf USMF of met uw eigen gegevens. Een preconditie is dat u ten minste één geconfigureerde site hebt.


## <a name="create-a-new-warehouse"></a>Een nieuw magazijn maken
1. Ga naar **Navigatievenster > Modules > Voorraadbeheer > Instellen > Opsplitsing van voorraad > Magazijnen**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Magazijn**.
4. Typ een waarde in het veld **Naam**.
5. Selecteer of typ een bestaande locatiewaarde in het veld **Locatie**.
6. Vouw de sectie **Magazijn** uit.
7. Stel de optie **Magazijnbeheerprocessen gebruiken** in op Ja. Met deze instelling kunt u magazijnbeheerprocessen (WMS) uitvoeren met magazijnwerk en mobiele apparaten.
8. Sluit de pagina.

## <a name="define-a-location-format"></a>Een locatie-indeling definiëren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Locatie-indelingen**. Locatie-indelingen zijn een benamingssysteem dat wordt gebruikt om unieke en consistente namen aan te maken voor verschillende locatiebakposities die binnen een magazijn worden gebruikt. Het kan handig zijn om scheidingstekens als onderdeel van de locatie-indeling te gebruiken om het gemakkelijker te maken onderdelen van de locatie zoals het gangnummer te identificeren. In dit voorbeeld wordt er een naam met vier onderdelen gemaakt. Dit kunnen bijvoorbeeld gang, rek, plank en bak zijn.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Locatie-indeling**.
4. Typ een waarde in het veld **Naam**.
5. Typ een waarde in het veld **Segmentomschrijving**. Dit onderdeel beschrijft wat het eerste onderdeel van de locatienaam betekent. Dat kan bijvoorbeeld 'Gang' zijn.
6. Typ een getal in het veld **Lengte**. Dit bepaalt hoeveel tekens dit gedeelte van de locatienaam moet hebben. Let op dat het totaal van alle onderdelen in de naam, inclusief de scheidingstekens, niet 10 tekens kan overschrijden.    
7. Typ een waarde in het veld **Scheidingsteken**. Dit bepaalt welk teken of symbool tussen het eerste en het tweede onderdeel van de naam wordt gebruikt.  
8. Klik in de sectie **Details** op **Nieuw**.
9. Typ een waarde in het veld **Segmentomschrijving**.
10. Typ een getal in het veld **Lengte**.
11. Typ een waarde in het veld **Scheidingsteken**.
12. Klik in de sectie **Details** op **Nieuw**.
13. Typ een waarde in het veld **Segmentomschrijving**.
14. Typ een getal in het veld **Lengte**.
15. Typ een waarde in het veld **Scheidingsteken**.
16. Klik in de sectie **Details** op **Nieuw**.
17. Typ een waarde in het veld **Segmentomschrijving**.
18. Typ een getal in het veld **Lengte**.
19. Klik op **Opslaan**.
20. Sluit de pagina.

## <a name="define-location-types"></a>Locatietypen definiëren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Locatietypen**. Locatietypen kunnen worden gebruikt als filteropties om de andere magazijnbeheerprocessen te controleren. U moet ten minste faserings- en definitieve verzendlocatietypen maken om het uitgaande magazijnbeheerproces te definiëren. 
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Locatietype**.
4. Typ een waarde in het veld **Beschrijving**.
5. Sluit de pagina.

## <a name="define-location-profile"></a>Locatieprofiel definiëren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Locatieprofielen**. De definitie van locatieprofielen is zeer belangrijk. Gegroepeerde locatiecapaciteit kan hier worden gecontroleerd, evenals het beleid dat bepaalt wat voor voorraad wordt opgeslagen en waar het wordt opgeslagen. Locatieprofielen kunnen worden gebruikt als filteropties om de andere magazijnbeheerprocessen te controleren. U moet minimaal een gebruikerslocatieprofiel maken om WMS in te schakelen.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Locatieprofiel-id**.
4. Typ een waarde in het veld **Naam**.
5. Klik in het veld **Locatie-indeling** op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld **Locatietype** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Schakel het selectievakje **Gemengde voorraadstatussen toestaan** in of uit. Schakel deze optie in als u gemengde voorraadstatuswaarden wilt toestaan op de locaties die zullen worden gegroepeerd door dit locatieprofiel. 
12. Schakel het selectievakje **Regels voor batchdagen overschrijven** in of uit. Schakel deze optie in om de regel te overschrijven voor hoeveel dagen de voorraadbatchvervaldatums kunnen verschillen om mengen toe te staan van voorraadbatches die niet aan deze regel voldoen.  
13. Schakel het selectievakje **Cyclustelling toestaan** in of uit. Schakel deze optie in om cyclustellingsprocessen toe te staan op alle locaties die zullen worden gegroepeerd door dit locatieprofiel. 
14. Vouw de sectie **Dimensies** uit of samen. Met het tabblad Dimensies kunt u parameters en methoden definiëren om exacte berekeningen toe te staan van de belastingscapaciteit binnen alle locaties.  
15. Sluit de pagina.

## <a name="enable-warehouse-management-parameters"></a>Parameters voor magazijnbeheer inschakelen
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Parameters voor magazijnbeheer**. Als u magazijnwerk wilt kunnen verwerken, moet u parameters instellen voor het gebruikerslocatieprofiel, het faseringslocatietype en het definitieve verzendlocatietype. Zodra het uitgaande proces eindigt op het definitieve verzendlocatietype dat u definieert, worden de gerelateerde uitgaande transacties bijgewerkt naar 'Verzameld'.
2. Vouw de sectie **Locatieprofielen** uit of samen.
3. Klik in het veld **Gebruikerslocatie** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Vouw de sectie **Locatietypen** uit of samen.
6. Klik in het veld **Faseringslocatietype** op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld **Uiteindelijk verzendlocatietype** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Sluit de pagina.

## <a name="define-warehouse-zone-groups"></a>Magazijnzonegroepen definiëren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Magazijnzonegroepen**. Magazijnzones kunnen worden gebruikt als filters voor opties om de andere magazijnbeheerprocessen te controleren. U moet een zonegroep maken voordat u een zone kunt definiëren.   
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Zonegroep-id**.
4. Typ een waarde in het veld **Naam zonegroep**.
5. Sluit de pagina.

## <a name="define-warehouse-zones"></a>Magazijnzones definiëren
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Zones**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Zone-id**.
4. Typ een waarde in het veld **Zonenaam**.
5. Klik in het veld **Zonegroep-id** op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Sluit de pagina.

## <a name="create-locations-using-the-location-setup-wizard"></a>Locaties maken met de wizard voor locatie-instelling
1. Ga naar **Navigatievenster > Modules > Magazijnbeheer > Instellingen > Magazijn > Wizard voor locatie-instelling**.
2. Klik in het veld **Magazijn** op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik in het veld **Zone-id** op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld **Locatieprofiel-id** op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer het gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Markeer in de lijst de geselecteerde rij.
12. Voer een getal in het veld **Vanaf nummer** in. De velden Vanaf nummer en Tot nummer definiëren hoeveel locaties worden gemaakt. Stel dat u Van nummer instelt op 1 en Tot nummer op 3 voor alle vier de regels in de locatie-indeling. Er worden dan 81 locaties gemaakt (3x3x3x3).   
13. Voer een getal in het veld **Tot nummer** in.
14. Zoek en selecteer de gewenste record in de lijst.
15. Voer een getal in het veld **Vanaf nummer** in.
16. Voer een getal in het veld **Tot nummer** in.
17. Zoek en selecteer het gewenste record in de lijst.
18. Voer een getal in het veld **Vanaf nummer** in.
19. Voer een getal in het veld **Tot nummer** in.
20. Zoek en selecteer het gewenste record in de lijst.
21. Voer een getal in het veld **Vanaf nummer** in.
22. Voer een getal in het veld **Tot nummer** in.
23. Klik op Maken.

## <a name="create-locations-manually"></a>Locaties handmatig maken
1. Ga naar **Magazijnbeheer > Instellingen > Magazijn > Locaties**. Handmatig locaties binnen een magazijn maken is eenvoudig. De locatienaam en de locatieprofiel-id zijn verplichte waarden. 
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Magazijn**.
4. Typ een waarde in het veld **Locatie**. Merk op dat u hier een nieuwe locatie maakt, dus u moet een nieuwe, unieke naam typen in plaats van een bestaande te selecteren.
5. Typ een waarde in het veld **Locatieprofiel-id**.
6. Sluit de pagina.

## <a name="define-pack-size-categories"></a>Categorieën van verpakkingsgrootte definiëren
1. Ga naar **Magazijnbeheer > Instellen > Magazijn > Categorieën verpakkingsgrootte**. Verpakkingsgroottecategorieën kunnen worden gebruikt om artikelen te groeperen die soortgelijke fysieke verpakkingsgrootten hebben. In dit voorbeeld wordt de verpakkingsgroottecategorie gebruikt om de capaciteit bij de orderverzamellocaties in een bepaalde zone van het magazijn te controleren. De verpakkingsgrootte-id moet worden toegewezen aan de vrijgegeven productentiteit om te kunnen worden gebruikt als onderdeel van de verwerking van opslaglimieten.  
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Verpakkingsgroottecategorie-id**.
4. Typ een waarde in het veld **Naam verpakkingsgroottecategorie**.
5. Sluit de pagina.

## <a name="define-location-stocking-limits"></a>Locatieopslaglimieten instellen
1. Ga naar **Magazijnbeheer > Instellingen > Magazijn > Opslaglimieten van locatie**. Opslaglimieten van locaties helpen te zorgen dat geen werk wordt gemaakt om te verzoeken dat voorraad wordt geplaatst op een locatie die niet de fysieke capaciteit voor die voorraad heeft.  
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Magazijn**.
4. Typ een waarde in het veld **Locatieprofiel-id**.
5. Typ een waarde in het veld **Verpakkingsgroottecategorie-id**.
6. Voer een getal in het veld **Hoeveelheid** in.
7. Klik op **Opslaan**.
8. Sluit de pagina.

## <a name="define-fixed-picking-locations"></a>Vaste orderverzamellocaties definiëren
1. Ga naar **Magazijnbeheer > Instellingen > Magazijn > Vaste locaties**. U kunt de te gebruiken locaties definiëren per product of per productvariant. Het is mogelijk om meerdere vaste locaties voor hetzelfde product binnen hetzelfde magazijn te maken.     
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Artikelnummer**.
4. Typ een waarde in het veld **Magazijn**.
5. Klik in het veld **Locatie** op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
