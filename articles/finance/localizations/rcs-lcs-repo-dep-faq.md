---
title: Afschaffing van Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage
description: Dit artikel biedt informatie over de afschaffing van Microsoft Dynamics Lifecycle Services Storage (LCS) die is gepland als onderdeel van de implementatie van de algemene opslagplaats van RCS (Regulatory Configuration Service).
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 65d45eaf618075e0c78881634fc77bda0fab277e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065669"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Afschaffing van Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage

[!include [banner](../includes/banner.md)]

Het gebruik van Microsoft Dynamics Lifecycle Services (LCS) als een opslagplaats voor ER-configuraties (Electronic Reporting) wordt afgeschaft. Bij deze afschaffing worden de volgende wijzigingen aangebracht:

- Door Microsoft geproduceerde configuraties die in Microsoft Dynamics 365-toepassingen worden gebruikt, worden niet meer gepubliceerd naar de bibliotheek voor gedeelde activa in LCS. In plaats daarvan worden ze alleen gepubliceerd via de algemene opslagplaats voor RCS. Configuraties voor Dynamics AX 2012 worden echter wel gepubliceerd in de bibliotheek voor gedeelde activa in LCS totdat de ondersteuningslevenscyclus voor AX 2012 eindigt.
- De functionaliteit waarmee u configuraties kunt uploaden naar de projectactivabibliotheek in LCS vanuit apps voor financiën en bedrijfsactiviteiten en vanuit RCS, wordt gedeactiveerd. U kunt echter wel de browser in LCS blijven gebruiken om configuraties naar de projectactivabibliotheek te uploaden. Het is dus nog steeds mogelijk om configuraties aan LCS toe te voegen, zodat deze in oplossingspakketten kunnen worden opgenomen.
- Het importeren van configuraties vanuit LCS blijft beschikbaar en wordt enige tijd ondersteund in apps voor financiën en bedrijfsactiviteiten en in RCS. De functionaliteit wordt uiteindelijk echter afgeschaft. (De exacte afschaffingsdatum wordt later bekendgemaakt.)

## <a name="deprecation-notice"></a>Bericht over afschaffing

Afschaffing van het gebruik van LCS als opslag is gecommuniceerd in [Verwijderde of afgeschafte functies in Dynamics 365 Finance - Bericht van afschaffing van LCS](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). De geplande afschaffingsdatum is 1 april 2022.

## <a name="key-features"></a>Belangrijke functies

- Gebruik RFS om ER-configuraties en globalisatiefuncties te maken en te bewerken.
- Push configuraties rechtstreeks van de RCS-ontwerper naar een gekoppelde toepassing, zoals een Dynamics 365 Finance-omgeving, zodat u snel wijzigingen in uw configuraties kunt aanbrengen en deze kunt testen.
- Bewaar, deel en beheer de levenscyclus voor zowel ER-configuraties als globalisatiefuncties via de gecentraliseerde opslag van de algemene opslagplaats.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Richtlijnen voor eenmalige en doorlopende acties

In dit gedeelte wordt een reeks stappen beschreven die één keer moeten worden uitgevoerd. Daarnaast worden de stappen beschreven die daarna doorlopend moeten worden uitgevoerd.

### <a name="one-time-action"></a>Eenmalige actie

Importeer alle vereiste configuraties van LCS naar RCS en publiceer deze vervolgens vanuit RCS naar de algemene opslagplaats. Als u projectspecifieke activabibliotheken gebruikt om afgeleide configuraties in LCS op te slaan, moeten de volgende stappen worden uitgevoerd, zolang LCS nog steeds toegankelijk is.

1. Als er nog geen RFS-exemplaar beschikbaar is, richt u er een in. Zie [RCS-overzicht](rcs-overview.md) voor meer informatie.
2. Registreer in het ingerichte RCS-exemplaar voor elk LCS-project in de activabibliotheek met afgeleide ER-configuraties, de juiste LCS-opslagplaats.
3. Importeer de ER-configuraties vanuit de LCS-opslagplaatsen naar RCS. Zie [Configuraties importeren vanuit LCS](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services) voor meer informatie.
4. Als de algemene opslagplaats niet automatisch is opgegeven, registreert u deze in RCS.
5. Upload alle afgeleide configuraties van het huidige RCS-exemplaar naar de algemene opslagplaats. Gebruik de functie **Configuratiepakketten** om te helpen bij het uploaden. Zie [Algemene RCS-opslagplaats uploaden](rcs-global-repo-upload.md) voor meer informatie.

### <a name="going-forward"></a>Verder

Gebruik de visuele ontwerpers in RCS voor de volgende doeleinden:

