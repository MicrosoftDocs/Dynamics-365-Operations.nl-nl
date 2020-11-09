---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Italië in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039787"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> De invoegtoepassing elektronische facturering voor Italië ondersteunt momenteel mogelijk niet alle functies die beschikbaar zijn voor elektronische facturen in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management. 

Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Italië. U wordt door de configuratiestappen geleid die landafhankelijk zijn in de Regulatory Configuration Services (RCS) en Finance. Verder wordt u door het proces voor het indienen van elektronische facturen geleid die worden gegenereerd in de Italiaanse **FatturaPA** -indeling via de service, en hierin wordt uitgelegd hoe u de resultaten van de verwerking kunt controleren.

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp uitvoert, moet u de stappen uitvoeren in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-instellingen

Tijdens de RCS-instelling voert u de volgende taken uit:

1. Importeer de functie e-Facturering voor het exporteren van elektronische facturen van klanten in de **FatturaPA** -indeling.
2. Controleer de indelingsconfiguraties die nodig zijn voor het genereren, indienen en ontvangen van respons op elektronische facturen.
3. Configureer die de gebeurtenissen die scenario's voor het indienen van elektronische facturen ondersteunen.
4. Publiceer de functie e-Facturering.

> [!NOTE]
> 'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server van de invoegtoepassing voor elektronische facturering. In dit geval is het exporteren van elektronische klantfacturen de functie e-Facturering die u gaat instellen.

## <a name="import-the-e-invoicing-feature"></a>De functie e-Facturering importeren

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **e-Facturering**.
3. Op de pagina **Functies voor e-Facturering** selecteert u **Importeren** om de functie e-Facturering uit de algemene opslagplaats te importeren.

    > [!NOTE]
    > Als u de lijst met beschikbare functies niet ziet, selecteert u **Synchroniseren**. 

4. Selecteer de functie **E-facturen exporteren (IT)** en selecteer **Importeren**.

