---
title: Kwaliteitsorders instellen
description: Deze procedure laat zien hoe u een kwaliteitsbeheerproces kunt inschakelen waarbij inkomende voorraad onmiddellijk na aankomstregistratie moet worden geïnspecteerd.
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9760aeb823730581aa1f02db1574e6f5eccd1f75
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145635"
---
# <a name="set-up-quality-orders"></a>Kwaliteitsorders instellen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een kwaliteitsbeheerproces kunt inschakelen waarbij inkomende voorraad onmiddellijk na aankomstregistratie moet worden geïnspecteerd. De procedure wordt gewoonlijk uitgevoerd door een kwaliteitsmanager. Het proces bevat het maken van een kwaliteitsgroep, om de artikelen te definiëren die zullen worden bemonsterd, en een testgroep voor het groeperen van de tests die zullen worden uitgevoerd op artikelen in de kwaliteitsgroep. U kunt deze taakgeleiding uitvoeren in het demobedrijf USMF.


## <a name="enable-quality-management"></a>Kwaliteitsbeheer inschakelen
1. Ga naar **Navigatievenster > Modules > Voorraadbeheer > Instellen > Parameters voor voorraad- en magazijnbeheer**.
2. Klik op het tabblad **Kwaliteitsbeheer**.
3. Stel de optie **Kwaliteitsbeheer gebruiken** in op 'Ja'.
4. Klik op **Rapportinstellingen**. In USMF is de rapportinstelling voor kwaliteitsbeheer al gedefinieerd. Als dit nog niet is gebeurd, kunt u hier nieuwe regels toevoegen voor verschillende soorten rapporten en het type document selecteren dat voor elk rapport moet worden gebruikt.  
5. Sluit de pagina.
6. Sluit de pagina.

## <a name="create-a-test"></a>Een test maken
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Tests**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Test**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer 'Optie' in het veld **Type**. In dit voorbeeld selecteren wij Optie zodat het mogelijk is de testresultaten op basis van vooraf gedefinieerde waarden toe te wijzen.  
6. Klik op **Opslaan**.
7. Sluit de pagina.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Testvariabelen maken om de manier te definiëren waarop testresultaten worden vastgelegd
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Testvariabelen**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Variabele**.
4. Typ een waarde in het veld **Beschrijving**.
5. Klik op **Opslaan**.
6. Klik op **Resultaten**.
7. Klik op **Nieuw**.
8. Typ een waarde in het veld **Resultaat**.
9. Typ een waarde in het veld **Beschrijving**.
10. Selecteer 'Geslaagd' in het veld **Uitslagstatus**.
11. Klik op **Opslaan**.
12. Klik op **Nieuw**.
13. Typ een waarde in het veld **Resultaat**.
14. Typ een waarde in het veld **Beschrijving**.
15. Klik op **Opslaan**.
16. Sluit de pagina.
17. Sluit de pagina.

## <a name="set-up-item-sampling"></a>Artikelbemonstering instellen
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Artikelbemonstering**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Artikelbemonstering**.
4. Typ een waarde in het veld **Beschrijving**.
5. Typ een getal in het veld **Waarde**. Deze waarde heeft betrekking op de hoeveelheidsspecificatie die in het aangrenzende veld is geselecteerd.  
6. Vouw de sectie **Proces** uit of samen.
7. Schakel het selectievakje **Volledig blokkeren** in of uit. Als u deze optie selecteert, wordt de gehele partij of orderregelhoeveelheid geblokkeerd als een test is mislukt. Als u deze niet selecteert, worden alleen de artikelen in de kwaliteitsorder geblokkeerd.  
8. Klik op **Opslaan**.
9. Sluit de pagina.

