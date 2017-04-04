---
title: Schermindelingen voor POS configureren
description: Dit onderwerp biedt informatie over schermindelingen voor de Microsoft Dynamics 365 for Operations - punt van verkooppunten (POS) ervaringen Retail.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Schermindelingen voor POS configureren

Dit onderwerp biedt informatie over schermindelingen voor de Microsoft Dynamics 365 for Operations - punt van verkooppunten (POS) ervaringen Retail.

De Microsoft Dynamics 365 voor bewerkingen: Retail punt van verkooppunten (POS)-gebruikersinterface kan worden geconfigureerd met behulp van een combinatie van Weergaveprofielen en schermindelingen aan winkels, kassa's en/of gebruikers toegewezen.

## <a name="visual-profile"></a>Weergaveprofiel
Weergaveprofielen zijn toegewezen aan de kassa's en worden gebruikt om op te geven van de visuele elementen die specifieke kassa en gedeelde voor gebruikers zijn. Alle gebruikers die zich in het journaal heeft thema, kleuren en afbeeldingen. **Profielnummer** -het Profielnummer is de unieke id van het weergaveprofiel. **Beschrijving** : de omschrijving kunt u een omschrijvende naam opgeven die helpt bij het identificeren van het juiste profiel voor uw situatie. **Thema** -gebruikers kunnen kiezen tussen de toepassing licht of donker thema. Deze instellingen van invloed op de kleur voor tekst en achtergrond overal in de toepassing. **Kleur accent** -de accentkleur overal in het POS wordt gebruikt om te differentiëren of bepaalde visuele elementen zoals tegels, opdrachtknoppen of hyperlinks markeren. Deze elementen zijn meestal uitvoerbaar. **Kleur van koptekst** -de kleur van de koptekst kan de gebruiker voor het configureren van de kleur van de koptekst van de pagina om te voldoen aan de huisstijl behoeften van de detailhandelaar. Deze functie is alleen beschikbaar in Dynamics 365 voor bewerkingen versie 1611. **Aanmelding achtergrond** -gebruikers een achtergrondafbeelding voor het aanmeldingsscherm kunnen opgeven. De bestandsgrootte van achtergrondafbeeldingen moeten zo klein mogelijk, zoals opslaan en laden van grote bestanden een gevolgen voor de toepassing werking en prestaties hebben kunnen. **Achtergrond van de toepassing** -de POS kan ook een afbeelding als achtergrond wilt gebruiken in de applicatie in plaats van de kleur van het vaste thema. Net als bij de aanmelding achtergrond, wordt het aanbevolen de bestandsgrootte zo minimaal mogelijk te houden.

## <a name="screen-layouts"></a>Schermindelingen
Scherm indeling configuratie bepaalt de acties, inhoud en plaats van de UI-besturingselementen in de welkomstpagina van de POS-scherm en het scherm van de transactie. ** Welkom-scherm **-In de meeste gevallen is het Welkom-scherm de pagina die gebruikers zien wanneer ze zich eerst in het POS. Het Welkom-scherm kan bestaan uit een huisstijlafbeelding en knoppenrasters die toegang tot POS-bewerkingen bieden. Normaal gesproken worden bewerkingen die niet specifiek voor de huidige transactie zijn hier geplaatst. **transactie scherm** -scherm van de transactie is het hoofdscherm van POS voor de verwerking van verkooptransacties en orders. Het scherm van de transactie kan worden geconfigureerd met behulp van de ontwerper van schermindeling. **Standaardinstellingen voor begindatum scherm** -sommige detailhandelaren geven de voorkeur aan dat de kassamedewerker navigeren rechtstreeks naar het scherm van de transactie na hun aanmelding. De standaardinstelling voor begin scherm kan gebruikers deze optie instellen voor elke schermindeling.

### <a name="assignment"></a>Toewijzing

Schermindelingen kunnen worden toegewezen op het niveau van de winkel, kassa of gebruiker. De gebruikerstoewijzing van de heeft voorrang boven de kassa en opslaan van toewijzing en de toewijzing kassa overschrijvingen de toewijzing van de winkel. In een eenvoudige scenario waar alle gebruikers dezelfde indeling ongeacht de kassa of rol gebruiken, kan de schermindeling alleen in de winkel worden ingesteld. In gevallen waar bepaalde journalen of gebruikers speciale indelingen moeten, kunnen ze worden toegewezen op de juiste wijze.

### <a name="layout-sizes"></a>Indelingsgrootten

