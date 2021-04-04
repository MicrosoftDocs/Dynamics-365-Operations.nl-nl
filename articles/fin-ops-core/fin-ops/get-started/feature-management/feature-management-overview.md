---
title: Overzicht van functiebeheer
description: Dit onderwerp bevat een beschrijving van de functie Functiebeheer en de manier waarop u deze kunt gebruiken.
author: ChrisGarty
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 6226fc69048b724a96f3de516c26829fdf50e7a2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570916"
---
# <a name="feature-management-overview"></a>Overzicht van Functiebeheer

[!include [banner](../../includes/banner.md)]

Functies worden toegevoegd en bijgewerkt in elke release. De functie Functiebeheer biedt een werkgebied waarin u een lijst met functies kunt weergeven die in elke release zijn geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven.

## <a name="the-feature-management-workspace"></a>Het werkgebied Functiebeheer

U kunt het werkgebied **Functiebeheer** openen door de gewenste tegel te selecteren op het dashboard. Er wordt een pagina weergegeven met een lijst met functies voor alle releases die worden ondersteund door de functie Functiebeheer. In de loop van de tijd zal Microsoft de functie Functiebeheer verbeteren zodat deze meer functionaliteit bevat om u te helpen bij het beheren van functies.

De lijst met functies bevat de volgende informatie:

- **Functienaam**: een beschrijving van de functie die is toegevoegd.
- **Inschakelstatus**: een symbool geeft aan of een functie is ingeschakeld (vinkje), niet is ingeschakeld (leeg), ingepland is voor inschakeling (klok), verplicht is ingeschakeld (slot), aandacht vereist vóór inschakelen (waarschuwing) of niet kan worden ingeschakeld (X). De instelling die wordt weergegeven, wordt gebruikt voor alle rechtspersonen. Houd er rekening mee dat zelfs wanneer een functie is ingeschakeld, deze nog steeds aan de beveiliging moet voldoen. Daarom is de functie alleen beschikbaar voor gebruikers die toegang hebben tot de functie op basis van hun beveiligingsrol. Deze is ook alleen beschikbaar voor rechtspersonen waartoe de gebruiker toegang heeft.
- **Inschakeldatum**: de datum waarop de functie is ingeschakeld of gepland staat om te worden ingeschakeld.
- **Toegevoegde functie**: de datum waarop de functie aan uw omgeving is toegevoegd. Deze datum wordt automatisch ingevoerd wanneer u uw omgeving bijwerkt tijdens de maandelijkse releasecycli.
- **Module**: de module waarop de nieuwe functie van invloed is.

Wanneer u een functie selecteert, wordt meer informatie weergegeven in het detailvenster rechts van de lijst met functies. Boven aan het deelvenster ziet u de functienaam, de datum waarop het onderdeel is toegevoegd, de module waarvoor de functie geldt en een koppeling **Meer informatie**. Selecteer deze koppeling om de documentatie voor de functie weer te geven. Als er geen documentatie beschikbaar is, wordt u naar een tijdelijke pagina geleid. Het detailvenster bevat ook een veld **Opmerkingen** waarin u uw eigen opmerkingen over de functie kunt toevoegen.

Het werkgebied **Functiebeheer** bevat tevens diverse tabbladen, elk met een lijst met functies.

- **Nieuw**: de tabblad bevat alle functies die zijn toegevoegd sinds de laatste maandelijkse update. Als u maandelijkse updates hebt overgeslagen, worden op het tabblad alle nieuwe functies weergegeven die zijn toegevoegd sinds u voor het laatst hebt bijgewerkt. De nieuwste functies worden boven aan de lijst weergegeven. Het totale aantal nieuwe functies wordt ook weergegeven in een tegel boven aan de pagina.
- **Niet ingeschakeld**: op dit tabblad worden alle functies weergegeven die niet zijn ingeschakeld. De nieuwste functies worden boven aan de lijst weergegeven. Het totale aantal nieuwe functies dat niet is ingeschakeld, wordt ook weergegeven in een tegel boven aan de pagina.
- **Gepland**: dit tabblad toont alle functies die zijn gepland voor inschakeling op een toekomstige datum. De functies met de vroegste geplande datum worden boven aan de lijst weergegeven. Het totale aantal geplande nieuwe functies wordt ook weergegeven in een tegel boven aan de pagina.
- **Alle**: op dit tabblad worden alle functies weergegeven. De nieuwste functies worden boven aan de lijst weergegeven.

## <a name="turn-on-a-feature"></a>Een functie inschakelen

