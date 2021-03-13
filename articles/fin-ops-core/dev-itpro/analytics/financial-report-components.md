---
title: Onderdelen van een financieel rapport
description: In dit artikel wordt beschreven hoe de onderdelen of bouwstenen van rapportdefinities worden gebruikt in de financiële rapportage.
author: aprilolson
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: d066ee69887f05c8fe14eebac1111c4db26ec628
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093971"
---
# <a name="financial-report-components"></a>Onderdelen van een financieel rapport

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe de onderdelen of bouwstenen van rapportdefinities worden gebruikt in de financiële rapportage. Deze bouwstenen bevatten rijdefinities, kolomdefinities en rapportagestructuurdefinities. In dit artikel wordt uitgelegd hoe u bouwstenen organiseert en vergrendelt.

De ontwerpfilosofie achter Ontwerper financiële rapporten is het opsplitsen van gegevens in de kleinste onderdelen of bouwstenen en vervolgens het naar behoefte combineren van de onderdelen. Daarom staat de opmaak van uw rapport los van uw financiële gegevens en kunt u het ontwerp van een rapport wijzigen zonder aanpassing van de financiële gegevens in uw Microsoft Dynamics ERP-systeem. Door deze benadering met bouwstenen te gebruiken, kunt u tekst, bedragen en berekeningen combineren om de rapporten te maken die u nodig hebt. Bovendien moedigt deze flexibiliteit creativiteit aan door het u gemakkelijk te maken om de bewerkingen op verschillende manieren weer te geven. De afzonderlijke bouwstenen van een rapportdefinitie zijn gelijk aan een driedimensioneel werkblad, maar zij hebben meer kracht. Een rapportdefinitie geeft de rijdefinitie, kolomdefinitie en optionele rapportagestructuurdefinitie op die voor het rapport moet worden gebruikt. Deze bevat ook informatie over waar u het rapport dat is gegenereerd opslaat en hoe u het opmaakt.

## <a name="building-blocks-of-a-report"></a>Bouwstenen van een rapport

| Bouwsteen            | Omschrijving | Meer informatie |
|---------------------------|-------------|----------------------|
| Rijdefinitie            | Een rijdefinitie definieert de beschrijvende regels (bijvoorbeeld salarissen of verkopen) in een rapport. Deze bevat ook de segmentwaarden of dimensies die de waarden voor elk regelartikel bevatten en omvat rij-opmaak en berekeningen. | [Rijdefinities](row-definitions-financial-reporting.md) |
| Kolomdefinitie         | Een kolomdefinitie definieert de te gebruiken periode bij het ophalen van gegevens uit de financiële dimensies. Deze bevat ook kolom-opmaak en berekeningen. | [Kolomdefinities](column-definitions-financial-reports.md) |
| Rapportagestructuurdefinitie | Een rapportagestructuurdefinitie lijkt op een organogram. Deze bevat afzonderlijke rapportage-eenheden die elk vak in de grafiek voorstellen. De eenheden kunnen afzonderlijke afdelingen van de financiële gegevens of hogerliggende eenheden zijn die gegevens van andere rapportage-eenheden samenvatten. | [Rapportagestructuurdefinities](financial-reporting-tree-definitions.md) |
| Rapportdefinitie         | Een rapportdefinitie gebruikt een rijdefinitie, een kolomdefinitie en een optionele rapportagestructuurdefinitie om een rapport te bouwen. Deze biedt ook extra opties en instellingen die u kunt gebruiken om een rapport aan te passen. | [Rapportdefinitie](design-financial-report-definitions.md) |

Als het ontwerpen van rapporten nieuw is voor u, wilt u wellicht de rapportwizard gebruiken om snel een rapportdefinitie te maken die u later kunt aanpassen. Als u ervaring hebt in het ontwerpen van rapporten en meer flexibiliteit voor rapportontwerp wilt, kunt u nieuwe of bestaande bouwstenen combineren om een nieuwe rapportdefinitie te maken. U hoeft alle beschikbare opties voor rapportdefinities niet volledig te begrijpen om kwaliteitsvolle rapporten te produceren. Terwijl u vertrouwd wordt met het ontwerpen van rapporten, kunt u uw rapportdefinities uitvouwen om te profiteren van geavanceerdere functies. Nadat u een basisrapport hebt gemaakt, kunt u de rapportdefinitie en eventuele bouwstenen aanpassen in de rapportdefinitie.