Deze functie is alleen van toepassing op Dynamics 365 voor bewerkingen versie 1611. Omdat in veel gevallen schermindelingen in meerdere formaten en oplossingen kunnen worden gebruikt, kunnen gebruikers hun indeling en inhoud configureren voor elk. De POS-toepassing wordt de grootte van het dichtstbijzijnde lay-out voor het apparaat automatisch gekozen op het moment van starten. Een schermindeling kan ook configuraties voor volledige en compacte apparaten bevatten. Deze configuratie kan een gebruiker moet worden toegewezen aan een enkele schermindeling die op verschillende maten en in formulier factoren in de winkel werkt. **Moderne POS - volledige** -volledige indelingen normaal gesproken moet worden gebruikt voor grotere weergegeven zoals pc-monitor of tabletten. Gebruikers kunnen kiezen welke gebruikersinterface-elementen wilt opnemen, bepalen de grootte en plaatsing en de gedetailleerde eigenschappen te configureren. Volledige indelingen ondersteunen configuraties met zowel Staand en Liggend. **Comprimeren van moderne POS -** -compacte indelingen normaal gesproken moet worden gebruikt voor telefoons of kleine tabletten. Ontwerpmogelijkheden zijn beperkt voor compacte apparaten. De kolommen en velden voor het ontvangst- en totalen, kunnen gebruikers configureren.

### <a name="screen-layout-designer"></a>Ontwerper van schermindeling

De grootte van elke indeling binnen een schermindeling moet worden geconfigureerd met behulp van de ontwerper van schermindeling. De ontwerper kan gebruikers opgeven en configureren van de elementen van de gebruikersinterface van het scherm van de transactie. De ontwerper van schermindeling gebruikt ClickOnce downloaden, installeren en starten van de meest recente versie van de toepassing telkens wanneer die de gebruiker toegang krijgt deze tot. Controleer Browservereisten voor het gebruik van ClickOnce — sommige browsers, zoals chroom, extensies vereist. **Numeriek toetsenblok** -het toetsenblok is de belangrijkste gebruikersinvoer in het scherm van de POS-transactie. Deze kan worden geconfigureerd voor het gehele toetsenblok die ideaal is voor drukgevoelige beeldschermen, of alleen het invoerveld, die kan worden gebruikt met een echt toetsenbord op het scherm weergeven. De numeriek toetsenblok-instellingen zijn beschikbaar in de volledige indeling alleen. In Dynamics 365 voor bewerkingen versie 1611 hebben compacte lay-outs altijd het volledige toetsenblok beschikbaar vanuit het scherm van de transactie. **Deelvenster totalen** - het deelvenster totalen kan worden geconfigureerd in een of twee kolommen worden weergegeven velden, zoals aantal, kortingsbedrag, subtotaal, toeslagen en btw-regel. In Dynamics 365 voor bewerkingen versie 1611, compacte indelingen alleen bieden ondersteuning voor een kolom één totalen. **Ontvangst** -** ** het deelvenster ontvangst bevat de verkoopregels, betalingsregels en leveringsinformatie voor de producten en services die worden verwerkt in het POS. Gebruikers kunnen kolommen, breedte en plaatsing opgeven. U kunt ook extra informatie die wordt weergegeven in de rij onder de regel van de hoofdtabel in compacte indelingen in Dynamics 365 voor bewerkingen versie 1611 configureren. **Klantenkaart** - kaart bevat gegevens over de klant die deel uitmaken van de klant dat momenteel is gekoppeld aan de transactie. De klantenkaart kan worden geconfigureerd voor extra informatie weergeven of verbergen. **Tabblad controle** - het besturingselement kan worden geplaatst op de schermindeling en andere besturingselementen zoals het toetsenblok, klantenkaart of knoppenrasters in het tabblad kunnen worden geplaatst. Het besturingselement is een container waarmee gebruikers meer inhoud in het scherm passen. Het besturingselement is alleen beschikbaar voor volledige-indelingen. ** Image **-besturingselement van de afbeelding kan worden gebruikt voor het logo of andere huisstijlafbeelding op het scherm van de transactie weergeven. Het besturingselement is alleen beschikbaar voor volledige-indelingen. **Aanbevolen producten** - als geconfigureerd voor het milieu, de aanbevolen producten control suggesties op basis van de computer leren wordt weergegeven. Het aanbevolen producten besturingselement is alleen beschikbaar voor volledige indelingen in Dynamics 365 voor bewerkingen versie 1611. ** Aangepast besturingselement **-het aangepaste besturingselement fungeert als een tijdelijke aanduiding in de schermindeling kan gebruikers ruimte gereserveerd voor aangepaste inhoud. Het aangepaste besturingselement is alleen beschikbaar voor volledige-indelingen.

<a name="see-also"></a>Zie ook
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


