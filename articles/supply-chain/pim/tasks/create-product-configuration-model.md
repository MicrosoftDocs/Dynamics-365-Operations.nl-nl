---
title: Een productconfiguratiemodel maken
description: Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca99c0346a3f982164076167c3429587aac18be6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568419"
---
# <a name="create-a-product-configuration-model"></a>Een productconfiguratiemodel maken

[!include [banner](../../includes/banner.md)]

Deze procedure toont aan hoe u een productconfiguratiemodel maakt en basisinformatie, zoals kenmerken en subcomponenten, invoert. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-product-model"></a>Een productmodel maken

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Selecteer **Nieuw**.
1. Typ een waarde in het veld **Naam**.
1. Typ een waarde in het veld **Beschrijving**.
1. Selecteer een optie in het veld **Oplossingsstrategie**.
    * De oplossingsstrategie bepaalt hoe de beperkingen in een op beperkingen gebaseerd productconfiguratiemodel worden verwerkt. Deze selectie kan een invloed hebben op de prestaties van het productconfiguratiemodel.  
1. Typ een waarde in het veld **Naam**.
    * Het hoofdcomponent vertegenwoordigt het productconfiguratiemodel, maar kan ook in andere productmodellen worden gebruikt.  
1. Selecteer **OK**.
1. Selecteer een optie in het veld **Configuraties opnieuw gebruiken**.
    * Als de parameter Configuraties opnieuw gebruiken op Ja is ingesteld, controleert het systeem identieke configuraties na elke sessie en elk hergebruik van de configuratie als een exacte overeenkomst wordt gevonden.  

## <a name="add-attributes"></a>Kenmerken toevoegen

1. Vouw de sectie **Kenmerken** uit.
2. Selecteer **Toevoegen**.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld **Naam**.
5. Typ een waarde in het veld **Oplossingsnaam**.
    * De oplossingsnaam wordt gebruikt door oplosser van beperkingen van de productconfiguratie. Deze mag geen spaties of speciale tekens bevatten, behalve _ (onderstrepingsteken).  
6. Typ een waarde in het veld **Beschrijving**.
    * De omschrijvingstekst wordt aan de gebruiker van de configuratie weergegeven en kan daarom fungeren als hulp bij het selecteren van de juiste kenmerkwaarde.  
7. Typ of selecteer een waarde in het veld **Kenmerktype**.
    * Het kenmerktype bepaalt welke waarden beschikbaar zijn voor het kenmerk.  
8. Schakel het selectievakje **Opnemen in hergebruik** in.
    * Deze optie is alleen beschikbaar als de optie Configuraties opnieuw gebruiken is geselecteerd. Als het selectievakje van het kenmerk wordt ingeschakeld, wordt met dit kenmerk rekening gehouden wanneer het systeem naar een exacte overeenkomst zoekt.  

## <a name="add-subcomponents"></a>Subonderdelen toevoegen

1. Vouw de sectie **Subonderdelen** uit.
2. Selecteer **Toevoegen**.
3. Markeer in de lijst de geselecteerde rij.
4. Typ een waarde in het veld **Naam**.
5. Typ een waarde in het veld **Oplossingsnaam**.
6. Typ een waarde in het veld **Beschrijving**.
7. Typ of selecteer een waarde in het veld **Onderdeel**.
    * Elke subonderdeel moet naar een componentdefinitie verwijzen. Dit ontwerp ondersteunt herbruikbare onderdelen en zorgt ervoor dat een onderdeel, als het is gedefinieerd, in veel productmodellen kan worden gebruikt.  
8. Selecteer **Opslaan**.
9. Selecteer **Details van stuklijstregel**.
    * Met het formulier Regeldetails van stuklijst kan de gebruiker de vereiste eigenschappen voor het subonderdeel selecteren. Elke eigenschap kan een vaste waarde krijgen of aan een kenmerk worden toegewezen. De toewijzing aan een kenmerk zorgt ervoor dat de regeleigenschap van de stuklijst verschillende waarden krijgt, afhankelijk van de geselecteerde configuratie.  
10. Typ of selecteer een waarde in het veld **Artikelnummer**.
    * Elke subonderdeel vertegenwoordigt een configureerbaar productmodel met op beperkingen gebaseerde configuratietechnologie. De verwijzing wordt gemaakt door het artikelnummer.  
11. Schakel het selectievakje **Instellen** in.
12. Selecteer **Ja** in het veld **Berekening**.
    * Het instellen van de berekeningsoptie zorgt ervoor dat het product wordt opgenomen bij de uitvoering van een kostenberekening voor het product.  
13. Selecteer het tabblad **Instellingen**.
14. Schakel het selectievakje **Instellen** in.
15. Voer een getal in het veld **Hoeveelheid** in.
    * Het hoeveelheidsveld bepaalt hoeveel van dit product wordt verbruikt in het geconfigureerde product.  
16. Schakel het selectievakje **Instellen** in.
17. Voer in het veld **Per reeks** een getal in.
18. Selecteer **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]