Als een functie niet is ingeschakeld, wordt een knop **Nu inschakelen** weergegeven in het detailvenster. U kunt deze knop gebruiken om de functie in te schakelen.

- Selecteer de functie die u wilt inschakelen en selecteer vervolgens **Nu inschakelen** in het detailvenster. De functie wordt ingeschakeld.

Sommige functies kunnen niet meer worden uitgeschakeld nadat deze zijn ingeschakeld. Als de functie die u wilt inschakelen niet kan worden uitgeschakeld, wordt een waarschuwing weergegeven. Op dat moment kunt u **Annuleren** selecteren om de bewerking te annuleren en de functie uitgeschakeld te laten. Als u echter de optie **Inschakelen** selecteert en de functie inschakelt, kunt u deze later niet meer uitschakelen.

In sommige functies wordt een bericht weergegeven met aanvullende informatie voordat u deze inschakelt. Deze functies worden aangeduid met een geel waarschuwingssymbool. U moet de aanvullende informatie zorgvuldig lezen om beter te begrijpen wat er gebeurt wanneer de functie is ingeschakeld. U kunt echter nog steeds selecteren **Inschakelen** selecteren om de functie aan te zetten.

In sommige functies wordt een bericht weergegeven dat de functie pas kan worden ingeschakeld nadat een actie is ondernomen. Deze functies worden aangeduid met een rood X-symbool. U moet de in de beschrijving beschreven acties uitvoeren voordat de functie wordt ingeschakeld. Als u een functie bijvoorbeeld pas kunt gebruiken als een configuratiesleutel is uitgeschakeld, moet u eerst de configuratiesleutel uitschakelen en vervolgens terugkeren naar functiebeheer om de functie in te schakelen.

Nadat een functie is ingeschakeld, wordt een bericht weergegeven onder de koppeling **Meer informatie** in het detailvenster. Dit bericht geeft aan dat de functie is ingeschakeld of geeft aan wanneer de functie in de toekomst wordt ingeschakeld. Dit wordt altijd weergegeven wanneer u de functie selecteert in de lijst met functies.

Functies die in de toekomst worden ingeschakeld, worden weergegeven op het tabblad **Gepland**. Deze functies worden ingeschakeld met een batchproces om middernacht op de opgegeven datum, op basis van de tijdzone die wordt aangegeven door de systeemdatum.

## <a name="reschedule-a-feature"></a>Een functie opnieuw plannen

Als een functie in de toekomst wordt ingeschakeld, wordt een knop **Plannen** weergegeven in het detailvenster. Met deze knop kunt u de waarde voor **Inschakeldatum** wijzigen in een andere datum.

1. Selecteer de geplande functie die u opnieuw wilt plannen en selecteer vervolgens **Plannen**.
2. Geef in het dialoogvenster dat verschijnt in het veld **Inschakeldatum** de nieuwe datum op waarop de functie moet worden ingeschakeld.
3. Selecteer **Inschakelen** om de functie opnieuw te plannen of **Uitschakelen** om de planning te annuleren.

## <a name="turn-off-a-feature"></a>Een functie uitschakelen

Als een functie al is ingeschakeld, wordt een knop **Uitschakelen** weergegeven in het detailvenster. U kunt deze knop gebruiken om de functie uit te schakelen. De knop **Uitschakelen** is niet beschikbaar als de functie niet kan worden uitgeschakeld nadat deze is ingeschakeld.

- Selecteer de functie die u wilt uitschakelen en selecteer vervolgens **Uitschakelen** in het detailvenster. De functie wordt uitgeschakeld en het veld **Inschakeldatum** wordt gewist.

Nadat een functie is uitgeschakeld, wordt een bericht weergegeven onder de koppeling **Meer informatie** in het detailvenster. In dit bericht wordt aangegeven dat de functie nog niet is ingeschakeld. Dit wordt altijd weergegeven wanneer u de functie selecteert in de lijst met functies. Functies die niet zijn ingeschakeld, worden weergegeven op het tabblad **Niet ingeschakeld**.

## <a name="features-that-must-be-turned-on"></a>Functies die moeten worden ingeschakeld

Soms wordt een kritieke functie geleverd die automatisch moet worden ingeschakeld wanneer u een update uitvoert. Deze functies worden automatisch ingeschakeld op de datum die is opgegeven in het veld **Inschakeldatum**. Voor deze functies wordt een bericht weergegeven onder de koppeling **Meer informatie** in het detailvenster. Dit bericht geeft aan dat de functie is ingeschakeld of geeft aan wanneer de functie in de toekomst wordt ingeschakeld. Dit wordt altijd weergegeven wanneer u de functie selecteert in de lijst met functies.

