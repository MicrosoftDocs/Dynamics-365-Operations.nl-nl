---
title: Locatie-instructies maken
description: In dit onderwerp wordt uitgelegd hoe u locatie-instructies maakt. Locatie-instructies zijn door gebruiker gedefinieerde regels voor het aangeven van verzamel- en wegzetlocaties voor voorraadverplaatsingen.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016765"
---
# <a name="create-location-directives"></a>Locatie-instructies maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u locatie-instructies maakt. Locatie-instructies zijn door gebruiker gedefinieerde regels voor het aangeven van verzamel- en wegzetlocaties voor voorraadverplaatsingen. Bijvoorbeeld, voor een verkoopordertransactie, bepaalt een locatie-instructie waar de artikelen worden verzameld en waar de verzamelde artikelen worden weggezet.

> [!NOTE]
> Dit onderwerp geldt voor functies in de module voor **Magazijnbeheer**. Het is niet van toepassing op functies in de module [Voorraadbeheer](../inventory/inventory-home-page.md).

Met locatie-instructies kunt u de volgende taken uitvoeren:

- Binnenkomende artikelen wegzetten.
- Artikelen verzamelen en faseren voor uitgaande transacties.
- Grondstoffen verzamelen en klaarzetten voor productie.
- Locaties aanvullen.

## <a name="prerequisites"></a>Vereisten

Voordat u een locatie-instructie kunt maken, moet u deze stappen volgen om er zeker van te zijn dat aan de vereisten wordt voldaan.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Een magazijn maken.
1. Stel op het sneltabblad **Magazijn** de optie **Magazijnbeheerprocessen gebruiken** in op *Ja*.
1. Locaties, locatietypen, locatieprofielen en locatie-indelingen maken. Zie [Locaties configureren in een magazijn met WMS-ondersteuning](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse) voor meer informatie.
1. Maak locaties, zones en zonegroepen. Zie [Magazijn instellen](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) en [Locaties configureren in een magazijn met WMS-ondersteuning](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse) voor meer informatie.

## <a name="setup"></a>Instelling

### <a name="create-location-directives"></a>Maak locatie-instructies aan

