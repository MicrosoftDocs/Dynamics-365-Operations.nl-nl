---
title: EUR-00002 Een EU Intrastat-aangifte genereren
description: Deze procedure begeleidt u bij de stappen die nodig zijn om de Intrastat-aangifte in de elektronische bestandsindeling te exporteren en een voorbeeld te bekijken van de aangiftegegevens in een Excel-indeling.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
ms.openlocfilehash: b14134763da262fabe533b2864a5472abaeb01c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283819"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 Een EU Intrastat-aangifte genereren

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u bij de stappen die nodig zijn om de Intrastat-aangifte in de elektronische bestandsindeling te exporteren en een voorbeeld te bekijken van de aangiftegegevens in een Excel-indeling. 

Voordat u deze procedure kunt uitvoeren, moet u transacties overboeken naar Intrastat. 

Deze procedure is gemaakt met het demobedrijf DEMF.


## <a name="import-configurations-with-settings"></a>Configuraties met instellingen importeren
1. Ga naar Werkruimten > Elektronische rapportage
2. Klik op Instellingen als actief.
3. Klik op Opslagplaatsen.
4. Klik op Openen.
5. Open de kolomfilter Configuratienaam.
6. Pas een filter toe op het veld "Configuratienaam" met de waarde "Intrastat (DE)" met behulp van de filteroperator ´begint met´.
    * U moet de configuratienaam selecteren die van toepassing is voor het land van uw rechtspersoon. In deze procedure wordt de Duitse rechtspersoon (DEMF) als voorbeeld gebruikt. Daarom moet "Intrastat (DE") worden gekozen.  
    * Klik op Importeren en klik vervolgens op Ja.  
7. Open de kolomfilter Configuratienaam.
8. Pas een filter toe op het veld "Configuratienaam" met de waarde "Intrastat-rapport" met behulp van de filteroperator ´begint met´.
    * Klik op Importeren en klik vervolgens op Ja.  

## <a name="set-up-foreign-trade-parameters"></a>Parameters voor buitenlandse handel instellen
1. Ga naar Belasting > Instellingen > Buitenlandse handel > Parameters buitenlandse handel
2. Vouw de sectie Elektronische rapportage uit.
3. Typ of selecteer een waarde voor Intrastat (DE) in het veld Bestandsindelingstoewijzing.
4. Typ of selecteer een waarde voor Intrastat-rapport in het veld Rapportindelingstoewijzing.
5. Vouw de sectie Afrondingsregels uit.
    * U moet de afrondingsregels instellen die van toepassing zijn in uw land/regio voor Intrastat-rapportage.  
6. Voer een nummer in het veld Afrondingsregel in.
    * Voer de afrondingsprecisie in. Voer bijvoorbeeld '0,01' in.  
7. Voer een getal in het veld Aantal decimalen voor bedrag in.
    * Voer bijvoorbeeld 2 in:  
8. Selecteer een optie in het veld Afronding onder 1 kg.
    * Selecteer bijvoorbeeld Afronden naar 1 kg.  
9. Voer een nummer in het veld Afrondingsregel in.
    * Voer bijvoorbeeld '1' in voor afrondinggewicht op het gehele getal.  
10. Vouw de sectie Ondergrens uit.
11. Voer een getal in het veld Gewicht in.
    * Voer bijvoorbeeld '10' als het minimumgewicht in.  
12. Typ een getal in het veld Bedrag.
    * Voer bijvoorbeeld '200' als het minimumbedrag in.  
13. Typ of selecteer een waarde in het veld Basisproduct.

## <a name="set-up-compression-of-intrastat"></a>Compressie van Intrastat instellen
1. Ga naar Belasting > Instellingen > Buitenlandse handel > Compressie van Intrastat.
2. Klik op Verwijderen.
3. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer bijvoorbeeld Basisproduct in de sectie Beschikbaar.  
4. Klik op Toevoegen.

## <a name="generate-intrastat-declaration"></a>Intrastat-aangifte genereren
1. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat
2. Klik op Valideren.
    * De validatie wordt uitgevoerd op basis van het veld Instelling controleren op de pagina Parameters buitenlandse handel.  
3. Klik op OK.
4. Klik op Bijwerken.
5. Klik op Ondergrens.
6. Voer een datum in het veld Startdatum in.
    * Voer bijvoorbeeld 1 januari 2015 in.  
7. Selecteer Ja in het veld Comprimeren.
8. Voer een datum in het veld Einddatum in.
    * Voer bijvoorbeeld 31 januari 2015 in.  
9. Klik op OK.
10. Klik op Bijwerken.
11. Klik op Comprimeren.
    * Deze compressie vindt plaats volgens uw instellingen bij de Compressie van Intrastat.  
12. Voer een datum in het veld Startdatum in.
    * Voer bijvoorbeeld 1 januari 2015 in.  
13. Voer een datum in het veld Einddatum in.
    * Voer bijvoorbeeld 31 januari 2015 in.  
14. Klik op OK.
15. Klik op Bijwerken.
16. Klik op Volgnummers opnieuw genereren.
17. Klik op OK.
18. Klik op Uitvoer.
19. Klik op Rapport.
20. Voer in het veld Vanaf de eerste datum van de aangifteperiode in.
    * Stel de datum bijvoorbeeld op 1 januari 2015 in.  
21. Voer een datum in het veld Einddatum in.
    * Voer bijvoorbeeld 31 januari 2015 in.  
22. Selecteer Ja in het veld Bestand maken.
23. Typ een waarde in het veld Bestandsnaam.
24. Selecteer Ja in het veld Rapport maken.
25. Typ een waarde in het veld Bestandsnaam van rapport.
26. Selecteer een optie in het veld Richting.
    * Selecteer bijvoorbeeld 'Verzendingen'.  
27. Klik op OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