## <a name="enable-all-features"></a>Alle functies inschakelen

Standaard zijn alle functies die aan uw omgeving worden toegevoegd, uitgeschakeld. U kunt alle functies inschakelen door de knop **Alles inschakelen** te selecteren. 

Wanneer u **Alles inschakelen** selecteert, wordt een optie weergegeven waar u de volgende informatie moet opgeven:
- Een lijst met alle functies die moeten worden bevestigd voordat ze kunnen worden ingeschakeld. Als u de functies in de lijst wilt inschakelen, selecteert u **Ja** voor de knop **Functies inschakelen waarvoor bevestiging vereist is**.
- Er wordt een lijst weergegeven met alle functies die niet kunnen worden ingeschakeld. Deze functies worden niet ingeschakeld.

Alle functies die kunnen worden ingeschakeld, worden ingeschakeld. Als een functie al is gepland om in de toekomst te worden ingeschakeld, wordt de planning niet gewijzigd. 

## <a name="turn-on-all-features-automatically"></a>Alle functies automatisch inschakelen

Standaard zijn alle functies die aan uw omgeving worden toegevoegd, uitgeschakeld, tenzij het verplichte functies zijn. Als u alle nieuwe functies automatisch wilt inschakelen, kunt u de vervolgkeuzelijst onder de werkgebiedtitel gebruiken om te wijzigen wat er gebeurt wanneer er nieuwe functies worden toegevoegd.

- Selecteer `Enable new features automatically` om automatisch alle nieuwe functies in te schakelen wanneer deze aan uw omgeving worden toegevoegd.
- Selecteer `Do not enable new features automatically` om alle nieuwe functies standaard op uit te zetten wanneer deze aan uw omgeving worden toegevoegd.


Wanneer u alle functie automatisch inschakelt, worden alle functies ingeschakeld die zouden worden ingeschakeld wanneer u op de knop **Alles inschakelen** klikt. Hiermee worden geen functies ingeschakeld waarvoor bevestiging vereist is of functies die pas na een bepaalde actie kunnen worden ingeschakeld.

## <a name="check-for-updates"></a>Controleren op updates

Na elke update worden functies aan uw omgeving toegevoegd. U kunt echter handmatig controleren op updates door op de knop **Controleren op updates** te klikken. Elke functie die na de update aan het systeem is toegevoegd, wordt aan de lijst met functies toegevoegd. Als een flighted-functie bijvoorbeeld na een release is ingeschakeld, kunt u controleren op updates en wordt de functie aan uw lijst toegevoegd.

## <a name="assigning-roles"></a>Rollen toewijzen

Het werkgebied **Functiebeheer** kan worden geopend door systeembeheerders en door gebruikers die zijn toegewezen aan de rollen Functiebeheer of Functieweergave. Deze twee rollen zijn gemaakt ter ondersteuning van de functie Functiebeheer. Gebruikers met de rol Functiebeheer kunnen elke functie in- of uitschakelen. Zij kunnen ook het veld **Opmerkingen** voor de functie bijwerken. Gebruikers in de rol Functieweergave kunnen alleen het werkgebied **Functiebeheer** weergeven. Zij kunnen functies niet in- of uitschakelen.

De rol Functiebeheer en de rol Functieweergave hebben geen voorrang boven de bestaande beveiliging die een gebruiker heeft. Ze bepalen alleen of de gebruiker functies kan in- of uitschakelen. Zij bieden geen toegang tot de functies zelf.

## <a name="features-that-use-configuration-keys"></a>Functies die configuratiesleutels gebruiken

Als een functie een configuratiesleutel gebruikt, maar de configuratiesleutel niet is ingeschakeld, wordt de functie niet in de lijst met beschikbare functies in het werkgebied **Functiebeheer** weergegeven. Nadat u de configuratiesleutel hebt ingeschakeld, moet u de functielijst bijwerken met de menuoptie **Controleren op update**. De functie wordt vervolgens weergegeven in de lijst met functies.

Als u de configuratiesleutel uitschakelt, wordt de functie niet uit de lijst met functies verwijderd.

## <a name="data-entities"></a>Gegevensentiteiten

Met een gegevensentiteit met de naam **Functiebeheer** kunt u de instellingen voor functiebeheer vanuit de ene omgeving exporteren en vervolgens in een andere omgeving importeren. Deze entiteit werkt alleen bestaande functies bij. De bedrijfslogica in de entiteit helpt ook te garanderen dat dezelfde regels die worden gebruikt in het werkgebied **Functiebeheer** worden toegepast wanneer de import is uitgevoerd. U kunt een verplichte functie-instelling bijvoorbeeld niet overschrijven door tijdens het importeren de datum te verwijderen.

