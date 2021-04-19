---
title: Boekingsinstellingen voor kortingsbeheer
description: In dit onderwerp wordt beschreven hoe u boekingsprofielen instelt. Boekingsprofielen worden gebruikt om boekingsposten voor berekeningregels voor kortingsbeheer te bepalen.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: e79feb567a48d08a9063bf20cface3c5c7fe8ecc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831741"
---
# <a name="rebate-management-posting-setup"></a>Boekingsinstellingen voor kortingsbeheer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Boekingsprofielen voor kortingsbeheer worden gebruikt om boekingsposten voor berekeningregels voor kortingsbeheer te bepalen. Wanneer een boekingsprofiel wordt geselecteerd in de header van de deal, is dit van toepassing op alle regels van de deal.

Deze functie is in verschillende bedrijven (rechtspersonen) werkzaam. U kunt het bedrijf opgeven waaraan de voorzieningen worden toegerekend en waardoor de claims worden betaald. U kunt ook verschillende debetrekeningen voor voorzieningen en creditrekeningen voor afschrijvingen instellen per bronboekingsbedrijf.

Als u boekingsprofielen voor kortingsbeheer wilt instellen voor klanten en leveranciers, gaat u naar **Kortingsbeheer \> Boekingsinstellingen voor kortingsbeheer \> Boekingsprofielen voor kortingsbeheer**. De pagina **Boekingsprofielen voor kortingsbeheer** bevat een lijstvenster met alle bestaande profielen. U kunt de knoppen in het actievenster gebruiken om profielen toe te voegen aan de lijst of uit de lijst te verwijderen.

In de resterende secties van dit onderwerp wordt beschreven hoe u de beschikbare velden gebruikt wanneer u een profiel maakt of bewerkt.

## <a name="posting-profile-header"></a>Header van boekingsprofiel

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn in de headersectie van elk boekingsprofiel voor kortingsbeheer.

