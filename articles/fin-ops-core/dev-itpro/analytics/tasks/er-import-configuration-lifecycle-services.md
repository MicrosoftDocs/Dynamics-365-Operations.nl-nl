---
title: Een ER-configuratie vanuit Lifecycle Services importeren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0830707885e8ed52581aa789df0279d78e3a9c10
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184825"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a>Een ER-configuratie vanuit Lifecycle Services importeren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Lifecycle Services (LCS) kan importeren.

In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze naar het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een ER-configuratie uploaden naar Lifecycle Services" voltooien. Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Configuraties.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Een gedeelde versie van gegevensmodelconfiguratie verwijderen
1. Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.
    * De eerste versie van een voorbeeldgegevensmodelconfiguratie is gemaakt en gepubliceerd naar LCS tijdens de procedure "Een ER-configuratie naar Lifecycle Services uploaden". In deze procedure verwijdert u deze versie van de ER-configuratie. Deze versie van een voorbeeldgegevensmodelconfiguratie wordt later geïmporteerd vanuit LCS.  
2. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft. Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.  
3. Klik op Status wijzigen.
4. Klik op Beëindigen.
    * Wijzig de status van de geselecteerde versie van ‘Gedeeld’ in ‘Beëindigd’ om deze voor verwijdering beschikbaar te maken.  
5. Klik op OK.
6. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de versie van deze configuratie die de status ‘Beëindigd’ heeft.  
7. Klik op Verwijderen.
8. Klik op Ja.
    * De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is beschikbaar.  
9. Sluit de pagina.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Een gedeelde versie van gegevensmodelconfiguratie importeren vanuit LCS
1. Markeer in de lijst de geselecteerde rij.
    * Open de lijst met opslagplaatsen voor de configuratieprovider ‘Litware, Inc.’ Litware, Inc openen.  
2. Klik op Opslagplaatsen.
3. Klik op Openen.
    * Selecteer de LCS-opslagplaats en open deze.  
4. Markeer in de lijst de geselecteerde rij.
    * Selecteer de eerste versie van de 'Voorbeeldmodelconfiguratie' in de lijst met versies.  
5. Klik op Importeren.
6. Klik op Ja.
    * Bevestig de import van de geselecteerde versie van LCS.  
    * Het informatiebericht (boven het formulier) bevestigt de voltooiing van de import van de geselecteerde versie.  
7. Sluit de pagina.
8. Sluit de pagina.
9. Klik op Configuraties.
10. Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.
11. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de versie van deze configuratie die de status ‘Gedeeld’ heeft.  
    * De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.  