Volg deze stappen om een locatie richtlijn te maken.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatie-instructies**.
1. Stel in het lijstvenster het veld **Werkordertype** in op het type voorraadtransactie waarvoor u een locatie-instructie maakt.
1. Selecteer in het actievenster **Nieuw** om een nieuwe locatie-instructie te maken.
1. Voor de nieuwe locatie-instructie stelt u de velden in zoals beschreven in de volgende tabel.

    | Veld | Beschrijving |
    |---|---|
    | Volgnummer | Voer een geheel getal in dat de volgorde van de locatie-instructie aangeeft. De volgorde bepaalt wanneer elke locatie-instructie wordt verwerkt voor het geselecteerde werkordertype. |
    | Naam | Voer een naam in voor de nieuwe locatie-instructie. | 
    | Werktype | Selecteer het type werk dat moet worden uitgevoerd. De lijst met waarden hangt af van het type voorraadtransactie dat u in het veld **Werkordertype** hebt geselecteerd. De volgende waarden zijn mogelijk beschikbaar:<ul><li>**Opslag** : de locatie-instructie zoekt naar de beste locatie voor het plaatsen of vinden van voorraad die in het systeem wordt geleverd via ontvangst-, productie- of voorraadcorrecties. De locatie-instructie wordt ook gebruikt om de faseringslocatie voor klaarzetten of de verzendlocatie van de uiteindelijke laaddeur te definiëren in de uitgaande stroom.</li><li>**Verzamelen** : de locatie-instructie probeert de beste locaties te vinden voor het fysiek reserveren van voorraad (werk maken). De verzameling kan ook worden voltooid (verzamelwerkregel kan worden gesloten) als het werk niet is voltooid. De gebruiker kan de fysieke orderverzameling voltooien. In het systeem is die actie een verzamelstap. De gebruiker kan vervolgens annuleren vanaf een mobiel apparaat en het werk (bijvoorbeeld plaatsen) later voltooien. De werkkoptekst wordt echter pas gesloten wanneer de laatste plaatsing is voltooid.</li><li>**Tellen** , **Correcties** , **Aangepast** , **Wijziging van voorraadstatus** , **Nummerplaat maken** , **Afdrukken** , **Statuswijziging** en **Verpakken naar geneste nummerplaten** : deze waarden zijn niet bruikbaar in een setup met locatie-instructies.</li></ul> |
    | Locatie | Selecteer de locatie waar het werk moet worden voltooid. |
    | Magazijn | Selecteer het magazijn waar het werk moet worden voltooid. |
    | Instructiecode | Selecteer een instructiecode om de selectie van locatie-instructies te bepalen die samenhangen met de werksjabloonneerzetregels waaraan deze code wordt toegewezen. Op de pagina **Instructiecode** kunt u nieuwe codes maken die kunnen worden gebruikt om een werksjabloon te koppelen aan een locatie-instructie. U kunt deze pagina ook gebruiken om de koppeling tussen een werksjabloonregel en een locatie-instructie tot stand te brengen (zoals een laaddeur of faseringslocatie). Zie voor meer informatie over het configureren van een instructiecode met een werksjabloon [Magazijnwerk beheren met werksjablonen en locatie-instructies](control-warehouse-location-directives.md).<p>Als er instructiecode is ingesteld en er werk moet worden gegenereerd, worden de locatie-instructies niet op volgorde doorzocht, maar wordt er op instructiecode gezocht. Zo kunt u specifieker opgeven welke locatiesjabloon wordt gebruikt voor een bepaalde stap in een werksjabloon, zoals de stap voor de fasering van materialen.</p> |
    | Beschikkingscode | Selecteer een beschikkingscode om het wegzetten van de ontvangen artikelen op een locatie aan te passen. (Zie voor meer informatie [Beschikkingscodes instellen](tasks/set-up-dispositions-codes.md).) Dit veld is alleen beschikbaar als het veld **Werkordertype** is ingesteld op *Inkooporders* , *Retourorders* of *Eindproducten wegzetten*. |
    | Meerdere SKU's | Stel deze optie in op *Ja* om meerdere voorraadeenheden (SKU´s) op een locatie te gebruiken. Deze optie moet bijvoorbeeld zijn ingesteld op *Ja* voor de laaddeur.<p>Als de optie **Meerdere SKU's** is ingesteld op *Ja* , wordt de wegzetlocatie opgegeven in het werk (zoals verwacht). De wegzetlocatie kan echter meerdere artikelen verwerken als het werk verschillende SKU's omvat die moeten worden verzameld en opgeslagen, niet als het werk slechts één SKU bevat die moet worden weggezet</p><p>Als u optie **Meerdere SKU's** is ingesteld op *Nee* , wordt de wegzetlocatie alleen opgegeven als er slechts één soort SKU moet worden weggezet.</p><p>Als u beide benaderingen wilt gebruiken, moet u twee regels met dezelfde structuur en instelling opgeven, maar de optie **Meerdere SKU's** instellen op *Ja* voor een van de regels en *Nee* voor de andere. Met andere woorden, er worden twee identieke locatie-instructies gebruikt voor wegzetacties, zelfs als u geen onderscheid maakt tussen enkele en meerdere SKU's in de werk-id. U moet ook een locatie-instructie opgeven voor orderverzameling, zelfs als u een order met meerdere artikelen hebt.</p><p>**Opmerking:** Als u de optie **Meerdere SKU's** instelt op *Ja* voor een locatie-instructie van het werktype *Wegzetten* , wordt altijd automatisch de eerste regel van de locatie-instructie geselecteerd ongeacht andere beperkingen die in de regels worden gemaakt.</p> |

