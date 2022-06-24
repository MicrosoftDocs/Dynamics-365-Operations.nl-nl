---
title: Taakkaart configureren voor apparaten
description: In dit artikel worden de verschillende opties beschreven voor het configureren van het taakkaartapparaat.
author: johanhoffmann
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 0f42ad593f59f716fb6cb535d73654d3549ba00e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860720"
---
# <a name="configure-job-card-for-devices"></a>Taakkaart configureren voor apparaten

[!include [banner](../includes/banner.md)]

Het taakkaartapparaat wordt gebruikt door werkvloerwerknemers om hun dagelijkse werkzaamheden te registreren, bijvoorbeeld wanneer taken worden gestart, feedback over taken wordt geregistreerd, indirecte activiteiten worden geregistreerd en verzuim wordt gerapporteerd. Deze registraties vormen de basis voor het bijhouden van de voortgang en de kosten van productieorders, en voor het berekenen van de basis voor het salaris van de werknemers. In dit artikel worden de verschillende opties beschreven voor het configureren van taakkaartapparaten.

## <a name="enable-new-features-in-feature-management"></a>Nieuwe functies in Functiebeheer inschakelen

Enkele van de instellingen die in dit artikel worden beschreven, moeten op uw systeem zijn ingeschakeld voordat deze voor u beschikbaar zijn. Gebruik de pagina [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om een of meer van de volgende functies in te schakelen, indien vereist.

### <a name="generate-license-plate"></a>Nummerplaat maken

Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (op volgorde):

1. *Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)
1. *Het automatisch genereren van nummerplaatnummers inschakelen bij het gereedmelden in het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)

### <a name="print-label"></a>Label afdrukken

