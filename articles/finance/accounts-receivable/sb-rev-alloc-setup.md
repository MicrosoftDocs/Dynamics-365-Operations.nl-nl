---
title: Opbrengsttoewijzing van meerdere elementen instellen
description: In dit artikel wordt beschreven hoe u de parameters kunt instellen voor de opbrengsttoewijzing van meerdere elementen in Facturering van abonnementen.
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
ms.openlocfilehash: 23dae125e256e3e567e200024ee61a6c97cb1143
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903300"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Opbrengsttoewijzing van meerdere elementen instellen

Met de functie voor de opbrengsttoewijzing van meerdere elementen kunt u verschillende sjablonen instellen die worden gebruikt om opbrengst te berekenen en toe te wijzen aan meerdere artikelen. Deze functionaliteit kan u helpen om te voldoen aan Accounting Standards Codification Topic 606 (ASC 606) en/of International Financial Reporting Standard 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Parameters voor opbrengsttoewijzing van meerdere elementen

Gebruik de pagina **Parameters voor opbrengsttoewijzing van meerdere elementen** om de parameters in te stellen voor de opbrengsttoewijzing van meerdere elementen.

### <a name="standalone-selling-price-origin"></a>Oorsprong zelfstandige verkoopprijs

Het veld **Oorsprong zelfstandige verkoopprijs** bepaalt waar de op zelfstandige verkoopprijs vandaan komt. U kunt de waarde bijwerken op de pagina **Zelfstandige verkoopprijs artikel** en voor de transactie. De volgende opties zijn beschikbaar.

| Optie | Description |
|--------|-------------|
| Bedrag | De zelfstandige verkoopprijs is een bedrag dat u opgeeft en groter dan 0 (nul) is. Het bedrag wordt zo nodig geconverteerd tussen de functionele en oorspronkelijke valuta's. |
| Basis verkoopprijs | De zelfstandige verkoopprijs komt overeen met de basisverkoopprijs van het artikel. |
| Factuurprijs | De zelfstandige verkoopprijs komt overeen met de factuurprijs van het artikel. |
| Percentage van artikel | De zelfstandige verkoopprijs wordt opgegeven als percentagewaarde en wordt berekend op basis van de prijs van het artikel. Als u deze optie selecteert, geeft u het standaardpercentage op. |
| Restbedrag toewijzen | <p>De oorsprong van de zelfstandige verkoopprijs wordt berekend als *Totale contractwaarde van bovenliggend artikel* – *Totale zelfstandige verkoopprijs van onderliggende artikelen*:</p><ul><li>*Totale contractwaarde van bovenliggend artikel* is het netto- of factuurbedrag.</li><li>*Totale zelfstandige verkoopprijs van onderliggende artikelen* is de som van de uitgebreide of zelfstandige contractverkoopprijs van alle onderliggende artikelen, met uitzondering van het onderliggende artikel dat de oorsprong van deze zelfstandige verkoopprijs gebruikt.</li></ul><p>Als het berekende bedrag een negatieve waarde heeft, wordt het bedrag ingesteld op 0 (nul).</p><p>**Opmerking:** deze optie kan slechts voor één onderliggend artikel in de opbrengstsplitsing worden geselecteerd.</p> |
| Geen | De oorsprong van de zelfstandige verkoopprijs is gebaseerd op de onderliggende artikelen. Deze optie geldt voor artikelen die zijn gedefinieerd als bovenliggende artikelen in een sjabloon voor opbrengstsplitsing. Als het selectievakje **Gesplitste opbrengst** is ingeschakeld, wordt deze optie automatisch ingeschakeld en kan de instelling niet worden gewijzigd. |
| Percentage van bovenliggende factuurprijs | De oorsprong van de zelfstandige verkoopprijs is een percentage van de factuurprijs van het bovenliggende artikel. U kunt de standaardwaarde wijzigen. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing. |
| Percentage van bovenliggende standaardprijs | De oorsprong van de zelfstandige verkoopprijs is een percentage van de standaardprijs van het bovenliggende artikel. U kunt de standaardwaarde wijzigen. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing. Dit is de standaardoptie voor onderliggende artikelen. Wanneer de optie voor een onderliggend artikel van **Percentage van bovenliggende standaardprijs** in **Percentage van bovenliggende factuurprijs** of van **Percentage van bovenliggende factuurprijs** in **Percentage van bovenliggende standaardprijs** wordt gewijzigd, worden de berekende waarden ook bijgewerkt. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Rekening voor afrondingsverschillen bij opbrengsttoewijzing

In het veld **Rekening voor afrondingsverschillen bij opbrengsttoewijzing** geeft u de rekening op die wordt gebruikt om eventuele afrondingscorrecties in een contractopbrengstbedrag te registreren. Deze is beschikbaar wanneer terugkerende contractfacturering wordt gebruikt.

