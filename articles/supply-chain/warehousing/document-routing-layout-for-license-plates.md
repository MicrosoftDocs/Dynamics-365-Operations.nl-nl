---
title: Indeling van documentroutering voor nummerplaatlabels
description: In dit onderwerp wordt beschreven hoe u opmaakmethoden kunt gebruiken om waarden op labels af te drukken.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 7c20d3d0540f8f1a05928df9aff5253745982da9
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558257"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="8e500-103">Indeling van documentroutering voor nummerplaatlabels</span><span class="sxs-lookup"><span data-stu-id="8e500-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8e500-104">De indeling van de documentroutering bepaalt de indeling van nummerplaatlabels en de gegevens die erop worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="8e500-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="8e500-105">U configureert de afdruktriggerpunten wanneer u menuopdrachten voor mobiele apparaten en werksjablonen instelt.</span><span class="sxs-lookup"><span data-stu-id="8e500-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="8e500-106">In een normaal scenario drukken magazijnmedewerkers de nummerplaatlabels af nadat ze de inhoud hebben geregistreerd van pallets die in het ontvangstgebied binnenkomen.</span><span class="sxs-lookup"><span data-stu-id="8e500-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="8e500-107">De fysieke labels worden op de pallets aangebracht.</span><span class="sxs-lookup"><span data-stu-id="8e500-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="8e500-108">Ze kunnen dan worden gebruikt voor validatie in het opslagproces dat volgt en toekomstige uitgaande verzamelbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="8e500-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="8e500-109">U kunt zeer complexe labels afdrukken, op voorwaarde dat de afdrukapparatuur de tekst kan interpreteren die wordt verzonden.</span><span class="sxs-lookup"><span data-stu-id="8e500-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="8e500-110">Een ZPL-indeling (Zebra Programming Language) bevat een streepjescode die er bijvoorbeeld als volgt uitziet.</span><span class="sxs-lookup"><span data-stu-id="8e500-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

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

<span data-ttu-id="8e500-111">Als onderdeel van het afdrukproces wordt de tekst `$LicensePlateId$` in dit voorbeeld vervangen door een gegevenswaarde.</span><span class="sxs-lookup"><span data-stu-id="8e500-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="8e500-112">Als u de waarden wilt weergeven die worden afgedrukt, gaat u naar **Magazijnbeheer \> Query's en rapporten \> Nummerplaatlabels**.</span><span class="sxs-lookup"><span data-stu-id="8e500-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="8e500-113">Er zijn verschillende veelgebruikte hulpmiddelen voor het genereren van labels om helpen de tekst voor de labelindeling op te maken.</span><span class="sxs-lookup"><span data-stu-id="8e500-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="8e500-114">Veel van deze hulpmiddelen ondersteunen de `$FieldName$`-indeling.</span><span class="sxs-lookup"><span data-stu-id="8e500-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="8e500-115">Daarnaast gebruikt Microsoft Dynamics 365 Supply Chain Management speciale opmaaklogica als onderdeel van de veldtoewijzing voor de indeling van de documentroutering.</span><span class="sxs-lookup"><span data-stu-id="8e500-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="8e500-116">Deze functie inschakelen voor uw systeem</span><span class="sxs-lookup"><span data-stu-id="8e500-116">Turn on this feature for your system</span></span>

