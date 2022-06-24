---
title: Opbrengsttoewijzing
description: In dit artikel wordt uitgelegd hoe u opbrengsttoewijzing gebruikt in Facturering van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 18739e0871592bc9eefcdf00f67dd4dd18f5d6f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864363"
---
# <a name="revenue-allocation"></a>Opbrengsttoewijzing

In dit artikel wordt uitgelegd hoe u parameters voor opbrengsttoewijzing configureert voor een factureringsplanning. U kunt opbrengsttoewijzing instellen en bewerken wanneer u de factureringsplanning maakt. Wanneer u de pagina **Opbrengsttoewijzing** opent voor een actieve of beëindigde factureringsplanning, zijn de velden alleen-lezen.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>De opbrengsttoewijzing opgeven voor een factureringsplanning

Volg deze stappen om de opbrengsttoewijzing op te geven voor een factureringsplanning.

1. Selecteer op de lijstpagina **Alle/actieve factureringsplanningen** een bestaande factureringsplanning of factureringsplanningsregel.
2. Selecteer op het tabblad **Opbrengsttoewijzing** bovenaan de pagina de waarde **Opbrengsttoewijzing**.
3. Selecteer in het veld **Type regeling met meerdere elementen** het type regeling met meerdere elementen (Multiple Element Arrangement, MEA).
4. Geef in het veld **Regelingsnummer met meerdere elementen** het nummer van de MEA op. Geef vervolgens in het veld **Rekening voor uitgestelde contractopbrengst** de rekening voor uitgestelde contractopbrengsten op.

    Als u het veld **Type regeling met meerdere elementen** instelt op **Enkel**, gelden voor elke regel hetzelfde **Regelingsnummer met meerdere elementen** en dezelfde **Rekening voor uitgestelde contractopbrengst**. Als u het veld **Type regeling met meerdere elementen** instelt op **Meerdere**, kunt u voor elke regel verschillende waarden voor **Regelingsnummer met meerdere elementen** en **Rekening voor uitgestelde contractopbrengst** opgeven.
    
    Een MEA-nummer kan alleen aan twee of meer artikelen worden toegewezen. Een enkele regel kan geen eigen MEA-nummer hebben.

5. Selecteer **Opslaan**.

### <a name="fields"></a>Velden

De pagina **Regeling met meerdere elementen** bevat de volgende velden.

