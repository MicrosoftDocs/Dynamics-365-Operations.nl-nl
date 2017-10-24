---
title: Weergave-instellingen voor mobiel apparaat magazijn
description: In dit artikel wordt beschreven hoe u het uiterlijk van het scherm van een mobiel apparaat instelt en snelkoppelingen koppelt aan besturingselementen, zoals knoppen.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 799cd4a940813e39f8be6b4c127b9efabc88e909
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-mobile-device-display-settings"></a>Weergave-instellingen voor mobiel apparaat magazijn

[!include[banner](../includes/banner.md)]


In dit artikel wordt beschreven hoe u het uiterlijk van het scherm van een mobiel apparaat instelt en snelkoppelingen koppelt aan besturingselementen, zoals knoppen. 

Dit artikel geldt voor functies voor "geavanceerde magazijnen" in Magazijnbeheer. Mobiele apparaten kunnen worden gebruikt voor veel van de taken die de werknemers uitvoeren.

## <a name="specify-styles-and-map-keyboard-shortcuts"></a>Stijlen opgeven en toetsenbordsneltoetsen toewijzen
Als onderdeel van mobiele apparaatconfiguratie kunt u andere indelingen voor mobiele apparaten definiëren. Om dit te doen, moet u de naam van het Cascading Style Sheets (CSS)-bestand en het Active Server Page Extension (ASPX)-bestand kennen. Standaardbestanden worden geïnstalleerd als onderdeel van de magazijn-portal voor mobiele apparaten. Als u de bestandsnamen niet kent, moet u uw systeembeheerder om hulp vragen. U kunt een nieuwe stijl definiëren op de pagina **Weergave-instellingen mobiel apparaat**:

-    Voer in het veld **CSS-bestand** de naam van uw CSS-bestand in. Neem de bestandsextensie .ccc op.
-   Geef in het veld **Weergave van instellingen voor mobiel apparaat** het ASPX-bestand op. Voeg de bestandsnaamextensie .aspx **niet** toe.

De CSS- en ASPX-bestanden moeten in zich in een specifieke map bevinden, zodat de Internet Information Services (IIS)-toepassing ze kan laden. Het kan handig zijn om verschillende CSS-bestanden te definiëren als u mobiele apparaatfunctionaliteit in verschillende browsers of op verschillende typen hardware uitvoert die andere indelingsbesturing vereisen. De eenvoudige instellingen zoals de achtergrondkleur, het lettertype en de tekengrootte voor tekst, en breedte en de werking van knoppen, kunnen eenvoudig worden gecontroleerd met ander gebruik van CSS-bestanden. Het ASPX-bestand wordt gebruikt om de mobiele site weer te geven op de ASP.NET-toepassing op de server. Het bestand beheert hoe de algehele structuur van HTML wordt opgemaakt. Het is een goed idee om deze functionaliteit aan te passen als u ernstige structurele problemen hebt met HTML en JavaScript, en deze code moet wijzigen voor uw specifieke apparaten. De HTML-besturingselementen op pagina van het mobiele apparaat toe te wijzen aan sneltoetsen, wijst u op de pagina **Weergave-instellingen mobiel apparaat** in het veld **Toetsenbordsneltoets** de numerieke codes voor de toetsen toe. U kunt het menu **Codes voor sneltoetsen weergeven** op het mobiele apparaat gebruiken om de numerieke tekencodes te zoeken. Merk op dat de toewijzingen kunnen verschillen, afhankelijk van de hardware die wordt gebruikt. U moet de volgende syntax gebruiken om de koppeling te creëren:

&lt;naam besturingselement&gt;(&lt;naam toets&gt;)=&lt;code toets&gt;;

Hier is een uitleg van de onderdelen van de syntaxis:

-   **&lt;naam besturingselement&gt;** - De naam van het besturingselement, bijvoorbeeld een knop, die in HTML wordt gerenderd.
-   **(&lt;naam toets&gt;)** – De naam van de toets waarvoor u de snelkoppeling maakt.
-   **&lt;Code toets&gt;** – De numerieke tekencode voor de toets die als sneltoets moet worden gebruikt.

Dit is een voorbeeld:

Annuleren(Esc)=27; Volledig(F2)=113

Op alle pagina's die een knop **Annuleren** hebben, heeft de knop deze tekst:

**(Esc) Annuleren**

Druk op de toets Esc op het toetsenbord om de knop **Annuleren** te activeren. Als u de instellingen voor stijl en toetsenbordsneltoetsen wilt toepassen op een specifiek apparaat, moet u een toewijzing maken in het veld **Criteria**. U moet een normale .NET-expressie gebruiken om de toewijzing te maken en de expressie moet uit drie gedeelten bestaan die worden gescheiden door een verticale streep (|), zoals hier weergegeven:

