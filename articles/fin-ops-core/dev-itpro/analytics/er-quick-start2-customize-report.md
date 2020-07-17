---
title: Een ER-indeling aanpassen om een aangepast elektronisch document te genereren
description: In dit onderwerp wordt uitgelegd hoe u een door Microsoft geleverde ER-indeling (Electronic Reporting) kunt aanpassen, zodat een aangepast elektronisch document wordt gegenereerd.
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67763b29744c4262249ef1ec04e7df490b31fe5b
ms.sourcegitcommit: 1e6a7b50596eaf9d965e0155f3f2c50f7f50747e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/22/2020
ms.locfileid: "3498087"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Een ER-indeling aanpassen om een aangepast elektronisch document te genereren

[!include[banner](../includes/banner.md)]

In de procedures in dit onderwerp wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Functioneel consultant elektronische rapportage deze taken kan uitvoeren:

- [Parameters voor het ER-raamwerk (elektronische rapportage) configureren](general-electronic-reporting.md).
- Door Microsoft geleverde ER-configuraties importeren, waarmee een betalingsbestand wordt gegenereerd terwijl een [leveranciers betaling](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) wordt verwerkt.
- Een aangepaste versie maken van een standaardconfiguratie voor een ER-indeling die door Microsoft wordt geleverd.
- De aangepaste ER-indelingsconfiguratie aanpassen, zodat betalingsbestanden worden gegenereerd die voldoen aan de vereisten van een specifieke bank.
- Wijzigingen in de standaardconfiguraties voor ER-indelingen overnemen in de aangepaste ER-indelingsconfiguratie.

U kunt alle volgende procedures uitvoeren in het bedrijf **GBSI**. U hoeft hiervoor geen code te schrijven.