| Veld | Description |
|---|---| 
| Type regeling met meerdere elementen | <p>Selecteer het MEA-type voor de transactie:</p><ul><li>**Meerdere**: de regelartikelen in de transactie maken deel uit van de MEA, of er is meer dan één regeling.</li><li>**Geen**: de transactie is een standaardtransactie zonder opbrengsttoewijzing.</li><li>**Enkel**: alle artikelen in de transactie maken deel uit van één MEA.</li></ul> |
| Regelingsnummer met meerdere elementen | <p>Het MEA-nummer van de regel. Dit veld is alleen beschikbaar wanneer het veld **Type regeling met meerdere elementen** is ingesteld op **Meerdere**.</p><p>Als dit veld leeg is en u een MEA-nummer toewijst, worden de velden **Oorsprong zelfstandige verkoopprijs** en **Zelfstandige verkoopprijs** automatisch bijgewerkt op basis van de waarden van de pagina **Zelfstandige verkoopprijs artikel**. Alleen de MEA-nummers die aan andere regels in de verkooporder zijn toegewezen, zijn beschikbaar.</p> |
| Rekening voor uitgestelde contractopbrengst | Geef de rekening op die moet worden gebruikt voor journaalposten wanneer een MEA-contractfactuur wordt gemaakt. Dit veld is alleen beschikbaar wanneer de facturering van terugkerende contracten wordt gebruikt. |
| **Regels** | |
| Variantnummer | Het variantnummer van de verkooporder. |
| Artikelnummer | Het artikelnummer van de verkooporder. |
| Factureringsfrequentie | De frequentie van de opbrengsttoewijzing: **Dagelijks**, **Maandelijks**, **Driemaandelijks**, **Halfjaarlijks** of **Jaarlijks**. |
| Quantity | De waarde uit de verkooporder. |
| Contractwaarde | De contractwaarde. |
| Regelingsnummer met meerdere elementen | <p>Het MEA-nummer van de regel. Dit veld is alleen beschikbaar wanneer het veld **Type regeling met meerdere elementen** is ingesteld op **Meerdere**.</p><p>Als dit veld leeg is en u een MEA-nummer toewijst, worden de velden **Oorsprong zelfstandige verkoopprijs** en **Zelfstandige verkoopprijs** automatisch bijgewerkt op basis van de waarden van de pagina **Zelfstandige verkoopprijs artikel**. Alleen de MEA-nummers die aan andere regels in de verkooporder zijn toegewezen, zijn beschikbaar. Als deze waarden niet zijn geconfigureerd voor het artikel, worden de waarden van de pagina **Parameters voor opbrengsttoewijzing van meerdere elementen** gebruikt.</p> | 
| Oorsprong zelfstandige verkoopprijs | <p>De oorsprong van de zelfstandige verkoopprijs:</p><ul><li>**Bedrag**: de zelfstandige verkoopprijs is een bedrag dat u opgeeft en groter dan 0 (nul) is. Het bedrag wordt zo nodig geconverteerd tussen de functionele en oorspronkelijke valuta's.</li><li>**Basis verkoopprijs**: de zelfstandige verkoopprijs komt overeen met de basisverkoopprijs van het artikel.</li><li>**Factuurprijs**: de zelfstandige verkoopprijs komt overeen met de factuurprijs van het artikel.</li><li>**Percentage van artikel**: de zelfstandige verkoopprijs wordt opgegeven als percentagewaarde en wordt berekend op basis van de prijs van het artikel. Als deze optie is geselecteerd, geeft u het standaardpercentage op.</li><li>**Restbedrag toewijzen**: de oorsprong van de zelfstandige verkoopprijs wordt berekend als *Totale contractwaarde van bovenliggend artikel* – *Totale zelfstandige verkoopprijs van onderliggende artikelen*:</p><ul><li>*Totale contractwaarde van bovenliggend artikel* is het netto- of factuurbedrag.</li><li>*Totale zelfstandige verkoopprijs van onderliggende artikelen* is de som van de uitgebreide of zelfstandige contractverkoopprijs van alle onderliggende artikelen, met uitzondering van het onderliggende artikel dat de oorsprong van deze zelfstandige verkoopprijs gebruikt.</li></ul><p>Als het berekende bedrag een negatieve waarde heeft, wordt het bedrag ingesteld op 0 (nul).</p><p>**Opmerking:** deze optie kan slechts voor één onderliggend artikel in de opbrengstsplitsing worden geselecteerd.</p></li><li>**Geen**: de oorsprong van de zelfstandige verkoopprijs is gebaseerd op de onderliggende artikelen. Deze optie geldt voor artikelen die zijn gedefinieerd als bovenliggende artikelen in een sjabloon voor opbrengstsplitsing. Als het selectievakje **Gesplitste opbrengst** is ingeschakeld, wordt deze optie automatisch ingeschakeld en kan de instelling niet worden gewijzigd.</li><li>**Percentage van bovenliggende factuurprijs**: de oorsprong van de zelfstandige verkoopprijs is een percentage van de factuurprijs van het bovenliggende artikel. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing.</li><li>**Percentage van bovenliggende standaardprijs**: de oorsprong van de zelfstandige verkoopprijs is een percentage van de standaardprijs van het bovenliggende artikel. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing. Wanneer de optie voor een onderliggend artikel van **Percentage van bovenliggende standaardprijs** in **Percentage van bovenliggende factuurprijs** of van **Percentage van bovenliggende factuurprijs** in **Percentage van bovenliggende standaardprijs** wordt gewijzigd, worden de berekende waarden ook bijgewerkt.</li></ul> |
| Zelfstandige verkoopprijs | <p>De zelfstandige verkoopprijs voor de regel in de transactievaluta.</p><p>De waarde in het veld **Bedrag** wordt ingevoerd of berekend.</p> |
| Zelfstandige verkoopprijs contract | De zelfstandige contractverkoopprijs. |
| Resterende contractopbrengst | Het resterende opbrengstbedrag voor het contract. Dit bedrag is het totaal van alle regels waarvoor nog geen facturen zijn gemaakt. |
| Totaal contractopbrengst | Het totale contractopbrengstbedrag voor de regel. Dit bedrag is het totaal van alle regels, ongeacht of daarvoor facturen zijn gemaakt of niet. |
| Rekening voor uitgestelde contractopbrengst | <p>Geef de rekening op die moet worden gebruikt voor journaalposten wanneer een MEA-contractfactuur wordt gemaakt.</p><p>Dit veld is alleen beschikbaar wanneer de facturering van terugkerende contracten wordt gebruikt.</p> |
| Fout | Eventuele fouten die zijn opgetreden voor de opbrengsttoewijzing. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Opbrengsttoewijzing gebruiken op een verkooporder

Volg deze stappen om de functionaliteit voor opbrengsttoewijzing op een verkooporder te gebruiken.

1. Maak op de pagina **Alle verkooporders** een verkooporder die artikelen bevat.
2. Selecteer op het tabblad **Factuur** onder **Opbrengsttoewijzing** de optie **Opbrengsttoewijzing**.
3. Geef in het veld **Type regeling met meerdere elementen** het MEA-type op.
4. Geef in het veld **Regelingsnummer met meerdere elementen** het nummer van de MEA op.
5. Als het veld **Type regeling met meerdere elementen** is ingesteld op **Meerdere**, selecteert u de gewenste regels en selecteert u vervolgens **Toepassen op selectie**.
6. Selecteer **Opslaan**.

Als u uitgestelde opbrengsten en onkosten gebruikt, wordt de uitstelplanning automatisch gemaakt. U kunt dit weergeven op de pagina **Alle uitstelplanningen**.