| Veld | Beschrijving |
|---|---|
| Boekingsprofiel | Voer een unieke naam in voor het profiel. |
| Beschrijving | Voer een beschrijving van het profiel in. |
| Module | Selecteer het type kortingen en royalty's dat aan het profiel is gekoppeld (*Klant* of *Leverancier*). |
| Type | Selecteer het profieltype (*Korting* of *Royalty*). |
| Type betaling | <p>Met dit veld wordt de indeling van de geboekte kortingsuitvoer bepaald.<p><p>Wanneer het veld **Type** is ingesteld op *Korting*, zijn de volgende waarden beschikbaar:</p><ul><li>*Geen*: er is geen standaardboekingstype. Daarom moet u het type definiëren wanneer u de verwerking doet.</li><li>*Betalen met leveranciers*: wanneer u de korting plaatst, wordt een leveranciersfactuur gemaakt voor de remiseleverancier die is ingesteld op de klant van de korting.</li><li>*Klantinhoudingen*: wanneer u de korting boekt, wordt een klantinhoudingsjournaal voor de kortingsklant gemaakt.</li><li>*Klantinhoudingen belastingfactuur*: wanneer u de korting boekt, wordt een vrije-tekstfactor voor de kortingsklant gemaakt.</li><li>*Handelsuitgave*: wanneer u de korting boekt, wordt een klantinhoudingsjournaal voor de kortingsklant gemaakt.</li><li>*Rapportage*: wanneer u de korting boekt, wordt een klantinhoudingsjournaal voor de kortingsklant gemaakt.</li></ul><p>Wanneer het veld **Type** is ingesteld op *Royalty*, zijn de volgende waarden beschikbaar:</p><ul><li>*Geen*: er is geen standaardboekingstype. Daarom moet u het type definiëren wanneer u de verwerking doet.</li><li>*Betalen met leveranciers*: wanneer u de korting plaatst, wordt een leveranciersfactuur gemaakt voor de kortingsleveranciersrekening.</li><li>*Rapportage*: wanneer u de korting plaatst, wordt een leveranciersfactuur gemaakt voor de kortingsleveranciersrekening.</li></ul><p>Zie de sectie [Betalingstypen](#payment-types) hieronder voor meer informatie. |
| Bedrijf | Selecteer het bedrijf (rechtspersoon) waaraan de voorzieningen worden toegerekend en waardoor de claims worden betaald. |

### <a name="payment-types"></a>Betalingstypen

In de volgende tabel wordt samengevat welke invloed de verschillende instellingen van het veld **Betalingstype** hebben op waar betalingen worden geboekt. Betalingen kunnen worden geboekt naar een klant-, leverancier- of remiserekening, afhankelijk van de doeltransactie en het kortingstype.

| Type betaling | Doeltransactietype | Kortingstype | Betaling aan (factuurrekening) |
|---|---|---|---|
| Betalen via leveranciers | Leveranciersfacturenjournaal | Klantenkorting | Remiseleveranciersrekening van klant |
| Betalen via leveranciers | Leveranciersfacturenjournaal | Royalty van klant | Leverancier |
| Betalen via leveranciers | Leveranciersfacturenjournaal | Leverancierskorting | Leverancier |
| Klantinhoudingen | Dagelijks journaal | Klantenkorting | Klantrekening |
| Klantinhoudingen voor belastingfacturen | Vrije-tekstfactuur | Klantenkorting | Klantrekening |
| Handelsuitgave | Dagelijks journaal | Klantenkorting | Klantrekening |
| Rapportage | Dagelijks journaal | Klantenkorting | Klantrekening |
| Rapportage | Leveranciersfacturenjournaal | Royalty van klant | Leverancier |
| Rapportage | Leveranciersfacturenjournaal | Leverancierskorting | Leverancier |

> [!NOTE]
> Houd rekening met de volgende punten bij het instellen van [kortingsbeheerdeals](rebate-management-deals.md):
>
> - Voor deals waarbij het veld **Afstemmen met** is ingesteld op *Deal*, kunt u de dynamische-dealrekening niet gebruiken tijdens het boeken. U moet een opgegeven klant- of leveranciersrekening gebruiken.
> - Voor transacties waarbij het veld **Afstemmen met** is ingesteld op *Regel*, kunt u een boekingsprofiel gebruiken dat tegenboekt naar een dynamische-dealrekening op de dealregel, omdat de klant per dealregel wordt ingesteld.

## <a name="posting-fasttab"></a>Sneltabblad Boeking

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Boeking** van elk boekingsprofiel voor kortingsbeheer.

| Veld | Beschrijving |
|---|---|
| Credittype | Selecteer of u een grootboekrekening of een klant of leverancier wilt crediteren. |
| Creditrekening | De rekening waarop creditbedragen worden geboekt wanneer kortingsvoorzieningen worden gemaakt. Deze rekening wordt ook gebruikt als de debetrekening wanneer de korting wordt geboekt om de klant te crediteren. |
| Journaalnaam<br>(In de sectie **Voorziening**) | Selecteer de naam van het journaal dat u wilt gebruiken om de geboekte voorziening vast te leggen. |
| Type | Selecteer of u de korting wilt boeken naar een grootboekrekening of naar een klant of leverancier. Als het veld **Betalingstype** in de header is ingesteld op *Klantinhoudingen voor belastingfacturen*, wordt dit veld ingesteld op *Klant/Leverancier*. |
| Rekeningbron gebruiken | <p>Selecteer een van de volgende waarden:</p><ul><li>*Geen*: als u deze waarde selecteert, moet u een rekening opgeven in het veld **Kortingsrekening**.</li><li>*Dealrekening*: gebruik de klant- of leveranciersrekening die is opgegeven op de kortingsregel. U kunt deze waarde alleen selecteren voor deals waarbij het veld **Afstemmen met** is ingesteld op *Regel* en voor dealregels waarbij het veld **Rekeningcode** is ingesteld op *Tabel*. Het is niet van toepassing op boekingsprofielen voor royalty's van klanten.</li></ul> |
| Kortingsrekening | De rekening waarnaar de werkelijke kortingskosten worden geboekt. |
| Journaalnaam<br>(In de sectie **Kortingsbeheer**) | Selecteer de naam van het journaal dat u wilt gebruiken om een creditnota voor het kortingsbedrag naar de klant te boeken. Dit veld is niet beschikbaar als het veld **Betalingstype** in de header is ingesteld op *Klantinhoudingen voor belastingfacturen*. |
| Btw-groep voor artikel | Geef op of de korting belastbaar is. |
| Journaalnaam<br>(In de sectie **Afschrijven**) | Als de geboekte korting niet gelijk is aan de voorziening, kan het verschil worden afgeschreven. Selecteer de naam van het journaal dat u wilt gebruiken om de geboekte afschrijving vast te leggen. |

## <a name="posting-by-company-fasttab"></a>Sneltabblad Boeking per bedrijf

Met het sneltabblad **Boeking per bedrijf** van elk boekingsprofiel voor kortingsbeheer kunt u de boekingsrekening opgeven die door elk bedrijf (rechtspersoon) in het raster wordt gebruikt.

Gebruik de knoppen op de werkbalk om bedrijven aan het raster toe te voegen en deze uit het raster te verwijderen. Telkens wanneer u een rij aan het raster toevoegt, gebruikt u het veld **Bedrijf** om de rechtspersoon voor die rij op te geven. Het veld **Naam** wordt vervolgensd automatisch ingesteld.

Selecteer de rij voor elk bedrijf en voer daarna de volgende gegevens in met behulp van de velden onder het raster:

- **Debettype**: selecteer of u een grootboekrekening of een klant of leverancier wilt debiteren.
- **Debetrekening:** voer de rekening in waarnaar het debetbedrag wordt geboekt wanneer kortingsvoorzieningen worden getroffen.
- **Hoofdrekening**: selecteer de hoofdrekening voor afschrijvingen.