---
title: Aan de slag met Elektronische facturering voor Mexico
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Mexico.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4266d7bca163b1d6aa1261e086f10a4f0f5d7e360051db169fbcab34363c81c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742148"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>Aan de slag met Elektronische facturering voor Mexico

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronische facturering voor Mexico ondersteunt momenteel mogelijk niet alle functies die beschikbaar zijn in het document Comprobante Fiscal Digital por Internet (CFDI) en in de gerelateerde integratie die in Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management is ingebouwd.

Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Mexico. U wordt door de configuratiestappen geleid die landafhankelijk zijn in de Regulatory Configuration Services (RCS) en Finance. Daarnaast begeleidt het u door de stappen die u moet volgen om CFDI-facturen via de service in te dienen en er wordt uitgelegd hoe u de verwerkingsresultaten en de status van CFDI-facturen controleert.

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp uitvoert, moet u de stappen uitvoeren in [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-instellingen

Tijdens de RCS-instelling voert u de volgende taken uit:

1. De functie e-Facturering voor het verwerken van CFDI-facturen importeren.
2. Controleer de indelingsconfiguraties die nodig zijn voor het genereren, verzenden en ontvangen van antwoorden over CFDI-facturen en het indienen en ontvangen van antwoorden over annulering.
3. De gebeurtenissen configureren die de scenario's voor verzending van CFDI-facturen ondersteunen.
4. De functie e-Facturering voor CFDI-facturen publiceren.

> [!NOTE]
> 'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server voor elektronische facturering. In dit geval zijn CFDI-facturen (MX) de functie e-Facturering die u gaat instellen.

## <a name="import-the-e-invoicing-feature"></a>De functie e-Facturering importeren

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **e-Facturering**.
3. Op de pagina **Functies voor e-Facturering** selecteert u **Importeren** om de **CFDI-facturen (MX)** uit de algemene opslagplaats te importeren.

    > [!NOTE]
    > Als de functie niet in de lijst wordt weergeven, selecteert u **Synchroniseren** en herhaalt u stap 3.

![De CFDI-facturen (MX)-functie importeren.](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Wanneer u de **CFDI-facturen (MX)** importeert vanuit de algemene opslagplaats, worden alle functie-instellingen, inclusief configuraties en acties, ook geïmporteerd.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Een nieuwe versie van de functie CFDI-facturen (MX) maken

U kunt een nieuwe versie maken als bijvoorbeeld URL's moeten worden bijgewerkt. Zie [e-Facturering CFDI](tasks/mx-00010-e-invoicing-cfdi.md) voor meer informatie.

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Nieuw**.

![Een nieuwe versie van de functie e-Facturering toevoegen.](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>De configuratieversie bijwerken

1. Op de pagina **Functies voor e-Facturering** selecteert u op het tabblad **Configuraties** de optie **Toevoegen** of **Verwijderen** om de configuratieversies (configuraties van de ER-bestandsindeling) te beheren.

    ![Configuraties voor de functies van e-Facturering beheren.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Wanneer u een nieuwe versie maakt, worden alle configuraties overgenomen van de laatst gepubliceerde versie. Voor het verwerken van CFDI-facturen zijn de volgende configuraties vereist:

    - CFDI-factuur (BusinessdocumentService)
    - CFDI-antwoordbericht importeren
    - CFDI-foutenlogboek importeren
    - CFDI-annuleringsverzoek (MX) (BusinessdocumentService)
    - CFDI-factuur (BusinessdocumentService)

2. Selecteer een configuratieversie in de lijst en selecteer **Bewerken** of **Weergeven** om de pagina **Indelingsontwerper** te openen. Hier kunt u de configuratie bewerken of weergeven.

    ![De pagina Indelingsontwerper openen.](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Gebruik de pagina **Indelingsontwerper** om de configuratie van bestanden met een ER-indeling te bewerken en weer te geven. Zie [Configuraties voor elektronische documenten maken](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md) voor meer informatie.

    ![Pagina Indelingsontwerper.](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>De instellingen voor de functie e-Facturering beheren

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** de optie **Toevoegen**, **Verwijderen** of **Bewerken** om de instellingen van de functie e-Facturering te beheren.

![De instellingen voor de functie e-Facturering beheren.](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Als u CFDI-facturen wilt indienen voor autorisatie (het XML-bestand genereren, het XML-bestand verzenden en het antwoord verwerken), moet u de functie **Verkoopfactuur** instellen.

Voor het indienen van een annulering van een CFDI-factuur, moet u de functie **Annulering** en **Annuleren** instellen.

### <a name="configure-the-sales-invoice-feature-setup"></a>De instellingen van de functie Verkoopfactuur configureren

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Verkoopfactuur**.
2. Selecteer **Bewerken** om de acties, regels voor toepasbaarheid en variabelen te configureren.

    ![De instellingen voor de functie e-Facturering bewerken.](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren. Met acties kunt u een lijst met bewerkingen definiëren die na elkaar moeten worden uitgevoerd om de gebeurtenis volledig uit te voeren.

    ![Tabblad Acties.](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Actie-ID | Actie                   | Naam actie                                  | Omschrijving van de actie                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Document transformeren       | CFDI e-Factuur genereren zonder digitale handtekening | Genereer de CFDI e-Factuur.                                |
    | 2         | Document ondertekenen            | Digitale handtekening                                 | De elektronische factuur digitaal ondertekenen voor verzending.                |
    | 3         | Mexicaanse PAC-service aanroepen | CFDI e-Factuur indienen                        | De WCF-client (Windows Communication Foundation) verzendt de CFDI e-Factuur. |
    | 4         | Reactie verwerken         | Reactie van webservice analyseren                 | Analyseer de reactie van de webservice en stuur het foutenlogboek terug. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>De URL voor Mexicaanse PAC-webservices instellen 

1. Ga naar de pagina **Instellingen functieversie** en selecteer op het tabblad **Acties**, op het sneltabblad **Acties** de optie **Mexicaanse PAC-service aanroepen**.
2. Voer op het sneltabblad **Parameters** in het veld **URL-adres** de URL van de webservice voor het indienen van CFDI-facturen in.

> [!NOTE]
> Gebruik dezelfde stappen om de URL voor de actie **Mexicaanse PAC-service aanroepen** bij te werken voor de functie-instellingen van **Annuleren** en **Annuleringsverzoek**.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>De conceptversie toewijzen aan een e-Factureringsomgeving

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Omgevingen** de optie **Inschakelen**.
2. Selecteer de omgeving in het veld **Omgeving**.
3. Selecteer in het veld **Geldig vanaf** de ingangsdatum van de omgeving.
3. Selecteer **Inschakelen**.

![Een e-Factureringsomgeving inschakelen.](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>De versiestatus wijzigen in Voltooid

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Concept**.
2. Selecteer **Status wijzigen \> Voltooien**.

## <a name="change-the-version-status-to-published"></a>De versiestatus wijzigen in Gepubliceerd

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Status wijzigen \> Publiceren**.

## <a name="publish-the-e-invoicing-feature"></a>De functie e-Facturering publiceren

1. Op de pagina **Functies voor e-Facturering** selecteert u het tabblad **Versies** om de status van de functie **CFDI-facturen (MX)** te beheren.
2. Selecteer **Status wijzigen** als u de status van de functie wilt wijzigen.

![De status van de functie e-Facturering wijzigen.](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>Integratie van Elektronisch factureren instellen in Finance

Als u elektronische facturering in Finance wilt instellen, voert u de volgende taken uit:

1. Importeer het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en de indelingen die nodig zijn voor CFDI-facturen.
2. Responstypen configureren voor het bijwerken van de CFDI-facturen. Deze responstypen worden gebruikt voor de respons van de PAC-server (geautoriseerde certificeringsaanbieder).

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en contextconfiguraties voor CFDI-facturen importeren

1. Meld u aan bij Finance.
2. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**. Controleer of deze configuratieaanbieder is ingesteld op **Actief**. Zie [Aanbieders van configuraties maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor informatie over de manier waarop u een aanbieder als deze als **Actief** kunt instellen.
3. Selecteer **Opslagplaatsen**.
4. Selecteer **Algemene resource \> Openen**.
5. Importeer **Factuurmodel**, **Factuurmodeltoewijzing**, **CFDI-factuurindeling (MX)**, **Indeling annuleringsverzoek CFDI-factuur (MX)** en **Indeling annulering CFDI-factuur (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>De functie voor de verwerking van CFDI-facturen inschakelen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Schakel op het tabblad **Functies** het selectievakje **Inschakelen** in bij de rijen voor functiereferenties **MX-00010** en **MX-00016**.

![De functies voor de verwerking van CFDI-facturen inschakelen.](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER-configuraties importeren en responstypen instellen voor het bijwerken van CFDI-facturen

#### <a name="import-er-configurations"></a>ER-configuraties importeren

1. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.
3. Selecteer **Opslagplaatsen**.
4. Selecteer **Algemene resource \> Openen**.
5. Importeer **Model responsbericht**, **CFDI-foutenlogboek importeren (MX)** en **CFDI-responsbericht importeren (MX)**.

#### <a name="set-up-the-response-types"></a>De responstypen instellen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen**.
3. Voer het klantfactuurjournaal in en selecteer in het veld **Tabelnaam** de projectfactuur.
4. Definieer voor elke tabel een gerelateerde documentcontext:

    - Voer voor **Klantfactuurjournaal** de optie **Klantfactuurcontext** in.
    - Voer voor **Projectfactuur** de optie **Projectfactuurcontext** in.

4. Selecteer **Responstypen** om de responstypen te configureren die kunnen worden geretourneerd vanuit Elektronische facturering en die worden opgenomen in een klantfactuurjournaal of projectfactuur.
5. Selecteer **Nieuw** en selecteer in het veld **Responstype** de optie **Respons**.
6. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
7. Selecteer in het veld **Modeltoewijzing** de optie **Importindeling responsbericht – Modeltoewijzing van responsbericht**.
8. Selecteer **Opslaan**.
9. Selecteer **Nieuw** en selecteer in het veld **Responstype** de optie **Responsgegevens**.
10. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
11. Selecteer in het veld **Modeltoewijzing** de optie **Importindeling CFDI-responsgegevens (details) – Responsgegevens importeren**.
12. Selecteer **Opslaan**.

## <a name="process-electronic-invoices-in-finance"></a>Elektronische facturen in Finance verwerken 

Tijdens de verwerking van CFDI-facturen in Finance via Elektronische facturering kunt u de volgende taken uitvoeren:

- CFDI-facturen indienen.
- De uitvoeringslogboeken voor het indienen weergeven.
- De annulering van een CFDI-factuur indienen.

### <a name="submit-cfdi-invoices"></a>CFDI-facturen indienen

Nadat u de functie **Integratie configureerbare functie voor elektronisch factureren** hebt ingeschakeld, kunt u het proces **Elektronische factuur exporteren/importeren** (**Klanten \> Facturen \> E-facturen**) voor het indienen van CFDI-facturen niet meer gebruiken. Het wordt vervangen door een nieuw proces met de naam **Elektronische documenten indienen**.

> [!NOTE]
> Voordat u het nieuwe proces **Elektronische documenten indienen** gebruikt, moet u controleren of de instellingen die nodig zijn voor de Mexicaanse e-facturen zijn voltooid. Zie [CFDI-indeling versie 3.3](./latam-mex-cfdi-3-3.md) voor meer informatie.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.
2. Als u een document voor het eerst indient, moet u altijd de optie **Documenten opnieuw indienen** op **Nee** instellen. Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.
3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.

![Een CFDI-document indienen.](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met Elektronische facturering te bevestigen. Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.

### <a name="view-submission-logs"></a>Indieningslogboeken weergeven

U kunt de indieningslogboeken voor alle ingediende documenten of voor slechts één ingediend document weergeven.

#### <a name="view-all-submission-logs"></a>Alle indieningslogboeken weergeven

Nadat u de functie **Integratie configureerbare functie voor elektronisch factureren** hebt ingeschakeld, is er een nieuwe pagina beschikbaar waarmee u het indieningsproces voor documenten kunt opvolgen. U kunt deze pagina gebruiken om de indieningslogboeken voor alle ingediende documenten weer te geven.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** **Klantfactuurjournaal** om te filteren op de vereiste elektronische documenten.

    ![Een documenttype selecteren om de indieningslogboeken weer te geven.](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.

    ![Details van indieningslogboeken weergeven.](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

De informatie in de indieningslogboeken wordt verdeeld over drie sneltabbladen:

- **Verwerkingsacties**: dit sneltabblad toont het uitvoeringslogboek voor de acties die zijn geconfigureerd in de functieversie die is ingesteld in RCS. De kolom **Status** geeft aan of de actie met goed gevolg is uitgevoerd.
- **Actiebestanden**: dit sneltabblad toont de tussenliggende bestanden die zijn gegenereerd tijdens de uitvoering van de acties. U kunt **Weergave** selecteren om het bestand te downloaden en weer te geven.
- **Logboek verwerkingsacties**: dit sneltabblad toont de resultaten van de communicatie tussen Elektronische facturering en de doelwebservice. Het toont ook wat er is geretourneerd door de verwerking vanuit de webservice. De kolom **Foutcode** geeft de retourcode weer die is geretourneerd door de autorisatie-webservice.

Wanneer de ingediende CFDI-factuur is geautoriseerd, wordt de status ervan gewijzigd in **Goedgekeurd**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Indieningslogboeken weergeven vanuit CFDI-facturen

Nadat u de functie **Integratie configureerbare functie voor elektronisch factureren** hebt ingeschakeld, kunt u ook de indieningslogboeken van CFDI-facturen weergeven.

1. Ga naar **Klanten \> Query's en rapporten \> CFDI (elektronische facturen)**.
2. Selecteer een CFDI-factuur die is ingediend nadat de functie **Integratie configureerbare functie voor elektronisch factureren** is ingeschakeld.
3. Selecteer in het actievenster op het tabblad **Historie** de optie **Logboek elektronische documenten**.

![Indieningslogboeken weergeven vanuit CFDI-facturen.](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> Voor CFDI-facturen die zijn ingediend voordat de functie **Integratie configureerbare functie voor elektronisch factureren** is ingeschakeld, is de knop **Historie** beschikbaar. De knop **Historie** is niet beschikbaar voor CFDI-facturen die zijn ingediend nadat de functie **Integratie configureerbare functie voor elektronisch factureren** is ingeschakeld.

### <a name="submit-cancellation-of-cfdi-invoices"></a>De annulering van CFDI-facturen indienen

Nadat u de functie **Integratie configureerbare functie voor elektronisch factureren** hebt ingeschakeld, kan het oude proces voor het annuleren van CFDI-facturen niet meer worden gebruikt. Deze wordt vervangen door een nieuw annuleringsproces dat is ingesloten op de pagina **Indieningslogboek voor elektronische documenten**.

1. Ga naar **Klanten \> Query's en rapporten \> CFDI (elektronische facturen)**.
2. Als de CFDI-factuur de status **Goedgekeurd** heeft , selecteert u **Functies \> CFDI annuleren**.
3. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
4. Selecteer de CFDI-factuur en selecteer **Functies \> Gerelateerde indieningen verzenden**.
5. Voer een omschrijving voor de gerelateerde indiening in en selecteer **OK**.

#### <a name="view-cancellation-submission-logs"></a>Indieningslogboeken van annuleringen weergeven

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** **Klantfactuurjournaal** om alleen te filteren op klantfactuurjournaaldocumenten.
3. Selecteer de CFDI-factuur en selecteer in het actievenster **Query's \> Gerelateerde indiening**.

    De pagina **Gerelateerde indieningen** toont alle gerelateerde indieningen en de bijbehorende status voor een bepaalde CFDI-factuur. In de volgende afbeelding staat de eerste regel voor de indiening waarin om goedkeuring van de CFDI-factuur werd gevraagd. De tweede regel staat voor de indiening waarmee die CFDI-factuur werd geannuleerd.

    ![Indieningslogboeken van annuleringen weergeven.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.

    ![Details van indieningslogboeken van annuleringen weergeven.](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Privacyverklaring
Voor het inschakelen van de functie **CFDI Mexicaanse elektronische factuur (MX)** moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-id voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Een beheerder kan de functie **CFDI Mexicaanse elektronische factuur (MX)** in- en uitschakelen door te navigeren naar **Organisatiebeheer \> Instellingen \> Parameters voor elektronische documenten**. Selecteer op het tabblad **Functies** de rijen met de functie **CFDI Mexicaanse elektronische factuur (MX)** en maak de juiste selectie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met Elektronische facturering](e-invoicing-get-started.md)
- [Elektronische facturering instellen](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]