---
title: Parameters voor Human Resources configureren
description: De instellingen van bepaalde parameters van Human Resources worden in alle bedrijven gedeeld, terwijl de instellingen van andere parameters bedrijfsspecifiek zijn. In dit artikel wordt uitgelegd hoe u bedrijfsspecifieke HR-parameters instelt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 131606ebaff49a2c63d22bcfdb5e523f4df87ec6
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129120"
---
# <a name="configure-human-resources-parameters"></a>Parameters voor Human Resources configureren

De instellingen van bepaalde parameters van Human Resources (HR) worden in alle bedrijven gedeeld, terwijl de instellingen van andere parameters bedrijfsspecifiek zijn. In dit artikel wordt uitgelegd hoe u bedrijfsspecifieke HR-parameters instelt.

Twee pagina's worden gebruikt om de parameters voor Human resources (HR) in te stellen. Voor parameters die door bedrijven worden gedeeld, gebruikt u de pagina **Gedeelde Human resources-parameters**. Voor parameters die bedrijfsspecifiek zijn (met andere woorden, de instellingen gelden voor één bedrijf), gebruikt u de pagina **Parameters personeel**. Op de **Human resources-parameters** pagina, zijn de instellingen verdeeld over zes tabbladen:

-   Algemeen
-   Werving - dit is niet opgenomen in Dynamics 365 Human Resources
-   Compensatie
-   Nummerreeksen
-   Family and Medical Leave Act (FMLA)
-   Selfservice werknemer

Elk tabblad bevat informatie over één bedrijf. De instellingen op het tabblad **Algemeen** bepalen het uiterlijk van informatie over verzuim, letsel en ziekte, en nieuwe werknemers. De instellingen op dit tabblad definieert tevens sommige standaardwaarden die worden weergegeven terwijl u werkt. In het bijzonder kunt u met dit tabblad de kleur selecteren die u op openstaande verzuimtransacties wilt toepassen, het gewenste opmaakmodel voor rapporten opgeven, definiëren of de integratie tussen cursussen en verzuimregistratie moet worden geactiveerd en de verzuimcode selecteren die wordt gebruikt voor het beheren van deze integratie. U kunt ook aangeven hoe een casus met letsel- of ziekte-incidenten moet worden bewaard, en het standaardidentificatienummer opgeven dat wordt weergegeven wanneer een nieuwe werknemer in dienst wordt genomen. 

De instellingen op het tabblad **Werving** definiëren de documenttypen die worden gebruikt voor correspondentie die automatisch naar sollicitanten worden verzonden en het wervingsproject dat worden gebruikt voor open sollicitaties (sollicitaties die niet specifiek voor een wervingsproject zijn). De periode die is gedefinieerd als ouderdomsperiode voor het wervingsproject bepaalt de wervingsprojecten die zijn opgenomen op de tegel **Verouderende projecten** in het werkgebied **Wervingsbeheer**. De periode die wordt ingesteld voor de sollicitatiedeadlinewaarschuwing wordt gebruikt om wervingsprojecten weer te geven die hun sollicitatiedeadline naderen op de tegel **Einde van sollicitatietermijn nadert** in het werkgebied **Werving**. 

De instellingen op het tabblad **Compensatie** definiëren of gebruikers moeten bevestigen dat ze informatie willen opslaan voor een vaste- of variabele-compensatieplan. Als u het selectievakje **Opslaan van validatie activeren** inschakelt, wordt een gebruiker wanneer hij of zij een compensatie-gerelateerde pagina afsluit, gevraagd of hij of zij de record wil opslaan. Op sommige pagina's in compensatiebeheer kunnen gebruikers geen gegevens verwijderen.. Door gebruikers te vragen of ze gegevens daadwerkelijk willen opslaan, worden er mogelijk minder gegevens opgeslagen die naderhand niet meer kunnen worden verwijderd. Als het selectievakje **Opslaan van validatie activeren** is uitgeschakeld, worden records altijd direct opgeslagen, misschien voordat de gebruiker klaar is. Als u prestatiebeheer gebruikt, kunt u met het tabblad **Compensatie** ook een beoordelingsmodel selecteren om te gebruiken in plaats van het model dat wordt toegewezen aan compensatieplannen wanneer prestaties worden beoordeeld. 

### <a name="previously-released-functionality"></a>Eerder uitgebrachte functionaliteit

De instellingen op het tabblad **Nummerreeks** bepalen de reeksen die worden gebruikt voor het automatisch toewijzen van id's aan items in Human resources, zoals sollicitaties, verzuimregistraties, resultaten van compensatieprocessen, casenummers, cursussen en cursusagenda's. Om nummerreeksverwijzingen en codes te onderhouden, gebruikt u de lijstpagina **Nummerreeksen**. Klik op **Organisatiebeheer** &gt; **Nummerreeksen** &gt; **Nummerreeksen**.

> [!NOTE]
> Het aantal uren dat is gewerkt, kan niet groter zijn dan 1250, en de lengte van het dienstverband kan niet langer dan 12 maanden zijn. Deze maximumwaarden zijn in overeenstemming met de federale wetgeving in de verenigde Staten. Tot slot bepalen de instellingen op het tabblad **Selfservice werknemer** welke informatie managers kunnen invoeren namens hun werknemers.