- De door Microsoft geleverde sjablonen uitbreiden.
- Nieuwe configuraties maken die uw organisatie nodig heeft.
- Globalisatiefuncties aanpassen voor elektronische facturering en de belastingberekeningsservice.

Gebruik de algemene opslagplaats voor de volgende doeleinden:

- Toegang krijgen tot door Microsoft geproduceerde configuraties en globalisatiefuncties.
- Configuraties die u hebt gemaakt of uitgebreid, uploaden naar de algemene opslagplaats voor opslag en deze gebruiken in de Dynamics 365-toepassingsomgevingen van uw organisatie of delen met externe organisaties. Zie [ER-configuratie in RCS maken en uploaden naar de algemene opslagplaats](rcs-global-repo-upload.md) voor meer informatie.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Betekent deze wijziging dat LCS niet kan worden gebruikt als centrale opslag voor configuraties?

Ja. De functionaliteit waarmee u configuraties kunt uploaden naar de projectactivabibliotheek in LCS vanuit apps voor financiën en bedrijfsactiviteiten, wordt gedeactiveerd. U kunt echter desgewenst de browser in LCS blijven gebruiken om configuraties naar de projectactivabibliotheek te uploaden.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ik had het idee dat RFS een vervangingsopslagplaats was voor het importeren van algemene sjabloonbestanden. En niet dat RFS wordt gebruikt om configuraties op te slaan. Wat is juist?

RCS is een ontwerpservice voor het maken en bewerken van ER-configuraties. RCS heeft een eigen opslagplaats die bekend staat als de algemene opslagplaats. Deze opslagplaats wordt gebruikt om configuraties op te slaan die in RCS worden gemaakt. Nadat het gebruik van LCS als opslag is afgeschaft, is de algemene opslagplaats de enige bron voor Microsoft-configuraties. U moet een eenmalige actie uitvoeren om alle benodigde configuraties vanuit LCS te importeren naar RCS en ze vervolgens te publiceren vanuit RCS naar de algemene opslagplaats.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Wat is zonder LCS de voorgestelde manier om configuraties op te slaan zodat configuraties voor "test" en "productie" eenvoudig kunnen worden beheerd en overgedragen?

Voor RCS wordt het concept van een *verbonden toepassing* gebruikt. Een verbonden toepassing vormt een verbinding tussen RCS en elk exemplaar van apps voor financiën en bedrijfsactiviteiten. Omdat RCS kan worden gebruikt voor het bewerken van configuraties, kan de verbonden toepassing worden gebruikt om de configuraties rechtstreeks van de ontwerper naar omgevingen voor apps voor financiën en bedrijfsactiviteiten te pushen. Hierdoor kunt u de configuraties snel wijzigen en testen in plaats van dat u de LCS-opslag op projectniveau moet doorlopen.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Zijn er voorbeelden waarin de instellingen en het beheer worden getoond?

Er zijn geen voorbeelden, maar u kunt de stappen eerder in dit artikel uitvoeren om uw configuraties te migreren naar de algemene opslagplaats voor RCS.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Is RCS een voorwaarde voor het configureren van elektronische rapportage?

Ja. RCS biedt mogelijkheden ter ondersteuning van het instellen van globalisatiefuncties die worden gebruikt door globalisatieservices, zoals elektronische facturering en de belastingberekeningsservice. De service heeft echter dezelfde visuele-ontwerperfunctionaliteit waarmee u ER-configuraties kunt uitbreiden of nieuwe ER-configuraties kunt maken. RCS biedt ook levenscyclusbeheer voor zowel ER-configuraties als globalisatiefuncties.

### <a name="which-regions-can-rcs-be-deployed-in"></a>In welke regio's kan RCS worden geïmplementeerd?

RCS is beschikbaar in de volgende Azure-regio's:

- Verenigde Staten
- India
- Frankrijk
- Europa

Zie [Overzicht van Dynamics-globalisatieservices](globalization-services-overview.md) voor meer informatie over productondersteuning. Zie [Dynamics 365 en Power Platform: beschikbaarheid, gegevenslocatie, taal en lokalisatie](https://aka.ms/rcs/D365Productavailabilityguide) voor meer informatie over geografische ondersteuning.

### <a name="whats-the-cost-of-using-rcs"></a>Wat zijn de kosten voor het gebruik van RCS?

RCS en de algemene opslagplaats worden gratis geleverd als onderdeel van bestaande licenties voor apps voor financiën en bedrijfsactiviteiten. Er zijn geen aparte kosten verbonden aan het gebruik van de ontwerpservice van RCS of het opslaan van configuraties in de algemene opslagplaats. Er is momenteel geen limiet voor het aantal configuraties of gekoppelde toepassingen.
