---
title: Genereren en uitvoeren van kant-en-klare rapporten
description: Gebruik deze taakbegeleider om kant-en-klare rapporten uit te voeren in Headquarters vanuit verschillende werkgebieden en query's en verkooprapporten in Commerce.
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
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e11bca1e6850f401f52c2ccbea1089a4e71591c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003698"
---
# <a name="generate-and-run-out-of-box-reports"></a>Genereren en uitvoeren van kant-en-klare rapporten

[!include [banner](../includes/banner.md)]

Gebruik deze taakbegeleider om kant-en-klare rapporten uit te voeren in Headquarters vanuit verschillende werkgebieden en query's en verkooprapporten in Commerce.

Het demobedrijf dat wordt gebruikt om deze registratie te maken is USRT. Deze registratie is bedoeld voor de systeembeheerdersrol.

## <a name="launch-reports-from-workspaces"></a>Rapporten starten vanuit werkgebieden
1. Ga naar Detailhandel en commerce > Producten en categorieën > Categorie- en productbeheer.
2. Klik op de pijl om de sectie Rapporten uit te vouwen of samen te vouwen.
3. Klik op Rapport Topproducten.
4. Voer een datum in het veld Begindatum in.
5. Voer een datum in het veld Einddatum in.
6. Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\Central\Houston'.
    * Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor rapportagedoeleinden in Commerce.   Ga naar Organisatiebeheer > Organisaties > Doelstellingen voor organisatiehiërarchie, kies Commerce-rapportage en controleer onder Toegewezen hiërarchieën de hiërarchienaam waarvoor de Standaardkolom is ingeschakeld. Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Winkels per regio de standaardorganisatiehiërarchie is voor rapportagedoeleinden.     
8. Klik op OK.
9. Selecteer een optie in het veld Weergeven.
10. Selecteer een optie in het veld Op.
11. Klik op OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>Rapporten starten vanuit de query- en verkooprapporten
1. Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van categorie.
2. Voer een datum in het veld Begindatum in.
3. Voer een datum in het veld Einddatum in.
4. Klik in het veld Kanaal op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer in de structuur 'Contoso Retail\Contoso Retail USA\West\Seattle'.
    * Dit toont de standaardhiërarchie voor detailhandelsorganisaties voor rapportagedoeleinden in Commerce. Ga naar Organisatiebeheer > Organisaties > Doelstellingen voor organisatiehiërarchie, kies Commerce-rapportage en controleer onder Toegewezen hiërarchieën de hiërarchienaam waarvoor de Standaardkolom is ingeschakeld. Als onderdeel van demogegevens (gebruikt voor taakregistratie) ziet u dat Winkels per regio de standaardorganisatiehiërarchie is voor rapportagedoeleinden.     
6. Klik op OK.
7. Klik op OK.

## <a name="export-an-hq-reports"></a>Een hoofdkantoorrapport exporteren
1. Ga naar Detailhandel en commerce > Query's en rapporten > Verkooprapporten > Rapport Verkoop van organisatie.
2. Voer een datum in het veld Begindatum in.
3. Voer een datum in het veld Einddatum in.
4. Klik op OK.
5. Klik op Exporteren.
6. Klik op PDF.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]