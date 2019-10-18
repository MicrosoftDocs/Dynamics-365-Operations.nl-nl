---
title: Configuraties voor toewijzing van model voor elektronische rapportage (ER) maken
description: Gebruik deze procedure voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en pas de ingebouwde ER-functies toe voor efficiënte statistische berekeningen.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcfc258e7fe364779fd77cc79413e8d5e871e214
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182687"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Configuraties voor toewijzing van model voor elektronische rapportage (ER) maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruik deze procedure voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en pas de ingebouwde ER-functies toe voor efficiënte statistische berekeningen. In deze procedure maakt u een configuratie voor voorbeeldbedrijf Litware, Inc. 

Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar.

Deze stappen kunnen worden voltooid met elke dataset. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure 'Een configuratieprovider maken en deze als actief markeren'.  
2. Klik op Rapportconfiguraties.
3. Klik op Filters weergeven.
4. Typ de filterwaarde 'Intrastat' in het veld Naam en gebruik de filteroperator 'begint met'.
    * Pas dit filter toe om de configuratie van het 'Intrastat'-gegevensmodel te vinden. Dit model bestaat mogelijk al in de configuratiestructuur. Als dit het geval is, gaat u naar de volgende subtaak.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Intrastat-modelconfiguratie ophalen die door Microsoft wordt geleverd
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
4. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de Microsoft-providertegel.  
5. Klik op Opslagplaatsen.
    * Klik op de Microsoft-providertegel op Opslagplaatsen.  
6. Klik op Filters weergeven.
7. Typ de filterwaarde 'resources' in het veld Naam en gebruik de filteroperator 'bevat'. 
8. Klik op Openen.
9. Selecteer in de structuur 'Intrastatmodel'.
10. Klik op Importeren.
11. Klik op Ja.
    * U hebt de ER-modelconfiguratie geïmporteerd die het gegevensmodel bevat die u wilt gebruiken om te onderzoeken hoe de nieuwe ER-functionaliteit kan worden gebruikt.  
12. Sluit de pagina.
13. Sluit de pagina.
14. Klik op Rapportconfiguraties.

## <a name="add-a-new-model-mapping-configuration"></a>Een nieuwe modeltoewijzingsconfiguratie toevoegen
1. Selecteer in de structuur 'Intrastatmodel'.
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Typ in het veld Nieuw 'Modeltoewijzing gebaseerd op het Intrastatmodel'.
4. Typ 'Voorbeeldtoewijzing Intrastat' in het veld Naam.
    * Voorbeeldtoewijzing van Intrastat  
5. Klik op Configuratie maken.

