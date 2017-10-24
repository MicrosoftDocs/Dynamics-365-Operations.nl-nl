---
title: Bedrijfsspecifieke HR-parameters instellen
description: De instellingen van bepaalde parameters van Human Resources (HR) worden in alle bedrijven gedeeld, terwijl de instellingen van andere parameters bedrijfsspecifiek zijn. In dit artikel wordt uitgelegd hoe u bedrijfsspecifieke HR-parameters instelt.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c280b5ae3b8fc208759ec486db0a1015a9c24633
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-company-specific-hr-parameters"></a>Bedrijfsspecifieke HR-parameters instellen

[!include[banner](includes/banner.md)]


De instellingen van bepaalde parameters van Human Resources (HR) worden in alle bedrijven gedeeld, terwijl de instellingen van andere parameters bedrijfsspecifiek zijn. In dit artikel wordt uitgelegd hoe u bedrijfsspecifieke HR-parameters instelt.

Twee pagina's worden gebruikt om de parameters voor Human resources (HR) in te stellen. Voor parameters die door bedrijven worden gedeeld, gebruikt u de pagina **Gedeelde Human resources-parameters**. Voor parameters die bedrijfsspecifiek zijn (met andere woorden, de instellingen gelden voor één bedrijf), gebruikt u de pagina **Parameters personeel**. Op de **Human resources-parameters** pagina, zijn de instellingen verdeeld over zes tabbladen:

-   Algemeen
-   Werving: dit maakt geen deel uit van Dynamics 365 for Talent
-   Compensatie
-   Nummerreeksen
-   Family and Medical Leave Act (FMLA)
-   Selfservice werknemer

Elk tabblad bevat informatie over één bedrijf. De instellingen op het tabblad **Algemeen** bepalen het uiterlijk van informatie over verzuim, letsel en ziekte, en nieuwe werknemers. De instellingen op dit tabblad definieert tevens sommige standaardwaarden die worden weergegeven terwijl u werkt. In het bijzonder kunt u met dit tabblad de kleur selecteren die u op openstaande verzuimtransacties wilt toepassen, het gewenste opmaakmodel voor rapporten opgeven, definiëren of de integratie tussen cursussen en verzuimregistratie moet worden geactiveerd en de verzuimcode selecteren die wordt gebruikt voor het beheren van deze integratie. U kunt ook aangeven hoe een casus met letsel- of ziekte-incidenten moet worden bewaard, en het standaardidentificatienummer opgeven dat wordt weergegeven wanneer een nieuwe werknemer in dienst wordt genomen. 

De instellingen op het tabblad **Werving** definiëren de documenttypen die worden gebruikt voor correspondentie die automatisch naar sollicitanten worden verzonden en het wervingsproject dat worden gebruikt voor open sollicitaties (sollicitaties die niet specifiek voor een wervingsproject zijn). De periode die is gedefinieerd als ouderdomsperiode voor het wervingsproject bepaalt de wervingsprojecten die zijn opgenomen op de tegel **Verouderende projecten** in de werkruimte **Wervingsbeheer**. De periode die wordt ingesteld voor de sollicitatiedeadlinewaarschuwing wordt gebruikt om wervingsprojecten weer te geven die hun sollicitatiedeadline naderen op de tegel **Einde van sollicitatietermijn nadert** in de werkruimte **Werving**. 

De instellingen op het tabblad **Compensatie** definiëren of gebruikers moeten bevestigen dat ze informatie willen opslaan voor een vaste- of variabele-compensatieplan. Als u het selectievakje **Opslaan van validatie activeren** inschakelt, wordt een gebruiker wanneer hij of zij een compensatie-gerelateerde pagina afsluit, gevraagd of hij of zij de record wil opslaan. Op sommige pagina's in compensatiebeheer kunnen gebruikers geen gegevens verwijderen.. Door gebruikers te vragen of ze gegevens daadwerkelijk willen opslaan, worden er mogelijk minder gegevens opgeslagen die naderhand niet meer kunnen worden verwijderd. Als het selectievakje **Opslaan van validatie activeren** is uitgeschakeld, worden records altijd direct opgeslagen, misschien voordat de gebruiker klaar is. Als u prestatiebeheer gebruikt, kunt u met het tabblad **Compensatie** ook een beoordelingsmodel selecteren om te gebruiken in plaats van het model dat wordt toegewezen aan compensatieplannen wanneer prestaties worden beoordeeld. 

### <a name="previously-released-functionality"></a>Eerder uitgebrachte functionaliteit
De instellingen op het tabblad **Nummerreeks** bepalen de reeksen die worden gebruikt voor het automatisch toewijzen van id's aan items in Human resources, zoals sollicitaties, verzuimregistraties, resultaten van compensatieprocessen, casenummers, cursussen en cursusagenda's. Om nummerreeksverwijzingen en codes te onderhouden, gebruikt u de lijstpagina **Nummerreeksen**. Klik op **Organisatiebeheer** &gt; **Nummerreeksen** &gt; **Nummerreeksen**.

### <a name="if-youre-using-dynamics-365-for-talent"></a>Als u Dynamics 365 for Talent gebruikt
De instellingen op het tabblad **Nummerreeks** bepalen de reeksen die worden gebruikt voor het automatisch toewijzen van id's aan items in Human resources, zoals sollicitaties, verzuimregistraties, resultaten van compensatieprocessen, casenummers, cursussen en cursusagenda's. Om nummerreeksverwijzingen en codes te onderhouden, gebruikt u de lijstpagina **Nummerreeksen**. Klik op **Systeembeheer** &gt; tabblad **Koppelingen** &gt; **Nummerreeksen** &gt; **Nummerreeksen**. 

De instellingen op het tabblad **FMLA** bepalen hoeveel uren een werknemer moet werken om in aanmerking te komen voor FMLA-vergoedingen, de duur van het dienstverband dat is vereist om in aanmerking te komen en de begindatum van het dienstverband die wordt gebruikt om de duur van het dienstverband te definiëren. De instellingen bepalen ook het aantal FMLA-uren waarop werknemers recht hebben en de FMLA-verlofkalender die wordt gebruikt om te berekenen hoeveel FMLA-uren werknemers hebben gebruikt. Het tabblad **FMLA** is alleen beschikbaar voor bedrijven in de Verenigde Staten. 

**Opmerking:** Het aantal uren dat is gewerkt, kan niet groter zijn dan 1,250, en de lengte van het dienstverband kan niet langer dan 12 maanden zijn. Deze maximumwaarden zijn in overeenstemming met de federale wetgeving in de verenigde Staten. Tot slot bepalen de instellingen op het tabblad **Selfservice werknemer** welke informatie een manager kan invoeren namens zijn of haar werknemers.

<a name="see-also"></a>Zie ook
--------

[HR-parameters instellen voor rechtspersonen](set-up-hr-parameters-across-legal-entities.md)