1. Optioneel: selecteer in het actievenster **Query bewerken** om de locaties te selecteren of beperkingen op te geven die worden toegepast wanneer u een specifieke locatie-instructie selecteert.
1. Maak op het sneltabblad **Regels** een of meer regels om eenheden te maken en een hoeveelheid in een magazijn te zoeken of te reserveren.
1. Voor elke nieuwe regel stelt u de velden in zoals beschreven in de volgende tabel.

    | Veld | Beschrijving |
    |---|---|
    | Volgnummer | Voer een geheel getal in dat de volgorde van de locatie-instructie aangeeft. De volgorde bepaalt wanneer elke locatie-instructie wordt verwerkt voor het geselecteerde werktype. |
    | Vanaf hoeveelheid | Geef het hoeveelheidsbereik bij aanvang op voor wanneer de volgorde van het middelste raster moet worden geselecteerd. Geef de hoeveelheid op in de maateenheid die is geselecteerd in het veld **Eenheid**. |
    | Tot hoeveelheid | Geef het hoeveelheidsbereik aan het einde op voor wanneer de volgorde van het middelste raster moet worden geselecteerd. Geef de hoeveelheid op in de maateenheid die is geselecteerd in het veld **Eenheid**. |
    | Eenheid | Selecteer de maateenheid voor de artikelen.<p>U kunt een minimum hoeveelheid en een maximum hoeveelheid opgeven waarop de richtlijn moet worden toegepast. U kunt ook opgeven dat de instructie moet worden gebruikt voor een specifieke voorraadeenheid. Het veld **Eenheid** wordt gebruikt voor de evaluatie van de hoeveelheid.</p><p>Het systeem evalueert hoeveelheden met behulp van de waarde **Eenheid** die op de regel is opgegeven om te bepalen of een regel in de locatie-instructie van toepassing is. Elke keer dat een locatie-instructieregel wordt geopend, wordt geprobeerd de vraageenheid om te zetten in een eenheid die is opgegeven op de regel. Als de eenheidomrekening niet bestaat, gaat het systeem naar de volgende regel.</p> |
    | Hoeveelheid plaatsen | Dit veld is alleen geldig wanneer u in het magazijn een hoeveelheid probeert te plaatsen of te zoeken. Met andere woorden, het is alleen geldig voor *wegzetten*. Selecteer de methode die wordt gebruikt om te controleren of de hoeveelheid in het bereik ligt dat is ingesteld in de velden **Vanaf hoeveelheid** en **Tot hoeveelheid**. Als de locatie-instructie geldt voor een binnenkomende transactie, selecteert u een van de volgende opties:<ul><li>**Nummerplaathoeveelheid** : wanneer moet worden gecontroleerd of de hoeveelheid zich in het doelbereik bevindt, gebruikt u de hoeveelheid op de ontvangen nummerplaat.</li><li>**In eenheden omgezette hoeveelheid** : wanneer moet worden gecontroleerd of de hoeveelheid zich in het doelbereik bevindt, gebruikt u de hoeveelheid die in eenheden is omgezet tijdens de transactie. Als u in een magazijn bijvoorbeeld een hoeveelheid van 1000 kunt ontvangen en dit is opgedeeld in 10 nummerplaten van elk 100, kunt u een hoeveelheid van 1000 artikelen gebruiken in plaats van een nummerplaathoeveelheid van 100.</li><li>**Resterende hoeveelheid** : wanneer moet worden gecontroleerd of een hoeveelheid zich in het doelhoeveelheidsbereik bevindt, wordt de resterende te ontvangen hoeveelheid gebruikt op de inkooporderregel die wordt ingecheckt.</li><li>**Verwachte hoeveelheid** : wanneer moet worden gecontroleerd of een hoeveelheid zich in het doelhoeveelheidsbereik bevindt, gebruikt u de totale hoeveelheid op de inkooporderregel, ongeacht de hoeveelheid die al is ontvangen.</li></ul> |

