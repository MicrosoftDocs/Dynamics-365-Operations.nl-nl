---
title: Schermindelingen voor het verkooppunt (POS)
description: Dit onderwerp biedt informatie over schermindelingen voor Microsoft Dynamics 365 for Retail POS.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ced27adb8fe481270cb008e187693cda96773339
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="screen-layouts-for-the-point-of-sale-pos"></a>Schermindelingen voor het verkooppunt (POS)

[!include [banner](includes/banner.md)]

Dit onderwerp biedt informatie over schermindelingen voor Microsoft Dynamics 365 for Retail POS.

De gebruikersinterface van Retail POS kan worden geconfigureerd met een combinatie van weergaveprofielen en schermindelingen die worden toegewezen aan winkels, kassa's en/of gebruikers.

In de volgende afbeelding worden de relaties weergegeven tussen de verschillende eenheden waaruit de configureerbare aspecten van de POS-gebruikersinterface bestaan.

![Entiteiten voor POS-schermindeling](../retail/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Weergaveprofiel
Weergaveprofielen worden toegewezen aan kassa's en worden gebruikt om de weergave-elementen op te geven die specifiek zijn voor kassa's en worden gedeeld door gebruikers. Alle gebruikers die zich aanmelden bij de kassa krijgen hetzelfde thema en dezelfde kleuren en afbeeldingen te zien.

![POS-welkomstscherm met licht thema](../retail/media/POS-Welcome-Screen-with-Light-theme.png)

![POS-transactiescherm met donker thema](../retail/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profielnummer**: het profielnummer is de unieke id van het weergaveprofiel.
- **Beschrijving**: u kunt een beschrijvende naam opgeven om het juiste profiel voor uw situatie te identificeren.
- **Thema**: u kunt kiezen tussen de lichte en donkere toepassingthema's. Het thema heeft invloed op de tekst- en achtergrondkleuren in de toepassing.
- **Accentkleur**: de accentkleur wordt overal in het POS gebruikt om bepaalde weergave-elementen, zoals tegels, opdrachtknoppen en hyperlinks, te onderscheiden of te markeren. Deze elementen zijn doorgaans uitvoerbaar.
- **Koptekstkleur**: u kunt de kleur van de koptekst van de pagina configureren om te voldoen aan de huisstijlvereisten van de detailhandelaar. Deze functie is alleen beschikbaar in versie 1611 van Microsoft Dynamics 365 for Retail.
- **Aanmeldingsachtergrond**: u kunt een achtergrondafbeelding opgeven voor het aanmeldingsscherm. De bestandsgrootte van achtergrondafbeeldingen moet zo klein mogelijk worden gehouden omdat het opslaan en laden van grote bestanden het gedrag en de prestaties van de toepassing kunnen beïnvloeden.
- **Achtergrond van de toepassing**: u kunt een achtergrondafbeelding kiezen om in de hele toepassing te gebruiken in plaats van de effen themakleur. Voor aanmeldingsachtergronden moet de bestandsgrootte zo klein mogelijk worden gehouden.

## <a name="screen-layouts"></a>Schermindelingen
Schermindelingsconfiguraties bepalen de acties, inhoud en plaatsing van de UI-besturingselementen in het POS-welkomstscherm en het scherm **Transactie**.

![Weergave POS-schermindeling](../retail/media/POS-Screen-Layout-View.png)

- **Welkomstscherm**: in de meeste gevallen zien gebruikers het welkomstscherm als eerste nadat zij zich hebben aangemeld bij het POS. Het welkomstscherm kan bestaan uit een branding-afbeelding en knoppenrasters die toegang tot POS-bewerkingen bieden. Normaal gesproken worden hier bewerkingen weergegeven die niet specifiek van toepassing op de huidige transactie zijn.

    ![POS-welkomstscherm](../retail/media/POS-Welcome-Screen.png)

- **Transactiescherm**: het scherm **Transactie** is het hoofdscherm in het POS voor de verwerking van verkooptransacties en orders. De inhoud en indeling worden geconfigureerd met behulp van de ontwerper van schermindelingen.

    ![POS-transactiescherm](../retail/media/POS-Transaction-Screen.png)

- **Standaardstartscherm**: sommige detailhandelaren geven er de voorkeur aan dat kassamedewerkers na het aanmelden rechtstreeks naar het scherm **Transactie** gaan. Via de instelling **Standaardstartscherm** kunt u het standaardscherm opgeven dat na het aanmelden voor elke schermindeling wordt weergegeven.

### <a name="assignment"></a>Toewijzing

Schermindelingen kunnen worden toegewezen op het niveau van de winkel, kassa of gebruiker. De gebruikerstoewijzing heeft voorrang op de kassa- en winkeltoewijzingen, de kassatoewijzing heeft voorrang op de winkeltoewijzing. In een eenvoudig scenario waarin alle gebruikers dezelfde indeling gebruiken, ongeacht de kassa of rol, kan de schermindeling alleen op winkelniveau worden ingesteld. In gevallen waarin bepaalde kassa's of gebruikers speciale indelingen vereisen, kunnen deze worden toegewezen.

### <a name="layout-sizes"></a>Indelingsgrootten

De meeste aspecten van de POS-gebruikersinterface zijn responsief en de lay-out wordt automatisch aangepast aan de grootte en stand van het scherm. Het POS-scherm **Transactie** moet echter worden geconfigureerd voor elke verwachte schermresolutie.

Bij het opstarten selecteert de POS-toepassing automatisch de indelingsgrootte die is geconfigureerd voor het apparaat. Een schermindeling kan ook configuraties voor de modi Liggend en Staand bevatten en voor volwaardige en compacte apparaten. Daarom kunnen gebruikers worden toegewezen aan één schermindeling die werkt voor verschillende afmetingen en vormfactoren die worden gebruikt in de winkel.

![POS-indelingsgrootten](../retail/media/POS-Screen-Layout-Sizes.png)

- **Naam**: u kunt een omschrijvende naam invoeren om de schermgrootte te identificeren.
- **Indelingstype**: in de POS-toepassing kan de gebruikersinterface in verschillende modi worden weergegeven om de beste gebruikerservaring op een bepaald apparaat te kunnen bieden.

    - **Modern POS - volledig**: volledige indelingen zijn doorgaans het meest geschikt voor grotere beeldschermen, zoals pc-beeldschermen en tablets. U kunt de gewenste gebruikersinterface-elementen selecteren, de grootte en positie van die elementen opgeven en hun gedetailleerde eigenschappen configureren. Volledige indelingen ondersteunen zowel staande (portrait) als liggende (landscape) configuraties.
    - **Modern POS - compact**: compacte indelingen zijn normaal gesproken het meest geschikt voor telefoons en kleine tablets. De ontwerpmogelijkheden zijn beperkt voor compacte apparaten. U kunt de kolommen en velden voor de deelvensters Ontvangstbewijs en Totalen configureren.

- **Breedte/Hoogte**: deze waarden staan voor de effectieve schermgrootte, in pixels, die wordt verwacht voor de indeling. Houd er rekening mee dat sommige besturingssystemen voor beeldschermen met hoge resoluties gebruikmaken van schaalaanpassingen.

> [!TIP]
> U kunt de vereiste indelingsgrootte voor een POS-scherm achterhalen door de resolutie in de app te bekijken. Start het POS en ga naar **Instellingen \> Sessie-informatie**. In het POS worden de momenteel geladen schermindeling, de indelingsgrootte en de resolutie van het app-venster weergegeven.

![POS-indelingsgrootten](../retail/media/POS-Session-Information.png)

### <a name="button-grids"></a>Knoppenrasters
Voor elke indelingsgrootte in een schermindeling kunt u knoppenrasters configureren en toewijzen voor het POS-welkomstscherm en het scherm **Transactie**. Knoppenrasters voor het welkomstscherm worden automatisch van links naar rechts, van het laagste nummer (welkomstscherm 1) naar het hoogste nummer weergegeven.

In volledige POS-indelingen wordt de plaats van knoppenrasters opgegeven in de ontwerper van schermindelingen.

In compacte POS-indelingen worden de knoppenrasters automatisch van boven naar beneden, van het laagste nummer (transactiescherm 1) naar het hoogste nummer weergegeven. Deze kunnen worden geopend in het menu **Acties**.

![Knoppenrasters voor compacte indelingen](../retail/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Afbeeldingen
Voor elke indelingsgrootte in een schermindeling kunt u afbeeldingen opgeven die moeten worden opgenomen in de POS-gebruikersinterface. Voor volledige POS-indelingen kan één afbeelding worden opgegeven voor het welkomstscherm. Deze afbeelding wordt links als het eerste element in de gebruikersinterface weergegeven. In het scherm **Transactie** kunnen afbeeldingen worden gebruikt als tabbladafbeeldingen of als logo. In compacte POS-indelingen worden deze afbeeldingen niet gebruikt.

### <a name="screen-layout-designer"></a>Ontwerper van schermindeling

In de ontwerper van schermindelingen kunt u verschillende aspecten van het POS-scherm **Transactie** configureren voor elke indelingsgrootte, zowel in de modus Staand als in de modus Liggend, zowel voor volledige als voor compacte indelingen. In de ontwerper van schermindelingen wordt de ClickOnce-implementatietechnologie gebruikt om altijd de meest recente versie van de toepassing te downloaden, te installeren en te starten als de gebruiker deze ontwerper opent. Controleer de browservereisten voor ClickOnce. In sommige browsers, zoals Google Chrome, zijn extensies vereist.

> [!IMPORTANT]
> U moet een schermindeling configureren voor elke indelingsgrootte die is gedefinieerd en wordt gebruikt door het POS.

### <a name="full-layout-designer"></a>Ontwerper van volledige indeling

In de ontwerper van volledige indelingen kunnen gebruikers besturingselementen in de gebruikersinterface naar het POS-scherm **Transactie** slepen en de instellingen van deze elementen configureren.

![Ontwerper van volledige POS-indeling (modus Liggend)](../retail/media/POS-Full-Layout-Designer-Landscape.png)

- **Indeling importeren/exporteren**: u kunt ontwerpen van POS-schermindelingen importeren en exporteren als XML-bestanden, zodat u deze eenvoudig opnieuw kunt gebruiken en kunt delen in verschillende omgevingen. Het is belangrijk dat u indelingsontwerpen voor de juiste indelingsformaten importeert. Anders passen gebruikersinterface-elementen mogelijk niet goed op het scherm.
- **Liggen/Staand**: als het POS-apparaat gebruikers in staat stelt te schakelen tussen de modi Liggend en Staand, moet u een schermindeling voor elke modus definiëren. Het POS detecteert schermrotatie automatisch om de juiste indeling te kunnen weergeven.
- **Indelingsraster**: in de POS-indelingsontwerper wordt een raster van 4 pixels gebruikt. UI-besturingselementen worden vastgezet op het raster zodat u de inhoud juist kunt uitlijnen.
- **Inzoomen in ontwerper**: u kunt in- en uitzoomen in de ontwerperweergave om de inhoud in het POS-scherm beter te kunnen bekijken. Deze functie is handig wanneer de schermresolutie in het POS aanzienlijk afwijkt van de resolutie van het scherm dat wordt gebruikt in de ontwerper.
- **Navigatiebalk weergeven/verbergen**: voor volledige POS-indelingen kunt u opgeven of de linkernavigatiebalk moet worden weergegeven in het scherm **Transactie**. Deze functie is handig voor weergaven met een lagere resolutie. Als u de zichtbaarheid wilt instellen, klikt u met de rechtermuisknop op de navigatiebalk in de ontwerper en schakelt u het selectievakje **Altijd zichtbaar** in of uit. Als de navigatiebalk is verborgen, kunnen POS-gebruikers deze nog steeds gebruiken via het menu in de linkerbovenhoek.

    ![Navigatiebalk weergeven/verbergen](../retail/media/Navigation-Bar.PNG)

- **POS-besturingselementen**: in de POS-indelingsontwerper worden de volgende besturingselementen ondersteund. U kunt veel besturingselementen configureren met de rechtermuisknop en het snelmenu.

    ![Besturingselementen in POS-gebruikersinterface](../retail/media/POS-UI-Controls.png)

    - **Numeriek toetsenblok**: het toetsenblok is het belangrijkste mechanisme voor gebruikersinvoer in het POS-scherm **Tranasactie**. U kunt het besturingselement zo configureren dat het volledige toetsenblok wordt weergegeven. Deze optie is ideaal voor apparaten met een aanraakscherm. U kunt deze ook zo configureren dat alleen het invoerveld wordt weergegeven. In dit geval wordt een fysiek toetsenbord gebruikt voor invoer. De instellingen voor het numerieke toetsenblok zijn alleen beschikbaar voor volledige indelingen. Voor compacte indelingen wordt het volledige toetsenblok weergegeven in het scherm **Transactie**.
    - **Deelvenster Totalen**: u kunt het deelvenster Totalen configureren in een of twee kolommen, om waarden als het aantal regels, kortingsbedrag, toeslagen, subtotaal en btw weer te geven. Compacte indelingen bieden slechts ondersteuning voor één kolom.
    - **Deelvenster Ontvangst**: het deelvenster Ontvangst bevat de verkoopregels, betalingsregels en leveringsinformatie voor de producten en services die worden verwerkt in het POS. U kunt de kolommen, breedte en plaatsing opgeven. In compacte indelingen kunt u ook extra informatie configureren die wordt weergegeven in de rij onder de hoofdregel.
    - **Klantenkaart**: de klantenkaart bevat gegevens over de klant die is gekoppeld aan de huidige transactie. U kunt de klantenkaart configureren om extra informatie weer te geven of te verbergen.
    - **Tabblad**: u kunt het tabblad toevoegen aan een schermindeling en vervolgens andere besturingselementen, zoals het toetsenblok, een klantenkaart of knoppenrasters, op het tabblad plaatsen. Het tabblad is een container waarmee u meer inhoud op het scherm kunt plaatsen. Het tabblad is alleen beschikbaar voor volledige indelingen.
    - **Afbeelding**: u kunt het afbeeldingsbesturingselement gebruiken om het winkellogo of andere branding-afbeeldingen weer te geven in het scherm **Transactie**. Het afbeeldingsbesturingselement is alleen beschikbaar voor volledige indelingen.
    - **Aanbevolen producten**: als het besturingselement voor aanbevolen producten is geconfigureerd voor de omgeving, worden hierin productsuggesties op basis van machine learning weergegeven.
    - **Aangepast besturingselement**: het aangepaste besturingselement fungeert als een tijdelijke aanduiding in de schermindeling. Hiermee kunt u ruimte reserveren voor aangepaste inhoud. Het aangepaste besturingselement is alleen beschikbaar voor volledige indelingen.

### <a name="compact-layout-designer"></a>Ontwerper voor compacte indeling
Net als in de ontwerper voor de volledige indeling kunt u in de ontwerper voor de compacte indeling de POS-schermindeling voor telefoons en kleine tablets configureren. In dit geval wordt echter de indeling zelf opgelost. U kunt de besturingselementen in de indeling configureren met de rechtermuisknop en het snelmenu. Voor extra inhoud kunt u echter niet gebruikmaken van de functie voor slepen en neerzetten.

![Ontwerper van compacte indeling](../retail/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Ontwerper van knoppenraster
In de ontwerper van het knoppenraster kunt u knoppenrasters configureren die kunnen worden gebruikt in het POS-welkomstscherm en het scherm **Transactie**, zowel voor volledige als compacte indelingen. Hetzelfde knoppenraster kan voor verschillende indelingen en indelingstypen worden gebruikt. Net als in de schermindelingsontwerper wordt in de ontwerper van het knoppenraster de ClickOnce-implementatietechnologie gebruikt om altijd de meest recente versie van de toepassing te downloaden, te installeren en te starten als de gebruiker deze ontwerper opent. Controleer de browservereisten voor ClickOnce. In sommige browsers, zoals Google Chrome, zijn extensies vereist.

![Ontwerper van knoppenraster](../retail/media/Button-Grid-Designer.png)

- **Knop Nieuw**: klik hierop om een nieuwe knop toe te voegen aan het knoppenraster. Nieuwe knoppen worden standaard in de linkerbovenhoek van het raster weergegeven. U kunt knoppen echter schikken door ze te slepen in de indeling.

    > [!IMPORTANT]
    > De inhoud van het knoppenraster kan overlappen. Wanneer u knoppen schikt, moet u ervoor zorgen dat andere knoppen niet worden verborgen.

- **Nieuw ontwerp**: klik hierop om automatisch een knoppenrasterindeling in te stellen door het aantal knoppen per rij en kolom op te geven.
- **Knopeigenschappen**: u kunt knopeigenschappen configureren door met de rechtermuisknop op de knop te klikken en het snelmenu te gebruiken.

    > [!IMPORTANT]
    > Sommige knoppenrasterinstellingen gelden alleen voor Enterprise POS en niet voor Retail Modern POS of Cloud POS.

    ![Knopeigenschappen voor knoppenraster](../retail/media/Button-grid-button-properties.png)

    - **Actie**: selecteer in de lijst met relevante POS-bewerkingen de bewerking die wordt geactiveerd als op de knop wordt geklikt in het POS.

        Zie [POS-bewerkingen, online en offline](pos-operations.md) voor een overzicht van ondersteunde POS-bewerkingen.

    - **Actieparameters**: voor sommige POS-bewerkingen worden aanvullende parameters gebruikt wanneer ze worden aangeroepen. Gebruikers kunnen voor de bewerking Product toevoegen bijvoorbeeld opgeven welk product moet worden toegevoegd.
    - **Knoptekst**: geef de tekst op die moet worden weergegeven op de knop in het POS.
    - **Knoptekst verbergen**: gebruik dit selectievakje om de knoptekst weer te geven of te verbergen. Knoptekst wordt vaak verborgen voor kleine knoppen waarop alleen een pictogram past.
    - **Knopinfo**: geef extra Help-tekst op die wordt weergegeven wanneer gebruikers de muisaanwijzer over de knop bewegen.
    - **Grootte in kolommen/rijen**: u kunt opgeven hoe hoog en breed de knop moet zijn.

        ![Grootte van POS-knoppen in rijen en kolommen](../retail/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Aangepast lettertype**: wanneer u het selectievakje **Aangepast lettertype inschakelen voor POS** inschakelt, kunt u een ander lettertype opgeven dan het standaardsysteemlettertype voor het POS.
    - **Aangepast thema**: standaard wordt voor POS-knoppen de accentkleur van het weergaveprofiel gebruikt. Als u het selectievakje **Aangepast thema gebruiken** inschakelt, kunt u extra kleuren opgeven.

        > [!NOTE]
        > In Retail Modern POS en Cloud POS worden alleen de waarden **Achtergrondkleur** en **Tekenkleur** gebruikt.

    - **Afbeelding van knop**: knoppen kunnen afbeeldingen of pictogrammen bevatten. Maak een keuze uit de beschikbare afbeeldingen die zijn opgegeven via **Retail \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> Afbeeldingen**.

![Voorbeeld van knoppenraster in het POS](../retail/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Aanvullende resources

[De Retail POS-indelingsontwerper installeren](install-pos-layout-designer.md)

