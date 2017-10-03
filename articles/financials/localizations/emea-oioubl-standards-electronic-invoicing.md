---
title: Ondersteunde standaarden voor elektronische facturering in Europa
description: In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition in de Europese regio.
author: mrolecki
manager: AnnBe
ms.date: 07/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.1, Operations, Core
ms.custom: 10274
ms.search.region: Austria, Denmark, Italy, Norway, Spain, France, Belgium, Netherlands
ms.search.industry: 
ms.author: mrolecki
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c944fd20273623ce3f7d03a24546addbe987084e
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="supported-standards-for-electronic-invoicing-in-europe"></a>Ondersteunde standaarden voor elektronische facturering in Europa

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt het dekkingsniveau toegelicht voor elektronisch factureren in Europa. 

Implementatie en goedkeuring van elektronische facturering binnen de Europese Unie is gereguleerd in [Richtlijn 2010/45/EU van de Raad](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:189:0001:0008:EN:PDF), die geldt in alle EU-lidstaten. Bedrijven die elektronisch factureren willen gebruiken, moeten verkooporderfacturen, vrije-tekstfacturen, projectfacturen, verkooporder-creditnota's en projectfactuur-creditnota's indienen als een .XML-bestand aan de overheid of andere handelspartijen die elektronische facturering toestaan. Deze .XML-bestanden moeten voldoen aan bepaalde standaarden. De landspecifieke vereisten en hun implementatie kunnen verschillen binnen EU-lidstaten, maar gebruiken gewoonlijk Universal Business Language ([UBL](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=ubl)) in verschillende versies met aanpassingen, en [PEPPOL](http://www.peppol.eu)- specificaties en toegangspunten voor validatie en vervoer. Het belangrijkste voordeel van UBL is dat zakelijke documenten kunnen worden gestandaardiseerd voor verschillende doeleinden. Omdat UBL een flexibele, internationale standaard is die ondersteuning biedt voor veel zakelijke vereisten, kunnen deze zakelijke documenten worden uitgewisseld over de landsgrenzen.

## <a name="what-electronic-invoice-formats-are-currently-available-in-finance-and-operations"></a>Welke indelingen voor elektronische facturen zijn momenteel beschikbaar in Finance and Operations?

De volgende landspecifieke indelingen van elektronische facturen zijn beschikbaar:

-   OIOUBL v.2.02 voor Denemarken
-   EHF v.2.0.8 voor Noorwegen
-   PEPPOL BIS v.2 voor Oostenrijk, Frankrijk en België
-   UBL-OHNL 1.9 voor Nederland
-   FacturaE v.3.2.1 voor Spanje
-   FatturaPA v.1.2 voor Italië

Elektronische facturering is gebaseerd op [elektronische rapportage](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting). Er is een gegevensmodel met een **klantfactuurmodel** en een aantal landspecifieke configuraties voor elektronische rapportopmaken voor Oostenrijk (AT), Denemarken (DK), Italië (IT), Noorwegen (NO), Spanje (ES), Frankrijk (FR), België (BE) en Nederland (NL).

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

De elektronische facturen en creditnota's die u genereert, bevatten vereiste gegevens zoals een EAN-nummer (European Article Numbering), de contactpersoon, het dimensierekeningnummer en adresgegevens van de klant. Er worden validatieregels worden toegepast wanneer facturen worden gegenereerd om te controleren of de juiste gegevens zijn ingevoerd. De set met vereiste gegevens kan verschillen van land tot land. Vanwege de vereiste en de ondersteunde landen en indelingen kunnen veranderen, moet u altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben.

## <a name="additional-information"></a>Aanvullende gegevens
Voor meer informatie over het instellen van elektronische facturen, kunt u de volgende [Taakbegeleidingen](/dynamics365/unified-operations/dev-itpro/get-started/help-overview#task-guides) afspelen in het Help-venster:

 - OIOUBL elektronische facturen instellen
 - OIOUBL elektronische factureringsconfiguraties importeren
 - Klantrekeningen instellen voor elektronische OIOUBL-facturering

> [!NOTE] 
> Hoewel deze Taakbegeleidingen zijn gemaakt voor de specifieke Deense e-factuurindeling *OIOUBL*, zijn ze met kleine afwijkingen van toepassing op andere ondersteunde landen.