## <a name="organize-the-building-blocks"></a>De bouwstenen indelen
Gebruik mappen om uw bouwstenen in Report Designer in te delen. Alle mappen zijn specifiek voor het type bouwsteen dat ze bevatten. Alle mappen die bijvoorbeeld rijdefinities bevatten die zich in het deelvenster **Rijdefinities** in Report Designer bevinden.

### <a name="create-a-folder"></a>Een map maken

1. Selecteer in Report Designer het type bouwsteen dat u in het navigatievenster wilt indelen. Als u bijvoorbeeld een rijdefinitie wilt sorteren, klikt u op **Rijdefinities**.
2. Selecteer in het navigatievenster de bestaande map waaronder u de nieuwe map wilt maken en volg daarna een van de volgende stappen:

    - Klik met de rechtermuisknop op de bovenliggende map en klik vervolgens op **Nieuwe map**.
    - Selecteer de bovenliggende map, klik op **Bestand** en klik vervolgens op **Nieuwe map**.

3. Wanneer de nieuwe map wordt weergegeven, voert u de naam in van de nieuwe map en drukt u vervolgens op Enter.

## <a name="lock-a-building-block"></a>Een bouwsteen vergrendelen
U kunt een wachtwoord maken om een bouwsteen te vergrendelen en helpen beveiligen. Op dit manier kunt u een niveau van beveiliging toevoegen aan een rapportonderdeel zonder het gehele systeem te beveiligen. Een wachtwoord kan helpen informatie van bouwstenen te beveiligen die belangrijk is voor uw rapportageproces aan het einde van een maand. Een gebruiker in elke willekeurige rol kan een bouwsteen vergrendelen. Andere gebruikers hebben echter altijd alleen-lezen toegang tot een vergrendelde onderdeel. Gebruikers kunnen het beveiligde onderdeel openen, wijzigen en opslaan onder een nieuwe naam. Een gebruiker die de rol van beheerder heeft kan een vergrendelde bouwsteen altijd openen en wijzigen.

1. Open in Report Designer het rapportonderdeel dat u wilt vergrendelen, zoals een rijdefinitie, kolomdefinitie, rapportdefinitie of rapportagestructuurdefinitie.
2. Klik in het menu **Extra** op **Beveiligen/beveiliging opheffen**. U kunt ook op **Beveiligen/beveiliging opheffen** (het slotpictogram) in de werkbalk klikken.
3. Voer in het dialoogvenster **Beveiligen** een wachtwoord in en beveilig dit. Klik vervolgens op **OK**. Het slotpictogram op de werkbalk wordt gemarkeerd wanneer een open bouwsteen wordt vergrendeld.

U kunt een vergrendelde bouwsteen ontgrendelen door de bouwsteen te openen en vervolgens op **Beveiligen/beveiliging opheffen** op de werkbalk te klikken. U kunt ook in het menu **Extra** op **Beveiliging opheffen** klikken.

## <a name="building-block-groups"></a>Bouwsteengroepen

Bouwstenen zijn de rijdefinities, kolomdefinities, rapportagestructuurdefinities en rapportdefinities die u voor een rapport maakt. Bouwsteengroepen zijn verzamelingen definities en dimensiegroepen.

### <a name="view-a-building-block-group"></a>Een bouwsteengroep weergeven

U kunt alle bouwstenen weergeven die aan een bouwsteengroep zijn toegewezen. U kunt een bouwsteengroep ook exporteren of importeren.

1. Klik in Report Designer in het menu **Bedrijf** op **Bouwsteengroepen**.
2. Selecteer in het dialoogvenster **Bouwsteengroepen** de bouwsteen die u wilt weergeven.
3. Klik op **Beeld** om het dialoogvenster **Bouwsteengroep weergeven** te openen en de inhoud van de bouwsteengroep weer te geven.
4. Klik op **Sluiten** om de dialoogvensters te sluiten.

### <a name="export-a-building-block-group"></a>Een bouwsteengroep exporteren

