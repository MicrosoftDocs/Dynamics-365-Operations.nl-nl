---
title: Activa aanschaffen via inkoop
description: In dit artikel wordt beschreven hoe u de integratie instelt tussen Vaste activa en Leveranciers om automatisch vaste activa van inkooporders of leveranciersfacturen te maken of om automatisch verwervings- en verwervingscorrectietransacties voor vaste activa te boeken.
author: moaamer
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac25114fe8036a474d637e9ad9ede5e46b50d92e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891575"
---
# <a name="acquire-assets-through-procurement"></a>Activa aanschaffen via inkoop

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de integratie instelt tussen Vaste activa en Leveranciers om automatisch vaste activa van inkooporders of leveranciersfacturen te maken of om automatisch verwervings- en verwervingscorrectietransacties voor vaste activa te boeken. Met één inkoopregel wordt één activum gemaakt, ongeacht de hoeveelheid op de inkoopregel. Als u meerdere vaste activa moet maken, moet u meerdere inkoopregels maken.

 De volgende methoden zijn beschikbaar voor het integreren van Vaste activa en Leveranciers, en u moet dezelfde methode gebruiken voor alle vaste activa:
-   U maakt handmatig een vast activum voordat u het vast-activumnummer toevoegt aan de regel op de inkooporder of leveranciersfactuur. Er wordt automatisch een verwervingstransactie geboekt voor het activum wanneer u de leveranciersfactuur boekt. Dit is de standaardmethode.
-   U maakt handmatig een vast activum voordat u het vast-activumnummer toevoegt aan de regel op de inkooporder of leveranciersfactuur. Wanneer u de leveranciersfactuur boekt, wordt er geen bijboekingstransactie voor de activa geboekt.
-   Er wordt automatisch een vast activum gemaakt wanneer u een productontvangstbon of leveranciersfactuur boekt waarvoor het selectievakje Nieuwe vaste activa maken is ingeschakeld. Er wordt automatisch een verwervingstransactie geboekt voor het activum wanneer u de leveranciersfactuur boekt.
-   Er wordt automatisch een vast activum gemaakt wanneer u een productontvangstbon of leveranciersfactuur boekt waarvoor het selectievakje Nieuwe vaste activa maken is ingeschakeld. Wanneer u de leveranciersfactuur boekt, wordt er geen bijboekingstransactie voor de activa geboekt.

Kies een van de eerste twee methoden als u vaste activa liever handmatig maakt en aansluitend het nummer van de vaste activa aan de inkooporder of leveranciersfactuur wilt toewijzen. Kies een van de laatste twee methoden als u zelf wilt bepalen wat u wilt doen. Soms wilt u vaste activa handmatig maken en soms wilt u een vast activum automatisch laten maken op basis van de gegevens van de vaste activa op de regelitemdetails. 

Of u nu handmatig vaste activa maakt of de meer flexibele aanpak kiest, u moet eveneens beslissen of een verwervingstransactie alleen in Vaste activa kan worden geboekt of dat deze kan worden geboekt wanneer u een leveranciersfactuur boekt. In sommige organisaties wil men dat verwervingen en verwervingstransacties met behulp van handmatige boekingen in journaal of voorstellen handmatig in Vaste activa worden gemaakt. 

In dit artikel wordt elke methode uitgelegd.

## <a name="methods-for-manually-creating-fixed-assets"></a>Methoden voor handmatig vaste activa maken
Wanneer u een leveranciersfactuur boekt waarvoor het nummer van een vast activum in de regels is ingevoerd, en de optie Bijboekingen van activa vanuit Inkoop toestaan is geselecteerd op de pagina Parameters voor vaste activa, wordt de verwerving automatisch geboekt en verandert de status van het activum in Openstaand. 

Als een verwerving niet kan worden geboekt, kunt u een verwervingstransactie handmatig in Vaste activa invoeren of met een verwervingsvoorstel in het journaal Vaste activa meerdere verwervingstransacties tegelijk maken.

> [!NOTE]                                                                                                                              
> Als vaste activa zo zijn ingesteld dat verwervingstransacties alleen door een bepaalde gebruikersgroep kunnen worden geboekt, moet u lid van die gebruikersgroep zijn om verwervingstransacties van facturen te kunnen boeken.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Methoden voor automatisch vaste activa maken
Wanneer u een productontvangstbon boekt waarvoor de optie Nieuwe vaste activa maken is geselecteerd voor een regel, wordt er een nieuw vast activum gemaakt met de status Nog niet bijgeboekt. Boekt u vervolgens een leveranciersfactuur met een nieuw vast activum, dan wordt er een verwervingstransactie voor het nieuwe activum geboekt en verandert de status van het activum in Openstaand als de vaste activa zo zijn ingesteld dat vanuit Leveranciers activa mogen worden bijgeboekt en u lid bent van een gebruikersgroep die verwervingstransacties mag boeken. 