- [Het ER-raamwerk configureren](#ConfigureFramework)

    - [ER-parameters configureren](#ConfigureParameters)
    - [Een ER-configuratieprovider activeren](#ActivateProvider)

        - [De lijst met ER-configuratie providers bekijken](#ReviewProvidersList)
        - [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider)
        - [Een ER-configuratieprovider activeren](#ActivateAddedProvider)

- [De standaardconfiguraties voor ER-indeling importeren](#ImportERSolution1)

    - [De standaard-ER-configuraties importeren](#ImportERFormat1)
    - [De geïmporteerde ER-configuraties bekijken](#ReviewImportedERSolution)

- [Een leveranciersbetaling voorbereiden voor verwerking](#PrepareVendorPayment)

    - [Bankgegevens toevoegen voor een leveranciersaccount](#AddBankAccount)
    - [Een leveranciersbetaling invoeren](#EnterVendorPayment)

- [Een leveranciersbetaling verwerken met de standaard-ER-indeling](#ProcessVendorPayment1)

    - [De elektronische betalingsmethode configureren](#ConfigureMethodOfPayment1)
    - [Een leveranciersbetaling verwerken](#ProcessPayment1)

- [De standaard-ER-indeling aanpassen](#CustomizeProvidedFormat)

    - [Een aangepaste indeling maken](#DeriveProvidedFormat)
    - [Een aangepaste indeling bewerken](#ConfigureDerivedFormat)
    - [Een aangepaste indeling markeren als uitvoerbaar](#MarkFormatRunnable)

- [Een leveranciersbetaling verwerken met de aangepaste ER-indeling](#ProcessVendorPayment2)

    - [De elektronische betalingsmethode configureren](#ConfigureMethodOfPayment2)
    - [Een leveranciersbetaling verwerken](#ProcessPayment2)

- [Nieuwe versies van de standaardconfiguraties voor ER-indeling importeren](#ImportERSolution2)

    - [Nieuwe versies van de standaard-ER-configuraties importeren](#ImportERFormat2)
    - [De geïmporteerde ER-indelingsconfiguraties bekijken](#ReviewImportedERFormat)

- [De wijzigingen in de nieuwe versie van een geïmporteerde indeling in een aangepaste indeling overnemen](#AdoptNewBaseVersion)

    - [De huidige conceptversie van een aangepaste indeling voltooien](#CompleteDerivedFormat)
    - [Een aangepaste indeling rebasen op een nieuwe basisversie](#RebaseDerivedFormat)
    - [Een leveranciersbetaling verwerken met de gerebasede ER-indeling](#ProcessPayment3)

- [Aanvullende bronnen](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Het ER-raamwerk configureren

Als u een gebruiker bent in de rol Functioneel consultant elektronische rapportage, moet u de minimale set ER-parameters configureren voordat u het ER-framework kunt gaan gebruiken om een aangepaste versie van een standaard-ER-indeling te ontwerpen.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER-parameters configureren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.
4. Stel op het tabblad **Bijlagen** de volgende parameters in:

    - Selecteer in het veld **Configuraties** het type **Bestand** voor het bedrijf **USMF**.
    - Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.

Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Een ER-configuratieprovider activeren

Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider. De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt. Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.

> [!NOTE]
> Alleen de eigenaar van een ER-configuratie kan deze bewerken. Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>De lijst met ER-configuratie providers bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL. Bekijk de inhoud van deze pagina. Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Een nieuwe ER-configuratieprovider toevoegen

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Selecteer **Nieuw** op de pagina **Configuratieproviders**.
4. Voer in het veld **Naam** de tekst **Litware, Inc.** in.
5. Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.
6. Selecteer **Opslaan**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Een ER-configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.

Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>De standaardconfiguraties voor ER-indeling importeren

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>De standaard-ER-configuraties importeren

Als u de standaard-ER-configuraties wilt toevoegen aan uw huidige exemplaar van Microsoft Dynamics 365 Finance, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die voor dat exemplaar is geconfigureerd.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.
3. Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**. Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.
4. Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **BACS (UK)**.
5. Selecteer op het sneltabblad **Versies** de versie **1.1** van de geselecteerde ER-indelingsconfiguratie.
6. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.

![Configuratie archiefpagina](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>De geïmporteerde ER-configuraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit.
4. Naast de geselecteerde ER-indeling **BACS (UK)** zijn ook er nog andere vereiste-configuraties geïmporteerd. Controleer of de volgende ER-configuraties beschikbaar zijn in de configuratiestructuur:

    - **Betalingsmodel**: Deze configuratie bevat het ER-onderdeel [Gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) dat de gegevensstructuur van het zakelijke betalingsdomein vertegenwoordigt.
    - **Toewijzing voor betalingsmodel 1611**: Deze configuratie bevat het ER-onderdeel [Modeltoewijzing](general-electronic-reporting.md#data-model-and-model-mapping-components) dat aangeeft hoe het gegevensmodel tijdens runtime wordt ingevuld met toepassingsgegevens.
    - **BACS (UK)**: Deze configuratie bevat de ER-onderdelen [Indeling](general-electronic-reporting.md#FormatComponentOutbound) en Indelingstoewijzing. Het onderdeel Indeling specificeert de rapportindeling. Het onderdeel indelingstoewijzing bevat de modelgegevensbron en geeft aan hoe de rapportindeling wordt ingevuld door deze gegevensbron te gebruiken tijdens runtime.

![Pagina Configuraties](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Een leveranciersbetaling voorbereiden voor verwerking

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Bankgegevens toevoegen voor een leveranciersaccount

U moet bankgegevens toevoegen voor een leveranciersaccount waarnaar later wordt verwezen in een geregistreerde betaling.

1. Ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**.
2. Selecteer op de pagina **Alle leveranciers** de leveranciersaccount **GB_SI_000001** en selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Instellen** de optie **Bankrekeningen**.
3. Selecteer op de pagina **Bankrekeningen van leveranciers** de optie **Nieuw** en voer de volgende gegevens in:

    1. Voer in het veld **Bankrekening** de waarde **GBP OPER** in.
    2. Selecteer in het veld **Bankgroepen** de waarde **BankGBP**.
    3. Voer in het veld **Bankrekeningnummer** de waarde **202015** in.
    4. Voer in het veld **SWIFT-code** de waarde <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** in.
    5. Voer in het veld **IBAN** de waarde **GB33BUKB20201555555555** in.
    6. U kunt in het veld **Routenummer** de standaardwaarde <a id="DefineRoutingNumber"></a>**123456** aanhouden.

    ![Pagina Bankrekeningen van leverancier](./media/er-quick-start2-bank-account.png)

4. Selecteer **Opslaan**.
5. Sluit de pagina.
6. Open op de pagina **Alle leveranciers** de leveranciersrekening **GB_SI_000001**.
7. Selecteer op de pagina met leveranciersgegevens de optie **Bewerken** om de pagina zo nodig bewerkbaar te maken.
8. Ga naar het sneltabblad **Betaling** en selecteer in het veld **Bankrekening** de waarde **GBP OPER**.

    ![Pagina Details leverancier](./media/er-quick-start2-bank-account-reference.png)

9. Selecteer **Opslaan**.
10. Sluit de pagina.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Een leveranciersbetaling invoeren

U moet een nieuwe leveranciersbetaling invoeren door middel van een [betalingsvoorstel](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer **Nieuw** op de pagina **Journaal met betalingen van leverancier**.
3. Selecteer in het veld **Naam** de waarde **VendPay**.
4. Selecteer **Regels**
5. Selecteer **Betalingsvoorstel** \> **Betalingsvoorstel maken**.
6. Configureer in het dialoogvenster **Betalingsvoorstel voor leverancier** alleen voorwaarden voor het filteren van records met de leveranciersrekening **GB_SI_000001** en selecteer vervolgens **OK**.
7. Selecteer de regel voor de factuur **00000007_Inv** en selecteer vervolgens **Betaling maken**.

    ![Dialoogvenster Betalingsvoorstel voor leverancier](./media/er-quick-start2-payment-proposal.png)

8. Controleer of de ingevoerde betaling is geconfigureerd voor gebruik van de betalingsmethode **Elektronisch**.

    ![Pagina Leveranciersbetalingen](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Een leveranciersbetaling verwerken met de standaard-ER-indeling

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>De elektronische betalingsmethode configureren

U moet de betalingsmethode Elektronisch configureren, zodat deze de geïmporteerde ER-indelingsconfiguratie gebruikt.

1. Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.
2. Selecteer op de pagina **Betalingsmethoden - leveranciers** de betalingsmethode **Elektronisch** in het linkerdeelvenster.
3. Selecteer **Bewerken**.
4. Stel op het sneltabblad **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.
5. Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indelingsconfiguratie **BACS (UK)**.

    ![Pagina Betalingsmethoden - leveranciers](./media/er-quick-start2-method-of-payment1.png)

6. Selecteer **Opslaan**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Een leveranciersbetaling verwerken

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd en selecteer vervolgens **Regels**.
3. Selecteer op de pagina **Leveranciersbetalingen** de waarde **Betalingen genereren**.
4. Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:

    - Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
    - Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.

5. Selecteer **OK**.
6. Stel in het dialoogvenster **Parameters elektronische rapport** de optie **Controlerapport afdrukken** in op **Ja** en selecteer **OK**.

    ![Pagina Parameters elektronisch rapport](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Naast het betalingsbestand kunt u nu ook het controlerapport genereren.

7. Download het zip-bestand en pak de volgende bestanden uit:

    - Het controlerapport in Excel-indeling
    - Het betalingsbestand in txt-indeling

        Merk op dat conform de [structuur](#PositionRoutingNumber) van de opgegeven ER-indeling de betalingsregel in het gegenereerde bestand begint met het routenummer dat was [gedefinieerd](#DefineRoutingNumber) voor de geconfigureerde bankrekening.

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>De standaard-ER-indeling aanpassen

Voor het voorbeeld dat in deze sectie wordt getoond, wilt u de ER-configuraties gebruiken die door Microsoft worden geleverd om betalingsbestanden voor leveranciers te genereren in de BACS-indeling. Maar u moet een aanpassing toevoegen om de behoeften van een bepaalde bank te ondersteunen. U wilt ook uw aangepaste indeling kunnen upgraden wanneer er nieuwe versies van de ER-configuraties beschikbaar komen. U wilt de upgrade echter wel uitvoeren tegen de laagste kosten.

In dit geval moet u als vertegenwoordiger van Litware, Inc. een nieuwe ER-indelingsconfiguratie maken (afleiden) met de door Microsoft geleverde configuratie **BACS (UK)** als basis.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Een aangepaste indeling maken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK)**. Litware, Inc. gebruikt versie 1.1 van deze ER-indelingsconfiguratie als basis voor de aangepaste versie.
3. Klik op **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen. Met behulp van dit dialoogvenster kunt u een nieuwe configuratie voor een aangepaste betalingsindeling maken.
4. Selecteer in de veldgroep **Nieuw** de optie **Afleiden van naam: BACS (VK), Microsoft**.
5. Voer in het veld **Naam** de waarde **BACS (UK, aangepast)** in.

    ![Het vervolgkeuzemenu Configuratie maken](./media/er-quick-start2-add-derived-format.png)

6. Selecteer **Configuratie maken**.

Versie 1.1.1 van de ER-indelingsconfiguratie **BACS (UK, aangepast)** wordt gemaakt. Deze versie heeft de [status](general-electronic-reporting.md#component-versioning) **Concept** en kan worden bewerkt. De huidige inhoud van uw aangepaste ER-indeling komt overeen met de inhoud van de indeling die wordt geleverd door Microsoft.

![Pagina Configuraties](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Een aangepaste indeling bewerken

U moet de aangepaste indeling zo configureren dat deze voldoet aan de vereisten die uw bank stelt. Een bank kan bijvoorbeeld vereisen dat betalingsbestanden die zijn gegenereerd, de SWIFT-code (Society for Worldwide Interbank Financial Telecommunication) bevatten van een bank waaraan de rol van agent is toegewezen in de verwerkte leverancierbetaling. SWIFT-codes zijn internationale bankcodes waarmee wereldwijd specifieke banken worden geïdentificeerd. Deze worden ook wel BIC's (Bank Identifier Codes) genoemd. De SWIFT-code moet 11 tekens lang zijn en moet aan het begin van elke betalingsregel in een gegenereerd betalingsbestand staan.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK, aangepast)**.
3. Selecteer op het sneltabblad **Versies** de versie **1.1.1** van de geselecteerde configuratie.
4. Selecteer **Ontwerper**.
5. Selecteer op de pagina **Indelingsontwerper** de optie **Details weergeven** om meer informatie over de indelingselementen weer te geven.
6. Vouw de volgende elementen uit en bekijk ze:

    - Het element **BACSReportsFolder** van het type **Map**. Dit element wordt gebruikt om uitvoer in zip-indeling te genereren.
    - Het element **bestand** van het type **Bestand**. Dit element wordt gebruikt om een betalingsbestand in txt-indeling te genereren.
    - Het element **transactions** van het type **Reeks**. Dit element wordt gebruikt om een enkele betalingsregel in een betalingsbestand te genereren.
    - Het element **transaction** van het type **Reeks**. Dit element wordt gebruikt om individuele velden van een enkele betalingsregel te genereren.

7. Selecteer het element **transaction**.

    ![Het element transaction in de ER Operations-ontwerper](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Het opgegeven rapport wordt zo geconfigureerd dat <a id="PositionRoutingNumber"></a>elke betalingsregel begint met het routenummer van de bank. Hiervoor wordt het indelingselement **vendBankRouteNum** gebruikt. 

8. Selecteer **Toevoegen** en selecteer vervolgens het type **Tekst\\tekenreeks** van het indelingselement dat u wilt toevoegen:

    1. Voer in het veld **Naam** de tekst **vendBankSWIFT** in.
    2. Voer in het veld **Minimumlengte** **11** in.
    3. Voer in het veld **Maximumlengte** **11** in.
    4. Selecteer **OK**.

    > [!NOTE]
    > Het element **vendBankSWIFT** wordt gebruikt om de SWIFT-code van de bank van een leverancier in gegenereerde bestanden in te voeren.

9. Selecteer in de boomstructuur met indelingsstructuren de waarde **vendBankSWIFT**.
10. Selecteer **Omhoog** om het geselecteerde opmaakelement één niveau omhoog te verplaatsen. Herhaal deze stap totdat het element **vendBankSWIFT** het <a id="PositionSWIFTCode"></a>eerste element onder het bovenliggende element **transaction** is.

    ![VendBankSWIFT als eerste element onder transaction in de ER Operations-ontwerper](./media/er-quick-start2-derived-format1.png)

11. Terwijl het element **vendBankSWIFT** nog steeds is geselecteerd in de structuur met de indelingsstructuur, selecteert u het tabblad **Toewijzing** en vouwt u vervolgens de gegevensbron **model** uit.
12. Vouw **model.Payment** \> **model.Payment.CreditorAgent** uit en selecteert het gegevensbronveld **model.Payment.CreditorAgent.BICFI**. Met dit veld van de gegevensbron wordt de SWIFT-code beschikbaar gemaakt van een leveranciersbank waaraan de rol van de agent in de verwerkte leverancierbetaling is toegewezen.
13. Selecteer **Binden**. Het indelingselement **vendBankSWIFT** is nu gekoppeld aan het gegevensbronveld **model.Payment.CreditorAgent.BICFI**, zodat SWIFT-codes worden ingevoerd in gegenereerde betalingsbestanden.

    ![Indelingselement vendBankSWIFT dat is gekoppeld aan het gegevensbronveld model.Payment.CreditorAgent.BICFI in de ER Operations-ontwerper](./media/er-quick-start2-derived-format2.png)

14. Selecteer **Opslaan**.
15. Sluit de pagina met de ontwerper.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Een aangepaste indeling markeren als uitvoerbaar

Nu de eerste versie van uw aangepaste indeling is gemaakt en de status **Concept** heeft , kunt u deze versie uitvoeren om hem te testen. Om het rapport uit te voeren, moet u een leveranciersbetaling verwerken met behulp van de betalingsmethode die verwijst naar door u aangepaste ER-indeling. Wanneer u een ER-indeling aanroept vanuit de toepassing, worden standaard alleen de versies met de status **Voltooid** en **Gedeeld** [meegenomen](general-electronic-reporting.md#component-versioning). Dit gedrag voorkomt dat ER-indelingsprofielen met niet-voltooide ontwerpen worden gebruikt. Voor het testen kunt u de toepassing dwingen de versie van de ER-indeling te gebruiken met de status **Concept**. Op deze manier kunt u de versie van de huidige indelingsversie aanpassen als er wijzigingen nodig zijn. Meer informatie over dit onderwerp vindt u in [Toepasbaarheid](electronic-reporting-destinations.md#applicability).

Als u de conceptversie van een ER-indeling wilt gebruiken, moet u de ER-indeling expliciet markeren.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.
4. Selecteer zo nodig **Bewerken** om de huidige pagina bewerkbaar te maken.
5. Selecteer in de configuratiestructuur in het linkerdeel venster de waarde **BACS (UK, aangepast)**.
6. Stel de optie **Concept uitvoeren** in op **Ja**.

    ![De optie Concept uitvoeren op de pagina Configuraties](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Een leveranciersbetaling verwerken met de aangepaste ER-indeling

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>De elektronische betalingsmethode configureren

U moet de elektronische betalingsmethode configureren, zodat de aangepaste ER-indeling wordt gebruikt voor de verwerking van leveranciersbetalingen.

1. Ga naar **Leveranciers** \> **Betalingsinstelling** \> **Betalingsmethoden**.
2. Selecteer op de pagina **Betalingsmethoden - leveranciers** de betalingsmethode **Elektronisch** in het linkerdeelvenster.
3. Selecteer **Bewerken**.
4. Stel op het sneltabblad **Bestandsindelingen** de optie **Algemene elektronische exportindeling** in op **Ja**.
5. Selecteer in het veld **Indelingsconfiguratie exporteren** de ER-indelingsconfiguratie **BACS (UK, aangepast)**.

    ![Pagina Betalingsmethoden - leveranciers](./media/er-quick-start2-method-of-payment2.png)

6. Selecteer **Opslaan**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Een leveranciersbetaling verwerken

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd.
3. Selecteer **Regels**
4. Selecteer op de pagina **Leveranciersbetalingen** boven het raster **Betalingsstatus** \> **Geen**.
5. Selecteer **Betaling genereren**.
6. Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:

    - Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
    - Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.

7. Selecteer **OK**.
8. Stel in het dialoogvenster **Parameters elektronische rapport** de optie **Controlerapport afdrukken** in op **Ja** en selecteer **OK**.

    > [!NOTE]
    > Naast het betalingsbestand kunt u nu alleen het controlerapport genereren.

9. Download het zip-bestand en pak de volgende bestanden uit:

    - Het controlerapport in Excel-indeling
    - Het betalingsbestand in txt-indeling

        Merk op dat, conform de structuur van uw aangepaste ER-indeling, de betalingsregel in het gegenereerde bestand nu [begint](#PositionSWIFTCode) met de SWIFT-code die is [ingevoerd](#DefineSWIFTCode) voor de bankrekening van de leverancier voor wie de betaling is verwerkt.

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Nieuwe versies van de standaardconfiguraties voor ER-indeling importeren

Voor het voorbeeld dat in deze sectie wordt weergegeven, ontvangt u een melding over Knowledge Base-artikel [KB 3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). In dit bericht wordt u gewaarschuwd over de nieuwe versie van de ER-indeling **BACS (UK)** die door Microsoft is gepubliceerd. Behalve het controlerapport kunnen gebruikers met deze nieuwe versie het betalingsadviesrapport en het bijbehorende notarapport genereren tijdens het verwerken van een leveranciersbetaling. U wilt deze functionaliteit gaan gebruiken.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Nieuwe versies van de standaard-ER-configuraties importeren

Als u de nieuwe versies van de ER-configuraties wilt toevoegen aan het huidige Finance-exemplaar, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die u voor dat exemplaar hebt geconfigureerd.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider Microsoft weer te geven.
3. Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**. Als u wordt gevraagd om toestemming te geven om verbinding te maken met de Regulatory Configuration Service, volgt u de instructies voor autorisatie.
4. Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **BACS (UK)**.
5. Selecteer op het sneltabblad **Versies** de versie **3.3** van de geselecteerde ER-indelingsconfiguratie.
6. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.

![Configuratie archiefpagina](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Lifecycle Services (LCS).

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>De geïmporteerde ER-indelingsconfiguraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK)**.
4. Selecteer op het sneltabblad **Versies** de versie **3.3**.
5. Selecteer **Ontwerper**.
6. Vouw op de **pagina Indelingsontwerper** het indelingselement **BACSReportsFolder** uit.
7.  Merk op dat versie 3.3 het indelingselement **PaymentAdviceReport** bevat, dat wordt gebruikt om een betalingsadviesrapport te genereren wanneer een leveranciersbetaling wordt verwerkt.

    ![Het indelingselement PaymentAdviceReport in de ER Operations-ontwerper](./media/er-quick-start2-imported-solution2.png)

8. Sluit de pagina met de ontwerper.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>De wijzigingen in de nieuwe versie van een geïmporteerde indeling in een aangepaste indeling overnemen

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>De huidige conceptversie van een aangepaste indeling voltooien

Als u de huidige status van de aangepaste indeling wilt behouden, voltooit u de conceptversie 1.1.1 door de status te wijzigen van **Concept** in **Voltooid**.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit. Vouw hieronder **BACS (UK)** uit en selecteer **BACS (UK, aangepast)**.
4. Selecteer op het sneltabblad **Versies** de optie **Status wijzigen** \> **Voltooien** en selecteer vervolgens **OK**.

De status van versie 1.1.1 wordt gewijzigd van **Concept** in **Voltooid** en de versie wordt alleen-lezen. Er is een nieuwe bewerkbare versie 1.1.2 toegevoegd, met de status **Concept**. U kunt deze versie gebruiken om verdere wijzigingen aan te brengen in de aangepaste ER-indeling.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Een aangepaste indeling rebasen op een nieuwe basisversie

Als u de nieuwe functionaliteit van versie 3.3 van de indeling **BACS (UK)** wilt gebruiken in uw aanpassingen, moet u de basisconfiguratieversie wijzigen voor de aangepaste configuratie, **BACS (UK, aangepast)**. Dit proces wordt [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) genoemd. Gebruik in plaats van versie 1.1 van **BACS (UK)** de nieuwe versie 3.3.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Betalingsmodel** uit en selecteer **BACS (UK, aangepast)**.
3. Selecteer op het sneltabblad **Versies** versie **1.1.2** en selecteer vervolgens **Rebase**.
4. Selecteer in het dialoogvenster **Rebase** in het veld **Doelversie** de versie **3.3** van de basisconfiguratie om deze toe te passen als de nieuwe basis en gebruik deze om de configuratie bij te werken.

    ![Het dialoogvenster Rebase](./media/er-quick-start2-rebase1.png)

5. Selecteer **OK**.
6. U ziet dat het nummer van de conceptversie is gewijzigd van **1.1.2** in **3.3.2**, wat de wijziging van de basisversie weergeeft.

    Wanneer de aangepaste versie en een nieuwe basisversie worden samengevoegd, kunnen conflicten worden gedetecteerd vanwege indelingswijzigingen die niet automatisch kunnen worden samengevoegd.

    ![Gerebasede configuratie met conflicten op de pagina Configuraties](./media/er-quick-start2-rebase2.png)

    Als conflicten worden gedetecteerd, moeten deze handmatig worden opgelost in de indelingsontwerper.

7. Selecteer op het sneltabblad **Versies** de versie **3.3.2**.
8. Selecteer **Ontwerper**.
9. Selecteer op de pagina **Indelingsontwerper** op het sneltabblad **Details** een rebase-conflictrecord en selecteer vervolgens **Basiswaarde toepassen**.

    ![Een rebase-conflictrecord in de ER Operations-ontwerper](./media/er-quick-start2-rebase3.png)

10. Selecteer **Opslaan**.

    De rebase-conflictrecord moet nu niet meer zichtbaar zijn op het sneltabblad **Details**.

    ![Conflict opgelost in de ER Operations-ontwerper](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > U hebt het conflict opgelost door te bevestigen dat versie 3 van het basis model moet worden gebruikt in deze ER-indeling.

11. Navigeer naar **BACSReportsFolder** \> **bestand** \> **transacties** \> **transactie**.
12. Op het tabblad **Toewijzing** ziet u dat versie 3.3.2 van de aangepaste ER-indeling zowel uw aanpassing bevat (het indelingselement **vendBankSWIFT** en de binding ervan) als ook de nieuwe functionaliteit van versie 3.3 van de basis-ER-indeling, die door Microsoft is geleverd (het indelingselement **PaymentAdviceReport Format** samen met de geneste elementen en geconfigureerde bindingen). Met slechts enkele muisklikken hebt u de wijzigingen van een nieuwe basisversie toegepast door deze samen te voegen met uw aanpassingen.

    ![Samengevoegde indeling in de ER Operations-ontwerper](./media/er-quick-start2-rebase5.png)

13. Sluit de pagina met de ontwerper.

> [!NOTE]
> De rebase-actie kan ongedaan worden gemaakt. Als u deze rebase wilt annuleren, selecteert u versie **1.1.1** van de indeling **BACS (UK, aangepast)** op het sneltabblad **Versies** en selecteert u **Deze versie ophalen**. Versie 3.3.2 krijgt dan weer het nummer 1.1.2 en de inhoud van conceptversie 1.1.2 komt weer overeen met de inhoud van versie 1.1.1.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Een leveranciersbetaling verwerken met de gerebasede ER-indeling

1. Ga naar **Leveranciers** \> **Betalingen** \> **Betalingsjournaal**.
2. Selecteer op de pagina **Betalingsjournaal van leverancier** het betalingsjournaal dat u eerder hebt toegevoegd.
3. Selecteer **Regels**
4. Selecteer op de pagina **Leveranciersbetalingen** boven het raster **Betalingsstatus** \> **Geen**.
5. Selecteer **Betaling genereren**.
6. Voer in het dialoogvenster **Betalingen genereren** de volgende informatie in:

    - Selecteer in het veld **Betalingsmethode** de optie **Elektronisch**.
    - Selecteer in het veld **Bankrekening** de optie **GBSI OPER**.

7. Selecteer **OK**.
8. Voer in het dialoogvenster **Parameters elektronisch rapport** de volgende informatie in:

    - Zet de optie **Controlerapport afdrukken** op **Ja**.
    - Zet de optie **Betalingsadvies afdrukken** op **Ja**.

    ![Dialoogvenster Parameters elektronisch rapport](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Naast het betalingsbestand kunt u nu zowel het controlerapport als het betalingsadviesrapport genereren.

9. Selecteer **OK**.
10. Download het zip-bestand en pak de volgende bestanden uit:

    - Het controlerapport in Excel-indeling
    - Het betalingsadvies in Excel-indeling

        ![Betalingsadviesrapport in Excel-indeling](./media/er-quick-start2-payment-advice-report.png)

    - Het betalingsbestand in txt-indeling

        Merk op dat, conform de structuur van uw aangepaste ER-indeling, de betalingsregel in het gegenereerde bestand nu begint met de SWIFT-code die is ingevoerd voor de bankrekening van een leverancier voor wie de betaling is verwerkt.

        ![Betalingsbestand in txt-indeling](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [ER-configuraties downloaden uit Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](er-download-configurations-global-repo.md)