![De functie E-facturen importeren (IT) exporteren](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Wanneer u de functie **E-facturen exporteren (IT)** uit de algemene opslagplaats importeert, worden alle instellingen die in de volgende secties worden beschreven, ook geïmporteerd.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Een nieuwe versie van de functie E-facturen exporteren (IT) maken

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Nieuw**. 

    ![Een nieuwe versie van de functie e-Facturering toevoegen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Hierna configureert u de indelingen voor elektronische rapportage (ER) die aan de functie e-Facturering zijn gekoppeld.

2. Selecteer op het tabblad **Configuraties** de optie **Toevoegen** om de configuratieversies te beheren.

    ![Configuratieversies voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    In deze stap voegt u de ER-indelingen toe voor verschillende bestanden die worden gebruikt voor het exporteren van Italiaanse e-facturen. Voor Italiaanse FatturaPA e-facturen gebruikt u de volgende standaardconfiguraties of de feitelijke aangepaste configuraties die u gebruikt voor e-facturering:

    - Verkoopfactuur (IT)
    - Projectfactuur (IT)

    Wanneer u een functie e-Facturering maakt die is afgeleid van een andere functie voor e-facturering, worden alle ER-indelingen overgenomen van de oorspronkelijke functie.

3. Selecteer een specifieke configuratie voor bestanden met een ER-indeling.
4. Selecteer **Bewerken** of **Weergeven** om de pagina **Indelingsontwerper** te openen.

    ![De pagina Indelingsontwerper openen](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Gebruik de pagina **Indelingsontwerper** om de configuratie van bestanden met een ER-indeling te bewerken en weer te geven.

    ![Pagina Indelingsontwerper](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>De instellingen voor de functie e-Facturering beheren

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** de optie **Toevoegen** , **Verwijderen** of **Bewerken** om de instellingen van de functie e-Facturering te beheren.

![De instellingen voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

In deze stap configureert u de gebeurtenissen die van toepassing zijn op elektronische facturen, waaronder het genereren van de XML-uitvoerbestanden in **FatturaPA** -indeling en digitale handtekening (indien nodig).

### <a name="configure-the-sales-invoice-feature-setup"></a>De instellingen van de functie Verkoopfactuur configureren

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Verkoopfactuur**.
2. Selecteer **Bewerken**.
3. Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren. Met acties kunt u een lijst met bewerkingen definiëren die na elkaar moeten worden uitgevoerd om de gebeurtenis volledig uit te voeren.

    ![Tabblad Acties](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Actie-ID | Naam actie        | Omschrijving van de actie                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Document transformeren | Maak het XML-bestand van de e-factuur in **FatturaPA** -indeling. |
    | 2         | Document ondertekenen      | Pas een digitale handtekening toe op het XML-bestand.             |

4. Selecteer het tabblad **Toepasbaarheidsregels** om de toepasbaarheidsregels weer te geven en te onderhouden. Regels voor toepasbaarheid definiëren de context waarin de actie wordt uitgevoerd.

    ![Tabblad Toepasbaarheidsregels](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Selecteer het tabblad **Variabelen** om de variabelen weer te geven en te onderhouden.

    ![Tabblad Variabelen](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. De openbare variabelen definiëren die vereist zijn om de acties uit te voeren.

### <a name="configure-the-project-invoice-feature-setup"></a>De instellingen van de functie Projectfactuur configureren 

De stappen en instellingen die nodig zijn om de instelling van de functie **Projectfactuur** te configureren, zijn vergelijkbaar met de stappen en instellingen voor de instelling van de functie **Verkoopfactuur**. Zie de procedures voor verkoopfacturen wanneer u met projectfacturen werkt.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>De functie e-Facturering aan de omgeving toewijzen

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Omgevingen** de optie **Inschakelen**.
2. Selecteer de omgeving in het veld **Omgeving**.
3. Selecteer in het veld **Geldig vanaf** de ingangsdatum van de omgeving.
4. Selecteer **Inschakelen**. 

![De omgeving voor e-Facturering inschakelen](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>De functie e-Facturering publiceren

U kunt de functie e-Facturering publiceren door de versiestatus te wijzigen in **Voltooid** of **Gepubliceerd**.

### <a name="change-the-version-status-to-completed"></a>De versiestatus wijzigen in Voltooid

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Concept**.
2. Selecteer **Status wijzigen \> Voltooien**. 

### <a name="change-the-version-status-to-published"></a>De versiestatus wijzigen in Gepubliceerd 

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Voltooid**.
2. Selecteer **Status wijzigen \> Publiceren**.

![De status van de functie e-Facturering wijzigen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance

Tijdens de instelling van Finance voert u de volgende taken uit:

1. Het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en de contextconfiguraties voor FatturaPA-e-facturen importeren.
2. Configureer het certificaat dat vereist is voor het digitaal ondertekenen van Italiaanse e-facturen.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Het ER-gegevens model, de toewijzing van gegevensmodellen en de indelingen importeren

1. Controleer in de werkruimte **Elektronische rapportage** of de configuratieaanbieder **Bedrijfsdocumentenservice** is ingesteld op **Actief**.
2. Selecteer **Opslagplaatsen**.
3. Selecteer **Algemene resource \> Openen**.
4. Importeer **Factuurmodel** , **Toewijzing factuurmodellen** en **Contextmodel klantfactuur**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>De functie voor het exporteren van elektronische klantfacturen voor Italië inschakelen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Schakel op het tabblad **Functies** het selectievakje **Ingeschakeld** in bij de rij voor functiereferentie **IT00036**.

![De functie FatturaPA inschakelen](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Elektronische documenten configureren

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen** en voer de tabellen in die vereist zijn om Italiaanse e-facturen te genereren:

    - **Tabelnaam:** Klantfactuurjournaal
    - **Tabelnaam:** Projectfactuur

3. Definieer voor elke tabel een gerelateerde documentcontext:

    - Selecteer voor **Klantfactuurjournaal** de optie **Klantfactuurcontext**.
    - Selecteer voor **Projectfactuur** de optie **Projectfactuurcontext**.

![Responstypen instellen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Verwerking van elektronische facturen

Tijdens de verwerking in Finance voert u de volgende taken uit:

1. Italiaanse e-facturen genereren via de invoegtoepassing voor elektronische facturering
2. De uitvoeringslogboeken weergeven en de resultaten van de verwerking beoordelen

### <a name="generate-electronic-invoices"></a>Elektronische facturen genereren

Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld en de functie **IT00036** hebt geactiveerd, kan het oude Finance-proces voor het genereren van Italiaanse e-facturen niet meer worden gebruikt. Het wordt vervangen door een nieuw proces met de naam **Elektronische documenten indienen**.

U kunt de documenten handmatig indienen op basis van uw behoefte aan e-factuurdocumenten.

> [!NOTE]
> Voordat u doorgaat, controleert u of de instellingen die nodig zijn voor de Italiaanse e-facturen zijn voltooid. Zie [Elektronische klantfacturen](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices) voor meer informatie. Houd er rekening mee dat sommige instellingsstappen die in dat onderwerp worden beschreven, mogelijk niet beschikbaar zijn vanwege de activering van elektronische facturering.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.
2. Als u een document voor het eerst indient, moet u de optie **Documenten opnieuw indienen** op **Nee** instellen. Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.
3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.

![Het dialoogvenster Elektronische documenten indienen](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filterquery

1. Configureer in het dialoogvenster **Query** de filtervoorwaarden voor verkoop- en projectfacturen of laat de voorwaarden leeg om alle ingediende facturen mee te nemen.

    ![Filtercriteria voor indienen instellen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Selecteer **OK** om het dialoogvenster **Query** te sluiten.
3. Klik op **OK** om de geselecteerde documenten in te dienen.

> ![OPMERKING] Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met de invoegtoepassing voor elektronische facturering te bevestigen. Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.

#### <a name="view-submission-logs"></a>Indieningslogboeken weergeven

U kunt de indieningslogboeken voor alle ingediende documenten weergeven.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** de optie **Klantfactuurjournaal** of **Projectfactuur** om te filteren op de vereiste elektronische documenten.

    ![Een documenttype selecteren om de indieningslogboeken weer te geven](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    De waarde die wordt weergegeven in de kolom **Indieningsstatus** staat voor de status van het indieningsproces. Hiermee wordt aangegeven of het proces volgens de configuratie is uitgevoerd en of er aanvullende actie vereist is.

3. Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.

    ![Details van indieningslogboeken weergeven](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Op het sneltabblad **Verwerkingsacties** kunt u het uitvoeringslogboek weergeven voor de acties die zijn geconfigureerd in de functieversie die is ingesteld in RCS. De kolom **Status** geeft aan of de actie met goed gevolg is uitgevoerd.
5. Op het sneltabblad **Actiebestanden** kunt u de tussenliggende bestanden weergeven die zijn gegenereerd tijdens de uitvoering van de acties. U kunt **Weergeven** selecteren om het uitvoer-XML-bestand in **FatturaPA** -indeling te downloaden en de inhoud weer te geven.

## <a name="related-topics"></a>Verwante onderwerpen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)
- [De invoegtoepassing voor elektronische facturering instellen](e-invoicing-setup.md)