In de volgende voorbeelden wordt beschreven wat er gebeurt wanneer u de entiteit **Functiebeheer** gebruikt om gegevens te importeren.

- Als u de waarde van het veld **Ingeschakeld** wijzigt in **Ja**, wordt de functie ingeschakeld en wordt het veld **Inschakeldatum** ingesteld op de huidige datum.
- Als u de waarde van het veld **Ingeschakeld** wijzigt in **Nee** of het veld **EnableDate** leeg laat, wordt de functie uitgeschakeld en wordt het veld **Inschakeldatum** gewist. U kunt een verplichte functie of een functie die niet meer kan worden uitgeschakeld na het inschakelen, niet uitschakelen.
- Als u de waarde van het veld **EnableDate** in een toekomstige datum wijzigt, wordt de functie voor die datum gepland.
- Als u de waarde van het veld **Ingeschakeld** wijzigt in **Ja** en de waarde van het veld **EnableDate** op een toekomstige datum instelt, wordt de functie voor die datum gepland. 
- Als u de waarde van het veld **Ingeschakeld** wijzigt in **Nee**, maar ook de waarde van het veld **EnableDate** op een toekomstige datum instelt, wordt de functie voor die datum gepland.
- Als een functie is ingeschakeld en u een veld **EnableDate** toevoegt dat op een toekomstige datum is ingesteld, blijft de functie ingeschakeld. Als u de functie opnieuw wilt plannen, moet u het veld **Ingeschakeld** in **Nee** wijzigen.

## <a name="feature-management-and-flighting"></a>Functiebeheer en flighting

Met Functiebeheer kunt u de functies beheren die in elke release worden geleverd. Met flighting kunnen Microsoft-teams functies vrijgeven voor een beperkt aantal klanten, zodat de functies kunnen worden getest en gevalideerd zonder dat dit gevolgen heeft voor alle klanten. Met Functiebeheer wordt niet de flighting van alle functies bestuurd.

## <a name="new-features-are-optional-for-12-months"></a>Nieuwe functies zijn gedurende 12 maanden optioneel

