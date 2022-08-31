---
title: USMCA-certificaat van oorsprong
description: Met deze functie kunt u documenten voor het certificaat van oorsprong afdrukken die voor de Verenigde Staten-Mexico-Canada-overeenkomst (USMCA) zijn vereist.
author: Weijiesa
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: edf235351fc7cbffc6bf80c7e05c53159c1e8a7f
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336540"
---
# <a name="usmca-certification-of-origin"></a>USMCA-certificaat van oorsprong

[!include [banner](../includes/banner.md)]

Met deze functie kunt u documenten voor het certificaat van oorsprong afdrukken die voor de Verenigde Staten-Mexico-Canada-overeenkomst (USMCA) zijn vereist.

Het *document voor het USMCA-certificaat van oorsprong* bevat de minimaal vereiste gegevenselementen voor aangifte. Sommige gegevenselementen kunnen worden ingevuld voordat ze worden afgedrukt, terwijl andere elementen handmatig moeten worden ingevuld na het afdrukken. Om een preferentiële tariefbehandeling te verkrijgen, moet het document worden ingevuld en in het bezit zijn van de importeur op het moment dat de aangifte wordt gedaan. Het document kan worden ingevuld door de importeur, de exporteur of de producent.

U kunt het document afdrukken voor een enkele zending vanuit de lijstpagina **Alle zendingen** of vanuit de pagina **Zendingsgegevens**.

Het document is alleen toegankelijk als het land in het primaire adres voor de rechtspersoon de Verenigde Staten is.

Afhankelijk van de geselecteerde afdrukinstellingen van het document, kan het document vooraf worden ingevuld met gegevens vanuit uw systeem. Het is mogelijk om gegevens te wijzigen of toe te voegen aan het afgedrukte document door het afgedrukte document te exporteren naar een bewerkbare indeling, zoals Microsoft Word. Na het exporteren kunt u alle vereiste wijzigingen toepassen voordat u een aangifte doet.

## <a name="turn-the-usmca-feature-on-or-off"></a>De USMCA-functie in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Document van USMCA-oorsprongscertificaat* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="document-content"></a>Inhoud van document

Het document voor het USMCA-certificaat van oorsprong bevat de volgende gegevenselementen:

- Adreselementen
- Rol van de certificerende partij
- Enkele zending
- Facturen
- Afroepperiode
- Artikeldetails
- Handtekening van certificerende
- Aantal pagina's

Zie de overige secties in dit artikel voor meer informatie over elk van deze elementen en de manier waarop hun waarden worden gevonden.

## <a name="print-a-usmca-certification-of-origin-document"></a>Een document voor USMCA-certificaat van oorsprong afdrukken

Ga als volgt te werk om een document voor het USMCA-certificaat van oorsprong voor een zending af te drukken:

1. U kunt een van de volgende dingen doen:
    - Ga naar **Transportbeheer > Zendingen > Alle zendingen** en selecteer de zending waarvoor u het document wilt afdrukken.
    - Open de pagina **Zendingsgegevens** voor de zending waarvoor u het document wilt afdrukken (op deze pagina kunt u op verschillende manieren komen, ook vanuit de pagina **Alle zendingen**).
1. Open in het actievenster het tabblad **Zendingen** en selecteer **USMCA-certificaat van oorsprong** in de groep **Afdrukken**.
1. Het dialoogvenster **Certificaat of oorsprong** wordt geopend. Voer de instellingen in de volgende subsecties in en selecteer vervolgens **OK** om het document te genereren.
1. Er wordt een voorbeeld van het document wordt geopend. Gebruik de opdrachten in het actievenster om het document af te drukken of desgewenst te exporteren.

### <a name="certifying-party"></a>Certificerende partij

Gebruik de vervolgkeuzelijst **Certificerende partij** om het type partij te identificeren dat het document afdrukt. Geef op of de certificerende partij de *Exporteur*, *Exporteur en producent*, de *Producent* of de *Importeur* is of laat dit veld leeg als de certificerende partij geen van deze partijen is. De optie die u selecteert, bepaalt wat wordt afgedrukt in de adressecties van het document.

