---
title: Inleiding tot functionele locaties
description: Dit onderwerp bevat een overzicht van functionele locaties in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d7d98ec5434d9cdc93276952035b559625be2bd
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783183"
---
# <a name="introduction-to-functional-locations"></a>Inleiding tot functionele locaties

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Dit onderwerp bevat een overzicht van functionele locaties in Activabeheer. Functionele locaties zijn elementen van een technische structuur, zoals de functionele eenheden in een systeem. Functionele locaties worden hiërarchisch gemaakt en u installeert hierop activa. De instelling van functionele locaties in uw bedrijf is afhankelijk van de vereisten van het bedrijf.

Hier volgen enkele voorbeelden van hoe u functionele locaties kunt gebruiken:

- **Functioneel**: de functionele locaties kunnen gebruikersgericht zijn en worden gebruikt om activa met soortgelijk gedrag te beheren.
- **Procesgerelateerd**: functionele locaties kunnen werkstroomgericht zijn.
- **Ruimtelijk**: de functionele locaties kunnen geografische locaties of sites vertegenwoordigen.

Elke functionele locatie wordt onafhankelijk beheerd in Activabeheer. Hier volgen enkele nuttige functies van functionele locaties:

- Specificaties voor functionele locaties instellen.
- Specificatievereisten voor activa instellen.
- Onderhoudsreeksen voor preventief en reactief onderhoud instellen.
- Geïnstalleerde activa beheren.
- Actieve aanvragen en werkorders bijhouden die zijn gerelateerd aan geïnstalleerde activa.
- Fouten bijhouden die zijn geregistreerd voor activa.
- Onderhoudskosten bijhouden voor de activa die op een bepaald moment zijn gerelateerd aan een functionele locatie.

Functionele locaties bieden traceerbaarheid van activa met betrekking tot aanvragen, werkorders, foutregistraties, toestandsbeoordelingen, productiestopregistraties en teller registraties voor activa.

> [!NOTE]
> Zelfs als een activum op verschillende functionele locaties is geïnstalleerd tijdens de levensduur, kunnen de kosten worden gerelateerd aan elke locatie. Met andere woorden, de activakosten zijn altijd gerelateerd aan de functionele locatie waarop het activum op een bepaald moment was geïnstalleerd.

Functionele locaties zijn **niet** flexibel. Daarom kunt u, nadat u een functionele locatiehiërarchie hebt ingesteld, geen locaties hierin verplaatsen. 

Nadat u een functionele locatiehiërarchie hebt gemaakt, bestaat de volgende stap uit het installeren van activa hierin. Zie [Activa installeren op functionele locaties](../functional-locations/install-objects-on-functional-locations.md) voor meer informatie.

## <a name="all-functional-locations"></a>Alle functionele locaties

Selecteer **Activabeheer** \> **Algemeen** \> **Functionele locaties** \> **Alle functionele locatie** om de lijstpagina **Alle functionele locaties** te openen. Op deze pagina worden alle functionele locaties weergegeven plus een deel van de informatie die aan elk hiervan is gerelateerd. Als u alleen actieve functionele locaties wilt weergeven, selecteert u **Actieve functionele locaties**. Als u alleen de functionele locatie die waaraan u bent gerelateerd als medewerker, selecteert u **Mijn actieve functionele locaties**. (Deze relatie is ingesteld op de pagina **Medewerkers**. Zie [Onderhoudsmedewerkers en medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor meer informatie.)

Selecteer op de lijstpagina **Alle functionele locaties** een koppeling in de kolom **Functionele locatie** om de details van de geselecteerde record weer te geven. Als u de functionele locatie wilt bewerken, selecteert u de knop **Bewerken**. De detailweergave bevat gedetailleerde informatie die is gerelateerd aan de locatie. Het bevat ook een deelvenster **Verwante informatie** aan de rechterkant. Dit deelvenster toont de hiërarchie van functionele locaties. U kunt het deelvenster **Verwante informatie** uitvouwen en samenvouwen.

De knoppen in het actievenster zijn geordend op tabbladen. In de volgende tabel worden kort de knoppen beschreven die betrekking hebben op Activabeheer.

| Knopnaam                         | Beschrijving                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Bewerken                                | Schakelen tussen de bewerkingsmodus en de weergavemodus voor de pagina.                                                                                         |
| Nieuw                                 | Een nieuwe functionele locatie maken.                                                                                                            |
| Verwijderen                              | De geselecteerde functionele locatie verwijderen.                                                                                                     |
| Hernoemen                              | De naam van de geselecteerde functionele locatie wijzigen.                                                                                                     |
| Functionele locatiestructuur kopiëren  | De hiërarchie van functionele locaties kopiëren.                                                                                                      |
| Activum installeren                       | Een activum installeren, met inbegrip van onderliggende activa, op de functionele locatie.                                                                        |
| Activum vervangen                       | De activahiërarchie vervangen door een andere activahiërarchie op de functionele locatie.                                                         |
| Kostenbeheer                        | Open de pagina **Kostenbeheer voor functionele locatie**, waar u een kostenberekening kunt uitvoeren voor de geselecteerde functionele locatie.                |
| Uurcontrole                        | Open de pagina **Uurcontrole voor functionele locatie**, waar u een kostenberekening kunt uitvoeren voor de geselecteerde functionele locatie.                |
| Activa                              | Open de pagina **Alle activa**, waar u een lijst met activa kunt weergeven die zijn gerelateerd aan de geselecteerde functionele locatie.                      |
| Aanvragen                            | Open de pagina **Actieve aanvragen**, waar u een lijst met aanvragen kunt weergeven die zijn gerelateerd aan de geselecteerde functionele locatie.               |
| Werkorders                         | Open de pagina **Actieve werkorders**, waar u een lijst met werkorders kunt weergeven die zijn gerelateerd aan de geselecteerde functionele locatie.         |
| Fouten                              | Open de pagina **Activafouten**, waar u een lijst met registraties van activafouten kunt weergeven die zijn gerelateerd aan de geselecteerde functionele locatie. |
| Status van functionele locatie bijwerken    | De fase van de geselecteerde functionele bijwerken.                                                                                        |
| Logboek voor levenscyclusstatus                 | Een logboek weergeven waarin de fasen van de geselecteerde functionele locatie worden weergegeven.                                                                        |