## <a name="item-standalone-selling-price"></a>Zelfstandige verkoopprijs artikel

Gebruik de pagina **Zelfstandige verkoopprijs artikel** om de oorsprong en zelfstandige verkoopprijs van een artikel op te geven. De waarden die op deze pagina worden opgegeven, worden gebruikt als de standaardwaarden op de pagina **Opbrengsttoewijzing** in Opbrengsttoewijzing met meerdere elementen en Terugkerende contractfacturering.

### <a name="specify-item-standalone-selling-price"></a>Zelfstandige verkoopprijs van een artikel opgeven

Volg deze stappen om de zelfstandige prijs voor een artikel op te geven.

1. Selecteer op de pagina **Zelfstandige verkoopprijs artikel** in het veld **Oorsprong zelfstandige verkoopprijs** de oorsprong van de zelfstandige verkoopprijs.
2. Voer een van de volgende stappen uit, afhankelijk van de waarde die u hebt geselecteerd in het veld **Oorsprong zelfstandige verkoopprijs**:

    * Als u **Percentage van artikel** hebt geselecteerd, geeft u het percentage op in het veld **Percentage**.
    * Als u **Bedrag** hebt geselecteerd, geeft u het bedrag op in het veld **Zelfstandige verkoopprijs**.

2. Selecteer voor elk artikel dat u aan de lijst wilt toevoegen de optie **Toevoegen**.
3. Selecteer de artikelcode in het veld **Artikelcode**. Selecteer de artikelrelatie in het veld **Artikelrelatie**. Voor artikelen waarvoor het selectievakje **Gesplitste opbrengst** is uitgeschakeld, moet de geselecteerde combinatie van een artikelcode en een artikelrelatie uniek zijn.
4. Wijzig zo nodig de standaardwaarde van het veld **Oorsprong zelfstandige verkoopprijs**, **Zelfstandig verkoopprijs** of **Percentage**.
5. Selecteer voor elk bovenliggend artikel dat u aan de lijst wilt toevoegen de optie **Toevoegen**.
6. Selecteer de artikelcode in het veld **Artikelcode**. Selecteer de artikelrelatie in het veld **Artikelrelatie**.
7. Schakel het selectievakje **Gesplitste opbrengst** in.
8. Selecteer de artikelrelatie in het veld **Artikelrelatie**. De lijst wordt bijgewerkt met het bovenliggende artikel en alle onderliggende artikelen.
9. Wijzig voor het onderliggende artikel desgewenst de standaardwaarde van het veld **Oorsprong zelfstandige verkoopprijs**, **Percentage van bovenliggende standaardprijs**, **Percentage van bovenliggende factuurprijs** of **Restbedrag toewijzen**.
10. Als u meerdere artikelen tegelijk wilt toevoegen, selecteert u **Artikelen toevoegen**.
11. Werk de query bij om de reeks artikelen te selecteren die u wilt toevoegen.
12. Selecteer **OK**, bekijk de lijst met artikelen die u hebt toegevoegd en selecteer **OK**.

### <a name="fields"></a>Velden

De pagina **Zelfstandige verkoopprijs artikel** bevat de volgende velden.

