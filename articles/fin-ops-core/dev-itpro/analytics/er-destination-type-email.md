---
title: ER-bestemmingstype voor e-mail
description: Dit onderwerp bevat informatie over het configureren van een e-mailbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745556"
---
# <a name="email-destination"></a>E-mailbestemming

[!include [banner](../includes/banner.md)]

U kunt een e-mailbestemming configureren voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten. Op basis van de doelinstelling wordt een gegenereerd document geleverd als een bijlage van een e-mailbericht.

Stel **Ingeschakeld** in op **Ja** om een uitvoerbestand per e-mail te verzenden. Nadat deze optie is ingeschakeld, kunt u de e-mailontvangers opgeven en het onderwerp en de tekst van het e-mailbericht bewerken. U kunt constante teksten voor het onderwerp en de hoofdtekst van het e-mailbericht instellen of u kunt ER-[formules](er-formula-language.md) gebruiken om e-mailteksten dynamisch te maken. 

U kunt e-mailadressen voor ER op twee manieren configureren. U kunt de configuratie voltooien op dezelfde manier als de afdrukbeheerfunctie of u kunt een e-mailadres oplossen door via een formule direct naar de nieuwe ER-configuratie te verwijzen.

[![E-mailbestemming inschakelen](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-mailadrestypen

Als u **Bewerken** selecteert in het veld **Aan** of **Cc**, wordt het dialoogvenster **E-mail naar** weergegeven. Vervolgens kunt u het type te gebruiken e-mailadres selecteren. De e-mailtypen **Configuratie-e-mail** en **Afdrukbeheer** worden momenteel ondersteund.

[![E-mailtype selecteren](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>Afdrukbeheer

Als u het e-mailtype **Afdrukbeheer** selecteert, kunt u vaste e-mailadressen invoeren in het veld **Aan**. 

[![Vaste e-mailadressen configureren](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

Als u niet-vaste e-mailadressen wilt gebruiken, moet u het brontype voor e-mail selecteren voor een bestandsbestemming. De volgende waarden worden ondersteund: **Klant**, **Leverancier**, **Prospect**, **Contact**, **Concurrent**, **Werknemer**, **Sollicitant**, **Potentiële leverancier** en **Niet-toegestane leverancier**. Nadat u een e-mailbrontype hebt geselecteerd, gebruikt u de knop naast het veld **E-mail van bronrekening** om het formulier **Formuleontwerper** te openen. U kunt dit formulier gebruiken om een formule toe te voegen die tijdens runtime de **partijrekening** retourneert van het geselecteerde brontype van het verwerkte document naar de e-mailbestemming.

[![E-mailbronaccount configureren](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

Formules zijn specifiek voor de ER-configuratie. Voer in het veld **Formule** een documentspecifieke verwijzing naar een klant- of leverancierspartijtype in. In plaats van te typen kunt u ook het gegevensbronknooppunt zoeken waarmee de klant- of leveranciersrekening wordt voorgesteld. Selecteer vervolgens **Gegevensbron toevoegen** om de formule bij te werken. Als u bijvoorbeeld de configuratie **ISO 20022 Kredietoverdracht** gebruikt, is het knooppunt dat een leveranciersrekening vertegenwoordigt `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.

Als u een tekenreekswaarde invoert, bijvoorbeeld `"DE-001"`, en een formule opslaat, wordt er een e-mail verzonden naar de contactpersoon van de leverancier, **de-001**.


[De pagina ![ER-formuleontwerper](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![Kenmerken van e-mailbronaccount configureren](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>Configuratie-e-mail

Gebruik dit e-mailtype als de configuratie die u gebruikt, een knooppunt heeft in de gegevensbronnen dat een **e-mailadres** retourneert. U kunt gegevensbronnen en functies in de Formuleontwerper gebruiken om een correct opgemaakt e-mailadres te krijgen. Als u bijvoorbeeld de configuratie **ISO 20022 Kredietoverdracht** gebruikt, is het knooppunt dat een e-mailadres van een contactpersoon van een leverancier vertegenwoordigt `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.

[![E-mailadresbron configureren](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>Aanvullende resources

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
- [Formuleontwerper in elektronische rapportage (ER)](general-electronic-reporting-formula-designer.md)
