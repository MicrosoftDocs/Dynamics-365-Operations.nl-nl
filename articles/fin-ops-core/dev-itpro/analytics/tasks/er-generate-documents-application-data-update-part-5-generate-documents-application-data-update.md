---
title: Documenten genereren die toepassingsgegevens bevatten
description: 'Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Documenten genereren met update van toepassingsgegevens (deel 4: Indeling wijzigen)" voltooien.'
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2591f5b32417dd7517f76fc237d2337af64b3f61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745030"
---
# <a name="generate-documents-that-have-application-data"></a>Documenten genereren die toepassingsgegevens bevatten

[!include [banner](../../includes/banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure "ER Documenten genereren met update van toepassingsgegevens (deel 4: Indeling wijzigen)" voltooien.



De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken. In deze procedure voert u de ER-indelingsconfiguratie uit om het Intrastat-rapport genereren en toepassingsgegevens bij te werken voor het archiveren van details van het rapportageproces.



Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de DEMF-gegevensset. Zorg voordat u begint dat de context van het land/de regio voor het DEMF-bedrijf BEL (België) is.


## <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen
1. Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.
2. Klik op het tabblad Nummerreeksen.

    Bij het archiveren van details van het Intrastat-rapportageproces moeten we records identificeren van elk archief dat we hebben gemaakt. Daarvoor moet een speciale nummerreeks worden geconfigureerd.  

3. Selecteer de verwijzing 'Intrastat-archief-id'.
4. Typ een waarde in het veld Nummerreekscode.

    Typ of selecteer de waarde 'Fore_2' in het veld 'Nummerreekscode'.  

5. ResolveChanges de nummerreekscode.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="run-modified-er-format"></a>Gewijzigde ER-indeling uitvoeren
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Intrastat (model)' uit.
3. Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.
4. Klik op Uitvoeren.
5. Typ in het veld Invoeren 'intrastat2.xml'.
6. Klik op OK.

## <a name="review-er-format-executions-results"></a>Resultaten van uitvoering van ER-indeling
Bekijk het gegenereerde XML-bestand.  
1. Sluit de pagina.
2. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.

    Open dit formulier met Intrastat-transacties die zijn opgenomen in het gegenereerde elektronische document.  

3. Klik op Intrastat-archief.

    Omdat de uitgevoerde ER-indeling nu instellingen bevat voor het bijwerken van toepassingsgegevens, zijn de details van de voltooide Intrastat-rapportage gearchiveerd. In dit formulier ziet u de koptekstrecord van het gemaakte archief.  

4. Klik op Details.

    In dit formulier ziet u de details van het gemaakte archief.  

5. Sluit de pagina.
6. Sluit de pagina.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]