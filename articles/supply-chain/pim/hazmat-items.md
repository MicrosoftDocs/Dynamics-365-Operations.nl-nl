---
title: Gevaarlijke stoffen in producten, orders, zendingen en ladingen
description: In dit onderwerp wordt uitgelegd hoe u eigenschappen voor gevaarlijke stoffen kunt instellen voor vrijgegeven producten, hoe u voorraadlimieten voor gevaarlijke stoffen kunt instellen en hoe u gevaarlijke stoffen kunt opnemen in een verkooporder, zending of lading.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7e0564802bc53ce21236ffc6ed065bf6abac7c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243148"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Gevaarlijke stoffen in producten, orders, zendingen en ladingen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u eigenschappen voor gevaarlijke stoffen kunt instellen voor vrijgegeven producten, hoe u voorraadlimieten voor gevaarlijke stoffen kunt instellen en hoe u gevaarlijke stoffen kunt opnemen in een verkooporder, zending of lading.

## <a name="set-hazardous-material-specifications-for-products"></a>Specificaties voor gevaarlijke stoffen instellen voor producten

Nadat u een regelgeving voor gevaarlijke stoffen hebt gedefinieerd en de bijbehorende referentiecodes hebt ingesteld, zoals is beschreven in [Gevaarlijke stoffen instellen](hazmat-setup.md), kunt u deze gegevens koppelen aan vrijgegeven artikelen. De verzendtekst voor vervoersdocumenten wordt opgehaald uit de informatie over gevaarlijke stoffen voor de vrijgegeven artikelen.

Als onderdeel van het proces voor het koppelen van een vrijgegeven artikel aan een gevaarlijke stof moet u de regelgevingscode en het materiaal opgeven. Afhankelijk van de transportmethoden kunnen er verschillende regelgevingscodes aan een artikel worden gekoppeld, en u kunt meerdere regelgevingen en materiaalcodes aan een artikel koppelen.

Voer de volgende stappen uit als u een vrijgegeven product wilt instellen als een gevaarlijke stof.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer of maak een product om de pagina **Vrijgegevens productgegevens** te openen.
1. Stel op het sneltabblad **Voorraad beheren** de optie **Gevaarlijke stof** in op **Ja**. Met deze instelling wordt het artikel aangeduid als een gevaarlijke stof. De instelling wordt gebruikt wanneer het vervoersdocument wordt afgedrukt.
1. Selecteer in het Actievenster, op het tabblad **Voorraad beheren** in de groep **Conformiteit** de optie **Artikel met gevaarlijke stoffen**.
1. Vul de pagina **Artikel met gevaarlijke stoffen** voor het geselecteerde artikel in met behulp van de velden die in de volgende subsecties worden beschreven.

### <a name="item-hazardous-materials-header"></a>Kop voor artikel met gevaarlijke stoffen

In de volgende tabel worden de velden beschreven die bovenaan de pagina **Artikel met gevaarlijke stoffen** beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| artikelnummer | Het vrijgegeven product waarmee u werkt. |
| Reguleringscode | Selecteer de regelgeving voor gevaarlijke stoffen die van toepassing is op het product. De regelgeving bepaalt hoe de afgedrukte verzendtekst voor een artikel en de bijbehorende leveringsmethoden wordt gemaakt. Wanneer de code is toegewezen, kan deze niet op deze pagina worden bewerkt. U kunt echter wel een nieuwe regelgevingscode toewijzen door **Nieuw** te selecteren. |
| Materiaalcode | (Optioneel) Selecteer de code voor gevaarlijke stoffen die van toepassing is op het product. De materiaalcode biedt een sjabloon die standaardwaarden bevat voor veel andere velden op deze pagina. Wanneer u een code selecteert, worden alle specificaties voor gevaarlijke stoffen naar het huidige product gekopieerd. Het systeem vraagt u echter eerst om te bevestigen dat artikelmateriaalgegevens moeten worden ingevuld vanuit de materiaalcode. |
| Groepscode | (Optioneel) Selecteer de classificatiegroep voor gevaarlijke stoffen die van toepassing is op het product. Net als voor het veld **Materiaalcode** geldt ook hier dat wanneer u een code selecteert, alle specificaties voor gevaarlijke stoffen naar het huidige product gekopieerd. Het systeem vraagt u echter eerst om te bevestigen dat gegevens voor de artikelklassegroep moeten worden ingevuld vanuit de groepscode. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Sneltabblad Beschrijvingen

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Beschrijvingen**.

