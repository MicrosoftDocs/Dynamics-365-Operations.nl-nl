---
title: Rapportonderdelen indelen in Report Designer
description: In dit artikel wordt uitgelegd hoe u bestaande rapporten, bouwstenen en objecten in Report Designer kunt organiseren.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a94a88114072792243026e441e6c5a62ee80fc56
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802683"
---
# <a name="organize-report-components-in-report-designer"></a>Rapportonderdelen indelen in Report Designer

[!include [banner](../includes/banner.md)]

Nadat u bouwstenen hebt ontworpen en rapporten hebt gegenereerd, is het handig om deze objecten te ordenen zodat gebruikers ze eenvoudig kunnen vinden. In dit artikel wordt uitgelegd hoe u bestaande rapporten, bouwstenen en objecten in Report Designer kunt organiseren.

U kunt de naam van mappen, rapporten, bouwstenen en andere objecten in Report Designer wijzigen om te helpen uw bestanden in te delen. Afhankelijk van het type object waarvan u de naam wijzigt, moet u mogelijk koppelingen met dat object bijwerken.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>De naam van een map of bouwsteen wijzigen in Report Designer
In Report Designer kunt u de naam van mappen, rapportdefinities, rijdefinities, kolomdefinities en rapporteringsstructuurdefinities wijzigen.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>De naam van een map of bouwsteen wijzigen in Report Designer

1. Blader in het navigatiedeelvenster van Report Designer naar de map of het object waarvan u de naam wilt wijzigen.
2. Klik met de rechtermuisknop op de map of het object en klik vervolgens op **Naam wijzigen**. Het veld **Naam** in het navigatievenster komt beschikbaar.
3. Typ een nieuwe naam en druk vervolgens op **Enter**.
4. Als de bouwsteen een rijdefinitie, kolomdefinitie of rapportagestructuurdefinitie is, moet u andere bouwstenen bijwerken die hieraan zijn gekoppeld. Klik met de rechtermuisknop op de bouwsteen waarvan u de naam hebt gewijzigd in stap 3, selecteer **Koppelingen** en selecteer vervolgens een item in de lijst om het bij te werken.
5. Herhaal stap 4 tot alle gekoppelde artikelen zijn bijgewerkt.

## <a name="create-and-manage-report-groups"></a>Rapportgroepen maken en beheren
U kunt rapportdefinities groeperen om meerdere rapporten tegelijk te genereren. Als u rapportgroepen wilt maken, wijzigen, verwijderen en genereren, moet u de rol van ontwerper of beheerder hebben. Gebruikers die de rol van generator hebben, kunnen rapportgroepen genereren en kunnen ook de instelling van gebruikerrapportdefinities wijzigen voor rapportgroepen.

### <a name="create-a-report-group"></a>Een rapportgroep maken

1. Klik in Report Designer in het navigatievenster op **Rapportgroepen**.
2. Klik in het menu **Bestand** op **Nieuw** &gt; **Rapportgroepdefinitie** om een nieuwe groep in het venster van de viewer te openen. U kunt ook klikken op de knop **Rapportgroep** ![Rapportgroep.](media/report-group.gif "Rapportgroep") op de werkbalk.
3. Klik op het tabblad **Rapportgroep**. Als u de informatie over de afzonderlijke rapportdefinities wilt negeren voor het genereren van dit rapport, schakelt u het selectievakje **Instellingen voor bedrijf, details en datum uit individuele rapportdefinities negeren** in. De bedrijfsnaam, het detailniveau, voorlopige instellingen en datumgegevens worden automatisch ingevuld, maar u kunt wel updates uitvoeren.
4. Als u meerdere rapporten wilt genereren die de aangiftevaluta tonen, schakelt u het selectievakje **Alle aangiftevaluta opnemen** in. U kunt vervolgens meerdere weergaven openen door op de knop **Valuta** te klikken in de Web Viewer wanneer u het rapport weergeeft.
5. Klik in het veld **Rapporten in groep** op **Toevoegen** om de rapporten te selecteren die u in de rapportgroep wilt opnemen. Als u meerdere rapporten wilt selecteren in het dialoogvenster **Toevoegen**, houdt u de toets Ctrl ingedrukt terwijl u rapporten selecteert. Wanneer u klaar bent met het selecteren van rapporten, klikt u op **OK**.
6. Klik op **Bestand** &gt; **Opslaan** om de nieuwe rapportgroep op te slaan.

### <a name="modify-a-report-group"></a>Een rapportgroep wijzigen

1. Klik in Report Designer in het navigatievenster op **Rapportgroepen**.
2. Dubbelklik op de rapportgroep die u wilt wijzigen.
3. Breng de gewenste wijzigingen aan op het tabblad **Rapportgroep**.
4. Klik in het menu **Bestand** op **Opslaan** om de gewijzigde rapportgroep op te slaan of klik op de knop **Opslaan** ![Opslaan.](media/save.gif "Opslaan") op de werkbalk.

