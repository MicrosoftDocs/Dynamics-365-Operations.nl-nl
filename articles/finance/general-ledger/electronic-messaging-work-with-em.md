---
title: Werken met de functionaliteit voor elektronische berichten
description: Dit artikel bevat informatie over het werken met de functionaliteit voor elektronische berichten (EM).
author: AdamTrukawka
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 929d3d3aad249007264204a3fd51377c8bb42377
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279267"
---
# <a name="work-with-the-electronic-messages-functionality"></a>Werken met de functionaliteit Elektronische berichten

[!include [banner](../includes/banner.md)]

Als u op berichtniveau werkt, is de pagina **Elektronische berichten** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Elektronische berichten**) geschikter. Als u op het gegevensverzamelings- of berichtitemniveau werkt, is de pagina **Items elektronisch bericht** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Items elektronisch bericht**) geschikter.

## <a name="electronic-messages"></a>Elektronische berichten

Op de pagina **Elektronische berichten** wordt de verwerking weergegeven die voor u beschikbaar is, op basis van uw rol. Beveiligingsrollen worden aan verwerking gekoppeld bij het instellen van die verwerking. Voor elke verwerking die beschikbaar is voor u, worden op de pagina elektronische berichten en gerelateerde gegevens weergegeven.

Op het sneltabblad **Berichten** worden elektronische berichten voor de geselecteerde verwerking weergegeven. Afhankelijk van de status van het geselecteerde bericht en de vooraf gedefinieerde verwerking kunt u bepaalde acties uitvoeren met de knoppen boven het raster:

- **Nieuw**: deze knop is gekoppeld aan acties van het type **Bericht maken**.
- **Verwijderen**: deze knop is beschikbaar als het selectievakje **Verwijderen toestaan** is ingeschakeld voor de huidige status van het geselecteerde bericht.
- **Gegevens verzamelen**: deze knop is gekoppeld aan acties van het type **Records invullen**.
- **Rapport genereren**: deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.
- **Rapport verzenden**: deze knop is gekoppeld aan acties van het type **Webservice**.
- **Antwoord importeren**: deze knop is gekoppeld aan acties van het type **Import van elektronische rapportage**.
- **Status bijwerken**: deze knop is gekoppeld aan acties van het type **Verwerking door gebruiker van berichtniveau**.
- **Berichtitems**: open de pagina **Items elektronisch bericht**.

Het sneltabblad **Actielogboek** bevat informatie over alle acties die zijn uitgevoerd voor het geselecteerde bericht. Als een actie een fout heeft veroorzaakt, wordt informatie over de fout gekoppeld aan de gerelateerde regel in het raster. Als u informatie over de fout wilt bekijken, selecteert u de regel in het raster en selecteert u vervolgens de knop **Bijlage** (paperclipsymbool) in de rechterbovenhoek op de pagina.

Het sneltabblad **Aanvullende velden voor bericht** bevat alle extra velden die zijn gedefinieerd voor berichten in de instellingen voor verwerking. Het sneltabblad bevat eveneens de waarden van deze extra velden.

Het sneltabblad **Berichtartikelen** bevat alle berichtartikelen die zijn gerelateerd aan het geselecteerde bericht. Afhankelijk van de status van het geselecteerde berichtitem kunt u bepaalde acties uitvoeren met de knoppen boven het raster:

- **Verwijderen**: deze knop is beschikbaar als het selectievakje **Verwijderen toestaan** is ingeschakeld voor de huidige status van het geselecteerde berichtitem.
- **Status bijwerken**: deze knop is gekoppeld aan acties van het type **Verwerking door gebruiker**.
- **Oorspronkelijk document**: open een pagina die het oorspronkelijke document voor het geselecteerde berichtitem bevat.

De rapporten die al zijn gegenereerd en ontvangen voor een bericht, worden aan dat bericht gekoppeld. U kunt de bijlagen bekijken die zijn gerelateerd aan een bericht door het bericht te selecteren en vervolgens de knop **Bijlage** (paperclipsymbool) in de rechterbovenhoek van de pagina te selecteren.

![De knop Bijlage](media/attachment-icon.png)

De pagina **Bijlagen** bevat de bijlagen die zijn gerelateerd aan het geselecteerde bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

![De knop Openen](media/open-button.png)

U kunt bijlagen bekijken die zijn gerelateerd aan een bepaalde actie die eerder is uitgevoerd voor een bericht. Selecteer het bericht op de pagina **Elektronische berichten** op het sneltabblad **Berichten**. Selecteer de actie op het sneltabblad **Actielogboek** en selecteer vervolgens de knop **Bijlage** (paperclipsymbool) in de rechterbovenhoek van de pagina.

U kunt de hele verwerking uitvoeren of alleen een specifieke actie door **Verwerking uitvoeren** in het actievenster te selecteren.

## <a name="electronic-message-items"></a>Items elektronisch bericht

Op de pagina **Items elektronisch bericht** worden alle berichtitems en een logboek van de acties die zijn uitgevoerd voor elk berichtitem weergegeven. Op de pagina worden ook de extra velden die zijn gedefinieerd voor de berichtitems en de waarden hiervan weergegeven.

In de volgende tabel worden de velden op het tabblad **Berichtitems** beschreven.

