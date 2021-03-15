---
title: ER-configuraties ontwerpen om byte order mark (BOM) in gegenereerde bestanden te onderdrukken
description: In dit onderwerp wordt uitgelegd hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren die byte order mark (BOM) tekens onderdrukken.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060814"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a>ER-configuraties ontwerpen om byte order mark (BOM) in gegenereerde bestanden te onderdrukken

[!include [banner](../includes/banner.md)]

U kunt een [Electronic reporting (ER)](general-electronic-reporting.md) [oplossing](er-quick-start1-new-solution.md) ontwerpen om uitgaande documenten te genereren. Als u documenten wilt genereren als tekst- of XML-bestanden, moet de oplossing een ER-[configuratie](general-electronic-reporting.md#Configuration) bevatten die een ER-[indelings](general-electronic-reporting.md#FormatComponentOutbound)component bevat. Als u de [tekenversleuteling](https://docs.microsoft.com/windows/win32/intl/character-sets) wilt opgeven die de set tekens in gegenereerde bestanden vertegenwoordigt, moet de ER-indeling het indelingselement **Common\\File** bevatten. Om het ER-indelingsonderdeel te configureren, moet u de [concept](general-electronic-reporting.md#component-versioning)-versie van de ER-configuratie in de ER-indelingsontwerper openen en het element **Common\\File** toevoegen. Geef in het veld **Codering** de codering op van uitgaande bestanden die tijdens runtime worden gegenereerd met dit onderdeel.

> [!NOTE]
> Als de indeling een onjuiste coderingsnaam bevat, ontstaat er een fout wanneer u de wijzigingen in de instellingen van de indeling opslaat.

![Een hoofdelement toevoegen op de pagina Indelingsontwerper](./media/er-suppress-bom-characters-image1.gif)

Als u **UTF-8**, **UTF-16** of **UTF-32** als codering opgeeft, komt de optie **BOM-tekens onderdrukken** beschikbaar. Stel deze optie in op **Ja** om [BOM-tekens (byte order mark)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) te onderdrukken in uitgaande bestanden die tijdens runtime worden gegenereerd wanneer de bewerkbare ER-indeling wordt uitgevoerd.

> [!NOTE]
> Als u het veld **Codering** leeg laat, wordt de standaardcodering **UTF-8** gebruikt.

![De optie BOM-tekens onderdrukken instellen op de pagina Indelingsontwerper](./media/er-suppress-bom-characters-image2.gif)

Voer de juiste procedure uit om de functionaliteit tijdens runtime te controleren. Voer bijvoorbeeld de stappen in het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) uit. Nadat u de stappen in het gedeelte [De indeling wijzigen zodat de berekening wordt gebaseerd op gegenereerde uitvoer](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) van dat onderwerp hebt uitgevoerd, voert u deze extra stappen uit.

1. De UTF-codering opgeven:

    1. Selecteer het element **Rapport** van het type **Common\\File**.
    2. Geef in het veld **Codering** de codering **UTF-8** op.

2. Genereer een XML-bestand dat een BOM-teken bevat:

    1. Stel de optie **BOM-tekens onderdrukken** in op **Nee** om BOM-tekens op te nemen in gegenereerde XML-bestanden.
    2. Voltooi de stappen in het gedeelte [De uitvoering van het samenvattings-XML-element uitstellen zodat het berekende totaal wordt gebruikt](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) van het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) en sla het gegenereerde bestand op als **SampleXmlReport.xml**.

3. Genereer een XML-bestand dat geen BOM-teken bevat:

    1. Stel de optie **BOM-tekens onderdrukken** in op **Ja** om BOM-tekens te onderdrukken in gegenereerde XML-bestanden.
    2. Voltooi de stappen in het gedeelte [De uitvoering van het samenvattings-XML-element uitstellen zodat het berekende totaal wordt gebruikt](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) van het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) en sla het gegenereerde bestand op als **SampleXmlReport (1).xml**.

4. Vergelijk de gegenereerde bestanden in een bestandsvergelijkingsprogramma.

    Het eerste verschil dat u ziet, is in de bestandskoptekst. Het SampleXmlReport.xml-bestand bevat een BOM-teken, terwijl het bestand SampleXmlReport (1).xml dit niet bevat.

    ![Gegenereerde bestanden vergelijken met een bestandsvergelijkingsprogramma](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a>Zie ook

- [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]