De **Certificerende partij** die u kiest, wordt in het afgedrukte document opgenomen.

Het document kan zowel voor inkomende als uitgaande zendingen worden afgedrukt. Selecteer *Importeur* als **Certificerende partij** alleen voor inkomende zendingen.

In de volgende tabel worden de typen gegevens beschreven die zijn opgenomen in het document op basis van de door u gekozen **Certificerende partij**.

| Certificerende&nbsp;partij | Beschrijving |
|---|---|
| *\[Leeg\]* | Voegt de volgende gegevens toe aan het document:<ul><li>**Gegevens van de certificerende partij**: de adresgegevens van het magazijn van verzending, indien beschikbaar, anders wordt het adres van de verzendlocatie gebruikt, indien beschikbaar, en anders wordt het adres gebruikt van de rechtspersoon (bedrijf) die is geselecteerd in Supply Chain Management.</li><li>**Gegevens exporteur**: leeg</li><li>**Gegevens producent**: leeg</li><li>**Gegevens importeur**: leeg</li><ul>|
| *Exporteur* | Voegt de volgende gegevens toe aan het document:<ul><li>**Gegevens van de certificerende partij**: de adresgegevens van het magazijn van verzending, indien beschikbaar, anders wordt het adres van de verzendlocatie gebruikt, indien beschikbaar, en anders wordt het adres gebruikt van de rechtspersoon (bedrijf) die is geselecteerd in Supply Chain Management.</li><li>**Gegevens exporteur** : gebruikt de adresgegevens voor de rechtspersoon.</li><li>**Gegevens producent**: leeg</li><li>**Gegevens importeur**: gebruikt de factuurrekening voor de gerelateerde verkooporder.</li><ul>|
| *Exporteur en producent* | Voegt de volgende gegevens toe aan het document:<ul><li>**Gegevens van de certificerende partij**: de adresgegevens van het magazijn van verzending, indien beschikbaar, anders wordt het adres van de verzendlocatie gebruikt, indien beschikbaar, en anders wordt het adres gebruikt van de rechtspersoon (bedrijf) die is geselecteerd in Supply Chain Management.</li><li>**Gegevens exporteur** : gebruikt de adresgegevens voor de rechtspersoon.</li><li>**Gegevens producent**: gebruikt de adresgegevens voor de rechtspersoon.</li><li>**Gegevens importeur**: gebruikt de factuurrekening voor de gerelateerde verkooporder.</li><ul>|
| *Importeur* | Voegt de volgende gegevens toe aan het document:<ul><li>**Gegevens van de certificerende partij**: de adresgegevens van het magazijn van verzending, indien beschikbaar, anders wordt het adres van de verzendlocatie gebruikt, indien beschikbaar, en anders wordt het adres gebruikt van de rechtspersoon (bedrijf) die is geselecteerd in Supply Chain Management.</li><li>**Gegevens exporteur**: leeg</li><li>**Gegevens producent**: leeg</li><li>**Gegevens importeur**: gebruikt de adresgegevens voor de rechtspersoon.</li><ul>|
| *Producent* | Voegt de volgende gegevens toe aan het document:<ul><li>**Gegevens certificerende partij**: gebruikt de adresgegevens van het magazijn van verzending, indien beschikbaar, anders wordt het adres van de verzendlocatie gebruikt, indien beschikbaar, en anders wordt het adres gebruikt van de rechtspersoon (bedrijf) die is geselecteerd in Supply Chain Management.</li><li>**Gegevens exporteur**: leeg</li><li>**Gegevens producent**: gebruikt de adresgegevens voor de rechtspersoon.</li><li>**Gegevens importeur**: leeg</li><ul>|

### <a name="has-various-producers"></a>Heeft verschillende producenten

Met de vervolgkeuzelijst **Certificerende partij** bepaalt u de tekst die moet worden gebruikt voor de producentgegevens in het document. Kies een van de volgende opties:

- *Diverse producenten*: drukt de tekst "diverse" af in de producentgegevens.
- *Beschikbaar op aanvraag*: drukt de tekst "beschikbaar op aanvraag bij de invoerautoriteit" af in de producentgegevens.