<span data-ttu-id="8e500-117">Als de functies die in dit onderwerp worden beschreven, nog niet in het systeem aanwezig zijn, gaat u naar [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Verbeterde indelingen voor nummerplaatlabels* in.</span><span class="sxs-lookup"><span data-stu-id="8e500-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="8e500-118">Aangepaste getalnotaties</span><span class="sxs-lookup"><span data-stu-id="8e500-118">Custom number formats</span></span>

<span data-ttu-id="8e500-119">U kunt de opmaak van numerieke veldwaarden die worden afgedrukt aanpassen met behulp van codes die de volgende notatie hebben.</span><span class="sxs-lookup"><span data-stu-id="8e500-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="8e500-120">Hier volgt een uitleg van deze opmaak:</span><span class="sxs-lookup"><span data-stu-id="8e500-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="8e500-121">`FieldName` is de naam van het gegevensveld (bijvoorbeeld **Hoeveelheid**).</span><span class="sxs-lookup"><span data-stu-id="8e500-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="8e500-122">`FormatString` definieert hoe de gegevens moeten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="8e500-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="8e500-123">De volgende voorbeelden laten zien hoe u het veld met de werkhoeveelheid(**Hoeveelheid**) kunt aanpassen:</span><span class="sxs-lookup"><span data-stu-id="8e500-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="8e500-124">Als u altijd vier cijfers wilt weergeven (met nullen als tijdelijke aanduidingen ), gebruikt u `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="8e500-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="8e500-125">Als de hoeveelheid bijvoorbeeld 10 is, wordt in het label "0010" weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8e500-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="8e500-126">Gebruik `$Qty:0.00$` om altijd twee decimalen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8e500-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="8e500-127">Als de hoeveelheid bijvoorbeeld 10 is, wordt in het label "10,00" weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8e500-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="8e500-128">Zie [Aangepaste numerieke tekenreeksen](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings) voor een volledige lijst met de beschikbare notatiereeksen voor getallen.</span><span class="sxs-lookup"><span data-stu-id="8e500-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="8e500-129">Aangepaste tekenreeksen</span><span class="sxs-lookup"><span data-stu-id="8e500-129">Custom string formats</span></span>

<span data-ttu-id="8e500-130">U kunt de eerste tekens van een tekenreeks verwijderen met de volgende velden en opmaakcode.</span><span class="sxs-lookup"><span data-stu-id="8e500-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="8e500-131">Hier geeft `#` het aantal tekens op dat u wilt overslaan.</span><span class="sxs-lookup"><span data-stu-id="8e500-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="8e500-132">Als u bijvoorbeeld een SSCC-nummerplaatnummer (Serial Shipping Container Code) wilt afdrukken, waarin de eerste twee tekens niet zijn opgenomen, gebruikt u `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="8e500-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="8e500-133">In dat geval wordt het nummerplaatnummer 0011111111111222221 afgedrukt als "11111111111222221".</span><span class="sxs-lookup"><span data-stu-id="8e500-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="8e500-134">Aangepaste datum- en tijdnotaties</span><span class="sxs-lookup"><span data-stu-id="8e500-134">Custom date/time formats</span></span>

<span data-ttu-id="8e500-135">In het volgende voorbeeld ziet u hoe u de indeling instelt die wordt gebruikt om datums af te drukken.</span><span class="sxs-lookup"><span data-stu-id="8e500-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="8e500-136">In dit voorbeeld wordt de datum 30 april 2020 afgedrukt als "30-04-2020".</span><span class="sxs-lookup"><span data-stu-id="8e500-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="8e500-137">Zie [Aangepaste reeksen voor datum en tijd](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings) voor een volledige lijst met de beschikbare notatiereeksen voor datum/tijd.</span><span class="sxs-lookup"><span data-stu-id="8e500-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="8e500-138">Afzonderlijke regels uit gegevens met meerdere regels afdrukken</span><span class="sxs-lookup"><span data-stu-id="8e500-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="8e500-139">Als een gegevensveld meerdere regels bevat (dat wil zeggen regels die zijn gescheiden door regeleinden), kunt u een afzonderlijke regel afdrukken met de volgende notatie.</span><span class="sxs-lookup"><span data-stu-id="8e500-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="8e500-140">Hier is `#` het regelnummer dat u wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="8e500-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="8e500-141">(Gebruik 1 voor de eerste regel.)</span><span class="sxs-lookup"><span data-stu-id="8e500-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="8e500-142">Het systeem heeft bijvoorbeeld een veld `AdditionalAddress` waarin het volgende adres met meerdere regels wordt opgeslagen:</span><span class="sxs-lookup"><span data-stu-id="8e500-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="8e500-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="8e500-143">Contoso Inc.</span></span>  
<span data-ttu-id="8e500-144">Straatnaam 123</span><span class="sxs-lookup"><span data-stu-id="8e500-144">123 Street Name</span></span>  
<span data-ttu-id="8e500-145">Een plaats, een provincie</span><span class="sxs-lookup"><span data-stu-id="8e500-145">Some City, Some State</span></span>

<span data-ttu-id="8e500-146">U kunt dit adres met één regel per keer afdrukken met de volgende codes.</span><span class="sxs-lookup"><span data-stu-id="8e500-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="8e500-147">Code</span><span class="sxs-lookup"><span data-stu-id="8e500-147">Code</span></span> | <span data-ttu-id="8e500-148">Tekst die wordt afgedrukt</span><span class="sxs-lookup"><span data-stu-id="8e500-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="8e500-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="8e500-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="8e500-150">Straatnaam 123</span><span class="sxs-lookup"><span data-stu-id="8e500-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="8e500-151">Een plaats, een provincie</span><span class="sxs-lookup"><span data-stu-id="8e500-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="8e500-152">Afdrukken en opmaken vanuit een weergavemethode</span><span class="sxs-lookup"><span data-stu-id="8e500-152">Print and format from a display method</span></span>

<span data-ttu-id="8e500-153">U kunt afdrukken vanuit een weergavemethode met de volgende notatie.</span><span class="sxs-lookup"><span data-stu-id="8e500-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="8e500-154">U kunt deze notatie combineren met andere typen die eerder in dit onderwerp zijn beschreven.</span><span class="sxs-lookup"><span data-stu-id="8e500-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="8e500-155">U hebt bijvoorbeeld een weergavemethode met de naam `DisplayListOfItemsNumbers()` en u wilt het eerste artikelnummer van deze methode afdrukken.</span><span class="sxs-lookup"><span data-stu-id="8e500-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="8e500-156">In dit geval kunt u de volgende code gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8e500-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="8e500-157">Meer informatie over het afdrukken van labels</span><span class="sxs-lookup"><span data-stu-id="8e500-157">More information about how to print labels</span></span>

<span data-ttu-id="8e500-158">Zie [Afdrukken van nummerplaatlabel inschakelen](tasks/license-plate-label-printing.md) voor meer informatie over het instellen en afdrukken van labels.</span><span class="sxs-lookup"><span data-stu-id="8e500-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]