Als u deze functie beschikbaar wilt maken, schakelt u de volgende functies in [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (op volgorde):

1. *Nummerplaat voor gereedmelding toegevoegd aan het apparaat voor taakkaarten*<br>(Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)
1. *Label afdrukken vanaf apparaat voor taakkaart*<br>(Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht.)

### <a name="allow-locking-of-touch-screen"></a>Vergrendeling van aanraakscherm toestaan

Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Functie voor vergrendelen van taakkaartapparaat en taakkaartterminal zodat ze kunnen worden schoongemaakt* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="manage-your-device-configurations"></a>Uw apparaatconfiguraties beheren

Ga naar **Productiebeheer > Instellen > Productie-uitvoering > Taakkaart configureren voor apparaten** voor het instellen van de apparaatconfiguraties. De pagina **Taakkaart voor apparaten configureren** wordt geopend, waarin een lijst met bestaande configuraties wordt weergegeven. U kunt vanaf daar het volgende doen: 

- Selecteer de apparaatconfiguratie die in de linkerkolom staat om deze weer te geven en te bewerken.
- Selecteer **Nieuw** in het actievenster om een nieuwe apparaatconfiguratie aan de lijst toe te voegen. Voer een naam in het veld **Configuratie** in waarmee de nieuwe configuratie kan worden geïdentificeerd. De waarde die u hier invoert, moet uniek zijn onder alle hardwareconfiguraties en u kunt deze later niet bewerken.

Zie de volgende secties voor meer informatie over de instellingen voor het configureren van taakkaartapparaten.

## <a name="general-settings"></a>Algemene instellingen

Op het sneltabblad **Algemeen** kunt u de verschillende opties configureren die beschikbaar zijn voor de geselecteerde apparaatconfiguratie. De volgende instellingen zijn beschikbaar:

- **Hoeveelheid rapporteren bij uitklokken**: stel dit in op **Ja** om werknemers te vragen om bij het uitklokken feedback te rapporteren over taken die zijn uitgevoerd. Indien ingesteld op **Nee**, wordt dit niet aan werknemers gevraagd.
- **Werknemer vergrendelen**: wanneer deze optie is ingesteld op **Nee**, wordt elke werknemer onmiddellijk afgemeld nadat ze een registratie (zoals een nieuwe taak) hebben gemaakt, waarna het apparaat terugkeert naar de aanmeldingspagina. Als deze optie is ingesteld op **Ja**, blijft elke werknemer aangemeld bij het taakkaartapparaat. De werknemer kan echter nog steeds handmatig uitloggen om een andere werknemer toe te staan zich aan te melden terwijl de taakkaart wordt uitgevoerd onder hetzelfde systeemgebruikersaccount. Meer informatie over deze typen accounts vindt u in [Toegewezen gebruikers](#assigned-users).
- **Streepjescodescanner**: stel deze optie in op **Ja** om een optie op de taakkaart weer te geven waarmee werknemers het begin van een nieuwe taak kunnen registreren door een streepjescode te scannen.
- **De werkelijke registratietijd gebruiken**: stel dit in op **Ja** om de tijd in te stellen voor elke nieuwe registratie die gelijk is aan de exacte tijd waarop de registratie is ingediend door een werknemer. Stel in op **Nee** als u de aanmeldingstijd wilt gebruiken. U stelt dit meestal in op **Ja** als u de opties **Werknemer vergrendelen** en/of **Eén werknemer** hebt ingeschakeld, waarbij werknemers vaak blijven aangemeld gedurende langere perioden.
- **Eén werknemer**: stel deze optie in op **Ja** als slechts één werknemer het taakkaartapparaat gebruikt waarvoor deze configuratie actief is. Als deze optie is geselecteerd, wordt de optie **Werknemer vergrendelen** automatisch ingesteld op **Ja**. Bovendien verwijdert u met deze optie de vereiste (en de mogelijkheid) om zich aan te melden met behulp van een badge-id (of vergelijkbaar). In plaats daarvan meldt de werknemer zich aan bij Supply Chain Management met een systeemgebruikersaccount dat is gekoppeld aan een *werknemer met tijdregistratie* (uit de tabel *werknemers*) en dat op hetzelfde moment wordt aangemeld bij het taakkaartapparaat als die werknemer.  Meer informatie over deze typen accounts vindt u in [Toegewezen gebruikers](#assigned-users).
- **Werknemers persoonlijke filters laten instellen**: stel deze optie in op **Ja** als u wilt dat werknemers de taken kunnen filteren die op het apparaat worden getoond. De werknemer kan waarden wijzigen voor een van de drie filtercriteria: **Productie-eenheid**, **Resourcegroep** en **Resource**. Er worden alleen taken weergegeven die zijn gepland voor resources die overeenkomen met de geselecteerde filtercriteria op het apparaat. U kunt ook standaardwaarden toewijzen voor een of meer van deze criteria, en deze worden toegepast zelfs als deze optie niet is geselecteerd.
- **Vergrendelen van het touchscreen toestaan**: stel deze optie in op **Ja** om werknemers in staat te stellen het touchscreen van het taakkaartapparaat te vergrendelen zodat ze het kunnen schoonmaken. Als deze functie is ingeschakeld, wordt de knop **Scherm vergrendelen voor schoonmaken** toegevoegd aan de aanmeldpagina van het apparaat. Wanneer een werknemer deze knop selecteert, wordt het touchscreen tijdelijk vergrendeld voor onbedoelde invoer en wordt een afteltimer weergegeven. De werknemer kan nu het apparaat en het scherm veilig schoonmaken. Wanneer de timer is afgelopen, wordt het touchscreen automatisch weer automatisch ontgrendeld.
- **Duur schermvergrendeling**: wanneer de optie **Vergrendelen van het touchscreen toestaan** is ingeschakeld, gebruikt u deze optie om het aantal seconden op te geven dat het touchscreen moet worden vergrendeld voor schoonmaken. De duur moet tussen 5 en 120 seconden liggen.
- **Productie-eenheid**: selecteer een productie-eenheid die moet worden toegepast als standaard filtercriterium voor de lijst met taken die voor elke werknemer wordt weergegeven. Alleen taken die zijn gepland voor resources die zijn gegroepeerd onder de geselecteerde productie-eenheid, worden eerst weergegeven door het apparaat. Als **Werknemers persoonlijke filters laten instellen** is ingeschakeld, kunnen werknemers deze waarde bewerken, anders wordt dit filter altijd toegepast wanneer de apparaatconfiguratie actief is.
- **Resourcegroep**: selecteer een resourcegroep die moet worden toegepast als standaard filtercriterium voor de lijst met taken die voor elke werknemer wordt weergegeven. Alleen taken die zijn gepland voor resources die zijn gegroepeerd onder de geselecteerde resourcegroep, worden eerst weergegeven door het apparaat. Als **Werknemers persoonlijke filters laten instellen** is ingeschakeld, kunnen werknemers deze waarde bewerken, anders wordt dit filter altijd toegepast wanneer de apparaatconfiguratie actief is.
- **Resource**: selecteer een resource die moet worden toegepast als standaard filtercriterium voor de lijst met taken die voor elke werknemer wordt weergegeven. Alleen taken die zijn gepland voor voor de geselecteerde resource, worden eerst weergegeven door het apparaat. Als **Werknemers persoonlijke filters laten instellen** is ingeschakeld, kunnen werknemers deze waarde bewerken, anders wordt dit filter altijd toegepast wanneer de apparaatconfiguratie actief is.
- **Nummerplaat genereren**: stel deze optie in op **Ja** om voor elke gereedmelding op het taakkaartapparaat een nieuwe nummerplaat te genereren. Het nummerplaatnummer wordt gegenereerd op basis van een nummerreeks die is ingesteld op de **pagina Parameters voor magazijnbeheer**. Wanneer de instelling is ingesteld op **Nee**, moeten werknemers een bestaande nummerplaat opgeven bij het gereedmelden.
- **Label afdrukken**: stel deze optie in op **Ja** om een nummerplaatlabel af te drukken wanneer de werknemer het taakkaartapparaat gebruikt voor de gereedmelding. De configuratie van het label wordt ingesteld in de documentroutering, zoals wordt beschreven in de [Indeling van documentroutering voor nummerplaatlabels](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Toegewezen gebruikers

Gebruik het sneltabblad **Toegewezen gebruikers** om een of meer systeemgebruikers te koppelen aan de huidige apparaatconfiguratie. Aan elke systeemgebruiker kan slechts één configuratie van een taakapparaat worden toegewezen.

Bij het instellen van een apparaat meldt de IT-medewerker zich doorgaans aan bij Supply Chain Management met een systeemgebruikersaccount. Vervolgens geldt de configuratie van het taakapparaat die aan die systeemgebruiker is gekoppeld zolang de systeemgebruiker zich blijft aanmelden. Deze systeemgebruikersaccounts zijn doorgaans alleen toegankelijk via de pagina taakkaartapparaat en geen ander onderdeel van Supply Chain Management.

Nadat de systeemgebruiker is aangemeld en de configuratie van het taakapparaat is geladen, kunnen werknemers zich vervolgens aanmelden bij het taakkaartapparaat via hun *geregistreerde werknemeraccount* (bijvoorbeeld door een streepjescode op hun badge te scannen), zodat ze nieuwe taken kunnen starten en andere soorten registraties kunnen uitvoeren. Verschillende werknemers kunnen zich gedurende de dag aan- en afmelden, terwijl dezelfde apparaatconfiguratie van kracht blijft op het apparaat omdat de systeemgebruiker zich voor de dag aanmeldt bij Supply Chain Management.

Zoals eerder vermeld, melden werknemers zich bij het gebruik van een apparaatconfiguratie met de optie **Eén werknemer** gewoonlijk aan bij Supply Chain Management als een systeemgebruiker die is gekoppeld aan een eigen *werknemeraccount met tijdregistratie*, zodat ze de apparaatconfiguratie laden en zich tegelijkertijd aanmelden als werknemer op het taakkaartapparaat.

## <a name="additional-resources"></a>Aanvullende bronnen

[Gereedmelden vanaf het taakkaartapparaat](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]