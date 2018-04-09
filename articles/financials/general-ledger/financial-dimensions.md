---
title: "Financiële dimensies"
description: "In dit onderwerp worden de verschillende typen financiële dimensies beschreven en hoe ze worden ingesteld."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Financiële dimensies

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de verschillende typen financiële dimensies uitgelegd en hoe ze worden ingesteld.

Gebruik de pagina **Financiële dimensies** om financiële dimensies te maken die u als rekeningsegmenten kunt gebruiken voor rekeningschema's. Er zijn twee typen financiële dimensies: aangepaste dimensies en door een entiteit ondersteunde dimensies. De aangepaste dimensies worden gedeeld door rechtspersonen en de waarden worden door gebruikers ingevoerd en onderhouden. Voor door een entiteit ondersteunde dimensies worden de waarden elders in het systeem gedefinieerd, zoals de entiteiten Klanten of Winkels. Bepaalde door entiteiten ondersteunde dimensies zijn verdeeld over rechtspersonen en sommige door entiteiten ondersteunde dimensies zijn bedrijfsspecifiek. 

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

Als u een door de gebruiker gedefinieerde financiële dimensie wilt maken, selecteert u in het veld **Waarden gebruiken van** **&lt; Aangepaste dimensie &gt;**. U kunt ook een opmaakmasker opgeven om de hoeveelheid en het type gegevens te beperken die u voor dimensiewaarden kunt invoeren. U kunt tekens, zoals letters of een koppelteken (-), invoeren die voor elke dimensiewaarde hetzelfde blijven. U kunt ook hekjes (\#) en en-tekens (&) invoeren die dienen als tijdelijke aanduidingen voor letters en cijfers die elke keer worden gewijzigd als een dimensiewaarde wordt gemaakt. Gebruik een hekje (\#) als tijdelijke aanduiding voor een cijfer en een en-teken (&) als tijdelijke aanduiding voor een letter. Het veld voor het opmaakmasker is alleen beschikbaar wanneer u **&lt; Aangepaste dimensie &gt;** selecteert in het veld **Waarden gebruiken van**.

**Voorbeeld**

Om de dimensiewaarde te beperken tot de letters "CC" en drie getallen, voert u **CC\#\#\#** als opmaakmasker in.

## <a name="entity-backed-dimensions"></a>Door een entiteit ondersteunde dimensies

Als u een door een entiteit ondersteunde financiële dimensie wilt maken, selecteert u in het veld **Waarden gebruiken van** een door het systeem gedefinieerde entiteit waarop de financiële dimensie moet worden gebaseerd. Waarden van financiële dimensies worden vervolgens op basis van die entiteit gemaakt. Als u bijvoorbeeld dimensiewaarden voor projecten wilt maken, selecteert u **Projecten**. Er wordt vervolgens voor elke projectnaam een dimensiewaarde gemaakt. Op de pagina **Waarden van financiële dimensies** worden de waarden voor de entiteit weergegeven. Als deze waarden specifiek voor het bedrijf zijn, wordt op de pagina ook het bedrijf weergegeven.

## <a name="activating-dimensions"></a>Dimensies activeren

Wanneer u een financiële dimensie activeert, wordt de tabel bijgewerkt om de naam van de financiële dimensie te bevatten. Verwijderde dimensies worden verwijderd. U kunt dimensiewaarden invoeren voordat u een financiële dimensie activeert. Een financiële dimensie kan echter pas ergens worden gebruikt als deze wordt geactiveerd. U kunt een financiële dimensie bijvoorbeeld pas toevoegen aan een rekeningstructuur als de financiële dimensie is geactiveerd. Wanneer u klikt op **Activeren**, worden alle dimensies bijgewerkt en worden statuswijzigingen weergegeven. 

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


Zie de volgende onderwerpen voor meer informatie:
- [Financiële dimensies definiëren](tasks/define-financial-dimensions.md)
- [Standaardsjablonen voor financiële dimensies onderhouden](tasks/maintain-financial-dimension-default-templates.md)

