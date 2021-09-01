---
title: Gevaarlijke stoffen instellen
description: In dit onderwerp wordt uitgelegd hoe u de gegevens instelt die nodig zijn om artikelen te classificeren als gevaarlijke stoffen. Wanneer u een verkooporder maakt die een artikel bevat dat is geclassificeerd als een gevaarlijk goed, genereert het systeem voor die verkooporder een documentatie voor gevaarlijke stoffen wanneer het artikel wordt verzonden.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: c360d6a0fd5ffb65d1ea50d50e1ea5de00c84abe72e83c72b9bc4d6826cb41d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712977"
---
# <a name="set-up-hazardous-materials"></a>Gevaarlijke stoffen instellen

[!include [banner](../includes/banner.md)]

Als u de functie voor gevaarlijke stoffen wilt gebruiken, moet u eerst de gegevens instellen die nodig zijn om artikelen te classificeren als gevaarlijke stoffen. Wanneer u vervolgens een verkooporder maakt die een artikel bevat dat is geclassificeerd als een gevaarlijk goed, genereert het systeem voor die verkooporder een documentatie voor gevaarlijke stoffen wanneer het artikel wordt verzonden.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>De functie voor gevaarlijke stoffen inschakelen voor uw systeem

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Productgegevensbeheer*
- **Functienaam:** *Productgegevens over gevaarlijke stoffen en vervoersdocumentatie*

## <a name="hazardous-material-regulations"></a>Voorschriften voor gevaarlijke stoffen

Als u de processen voor gevaarlijke stoffen wilt gebruiken, moet u eerst een regelgeving maken. Regelgevingen definiëren hoe de afgedrukte verzendtekst voor een artikel wordt gemaakt. Ze definiëren ook de bijbehorende leveringsmethoden.

Hier volgen enkele algemene regelgevingen:

- **ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg
- **CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen
- **IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)
- **IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen

Deze regelgevingen helpen bepalen welke informatie moet worden weergegeven wanneer u de verzendtekst voor een artikel afdrukt. U kunt net zoveel regelgevingen definiëren als nodig zijn.

> [!IMPORTANT]
> Het gebruik van de functionaliteit voor het instellen van informatiecodes met betrekking tot gevaarlijke stoffen betekent niet dat uw bedrijf daardoor compatibel is met regelgevingen. Het is slechts een hulpmiddel bij het opstellen van processen voor uw bedrijf.

Gewoonlijk is er een regelgeving beschikbaar voor een specifieke transportmodus, zoals zeetransport, wegtransport of luchttransport. Dat betekent dat u elke regelgeving aan een leveringsmethode kunt koppelen. De leveringsmethode wordt gebruikt wanneer specifieke documenten worden afgedrukt in Magazijnbeheer. In Magazijnbeheer wordt elke verzending gekoppeld aan een vervoerder en een vervoerdersservice die zijn ingesteld in de module **Transport**. De leveringsmethode is gekoppeld aan de vervoerder en vervoerdersservice. Wanneer u een rapport uitvoert, wordt de leveringsmethode gebruikt om de verzendtekst te vinden die aan een vrijgegeven artikel is gekoppeld.

Deze instellingsgegevens zijn niet specifiek voor elke rechtspersoon (bedrijf). Dat betekent dat een gemeenschappelijke set gegevens over gevaarlijke stoffen kan worden gedeeld met alle rechtspersonen.

Voor elke regelgeving kunt u een lijst met materialen definiëren en deze gebruiken als een sjabloonlijst die is gekoppeld aan vrijgegeven artikelen. Voor elke regelgeving kunt u ook afdrukinstellingen definiëren. Met afdrukinstellingen kunt u bepalen hoe de verzendtekst voor een artikel wordt opgebouwd. De afdrukinstellingen worden gebruikt om de verzendtekst voor een vrijgegeven artikel samen te stellen.

Om regelgevingen voor gevaarlijke stoffen in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Regelgeving voor gevaarlijke stoffen**. Op de pagina **Regelgeving voor gevaarlijke stoffen** kunt u een willekeurig aantal regelgevingen maken en deze configureren met behulp van de velden die in de volgende subsecties worden beschreven.