1. Optioneel: U kunt de volgende aanvullende velden instellen op het sneltabblad **Regels**.

    | Veld | Beschrijving |
    |---|---|
    | Beperken op eenheid | Schakel dit selectievakje in om de maateenheden te beperken die als geldige selectiecriteria worden beschouwd voor de locatie-instructieregels. Wanneer er maateenheden zijn opgegeven, worden alleen de artikelen waarvoor de eenheid overeenkomt met ten minste één eenheid die voor de eenheidsvolgordegroep is gedefinieerd, als geldig beschouwd voor de regelselectie.<p>De eenheid is bijvoorbeeld beperkt tot pallets en het artikel is gekoppeld aan een eenheidsvolgordegroep die de eenheid *pallets* bevat. In dit geval worden de artikelen beschouwd als een geldige optie voor de locatie-instructie.</p><p>In het selectievakje **Beperken op eenheid** worden echter niet de eenheden bepaald die op werkregels zijn toegepast. De eenheidsbeperking geldt alleen voor eenheden die beschikbaar worden gemaakt via de eenheidsvolgordegroep.</p><p>Een artikel is bijvoorbeeld gekoppeld aan een eenheidsvolgordegroep die zowel de eenheid *pallets* als de eenheid *stuks* bevat. Er is een maateenheid gedefinieerd waarbij 1 pallet = 100 stuks en de locatie-instructie gebruikt de functionaliteit **Beperken op eenheid** alleen voor pallets. Bovendien is er een werksjabloon gedefinieerd die het maken van de werkkoptekst beperkt tot 50 stuks. In dit geval worden werkregels van 50 stuks gemaakt.</p><p>Voer de volgende stappen uit om de maateenheid voor de beperking op te geven:</p><ol><li>Selecteer op het sneltabblad **Regels** de optie **Beperken op eenheid**. Deze knop is alleen beschikbaar als u het selectievakje **Beperken op eenheid** op de regel hebt ingeschakeld en vervolgens **Opslaan** hebt geselecteerd.</li><li>Selecteer in het veld **Eenheid** de maateenheid voor het beperken van de orderverzamel- en wegzetprocessen.</li></ol> |
    | Naar eenheid afronden | Selecteer deze optie om aan te geven dat de orderverzameling voor grondstoffen naar boven moet worden afgerond tot een veelvoud van de materiaalverwerkingseenheid die is opgegeven in het veld **Beperken op eenheid**. Dit veld is alleen van toepassing voor orderverzameling van grondstoffen en locatie-instructies van het type *Orderverzameling*. |
    | Zoek verpakkingshoeveelheid | Schakel dit selectievakje in als een hoeveelheid voor de verpakkingseenheid in de pagina **Verkooporder** is opgegeven. Als u dit selectievakje inschakelt, worden alleen de locaties met deze hoeveelheid geselecteerd. |
    | Splitsing toestaan | Selecteer dit selectievakje om het gedefinieerde hoeveelheid artikelen, op te splitsen, over meerdere locaties. |
    | Sjabloon voor directe aanvulling | Maak verbinding met een aanvullingssjabloon zodat de aanvulling direct wordt gestart als artikelen niet zijn toegewezen. Als u het veld leeg laat, wordt de aanvulling van artikelen pas gestart nadat alle regels van de locatie-instructie zijn verwerkt.<p>Dit veld is alleen beschikbaar voor geselecteerde werkordertypen, waarbij aanvulling is toegestaan, zoals *Verkooporders* en *Orderverzamelen van grondstoffen*.</p> |

