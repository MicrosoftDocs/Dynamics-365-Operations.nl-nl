---
title: Schermindelingen configureren voor POS
description: Dit onderwerp biedt informatie over schermindelingen voor het gebruik van Microsoft Dynamics 365 for Operations - Retail POS.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7dee20166ea89b56523e3ef38e66de53d6e4a621
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Schermindelingen configureren voor POS

[!include[banner](includes/banner.md)]


Dit onderwerp biedt informatie over schermindelingen voor het gebruik van Microsoft Dynamics 365 for Operations - Retail POS.

De gebruikersinterface van Microsoft Dynamics 365 for Operations - Retail POS kan worden geconfigureerd met een combinatie van weergaveprofielen en schermindelingen, die u toewijst aan winkels, kassa's en/of gebruikers.

## <a name="visual-profile"></a>Weergaveprofiel
Weergaveprofielen worden toegewezen aan kassa's en worden gebruikt om de visuele elementen op te geven die specifiek zijn voor kassa's en worden gedeeld door gebruikers. Alle gebruikers die zich aanmelden bij de kasse werken met hetzelfde thema en dezelfde kleuren en afbeeldingen. 

**Profielnummer**: Het profielnummer is de unieke id van het weergaveprofiel. 

**Beschrijving**: In de beschrijving kunt u een omschrijvende naam opgeven die helpt bij om het juiste profiel voor uw situatie te identificeren.

**Thema**: Gebruikers kunnen kiezen tussen de lichte en de donktere toepassingthema's. Deze instellingen zijn van invloed op de kleur voor tekst en achtergrond in de gehele toepassing.

**Accentkleur**: De accentkleur wordt overal in het POS gebruikt om bepaalde visuele elementen zoals tegels, opdrachtknoppen of hyperlinks te differentiëren of te markeren. Deze elementen zijn meestal uitvoerbaar.

**Koptekstkleur**: Met de koptekstkleur kan de gebruiker de kleur van de paginakoptekst configureren, zodat deze aansluit bij de brandingbehoefte van de detailhandelaar. Deze functie is alleen beschikbaar in Dynamics 365 for Operations, versie 1611.

**Aanmeldingsachtergrond**: Gebruikers kunnen een achtergrondafbeelding opgeven voor het aanmeldingsscherm. De bestandsgrootte van achtergrondafbeeldingen moet zo klein mogelijk worden ghouden, omdat het opslaan en laden van grote bestanden het gedrag en de prestaties van de toepassing kunnen beïnvloeden.

**Achtergrond van de toepassing**: Het POS kan ook een in de gehele toepassing een afbeelding als achtergrond gebruiken in plaats van de effen themakleur. Net als bij de aanmeldingsachtergrond wordt het aanbevolen de bestandsgrootte zo klein mogelijk te houden.

## <a name="screen-layouts"></a>Schermindelingen
De schermindelingsconfiguratie bepaalt de acties, inhoud en plaatsing van de UI-besturingselementen in de POS-schermen Welkom en Transactie. 

**Welkomstscherm**: in de meeste gevallen zien gebruikers het Welkomstscherm het eerst wanneer zij zich aanmelden bij het POS. Het Welkomstscherm kan bestaan uit een afbeelding met de branding en knoppenrasters die toegang tot POS-bewerkingen bieden. Normaal gesproken worden hier bewerkingen geplaatst die niet specifiek voor de huidige transactie zijn. 

**Transactiescherm**: Het transactiescherm is het hoofdscherm in POS voor verwerking van verkooptransacties en orders. Het transactiescherm kan worden geconfigureerd met behulp van de schermindelingontwerper. 

**Standaardstartscherm**: Sommige detailhandelaren geven er de voorkeur aan dat de kassamedewerker na het aanmelden rechtstreeks naar het transactiescherm wordt doorgezonden. Met de instelling voor het standaardstartscherm kunnen gebruikers deze optie instellen voor elke schermindeling.

### <a name="assignment"></a>Toewijzing

Schermindelingen kunnen worden toegewezen op het niveau van de winkel, kassa of gebruiker. De gebruikerstoewijzing heeft voorrang op de toewijzing voor de kassa en de winkel; de kassatoewijzing heeft voorrang op de toewijzing voor de winkel. In een eenvoudig scenario waarin alle gebruikers dezelfde indeling gebruiken, ongeacht de kassa of rol, kan de schermindeling alleen voor de winkel worden ingesteld. In gevallen waarin bepaalde kassa's of gebruikers speciale indelingen vereisen, kunnen ze dienovereenkomstig worden toegewezen.

### <a name="layout-sizes"></a>Indelingsgrootten