> [NOTE] Als u rapporten hebt gepland die met ingestelde intervallen moeten worden gegenereerd, kunt u die instellingen negeren en onmiddellijk een rapport genereren.

### <a name="generate-a-report-group-report"></a>Een rapportgroeprapport genereren

1. Klik in Report Designer in het navigatievenster op **Rapportgroepen**.
2. Open de rapportgroep die u wilt genereren.
3. Klik op de knop **Rapport genereren** ![Rapport genereren.](media/generate-report.gif "Rapport genereren") om rapporten te genereren.

### <a name="delete-a-report-group"></a>Een rapportgroep verwijderen

1. Klik in Report Designer in het navigatievenster op **Rapportgroepen**.
2. Klik met de rechtermuisknop op de rapportgroep die u wilt verwijderen en selecteer vervolgens **Verwijderen**.
3. Wanneer een bevestigingsbericht wordt weergegeven, klikt u op **Ja**.

## <a name="report-group-tab-controls"></a>Besturingselementen op tabblad Rapportgroep
De volgende tabel bevat beschrijvingen van de besturingselementen op het tabblad **Rapportgroep**.

<table>
<thead>
<tr>
<th>Control</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Instellingen voor bedrijf, details en datum uit individuele rapportdefinities negeren</td>
<td>Schakel dit selectievakje in om afzonderlijke rapportdefinities van de rapporten in deze rapportgroep te negeren voor alleen artikelgeneratie van deze rapporten.</td>
</tr>
<tr>
<td>Bedrijfsnaam</td>
<td>Selecteer het bedrijf dat u voor de rapporten wilt gebruiken.</td>
</tr>
<tr>
<td>Detailniveau</td>
<td>Geef het gewenste detailniveau op voor de rapporten.
<ul>
<li><strong>Financial</strong> - Een overzichtsrapport met een hoog niveau. U kunt rekeningen en dimensies niet in detail bekijken, behalve voor de rekeningen en dimensies die via een rapportagestructuur zijn toegevoegd.</li>
<li><strong>Financieel &amp; rekening</strong> − Een rapport dat een samenvatting op hoog niveau en rekeninggegevens bevat.</li>
<li><strong>Financieel, rekening &amp; transactie</strong> − Een rapport dat een samenvatting op hoog niveau en transactiegegevens bevat.</li>
</ul></td>
</tr>
<tr>
<td>Voorlopig</td>
<td>Geef de gewenste typen activiteit op voor de rapporten.
<ul>
<li><strong>Alleen geboekte activiteit</strong>− Alleen de transacties en saldi worden opgenomen die in uw financiële gegevens zijn geboekt.</li>
<li><strong>Geboekte en niet-geboekte activiteit</strong>− Alle transacties en saldi worden opgenomen die in uw financiële gegevens zijn ingevoerd en geboekt.</li>
<li><strong>Alleen niet-geboekte activiteit</strong>− Alleen de transacties worden opgenomen die in uw financiële gegevens zijn ingevoerd, maar nog niet geboekt.</li>
</ul></td>
</tr>
<tr>
<td>Alle aangiftevaluta opnemen</td>
<td>Alle extra aangiftevaluta's die in uw Microsoft Dynamics 365 Finance-systeem zijn geconfigureerd, worden hier vermeld. Schakel dit selectievakje in om extra rapporten te genereren in de valuta's die worden aangegeven. Deze rapporten kunnen vervolgens in de Web Viewer worden bekeken door te klikken op de knop <strong>Valuta</strong> en dan een valuta te selecteren.</td>
</tr>
<tr>
<td>Datumgegevens die niet zijn opgeslagen met rapportdefinitie</td>
<td><ul>
<li>Basisperiode</li>
<li>Basisjaar</li>
<li>Behandelde periode</li>
</ul>
Alleen standaardinstellingen voor de basisperiode worden opgeslagen met de rapportdefinitie.</td>
</tr>
<tr>
<td>Datumgegevens die zijn opgeslagen met rapportdefinitie</td>
<td><ul>
<li>Rapportdatum</li>
<li>Standaardbasisperiode</li>
</ul></td>
</tr>
<tr>
<td>Rapporten in groep</td>
<td>U kunt in de rapportgroep rapporten toevoegen, verwijderen en herschikken.
<ul>
<li>Als u rapportdefinities wilt toevoegen aan de rapportgroep, dubbelklikt u op de rapportgroep om deze te openen en klikt u vervolgens op <strong>Toevoegen</strong>. Selecteer de rapporten die u wilt opnemen in de rapportgroep en klik vervolgens op <strong>OK</strong>.</li>
<li>Als u een rapport wilt verwijderen uit de rapportgroep, selecteert u dit en klikt u vervolgens op <strong>Verwijderen</strong>.</li>
<li>Als u de volgorde wilt wijzigen waarin de rapporten worden gegenereerd, selecteert u een rapport in de lijst en klikt u vervolgens op <strong>Omhoog</strong> of <strong>Omlaag</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Aanvullende bronnen

[Financiële rapportage](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