## <a name="create-a-quality-group"></a>Een kwaliteitsgroep maken
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitsgroepen**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Kwaliteitsgroep**. Gebruik een beschrijvende naam om u te helpen bepalen welk type artikelen de groep zal bevatten (uw bemonsteringscriteria).  
4. Typ een waarde in het veld **Beschrijving**.
5. Klik op **Opslaan**.
6. Klik op **Artikelen toevoegen**.
7. Selecteer de rij **Artikelnummer**. In dit voorbeeld wordt het filteren uitgevoerd op basis van het artikelnummer.  
8. Typ een waarde in het veld **Criteria**. Typ bijvoorbeeld T* om te filteren op de artikelnummers met T beginnen.  
9. Klik op **OK**.
10. Klik op **OK**.
11. Klik op **Artikelkwaliteitsgroepen**.
12. Sluit de pagina.
13. Sluit de pagina.

## <a name="create-a-test-group"></a>Een testgroep maken
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Testgroepen**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Testgroep**. Geef de **Testgroep** een naam die u zal helpen onthouden welk type testen wordt uitgevoerd en welke kwaliteitsgroep hieraan moet worden gekoppeld. Als het bijvoorbeeld moet worden gebruikt met een kwaliteitsgroep die artikelen selecteert die met een T beginnen, kunt u het T-artikelen testen noemen.  
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer in het veld **Artikelbemonstering** de artikelbemonsteringsregel die u eerder hebt gemaakt.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik op **Toevoegen**.
8. Typ een getal in het veld **Volgnummer**.
9. Selecteer in het veld **Test** de test die u eerder hebt gemaakt.
10. Zoek en selecteer het gewenste record in de lijst.
11. Klik op het tabblad **Test**.
12. Selecteer in het veld **Variabele** de testvariabele die u eerder hebt gemaakt
13. Zoek en selecteer het gewenste record in de lijst.
14. Klik in het veld **Standaarduitslag** op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
16. Klik op **Opslaan**.
17. Sluit de pagina.

## <a name="define-when-quality-orders-will-be-created"></a>Definiëren wanneer kwaliteitsorders worden gemaakt
1. Ga naar **Voorraadbeheer > Instellingen > Kwaliteitsbeheer > Kwaliteitskoppelingen**.
2. Klik op **Nieuw**.
3. Selecteer een optie in het veld **Verwijzingstype**.
4. Selecteer 'Groep' in het veld **Artikelcode**. In dit voorbeeld selecteren we Groep en gebruiken we de kwaliteitsgroep die we eerder hebben gemaakt. U kunt dit ook instellen op "Tabel" om handmatig de artikelen op te geven of "Alle" selecteren om alle artikelen toe te voegen aan de kwaliteitsorder.  
5. Selecteer in het veld **Artikel** de artikelgroep die u eerder hebt gemaakt. Welke opties beschikbaar zijn in het veld Artikel is afhankelijk van wat u hebt ingesteld in het veld Artikelcode.  
6. Zoek en selecteer de gewenste record in de lijst.
7. Vouw de sectie Proces uit of samen.
8. Selecteer een optie in het veld **Gebeurtenistype**. Dit is de gebeurtenis waarmee de test wordt geactiveerd. Welke opties hier beschikbaar zijn is afhankelijk van het proces dat u hebt geselecteerd in het veld Verwijzingstype.  
9. Selecteer een optie in het veld **Uitvoering**.
10. Vouw de sectie **Kwaliteitsorderproces** uit of samen.
11. Klik in het veld **Gebeurtenisblokkering** op de vervolgkeuzeknop om de zoekopdracht te openen. In dit veld wordt de lijst weergegeven met processen die kunnen worden geblokkeerd als de kwaliteitsorder nog open staat. De opties zijn afhankelijk van wat u in het veld Gebeurtenistype hebt geselecteerd.  
12. Klik in de lijst op de koppeling in de geselecteerde rij. Dit is afhankelijk van de vorige geselecteerde waarden. Selecteer of de volgende processen moeten worden geblokkeerd terwijl er openstaande kwaliteitsorders aan een brondocumentregel zijn gekoppeld.  
13. Vouw de sectie **Specificaties** uit of samen.
14. Selecteer in het veld **Testgroep** de testgroep die u eerder hebt gemaakt.
15. Zoek en selecteer het gewenste record in de lijst.
16. Klik op **Opslaan**.
17. Sluit de pagina.

