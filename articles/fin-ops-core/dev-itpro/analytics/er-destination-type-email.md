---
title: ER-bestemmingstype voor e-mail
description: In dit onderwerp wordt uitgelegd hoe u een e-mailbestemming kunt configureren voor elke MAP- of BESTAND-component van een ER-indeling (Electronic Reporting).
author: NickSelin
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a575c04a5042e4db08f387bc7bce46225c109844
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753499"
---
# <a name="email-er-destination-type"></a>ER-bestemmingstype voor e-mail

[!include [banner](../includes/banner.md)]

Wanneer een ER-indeling (elektronische rapportage) wordt uitgevoerd, kunnen er een of meer uitgaande documenten worden gegenereerd. Indelingsonderdelen **Map** of **Bestand** worden gebruikt in ER-indelingen om de structuur van uitgaande documenten op te geven. U kunt een e-mailbestemming configureren voor deze typen onderdelen om uitgaande documenten te verzenden als e-mailbijlagen.

U kunt een e-mailbestemming configureren voor elk onderdeel **Map** of **Bestand** van een ER-indeling. In dit geval **wordt elk uitgaand document afzonderlijk per e-mail verzonden**. Op basis van deze doelinstelling wordt een gegenereerd document geleverd als een bijlage van een e-mailbericht. 

> [!NOTE]
> Als er geen document wordt gegenereerd omdat de expressie **Ingeschakeld** voor het relevante onderdeel **Bestand** is geconfigureerd om een Booleaanse waarde **Onwaar** te retourneren, wordt er geen e-mailbericht verzonden, zelfs als er een e-mailbestemming is geconfigureerd en ingeschakeld voor het onderdeel.