Als de optie Nieuw vast activum? niet was geselecteerd op de inkoopregel toen u de productontvangstbon boekte maar wel was geselecteerd toen u de leveranciersfactuur boekte, wordt het nieuwe vaste activum gemaakt en bijgeboekt met de status Openstaand, als de vaste activa zijn ingesteld voor maken en bijboeken. Er wordt geen extra activum gemaakt wanneer u een leveranciersfactuur boekt als er al een activum was gemaakt toen u de productontvangstbon boekte.

### <a name="capitalization-threshold"></a>Drempel voor kapitalisatie

Wanneer u een methode gebruikt waarbij het activum automatisch wordt gemaakt en bijgeboekt, kunt u het systeem zo instellen dat wordt gecontroleerd of het inkoopbedrag van het vaste activum voldoet aan de kapitalisatiedrempel voor de afschrijving van vaste activa. In dat geval is de optie Afschrijving ingeschakeld in de boeken voor het activum wanneer dat vanuit Leveranciers wordt gemaakt. 

Een kapitalisatiedrempel is een geldbedrag waarmee wordt bepaald of activa worden afgeschreven als zij aan een bepaald bedrag voldoen. Als u bijvoorbeeld een activum aanschaft waarvan het bedrag lager is dan de kapitalisatiedrempel, komt het activum niet in aanmerking om te worden afgeschreven. Is het bedrag van dat activum gelijk aan of hoger dan de kapitalisatiedrempel, dan komt het activum in aanmerking om te worden afgeschreven. 

U kunt de kapitalisatiedrempel instellen op de pagina Vaste-activagroepen.

## <a name="scenario"></a>Scenario
Aan de hand van het volgende scenario wordt een volledige integratiecyclus van vaste activa en leveranciers besproken. Er wordt een voorbeeld gegeven en het gebruik van bijboekingsvoorstellen wordt uitgelegd. 

In dit scenario wordt het systeem als volgt opgezet:

-   Activa worden automatisch gemaakt tijdens het boeken van een productontvangstbon of leveranciersfactuur, maar de vaste activa worden zo ingesteld dat er geen bijboekingstransacties vanuit Leveranciers kunnen worden geboekt.
-   De rekeningen worden opgegeven in het veld Rekeningtype voor de rekeningtypen Ontvangst van vaste activa en Uitgifte van vaste activa op de pagina Artikelengroepen.
-   De kapitalisatiedrempel voor de computersgroep (COMP) is 1500.
-   U moet een inkooporder voor een nieuwe laptop voor een werknemer invoeren, de inkooporder boeken, controleren of de desbetreffende expeditiemedewerker een productontvangstbon boekt, de leveranciersfactuur boeken en vervolgens controleren of de boekhouder de status van het bestelde activum 'laptop' op Openstaand heeft gezet.

Als eerste voert u op de pagina Inkooporder de gegevens voor de laptop in, die 1600 euro kost. U selecteert de optie Nieuw vast activum? op het sneltabblad Vaste activa van de inkooporderregels, selecteert COMP als de vaste-activagroep en slaat de inkooporder op. 

Wanneer de laptop binnen is, voert de expeditiemedewerker de productontvangstbon in en boekt deze om de ontvangst van de laptop te registreren. Het activum 'laptop' wordt gemaakt en heeft de status Nog niet bijgeboekt. Het bedrag overschrijdt de kapitalisatiedrempel. De optie Afschrijving is dus ingeschakeld in de boeken voor het activum 'laptop'. De volgende transacties worden uitgevoerd.

| Omschrijving                               | Rekening             | Debet    | Credit   |
|-------------------------------------------|---------------------|----------|----------|
| Inkoop, productontvangstbon van inkoop        | Niet-gefactureerde ontvangsten | 1.600,00 |          |
| Inkoop, tegenrekening productontvangstbon inkoop | Toegerekende kosten   |          | 1.600,00 |

