---
title: Parameters voor HR-resources instellen voor rechtspersonen
description: U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: cc5acf7ba1b350ee2c91923c7de3b4780385f3ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303821"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>Parameters voor HR-resources instellen voor rechtspersonen

[!include [banner](includes/banner.md)]

U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.

Bepaalde typen records, zoals positierecords worden gedeeld tussen bedrijven. Voor deze records moet u gedeelde parameters instellen. U gebruikt bijvoorbeeld **Gedeelde Human resources-parameters** om human resources-parameters in te stellen voor rechtspersonen. 

Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit. 

### <a name="previously-released-functionality"></a>Eerder uitgebrachte functionaliteit
Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven. U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren. Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**. Om een nieuw identificatietype te definiëren of de lijst met bestaande typen te controleren, klikt u op **Personeelsbeheer** &gt; tabblad **Koppelingen** &gt; **Instellingen** &gt; **Identificatietypen**. U kunt eenvoudige code en omschrijving invoeren. 

### <a name="if-youre-using-dynamics-365-for-talent"></a>Als u Dynamics 365 for Talent gebruikt
Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven. U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren. Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**. Om een nieuw identificatie type te definiëren of de lijst met bestaande typen te controleren, klikt u op **HRM** &gt; **Instellen** &gt; **Identificatietypen**. U kunt eenvoudige code en omschrijving invoeren. 

Op het **Nummerreeksen** tabblad, kunt u nummerreeksen selecteren die voor de volgende records worden gebruikt: Het personeelsnummer, Positie, ID gebruikersaanvraag, I-9-document, Sollicitant, Discussie, Vergoeding-id en personeelsactie (als dit recordtype is ingeschakeld). Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**. U kunt deze pagina vinden via de paginazoekfunctie. 

Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:

-   **Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.
-   **Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Als u deze optie hebt geselecteerd, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar wordt en vervolgens op het tabblad **Algemeen** de datum **Beschikbaar voor toewijzing** invoeren om de werknemerstoewijzing in te schakelen.


<a name="additional-resources"></a>Aanvullende resources
--------

[Bedrijfsspecifieke HR-parameters instellen](set-up-company-specific-hr-parameters.md)



