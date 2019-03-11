---
title: Financiële dimensies
description: In dit onderwerp worden de verschillende typen financiële dimensies beschreven en hoe ze worden ingesteld.
author: aprilolson
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ems.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 2fb325e143eff067e1c9d0f23a1f913fc2dc36f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "317540"
---
# <a name="financial-dimensions"></a>Financiële dimensies

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld.

Gebruik de pagina **Financiële dimensies** om financiële dimensies te maken die u als rekeningsegmenten kunt gebruiken voor rekeningschema's. Er zijn twee typen financiële dimensies: aangepaste dimensies en door een entiteit ondersteunde dimensies. De aangepaste dimensies worden gedeeld door rechtspersonen en de waarden worden door gebruikers ingevoerd en onderhouden. Voor door een entiteit ondersteunde dimensies worden de waarden elders in het systeem gedefinieerd, zoals in de entiteiten Klanten of Winkels. Bepaalde door entiteiten ondersteunde dimensies zijn verdeeld over rechtspersonen en sommige door entiteiten ondersteunde dimensies zijn bedrijfsspecifiek.

Nadat u de financiële dimensies hebt gemaakt, gebruikt u de pagina **Waarden van financiële dimensie** om aanvullende eigenschappen toe te wijzen aan elke financiële dimensie.

U kunt financiële dimensies gebruiken om rechtspersonen te vertegenwoordigen. U hoeft de rechtspersonen niet te maken in Microsoft Dynamics 365 for Finance and Operations. Financiële dimensies zijn echter niet bedoeld om te voldoen aan operationele of zakelijke behoeften van rechtspersonen. De boekhouding tussen eenheden-functie in Finance and Operations is ontworpen om alleen met de boekhoudkundige vermeldingen te werken die door de transactie worden gemaakt.

Voordat u de financiële dimensies instelt als rechtspersonen, moet u uw bedrijfsprocessen evalueren in de volgende gebieden om te bepalen of deze instelling zal werken voor uw organisatie:

- Voorraad
- Verkoop en inkoop tussen financiële dimensies en rechtspersonen
- Btw-berekening en rapportage
- Operationele rapporteren

Hieronder vindt u enkele beperkingen:

- U kunt de btw-functionaliteit alleen gebruiken met rechtspersonen, niet met financiële dimensies.
- Sommige rapporten bevatten geen financiële dimensies. Als u op basis van financiële dimensie wilt rapporteren, moet u dus mogelijk de rapporten wijzigen.

## <a name="custom-dimensions"></a>Aangepaste dimensies

Als u een door de gebruiker gedefinieerde financiële dimensie wilt maken, selecteert u **Aangepaste dimensie** in het veld **Waarden gebruiken van**.