### <a name="hazardous-material-regulation-header"></a>Kop van regelgeving voor gevaarlijke stoffen

Elke regelgeving heeft een code en een beschrijving. In de volgende tabel worden de velden beschreven die beschikbaar zijn in de kop.

| Veld | Beschrijving |
|---|---|
| Reguleringscode | Voer een code in om de regelgevingsregistratie voor gevaarlijke stoffen te identificeren. |
| Beschrijving | Voer een beschrijving in van de regelgeving voor gevaarlijke stoffen. |

### <a name="print-setup-fasttab"></a>Sneltabblad Afdrukinstellingen

Elke regelgeving kan een willekeurig aantal afdrukinstellingen hebben. U definieert de afdrukinstellingen op het sneltabblad **Afdrukinstellingen**. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor de afdrukinstellingen.

| Veld | Beschrijving |
|---|---|
| Volgorde | Geef de volgorde op waarin in de verzendtekst naar velden wordt verwezen. |
| Afdrukveld | Selecteer het veld dat u in de verzendtekst wilt opnemen. Niet alle velden voor gevaarlijke stoffen kunnen worden afgedrukt. Alleen de gemeenschappelijke velden die worden gebruikt om de verzendtekst in de diverse regelingen te definiëren, zijn beschikbaar. U moet het eerste afdrukveld definiëren als veldscheidingsteken en **Reeks** instellen op *0* (nul), zodat deze kan worden gebruikt als scheidingsteken tussen andere velden. Er is slechts één verwijzing naar het veldscheidingsteken vereist.<p>De volgende waarden zijn beschikbaar:</p><ul></li><li>**Veldscheidingsteken**: dit afdrukveld wordt gebruikt als veldscheidingsteken voor de tekst. Er is slechts één veldscheidingsteken in de reeks vereist. Normaal gesproken stelt u het veld **Reeks** voor dit afdrukveld in op *0* (nul). Het systeem zoekt naar een veldscheidingsteken en gebruikt het eerste veld dat in de lijst wordt gevonden. De tekstwaarde die in de tekenreeks wordt gebruikt, wordt uit het veld **Afdrukken na** gehaald.</li><li>**Identificatie**: met dit afdrukveld wordt de [identificatiecode en/of -beschrijving](#identification) in de afgedrukte tekst geplaatst.</li><li>**Klasse**: met dit afdrukveld wordt de [klassecode en/of -beschrijving](#classes) in de afgedrukte tekst geplaatst.</li><li>**Verdeling**: met dit afdrukveld wordt de [verdelingscode en/of -beschrijving](#divisions) in de afgedrukte tekst geplaatst.</li><li>**Verpakkingsgroep**: met dit afdrukveld wordt de [code en/of beschrijving van de verpakkingsgroep](#packing-group) in de afgedrukte tekst geplaatst.</li><li>**Tunnelcode en/of -beschrijving**: met dit afdrukveld wordt de [tunnelcode en/of -beschrijving](#tunnel) in de afgedrukte tekst geplaatst.</li><li>**Juiste verzendnaam**: met dit afdrukveld wordt de [juiste verzendnaam](hazmat-items.md#hazmat-description) in de afgedrukte tekst geplaatst.</li><li>**Technische naam**: met dit afdrukveld wordt de [technische naam en/of -beschrijving](#technical-name) in de afgedrukte tekst geplaatst.</li><li>**Transportcategorie**: met dit afdrukveld wordt de [code en/of beschrijving van de transportcategorie](#transport-category) in de afgedrukte tekst geplaatst.</li><li>**Bergruimte**: met dit afdrukveld wordt de [bergruimtecode en/of -beschrijving](#stowage) in de afgedrukte tekst geplaatst.</li><li>**Vaste tekst**: met dit afdrukveld wordt de tekst ingevoerd die is gedefinieerd in het veld **Vaste tekst** voor deze rij.</li><li>**Labelcode en/of -beschrijving**: met dit afdrukveld wordt de [labelcode en/of -beschrijving](#label) in de afgedrukte tekst geplaatst.</li><li>**Verpakking luchttransport**: met dit afdrukveld wordt de [code en/of beschrijving van de instructies voor verpakking voor luchttransport](#packing-instruction) in de afgedrukte tekst geplaatst.</li><li>**Beperkte hoeveelheid**: met dit afdrukveld wordt gecontroleerd of het artikel is gemarkeerd als een [artikel met beperkte hoeveelheid](hazmat-items.md#material-management) en als dat zo is, wordt de tekst ingevoerd die is gedefinieerd in het veld **Vaste tekst** voor deze rij.</li><li>**Verpakkingsbeschrijving**: met dit afdrukveld wordt de [verpakkingsbeschrijving](#packing-description) in de afgedrukte tekst geplaatst.</li></ul> |
| Afdrukken vóór | Voer de tekst in die moet worden afgedrukt vóór de inhoud die is gedefinieerd met de instelling van **Afdrukveld**. |
| Afdrukken na | Voer de tekst in die moet worden afgedrukt na de inhoud die is gedefinieerd met de instelling van **Afdrukveld**. |
| Afdrukken met vorige | Schakel dit selectievakje in als u wilt voorkomen dat het veldscheidingsteken tussen het vorige veld en dit veld wordt afgedrukt. Gebruik dit selectievakje voor afdrukvelden die optioneel zijn of zijn opgenomen in een ander afdrukveld. |
| Vaste tekst | Als u het veld **Afdrukveld** instelt op **Vaste tekst** of **Beperkte hoeveelheid**, voert u de tekst in die moet worden afgedrukt. |
| Opnemen in afdruk | Selecteer in het geselecteerde afdrukveld de waarden die voor deze rij moeten worden afgedrukt. U kunt de code, de beschrijving of beide afdrukken. |

### <a name="mode-of-delivery-fasttab"></a>Sneltabblad Leveringsmethode

De regelgeving is een gedeelde tabel en is niet specifiek voor elke rechtspersoon. Leveringsmethoden zijn echter wel specifiek voor een rechtspersoon. Wanneer u een leveringsmethode instelt, moet u dus de relatie tussen de regelgeving, rechtspersoon en leveringsmethode selecteren.

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Leveringsmethode**.

| Veld | Beschrijving |
|---|---|
| Bedrijf | Selecteer een rechtspersoon die u aan deze regelgeving wilt koppelen. |
| Leveringsmethode | Selecteer op basis van de geselecteerde rechtspersoon de leveringsmethode die aan de regelgeving moet worden gekoppeld. |

### <a name="country-fasttab"></a>Sneltabblad Land

Voor referentiedoeleinden kunt u de landen of regio's weergeven waarvoor de regelgeving relevant is. Wanneer verzendingsrapporten worden uitgevoerd, wordt echter alleen de leveringsmethode gebruikt om de regelgeving te bepalen. Wanneer u een magazijnverzending controleert, is er geen directe koppeling met de leveringsmethode. De zending kan worden gekoppeld aan een vervoerder en vervoerdersservice. Wanneer u een vervoerdersservice definieert, moet u deze koppelen aan een leveringsmethode. Deze relatie wordt gebruikt in verzendingsrapporten, zoals de vrachtbrief, om de verzendtekst voor een artikel te zoeken.

In de volgende tabel wordt het veld beschreven dat beschikbaar zijn op het sneltabblad **Land**.

| Veld | Beschrijving |
|---|---|
| Land/regio | Selecteer het land dat of de regio die u aan de regelgeving wilt koppelen. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materiaalcodes

Met materiaalcodes geeft u instellingen op die zijn gerelateerd aan een specifiek gevaarlijk bestanddeel dat mogelijk voorkomt in een vrijgegeven product. Elke materiaalcode behoort tot een specifieke regelgeving voor gevaarlijke stoffen en de definitie ervan moet aan die regelgeving voldoen. Wanneer u een materiaalcode met behulp van het veld **Materiaalcode** toepast op een vrijgegeven product, worden alle instellingen voor gevaarlijke stoffen van de materiaalcode automatisch op dat product toegepast. Daardoor is het proces van het instellen van vrijgegeven producten sneller en minder foutgevoelig.

Voer de volgende stappen uit om de definities van gevaarlijke stoffen te beheren.

1. Ga naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Regelgeving voor gevaarlijke stoffen**.
2. Selecteer de regelgeving waarvoor een definitie voor gevaarlijke stoffen wilt instellen.
3. Ga in het actievenster naar het tabblad **Instellingen** en selecteer **Gevaarlijke stoffen**.
4. Voer in het veld **Materiaalcode** een materiaalcode in voor de definitie van de gevaarlijke stof. U selecteert deze waarde wanneer u de materiaalcode toepast op een vrijgegeven product.

    Het veld **Regelgevingscode** is alleen-lezen en toont de regelgeving die u in stap 2 hebt geselecteerd.

5. Gebruik de overige velden op deze pagina om elke gevaarlijke stof te maken en in te stellen die van toepassing is op de geselecteerde regelgeving. De beschikbare velden zijn een subset van de velden voor de gevaarlijke stof die beschikbaar zijn voor afzonderlijke vrijgegeven producten. Meer informatie vindt u in [Gevaarlijke stoffen in producten, orders, zendingen en ladingen](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Classificatiegroepen voor gevaarlijke stoffen

Elke classificatiegroep voor gevaarlijke stoffen bepaalt een groep veldwaarden die een sjabloon vormen. U kunt deze sjabloon later gebruiken wanneer u informatie over gevaarlijke stoffen instelt voor een vrijgegeven artikel.

Wanneer u de code voor een classificatiegroep voor gevaarlijke stoffen toewijst aan een vrijgegeven artikel, worden de gegevens die aan die classificatiegroep zijn gekoppeld, gekopieerd naar de desbetreffende velden van het artikel. Dat betekent dat u de instellingsprocessen kunt vereenvoudigen door een set gerelateerde veldwaarden in te stellen die u vaak samen gebruikt.

Deze instellingsgegevens zijn niet specifiek voor elke rechtspersoon. Dat betekent dat een gemeenschappelijke set gegevens over gevaarlijke stoffen kan worden gedeeld met alle rechtspersonen.

Om classificatiegroepen voor gevaarlijke stoffen in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Classificatiegroep voor gevaarlijke stoffen**. Op de pagina **Classificatiegroep voor gevaarlijke stoffen** kunt u een willekeurig aantal groepen maken en deze configureren met behulp van de velden die in de volgende tabel worden beschreven.

| Veld | Beschrijving |
|---|---|
| Groepscode | Voer een code in om de groep te identificeren. |
| Beschrijving | Voer een omschrijving in van de groep. |
| Klassecode | Koppel een gevaarlijke stof [klassecode](#classes) aan de groep. |
| Divisiecode | Koppel een gevaarlijke stof [verdelingscode](#divisions) aan de groep. |
| Code verpakkingsgroep | Koppel de [code van een verpakkingsgroep](#packing-group) aan de groep. |
| Categoriecode transport | Koppel de [code van een transportcategorie](#transport-category) aan de groep. |
| Factor | Voer de vermenigvuldiger voor gevaarlijke stoffen in die van toepassing is op de geselecteerde klasse en verdeling voor gevaarlijke stoffen overeenkomstig de toepasselijke regelgeving. Deze vermenigvuldiger wordt gebruikt als onderdeel van de formule waarmee het totale aantal *punten voor gevaarlijke stoffen* wordt berekend die in een lading of zending zijn opgenomen. Meer informatie over punten voor gevaarlijke stoffen en deze vermenigvuldiger vindt u in [sneltabblad Materiaalbeheer](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Klassen voor gevaarlijke stoffen

Een klasse voor gevaarlijke stoffen wordt meestal toegewezen aan de lijst met klassen die is opgegeven in de regelgeving waaraan u conformeert. Zo is geeft "klasse 3" in de Amerikaanse CFR 49 ontvlambaar en brandbare vloeistoffen aan. U kunt de klassen instellen die relevant zijn voor de materialen die u moet classificeren.

Elke klasse wordt toegewezen aan een materiaalinstelling in de lijst met materialen die aan de regelgeving is gerelateerd. U wijst aan elk vrijgegeven artikel een klasse toe om de gevaarlijke aard van een product te beschrijven.

Deze instellingsgegevens zijn niet specifiek voor elke rechtspersoon. Dat betekent dat een gemeenschappelijke set gegevens over gevaarlijke stoffen kan worden gedeeld met alle rechtspersonen.

Klassen voor gevaarlijke stoffen werken op de volgende manier samen met verdelingen, groepen en compatibiliteitsgroepen:

- Wanneer u een klasse voor gevaarlijke stoffen toewijst aan een vrijgegeven artikel, moet u ook een [verdeling voor gevaarlijke stoffen](#divisions) toewijzen.
- U kunt klassen voor gevaarlijke stoffen gebruiken in combinatie met [classificatiegroepen voor gevaarlijke stoffen](#classification-groups) om een sjabloon met codes voor het instellen van artikelen in te stellen.
- U kunt [compatibiliteitsgroepen voor gevaarlijke stoffen](#compatibility-groups) gebruiken om vast te stellen welke klassen en verdelingen voor gevaarlijke stoffen samen kunnen worden verzonden.

Om klassen voor gevaarlijke stoffen in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Klasse voor gevaarlijke stoffen**. Op de pagina **Klasse voor gevaarlijke stoffen** kunt u een willekeurig aantal klassen maken en deze configureren met behulp van de velden die in de volgende tabel worden beschreven.

| Veld | Beschrijving |
|---|---|
| Klassecode | Voer een code in om deze klasse te identificeren. U kunt deze code voor het artikel definiëren. Deze wordt vervolgens gebruikt in opzoeklijsten wanneer u een klasse van gevaarlijk stoffen toewijst aan een vrijgegeven artikel. |
| Beschrijving | Voer een beschrijving van de klasse in. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Verdelingen voor gevaarlijke stoffen

Een verdeling voor gevaarlijke stoffen is een subset van een klasse voor gevaarlijke stoffen. U moet zowel een verdeling als een klasse toewijzen aan elk product dat gevaarlijke stoffen bevat.

Voor klassen die geen verdelingen hebben, maakt u een verdeling waarin de code *0* is. Bijvoorbeeld, in de IATA-regelgeving hebben radioactieve stoffen uit klasse 7 geen onderverdelingen. In dit geval maakt u een verdeling *0* die u aan een vrijgegeven product kunt koppelen wanneer u de klasse toewijst.

Deze instellingsgegevens zijn niet specifiek voor elke rechtspersoon. Dat betekent dat een gemeenschappelijke set gegevens over gevaarlijke stoffen kan worden gedeeld met alle rechtspersonen.

Verdelingen voor gevaarlijke stoffen werken op de volgende manieren samen met klassen, groepen en compatibiliteitsgroepen:

- Wanneer u een verdeling voor gevaarlijke stoffen toewijst aan een vrijgegeven artikel, moet u ook een [klasse voor gevaarlijke stoffen](#classes) toewijzen.
- U kunt verdelingen voor gevaarlijke stoffen gebruiken in combinatie met [classificatiegroepen voor gevaarlijke stoffen](#classification-groups) om een sjabloon met codes voor het instellen van artikelen in te stellen.
- U kunt [compatibiliteitsgroepen voor gevaarlijke stoffen](#compatibility-groups) gebruiken om vast te stellen welke klassen en verdelingen voor gevaarlijke stoffen samen kunnen worden verzonden.

Om verdelingen voor gevaarlijke stoffen in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoerdocumentatie gevaarlijke stoffen \> Verdeling voor gevaarlijke stoffen**. Op de pagina **Verdeling voor gevaarlijke stoffen** kunt u een willekeurig aantal verdelingen maken en deze configureren met behulp van de velden die in de volgende tabel worden beschreven.

| Veld | Beschrijving |
|---|---|
| Afdeling | Voer een code in om te gebruiken als referentienummer voor de verdeling. |
| Beschrijving | Voer een beschrijving in voor de verdeling. |
| Klasse | Zoek de klasse op waartoe de verdeling behoort en wijs deze toe. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Compatibiliteitsgroepen voor gevaarlijke stoffen

Met compatibiliteitsgroepen voor gevaarlijke stoffen kan worden vastgesteld welke klassen en verdelingen voor gevaarlijke stoffen samen kunnen worden verzonden. Wanneer operators magazijnladingen of zendingen maken, kunnen ze een compatibiliteitscontrole uitvoeren waarbij een waarschuwing wordt gegeven als de lading of zending artikelen bevat die niet allemaal tot dezelfde compatibiliteitsgroep behoren.

Deze instellingsgegevens zijn niet specifiek voor elke rechtspersoon. Dat betekent dat een gemeenschappelijke set gegevens over gevaarlijke stoffen kan worden gedeeld met alle rechtspersonen.

Om compatibiliteitsgroepen voor gevaarlijke stoffen in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Compatibiliteitsgroep voor gevaarlijke stoffen**. Op de pagina **Compatibiliteitsgroep voor gevaarlijke stoffen** kunt u een willekeurig aantal compatibiliteitsgroepen maken en deze configureren met behulp van de velden die in de volgende subsecties worden beschreven.

### <a name="hazardous-material-compatibility-group-header"></a>Kop van compatibiliteitsgroep voor gevaarlijke stoffen

Elke compatibiliteitsgroep heeft een code en een beschrijving. In de volgende tabel worden de velden beschreven die beschikbaar zijn in de kop.

| Veld | Beschrijving |
|---|---|
| Compatibiliteitsgroep | Voer een code in om de compatibiliteitsgroep te identificeren |
| Beschrijving | Voer een beschrijving van de compatibiliteitsgroep in. |

### <a name="compatibility-group-details"></a>Details van compatibiliteitsgroep

Elke compatibiliteitsgroep definieert een lijst met klassen en verdelingen van gevaarlijke stoffen die samen kunnen worden vervoerd.

| Veld | Beschrijving |
|---|---|
| Klasse | Selecteer een klasse voor gevaarlijke stoffen die compatibel is met alle andere klassen in de groep. |
| Afdeling | Selecteer een verdeling voor gevaarlijke stoffen die tot de geselecteerde klasse behoort. |

## <a name="hazardous-material-specification-values"></a>Specificatiewaarden voor gevaarlijke stof

Microsoft Dynamics 365 Supply Chain Management biedt verschillende typen specificaties voor gevaarlijke stoffen. Voor elk type moet u een gecentraliseerde set waarden instellen voor elk relevant veld. Gebruikers kunnen vervolgens uit die waarden kiezen wanneer ze definities voor gevaarlijke stoffen of vrijgegeven producten configureren. Supply Chain Management biedt een verzameling pagina's waar u de waarden kunt instellen. Elke pagina is toegewezen aan één type specificatie. Zie de volgende subsecties voor een beschrijving van elke beschikbare specificatie en informatie over het instellen van de beschikbare waarden daarvoor.

Een voorbeeld van een specificatie voor een gevaarlijke stof is de _bergruimtecode_, waarmee wordt aangegeven hoe een bepaald materiaal tijdens het transport kan worden opgeslagen. Door de informatie in deze sectie te gebruiken, stelt u een centrale verzameling bergruimtecodes in. Deze verzameling wordt vervolgens aan gebruikers weergegeven in een vervolgkeuzelijst wanneer ze de bergruimtecode voor een vrijgegeven product instellen.

Deze waarden voor specificaties van gevaarlijke stoffen zijn niet specifiek voor elke rechtspersoon. Dat betekent dat u een set algemene waarden kunt hebben die worden gedeeld met al uw rechtspersonen.

U gebruikt [materiaalcodes](#hazmat-codes) om algemene verzamelingen instellingen te configureren voor elke specificatie zoals die van toepassing is op een bepaalde regelgeving. Vervolgens kunt u de juiste code toepassen op elk vrijgegeven product waar dat nodig is. Voor informatie over het toepassen van een code van een gevaarlijke stof op een specifiek vrijgegeven product en het configureren van afzonderlijke instellingen van dat product voor elke specificatie die hier wordt beschreven, raadpleegt u [Gevaarlijke stoffen in producten, orders, zendingen en ladingen](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Reactie op noodgevallen voor gevaarlijk materiaal

De specificatie *Reactie op noodgevallen voor gevaarlijke stoffen* geeft aan wat er moet gebeuren als er iets mis gaat terwijl een product dat een bepaalde gevaarlijke stof bevat, wordt vervoerd.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Reactie op noodgevallen voor gevaarlijke stoffen**. Op de pagina **Reactie op noodgevallen voor gevaarlijke stoffen** kunt u een willekeurig aantal waarden maken en elke waarde configureren met een classificatiecode en een korte beschrijving.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Identificatie van gevaarlijk materiaal

De specificatie *Identificatie van gevaarlijke stof* identificeert de klasse of de aard van een gevaarlijke stof. De waarde is doorgaans een code die is gebaseerd op een UN-standaard (Verenigde Naties). Elke klasse wordt aangeduid met een code en een beschrijving en kan beperkingen instellen voor transportmethoden. Als u bijvoorbeeld een ontvlambaar artikel of materiaal wilt identificeren, maakt u een klasse voor een gevaarlijke stof met code *FL* en omschrijving *Flammable*. U geeft ook op dat de klasse niet door de lucht moet worden vervoerd.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Identificatie van gevaarlijke stoffen**. Op de pagina **Identificatie van gevaarlijke stoffen** kunt u een willekeurig aantal waarden maken en deze configureren met behulp van de velden die in de volgende tabel worden beschreven.

| Veld | Beschrijving |
|---|---|
| Id | Voer een code in die u wilt gebruiken als referentienummer waarmee deze klasse van gevaarlijke stoffen wordt geïdentificeerd. |
| Beschrijving | Voer een beschrijving van deze klasse in. |
| Beperken van luchttransport | Schakel dit selectievakje in om aan te geven dat deze klasse van gevaarlijke stoffen niet door de lucht mag worden vervoerd. |
| Beperken van zeetransport | Schakel dit selectievakje in om aan te geven dat deze klasse van gevaarlijke stoffen niet over zee mag worden vervoerd. |

### <a name="hazardous-material-label"></a><a name="label"></a>Label gevaarlijk materiaal

De specificatie *Label voor gevaarlijke stoffen* geeft het label voor gevaarlijke stoffen aan dat op relevante vrijgegeven producten moet worden toegepast. Op de labels zelf staat beschreven hoe het product moet worden behandeld. Zo zijn er bijvoorbeeld producten die een giftig gas bevatten. In dit geval stelt u een labelcode in voor het label voor giftige gassen. U bouwt ook uw bedrijfsproces op zodat deze waarde wordt opgezocht wanneer u producten levert.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Label voor gevaarlijke stoffen**. Op de pagina **Label voor gevaarlijke stoffen** kunt u een willekeurig aantal labels maken en elk label configureren met een identificatiecode en een korte beschrijving.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Verpakkingsomschrijvingen voor gevaarlijk materiaal

De specificatie *Beschrijvingen voor verpakking van gevaarlijke stoffen* geeft aan hoe een gevaarlijk artikel moet worden verpakt. Het kan bijvoorbeeld nodig zijn om het te verpakken in een bepaald type stalen ton of een andere speciale verpakking.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Beschrijvingen voor verpakking van gevaarlijke stoffen**. Op de pagina **Beschrijvingen voor verpakking van gevaarlijke stoffen** kunt u een willekeurig aantal verpakkingsbeschrijvingen maken en elke beschrijving configureren met een identificatiecode en een korte beschrijving.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Verpakkingsgroep voor gevaarlijk materiaal

De specificatie *Verpakkingsgroep voor gevaarlijke stoffen* identificeert de verpakkingsgroep voor een gevaarlijk artikel. Met de verpakkingsgroep kunt u een code en een omschrijving definiëren om aan te geven hoe gevaarlijke materiaal artikelen moeten worden verpakt tijdens het transport of de verzending. De verpakkingsgroep wordt aan het artikel toegewezen op de pagina **Artikel met gevaarlijke stoffen**.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Verpakkingsgroep voor gevaarlijke stoffen**. Op de pagina **Verpakkingsgroep voor gevaarlijke stoffen** kunt u een willekeurig aantal verpakkingsgroepen maken en elke beschrijving configureren met een identificatiecode en een korte beschrijving.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Verpakkingsinstructie voor gevaarlijk materiaal

De specificatie *Verpakkingsinstructie voor gevaarlijke stoffen* definieert verpakkingsinstructies die moeten worden gevolgd wanneer een bepaald gevaarlijk artikel wordt voorbereid voor transport door de lucht.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie voor gevaarlijke stoffen \> Verpakkingsinstructie voor gevaarlijke stoffen**. Op de pagina **Verpakkingsinstructie voor gevaarlijke stoffen** kunt u een willekeurig aantal verpakkingsinstructie-id's maken en deze configureren met een identificatiecode en een korte beschrijving.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Opslagruimte gevaarlijk materiaal

De specificatie *Bergruimte voor gevaarlijke stoffen* geeft aan hoe een product op een schip moet worden opgeborgen wanneer het over zee wordt vervoerd.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Bergruimte voor gevaarlijke stoffen**. Op de pagina **Bergruimte voor gevaarlijke stoffen** kunt u een willekeurig aantal bergruimte-id's maken en deze configureren met een identificatiecode en een korte beschrijving.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Transportcategorie gevaarlijk materiaal

De specificatie *Transportcategorie voor gevaarlijke stoffen* wordt meestal gebruikt om vergelijkbare gevaarlijke producten op rapporten te groeperen. U kunt transportcategorieën bijvoorbeeld gebruiken in het rapport **Zendingsoverzicht** dat u kunt afdrukken vanuit de magazijnverzendingsrecord.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Transportcategorie voor gevaarlijke stoffen**. Op de pagina **Transportcategorie voor gevaarlijke stoffen** kunt u een willekeurig aantal transportcategorieën maken en elke categorie configureren met een weergavenaam en een korte beschrijving.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Technische naam van gevaarlijk materiaal

De specificatie *Technische naam voor gevaarlijke stoffen* kan worden gebruikt om een veelgebruikte of interne bedrijfsnaam in te stellen om elk materiaal te beschrijven.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Technische naam voor gevaarlijke stoffen**. Op de pagina **Technische naam voor gevaarlijke stoffen** kunt u een willekeurig aantal technische namen maken en elke naam configureren met een weergavenaam en een korte beschrijving.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Tunnel gevaarlijk materiaal

De specificatie *Tunnel voor gevaarlijke materiaal materialen* beperkt de typen tunnels via welke een gevaarlijke stof kan worden getransporteerd door de typen tunnels te identificeren die moeten worden gebruikt. Tunnelcategorieën worden vastgesteld op basis van toepasselijke voorschriften voor het transport van gevaarlijke stoffen. Deze specificatie is doorgaans alleen van toepassing op wegtransport.

Om waarden voor deze specificatie in te stellen, gaat u naar **Productgegevensbeheer \> Instellen \> Vervoersdocumentatie gevaarlijke stoffen \> Tunnel voor gevaarlijke stoffen**. Op de pagina **Tunnel voor gevaarlijke stoffen** kunt u een willekeurig aantal tunnel-id's maken en deze configureren met een identificatiecode en een korte beschrijving.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]