1. Selecteer op het sneltabblad **Locatie-instructieacties** op **Nieuw** om de locatie of het bereik van locaties te selecteren.
1. In het veld **Volgnummer** wordt de volgorde weergegeven waarin de locatie-instructie wordt verwerkt voor het geselecteerde werktype. U kunt de volgorde wijzigen. Wees echter voorzichtig met volgnummers voor de locatie-instructieacties, omdat deze altijd in deze volgorde worden uitgevoerd.
1. Voer in het veld **Naam** de naam in voor de locatie-instructieactie. Geef duidelijk aan wat de actie is.
1. Optioneel: Selecteer **Query bewerken** om de magazijnlocaties en andere criteria te wijzigen.
1. Optioneel: U kunt de volgende aanvullende velden instellen voor een locatie-instructie.

    | Veld | Beschrijving |
    |---|---|
    | Gebruik vaste locaties | Selecteer voor welke locaties u een locatie-instructie zou moeten overwegen:<ul><li>**Vaste en niet-vaste locaties** : alle locaties komen in aanmerking voor de locatie-instructie.</li><li>**Alleen vaste locaties voor het product** : alleen vaste locaties voor producten komen in aanmerking voor de locatie-instructie.</li><li>**Alleen vaste locaties voor de productvariant** : alleen vaste locaties voor productvarianten komen in aanmerking voor de locatie-instructie.</li></ul> |
    | Negatieve voorraad toestaan | Schakel dit selectievakje in om negatieve voorraad van artikelen op de opgegeven magazijnlocatie toe te staan. |
    | Batch ingeschakeld | Schakel dit selectievakje in om batchstrategieën voor de artikelen te gebruiken waarvoor batches zijn ingeschakeld. Als dit selectievakje is ingeschakeld en het veld **Strategie** is ingesteld op *Geen* , gaat het systeem verder naar de volgende actieregel. |
    | Strategie | Selecteer de strategie die de locatie-instructie moet gebruiken:<ul><li>**Geen** : er wordt geen strategie gebruikt.</li><li>**Verpakkingshoeveelheid afstemmen** : deze strategie wordt gebruikt om te controleren of een orderverzamellocatie de benodigde verpakkingshoeveelheid heeft. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Orderverzamelen*.</li><li>**Consolideren** : deze strategie wordt gebruikt om artikelen in een bepaalde locatie te consolideren wanneer vergelijkbare artikelen beschikbaar zijn. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Wegzetten*. In een standaardinstelling voor wegzetten wordt op de eerste actieregel geprobeerd te consolideren en vervolgens wordt op de tweede actieregel geprobeerd om weg te zetten zonder consolidatie. Door goederen te consolideren wordt orderverzamelen later efficiënter.</li><li>**FEFO-batchreservering** : deze strategie wordt gebruikt wanneer voorraad wordt gevonden door middel van een batchvervaldatum, en voor een batchreservering wordt toegewezen. De FEFO-batchreserveringsstrategie (First Expiry, First Out) wordt ook gebruikt wanneer de voorraad is gelokaliseerd aan de hand van een uiterste houdbaarheidsdatum van de batch naast de vervaldatum. U kunt deze strategie alleen maar voor batch ingeschakelde artikelen gebruiken. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Orderverzamelen*. Wanneer u deze strategie selecteert, heft u eventuele querysortering op voor batchnummers die worden toegepast.</li><li>**Naar volledige LP afronden** : deze strategie wordt gebruikt om de voorraadhoeveelheid af te ronden om de nummerplaathoeveelheid te verzamelen die aan de artikelen is toegewezen. Deze strategie kan alleen worden gebruikt voor locatie-instructies van het aanvullingstype en alleen als het veld **Werktype** wordt ingesteld op *Orderverzamelen*.</li><li>**Lege locatie zonder inkomend werk** : deze strategie wordt gebruikt om blanco locaties te vinden. Een locatie wordt beschouwd als leeg als het geen fysieke voorraad en geen verwacht inkomend werk heeft. Deze strategie is alleen geldig als het veld **Werktype** is ingesteld op *Wegzetten*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Voorbeeld van het gebruik van locatie-instructies

Voor dit voorbeeld kijken we naar een inkooporderproces waar de locatie-instructie vrije capaciteit in een magazijn moet zoeken voor voorraadartikelen die zojuist zijn geregistreerd in het ontvangende dok. Eerst moet u we beschikbare capaciteit in het magazijn vinden door te consolideren met bestaande voorhanden voorraad. Als consolidatie niet mogelijk is, moet u een lege locatie zoeken.

Voor dit scenario moet u twee locatie-instructieacties definiëren. De eerste actie in de reeks moet de **consolidatie** -strategie gebruiken, de tweede de **Lege locatie met geen inkomend werk** -strategie. Tenzij u een derde actie definieert om een overloopscenario te dekken, zijn er twee resultaten mogelijk wanneer er geen capaciteit meer is in het magazijn: werk kan worden gemaakt zonder dat er locaties worden gedefinieerd of het werkaanmaakproces mislukt. Het resultaat wordt gedefinieerd door de instellingen op de pagina **Fouten bij locatie-instructie** , waar u kunt kiezen om de optie **Werk stoppen bij fout van locatie-instructie** voor elk type werkorder te selecteren.

## <a name="next-step"></a>Volgende stap

Nadat u locatie-instructies hebt gemaakt, kunt u elke instructiecode aan een werksjablooncode voor het maken van werk koppelen. Zie voor meer informatie [Magazijnwerk beheren met werksjablonen en locatie-instructies](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Technische informatie voor systeembeheerders

Als u geen toegang hebt tot de pagina's waarmee u deze taak kunt voltooien, moet u contact opnemen met uw systeembeheerder en de informatie opgeven die wordt beschreven in de volgende tabel.

| Categorie | Vereiste |
|---|---|
| Configuration Keys | Ga naar **Systeembeheer \> Instellingen \> Licentieconfiguratie**. Breid de licentiesleutel voor **Handel** uit en selecteer de configuratiesleutel voor **Magazijn- en transportbeheer**. |