| Veld | Beschrijving |
|---|---|
| Geschikte verzendnaam | Voer de standaardbeschrijving in voor het materiaal, zoals is opgegeven in de toepasselijke regelgeving. U kunt vertalingen voor deze waarde opgeven op het sneltabblad **Vertaling van verzendingstekst voor artikel**, zoals wordt beschreven in de volgende sectie. |
| Technische naam | Selecteer de algemene naam van het materiaal. Deze naam kan een naam zijn die intern door uw bedrijf voor het materiaal wordt gebruikt. |
| N.O.S. | Schakel dit selectievakje in om aan te geven dat de **Juiste verzendnaam** een N.O.S.-verzendnaam (niet specifieke) voor het artikel is. N.O.S. verzendnamen worden gebruikt voor groepen vergelijkbare chemicaliën en materialen met specifieke eindtoepassingen, maar die mogelijk niet op naam worden vermeld in de hazmat-tabel in een specifieke regelgeving. |

### <a name="item-ship-text-translation-fasttab"></a>Sneltabblad Vertaling van verzendingstekst voor artikel

Het sneltabblad **Vertaling van verzendingstekst voor artikel** bevat een raster met vertalingen van de waarden voor **Juiste verzendnaam** die voor de primaire taal zijn gedefinieerd op het sneltabblad **Beschrijvingen**. Deze vertalingen kunnen worden gebruikt in verzendtekst voor een of meer aanvullende talen.

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Vertaling van verzendingstekst voor artikel**.


| Veld | Beschrijving |
|---|---|
| Taal | De taalcode die in de rij wordt gebruikt. Bijvoorbeeld, **pt-br** geeft Portugees (Brazilië) aan. |
| Afdruktekst verzending | De vertaalde waarde voor **Juiste verzendnaam** in de taal die de rij gebruikt. |

Als u een vertaling wilt toevoegen of bewerken, selecteert u **Vertalingen** boven het raster om de pagina **Tekstvertalingen** te openen. Voer vervolgens een van deze stappen uit:

- Als u een nieuwe vertaling wilt toevoegen selecteer in het actievenster de optie **Toevoegen**. Selecteer de taal die u wilt toevoegen en voer in het veld **Vertaalde tekst** de vertaling in.
- Als u een bestaande vertaling wilt bewerken, selecteert u een doeltaal in het veld **Taal** en bewerkt u zo nodig de vertaling in het veld **Vertaalde tekst**.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Sneltabblad Materiaalbeheer

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Materiaalbeheer**.

| Veld | Beschrijving |
|---|---|
| Klasse | Selecteer de klasse voor de gevaarlijke stof waartoe het product behoort, zoals gedefinieerd in de regelgeving waaraan u conformeert. U moet zowel een verdeling als een klasse toewijzen aan elk product dat gevaarlijke stoffen bevat. |
| Beschrijving | De beschrijving die is gedefinieerd voor de klasse die is geselecteerd in het veld **Klasse**. Dit veld is alleen-lezen. |
| Afdeling | Selecteer de verdeling voor de gevaarlijke stof waartoe het product behoort, zoals gedefinieerd in de regelgeving waaraan u conformeert. De verdeling is een subset van de klasse. U moet zowel een verdeling als een klasse toewijzen aan elk product dat gevaarlijke stoffen bevat. |
| Id | Selecteer de identificatiecode van de gevaarlijke stof. Deze code is doorgaans gebaseerd op een UN-standaard (Verenigde Naties). |
| Verpakkingsgroep | Selecteer de verpakkingsgroep die van toepassing is op het huidige artikel. |
| Beschrijving | De beschrijving die is gedefinieerd voor de groep die is geselecteerd in het veld **Verpakkingsgroep**. Dit veld is alleen-lezen. |
| Verpakkingsbeschrijvingen | Selecteer de toepasselijke verpakkingsbeschrijving. Deze code verwijst naar een beschrijving die aangeeft hoe het product moet worden verpakt. |
| Labels voor gevaarlijke stoffen | Selecteer een code die verwijst naar het toepasselijke label voor gevaarlijke stoffen dat op het product moet worden bevestigd. |
| Beperkte hoeveelheid | Stel deze optie in op **Ja** als u het totale productgewicht wilt rapporteren dat is opgenomen in elke lading en op elke laadregel. |
| Hoeveelheid | Voer de hoeveelheid gevaarlijk stoffen in het product in, in de opgegeven eenheid. Deze waarde wordt gebruikt om de totale score van gevaarlijke stoffen te berekenen voor ladingen en zendingen die het product bevatten. |
| Factor | Voer de vermenigvuldiger in die wordt toegepast bij het berekenen van de score van gevaarlijke stoffen voor elke laadregel die het product bevat. Deze waarde wordt bepaald door de toepasselijke regelgeving, afhankelijk van het type gevaarlijke stof dat in het product is opgenomen. |
| Eenheid | Selecteer de maateenheid die van toepassing is op de hoeveelheid gevaarlijke stoffen in het product, zoals is opgegeven in het veld **Hoeveelheid**. Deze waarde wordt gebruikt om de totale score van gevaarlijke stoffen te berekenen voor ladingen en zendingen die het product bevatten. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Berekening van de score van gevaarlijke stoffen

