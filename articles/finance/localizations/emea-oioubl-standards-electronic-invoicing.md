---
title: Ondersteunde standaarden voor elektronische facturering in Europa
description: In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa.
author: mrolecki
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: ''
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c86cc90e5f441641bc14d20898e65325d7c7d716
ms.sourcegitcommit: 1ca48d95fbff2555307cc1e5e5e23feea79a8bc1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/03/2020
ms.locfileid: "3763681"
---
# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Ondersteunde standaarden voor elektronische facturering in Europa

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa. 

Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten. Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan. Deze .XML-bestanden moeten voldoen aan bepaalde standaarden. De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](https://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer. Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden. Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.

## <a name="electronic-invoice-formats-currently-available-in-dynamics-365-finance"></a>Elektronische factuurindelingen die momenteel beschikbaar zijn in Dynamics 365 Finance

De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:

-   OIOUBL v.2.02 voor Denemarken
-   EHF v. 3.0 voor Noorwegen
-   PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België
-   UBL-OHNL 1.9 voor Nederland
-   FacturaE v.3.2.1 voor Spanje
-   FatturaPA v.1.2 voor Italië
-   xRechnung v. 1.2 voor Duitsland
-   Open PEPPOL BIS Billing v.3.0 voor de Europese Unie
-   Specifieke Estse indelingsversie 1.2
-   Finvoice 3.0 voor Finland

Elektronische facturering is gebaseerd op [ER (Elektronische rapportage)](../../dev-itpro/analytics/general-electronic-reporting.md). Een gegevensmodel met een **factuurmodel**, een factuurmodeltoewijzing en een aantal land-/regiospecifieke configuraties voor ER-indelingen zijn gemaakt voor Oostenrijk (AT), Denemarken (DK), Italië (IT), Noorwegen (NO), Spanje (ES), Frankrijk (FR), België (BE), Nederland (NL), Duitsland (DE), Estland (EE), Finland (FI) en de EU.

-   OIOUBL Verkoopfactuur - voor AT, DK en NO
-   OIOUBL Verkoopcreditnota - voor AT, DK en NO
-   OIOUBL Projectfactuur - voor AT, DK en NO
-   OIOUBL Projectcreditnota - voor AT, DK en NO
-   UBL Verkoopfactuur FR
-   UBL Verkoopcreditnota FR
-   UBL Projectfactuur FR
-   UBL Projectcreditnota FR
-   UBL Verkoopfactuur BE
-   UBL Verkoopcreditnota BE
-   UBL Projectfactuur BE
-   UBL Projectcreditnota BE
-   UBL Verkoopfactuur NL
-   UBL Verkoopcreditnota NL
-   UBL Projectfactuur NL
-   UBL Projectcreditnota NL 
-   Verkoopfactuur (ES)
-   Verkoopfactuur (IT)
-   Projectfactuur (ES)
-   Projectfactuur (IT)
-   Verkoopfactuur DE
-   Projectfactuur DE
-   Peppol-verkoopfactuur - voor EU
-   Peppol-verkoopcreditnota - voor EU
-   Peppol-projectfactuur - voor EU
-   Peppol-projectcreditnota - voor EU
-   Verkoopfactuur (EE)
-   Projectfactuur (EE)
-   Verkoopfactuur (FI)
-   Projectfactuur (FI)

De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant. Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd. De set met vereiste gegevens kan verschillen van land tot land. Omdat de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.

## <a name="additional-resources"></a>Aanvullende bronnen
Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](../../fin-and-ops/get-started/help-overview.md#task-guides) afspelen in het Help-venster:

 - OIOUBL elektronische facturen instellen
 - OIOUBL elektronische factureringsconfiguraties importeren
 - Klantrekeningen instellen voor elektronische OIOUBL-facturering

> [!NOTE] 
> Hoewel deze taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen.
