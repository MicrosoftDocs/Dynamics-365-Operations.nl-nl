---
title: Genereren en uitvoeren van kant-en-klare rapporten
description: Gebruik deze taakbegeleiding om kant-en-klare rapporten op het hoofdkantoor uit te voeren vanuit verschillende werkgebieden en query's en verkooprapporten onder Detailhandel en commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "365242"
---
# <a name="generate-and-run-out-of-box-reports"></a>Genereren en uitvoeren van kant-en-klare rapporten

[!include[task guide banner](../includes/task-guide-banner.md)]

Gebruik deze taakbegeleiding om kant-en-klare rapporten op het hoofdkantoor uit te voeren vanuit verschillende werkgebieden en query's en verkooprapporten onder Detailhandel en commerce.



Het demobedrijf dat wordt gebruikt om deze registratie te maken is USRT. Deze registratie is bedoeld voor de systeembeheerdersrol.


## <a name="launch-reports-from-workspaces"></a>Rapporten starten vanuit werkgebieden
1. Ga naar Detailhandel en commerce > Producten en categorieën > Categorie- en productbeheer.
2. Klik op de pijl om de sectie Rapporten uit te vouwen of samen te vouwen.
3. Klik op Rapport Topproducten.
4. Voer een datum in het veld Begindatum in.
5. Voer een datum in het veld Einddatum in.
6. Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\Central\Houston'.
    * Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor detailhandelrapportagedoeleinden.   Ga naar Organisatiebeheer >Organisaties > Organisatiehiërarchiedoelstellingen en kies Detailhandelrapportage onder Toegewezen hiërarchieën, en controleer de hiërarchienaam waarvoor Standaardkolom is ingeschakeld.      Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Detailhandelwinkels per regio de standaardorganisatiehiërarchie is voor detailhandelrapportagedoeleinden.     
8. Klik op OK.
9. Selecteer een optie in het veld Weergeven.
10. Selecteer een optie in het veld Op.
11. Klik op OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a>Rapporten starten vanuit de query- en verkooprapporten onder de appkoppeling Detailhandel en commerce.
1. Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van categorie.
2. Voer een datum in het veld Begindatum in.
3. Voer een datum in het veld Einddatum in.
4. Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\West\Seattle'.
    * Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor detailhandelrapportagedoeleinden.   Ga naar Organisatiebeheer >Organisaties > Organisatiehiërarchiedoelstellingen en kies Detailhandelrapportage onder Toegewezen hiërarchieën, en controleer de hiërarchienaam waarvoor Standaardkolom is ingeschakeld.      Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Detailhandelwinkels per regio de standaardorganisatiehiërarchie is voor detailhandelrapportagedoeleinden.     
6. Klik op OK.
7. Klik op OK.

## <a name="export-an-hq-reports"></a>Een hoofdkantoorrapport exporteren
1. Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van organisatie.
2. Voer een datum in het veld Begindatum in.
3. Voer een datum in het veld Einddatum in.
4. Klik op OK.
5. Klik op Exporteren.
6. Klik op PDF.