U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die voor dimensiewaarden kunnen worden ingevoerd. U kunt tekens, zoals letters of een koppelteken (-), invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt ook hekjes (\#) en en-tekens (&) invoeren die dienen als tijdelijke aanduidingen voor tekens die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt. Gebruik een hekje (\#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter. Het veld voor het opmaakmasker is alleen beschikbaar wanneer u **Aangepaste dimensie** selecteert in het veld **Waarden gebruiken van**.

**Voorbeeld**

Om de dimensiewaarde te beperken tot de letters "CC" en drie getallen, voert u **CC\#\#\#** als opmaakmasker in.

## <a name="entity-backed-dimensions"></a>Door een entiteit ondersteunde dimensies

Als u een door een entiteit ondersteunde financiële dimensie wilt maken, selecteert u in het veld **Waarden gebruiken van** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd. Waarden van financiële dimensies worden vervolgens op basis van die entiteit gemaakt. Als u bijvoorbeeld dimensiewaarden voor projecten wilt maken, selecteert u **Projecten**. Er wordt vervolgens voor elke projectnaam een dimensiewaarde gemaakt. Op de pagina **Waarden van financiële dimensies** worden de waarden voor de entiteit weergegeven. Als deze waarden specifiek voor het bedrijf zijn, wordt op de pagina ook het bedrijf weergegeven.

## <a name="activating-dimensions"></a>Dimensies activeren

Wanneer u een financiële dimensie activeert, wordt de tabel bijgewerkt om de naam van de financiële dimensie te bevatten. Verwijderde dimensies worden verwijderd. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert. Een financiële dimensie kan echter pas ergens worden gebruikt als deze wordt geactiveerd. U kunt een financiële dimensie bijvoorbeeld pas toevoegen aan een rekeningstructuur als de financiële dimensie is geactiveerd. Wanneer u **Activeren** selecteert, worden alle dimensies bijgewerkt en worden statuswijzigingen weergegeven.

## <a name="translations"></a>Taalteksten

Op de pagina **Tekstvertaling** kunt u tekst invoeren voor de geselecteerde financiële dimensie in verschillende talen. Op de pagina **Vertaling hoofdrekening** kunt u tekst invoeren voor de hoofdrekening in verschillende talen. 

## <a name="legal-entity-overrides"></a>Overschrijvingen rechtspersoon

Niet alle dimensies zijn geldig voor alle rechtspersonen. Daarnaast zijn sommige dimensies mogelijk alleen relevant voor een bepaalde periode. In deze gevallen kunt u de sectie **Overschrijvingen rechtspersoon** gebruiken om de bedrijven op te geven waarvoor de dimensie moet worden opgeschort, wie de eigenaar is en gedurende welke periode de dimensie actief is.

## <a name="deleting-financial-dimensions"></a>Financiële dimensies verwijderen

Om de referentiële integriteit van de gegevens te helpen waarborgen, kunnen financiële dimensies zelden worden verwijderd. Als u een financiële dimensie probeert te verwijderen, worden de volgende criteria geëvalueerd:

- Is de financiële dimensie gebruikt in geboekte of niet-geboekte transacties of een willekeurig type dimensiewaardecombinatie?
- Wordt de financiële dimensie gebruikt in een actieve rekeningstructuur, geavanceerde regelstructuur of set met financiële dimensies?
- Maakt de financiële dimensie deel uit van een standaardindeling voor de integratie van financiële dimensies?
- Is de financiële dimensie ingesteld als een standaarddimensie?

Als aan een van de criteria wordt voldaan, kunt u de financiële dimensie niet verwijderen.

## <a name="default-dimension-values"></a>Waarden standaarddimensie

U kunt waarden uit hoofdrecords, zoals klanten en leveranciers, als standaardwaarden gebruiken in nieuwe dimensies. Wanneer de nieuwe dimensies worden gemaakt, wordt de hoofdrecord-id in de dimensiewaarden ingevoerd voor deze hoofdrecords. Wanneer u een nieuwe klant maakt, wordt de klant-id bijvoorbeeld ingevoerd in de klantdimensie. Wanneer u verkooporders, facturen of andere documenten maakt waarvoor u een klant-id nodig hebt, worden de bestaande standaardregels gebruikt en wordt de klant-id toegevoegd aan het document.

Deze functie is gekoppeld aan een instelling in de dimensie. De naam van deze instelling is **Kopieer waarden naar deze dimensie op elk nieuw gemaakte DimensionName**, waarbij **DimensionName** de naam van de dimensie is. De functie is standaard uitgeschakeld. Deze kan op elk gewenst moment worden ingeschakeld.

Als er al records bestaan voor de dimensie, worden de hoofdrecords bijgewerkt wanneer u de functie inschakelt. Bestaande documenten en transacties worden echter niet bijgewerkt.

Als u een sjabloon gebruikt om een hoofdrecord te maken, moet u ervoor zorgen dat de sjabloonwaarde voor de hoofddimensie leeg is. Als u klanten op basis van een sjabloon maakt, moet u er bijvoorbeeld voor zorgen dat klantdimensie in de sjabloon leeg is. De klantdimensiewaarde wordt standaard ingesteld op basis van het nieuwe klantnummer wanneer u de nieuwe klant maakt.  

## <a name="derived-dimensions"></a>Afgeleide dimensies

U kunt een dimensie zo configureren dat gegevens voor andere dimensies automatisch worden ingevoerd wanneer u die dimensie in een document invoert. Als u kostenplaats 10 invoert, kan bijvoorbeeld automatisch een waarde van **20** worden ingevoerd in de afdelingsdimensie.

U kunt afgeleide waarden instellen op de pagina Dimensies.

1. Selecteer een dimensie en selecteer vervolgens **Afgeleide dimensies**.

    De pagina **Afgeleide dimensies** bevat een raster. Het geselecteerde dimensiesegment is de eerste kolom in dit raster.

2. Voeg de segmenten toe die moeten worden afgeleid. Elk segment wordt weergegeven als een kolom.

Voer de dimensiecombinaties in die moeten worden afgeleid van de dimensie in de eerste kolom. Als u de kostenplaats wilt gebruiken als de dimensie waarvan de afdeling en locatie moeten worden afgeleid, voert u bijvoorbeeld kostenplaats 10, afdeling 20 en locatie 30 in. Wanneer u vervolgens kostenplaats 10 invoert in een hoofdrecord of op een transactiepagina, worden afdeling 20 en locatie 30 standaard ingevoerd.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Bestaande waarden overschrijven met afgeleide dimensies
 
Het afgeleide dimensieproces overschrijft standaard bestaande waarden niet voor afgeleide dimensies. Als u kostenplaats 10 invoert en er geen andere dimensie wordt ingevoerd, worden afdeling 20 en locatie 30 standaard ingevoerd. Als u de kostenplaats wijzigt, worden de waarden die al zijn ingevoerd niet meer gewijzigd. Daarom kunt u standaarddimensies voor hoofdrecords maken. Deze dimensies worden niet gewijzigd door afgeleide dimensies.

U kunt de werking van afgeleide dimensies om bestaande waarden te overschrijven wijzigen door het selecteren van het selectievakje **Bestaande dimensiewaarden vervangen door afgeleide waarden** op de pagina **Afgeleide dimensies**. Als dit veld is geselecteerd, kunt u een dimensie met afgeleide dimensiewaarden invoeren en overschrijven deze afgeleide dimensiewaarden alle waarden die al bestaan. Als u in het vorige voorbeeld bijvoorbeeld kostenplaats 10 invoert en er geen andere dimensie wordt ingevoerd, worden afdeling 20 en locatie 30 standaard ingevoerd. Echter, als de waarden al afdeling 50 en locatie 60 waren, worden de waarden nu gewijzigd in afdeling 20 en locatie 30.
 
Afgeleide dimensies met deze instelling vervangen niet automatisch de bestaande standaardwaarden voor dimensies wanneer standaardwaarden voor dimensies worden gebruikt. Dimensiewaarden worden alleen overschreven wanneer u een nieuwe dimensiewaarde op een pagina invoert en er bestaande afgeleide waarden voor die dimensie op de pagina zijn.

### <a name="preventing-changes-with-derived-dimensions"></a>Wijzigingen met afgeleide dimensies voorkomen
 
Als u **Segment toevoegen** gebruikt op de **pagina Afgeleide dimensies** om een segment toe te voegen als een afgeleide dimensie, is er onder aan de pagina **Segment toevoegen** een optie waarmee u wijzigingen in die dimensie kunt voorkomen wanneer deze op een pagina wordt afgeleid. De standaardinstelling is uitgeschakeld, zodat niet wordt voorkomen dat de afgeleide dimensiewaarden worden gewijzigd. Wijzig de instelling in **Ja** als u wilt voorkomen dat de dimensie wordt gewijzigd nadat deze is afgeleid. Als de waarde voor de dimensie Afdeling bijvoorbeeld is afgeleid van de waarde van de dimensie Kostenplaats, kan de waarde van Afdeling niet worden gewijzigd als de instelling **Wijzigingen voorkomen** **Ja** is. 
 
De instelling voorkomt geen wijzigingen als de dimensiewaarde geldig is, maar deze niet wordt vermeld in de lijst met afgeleide dimensies. Als Afdeling 20 bijvoorbeeld is afgeleid van Kostenplaats 10 en u Kostenplaats 10 invoert, kunt u Afdeling 20 niet bewerken. Als u echter Kostenplaats 20 invoert en dit is niet in de lijst van afgeleide dimensies voor de kostenplaats staat, kunt u de waarde Afdeling wel bewerken. 
 
In alle gevallen worden de rekeningwaarde en alle dimensiewaarden nog steeds gevalideerd tegen de rekeningstructuren nadat de afgeleide dimensiewaarden zijn toegepast. Als u afgeleide dimensies gebruikt en de validatie ervan mislukt wanneer ze op een pagina worden gebruikt, moet u de afgeleide dimensiewaarden op de pagina met afgeleide dimensies wijzigen voordat u ze in transacties kunt gebruiken. 
 
Wanneer u dimensies wijzigt op het sneltabblad **Financiële dimensies**, is de dimensie die is gemarkeerd om wijzigingen te voorkomen, niet bewerkbaar. Als u een rekening en dimensies in het besturingselement met gesegmenteerde invoer invoert op een pagina, zijn de dimensies bewerkbaar. Wanneer u echter de markering uit het besturingselement voor gesegmenteerde invoer verplaatst en naar een ander veld gaat of een actie uitvoert, worden de rekening en de dimensies gevalideerd tegen de lijst met afgeleide dimensies en de rekeningstructuren om te zorgen dat u de juiste waarden hebt ingevoerd. 

### <a name="derived-dimensions-and-entities"></a>Afgeleide dimensies en entiteiten

U kunt de segmenten en waarden van afgeleide dimensies instellen met behulp van entiteiten.

- Met de entiteit Afgeleide dimensies configureert u de aansturende dimensies en de segmenten die worden gebruikt voor deze dimensies.
- Met de entiteit Afgeleide dimensiewaarde kunt u de waarden importeren die moeten worden afgeleid voor elke aansturende dimensie.

Wanneer u een entiteit gebruikt om gegevens te importeren en er met die entiteit dimensies worden geïmporteerd, worden de afgeleide dimensieregels toegepast tijdens het importeren, tenzij de entiteit die dimensies specifiek overschrijft.

Zie de volgende onderwerpen voor meer informatie:

- [Financiële dimensies definiëren](tasks/define-financial-dimensions.md)
- [Standaardsjablonen voor financiële dimensies onderhouden](tasks/maintain-financial-dimension-default-templates.md)