Vervolgens boekt u de leveranciersfactuur voor de laptop. De laptopstatus wordt niet gewijzigd, omdat vaste activa zo zijn ingesteld dat wordt voorkomen dat een activumverwervingstransactie wordt geboekt wanneer een leveranciersfactuur wordt geboekt. De optie Nieuwe vaste activa maken werd geselecteerd wanneer de leveranciersfactuur werdt geboekt. Daarom werd de rekening Ontvangst van vaste activa gebruikt. De rekening Uitgifte van vaste activa werd niet gebruikt omdat er geen bijboeking heeft plaatsgevonden. Deze wordt later gebruikt wanneer de boekhouder van uw organisatie met behulp van verwervingsvoorstellen een verwervingstransactie in Vaste activa boekt. 

De volgende transacties worden uitgevoerd.

| Omschrijving                               | Rekening             | Debet    | Credit   |
|-------------------------------------------|---------------------|----------|----------|
| Inkoop, tegenrekening productontvangstbon inkoop | Toegerekende kosten   | 1.600,00 |          |
| Leveranciersaldo                            | Leveranciers    |          | 1.600,00 |
| Inkoop, ontvangst van vaste activa             | Onkosten computer    | 1.600,00 |          |
| Inkoop, productontvangstbon van inkoop        | Niet-gefactureerde ontvangsten |          | 1.600,00 |

Tot slot bekijkt de boekhouder alle vaste activa met de status Nog niet bijgeboekt. Het nieuwe activum 'laptop' wordt daarom beoordeeld. De boekhouder opent vervolgens de pagina Bijboekingsvoorstel vanuit de journaalregels Vaste activa en maakt verwervingstransacties voor alle activa die een factuur maar ook nog steeds de status Nog niet bijgeboekt hebben. Wanneer het journaal wordt geboekt, wordt de status van het activum 'laptop' gewijzigd in Openstaand. De rekening Uitgifte van vaste activa wordt gecrediteerd en de rekening voor het bijboeken van activa wordt gedebiteerd. 

Hieronder vindt u enkele varianten voor dit scenario:

-   Als vaste activa zo zijn ingesteld dat bijboekingstransacties voor activa worden geboekt wanneer leveranciersfacturen worden geboekt, hoeft de boekhouder geen bijboekingsvoorstellen in Vaste activa te gebruiken omdat de bijboekingstransactie wordt gemaakt. Ook worden er verschillende rekeningen bijgewerkt wanneer u de leveranciersfactuur boekt. In plaats van Onkosten computer, is de voorraadrekening Ontvangst van vaste activa gedebiteerd en worden twee extra transacties uitgevoerd: de rekening voor het bijboeken van activa wordt gedebiteerd en de voorraadrekening Uitgifte van vaste activa wordt gecrediteerd.
-   Als de optie Nieuwe vaste activa maken niet is geselecteerd wanneer de productontvangstbon wordt geboekt, wordt er op dat moment geen activum gemaakt. Als u de optie Nieuwe vaste activa maken selecteert en dan de leveranciersfactuur boekt, wordt het activum gemaakt met de status Nog niet bijgeboekt of met de status Openstaand als u ook verwervingstransacties boekt wanneer er leveranciersfacturen worden geboekt.
-   Als de laptop 1400 en geen 1600 euro kost, wordt de kapitalisatiedrempel niet bereikt. Het activum wordt dus gemaakt en de optie Afschrijving wordt gewist.
-   Als er een facturenregister wordt gebruikt en het facturenregister is geboekt, gebruikt u de pagina Factuurgoedkeuringsjournaal om het boekstuk op te halen, de inkooporder aan de leveranciersfactuur te koppelen, de optie Nieuwe vaste activa maken te selecteren en vervolgens de leveranciersfactuur te boeken. Als u lid bent van een gebruikersgroep die bijboekingstransacties mag maken, wordt de bijboeking gemaakt en heeft het activum de status Openstaand.
-   Als er slechts een deel van de hoeveelheid is ontvangen, wordt er vanwege de beperkingen van de gebruikersgroep geen activabijboeking voor de eerste leveranciersfactuur gemaakt. De enige manier waarop een bijboeking voor de tweede leveranciersfactuur van de bestelde hoeveelheid kan worden geboekt, is wanneer er al een bijboekingstransactie voor de eerste leveranciersfactuur is ingevoerd en u lid bent van de gebruikersgroep die bijboekingen kan boeken.


Zie [Integratie vaste activa](fixed-asset-integration.md) voor meer informatie.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