Request.UserHostAddress=&lt;hostadres gebruiker&gt;|HostName=&lt;hostnaam gebruiker&gt;|Request.UserAgent=&lt;agent gebruiker&gt;

Hier is een uitleg van de onderdelen van de expressie:

-   **&lt;hostadres gebruiker&gt;** – Een normale .NET-expressie die overeenkomt met het IP-adres van de aanvrager.
-   **&lt;hostnaam gebruiker&gt;** – Een normale .NET-expressie die overeenkomt met de netwerknaam van de aanvrager.
-   **&lt;agent gebruiker&gt;** – Een normale .NET-expressie die overeenkomt met de browser-id die de aanvrager gebruikt.

In het volgende voorbeeld is het gebruik van Internet Explorer 8 mogelijk:

Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0

U kunt het menu **Serverconfiguratie voor weergave-instellingen weergeven** op het mobiele apparaat gebruiken om de informatie over de instellingen te zoeken.

## <a name="define-text-colors-for-messages"></a>Tekstkleuren definiëren voor berichten
U kunt de pagina **Tekstkleuren voor mobiel apparaat** gebruiken om de diverse kleuren te bepalen die worden gebruikt in systeemberichten, zoals foutberichten. De tekstkleur kan bijvoorbeeld het doel of de ernst van het bericht aangeven. De volgende typen berichten worden weergegeven:

| Berichttype | Beschrijving                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Standaard      | Standaardberichten gebruiken de standaardkleurinstellingen voor alle berichten, zoals gedefinieerd door het CSS-bestand voor de Magazijn-portal voor mobiele apparaten.                                                   |
| Fout        | Foutberichten geven een probleem aan dat de gebruiker moet oplossen voordat hij of zij kan doorgaan.                                                                                             |
| Geslaagd      | Succesberichten bevestigen dat een actie is geslaagd.                                                                                                                                |
| Waarschuwing      | De waarschuwingsberichten brengen de werknemer op de hoogte dat er een probleem is, of dat er een probleem kan zijn als de werknemer zo doorgaat. De medewerker hoeft het probleem echter niet op te lossen om door te gaan. |

Om de kleur te selecteren, klikt u op **Kleur selecteren**, in het palet of typt u een hexadecimale kleurencode.

## <a name="define-the-date-format-to-use-on-mobile-devices"></a>Definieer de te gebruiken datumindeling op mobiele apparaten
U kunt de lijst met geaccepteerde datumindelingen uitbreiden voor elke installatie. Deze mogelijkheid kan bijvoorbeeld nuttig zijn als u een indeling wilt opgeven die het voor een werknemer gemakkelijker maakt datums in te voeren op een mobiel apparaat. De standaardindeling wordt bepaald door de standaardtaal voor de gebruiker, die in het veld op **Taal** de pagina **Gebruikersopties** wordt opgegeven. (Dezelfde pagina wordt ook gebruikt om een werknemer te koppelen aan een specifieke magazijnwerkgebruiker.) **Opmerking:** de magazijnportal voor mobiele apparaten maakt geen gebruik van de instelling van het veld **Datum-, tijd- en getalnotatie** op de pagina **Voorkeuren voor gebruikerstaal en regio**. Om een datumnotatie te wijzigen, moet u bekend zijn met normale expressies in het Microsoft .NET Framework. Zie voor meer informatie [Normale .NET Framework-expressies](http://go.microsoft.com/fwlink/?LinkId=391260). Als u datumnotaties wilt definiëren, bewerkt u het bestand Dates.ini-bestand dat u kunt vinden in Content\\Settings\Dates\\Dates.ini. op de server van de magazijnportal voor mobiele apparaten. Dit bestand gebruikt .NET normale expressies om de datumnotatie te bepalen. De normale expressie moet subexpressies omvatten die benoemde groepen vormen voor dag, maand en jaar (DDMMJJ), zoals getoond in het volgende voorbeeld:

^(?&lt;dag&gt;\\d{2})(?&lt;maand&gt;\\d{2})(?&lt;jaar&gt;\\d{2})$

Elke subexpressie vereist een tot twee cijfers voor de dag en de maand, en een tot vier cijfers voor het jaar. De volgende subexpressie definieert bijvoorbeeld een benoemde groep voor een jaar en vereist ten minste twee cijfers of maximaal vier cijfers:

(?&lt;jaar&gt;\\d{2,4})

U kunt meerdere expressie in hetzelfde bestand opgeven. Elke expressie moet op een aparte regel staan. De eerste expressie die wordt afgestemd, wordt gebruikt om de datum te parseren.

<a name="see-also"></a>Zie ook
--------

[Configuratie van mobiele apparaten voor magazijnwerk](configure-mobile-devices-warehouse.md)




