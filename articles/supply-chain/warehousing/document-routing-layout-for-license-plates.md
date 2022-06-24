---
title: Indeling van documentroutering voor nummerplaatlabels
description: In dit artikel wordt beschreven hoe u opmaakmethoden kunt gebruiken om waarden op labels af te drukken.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 10e63353cda93d666d7f23f59508b73e5492c3cc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847870"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Indeling van documentroutering voor nummerplaatlabels

[!include [banner](../includes/banner.md)]


De indeling van de documentroutering bepaalt de indeling van nummerplaatlabels en de gegevens die erop worden afgedrukt. U configureert de afdruktriggerpunten wanneer u menuopdrachten voor mobiele apparaten en werksjablonen instelt.

In een normaal scenario drukken magazijnmedewerkers de nummerplaatlabels af nadat ze de inhoud hebben geregistreerd van pallets die in het ontvangstgebied binnenkomen. De fysieke labels worden op de pallets aangebracht. Ze kunnen dan worden gebruikt voor validatie in het opslagproces dat volgt en toekomstige uitgaande verzamelbewerkingen.

U kunt zeer complexe labels afdrukken, op voorwaarde dat de afdrukapparatuur de tekst kan interpreteren die wordt verzonden. Een ZPL-indeling (Zebra Programming Language) bevat een streepjescode die er bijvoorbeeld als volgt uitziet.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Als onderdeel van het afdrukproces wordt de tekst `$LicensePlateId$` in dit voorbeeld vervangen door een gegevenswaarde.

Als u de waarden wilt weergeven die worden afgedrukt, gaat u naar **Magazijnbeheer \> Query's en rapporten \> Nummerplaatlabels**.

Er zijn verschillende veelgebruikte hulpmiddelen voor het genereren van labels om helpen de tekst voor de labelindeling op te maken. Veel van deze hulpmiddelen ondersteunen de `$FieldName$`-indeling. Daarnaast gebruikt Microsoft Dynamics 365 Supply Chain Management speciale opmaaklogica als onderdeel van de veldtoewijzing voor de indeling van de documentroutering.

## <a name="turn-on-this-feature-for-your-system"></a>Deze functie inschakelen voor uw systeem

Als de functies die in dit artikel worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Verbeterde indelingen voor nummerplaatlabels* in. (Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld.)

## <a name="custom-number-formats"></a>Aangepaste getalnotaties

U kunt de opmaak van numerieke veldwaarden die worden afgedrukt aanpassen met behulp van codes die de volgende notatie hebben.

```dos
$FieldName:FormatString$
```

Hier volgt een uitleg van deze opmaak:

- `FieldName` is de naam van het gegevensveld (bijvoorbeeld **Hoeveelheid**).
- `FormatString` definieert hoe de gegevens moeten worden afgedrukt.

De volgende voorbeelden laten zien hoe u het veld met de werkhoeveelheid(**Hoeveelheid**) kunt aanpassen:

- Als u altijd vier cijfers wilt weergeven (met nullen als tijdelijke aanduidingen ), gebruikt u `$Qty:0000$`. Als de hoeveelheid bijvoorbeeld 10 is, wordt in het label "0010" weergegeven.
- Gebruik `$Qty:0.00$` om altijd twee decimalen weer te geven. Als de hoeveelheid bijvoorbeeld 10 is, wordt in het label "10,00" weergegeven.

Zie [Aangepaste numerieke tekenreeksen](/dotnet/standard/base-types/custom-numeric-format-strings) voor een volledige lijst met de beschikbare notatiereeksen voor getallen.

## <a name="custom-string-formats"></a>Aangepaste tekenreeksen

U kunt de eerste tekens van een tekenreeks verwijderen met de volgende velden en opmaakcode.

```dos
$FieldName:#..$
```

Hier geeft `#` het aantal tekens op dat u wilt overslaan. Als u bijvoorbeeld een SSCC-nummerplaatnummer (Serial Shipping Container Code) wilt afdrukken, waarin de eerste twee tekens niet zijn opgenomen, gebruikt u `$LicensePlateId:2..$`. In dat geval wordt het nummerplaatnummer 0011111111111222221 afgedrukt als "11111111111222221".

## <a name="custom-datetime-formats"></a>Aangepaste datum- en tijdnotaties

In het volgende voorbeeld ziet u hoe u de indeling instelt die wordt gebruikt om datums af te drukken.

```dos
$PrintedDate:dd-MM-yyyy$
```

In dit voorbeeld wordt de datum 30 april 2020 afgedrukt als "30-04-2020".

Zie [Aangepaste reeksen voor datum en tijd](/dotnet/standard/base-types/custom-date-and-time-format-strings) voor een volledige lijst met de beschikbare notatiereeksen voor datum/tijd.

## <a name="print-individual-lines-from-multiline-data"></a>Afzonderlijke regels uit gegevens met meerdere regels afdrukken

Als een gegevensveld meerdere regels bevat (dat wil zeggen regels die zijn gescheiden door regeleinden), kunt u een afzonderlijke regel afdrukken met de volgende notatie.

```dos
$FieldName[#]$
```

Hier is `#` het regelnummer dat u wilt afdrukken. (Gebruik 1 voor de eerste regel.)

Het systeem heeft bijvoorbeeld een veld `AdditionalAddress` waarin het volgende adres met meerdere regels wordt opgeslagen:

Contoso Inc.  
Straatnaam 123  
Een plaats, een provincie

U kunt dit adres met één regel per keer afdrukken met de volgende codes.

| Code | Tekst die wordt afgedrukt |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | Straatnaam 123 |
| `$AdditionalAddress[3]$` | Een plaats, een provincie |

## <a name="print-and-format-from-a-display-method"></a>Afdrukken en opmaken vanuit een weergavemethode

U kunt afdrukken vanuit een weergavemethode met de volgende notatie.

```dos
$DisplayMethod()$
```

U kunt deze notatie combineren met andere typen die eerder in dit artikel zijn beschreven. U hebt bijvoorbeeld een weergavemethode met de naam `DisplayListOfItemsNumbers()` en u wilt het eerste artikelnummer van deze methode afdrukken. In dit geval kunt u de volgende code gebruiken.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Meer informatie over het afdrukken van labels

Zie [Afdrukken van nummerplaatlabel inschakelen](tasks/license-plate-label-printing.md) voor meer informatie over het instellen en afdrukken van labels.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]