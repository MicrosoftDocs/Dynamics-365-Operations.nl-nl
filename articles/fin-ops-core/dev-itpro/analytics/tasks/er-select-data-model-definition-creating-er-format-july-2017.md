---
title: Definities voor gegevensmodel selecteren tijdens het maken van indelingen
description: Als u de stappen in deze procedure wilt uitvoeren, moet u eerst de stappen in de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65b3a74f98282f01940c5d17f8aa893d174883da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290119"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Definities voor gegevensmodel selecteren tijdens het maken van indelingen

[!include [banner](../../includes/banner.md)]

Als u de stappen in deze procedure wilt uitvoeren, moet u eerst de stappen in de procedure 'ER Een configuratieprovider maken en deze als actief markeren' voltooien. 

Deze procedure laat zien hoe een basisitem van een model kan worden geselecteerd als een gegevensmodeldefinitie voor het invoegen van een ER-indelingsconfiguratie (Electronic Reporting) die is ontworpen om elektronische documenten te genereren. In deze procedure voegt u een nieuwe ER-indelingsconfiguratie voor het voorbeeldbedrijf Litware, Inc toe. 

Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar. De stappen kunnen worden voltooid met elke dataset.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als Actief. Als u deze configuratieprovider niet ziet, voert u eerst de stappen uit in de procedure Een configuratieprovider maken en deze als actief markeren.  
2. Klik op Rapportconfiguraties.

## <a name="add-a-new-er-data-model-configuration"></a>Een nieuwe ER-gegevensmodelconfiguratie toevoegen
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
    * We voegen een nieuwe ER-modelconfiguratie toe met een gegevensmodel dat is ontworpen om te worden gebruikt als gegevensbron voor het genereren van ER-rapporten.  
2. Typ in het veld Naam 'Betalingsmodel (fictief)'.
    * Betalingsmodel (fictief)  
3. Klik op Configuratie maken.
4. Klik op Ontwerper.
    * Open de ER-ontwerper om de structuur op te geven van een gegevensmodel van deze configuratie.  
    * Stel dat we het gegevensmodel ontwerpen voor betalingenbedrijfsdomein om 2 betalingsmethoden te ondersteunen, kredietoverboeking en automatische afschrijving.  
5. Klik op Nieuw om het verwijderdialoogvenster te openen.
6. Typ 'Betalingen - kredietoverboeking' in het veld Naam.
    * Betaling - kredietoverboeking  
7. Klik op Toevoegen.
8. Klik op Nieuw om het verwijderdialoogvenster te openen.
9. Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".
10. Typ 'Betalingen - directe afschrijving' in het veld Naam.
    * Betalingen - automatische afschrijving  
11. Klik op Toevoegen.
12. Klik op Opslaan.
13. Sluit de pagina.
14. Klik op Status wijzigen.
    * De conceptversie van het model voltooien om het beschikbaar te maken in nieuwe modeltoewijzingen en -indelingen.  
15. Klik op Voltooien.
16. Klik op OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Beginnen met het invoeren van een nieuwe ER-indelingsconfiguratie
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.
3. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
    * Alle basisitems van het geselecteerde gegevensmodel zijn momenteel beschikbaar voor selectie als een gegevensmodeldefinitie. U kunt doorgaan met uw indeling te ontwerpen met behulp van een van de vereiste basisitems van het gegevensmodel. Een ontbrekende modeltoewijzing voor het geselecteerde basisitem voorkomt niet dat u doorgaat.  
4. Sluit de pagina.

## <a name="add-a-new-er-model-mapping-configuration"></a>Een nieuwe ER-modelgegevensmodelconfiguratie toevoegen
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.
3. Typ in het veld Naam 'Betalingsmodeltoewijzingen (fictief)'.
    * Betalingsmodeltoewijzingen (fictief)  
4. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
5. Klik op Configuratie maken.

## <a name="design-er-model-mappings"></a>ER-modeltoewijzingen ontwerpen
1. Klik op Ontwerper.
    * Gebruik de ER-ontwerper om de modeltoewijzingen op te geven voor de vereiste basisitems.  
2. Klik op Ontwerper.
    * Instelling van geselecteerde modeltoewijzing simuleren voor het geselecteerde basisitem van het model.  
3. Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.
4. Klik op Basis toevoegen.
5. Typ 'Grootboek' in het veld Naam.
6. Typ "LedgerJournalTrans" in het veld Tabel.
    * LedgerJournalTrans  
7. Klik op OK.
8. Klik op Opslaan.
9. Sluit de pagina.
10. Sluit de pagina.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Beginnen met het invoeren van een andere ER-indelingsconfiguratie
1. Selecteer 'Betalingsmodel (fictief)' in de structuur.
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Betalingsmodel (fictief)' in.
4. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
    * Houd er rekening mee dat nu slechts één basisitem beschikbaar is voor toewijzing aan de gegevensbronnen van de toepassing. Wanneer ten minste één modeltoewijzing wordt geïntroduceerd, kunnen alleen de basisitems van het model die aan toepassingsgegevensbronnen zijn toegewezen, als modeldefinitie worden geselecteerd terwijl de ER-indeling wordt toegevoegd.   
5. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