| Veld | Description |
|-------|-------------|
| Oorsprong zelfstandige verkoopprijs | <p>Selecteer de oorsprong van de zelfstandige verkoopprijs:</p><ul><li>**Bedrag**: de zelfstandige verkoopprijs is een bedrag dat u opgeeft en groter dan 0 (nul) is. Het bedrag wordt zo nodig geconverteerd tussen de functionele en oorspronkelijke valuta's.</li><li>**Basis verkoopprijs**: de zelfstandige verkoopprijs komt overeen met de basisverkoopprijs van het artikel.</li><li>**Factuurprijs**: de zelfstandige verkoopprijs komt overeen met de factuurprijs van het artikel.</li><li>**Percentage van artikel**: de zelfstandige verkoopprijs wordt opgegeven als percentagewaarde en wordt berekend op basis van de prijs van het artikel. Als u deze optie selecteert, geeft u het standaardpercentage op.</li></ul>**Restbedrag toewijzen**: de oorsprong van de zelfstandige verkoopprijs wordt berekend als *Totale contractwaarde van bovenliggend artikel* – *Totale zelfstandige verkoopprijs van onderliggende artikelen*:</p><ul><li>*Totale contractwaarde van bovenliggend artikel* is het netto- of factuurbedrag.</li><li>*Totale zelfstandige verkoopprijs van onderliggende artikelen* is de som van de uitgebreide of zelfstandige contractverkoopprijs van alle onderliggende artikelen, met uitzondering van het onderliggende artikel dat de oorsprong van deze zelfstandige verkoopprijs gebruikt.</li></ul><p>Als het berekende bedrag een negatieve waarde heeft, wordt het bedrag ingesteld op 0 (nul).</p><p>**Opmerking:** deze optie kan slechts voor één onderliggend artikel in de opbrengstsplitsing worden geselecteerd.</p></li><li>**Geen**: de oorsprong van de zelfstandige verkoopprijs is gebaseerd op de onderliggende artikelen. Deze optie geldt voor artikelen die zijn gedefinieerd als bovenliggende artikelen in een sjabloon voor opbrengstsplitsing. Als het selectievakje **Gesplitste opbrengst** is ingeschakeld, wordt deze optie automatisch ingeschakeld en kan de instelling niet worden gewijzigd.</li><li>**Percentage van bovenliggende factuurprijs**: de oorsprong van de zelfstandige verkoopprijs is een percentage van de factuurprijs van het bovenliggende artikel. U kunt de standaardwaarde wijzigen. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing.</li><li>**Percentage van bovenliggende standaardprijs**: de oorsprong van de zelfstandige verkoopprijs is een percentage van de standaardprijs van het bovenliggende artikel. U kunt de standaardwaarde wijzigen. Deze optie is alleen beschikbaar voor onderliggende artikelen in een sjabloon voor opbrengstsplitsing. Dit is de standaardoptie voor onderliggende artikelen. Wanneer de optie voor een onderliggend artikel van **Percentage van bovenliggende standaardprijs** in **Percentage van bovenliggende factuurprijs** of van **Percentage van bovenliggende factuurprijs** in **Percentage van bovenliggende standaardprijs** wordt gewijzigd, worden de berekende waarden ook bijgewerkt.</li></ul> |
| Zelfstandige verkoopprijs | Geef de zelfstandige verkoopprijs van het artikel op. Dit veld is beschikbaar als het veld **Oorsprong zelfstandige verkoopprijs** is ingesteld op **Bedrag**. |
| Percentage | Geef het percentage van de zelfstandige verkoopprijs op. Dit veld is beschikbaar als het veld **Oorsprong zelfstandige verkoopprijs** is ingesteld op **Percentage van artikel**, **Percentage van bovenliggende factuurprijs** of **Percentage van bovenliggende standaardprijs**. |
| Gesplitste opbrengst | <p>Geef op of een regel gebruikmaakt van opbrengstsplitsing:</p><ul><li>**Geselecteerd**: alleen artikelen waarvoor een sjabloon voor opbrengstsplitsing is ingesteld, kunnen worden geselecteerd in het veld **Artikelrelatie**. U kunt dit selectievakje alleen inschakelen voor bovenliggende artikelen van een sjabloon voor opbrengstsplitsing.</li><li>**Uitgeschakeld:** het artikel is een standaardartikel dat niet gebruikmaakt van opbrengstsplitsing.</li></ul> |
| Relatie | Een symbool geeft aan of het artikel een bovenliggend of onderliggend artikel is in een opbrengstsplitsing. |
| Artikelcode | <p>Selecteer de artikelcode: **Tabel** of **Groep**.</p><p>Als het selectievakje **Gesplitste opbrengst** is ingeschakeld, wordt dit veld ingesteld op **Tabel** en kan de waarde niet worden gewijzigd.</p> |
| Artikelrelatie | <p>Selecteer een artikelnummer.</p><p>Als het selectievakje **Gesplitste opbrengst** is ingeschakeld, kunnen alleen artikelen worden geselecteerd die bovenliggende artikelen zijn en waarvoor een sjabloon voor opbrengstsplitsing is ingesteld. Als het bovenliggende artikel is geselecteerd, wordt de lijst automatisch bijgewerkt met de onderliggende artikelen van dat bovenliggende artikel.</p> |
| Bovenliggend artikel | Voor het bovenliggende artikel bevat dit veld het artikelnummer. Voor onderliggende artikelen in een opbrengstsplitsing ziet u hier het artikelnummer van het bovenliggende artikel. |

## <a name="mea-templates"></a>MEA-sjablonen

Gebruik de pagina **MEA-sjablonen** om MEA-sjabloon-id's (Multiple Element Arrangement) te maken en te bewerken. Deze id's worden op de pagina **Opbrengsttoewijzing** gebruikt om artikelen samen te groepen.

### <a name="create-a-template"></a>Een sjabloon maken

Ga als volgt te werk om een MEA-sjabloon in te stellen.

1. Selecteer **Nieuw** op de pagina **MEA-sjablonen**.
1. Voer in het veld **MEA-sjabloon-id** een unieke id in.
1. Voer in het veld **Beschrijving** een beschrijving in.
1. Selecteer in het veld **Rekening voor uitgestelde contractopbrengst** de rekening die u voor journaalboekingen wilt gebruiken wanneer er een MEA-contractfactuur wordt gemaakt. Dit veld is beschikbaar wanneer de facturering van terugkerende contracten is ingeschakeld en wordt gebruikt.
1. Selecteer **Opslaan**.
