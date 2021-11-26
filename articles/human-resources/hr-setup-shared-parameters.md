---
title: Gedeelde parameters configureren
description: In dit onderwerp wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 039d8e2100824921d568c013fe3e113e1b091979
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729094"
---
# <a name="configure-shared-parameters"></a>Gedeelde parameters configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals **Positie** records. In dit onderwerp wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.

Bepaalde typen records, zoals **positierecords** worden gedeeld tussen bedrijven. Voor deze records moet u gedeelde parameters instellen. De pagina **Gedeelde Human resources-parameters** wordt bijvoorbeeld gebruikt om human resources-parameters in te stellen voor rechtspersonen. 

Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit. 

### <a name="settings"></a>Instellingen
Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven. U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren. Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**. Om een nieuw identificatietype te definiëren of de lijst met bestaande typen te controleren, gaat u naar **Personeelsbeheer** &gt; **Koppelingen** &gt; **Instellingen** &gt; **Identificatietypen**. U kunt eenvoudige code en omschrijving invoeren. 

Op het tabblad **Nummerreeksen** kunt u de nummerreeksen kiezen die voor de volgende records gebruikt worden: **Personeelsnummer**, **Positie**, **Gebruikersaanvraag-id**, **I-9 document**, **Sollicitant**, **Discussie**, **Vergoeding-id** en **Personeelsactie** (als dit recordtype ingeschakeld is). Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**. U kunt deze pagina vinden via de paginazoekfunctie. 

Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:

- **Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.
- **Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Als u deze optie selecteert, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar komt. Voer vervolgens op het tabblad **Algemeen** de datum voor **Beschikbaar voor toewijzing** in om medewerkertoewijzing in te schakelen.

Op het tabblad **Geavanceerde toegang** kunt u de toegang beperken tot bepaalde gegevens of koppelingen:

- **Toegang tot werknemersgegevens beperken**: selecteer deze functie als gebruikers werknemersgegevens alleen mogen bekijken voor rechtspersonen waartoe ze toegang hebben, en voor medewerkers die een dienstverband hebben in deze rechtspersonen.

    Nadat deze functie is geselecteerd, moet u de volgende stappen volgen om de juiste machtigingen in te stellen voor elke gebruiker van wie de weergave moet worden beperkt:

    1. Selecteer een gebruiker op de pagina **Gebruikers**.
    1. Selecteer een rol voor de gebruiker. De optie **Organisaties toewijzen** komt beschikbaar.
    1. Selecteer **Organisaties toewijzen**.
    1. Selecteer op de nieuwe pagina **De toegang verlenen tot specifieke organisaties** en selecteer vervolgens de organisaties waartoe de gebruiker toegang moet hebben.
    1. Herhaal stap 2 tot en met 4 voor elke extra rol die de gebruiker heeft, inclusief de rol van de systeemgebruiker.

    > [!NOTE]
    > De bedrijven waartoe een gebruiker toegang heeft, moeten overeenkomen met alle rollen van de gebruiker.

- **Compensatieweergave voor bedrijven inschakelen**: compensatie voor werknemers wordt toegewezen per rechtspersoon van dienstverband. Soms kan een werknemer in dienst zijn bij meerdere rechtspersonen tegelijk. Wanneer deze functie is geselecteerd, wordt de compensatie voor elke rechtspersoon weergegeven in **Selfservice werknemer** en **Selfservice manager** zonder dat u van rechtspersoon hoeft te veranderen. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
