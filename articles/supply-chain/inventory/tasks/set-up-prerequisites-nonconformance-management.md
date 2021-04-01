---
title: Vereisten voor niet-conformeringsbeheer instellen
description: Met dit onderwerp kunt u de processen van het niet-conformeringsbeheer inschakelen.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e30f110e5f0008e66ec4781a35368a75143b565
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244322"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Vereisten voor niet-conformeringsbeheer instellen

[!include [banner](../../includes/banner.md)]

Met dit onderwerp kunt u de processen van het niet-conformeringsbeheer inschakelen. Met een niet-conformering wordt een artikel met kwaliteitsproblemen beschreven, waarbij de omschrijvende informatie de bron en het type probleem bevat. Deze procedure gebruikt het demobedrijf USMF. Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsmanager.


## <a name="enable-quality-management-processes-within-the-company"></a>Kwaliteitsbeheerprocessen binnen het bedrijf inschakelen
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellen > Parameters voor voorraad- en magazijnbeheer**.
2. Selecteer het tabblad **Kwaliteitsbeheer**.
3. Selecteer **Ja** in het veld **Kwaliteitsbeheer** om processen voor kwaliteitsbeheer voor het bedrijf in te schakelen.
4. Voer in het veld **Uurtarief** een uurtarief in de lokale valuta in. Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een non-conformiteit. Het uurtarief en de berekende kosten vormen referentiegegevens voor een non-conformiteit en ze worden niet gebruikt door andere functionaliteit.  
5. Selecteer **Rapport instellen** om de notitietypen voor kwaliteitsrapporten op te geven die worden gebruikt in verschillende typen kwaliteitsbeheerrapporten.

## <a name="enable-user-for-nonconformance-processing"></a>Gebruiker voor niet-conformeringsverwerking inschakelen
1. Ga in het navigatievenster naar **Modules > Systeembeheer > Gebruikers > Gebruikers**. 
2. Gebruik het snelfilter om de gebruiker te zoeken die de niet-conformeringsrecords goedkeurt of afwijst. Filter bijvoorbeeld op het veld **Naam** met de waarde `Ricardo`. Om de goedkeuring van een niet-conformering te verwerken, moet aan de gebruiker die niet-conformeringen goedkeurt of afwijst, de waarde Naam worden toegewezen op de pagina **Gebruikers**. Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.  
3. Markeer de rij van de gewenste record.
4. Selecteer **Gebruikersopties**.
5. Selecteer het tabblad **Voorkeuren**.
6. Selecteer **Ja** in het veld **Documentverwerking inschakelen**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Typen diagnose voor niet-conformeringsverwerking definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Typen diagnose**. Gebruik de pagina **Diagnosetypen** om een classificatie van diagnostische acties te definiëren. Met een correctie definieert u welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde non-conformiteit, wie deze moet uitvoeren en wat de aangevraagde en geplande voltooiingsdatum is.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Diagnose**.
4. Typ een waarde in het veld **Beschrijving**.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Kwaliteitstoeslagen voor niet-conformeringsverwerking definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitstoeslagen**. Gebruik de pagina **Kwaliteitstoeslagen** om een classificatie van toeslagen te definiëren die wordt gebruikt in bewerkingen die zijn gerelateerd aan niet-conformeringen.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Toeslagcode**.
4. Typ een waarde in het veld **Beschrijving**.

## <a name="define-the-operations-for-nonconformance-processing"></a>De bewerkingen voor niet-conformeringsverwerking definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Bewerkingen**. Gebruik de pagina **Bewerkingen** om een classificatie te definiëren voor het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering. Wanneer u een bewerking relateert aan een niet-conformering, kunt u informatie over het bijbehorende materiaal, gekoppelde werkuren en diverse toeslagen definiëren die vereist zijn om de bewerking uit te voeren. Deze informatie vormt de basis voor het berekenen van de geschatte kosten voor de uitvoering van de bewerking.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Bewerking**.
4. Typ een waarde in het veld **Beschrijving**.

## <a name="define-problem-types-for-nonconformance-processing"></a>Probleemtypen voor niet-conformeringsverwerking definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Probleemtypen**. Gebruik de pagina **Probleemtypen** om een classificatie te definiëren van de kwaliteitsproblemen die zich voordoen in de verschillende niet-conformeringstypen. De niet-conformeringstypen omvatten **Intern**, **Klant**, **Leverancier**, **Serviceaanvraag**, **Productie** en **Productie van coproducten**. Één probleemtype kan aan meerdere niet-conformeringstypen worden gekoppeld.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Probleemtype**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer **Non-conformiteitstypen**. Gebruik de pagina **Niet-conformeringstypen** om het gebruik van een probleemtype te autoriseren voor een of meer niet-conformeringstypen. Een probleemtype voor een defectcode kan bijvoorbeeld van toepassing zijn op alle non-conformiteitstypen, terwijl een probleemtype voor klachten van klanten alleen van toepassing is op de non-conformiteitstypen voor klanten en serviceaanvragen.  
6. Selecteer **Nieuw**.
7. Selecteer een optie in het veld **Niet-conformeringstype** van de nieuwe rij.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Quarantainezones voor niet-conformeringsverwerking definiëren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Quarantainezones**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Quarantainezone**.
4. Typ een waarde in het veld **Beschrijving**.
5. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]