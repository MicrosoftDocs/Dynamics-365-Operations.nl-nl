---
title: Gedeelde parameters configureren
description: U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.
author: andreabichsel
ms.date: 06/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66f57c9613ba04ebb3748699105469586c27d66131c062d1af286b24199c4be7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723642"
---
# <a name="configure-shared-parameters"></a>Gedeelde parameters configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U moet gedeelde parameters instellen voor records die tussen bedrijven worden gedeeld, zoals Positierecords. In dit artikel wordt uitgelegd hoe u Human Resources-parameters instelt voor alle rechtspersonen.

Bepaalde typen records, zoals positierecords worden gedeeld tussen bedrijven. Voor deze records moet u gedeelde parameters instellen. U gebruikt bijvoorbeeld **Gedeelde Human resources-parameters** om human resources-parameters in te stellen voor rechtspersonen. 

Op de **Gedeelde Human resources-parameters** pagina worden de parameters gegroepeerd in gebieden, op basis van hun functionaliteit. 

### <a name="settings"></a>Instellingen
Op het **Identificatie** tabblad, moet u de identificatietypen selecteren die de identificatienummers vertegenwoordigen die op de pagina worden weergeven. U moet identificatietypen instellen voordat u identificatiegegevens voor werknemers kunt invoeren. Informatie over het burgerservicenummer, het nationale id-nummer, het vreemdelingen-id-nummer en de persoonlijke id-code wordt onderhouden op de pagina **Identificatietype**. Om een nieuw identificatietype te definiëren of de lijst met bestaande typen te controleren, klikt u op **Personeelsbeheer** &gt; tabblad **Koppelingen** &gt; **Instellingen** &gt; **Identificatietypen**. U kunt eenvoudige code en omschrijving invoeren. 

Op het **Nummerreeksen** tabblad, kunt u nummerreeksen selecteren die voor de volgende records worden gebruikt: Het personeelsnummer, Positie, ID gebruikersaanvraag, I-9-document, Sollicitant, Discussie, Vergoeding-id en personeelsactie (als dit recordtype is ingeschakeld). Voor het verzorgen van verwijzingen en codes, gebruikt u de lijstpagina **Nummerreeksen**. U kunt deze pagina vinden via de paginazoekfunctie. 

Op het **Posities** tabblad, geeft u aan of de nieuwe posities beschikbaar zijn voor standaard toewijzing:

- **Altijd:** U kunt werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Wanneer posities worden gemaakt, worden de datum en tijd van **Beschikbaar voor toewijzing** op het tabblad **Algemeen** van de pagina **Positie** automatisch ingesteld op de aanmaakdatum- en tijd.
- **Nooit** – U kunt geen werknemers toewijzen aan nieuwe posities wanneer posities worden gemaakt. Als u deze optie selecteert, moet u de pagina **Positie** openen voor elke nieuwe positie zodra deze beschikbaar komt. Voer vervolgens op het tabblad **Algemeen** de datum voor **Beschikbaar voor toewijzing** in om medewerkertoewijzing in te schakelen.

Op het tabblad **Geavanceerde toegang** kunt u de toegang beperken tot bepaalde gegevens of koppelingen:

- **Toegang tot werknemersgegevens beperken**: schakel deze functie in als gebruikers werknemersgegevens alleen mogen bekijken voor rechtspersonen waartoe ze toegang hebben, en voor werknemers die een dienstverband hebben in deze rechtspersonen.

    Nadat deze functie is ingeschakeld, moet u de volgende stappen volgen om de juiste machtigingen in te stellen voor elke gebruiker van wie de weergave moet worden beperkt:

    1. Selecteer een gebruiker op de pagina **Gebruikers**.
    1. Selecteer een rol voor de gebruiker. De optie **Organisaties toewijzen** komt beschikbaar.
    1. Selecteer **Organisaties toewijzen**.
    1. Selecteer op de nieuwe pagina **De toegang verlenen tot specifieke organisaties** en selecteer vervolgens de organisaties waartoe de gebruiker toegang moet hebben.
    1. Herhaal stap 2 tot en met 4 voor elke andere rol die de gebruiker heeft, inclusief de rol van de systeemgebruiker.

    > [!NOTE]
    > De bedrijven waartoe een gebruiker toegang heeft, moeten overeenkomen met alle rollen van de gebruiker.

- **Compensatieweergave voor bedrijven inschakelen**: compensatie voor werknemers wordt toegewezen per rechtspersoon van dienstverband. Soms kan een werknemer in dienst zijn bij meerdere rechtspersonen tegelijk. Wanneer deze functie is ingeschakeld, wordt de compensatie voor elke rechtspersoon weergegeven in Selfservice werknemer en Selfservice manager zonder dat u van rechtspersoon hoeft te veranderen. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