U kunt ook verschillende onderdelen **Map** of **Bestand** samen [groeperen](#grouping) en vervolgens een e-mailbestemming configureren voor alle onderdelen in de groep. In dit geval worden alle uitgaande documenten die worden gegenereerd door onderdelen die tot de groep behoren, **als meerdere bijlagen van één e-mailbericht verzonden**. Op basis van deze doelinstelling wordt elk gegenereerd document geleverd als een bijlage van een enkel e-mailbericht.

> [!NOTE]
> Als er ten minste één document wordt gegenereerd door een onderdeel **Bestand** in een groep onderdelen, wordt een e-mailbericht verzonden. Als er geen document wordt gegenereerd door gegroepeerde onderdelen omdat de expressie **Ingeschakeld** voor elk onderdeel **Bestand** is geconfigureerd om een Booleaanse waarde **Onwaar** te retourneren, wordt er geen e-mailbericht verzonden, zelfs als er een e-mailbestemming is geconfigureerd en ingeschakeld voor die groep onderdelen.
>
> **E-mail** is de enige bestemming die kan worden geconfigureerd voor een groep onderdelen. Als u een document wilt afleveren dat is verzonden op basis van de instelling voor de e-mailbestemming voor een groep, voegt u nog een bestemmingsrecord toe, selecteert u het gewenste onderdeel en configureert u vervolgens een andere bestemming voor deze record.

Er kunnen meerdere groepen onderdelen worden geconfigureerd voor een enkele ER-indelingsconfiguratie. Op deze manier kunt u een e-mailbestemming configureren voor elke groep onderdelen en een e-mailbestemming voor elk onderdeel.

## <a name="configure-an-email-destination"></a>Een e-mailbestemming configureren

Als u een uitvoerbestand of meerdere uitvoerbestanden per e-mail wilt verzenden, selecteert u op de Pagina **Bestemming elektronische rapportage** op het sneltabblad **Bestandsbestemming** een onderdeel of groep onderdelen in het raster en selecteert u vervolgens **Instellingen**. Stel in het dialoogvenster **Bestemmingsinstellingen** dat verschijnt op het tabblad **E-mail** de optie **Ingeschakeld** in op **Ja**. U kunt vervolgens e-mailontvangers opgeven en het onderwerp en de tekst van het e-mailbericht bewerken. U kunt constante tekst voor het onderwerp en de hoofdtekst van het e-mailbericht instellen of u kunt ER-[formules](er-formula-language.md) gebruiken om e-mailteksten dynamisch te maken.

U kunt e-mailadressen voor ER op twee manieren configureren. U kunt de configuratie voltooien op dezelfde manier als de afdrukbeheerfunctie of u kunt een e-mailadres oplossen door via een formule direct naar de nieuwe ER-configuratie te verwijzen.

[![De optie Ingeschakeld instellen op Ja voor een e-mailbestemming](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>E-mailadrestypen

Als u **Bewerken** selecteert naast het veld **Aan** of **CC** in het dialoogvenster **Bestemmingsinstellingen**, wordt het dialoogvenster **E-mail naar** weergegeven. Selecteer **Toevoegen** en selecteer vervolgens het type e-mailadres dat u wilt gebruiken. Er worden momenteel twee typen ondersteund: **E-mail van Afdrukbeheer** en **Configuratie-e-mail**.

[![Het type e-mailadres selecteren](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management-email"></a>E-mail van Afdrukbeheer

Als u **E-mail van Afdrukbeheer** selecteert als type e-mailadres, kunt u in het dialoogvenster **E-mail naar** een vast e-mailadres invoeren door de volgende velden in te stellen:

- Selecteer **Geen** in het veld **E-mailbron**.
- Voer in het veld **Extra e-mailadressen, gescheiden door ";"** de vaste e-mailadressen in.

U kunt ook e-mailadressen ophalen uit de contactgegevens van de partij waarvoor u een uitgaand document hebt gegenereerd. Als u niet-vaste e-mailadressen wilt gebruiken, selecteert u in het veld **E-mailbron** de [rol](../../fin-ops/organization-administration/overview-global-address-book.md#party-roles) van de partij voor een bestandsbestemming. De volgende rollen worden ondersteund:

- Klant
- Leverancier
- Prospect
- Contact
- Concurrent
- Werknemer
- Sollicitant
- Potentiële leverancier
- Niet-toegestane leverancier

Als u bijvoorbeeld een e-mailbestemming wilt configureren voor een ER-indeling die wordt gebruikt om betalingen van leveranciers te verwerken, selecteert u de rol **Leverancier**.

Nadat u de gewenste rol hebt geselecteerd, selecteert u de knop **Binden** (kettingsymbool) naast het veld **E-mailbronaccount** om de pagina [Formuleontwerper](general-electronic-reporting-formula-designer.md) te openen. U kunt deze pagina vervolgens gebruiken voor het configureren van een formule die tijdens runtime het rekeningnummer retourneert van de partij die vanuit het verwerkte document aan de geconfigureerde rol is toegewezen voor de e-mailbestemming.

> [!NOTE]
> Formules zijn specifiek voor de ER-configuratie.

Voer op de pagina **Formuleontwerper** in het veld **Formule** een documentspecifieke verwijzing in naar een ondersteunde rol. In plaats van de verwijzing te typen, zoekt u in het deelvenster **Gegevensbron** het knooppunt van de gegevensbron die een rekening vertegenwoordigt met de geconfigureerde rol en selecteert u vervolgens **Gegevensbron toevoegen** om de formule bij te werken. Als u bijvoorbeeld de e-mailbestemming configureert voor de configuratie **ISO 20022 Kredietoverdracht** die wordt gebruikt om leveranciersbetalingen te verwerken, is `'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` het knooppunt dat een leveranciersrekening vertegenwoordigt.

![Een e-mailbronaccount configureren](./media/er_destinations-emaildefineaddresssource.gif)

Als de rekeningnummers van de geconfigureerde rol uniek zijn voor het gehele exemplaar van Microsoft Dynamics 365 Finance, kan het veld **Bvan e-mailbron** in het dialoogvenster **E-mail naar** leeg blijven.

U kunt ook een situatie hebben waarin verschillende partijen in het [algemene adresboek](../../fin-ops/organization-administration/overview-global-address-book.md) zijn geregistreerd in verschillende bedrijven ([rechtspersonen](../../fin-ops/organization-administration/organizations-organizational-hierarchies.md#legal-entities)), zodat ze allemaal hetzelfde rekeningnummer gebruiken om de geconfigureerde rol te vullen. In dit geval zijn de rekeningnummers voor de geconfigureerde rol niet uniek voor de gehele Finance-exemplaar. Daarom kunt u niet alleen een rekeningnummer opgeven om een partij expliciet te selecteren. U moet ook het bedrijf opgeven in het bereik waarvan de partij is geregistreerd om de geconfigureerde rol te kunnen invullen. Selecteer de knop **Binden** (kettingsymbool) naast het veld **Bedrijf van e-mailbron** in het dialoogvenster **E-mail naar** om de pagina [Formuleontwerperr](general-electronic-reporting-formula-designer.md) te openen. U kunt deze pagina vervolgens gebruiken om een formule te configureren die tijdens runtime de code retourneert van het bedrijf waarvoor de gewenste bron deel moet uitmaken van het bereik.

> [!TIP]
> Als u de bedrijfscode moet gebruiken voor het uitvoeren van een ER-indeling, maar de ER-indeling geen gegevensbron bevat waaruit de bedrijfscode kan worden opgehaald, configureert u de formule `GetCurrentCompany()` met de ingebouwde ER-functie [GETCURRENTCOMPANY](er-functions-other-getcurrentcompany.md).

> [!NOTE]
> Formules zijn specifiek voor de ER-configuratie.

Als u het type e-mailadres wilt opgeven dat tijdens runtime moet worden gebruikt, selecteert u in het dialoogvenster **E-mail naar** de optie **Bewerken** naast het veld **Aan** om het dialoogvenster **E-mailadres toewijzen** te openen. Stel daarna de volgende velden in:

- Selecteer in het veld **Doel** de gewenste doelen. Alleen e-mailadressen van de geselecteerde doelen van contactpersonen van de ontdekte partij worden gebruikt.
- Stel de opie **Primaire contactpersoon** in op **Ja** als u een e-mailadres wilt gebruiken dat als primair e-mailadres is geconfigureerd voor de ontdekte partij.

> [!NOTE]
> Als doelen zijn geselecteerd in het veld **Doel** en de optie **Primaire contactpersoon** is ingesteld op **Ja**, wordt elk e-mailadres dat aan ten minste één geconfigureerd criterium voldoet, tijdens runtime gebruikt.

### <a name="configuration-email"></a>Configuratie-e-mail

Selecteer **Configuratie-e-mail** als het type e-mailadres als de configuratie die u gebruikt een knooppunt heeft in de gegevensbronnen die een enkel e-mailadres of meerdere e-mailadressen gescheiden door puntkomma's (;) retourneren. U kunt [gegevensbronnen](general-electronic-reporting.md#FormatComponentOutbound) en [functies](er-formula-language.md#functions) in de formuleontwerper gebruiken om een e-mailadres met juiste indeling te krijgen of meerdere e-mailadressen met een juiste indeling die door puntkomma's worden gescheiden. Als u bijvoorbeeld de configuratie **ISO 20022 Kredietoverdracht** gebruikt, is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` het knooppunt dat het primaire e-mailadres van een leverancier vertegenwoordigt in de contactgegevens van de leverancier waarnaar de begeleidende brief moet worden verzonden.

[![Een e-mailadresbron configureren](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="group-format-components"></a><a id="grouping"></a>Indelingsonderdelen groeperen

Als u indelingsonderdelen wilt groeperen, selecteert u op de pagina **Bestemming elektronische rapportage** op het sneltabblad **Bestandsbestemming** de onderdelen in het raster en selecteert u vervolgens **Groeperen**.

**E-mail** is de enige eerder geconfigureerde bestemming die nog beschikbaar is voor de geselecteerde onderdelen. Er zijn geen andere eerder geconfigureerde bestemmingen beschikbaar, omdat deze worden beschouwd als niet-ondersteund voor een groep onderdelen. U wordt naar behoren geïnformeerd over deze wijzigingen.

De record die u eerder hebt toegevoegd, wordt beschouwd als de koptekst van de groep die is gemaakt. Deze koptekstrecord bevat de instellingen voor e-mailbestemmingen voor de groep. Andere records zijn groepsleden die de instellingen voor e-mailbestemmingen van de koptekstrecord van de groep zullen gebruiken.

U kunt de groepering van indelingsonderdelen opheffen door op het sneltabblad **Bestandsbestemming** een record te selecteren die tot de groep behoort en vervolgens **Groep opheffen** te selecteren.

- Als u een koptekstrecord selecteert, wordt de groepering van de hele groep opgeheven.
- Als u een lidrecord selecteert en de record de laatste lidrecord in een groep is, wordt de groepering van de hele groep opgeheven.
- Als u een lidrecord selecteert die niet de laatste lidrecord in een groep is, wordt die record uitgesloten van de huidige groep.

In de volgende afbeelding ziet u de structuur van een ERindeling die is geconfigureerd voor het produceren van een uitgaand zip-bestand met een notitie bij aanmaningen en toepasselijke klantfacturen in PDF-indeling.

[![Structuur van een ER-indeling die uitgaande documenten genereert](./media/ER_Destinations-Email-Grouping1.png)](./media/ER_Destinations-Email-Grouping1.png)

In de volgende afbeelding ziet u het proces, zoals beschreven in dit onderwerp, voor het groeperen van afzonderlijke onderdelen en het inschakelen van de bestemming **E-mail** voor de nieuwe groep, zodat een notitie bij een aanmaning wordt verzonden met de desbetreffende klantfacturen als e-mailbijlagen.

[![Afzonderlijke onderdelen groeperen en de e-mailbestemming inschakelen](./media/ER_Destinations-Email-Grouping2.gif)](./media/ER_Destinations-Email-Grouping2.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
- [Formuleontwerper in elektronische rapportage (ER)](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]