---
title: HR-parameters instellen voor rechtspersonen
description: U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: 5df6079605d2d8d320c38d302e8e5e2cba51a3f1
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>HR-parameters instellen voor rechtspersonen

U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.

Bepaalde typen records, zoals positierecords worden gedeeld tussen bedrijven. Voor deze records moet u gedeelde parameters instellen. U gebruikt bijvoorbeeld **Gedeelde Human resources-parameters** om human resources-parameters in te stellen voor rechtspersonen. 

Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit. 

Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven. U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren. Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**. Als u wilt een nieuwe ID-type definieert of bekijk de lijst met bestaande typen, klikt u op **Human resources**&gt;**Setup**&gt;**identificatietypen**. U kunt eenvoudige code en omschrijving invoeren. 

Op het **Nummerreeksen** tabblad, kunt u nummerreeksen selecteren die voor de volgende records worden gebruikt: Het personeelsnummer, Positie, ID gebruikersaanvraag, I-9-document, Sollicitant, Discussie, Vergoeding-id en personeelsactie (als dit recordtype is ingeschakeld). Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**. U kunt deze pagina vinden via de paginazoekfunctie. 

Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:

-   **Altijd** : U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Wanneer posities worden gemaakt, de **beschikbaar voor toewijzing** datum en tijd op de **algemeen** tabblad van de **positie** pagina automatisch ingesteld op de aanmaakdatum en -tijd.
-   **Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Als u deze optie hebt geselecteerd, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar wordt en vervolgens op het tabblad **Algemeen** de datum **Beschikbaar voor toewijzing **invoeren om de werknemerstoewijzing in te schakelen.


<a name="see-also"></a>Zie ook
--------

[Bedrijf specifieke HRM-parameters instellen](set-up-company-specific-hr-parameters.md)


