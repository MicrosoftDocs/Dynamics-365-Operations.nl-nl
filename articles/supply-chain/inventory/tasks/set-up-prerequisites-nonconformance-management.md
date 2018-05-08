---
title: Vereisten voor beheer instellen
description: Met deze procedure kunt u de processen van het niet-conformeringsbeheer inschakelen.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4bb4af7cb7aff101a8b9e6162823515f63b12886
ms.openlocfilehash: 9b5b05a3c00f093066a2714964bb99146427c3bc
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-prerequisites-for-management"></a>Vereisten voor beheer instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Met deze procedure kunt u de processen van het niet-conformeringsbeheer inschakelen. Met een niet-conformering wordt een artikel met kwaliteitsproblemen beschreven, waarbij de omschrijvende informatie de bron en het type probleem bevat. Deze procedure gebruikt het demobedrijf USMF. Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsmanager.


## <a name="enable-quality-management-processes-within-the-company"></a>Kwaliteitsbeheerprocessen binnen het bedrijf inschakelen
1. Ga naar Voorraadbeheer > Instellingen > Parameters voor voorraad- en magazijnbeheer.
2. Klik op het tabblad Kwaliteitsbeheer.
3. Selecteer Ja in het veld Kwaliteitsbeheer gebruiken.
    * Selecteer deze parameter om kwaliteitsbeheerprocessen voor het bedrijf in te schakelen.  
4. Voer een getal in het veld Uurtarief in.
    * Gebruik het veld Uurtarief om een uurtarief in de lokale valuta in te voeren. Het uurtarief wordt gebruikt voor het berekenen van de kosten voor bewerkingen die zijn gerelateerd aan een non-conformiteit. Het uurtarief en de berekende kosten vormen referentiegegevens voor een non-conformiteit en ze worden niet gebruikt door andere functionaliteit.  
5. Klik op Rapportinstellingen.
    * Op deze pagina definieert u de notitietypen voor kwaliteitsrapporten die worden gebruikt in verschillende typen kwaliteitsbeheerrapporten.  
6. Sluit de pagina.
7. Sluit de pagina.

## <a name="enable-user-for-nonconformance-processing"></a>Gebruiker voor niet-conformeringsverwerking inschakelen
1. Ga naar Systeembeheer > Gebruikers > Gebruikers.
    * Om de goedkeuring van een niet-conformering te verwerken, moet aan de gebruiker die niet-conformeringen goedkeurt of afwijst, de waarde 'Naam' worden toegewezen op de pagina Gebruikers. Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.  
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Naam met de waarde 'Ricardo'.
    * Gebruik het filter om de gebruiker te zoeken die de niet-conformeringsrecords goedkeurt of afwijst.  
3. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Om de goedkeuring van een niet-conformering te verwerken, moet u ervoor zorgen dat aan de gebruiker die niet-conformeringen goedkeurt of afwijst, de waarde 'Naam' is toegewezen op de pagina Gebruikers.  
4. Klik op Gebruikersopties.
5. Klik op het tabblad Voorkeuren.
6. Selecteer Ja in het veld Documentverwerking inschakelen.
    * Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.  
7. Sluit de pagina.
8. Sluit de pagina.
9. Sluit de pagina.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Typen diagnose voor niet-conformeringsverwerking definiëren
1. Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Typen diagnose.
    * Gebruik de pagina Diagnosetypen om een classificatie van diagnostische acties te definiëren. Met een correctie definieert u welk type diagnostische actie moet worden uitgevoerd voor een goedgekeurde non-conformiteit, wie deze moet uitvoeren en wat de aangevraagde en geplande voltooiingsdatum is.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Diagnose.
4. Typ een waarde in het veld Omschrijving.
5. Sluit de pagina.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Kwaliteitstoeslagen voor niet-conformeringsverwerking definiëren
1. Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitstoeslagen.
    * Gebruik de pagina van Kwaliteitstoeslagen om een classificatie van toeslagen te definiëren die wordt gebruikt in bewerkingen die zijn gerelateerd aan niet-conformeringen.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Toeslagcode.
4. Typ een waarde in het veld Omschrijving.
5. Sluit de pagina.

## <a name="define-the-operations-for-nonconformance-processing"></a>De bewerkingen voor niet-conformeringsverwerking definiëren
1. Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Bewerkingen.
    * Gebruik de pagina Bewerkingen om een classificatie te definiëren voor het werk dat kan worden uitgevoerd voor een goedgekeurde niet-conformering. Wanneer u een bewerking relateert aan een niet-conformering, kunt u informatie over het bijbehorende materiaal, gekoppelde werkuren en diverse toeslagen definiëren die vereist zijn om de bewerking uit te voeren. Deze informatie vormt de basis voor het berekenen van de geschatte kosten voor de uitvoering van de bewerking.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Bewerking.
4. Typ een waarde in het veld Omschrijving.
5. Sluit de pagina.

## <a name="define-problem-types-for-nonconformance-processing"></a>Probleemtypen voor niet-conformeringsverwerking definiëren
1. Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Probleemtypen.
    * Gebruik de pagina Probleemtypen om een classificatie te definiëren van de kwaliteitsproblemen die zich voordoen in de verschillende niet-conformeringstypen. De niet-conformeringstypen omvatten Intern, Klant, Leverancier, Serviceaanvraag, Productie en Productie van coproducten. Één probleemtype kan aan meerdere niet-conformeringstypen worden gekoppeld.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Probleemtype.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Niet-conformeringstypen.
    * Gebruik de pagina Niet-conformeringstypen om het gebruik van een probleemtype te autoriseren voor een of meer niet-conformeringstypen. Een probleemtype voor een defectcode kan bijvoorbeeld van toepassing zijn op alle non-conformiteitstypen, terwijl een probleemtype voor klachten van klanten alleen van toepassing is op de non-conformiteitstypen voor klanten en serviceaanvragen.  
6. Klik op Nieuw.
7. Markeer in de lijst de geselecteerde rij.
8. Selecteer een optie in het veld Niet-conformeringstype.
9. Sluit de pagina.
10. Sluit de pagina.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Quarantainezones voor niet-conformeringsverwerking definiëren
1. Ga naar Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Quarantainezones.
2. Klik op Nieuw.
3. Typ een waarde in het veld Quarantainezone.
4. Typ een waarde in het veld Omschrijving.
5. Sluit de pagina.