Diverse waarden die zijn opgegeven op het sneltabblad **Materiaalbeheer** voor een product worden gebruikt om een *score van gevaarlijke stoffen* te bereken voor elke laadregel die dat product bevat. De score wordt berekend met de volgende formule:

Score van gevaarlijke stoffen = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Dit is een sleutel voor de formule:

- *&lt;LineQty&gt;* is de hoeveelheid van het product die voor een laadregel is opgegeven.
- *&lt;HazmatQty&gt;* is de hoeveelheid van de gevaarlijke stof die voor een product is opgegeven in het veld **Hoeveelheid** op het sneltabblad **Materiaalbeheer**.
- *&lt;UnitConversion&gt;* is een omrekeningsfactor om de eenheid die wordt gebruikt voor de hoeveelheid op de laadregel te converteren naar de eenheid die voor een product is opgegeven in het veld **Eenheid** op het sneltabblad **Materiaalbeheer**.
- *&lt;Multiplier&gt;* is de vermenigvuldiger die voor een product is opgegeven in het veld **Vermenigvuldiger** op het sneltabblad **Materiaalbeheer**.

Deze score wordt aangegeven voor elke laadregel die een product bevat waarin deze waarden zijn opgegeven. Meer informatie vindt u in de secties [Zendingen die gevaarlijke stoffen bevatten](#hazmat-shipments) en [Ladingen die gevaarlijke stoffen bevatten](#hazmat-loads) verderop in dit onderwerp.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Berekening van het gewicht van gevaarlijke stoffen

Ladingen en laadregels die producten bevatten waarvoor de optie **Beperkte hoeveelheid** op het sneltabblad **Materiaalbeheer** is ingesteld op **Ja**, tonen het totale gewicht van gevaarlijke stoffen, zoals wordt beschreven in de secties [Zendingen die gevaarlijke stoffen bevatten](#hazmat-shipments) en [Ladingen die gevaarlijke stoffen bevatten](#hazmat-loads) verderop in dit onderwerp. Het gewicht van gevaarlijke stoffen wordt berekend met de volgende formule:

Gewicht van gevaarlijke stoffen = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Dit is een sleutel voor de formule:

- *&lt;LineQty&gt;* is de hoeveelheid van het product die voor een laadregel is opgegeven.
- *&lt;ProductWeight&gt;* is het nettogewicht dat is opgegeven voor het product, in de voorraadeenheid die is opgegeven voor het product.
- *&lt;UnitConversion&gt;* is een omrekeningsfactor om de eenheid die wordt gebruikt voor de hoeveelheid op de laadregel te converteren naar de voorraadeenheid die wordt gebruikt voor *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>Sneltabblad Transportgegevens

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Transportgegevens**.

| Veld | Beschrijving |
|---|---|
| Transportcategorie | Selecteer de gerelateerde transportcategorie. |
| Tunnelcode | Selecteer de gerelateerde tunnelbeperkingscode voor het artikel. |
| Opslagruimte gevaarlijk materiaal | Selecteer de referentiecode die wordt gebruikt voor de behandeling van bergruimte van zeevracht wanneer het artikel over zee wordt vervoerd. |
| Type vliegtuig | Selecteer de vliegtuigbeperking die van toepassing is op het materiaal wanneer het via de lucht wordt vervoerd. |
| Verpakking - alleen vrachtvliegtuigen | Op basis van de waarde die u hebt geselecteerd in het veld **Type vliegtuig** selecteert u de code voor verpakkingsinstructies die van toepassing is wanneer het product alleen met een cargovlucht kan worden vervoerd. |
| Verpakking - passagiers- en vrachtvliegtuigen | Op basis van de waarde die u hebt geselecteerd in het veld **Type vliegtuig** selecteert u de code voor verpakkingsinstructies die van toepassing is wanneer het product kan worden vervoerd met een cargovlucht of passagiersvlucht. |
| IATA-ster | Stel deze optie in op **Ja** om aan te geven dat de luchttransportspecificaties die op dit sneltabblad zijn ingevoerd, verband houden met de IATA-norm (International Air Transport Association) voor gevaarlijke stoffen. Dit veld is alleen bedoeld voor informatieve doeleinden. |
| Reactie op noodgevallen | Selecteer de code die verwijst naar instructies voor het omgaan met het materiaal in noodgevallen. |

### <a name="environmental-information-fasttab"></a>Sneltabblad Milieugegevens

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Milieugegevens**.

| Veld | Beschrijving |
|---|---|
| Schadelijk voor milieu | Stel deze optie in op **Ja** om aan te geven dat het product milieutechnisch gevaarlijk is. Gebruik dit veld voor uw eigen rapportagedoeleinden. |
| Mariene verontreiniging | Stel deze optie in op **Ja** om aan te geven dat het product zeevervuilend is. Gebruik dit veld voor uw eigen rapportagedoeleinden. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Voorraadlimieten instellen voor gevaarlijke producten

Om veiligheidsredenen moet u mogelijk de totale hoeveelheid van een bepaald product beperken die op één locatie kan worden opgeslagen. Volg deze stappen om voorraadlimieten in te stellen voor een product.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer een product om de pagina **Details van vrijgegeven product** te openen.
1. Selecteer in het Actievenster, op het tabblad **Voorraad beheren** in de groep **Conformiteit** de optie **Rapportagegegevens**.
1. Stel in de velden **Voorraadlimiet gevaarlijke stoffen** en **Waarschuwing limiet gevaarlijke stoffen** de toepasselijke waarden in voor het geselecteerde product.

Met het rapport **Voorraadlimiet voor gevaarlijke stoffen** kunt u de voorraadniveaus van de gevaarlijke stoffen op uw magazijnlocaties controleren, om na te gaan of ze onder de veilige limieten blijven die hier zijn ingesteld. Meer informatie vindt u in [Rapport Voorraadlimiet voor gevaarlijke stoffen](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Verkoopordertransacties die gevaarlijke stoffen bevatten

Als u een product dat is geclassificeerd als een gevaarlijke stof wilt opnemen in een verkooporder, moet u de relevante vervoerder koppelen aan de verkooporder. Open de verkooporder en stel vervolgens op het sneltabblad **Levering** de velden **Vervoerder** en **Vervoerdersservice** in, zoals vereist.

De vervoerder is eveneens gekoppeld aan de leveringsmethode. Dat betekent dat u ervoor moet zorgen dat deze gegevens zijn afgestemd op de regelgeving voor gevaarlijke stoffen. Met andere woorden, de leveringsmethode die is opgegeven in de regelgeving voor gevaarlijke stoffen moet overeenkomen met de specificaties in de koptekst van de verkooporder. Op deze manier zijn de regelgeving, vervoerder en vervoerdersservice verbonden met de zendingsregels die op een verkooporder worden gebruikt.

Nadat een verkooporder is voltooid en gereed is om te worden verzonden, kan deze worden vrijgegeven aan het magazijn om de overdracht tussen verkoop- en magazijnbewerkingen aan te geven.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Zendingen die gevaarlijke stoffen bevatten

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>De scores voor gevaarlijke stoffen voor elke zendingsregel bekijken

De pagina **Details van zending** voor een zending toont de waarden voor het totale gewicht en de punten van gevaarlijke stoffen die zijn berekend voor elke laadregel die in die zending is opgenomen. Voer de volgende stappen uit om de scores en gewichten te bekijken.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Selecteer een zending om de pagina **Details van zending** te openen.
1. Bekijk de regels op het sneltabblad **Laadregels**. Voor elke regel ziet u de berekeningen voor de gevaarlijke stoffen in de volgende velden:

    - **Punten voor gevaarlijke stoffen**: dit veld toont de score voor gevaarlijke stoffen voor de laadregel. De waarde wordt berekend op basis van de regels en waarden die zijn ingesteld voor de toepasselijke regelgeving en in de instellingen van het vrijgegeven product. De berekening gebruikt de hoeveelheid op de laadregel en de vermenigvuldiger in de [Instellingen voor materiaalbeheer](#material-management) voor het vrijgegeven product.
    - **Beperkt nettogewicht**: voor producten die zijn gemarkeerd als producten met een beperkte hoeveelheid omdat ze gevaarlijke stoffen bevatten, bevat dit veld het totale nettogewicht van de gevaarlijke inhoud dat op de laadregel is opgenomen. De berekening is gebaseerd op de producten die in de instellingen van het vrijgegeven product zijn gemarkeerd als gevaarlijke stoffen. Als een artikel is gemarkeerd als een artikel met een beperkte hoeveelheid, wordt de hoeveelheid op elke laadregel gebruikt en wordt gerefereerd aan het gewicht in de [Instellingen voor materiaalbeheer](#material-management) voor het vrijgegeven product.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Controleren op compatibiliteit tussen gevaarlijke stoffen die in een zending zijn opgenomen

Het systeem kan beoordelen of alle gevaarlijke stoffen die in een zending zijn opgenomen, geschikt zijn om samen te worden verzonden. Om de compatibiliteit te evalueren, controleert het systeem de compatibiliteitsgroep die is toegewezen aan elk product dat in de zending is opgenomen. Meer informatie vindt u in [Rapport Compatibiliteitsgroepen voor gevaarlijke stoffen](hazmat-setup.md#compatibility-groups).

Voer deze stappen uit om de compatibiliteitscontrole uit te voeren.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle zendingen**.
1. Selecteer een zending om de pagina **Details van zending** te openen.
1. Selecteer in het Actievenster op het tabblad **Zendingen** in de groep **Acties** de optie **Compatibiliteitscontrole**.

U ontvangt een bericht waarin u wordt geïnformeerd over de resultaten van de controle.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Ladingen die gevaarlijke stoffen bevatten

### <a name="view-hazardous-material-scores-for-each-load-line"></a>De scores voor gevaarlijke stoffen voor elke laadregel bekijken

De pagina **Details van lading** voor een lading toont de waarden voor het totale gewicht en de punten van gevaarlijke stoffen die zijn berekend voor die lading en voor elke laadregel. Voer de volgende stappen uit om de scores en gewichten te bekijken.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle ladingen**.
1. Selecteer een lading om de pagina **Details van lading** te openen. (U kunt de details van een lading ook openen door een koppeling te selecteren in een gerelateerde zending.)
1. Op het sneltabblad **Lading** kunt u de totale score en het totale gewicht voor gevaarlijke stoffen voor de hele lading controleren door de volgende velden te controleren:

    - **Punten voor gevaarlijke stoffen**: dit veld toont de score voor gevaarlijke stoffen voor de lading. De waarde wordt berekend op basis van de regels en waarden die zijn ingesteld voor de toepasselijke regelgeving en in de instellingen van het vrijgegeven product. De berekening gebruikt de hoeveelheid die is opgenomen in de lading en refereert aan de vermenigvuldiger in de [Instellingen voor materiaalbeheer](#material-management) voor het vrijgegeven product.
    - **Beperkt nettogewicht**: voor producten die zijn gemarkeerd als producten met een beperkte hoeveelheid omdat ze gevaarlijke stoffen bevatten, bevat dit veld het totale nettogewicht van de gevaarlijke inhoud dat in de lading is opgenomen. De berekening is gebaseerd op de producten die in de instellingen van het vrijgegeven product zijn gemarkeerd als gevaarlijke stoffen. Als een artikel is gemarkeerd als een artikel met een beperkte hoeveelheid, wordt de hoeveelheid in elke lading gebruikt en wordt gerefereerd aan het gewicht in de [Instellingen voor materiaalbeheer](#material-management) voor het vrijgegeven product.

1. Als u de scores en gewichten voor afzonderlijke regels wilt bekijken, selecteert u het sneltabblad **Laadregels**. De waarden die voor elke regel worden opgegeven, komen overeen met de waarden die voor de hele lading zijn opgegeven, zoals wordt beschreven in de vorige stap.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Controleren op compatibiliteit tussen gevaarlijke stoffen die in een lading zijn opgenomen

Het systeem kan beoordelen of alle gevaarlijke stoffen die in een lading zijn opgenomen, geschikt zijn om samen te worden verzonden. Om de compatibiliteit te evalueren, controleert het systeem de compatibiliteitsgroep die is toegewezen aan elk product dat in de lading is opgenomen. Meer informatie vindt u in [Rapport Compatibiliteitsgroepen voor gevaarlijke stoffen](hazmat-setup.md#compatibility-groups).

Voer deze stappen uit om de compatibiliteitscontrole uit te voeren.

1. Ga naar **Magazijnbeheer \> Zendingen \> Alle ladingen**.
1. Selecteer een lading om de pagina **Details van lading** te openen. (U kunt de details van een lading ook openen door een koppeling te selecteren in een gerelateerde zending.)
1. Selecteer in het Actievenster op het tabblad **Ladingen** in de groep **Acties** de optie **Compatibiliteitscontrole**.

U ontvangt een bericht waarin u wordt geïnformeerd over de resultaten van de controle.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]