U kunt een bouwsteengroup of een specifiek bouwstenenrapport in een bouwsteengroep exporteren. U kunt de geëxporteerde bouwsteengroep als back-up gebruiken. U kunt de geëxporteerde gegevens ook tussen installaties kopiëren. Rapportontwerper bevat de lettertypen en de dimensiesets waarnaar wordt verwezen, samen met de bouwsteengroep.

1. Klik in Report Designer in het menu **Bedrijf** op **Bouwsteengroepen**.
2. Selecteer in het dialoogvenster **Bouwsteengroepen** de bouwsteengroep die u wilt exporteren en klik vervolgens op **Exporteren**.
3. Selecteer in het dialoogvenster **Exporteren** de te exporteren rapportdefinities:

    - Om al uw rapportdefinities en de gekoppelde bouwstenen te exporteren klikt u op **Alles selecteren**.
    - U kunt specifieke rapporten, rijen, kolommen, structuren of dimensiesets exporteren door op het gewenste tabblad te klikken en vervolgens de te exporteren items selecteren. Druk op Ctrl en houd deze toets ingedrukt om meerdere items op een tabblad te selecteren.

    > [!NOTE]
    > Wanneer u rapporten selecteert om te exporteren, worden de bijbehorende rijen, kolommen, structuren en dimensiegroepen ook geselecteerd.

4. Wanneer u klaar bent met het selecteren van te exporteren artikelen, klikt u op **Exporteren**.
5. Selecteer in het dialoogvenster **Opslaan als** een locatie om de bouwsteengroep naar te exporteren.
6. Voer in het veld **Bestandsnaam** een naam in voor het bestand. Rapportontwerper voegt automatisch een .tdbx-bestandsnaamextensie toe.
7. Klik op **Opslaan**. De bouwsteengroep wordt opgeslagen op de locatie die u hebt opgegeven.

### <a name="import-a-building-block-group"></a>Een bouwsteengroep importeren

U kunt een bouwsteengroep importeren in een bestaande bouwsteengroep. Alle geïmporteerde bouwsteengroepen behouden hun oorspronkelijke tekenstijlen en bedrijfsverwijzingen en bevatten de relevante dimensiesets.

1. Klik in Report Designer in het menu **Bedrijf** op **Bouwsteengroepen**.
2. Selecteer in het dialoogvenster **Bouwsteengroepen** de bouwsteengroep waarin u een bouwsteengroep wilt importeren en klik vervolgens op **Importeren**.
3. Selecteer in het dialoogvenster **Openen** de bouwsteengroep die u wilt importeren en klik vervolgens op **Openen**.
4. Selecteer in het dialoogvenster **Importeren** de te importeren rapportdefinities:

    - Als u alle rapportdefinities en de ondersteunende bouwstenen wilt importeren, klikt u op **Alles selecteren**.
    - Om specifieke rapporten, rijen, kolommen, structuren of dimensiesets te importeren, selecteert u de te importeren rapporten, rijen, kolommen, structuren of dimensiesets.

5. Wanneer u klaar bent met het selecteren van te importeren artikelen, klikt u op **Importeren**.

### <a name="undo-a-checkout-of-a-building-block"></a>Het uitchecken van een bouwsteen ongedaan maken

Wanneer u een bouwsteen opent, hebben andere gebruikers alleen-lezen toegang tot die bouwsteen. Soms vergeten gebruikers om een bouwsteen te sluiten of zij sluit het systeem af zonder de bouwsteen te sluiten. Daarom blijft de bouwsteen uitgecheckt en kunnen andere gebruikers deze niet openen. In deze gevallen kan een beheerder voor financiële rapportage het dialoogvenster **Uitgecheckte artikelen** gebruiken om bouwstenen in te checken die gebruikers uitgecheckt hebben gelaten.

> [!NOTE]
> U moet de rol van beheerder hebben om bouwstenen te kunnen inchecken met het dialoogvenster **Uitgecheckte items**.

1. Klik in Report Designer in het menu **Extra** op **Uitgecheckte artikelen**.
2. Schakel in het dialoogvenster **Uitgecheckte items** het selectievakje **Items van alle gebruikers weergeven** in. De lijst wordt bijgewerkt en u ziet alle uitgecheckte bouwstenen en door wie deze zijn uitgecheckt.
3. Selecteer een bouwsteen en klik vervolgens op **Uitchecken ongedaan maken**.
4. Klik op **Ja** om de nieuwe bouwsteen in te checken.

## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)