Wanneer een nieuwe niet-essentiële functie wordt geïnstalleerd, is deze optioneel gedurende een periode van twaalf maanden. Dit geeft u en uw organisatie tijd om te plannen voor het moment dat u een functie opneemt en deze te testen voor uw dagelijkse activiteiten. Meer informatie over dit onderwerp vindt u in [Veelgestelde vragen over updates van service met één versie](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/one-version#what-about-new-features).

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Functiebeheer gebruiken om ISV-functies of aangepaste functies in te schakelen

Functiebeheer is momenteel niet beschikbaar voor functies van onafhankelijke softwareleveranciers (ISV's) en aangepaste functies. Microsoft voegt echter meer functionaliteit toe om het beheer van functies te verbeteren. Nadat deze verbeteringen zijn voltooid, maakt microsoft Functiebeheer beschikbaar voor alle functies en krijgt u instructies voor het bijwerken van uw functies om deze te gebruiken.

## <a name="frequently-asked-questions-faq"></a>Veelgestelde vragen (FAQ)

### <a name="when-are-features-added-removed-or-changed"></a>Wanneer worden functies toegevoegd, verwijderd of gewijzigd? 
Functies worden toegevoegd, verwijderd en gewijzigd via codewijzigingen. Omgevingen moeten worden bijgewerkt om deze wijzigingen te kunnen ontvangen.

### <a name="does-a-feature-become-mandatory-automatically"></a>Wordt een functie automatisch verplicht? 
Nee, het is niet automatisch dat een functie verplicht wordt. De productteams moeten een codewijziging aanbrengen.

### <a name="when-do-features-become-mandatory"></a>Wanneer worden functies verplicht? 
Het beleid is dat alle nieuwe functies voor een periode van twaalf maanden in aanmerking komen en dat er geen wijzigingsbeheer nodig is totdat u de functie inschakelt. De productteams kunnen kiezen of een functie verplicht moet worden gesteld nadat deze periode is geëindigd. 

### <a name="why-isnt-there-a-specific-mandatory-enabled-date"></a>Waarom is er geen specifieke verplichte datum voor inschakelen? 
De timing van updateversies is variabel, timing van omgevingsupdates is variabel en klanten kunnen ervoor kiezen sommige updates over te slaan. Hierdoor zijn bepaalde datums moeilijk te bepalen. 

### <a name="wheres-the-documentation-for-features-that-are-being-made-mandatory"></a>Waar is de documentatie voor functies die verplicht worden gesteld? 
Deze documentatie is afkomstig uit de toepassingsteams. Deze worden vaak vermeld in [Verwijderde of afgeschafte functies](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features). 

### <a name="is-there-an-in-product-notification-or-signal-that-a-feature-is-going-to-be-mandatory-enabled"></a>Is er een melding of signaal in het product dat een functie verplicht wordt ingeschakeld? 
Er bestaat op dit moment geen meldingsmechanisme voor het verplicht maken van een functie.

### <a name="do-features-ever-get-enabled-without-the-customer-knowing-about-it"></a>Worden functies ooit ingeschakeld zonder dat de klant dit weet? 
Ja, als functies geen functionele gevolgen hebben, kunnen ze standaard worden ingeschakeld.

### <a name="what-is-feature-flighting-and-how-does-it-relate-to-feature-management"></a>Wat is functie-flighting en hoe is dit gerelateerd aan functiebeheer? 
Functie-flights zijn real-time switches die door Microsoft worden bediend. Ze staan los van het besturingselement voor klanten dat door Functiebeheer wordt geleverd. 
- Functies met beperkte preview worden niet weergegeven in Functiebeheer totdat ze zijn ingeschakeld. In productie moet de klant instemmen met deelname aan een speciaal programma voordat dit wordt uitgevoerd.
- Openbare preview-functies en vrijgegeven (algemeen beschikbare) functies worden weergegeven in Functiebeheer, tenzij ze worden uitgeschakeld. Het uitschakelen van een functie wordt beschouwd als laatste redmiddel voor productteams als er een kritiek probleem wordt gevonden. Dit is normaal gesproken een bewerking per klant.

### <a name="do-features-ever-get-flighted-off-without-the-customer-knowing-about-it"></a>Worden functies ooit uitgeschakeld zonder dat de klant dit weet? 
Ja, als een functie van invloed is op de werking van een omgeving zonder functionele effecten, kunnen deze standaard worden ingeschakeld.

### <a name="how-can-feature-enablement-be-checked-in-code"></a>Hoe kan de inschakeling van een functie worden gecontroleerd in code?
Gebruik de **isFeatureEnabled** van de klasse **FeatureStateProvider**, waarbij deze een instantie van de functieklasse doorgeeft. Voorbeeld: 

```xpp
if (FeatureStateProvider::isFeatureEnabled(BatchContentionPreventionFeature::instance()))
```

### <a name="how-can-feature-enablement-be-checked-in-metadata"></a>Hoe kan de inschakeling van een functie worden gecontroleerd in metagegevens?
De eigenschap **FeatureClass** kan worden gebruikt om aan te geven dat sommige metagegevens aan een functie zijn gekoppeld. De klassenaam die voor de functie moet worden gebruikt, bijvoorbeeld **BatchContentionPreventionFeature**. Deze metagegevens zijn alleen zichtbaar in die functie. De eigenschap **FeatureClass** is beschikbaar in menu's, menu-items, opsommingswaarden en tabel- en weergavevelden.

### <a name="what-is-a-feature-class"></a>Wat is een functieklasse?
Functies in Functiebeheer zijn gedefinieerd als *functieklassen*. Met een functieklasse **worden IFeatureMetadata geïmplementeerd** en wordt het kenmerk functieklasse gebruikt om zichzelf te identificeren bij de werkruimte Functiebeheer. Er zijn talloze voorbeelden van functieklassen beschikbaar die kunnen worden gecontroleerd op inschakeling in code met behulp van de API **FeatureStateProvider** en in metagegevens met de eigenschap **FeatureClass**. Voorbeeld: 

```xpp
[ExportAttribute(identifierStr(Microsoft.Dynamics.ApplicationPlatform.FeatureExposure.IFeatureMetadata))]
internal final class BankCurrencyRevalGlobalEnableFeature implements IFeatureMetadata
```

### <a name="what-is-the-ifeaturelifecycle-implemented-by-some-feature-classes"></a>Wat is de IFeatureLifecycle die door sommige functieklassen is geïmplementeerd?
IFeatureLifecycle is een intern Microsoft-mechanisme voor het aangeven van de levenscyclus van de functie. Hierbij kan het om de volgende functies gaan:
- `PrivatePreview` - heeft een flight nodig om zichtbaar te zijn.
- `PublicPreview` - wordt standaard weergegeven, maar met een waarschuwing dat het bij de functie nog om een voorbeeld gaat.
- `Released` - volledig vrijgegeven.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]