<table>
<thead>
<tr>
<th>Veld</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr>
<td>Wordt verwerkt</td>
<td>De naam van de verwerking die is gebruikt om het berichtitem te maken.</td>
</tr>
<tr>
<td>Berichtitem</td>
<td>De ID van het berichtitem. Deze ID wordt automatisch toegewezen op basis van de nummerreeks voor <b>Berichtitem</b> die is gedefinieerd op de pagina <b>Grootboekparameters</b>.</td>
</tr>
<tr>
<td>Datum berichtitem</td>
<td>De datum waarop het berichtitem is gemaakt.</td>
</tr>
<tr>
<td>Type berichtitem</td>
<td>Het type berichtitem. Er kunnen verschillende soorten berichtitems worden ingesteld voor dezelfde verwerking (bijvoorbeeld <b>Binnenkomende facturen</b> en <b>Uitgaande facturen</b>). Dit veld kan alleen automatisch worden ingesteld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Status berichtitem</td>
<td><p>De werkelijke status van het berichtitem. De beschikbare statussen variëren en zijn afhankelijk van het type berichtitem. Hieronder vindt u enkele voorbeelden:</p>
<ul>
<li><b>Ingevuld</b>: er is een record toegevoegd aan de tabel Berichtitems.</li>
<li><b>Geëvalueerd</b>: extra kenmerken zijn berekend voor het berichtartikel.</li>
<li><b>Gerapporteerd</b>: het berichtitem is toegevoegd aan een rapport.</li>
<li><b>Uitgesloten</b>: deze status komt van pas als bepaalde berichtitems uit een rapport moeten worden verwijderd voordat dit wordt geëxporteerd.</li>
</ul>
</td>
</tr>
<tr>
<td>Transmissiedatum</td>
<td>De datum waarop het berichtitem is verzonden voor verwerking waarbij automatisch een gegenereerd rapport buiten het systeem wordt verzonden.</td>
</tr>
<tr>
<td>Documentnummer</td>
<td>Het veld wordt automatisch ingesteld op basis van de instellingen voor de actie voor het invullen van records. Dit veld kan alleen automatisch worden ingesteld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Rekeningnummer</td>
<td>Het rekeningnummer van een klant of leverancier, of een andere veldwaarde, afhankelijk van het veld dat is gedefinieerd voor de actie Records invullen. Dit veld kan alleen automatisch worden ingesteld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Bericht</td>
<td>Het nummer van het bericht. Dit nummer wordt automatisch toegewezen op basis van de nummerreeks voor <b>Bericht</b> die is gedefinieerd op de pagina <b>Grootboekparameters</b>.</td>
</tr>
<tr>
<td>Berichtstatus</td>
<td>De werkelijke status van het elektronische bericht.</td>
</tr>
<tr>
<td>Volgende actie</td>
<td>De volgende acties die voor de huidige status van het berichtitem kunnen worden gestart.</td>
</tr>
</tbody>
</table>

Op het tabblad **Extra velden** worden de extra velden voor het geselecteerde berichtitem en de bijbehorende waarden weergegeven.

### <a name="run-processing"></a>Verwerking uitvoeren

Selecteer in het actievenster de optie **Verwerking uitvoeren** om de verwerking voor berichtitems uit te voeren. Als u een bepaalde actie wilt uitvoeren in het dialoogvenster **Verwerking uitvoeren**, stelt u de optie **Actie kiezen** in op **Ja** en selecteert u een actie. Als u de gehele verwerking wilt uitvoeren, laat u de optie **Actie kiezen** ingesteld op **Nee**.

### <a name="generate-report"></a>Rapport genereren

Selecteer **Rapport genereren** in het actievenster. Deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.

### <a name="update-status"></a>Status bijwerken

Selecteer **Status bijwerken** in het actievenster om de status van een of meer berichtitems bij te werken. Gebruik in het dialoogvenster **Status bijwerken** het sneltabblad **Op te nemen records** om de berichtitems te selecteren die u wilt bijwerken. Zorg ervoor dat u de selectiecriteria correct definieert, omdat berichtitemstatussen worden bijgewerkt volgens deze criteria, de oorspronkelijke status van de geselecteerde actie en de waarde die u opgeeft in het veld **Nieuwe status**. Nadat een statusupdate is voltooid, wordt het lastig om te bepalen welke items zijn bijgewerkt. Daarom is het moeilijk om de statusupdate terug te draaien.

### <a name="electronic-messages"></a>Elektronische berichten

Selecteer **Elektronische berichten** in het actievenster om een elektronisch bericht te bekijken dat is gerelateerd aan het geselecteerde berichtitem.

U kunt ook de bestanden bekijken die gerelateerd zijn aan een specifiek berichtitem. Selecteer het veld **Bericht** voor het berichtitem of selecteer **Elektronische berichten** in het actievenster. Selecteer op de pagina **Elektronisch bericht** het bericht waarvoor u bestanden wilt bekijken en selecteer vervolgens de knop **Bijlage** (paperclipsymbool) in de rechterbovenhoek van de pagina.

De pagina **Bijlagen** bevat de bijlagen die zijn gerelateerd aan het bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

### <a name="original-document"></a>Oorspronkelijk document

Selecteer **Oorspronkelijk document** in het actievenster om het oorspronkelijke document voor het geselecteerde berichtitem te openen.
