---
title: Rijdefinities in Ontwerper financiële rapporten
description: Een rijdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van elke rij in een financieel rapport wordt gespecificeerd. Een rijdefinitie kan worden gecombineerd met kolomdefinities, rapportagestructuurdefinities en rapportdefinities om een bouwsteengroep te maken die door meerdere bedrijven kan worden gebruikt.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2019
ms.locfileid: "350430"
---
# <a name="row-definitions-in-financial-report-designer"></a>Rijdefinities in Ontwerper financiële rapporten

[!include [banner](../includes/banner.md)]

Een rijdefinitie is een rapportonderdeel, of bouwsteen, waarmee de inhoud van elke rij in een financieel rapport wordt gespecificeerd. Een rijdefinitie kan worden gecombineerd met kolomdefinities, rapportagestructuurdefinities en rapportdefinities om een bouwsteengroep te maken die door meerdere bedrijven kan worden gebruikt.

## <a name="create-a-row-definition"></a>Een rijdefinitie maken

1. Klik in Report Designer in het navigatievenster op **Rijdefinities**.
2. Klik in het menu **Bestand** op **Nieuw** en klik vervolgens op **Rijdefinities**. Voor meer informatie over de inhoud van elke cel raadpleegt u [Rijdefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Een rijdefinitie openen
1. Klik in Report Designer in het navigatievenster op **Rijdefinities**.
2. Dubbelklik op de naam van de rijdefinitie die u wilt openen.
3. Als u eventuele bouwstenen wilt weergeven die aan de rijdefinitie zijn gekoppeld, klikt u met de rechtermuisknop op de rijdefinitie en selecteert u vervolgens **Koppelingen**

## <a name="contents-of-a-row-definition"></a>Inhoud van een rijdefinitie
Een rijdefinitie kan maximaal 20.000 financiële dimensierijen bevatten en kan de volgende informatie bevatten:

- Beschrijvende tekst die betekenis geeft aan het rapport door sectiekopteksten, regels en spaties te maken, zoals **Contant geld** of **Totale opbrengst**
- Koppelingen naar financiële gegevens, die dimensiewaarden in Microsoft Dynamics 365 for Finance and Operations kunnen omvatten

    > [!NOTE]
    > U kunt een rijdefinitie configureren om elke keer dat het rapport wordt gegenereerd, gegevens op te halen uit het financiële dimensiesysteem.

- Rijtotalen en formules die op de bijbehorende financiële gegevens zijn gebaseerd

Gewoonlijk bevat elke rij in een rijdefinitie een van de volgende soorten gegevens:

- Verwijzingen naar het financiële dimensiessysteem
- Totalen of berekeningen die zijn gebaseerd op de gegevens
- Opmaak

Er zijn twee methoden voor het invoeren van gegevens in een rijdefinitie:

- Voer handmatig rijgegevens in een nieuwe rijdefinitie in. Voor meer informatie raadpleegt u [Rijdefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).
- Gebruik de rapportontwerper om rijgegevens rechtstreeks uit de financiële dimensies op te halen. Zie voor meer informatie het gedeelte "Gerelateerde formules/rijen/eenheden" in [Rijddefinitiecellen wijzigen](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a>Dimensies toevoegen aan een rijdefinitie
Een dimensie is een snijpunt van gegevens en waarden. U kunt gegevens en waarden groeperen in de rapportontwerper. U kunt vervolgens transacties classificeren en meer in detail analyseren. U kunt het dialoogvenster **Rijen invoegen van dimensies** gebruiken om meerdere rijen tegelijkertijd toe te voegen aan een rijdefinitie. Het dialoogvenster geeft één kolom voor elke dimensie weer. De volgende tabel beschrijft de informatie die u voor elke dimensie kunt opgeven.

| Optie                | Beschrijving |
|-----------------------|-------------|
| Dimensie             | Het patroon dat de dimensie identificeert die aan de rijdefinitie moet worden toegevoegd. Dit patroon bevat één en-teken (&) of hekje (\#) voor elke positie in de dimensies. Gebruik in het algemeen allemaal en-tekens voor de dimensie Hoofdrekening en allemaal hekjes voor andere dimensies. |
| Begin dimensiebereik | De eerste waarde voor de dimensie om aan de rijdefinitie toe te voegen. |
| Einde dimensiebereik   | De laatste waarde voor deze dimensie die aan de rijdefinitie moet worden toegevoegd. |

Als u dimensies wilt toevoegen aan een rijdefinitie, volgt u deze stappen.

1. Klik in Report Designer op **Rijdefinities** en open vervolgens de rijdefinitie die u wilt wijzigen.
2. Klik in het menu **Bewerken** op **Rijen invoegen van dimensies**.
3. Selecteer in het dialoogvenster **Rijen invoegen van dimensies** in de rij **Dimensies** de cel voor de dimensie die u naar de rijdefinitie wilt overbrengen en klik vervolgens op **Alle &&&**.
4. Als u de rijdefinitie tot een bepaald bereik van dimensiewaarden wilt beperken, voert u de begindimensiewaarde in de cel **Begin van dimensiebereik** in en voert u vervolgens de einddimensiewaarde in de cel **Einde dimensiebereik** in. Als u alle waarden voor de geselecteerde dimensie wilt opnemen, laat u deze cellen leeg. Als u alle waarden voor de geselecteerde dimensie wilt opnemen, laat u deze cellen leeg.

    > [!NOTE]
    > Als u jokertekens (\* of ?) in dimensiebereikwaarden gebruikt, worden mogelijk niet alle gewenste resultaten geretourneerd (afhankelijk van de sortering van gegevens in de ERP-database).

5. Geef in het veld **Beginrijcode** de rijcode op voor de eerste dimensiewaarde die aan de rijdefinitie moet worden toegevoegd.
6. Geef in het veld **Elke rij verhogen met** een waarde op om de ruimte tussen opeenvolgende rijcodes te specificeren. Als de eerste rijcode bijvoorbeeld 100 is en de verhogingswaarde 30, hebben de eerste nieuwe rijen de codes 100, 130, 160, 190 en 220. Gebruik een verhogingswaarde die ruimte biedt voor het invoegen van nieuwe opmaak en formulerijen.
7. Klik tot slot op **OK**. Voor elk van de geselecteerde dimensiewaarden wordt één regel toegevoegd aan de rijdefinitie.

## <a name="adjust-rounding-in-a-row-definition"></a>Afronding in een rijdefinitie aanpassen
Wanneer u een balans hebt waarin de bedragen worden afgerond, zijn de totalen mogelijk niet in evenwicht. Dit probleem kan optreden als u bijvoorbeeld de afrondingsoptie gebruikt in een balansrapport en in de rapportdefinitie eveneens afronden is gespecificeerd. U kunt de optie **Afrondingscorrectie** gebruiken in de rijdefinitie om de bedragen op de balans in evenwicht te brengen. U kunt afronding uitschakelen of aanpassen op het tabblad **Instellingen** van de rapportdefinitie. In de volgende tabel wordt aangegeven hoe bedragen worden afgerond. In deze tabel verschillen de totalen van rijen 100 en 200 wanneer afronding is ingeschakeld.

| Rijcode | Bedragen zonder afronding | Bedrag met afronding naar gehele duizendtallen |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Totaal    | 7,300                    | 8                                       |

Als u afronding in een balans wilt aanpassen, volgt u deze stappen.

1. Klik in Report Designer op **Rijdefinities** en selecteer vervolgens de rijdefinitie die u wilt wijzigen.
2. Klik in het menu **Bewerken** op **Afrondingscorrectie**.
3. Voer in het dialoogvenster **Afrondingscorrecties** de volgende waarden in:

    - **Rij Afrondingscorrectie** - De rijcode voor de rij die moet worden aangepast om de balans in evenwicht te brengen.
    - **Rij Totale activa** - de rijcode voor de rij in de balans die de totale activa bevat.
    - **Rij Totaal aansprakelijkheden en eigen vermogen** - de rijcode voor de rij in de balans die de totale aansprakelijkheden en eigen vermogen bevat.
    - **Limiet van aanpassingsbedrag** - Een positief geheel getal dat de limiet voor automatische correcties aangeeft. Dit bedrag wordt vergeleken met de absolute waarde van het werkelijke afrondingsverschil.

    > [!NOTE]
    > Deze rijcodes moeten aan uw financiële gegevens zijn gekoppeld. Met andere woorden, de rij moet een dimensiewaarde bevatten in de cel **Koppeling naar financiële dimensies**. Verwijs **niet** naar een omschrijvings- (**DESC**), berekende (**CALC**) of totaalrij (**TOT**).

De bedragen in uw balans zullen nu in evenwicht zijn wanneer afronding is ingeschakeld.

> [!NOTE]
> De correctielimiet wordt toegepast aan de hand van de optie bij **Afrondingsprecisie** die is opgegeven voor de rapportdefinitie. Als u bijvoorbeeld selecteert om uw rapport op duizendtallen af te ronden en **2** invoert in het veld **Limiet van aanpassingsbedrag**, wordt een waarschuwingsbericht weergegeven wanneer de waarde die is opgegeven in het veld **Rij Afrondingscorrectie** met meer dan 2000 verhoogt of verlaagt.

## <a name="format-row-and-column-text"></a>Opmaakrij en kolomtekst
U kunt het uiterlijk van uw rapporten aanpassen door lettertypen te wijzigen en tekst op te maken. In de volgende secties wordt beschreven hoe u het uiterlijk van rijen en kolommen in rapporten opmaakt.

### <a name="manage-font-styles"></a>Tekenstijlen beheren

U kunt lettertypen maken en wijzigen voor uw rapport. U kunt deze stijlen vervolgens toepassen op het document of op een specifieke rij of kolom in een rapport.

<table>
<tbody>
<tr>
<td><strong>Een tekenstijl maken</strong></td>
<td>
<ol>
<li>Klik in Report Designer in het menu <strong>Opmaak</strong> op <strong>Stijlen en opmaak</strong>.</li>
<li>Klik op <strong>Nieuw</strong> in het dialoogvenster <strong>Stijlen en opmaak</strong> en voer een unieke naam voor de nieuwe stijl in.</li>
<li>Selecteer de gewenste instellingen voor de tekenstijl en klik op <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Een tekenstijl wijzigen</strong></td>
<td>
<ol>
<li>Klik in Report Designer in het menu <strong>Opmaak</strong> op <strong>Stijlen en opmaak</strong>.</li>
<li>Selecteer in het dialoogvenster <strong>Stijlen en opmaak</strong> de stijl die u wilt wijzigen en klik vervolgens op <strong>Wijzigen</strong>.</li>
<li>Selecteer de gewenste instellingen voor de tekenstijl en klik op <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Een tekenstijl toepassen</strong></td>
<td>
<ol>
<li>Selecteer in Report Designer in een definitie of kolomdefinitie of in kop- en voetteksten een of meer cellen.</li>
<li>Selecteer een tekenstijl in de lijst <strong>Stijl</strong> op de werkbalk.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Tekst van rij opmaken

De opmaak die in de rijdefinitie is opgegeven negeert de opmaak die in de kolomdefinitie en de rapportdefinitie is opgegeven. U kunt de tekstopmaak wijzigen met behulp van de besturingselementen op de werkbalk Opmaak. Deze besturingselementen zijn standaard Microsoft Windows-besturingselementen.

1. Open in Report Designer de rijdefinitie die u wilt wijzigen.
2. Selecteer de cellen die u wilt opmaken. Als u meerdere cellen wilt selecteren, houdt u Ctrl ingedrukt terwijl u de cellen selecteert.
3. Klik in de werkbalk op de knop van de opmaak die u wilt toepassen. Als u bijvoorbeeld een rij wilt laten inspringen, selecteert u de rij en klikt u vervolgens op **Inspringing vergroten** ![Inspringing vergroten](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Inspringing vergroten") op de werkbalk.

### <a name="adjust-columns-while-you-design-reports"></a>Kolommen aanpassen terwijl u rapporten ontwerpt

Om het gemakkelijker te maken om de kolommen waarin u werkt in de rijdefinitie weer te geven, kunt u de breedte van een kolom aanpassen en kunt u tevens kolommen verbergen (minimaliseren) of weergeven in het voorbeeldvenster. De wijzigingen die u aanbrengt zijn alleen van invloed op de weergave van de kolommen op het scherm. Ze hebben geen invloed op de kolomopmaak in rapporten.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>De breedte van een kolom wijzigen in het voorbeeldvenster

1. Open in Report Designer de rijdefinitie die u wilt wijzigen.
2. Selecteer in het menu **Opmaak** **Kolombreedte**.
3. Voer in het dialoogvenster **Kolombreedte** in en klik vervolgens op **OK**. U ook kunt de rechterbegrenzing van een kolomkopcel verslepen om de breedte van de kolom te wijzigen.

### <a name="hide-columns-in-the-view-pane"></a>Kolommen verbergen in het voorbeeldvenster

1. Open in Report Designer de rijdefinitie die u wilt wijzigen.
2. Selecteer de kolom of kolommen die u wilt minimaliseren.
3. Klik met de rechtermuisknop en klik vervolgens op **Verbergen**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Alle verborgen kolommen weergeven in het voorbeeldvenster

1. Open in Report Designer de rijdefinitie die u wilt wijzigen.
2. Klik met de rechtermuisknop op de geminimaliseerde kolom die u wilt weergeven en klik vervolgens op **Zichtbaar maken**.


## <a name="additional-resources"></a>Aanvullende resources

[Financiële rapportage](financial-reporting-intro.md)
