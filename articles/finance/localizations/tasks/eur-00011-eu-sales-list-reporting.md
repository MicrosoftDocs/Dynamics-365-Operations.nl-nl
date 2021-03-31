---
title: EUR-00011 Rapport van ICL-lijst instellen
description: Deze taak begeleidt u door een overzicht van de vereisten voor rapportage van de EU-verkooplijst.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ce458697fd61aabddcbf844dd0b2afbe3aa1c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228006"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a>EUR-00011 Rapport van ICL-lijst instellen

[!include [banner](../../includes/banner.md)]

Deze taak begeleidt u door een overzicht van de vereisten voor rapportage van de EU-verkooplijst. Raadpleeg voor meer informatie over EU-verkooplijstrapportage, met inbegrip van vereisten, de Help.

Deze taak is van toepassing op alle Europese landen/regio's. De handleiding werd gemaakt met de demogegevens van het bedrijf DEMF en dus Duitsland als voorbeeld voor land/regio. De handleiding maakt ook gebruik van Portugal als voorbeeld van EU-land/-regio.

Deze taken zijn bedoeld voor systeembeheerders.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Configuraties van elektronische rapportage importeren voor rapportage van EU-verkooplijst
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Instellingen als actief.
3. Klik op Opslagplaatsen.
4. Klik op Openen.
5. Klik in het actievenster op Opties.
6. Klik op Geavanceerd filteren/sorteren.
7. Klik op Toevoegen.
8. Selecteer 'Configuratienaam' in het veld Veld.
9. Typ in het veld Criteria 'EU-verkooplijst (DE)'.
10. Klik op OK.
11. Klik op Importeren.
12. Klik op Ja.
13. Klik in het actievenster op Opties.
14. Klik op Geavanceerd filteren/sorteren.
15. Klik op Opnieuw instellen.
16. Klik op Toevoegen.
17. Selecteer 'Configuratienaam' in het veld Veld.
18. Typ in het veld Criteria 'Rapport van EU-verkooplijst per rij'.
19. Klik op OK.
20. Klik op Importeren.
21. Klik op Ja.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Btw-codes voor rapportage van EU-verkooplijst instellen
1. Ga naar Btw > Indirecte belastingen > Btw > Btw-codes.
2. Gebruik het snelfilter om op het veld Btw-code te filteren met de waarde 'VAT19'.
3. Vouw de sectie Rapport instellen uit.
    * Controleer of de selectie Uitgesloten op Nee is ingesteld.  
    * U moet mogelijk de taakbegeleiding ontgrendelen om deze instelling te wijzigen.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Btw-groepen voor rapportage van EU-verkooplijst instellen
1. Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen.
2. Gebruik het snelfilter om op het veld Btw-groep te filteren met de waarde 'AR-DOM'.
3. Klik op Bewerken.
4. Vouw de sectie Instellingen uit.
5. Selecteer de eerste rij in de lijst.
6. Selecteer het selectievakje Vrijstelling.
7. Selecteer de tweede rij in de lijst.
8. Selecteer het selectievakje Vrijstelling.
9. Selecteer de derde rij in de lijst.
10. Selecteer het selectievakje Vrijstelling.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Btw-groepen voor artikel voor rapportage van EU-verkooplijst instellen
1. Ga naar Btw > Indirecte belastingen > Btw > Btw-groepen voor artikel.
2. Gebruik het snelfilter om op het veld -groep voor artikel te filteren met de waarde 'FULL'.
    * Controleer of de selectie Rapporteringstype op 'Artikel' is ingesteld.  
    * U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.  
3. Gebruik het snelfilter om op het veld -groep voor artikel te filteren met de waarde 'RED'.
    * Controleer of de selectie Rapporteringstype op 'Service' is ingesteld.  
    * U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Parameters van land/regio voor rapportage van EU-verkooplijst instellen
1. Ga naar Btw > Instellen > Btw > Parameters land/regio.
2. Klik op Nieuw.
3. Typ 'PRT' in het veld Land/regio.
4. Typ 'PT' in het Btw-veld.

## <a name="create-tax-exempt-numbers"></a>Btw-vrijstellingsnummers maken
1. Ga naar Btw > Instellen > Btw > Nummers van belastingvrijstelling.
2. Klik op Nieuw.
3. Typ 'PRT' in het veld Land/regio.
4. Typ 'PT12345' in het veld Nummers van belastingvrijstelling.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>Parameters van rapportage van EU-verkooplijst instellen
1. Ga naar Belasting > Instellen > Buitenlandse handel > Parameters buitenlandse handel.
2. Klik op het tabblad EU-verkooplijst.
3. Selecteer Ja in het veld Inkopen overboeken.
4. Vouw de sectie Afrondingsregels uit.
5. Stel Afrondingsregel in op '0.1'.
6. Selecteer Ja in het veld Minimumwaarde gebruiken.
7. Typ '2' in het veld Aantal decimalen.
8. Vouw de sectie Elektronische rapportage uit.
9. Selecteer 'EU-verkooplijst (DE)' in het veld Toewijzing van bestandsindeling.
10. Selecteer 'Rapport van EU-verkooplijst per rij' in het veld Toewijzing van rapportindeling.
11. Klik op het tabblad Land-/regio-eigenschappen.
    * Controleer of het veld Land-/regiotype op 'Binnenlands' is ingesteld voor Land/regio DEU.  
    * U moet mogelijk de taakbegeleiding ontgrendelen om de waarde in dit veld te wijzigen.  
12. Klik op Nieuw.
13. Typ 'PRT' in het veld Land/regio.
14. Typ 'PT' in het veld Intrastatcode.
15. Selecteer 'EU' in het veld Land-/regiotype.
16. Klik op het tabblad Nummerreeksen.
    * Controleer of er een Nummerreekscode is opgegeven voor de referentie 'EU-verkooplijst'.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Een klant maken voor demodoeleinden van rapportage van EU-verkooplijst
1. Ga naar Klanten > Klanten > Alle klanten.
2. Klik op Nieuw.
3. Typ 'PRT-001' in het veld Klantrekening.
4. Typ 'Een klant uit Portugal' in het veld Naam.
5. Selecteer '10' in het veld Klantgroep.
6. Selecteer 'AR-DOM' in het veld Btw-groep.
7. Selecteer 'PT12345' in het veld Nummers van belastingvrijstelling.
8. Typ 'PRT' in het veld Land/regio.
9. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]