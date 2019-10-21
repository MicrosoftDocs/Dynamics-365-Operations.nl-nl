---
title: 'ER: een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling (november 2016)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van Systeembeheerder of Ontwikkelaar voor Elektronische rapportage een nieuwe configuratie voor Elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1229c89f43f9ded955dadf2f4d87825c9ab4e71
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182572"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a>ER: een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling (november 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van Systeembeheerder of Ontwikkelaar voor Elektronische rapportage een nieuwe configuratie voor Elektronische rapportage (ER) kan maken die een sjabloon bevat voor het genereren van elektronische documenten in OPENXML-indeling. Deze configuratie wordt voor de verwerking van leveranciersbetalingen gebruikt.

In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Maken. Deze stappen kunnen in GBSI-bedrijven worden uitgevoerd.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien. U moet ook een Excel-bestand hebben dat wordt geïmporteerd bij het maken van de sjabloon. Dit bestand kan worden geopend vanuit [Sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266).


## <a name="upload-the-payments-data-model-configuration"></a>De gegevensmodelconfiguratie Betalingen uploaden
1. Ga in het navigatiedeelvenster naar **Modules > Organisatiebeheer > Werkruimten > Elektronische rapportage**.
2. Selecteer in de lijst de configuratieprovider voor het voorbeeldbedrijf Litware,Inc. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure [Een configuratieprovider maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md) voltooien.
3. Selecteer **Instellingen als actief**.
4. Selecteer **Opslagplaatsen**. Selecteer een opslagplaats voor het type Bronnen voor bedrijfsactiviteiten, indien beschikbaar. Als deze beschikbaar is, slaat u de volgende stappen in verband met het maken van een nieuwe opslagplaats over.  
5. Selecteer **Toevoegen** om het uitklapvenster te openen.
6. Voer in het veld **Type opslagplaats van configuratie** `Operations resourcesdd` in.
7. Selecteer **Opslagplaats maken**.
8. Selecteer **OK**.
9. Selecteer **Openen**.
10. Selecteer **Betalingsmodel** in de structuur.
11. Selecteer **Importeren**. Importeer dit gegevensmodel. Het wordt als een gegevensbron in een nieuwe indelingsconfiguratie gebruikt. Sla deze stap over als deze configuratie al is geïmporteerd.  
12. Selecteer **Ja**.
13. Sluit de pagina's totdat u terugkeert naar de pagina voor Elektronische rapporten.

## <a name="create-a-new-format-configuration"></a>Een nieuwe indelingsconfiguratie maken
1. Selecteer **Rapportageconfiguraties**.
2. Selecteer **Betalingsmodel** in de structuur.
3. Klik op **Configuratie maken** om het dialoogvenster te openen.
4. Voer in het veld **Nieuw** `Format based on data model PaymentModel` in. Maak een indeling die op het gegevensmodel PaymentModel is gebaseerd.
5. Typ in het veld **Naam** `Sample worksheet report`. Voorbeeldwerkbladrapport  
6. Typ in het veld **Omschrijving** `Sample worksheet report for vendors’ payments`. Voorbeeldwerkbladrapport voor betalingen van leveranciers.  
7. Typ of selecteer een waarde in het veld **Definitie gegevensmodel**. Selecteer de definitie **CustomerCreditTransferInitiation**.  
8. Selecteer **Configuratie maken**.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Een nieuw document in OPENXML-werkbladindeling ontwerpen
1. Selecteer **Betalingsmodel\Voorbeeldwerkbladrapport** in de structuur.
2. Selecteer **Ontwerper**.
3. Selecteer **Importeren** in het Actievenster.
4. Selecteer **Importeren uit Excel**.
5. Selecteer **Bijlagen**. Voeg het bestaande Excel-document als een sjabloon toe.  
6. Selecteer **Nieuw**.
7. Selecteer **Bestand**. Wijs naar het bestaande Excel-bestand.  
8. Sluit de pagina.
9. Typ of selecteer een waarde in het veld **Sjabloon**. Selecteer het gekoppelde Excel-bestand dat als sjabloon moet worden gebruikt.  
10. Selecteer **OK**. ER-indelingscomponenten zijn gemaakt in de ontwerpende indeling op basis van de structuur van het verwijzende MS Excel-document (benoemde bereiken).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Een nieuwe gegevensbron maken om totalen per valutacode te berekenen
1. Selecteer het tabblad **Toewijzen**.
2. Klik op **Basis toevoegen** om het dialoogvenster te openen.
3. Selecteer in de structuur **Functies\Groeperen op**.
4. Typ in het veld **Naam** `PaymentByCurrency`.
5. Selecteer **Groep bewerken op**.
6. Vouw in de structuur het **Model**uit en selecteer vervolgens **model\Payments**.
7. Selecteer **Veld toevoegen aan**.
8. Selecteer **Wat groeperen**.
9. Vouw in de structuur **model\Betalingen**uit en selecteer vervolgens **model\Betalingen\Valuta**.
10. Selecteer **Veld toevoegen aan**.
11. Selecteer **Gegroepeerde velden**.
12. Selecteer in de structuur **model\Betalingen\Opgedragen Bedrag(OpgedragenBedrag)**.
13. Selecteer **Veld toevoegen aan**en selecteer vervolgens **Samenvoegingsvelden**.
14. Selecteer een optie in het veld **Methode**. Selecteer de **SUM-aggregatie**-functie.  
15. Typ in het veld **Naam** `TotalInstructuredAmount`.
16. Selecteer **Opslaan**.
17. Sluit de pagina.
18. Selecteer **OK**.

