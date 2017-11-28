---
title: De indelingen voor schermen met demonstratiegegevens in MPOS/CPOS
description: Dit onderwerp bevat informatie over de schermindelingen die zijn opgenomen in de voorbeeldgegevensset voor de POS-ervaringen (Point Of Sale) in Microsoft Dynamics 365 for Retail.
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 563c89c75e2136294f8f841bec094c2aeb85d580
ms.openlocfilehash: b758b48230e8d9fabdccbe267a6ad6b9e74af0ff
ms.contentlocale: nl-nl
ms.lasthandoff: 10/17/2017

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a>Indelingen voor schermen met demonstratiegegevens in MPOS/CPOS

Dit onderwerp bevat informatie over de schermindelingen die zijn opgenomen in de voorbeeldgegevensset voor de POS-ervaringen (Point Of Sale) in Microsoft Dynamics 365 for Retail.

## <a name="overview"></a>Overzicht

De voorbeeldschermindelingen die zijn opgenomen in de Retail-demonstratiegegevens bieden inhoud die is geoptimaliseerd voor verschillende segmenten van de detailhandel, winkelmedewerkerrollen en apparaten. Eén indeling kan verschillende indelingsformaten en combinaties van knoppenrasters bevatten om in de behoefte te kunnen blijven voorzien wanneer werknemers tussen apparaten en stations schakelen. Dit onderwerp biedt meer informatie over de verschillen tussen deze indelingen, de mogelijkheden die ze bieden en de algehele ervaring die ze leveren.