Deze functie is alleen beschikbaar in Dynamics 365 for Operations, versie 1611. Omdat in veel gevallen schermindelingen in meerdere schermformaten en -resoluties kunnen worden gebruikt, kunnen gebruikers hun indeling en inhoud voor elk daarvan configureren. De POS-toepassing kiest bij het opstarten automatisch de indelingsgrootte die het best bij het apparaat past. Een schermindeling kan ook configuraties voor zowel volledige als ook compacte apparaten bevatten. Met deze configuratie kan een gebruiker worden toegewezen aan een enkele schermindeling die functioneert op verschillende afmetingen en vormfactor in de winkel. 

**Modern POS - volledig**: Volledige indelingen zijn normaal gesproken het meest geschikt voor grotere beeldschermen, zoals pc-monitors en tablets. Gebruikers kunnen kiezen welke UI-elementen worden opgenomen, de grootte en plaatsing ervan bepalen en de gedetailleerde eigenschappen configureren. Volledige indelingen ondersteunen zowel staande (portrait) als liggende (landscape) configuraties. 

**Modern POS - compact**: Compacte indelingen zijn normaal gesproken het meest geschikt voor telefoons of kleine tablets. De ontwerpmogelijkheden zijn beperkt voor compacte apparaten. Gebruikers kunnen de kolommen en velden voor de deelvensters Ontvangstbewijs en Totalen.

### <a name="screen-layout-designer"></a>De schermindelingontwerper

De grootte van elke indeling binnen een schermindeling moet worden geconfigureerd door middel van de schermindelingontwerper. In de ontwerper kunnen gebruikers de UI-elementen van het transactiescherm opgeven en configureren. De schermindelingontwerper gebruikt ClickOnce om de meest recente versie van de toepassing te downloaden, installeren en starten, telkens wanneer die de gebruiker deze opent. Controleer de browservereisten voor het gebruik van ClickOnce; sommige browsers, zoals Chrome, vereisen hiervoor extensies. 

**Numeriek toetsenblok**: Het toetsenblok is de belangrijkste gebruikersinvoer in het transactiescherm in POS. Het kan worden geconfigureerd om het gehele toetsenblok op het scherm weer te geven, wat ideaal is voor touchscreens, of alleen het invoerveld, dat kan worden gebruikt met een fysiek toetsenbord. De instellingen voor het numeriek toetsenblok zijn alleen beschikbaar in de volledige indeling. In Dynamics 365 for Operations, versie 1611, is voor compacte indelingen altijd het volledige toetsenblok beschikbaar vanuit het transactiescherm.

**Deelvenster Totalen**: Het deelvenster Totalen kan worden geconfigureerd in een of twee kolommen, met velden zoals aantal regels, kortingsbedrag, toeslagen, subtotaal, en btw. In Dynamics 365 for Operations, versie 1611, ondersteunen compacte indelingen alleen één enkele kolom met totalen. 

**Ontvangst**: het deelvenster Ontvangst bevat de verkoopregels, betalingsregels en leveringsinformatie voor de producten en services die worden verwerkt in het POS. Gebruikers kunnen de kolommen, breedte en plaatsing opgeven. In compacte indelingen in Dynamics 365 for Operations, versie 1611, kunt u ook extra informatie configureren die wordt weergegeven in de rij onder de hoofdregel. 

**Klantenkaart**: De klantenkaart bevat gegevens over de klant die momenteel is gekoppeld aan de transactie. De klantenkaart kan worden geconfigureerd om extra informatie weer te geven of te verbergen. 

**Tabblad**: Het tabblad kan worden geplaatst op de schermindeling en andere besturingselementen zoals het toetsenblok, klantenkaart of knoppenrasters kunnen in het tabblad worden geplaatst. Het tabblad is een container waarmee gebruikers meer inhoud in het scherm kunnen passen. Het tabblad is alleen beschikbaar voor volledige indelingen. 

**Afbeelding**: het afbeeldingsbesturingselement kan worden gebruikt om het winkellogo of andere branding-afbeeldingen weer te geven op het transactiescherm. Het afbeeldingsbesturingselement is alleen beschikbaar voor volledige indelingen. 

**Aanbevolen producten**: Als dit is geconfigureerd voor de omgeving, laat het besturingselement voor aanbevolen producten productsuggesties zien die zijn gegenereerd door middel van machine learning. Het besturingselement voor productaanbevelingen is alleen beschikbaar voor volledige indelingen in Dynamics 365 for Operations, versie 1611. **Aangepast besturingselement **: Het aangepaste besturingselement fungeert als een tijdelijke aanduiding in de schermindeling. Gebruikers kunnen daarmee plaats reserveren voor hun eigen inhoud. Het aangepaste besturingselement is alleen beschikbaar voor volledige indelingen.

<a name="see-also"></a>Zie ook
--------

[De Retail POS-indelingsontwerper installeren](install-pos-layout-designer.md)