## <a name="map-format-components-to-data-sources"></a>Indelingscomponenten aan gegevensbronnen toewijzen
1. Selecteer in de structuur **model\Betalingen\Initiërende Partij(InitiërendePartij)\Naam** en **Excel\RapportKop\Bedrijfsnaam**.
2. Selecteer **Binden**.
3. Selecteer **model\Betalingen\Crediteur\Identificatie\Bron ID(BronID)** en **Excel\PaymLines\VerkAccountNaam** in de structuur.
4. Selecteer **Binden**.
5. Selecteer **Model\Betalingen\Crediteur\Naam** en **Excel\PaymLines\VerkNaam**in de structuur.
6. Selecteer **Binden**.
7. Selecteer **Model\Betalingen\Crediteur Agent(CrediteurAgent)\Naam** en **Excel\PaymLines\Bank**in de structuur.
8. Selecteer **Binden**.
9. Selecteer **Model\Betalingen\Crediteur Agent(CrediteurAgent)\Routeringnummer(Routeringnummer)** en **Excel\PaymLines\Routeringnummer**in de structuur.
10. Selecteer **Binden**.
11. Selecteer **model\Betalingen\Crediteursaccount(Crediteursaccount)\Identificatie\Nummer** en **Excel\PaymLines\Accountnummer** in de structuur.
12. Selecteer **Binden**.
13. Selecteer **model\Betalingen\Opgedragen Bedrag(OpgedragenBedrag)** en **Excel\PaymLines\Debet** in de structuur.
14. Selecteer **Binden**.
15. Selecteer **Model\Betalingen\Valuta** en **Excel\PaymLines\Valuta**in de structuur.
16. Selecteer **Binden**.
17. Selecteer **BetalingPerValuta\gegroepeerd\Valuta** en **Excel\OverzichtRegels\OverzichtValuta**in de structuur.
18. Selecteer **Binden**.
19. Selecteer **BetalingPerValuta\gegroepeerd\TotaalOpgedragenBedrag** en **Excel\OverzichtRegels\OverzichtBedrag**in de structuur.
20. Selecteer **Binden**.
21. Selecteer **BetalingPerValuta** en **Excel\Overzichtregels** in de structuur.
22. Selecteer **Binden**.
23. Selecteer **Model\Betalingen** en **Excel\PaymLines**in de structuur.
24. Selecteer **Binden**.
25. Selecteer **Opslaan** en sluit daarna de pagina.

## <a name="use-the-created-configuration-for-payments-processing"></a>De gemaakte configuratie gebruiken voor betalingsverwerking
1. Selecteer **Status wijzigen**.
2. Selecteer **Voltooien**.
3. Selecteer **OK**.
4. Ga in het navigatievenster naar **Modules > Te betalen rekeningen > Betalingsinstelling > Betaalmethodes**.
5. Gebruik het snelfilter om in het veld **Betalingsmethode** te filteren met de waarde **Elektronisch**.
6. Selecteer **Bewerken**.
7. Vouw de sectie **Bestandsindelingen** uit.
8. Selecteer **Ja** in het veld **Algemene elektronische rapportage**.
9. Typ of selecteer een waarde in het veld **Indelingsconfiguratie exporteren**. Selecteer de configuratie **Voorbeeldwerkblad rapport**.  
10. Selecteer **Opslaan**.
11. Sluit de pagina.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>De gemaakte configuratie gebruiken voor het testen van de verwerking van betalingsjournalen
1. Ga in het navigatiedeelvenster naar **Modules > Te betalen accounts > Betalingen > Betalingsjournaal**.
2. Selecteer **Nieuw** om een nieuw betalingsjournaal te maken.
3. Typ in het veld **Naam** de tekst **VendPay**.
4. Selecteer **Regels**
5. Specificeer in het veld **Account** de waardes `GB_SI_000001`.
6. Stel **Debet** in op `1000`.
7. Selecteer **Nieuw**.
8. Specificeer in het veld **Account** de waardes `GB_SI_000005`.
9. Stel **Debet** in op `2000`.
10. Typ `EUR` in het veld **Valuta**.
11. Geef in het veld **Tegenrekening** de waarden op `GBSI OPER`.
12. Typ in het veld **Betalingsmethode** `Electronic`.
13. Selecteer **Opslaan**.
14. Selecteer **Betalingen genereren**.
15. Typ in het veld **Betalingsmethode** `Electronic`.
16. Typ `Payments` in het veld **Bestandsnaam**.
17. Typ in het veld **Bankrekening** `GBSI OPER`.
18. Selecteer **OK** en vervolgens weer **OK**. Controleer het gemaakte werkblad, inclusief details van betalingsregels en totalen voor elke valutacode die in dit betalingsbericht wordt gebruikt.  

