---
title: Orderverzamelregels groeperen
description: Dit onderwerp bevat een overzicht van de groepering van orderverzamelregels.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425777"
---
# <a name="pick-line-grouping"></a>Orderverzamelregels groeperen

[!include [banner](../includes/banner.md)]

Bij het groeperen van orderverzamelregels kunnen meerdere werkregels met hetzelfde artikel en dezelfde locatie worden gecombineerd in één orderverzameling die voor de gebruiker wordt weergegeven op een mobiel apparaat. Op deze manier kunnen magazijnmedewerkers de meest efficiënte instructies ontvangen die mogelijk zijn, maar de vereiste scheiding van werkregels in het systeem wordt ook gehandhaafd (bijvoorbeeld voor verschillende containers en orders).

## <a name="set-up-pick-line-grouping"></a>De groepering van orderverzamelregels instellen

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat** en maak een nieuwe menuoptie met de naam **Orderverzameling voor verkoopgroepsregels – Door gebruiker gestuurd**.
2. Stel onder **Menuopties voor mobiel apparaat** de volgende waarden in:

    - Voer in het veld **Naam van menuopdracht** de tekst **Orderverzamelen verkoop - Groepsregel** in.
    - Voer in het veld **Titel** de tekst **Orderverzamelen verkoop - Groepsregel** in.
    - Selecteer **Werk** in het veld **Modus**.
    - Stel de optie **Bestaand werk gebruiken** in op **Ja**.

3. Op het sneltabblad **Algemeen** kunt u de volgende waarden instellen:

    - Selecteer **Door gebruiker bestuurd** in het veld **Bestuurd door**.
    - Stel de optie **Nummerplaat maken** in op **Ja**.
    - Stel de optie **Groep verzamelen** in op **Ja**.

4. Voer op het sneltabblad **Werkklassen** de volgende stappen uit om de geldige werkklassen voor de menuopdracht voor mobiele apparaten te configureren:

    1. Selecteer **Nieuw**.
    2. Selecteer in het veld **Werkklasse-id** de optie **Verkoop** of **VO verzamelen**, afhankelijk van het magazijn dat u gebruikt.
    3. Selecteer **Verkooporders** in het veld **Werkordertype**.

### <a name="set-up-a-mobile-device-menu"></a>Een menu van een mobiel apparaat instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**. 
1. Voeg de zojuist gemaakte menuoptie toe aan het gewenste menu.

### <a name="set-up-a-work-template"></a>Een werksjabloon instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Zoek de werksjabloon die met deze functie moet worden gebruikt. Selecteer voor dit voorbeeld de standaardwerksjabloon van Contoso **51 Orderverzamelen voor fase**.
1. Selecteer **Query bewerken** in het menu.
1. Selecteer op het tabblad **Sorteren** de optie **Toevoegen** en stel de volgende waarden in:

    - Selecteer **Tijdelijke werktransacties** in het veld **Tabel**.
    - Selecteer **Tijdelijke werktransacties** in het veld **Afgeleide tabel**.
    - Selecteer **Artikelnummer** in het veld **Veld**.
    - Selecteer **Oplopend** in het veld **Zoekrichting**.

> [!NOTE]
> De groepering van orderverzamelregels werkt alleen als de werkregels zijn gesorteerd op artikel-id. Als regels met dezelfde artikels niet na elkaar worden geordend, worden ze niet gegroepeerd.

## <a name="example"></a>Voorbeeld

### <a name="create-picking-work"></a>Orderverzamelingswerk maken

Voordat u de groepering van orderverzamelregels kunt instellen, moet u in aanmerking komend uitgaand werk maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer **Nieuw** om een verkooporder te maken. 
3. Selecteer een klant in het veld **Klantrekening**. 
4. Selecteer op het sneltabblad **Algemeen** magazijn **51** in het veld **Magazijn**. Selecteer vervolgens **OK**.
5. Voeg onder **Verkooporderregels** de volgende zes regels toe:

    - **Regel 1:** selecteer in het veld **Artikelnummer** de optie **M9200**. Typ **3** in het veld **Hoeveelheid**.
    - **Regel 2:** selecteer in het veld **Artikelnummer** de optie **M9201**. Typ **3** in het veld **Hoeveelheid**. 
    - **Regel 3:** selecteer in het veld **Artikelnummer** de optie **M9202**. Typ **2** in het veld **Hoeveelheid**. 
    - **Regel 4:** selecteer in het veld **Artikelnummer** de optie **M9200**. Typ **1** in het veld **Hoeveelheid**. 
    - **Regel 5:** selecteer in het veld **Artikelnummer** de optie **M9200**. Typ **3** in het veld **Hoeveelheid**.
    - **Regel 6:** selecteer in het veld **Artikelnummer** de optie **M9202**. Typ **7** in het veld **Hoeveelheid**. 

    Hier is een overzicht van de totale aantallen voor elk artikel:

    - **Artikel M9200:** 7 elk
    - **Artikel M9201:** 3 elk
    - **Artikel M9202:** 9 elk

6. Voordat u de orders aan het magazijn vrijgeeft, moet u ervoor zorgen dat de picklocaties voldoende voorraad hebben voor alle artikelen op alle orders. Controleer de instelling **Locatie-instructie** om te bepalen welke orderverzamellocaties worden gebruikt voor het verzamelen van verkooporders.
7. Reserveer de voorraad en geef deze vrij aan het magazijn. Er wordt een werk-id met zes regels gemaakt. De regels worden gesorteerd op artikelnummer.

### <a name="run-the-mobile-device-flow"></a>De stroom voor mobiele apparaten uitvoeren

1. Selecteer op het mobiele apparaat het menu dat de nieuwe menuoptie voor mobiele apparaten bevat.
1. Selecteer de menuoptie **Orderverzamelen verkoop - Groepsregel** en initieer de orderverzameling.

    Nadat u het menu hebt selecteren en de werk-id hebt ingevoerd, ziet u de verzamelstap waarin alle pickregels voor artikel M9200 zijn gegroepeerd. U ontvangt de instructie om 7 stuks van elk artikel M9200 te kiezen.

1. Bevestig de verzamelstap. 
1. Ga naar het clientscherm van het onderhanden werk om te zien dat alle drie de orderverzamelregels voor artikel M9200 tegelijkertijd zijn gesloten.

    Werkregel 4 wordt weergegeven.

1. Bevestig de verzamelstap.

    Met de laatste orderverzamelstap op het mobiele apparaat worden de laatste twee orderverzamelregels uit de werkorder samengevoegd.

1. Voltooi de orderverzamelstap voor 9 stuks van elk artikel M9202.
1. Bevestig de wegzetstap en eventuele extra verzamel-/wegzetparen om het werk te voltooien.

> [!NOTE]
> - Werkregels kunnen alleen worden gegroepeerd als ze op volgorde zijn.
> - De volgende functionaliteit wordt niet ondersteund:
>
>    - Catch weight-artikelen. Als er catch weight-artikelen voor het werk aanwezig zijn, wordt een foutbericht weergegeven voordat u begint te kiezen.
>    - Orderverzameling.
>    - Werkregels met onvoltooid aanvullingswerk.
>    - Meerverzameling.
>    - Kort orderverzamelen met artikelhertoewijzing


[!INCLUDE[footer-include](../../includes/footer-banner.md)]