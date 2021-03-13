---
title: Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren
description: In dit onderwerp wordt uitgelegd hoe gebruikers een nieuwe ER-indeling (Electronic Reporting) kunnen configureren om rapporten als Microsoft Word-documenten te genereren.
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094149"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>Een nieuwe ER-configuratie ontwerpen om rapporten in Word-indeling te genereren

[!include [banner](../includes/banner.md)]

Als u rapporten wilt genereren als Microsoft Word-documenten, moet u een sjabloon voor de rapporten ontwerpen met bijvoorbeeld de Word-bureaubladtoepassing. In de volgende afbeelding ziet u de voorbeeldsjabloon voor het controlerapport dat kan worden gegenereerd om details van verwerkte leveranciersbetalingen weer te geven.

![Voorbeeldsjabloon voor het controlerapport in de Word-bureaubladtoepassing](./media/er-design-configuration-word-image1.png)

Als u een Word-document wilt gebruiken als sjabloon voor rapporten in Word-indeling, kunt u een nieuwe [Electronic reporting (ER)](general-electronic-reporting.md) [oplossing](er-quick-start1-new-solution.md) configureren. Deze oplossing moet een ER-[configuratie](general-electronic-reporting.md#Configuration) bevatten die een onderdeel voor [ER-indeling](general-electronic-reporting.md#FormatComponentOutbound) bevat.

> [!NOTE]
> Wanneer u een nieuwe ER-indelingsconfiguratie maakt om rapporten te genereren in Word-indeling, moet u ofwel **Word** als indelingstype selecteren in het vervolgvenster **Configuratie maken** of het veld **Indelingstype** leeg laten.

![Een indelingsconfiguratie maken op de pagina Configuraties](./media/er-design-configuration-word-image2.gif)

Het ER-indelingsonderdeel van de oplossing moet het indelingselement **Excel\\File** bevatten en dat indelingselement moet zijn gekoppeld aan het Word-document dat wordt gebruikt als sjabloon voor gegenereerde rapporten tijdens runtime. Om het ER-indelingsonderdeel te configureren, moet u de [concept](general-electronic-reporting.md#component-versioning)-versie van de gemaakt ER-configuratie in de ER-indelingsontwerper openen. Voeg vervolgens het element **Excel\\File** toe, koppel uw Word-sjabloon aan de bewerkbare ER-indeling en koppel die sjabloon aan het **Excel\\File**-element dat u hebt toegevoegd.

> [!NOTE]
> Wanneer u een sjabloon koppelt, moet u een [documenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) gebruiken dat eerder is [geconfigureerd](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in de ER-parameters om sjablonen van ER-indelingen op te slaan.

![Een sjabloon koppelen op de pagina Indelingontwerper](./media/er-design-configuration-word-image3.gif)

U kunt **Excel\\Range** en **Excel\\Cell** geneste elementen toevoegen voor het element **Excel\\File** om de gegevensstructuur op te geven die tijdens runtime in gegenereerde rapporten wordt ingevoerd. U moet deze elementen vervolgens verbinden met gegevensbronnen van de bewerkbare ER-indeling om de werkelijke gegevens op te geven die tijdens runtime in gegenereerde rapporten worden ingevoerd.

![Geneste elementen toevoegen op de pagina Indelingsontwerper](./media/er-design-configuration-word-image4.gif)

Wanneer u uw wijzigingen opslaat in de ER-indeling tijdens het ontwerpen, wordt de hiërarchische indelingsstructuur opgeslagen in de gekoppelde Word-sjabloon als een [aangepast XML-onderdeel](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) met de naam **Rapport**. U moet de gewijzigde sjabloon openen, downloaden uit Finance, lokaal opslaan en openen in de Word-bureaubladtoepassing. In de volgende afbeelding ziet u de lokaal opgeslagen voorbeeldsjabloon voor het controlerapport met het aangepaste XML-onderdeel **Rapport**.

![Voorbeeld van de voorbeeldrapportsjabloon in de Word-bureaubladtoepassing](./media/er-design-configuration-word-image5.gif)

Wanneer bindingen van de indelingselementen **Excel\\Range** en **Excel\\Cell** worden uitgevoerd tijdens de runtime, komen de gegevens van elke binding in het gegenereerde Word-document als afzonderlijk veld van het aangepaste XML-onderdeel **Rapport**. Als u de waarden uit de velden van het aangepaste XML-onderdeel in een gegenereerd document wilt invoeren, moet u de juiste Word-[inhoudsbesturingselementen](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) toevoegen aan de Word-sjabloon om als tijdelijke aanduidingen te dienen voor gegevens die tijdens runtime worden ingevuld. Als u wilt opgeven hoe inhoudsbesturingselementen worden ingevuld, kunt u elk inhoudsbesturingselement aan het juiste veld van het aangepaste XML-onderdeel **Rapport** toewijzen.

![Inhoudsbesturingselementen toevoegen en toewijzen in de Word-bureaubladtoepassing](./media/er-design-configuration-word-image6.gif)

U moet vervolgens de oorspronkelijke Word-sjabloon van de bewerkbare ER-indeling vervangen door de gewijzigde sjabloon die nu Word-inhoudsbesturingselementen bevat die waren toegewezen aan de velden van het aangepaste XML-onderdeel **Rapport**.

![De sjabloon op de pagina Indelingontwerper vervangen](./media/er-design-configuration-word-image7.gif)

Wanneer u de geconfigureerde ER-indeling uitvoert, wordt de gekoppelde Word-sjabloon gebruikt om een nieuw rapport te genereren. De werkelijke gegevens worden in het Word-rapport opgeslagen als een aangepast XML-onderdeel met de naam **Rapport**. Wanneer het gegenereerde rapport wordt geopend, worden de Word-inhoudsbesturingselementen gevuld met gegevens uit het aangepaste XML-onderdeel **Rapport**.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

**Vraag:** ik heb een ER-indeling geconfigureerd om een Word-document af te drukken met een bedrijfsadres. In de Word-sjabloon voor deze ER-indeling heb ik een besturingselement voor opgemaakte tekst ingevoegd om een bedrijfsadres weer te geven. In Finance heb ik het bedrijfsadres als tekst met meerdere regels ingevoerd en **Enter** geselecteerd om een regelterugloop toe te voegen voor elke regel die ik ingevoerd heb. Daarom verwacht ik dat het bedrijfsadres als tekst met meerdere regels wordt weergegeven in gegenereerde documenten. Het adres verschijnt echter als één regel tekst die speciale symbolen bevat in plaats van regelteruglopen. Wat is er mis met mijn instellingen?

**Antwoord:** in plaats van een besturingselement voor opgemaakte tekst te gebruiken, moet u een besturingselement voor tekst zonder opmaak gebruiken en het selectievakje **Regelteruglopen toestaan (meerdere alinea´s)** selecteren in de eigenschappen van het besturingselement.

## <a name="additional-resources"></a>Aanvullende bronnen

- [ER-configuraties opnieuw gebruiken met Excel-sjablonen om rapporten te genereren in Word-indeling](./tasks/er-design-configuration-word-2016-11.md)
- [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