![Apparaatonafhankelijke demonstratiegegevensindelingen](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Anatomie van een schermindelings-id

In Retail vindt u schermindelingen via **Retail** > **Afzetkanaalinstellingen** > **POS-instellingen** > **POS** > **Schermindelingen**.

![Pagina Schermindelingen in Retail](../retail/media/demo-screen-layouts-fig-2-1.png)

Schermindeling-id's kunnen uit maximaal 10 tekens bestaan. De id is een tekenreeks die uit drie soorten informatie bestaat, in de volgende volgorde:

1. Bedrijf
2. Indelingsversie
3. Persona

### <a name="company"></a>Bedrijf

| Brief | Bedrijf         |
|--------|-----------------|
| V      | Adventure Works |
| F      | Fabrikam        |
| E      | Contoso         |

### <a name="layout-version"></a>Indelingsversie

| Versienummer | Omschrijving                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | De basisversie die ondersteuning biedt voor meerdere schermformaten voor verschillende apparaten en hoogte-breedteverhoudingen |
| 3.1            | De basisversie met extra ondersteuning voor het deelvenster **Aanbevolen producten**        |

### <a name="persona"></a>Persona

| Afkorting | Persona       | Inhoud |
|--------------|---------------|----------|
| KAS          | Kassier       | Kassierindelingen bevatten alle transactiegerelateerde bewerkingen, zoals klantorders, retouren, kortingen, ongeldig gemaakte transacties en geschenkbonnen. Deze indelingen bevatten ook dagelijkse taken voor voorraadbeheer, zoals prijscontroles, voorraadzoekopdrachten en voorraadtellingen. Daarnaast zijn algemene functies voor ploegenbeheer beschikbaar voor beginbedragen, het uitstellen van diensten en de tijdklok. |
| MGR          | Winkelmanager | Winkelmanagerindelingen bevatten alle transactiegerelateerde bewerkingen die ook te vinden zijn in de indelingen voor kassiers en bevatten daarnaast btw-overschrijvingen. Deze indelingen bevatten ook dagelijkse taken voor voorraadbeheer, zoals prijscontroles, voorraadzoekopdrachten en voorraadtellingen. Er zijn functies voor ploegenbeheer beschikbaar voor het starten, uitstellen en sluiten van diensten. Daarnaast bevatten de indelingen ladebewerkingen voor opnames, verwijderingen, kascontroles en kluis- en bankstortingen. Ten slotte bieden deze indelingen toegang tot prestatierapporten en kunnen er X- en Z-rapporten worden afgedrukt. |
| MMW          | Magazijnmedewerker   | Indelingen voor magazijnmedewerkers zijn geoptimaliseerd voor voorraadbeheer. Deze bieden toegang tot dagelijkse taken voor prijscontroles, voorraadzoekopdrachten, orderverzameling en ontvangst, voorraadtellingen en kitdemontage. Deze indelingen bieden ook basisbewerkingen voor ploegen, voor de tijdklok en het uitstellen van diensten. Hoewel deze indelingen hoofdzakelijk voor backofficetaken bedoeld zijn, kunnen magazijnmedewerkers dezelfde bewerkingen als kassiers uitvoeren voor transactieschermen. |

### <a name="example-layout"></a>Voorbeeldindeling

Hier is een voorbeeld van een schermindelings-id voor het bedrijf Fabrikam, indelingsversie 3, en de persona Winkelmanager:

F3MGR

In de volgende afbeelding wordt een voorbeeld van het welkomstscherm voor een winkelmanager van Fabrikam weergegeven.

![Welkomstscherm voor de winkelmanager van Fabrikam](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Indelingsgrootten

### <a name="full-vs-compact-layouts"></a>Volledige versus compacte indelingen

Een schermindeling kan configuraties voor zowel volledige als compacte apparaten bevatten. Daarom kan een gebruiker worden toegewezen aan één schermindeling die werkt op verschillende afmetingen en vormfactoren in de winkel.

- **Modern POS - volledig**: volledige indelingen zijn normaal gesproken het meest geschikt voor grotere beeldschermen, zoals computerbeeldschermen en tablets. Gebruikers kunnen de UI-elementen in de indeling selecteren, de grootte en positie van die elementen opgeven en hun gedetailleerde eigenschappen configureren. Volledige indelingen ondersteunen zowel staande (portrait) als liggende (landscape) configuraties.
- **Modern POS - compact**: compacte indelingen zijn normaal gesproken het meest geschikt voor telefoons of kleine tablets. De ontwerpmogelijkheden zijn beperkt voor compacte apparaten. Gebruikers kunnen de kolommen en velden voor de deelvensters Ontvangstbewijs en Totalen configureren.

### <a name="screen-resolutions-that-are-provided"></a>Geleverde schermresoluties

In de volgende tabel worden de indelingsformaten weergegeven die beschikbaar zijn voor normale schermresoluties.

| Indelingstype | Resolutie | Hoogte-breedteverhouding | Doelweergave          |
|-------------|------------|--------------|-------------------------|
| Klein\*   | 480 × 853  | 16:9         | Telefoons                  |
| Volledig        | 1024 × 768 | 4:3          | Tablets                 |
| Volledig\*      | 1280 × 720 | 16:9         | Tablets                 |
| Volledig        | 1366 × 768 | 16:9         | Tablets, grotere schermen |
| Volledig        | 1440 × 960 | 3:2          | Tablets, grotere schermen |

\* Deze extra indelingsformaten zijn alleen beschikbaar in Adventure Works- en Fabrikam-indelingen.


>[!TIP]
> POS selecteert automatisch indelingsformaten, gebaseerd op de dichtstbijzijnde grootte die voor de schermresolutie van het huidige appvenster beschikbaar is. U vindt de schermindelings-id en indelingsresolutie die momenteel worden gebruikt door Retail Modern POS (MPOS) of Retail Cloud POS (CPOS) te openen, de pagina **Instellingen** te openen en de sectie **Sessie-informatie** te bekijken. U kunt ook de werkelijke vensterresolutie voor uw huidige toepassing of browserframe bekijken. Als u deze gegevens hebt, kunt u de bron van de indelingsinhoud in Retail vinden door naar **Afzetkanaalinstellingen** > **POS-instellingen** > **POS** > **Schermindelingen** te gaan.


![Schermindelingen en indelingsresoluties/-formaten in Retail en POS](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Bedrijven en merken

Elk fictief bedrijf is gericht op een ander segment en bevat productcatalogi die specifiek bedoeld zijn voor de markt van het bedrijf. Elk bedrijf heeft een unieke visuele stijl die bij de producten hoort. Tot de huisstijlelementen behoren de accentkleur, een donker of licht thema en begeleidende foto's die realistische ervaringen bieden.

### <a name="company-segment-and-visual-characteristics"></a>Bedrijfssegment en visuele kenmerken

| Bedrijf         | Locatie | Segment        | Accent | Thema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sportartikelen | Blauw   | Donker  |
| Fabrikam        | Houston  | Mode        | Groen  | Licht |
| Contoso         | Boston   | Elektronica    | Rood    | Donker  |


>[!NOTE]
> Adventure Works en Fabrikam zijn de twee vlaggenschipmerken. Contoso is beschikbaar, maar niet alle indelingen.


In de volgende afbeeldingen ziet u voorbeelden van de welkomstpagina en transactiepagina voor de drie fictieve bedrijven.

### <a name="adventure-works"></a>Adventure Works

![Welkomstpagina met demonstratiegegevens voor Adventure Works](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Transactiepagina met demonstratiegegevens voor Adventure Works](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Welkomstpagina met demonstratiegegevens voor Fabrikam](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Transactiepagina met demonstratiegegevens voor Fabrikam](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Indelingen met demonstratiegegevens voor Contoso](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Matrix voor gebruikersaanmelding

Er zijn al gebruikers opgegeven voor de verschillende schermindelingen. Met behulp van de volgende tabel moet u toegang kunnen krijgen tot elk van deze schermen. U hoeft u alleen maar aan te melden met een juiste operator-id.

| Bedrijf         | Schermindelings-id | Persona          | Operator-id's           |
|-----------------|------------------|---------------   |------------------------|
| Adventure Works | A3MGR            | Winkelmanager    | 000154, 000137, 000073 |
| Adventure Works | A3KAS            | Kassier          | 000150, 000175, 000165 |
| Adventure Works | A3MMW            | Magazijnmedewerker      | 000155, 000181, 000152 |
| Fabrikam        | F3MGR            | Winkelmanager    | 000160, 000168, 000163 |
| Fabrikam        | F3KAS            | Kassier          | 000161, 000113, 000114 |
| Fabrikam        | F3MMW            | Magazijnmedewerker      | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Winkelmanager    | 000100, 000111         |
| Contoso         | C3KAS            | Kassier          | 000110, 000120         |
| Contoso         | Niet van toepassing   | Magazijnmedewerker      | Niet van toepassing         |


>[!TIP]
> Activeer voor de beste resultaten een journaal in de bijbehorende winkellocatie en stel het bedrijf in op de persona waarmee u zich wilt aanmelden. Op deze manier kunt u ervoor zorgen dat het visuele profiel en brandingafbeeldingen consistent op elkaar zijn afgestemd. Als u een Fabrikam-indeling voor een kassamedewerker wilt bekijken, moet u bijvoorbeeld een journaal in de winkel in Houston activeren.


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