Wanneer **Certificerende partij** is ingesteld op *Exporteur en producent* of *Producent*, wordt de instelling van **Diverse producenten** overschreven en zijn de gegevens van het producentadres gelijk aan die van de certificerende partij.

### <a name="blanket-period"></a>Afroepperiode

Gebruik de instellingen **Afroepperiode van** en **Afroepperiode tot** om een afroepperiode op te geven, waarin het document meerdere zendingen van identieke goederen dekt, zelfs als het document slechts voor één zending wordt afgedrukt. U kunt de datums voor de afroepperiode instellen zonder beperkingen en de periode wordt aan het document toegevoegd. U kunt deze instellingen ook leeg laten of met datums in het verleden instellen.

### <a name="is-single-shipment"></a>Enkele zending

In het dialoogvenster **Certificaat van oorsprong** stelt u **Enkele zending** op een van de volgende opties in:

- *Ja*: voegt "enkele zending: ja" naast het factuurnummer.
- *Nee*: voegt niets toe.

## <a name="other-information-included-in-the-document"></a>Andere informatie die in het document is opgenomen

Naast de optionele elementen die u in het dialoogvenster **Certificaat of oorsprong** inschakelt, bevat het document voor het USMCA-certificaat van oorsprong de informatie en aangepaste velden die in de volgende subsecties worden samengevat. Een deel van deze informatie moet handmatig worden ingevoerd nadat u het document hebt gegenereerd.

### <a name="invoice-number"></a>Factuurnummer

De id's van verkoopfacturen die betrekking hebben op zendingen worden afgedrukt op het document, ongeacht de afroepperiode. Factuurnummers worden afgedrukt, ongeacht de optie die is geselecteerd voor **Enkele zending**.

### <a name="item-details"></a>Artikeldetails

Het document bevat diverse secties waarin specifieke artikelgegevens worden weergegeven:

- **SKU-nummer**: drukt het artikelnummer van het vrijgegeven product af.

- **Omschrijving**: drukt de omschrijving of naam af van het vrijgegeven product. Als er een omschrijving in de taal van de gebruiker bestaat, wordt deze afgedrukt. Als zo'n omschrijving niet bestaat, wordt de naam in de taal van de gebruiker afgedrukt. Als deze naam niet bestaat, wordt de artikelnaam afgedrukt.

- **Tariefclassificatie geharmoniseerd systeem (HS)**: drukt het geharmoniseerde tariefschema af dat aan het product is gekoppeld. U kunt deze schema's instellen door naar **Transportbeheer \> Instellingen \> Transportstandaard \> Geharmoniseerde tariefplanningen** te gaan.

- **Criterium van oorsprong:** u moet handmatig gegevens invoeren in deze sectie wanneer u het document voor de eerste keer vrijgeeft.

- **Land van oorsprong:** drukt het land van oorsprong af, dat u toepast door naar **Productgegevensbeheer \> Instellingen \> Productconformiteit \> Land van oorsprong** te gaan (zie ook [Land van oorsprong](../pim/country-of-origin.md)). De ISO-code voor het land van oorsprong wordt afgedrukt op basis van het land/de regio van bestemming in het leveringsadres van de zending en het artikel. Als er geen land van oorsprong is ingesteld, keert deze waarde terug naar de instelling die is gevonden bij **Vrijgegeven product \> Buitenlandse handel \> Oorsprong**. Als er geen gegevens van het land van oorsprong worden gevonden, moet u het land van oorsprong handmatig invoeren nadat u het document hebt gegenereerd.

### <a name="certifier-signature-and-date"></a>Handtekening van certificerende partij en datum

U moet dit handmatig invoeren nadat u het document hebt gegenereerd.

### <a name="consists-of-number-of-pages"></a>Bestaat uit aantal pagina's

De gebruiker die het certificaat ondertekent, moet het aantal pagina's (voor controle) handmatig invoeren nadat het document is gegenereerd.

### <a name="page-numbers"></a>Paginanummers

De huidige pagina en het aantal pagina's dat onder aan het document wordt afgedrukt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]