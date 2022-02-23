---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Brazilië in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962829"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> De invoegtoepassing Elektronische facturering voor Brazilië ondersteunt momenteel niet alle functies die beschikbaar zijn in de fiscale documentintegratie die in Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management is ingebouwd.

Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Brazilië. U wordt door de configuratiestappen geleid die landafhankelijk zijn in de Regulatory Configuration Services (RCS) en in Finance en Supply Chain Management. Het begeleidt u ook bij het indienen van een NF-e fiscaal document (Elektronisch fiscaal document model 55) via de service, en het legt uit hoe u de verwerkingsresultaten en de status van de fiscale documenten kunt bekijken.

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp uitvoert, moet u de stappen uitvoeren in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-instellingen

Tijdens de RCS-instelling voert u de volgende taken uit:

1. Importeer de functie e-Facturering voor NF-e fiscale documenten.
2. Controleer de bestandsindelingen die nodig zijn om NF-e fiscale documenten voor autorisatie in te dienen.
3. Controleer de bestandsindelingen die nodig zijn om de annulering van een goedgekeurde NF-e aan te vragen.
4. Configureer de gebeurtenis die nodig is om NF-e fiscale documenten voor autorisatie in te dienen.
5. Configureer de gebeurtenis die nodig is om de annulering van een goedgekeurde NF-e aan te vragen.
6. De functie e-Facturering toewijzen aan een omgeving voor de invoegtoepassing Elektronische facturering.
7. Publiceer de functie e-Facturering.

> [!NOTE]
> 'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server van de invoegtoepassing voor elektronische facturering. Met de instelling van de functie e-Facturering wordt onder andere het gebruik van configuratie-indelingen voor elektronische rapportage (ER) gecombineerd om configureerbare export- en importbestanden te maken, en het gebruik van acties en actiestromen om het maken van configureerbare regels mogelijk te maken voor het verzenden van aanvragen, het importeren van reacties en het parseren van de reactie-inhoud.

## <a name="import-the-e-invoicing-feature"></a>De functie e-Facturering importeren

1. Meld u aan bij uw RCS-account
2. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **e-Facturering**.
3. Op de pagina **Functies voor e-Facturering** selecteert u **Importeren** om van de functie e-Facturering een NF-e fiscaal document uit de algemene opslagplaats te importeren.

    ![De knop Importeren](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Selecteer de functie NF-e fiscaal document en selecteer **Importeren**.

    ![De functie NF-e importeren](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Een nieuwe versie van de functie NF-e fiscaal document maken

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Nieuw**.

![Een nieuwe versie van de functie e-Facturering toevoegen](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>De configuratieversie bijwerken

1. Op de pagina **Functies voor e-Facturering** selecteert u op het tabblad **Configuraties** de optie **Toevoegen** of **Verwijderen** om de configuratieversies (configuraties van de ER-bestandsindeling) te beheren.

    ![Configuraties voor de functies van e-Facturering beheren](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Wanneer u een nieuwe versie van de functie NF-e fiscaal document maakt, worden alle configuratieversies (ER-bestandsindelingen) overgenomen van de laatste versie.
    - Om het NF-e fiscaal document voor autorisatie in te dienen, zijn de volgende configuratieversies vereist:

        - Exportindeling voor indienen NF-e
        - NF-e-responsbericht importeren
        - NF-e-foutenlogboek importeren

    - De volgende configuratieversie is vereist om de NF-e-annulering in te dienen:

        - Exportindeling voor annuleren NF-e

2. Selecteer een configuratieversie in de lijst en selecteer **Bewerken** of **Weergeven** om de pagina **Indelingsontwerper** te openen. Hier kunt u de configuratie bewerken of weergeven.

    ![De pagina Indelingsontwerper openen](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Gebruik de pagina **Indelingsontwerper** om de configuratie van bestanden met een ER-indeling te bewerken of weer te geven. Zie [Configuraties voor elektronische documenten maken](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration) voor meer informatie.

    ![Pagina Indelingsontwerper](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>De instellingen voor de functie e-Facturering beheren

- Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** de optie **Toevoegen** of **Verwijderen** om de instellingen van de functie e-Facturering (NF-e-gebeurtenissen) te beheren.

![De instellingen voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Wanneer u een nieuwe versie van de functie NF-e fiscaal document maakt die is afgeleid van een andere functie voor e-facturering worden alle functie-instellingen (NF-e gebeurtenissen) overgenomen van de laatste versie.

Om NF-e fiscale documenten voor autorisatie in te dienen, is de functie-instelling **Indienen** vereist.

Om NF-e annulering in te dienen, is de functie-instelling **Annulering** vereist.

#### <a name="configure-the-submit-feature-setup"></a>De functie-instelling Indienen configureren

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Indienen**.
2. Selecteer **Bewerken**.

    ![Functie e-Facturering bewerken](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren.

    ![Tabblad Acties](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Controleer de acties die nodig zijn om een NF-e voor autorisatie in te dienen.

    | Actie-ID | Naam actie                  | Omschrijving van de actie                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Document transformeren           | Maak het XML-bestand NF-e voor indienen.                          |
    | 2         | Document ondertekenen                | Pas het digitale certificaat toe op het XML-bestand.                    |
    | 3         | Braziliaanse SEFAZ-service aanroepen | Dien het ondertekende XML-bestand voor autorisatie in bij de webservices. |
    | 4         | Reactie verwerken             | Haal de reactie van de webservice op.                                     |
    | 5         | Document transformeren           | Parseer de inhoud van het bestand dat als reactie is ontvangen.     |
    | 6         | Document transformeren           | Maak het XML-bestand om informatie over de status van de indiening op te vragen.    |
    | 7         | Braziliaanse SEFAZ-service aanroepen | Dien het XML-bestand dat de indieningsstatus aanvraagt, in.          |
    | 8         | Reactie verwerken             | Haal de reactie van de webservice op.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>De URL voor SEFAZ-webservices instellen 

1. Ga naar de pagina **Instellingen functieversie** en selecteer op het tabblad **Acties**, op het sneltabblad **Acties** de optie **Braziliaanse SEFAZ-service aanroepen** (actie-id **3**).
2. Voer op het sneltabblad **Parameters** in het veld **URL-adresparameter** de URL van de SEFAZ-webservice voor het indienen van NF-e in.
3. Selecteer op het sneltabblad **Acties** de optie **Braziliaanse SEFAZ-service aanroepen** (actie-id **7**).
4. Voer op het sneltabblad **Parameters** in het veld **URL-adresparameter** de URL van de SEFAZ-webservice voor het indienen van NF-e in.

#### <a name="configure-the-cancellation-feature-setup"></a>De functie-instelling Annulering configureren

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Annulering**.
2. Selecteer **Bewerken**.
3. Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren.
4. Controleer de acties die nodig zijn om de annulering van een goedgekeurde NF-e aan te vragen.

    | Actie-ID | Naam actie                  | Omschrijving van de actie                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Document transformeren           | Maak het XML-bestand NF-e-annulering voor indienen.            |
    | 2         | Document ondertekenen                | Pas het digitale certificaat toe op het XML-bestand.                   |
    | 3         | Braziliaanse SEFAZ-service aanroepen | Dien het ondertekende XML-bestand voor annulering in bij de webservices. |
    | 4         | Reactie verwerken             | Haal de reactie van de webservice op.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>De URL voor SEFAZ-webservices instellen

1. Ga naar de pagina **Instellingen functieversie** en selecteer op het tabblad **Acties**, op het sneltabblad **Acties** de optie **Braziliaanse SEFAZ-service aanroepen** (actie-id **3**).
2. Voer op het sneltabblad **Parameters** in het veld **URL-adresparameter** de URL van de SEFAZ-webservice voor het annuleren van een goedgekeurde NF-e in.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Een omgeving voor e-Facturering beschikbaar maken en een conceptversie toewijzen

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Omgevingen** de optie **Inschakelen**.
2. Selecteer de omgeving in het veld **Omgeving**.
3. Selecteer in het veld **Geldig vanaf** de ingangsdatum van de omgeving.
4. Selecteer **Inschakelen**.

![Een e-Factureringsomgeving inschakelen](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>De status wijzigen in Voltooid

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Concept**.
2. Selecteer **Status wijzigen \> Voltooien**.

### <a name="change-the-status-to-publish"></a>De status wijzigen in Publiceren

1. Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Voltooid**.
2. Selecteer **Status wijzigen \> Publiceren**.

![De functie e-Facturering publiceren](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance of Supply Chain Management

Tijdens de installatie voert u de volgende taken uit:

1. Schakel de federale functie NF-e in voor Brazilië.
2. Importeer het specifieke ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en de indelingen die nodig zijn voor NF-e fiscale documenten.
3. Importeer de ER-configuratie en stel de responstypen in die nodig zijn om de status van het fiscale document bij te werken nadat het indieningsproces is geretourneerd.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Schakel de federale functie NF-e in voor Brazilië

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Schakel op het tabblad **Functies** het selectievakje **Inschakelen** in bij de rij voor functiereferentie **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>De toewijzing voor het ER-gegevensmodel importeren die is vereist voor NF-e fiscale documenten

1. Meld u aan bij Finance.
2. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**. Controleer of deze configuratieaanbieder is ingesteld op **Actief**. Zie [Aanbieders van configuraties maken en deze als actief markeren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) voor informatie over de manier waarop u een aanbieder als deze als **Actief** kunt instellen.
3. Selecteer **Opslagplaatsen**.
4. Selecteer **Algemene resource \> Openen**.
5. Importeer configuraties van **Fiscale-documenttoewijzing**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>ER-configuraties importeren en de responstypen instellen voor fiscale documenten

1. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.
2. Selecteer **Opslagplaatsen**.
3. Selecteer **Algemene resource \> Openen**.
4. Importeer **NF-e foutenlogboek importeren (BR)**, **Importindeling NF-e responsgegevens (BR)** en **NF-e responsbericht importeren (BR)**.
5. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
6. Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen**.
6. Voer in het veld **Tabelnaam** **Koptekst fiscaal document** in.
7. Selecteer in het veld **Documentcontext** de optie **Model klantfactuurcontext: context fiscaal document**.
8. Selecteer **Responstypen**.
9. Selecteer **Nieuw** en selecteer in het veld **Responstype** de optie **Respons**.
10. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
11. Selecteer in het veld **Modeltoewijzing** de optie **Importindeling responsbericht – Modeltoewijzing van responsbericht**.
12. Selecteer **Opslaan**.
13. Selecteer **Nieuw** en voer in het veld **Responstype** de optie **Responsgegevens** in.
14. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
15. Selecteer in het veld **Modeltoewijzing** de optie **Importindeling NF-e-responsgegevens – Responsgegevens importeren**.
16. Selecteer **Opslaan**.

## <a name="electronic-invoice-processing"></a>Verwerking van elektronische facturen

Tijdens de verwerking in Finance voert u de volgende taken uit:

1. Een fiscaal document indienen via de invoegtoepassing Elektronische facturering.
2. De uitvoeringslogboeken van de indiening weergeven en de resultaten van de verwerking beoordelen.
3. De annulering van een fiscaal document indienen via de invoegtoepassing Elektronische facturering.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>NF-e fiscale documenten voor SEFAZ-autorisatie indienen 

Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kunt u het oude proces voor het indienen van NF-e fiscale documenten voor autorisatie (**NF-e-proces exporteren/importeren**) niet meer gebruiken. Het wordt vervangen door een nieuw proces met de naam **Elektronische documenten indienen**.

> [!NOTE]
> Controleer voordat u doorgaat of u een of meer fiscale klantdocumenten model 55 hebt die zijn uitgegeven door de fiscale instelling van de klant. De richting voor deze fiscale documenten moet worden ingesteld op **Uitgaand** en de status moet **Gemaakt** zijn. Zie [Belastingdocument voor klant verstrekken (Brazilië)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document) voor meer informatie.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.
2. Als u een document voor het eerst indient, moet u altijd de optie **Documenten opnieuw indienen** op **Nee** instellen. Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.
3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.
4. Selecteer **Toevoegen** op het tabblad **Bereik**.
5. Selecteer in het veld **Tabel** de optie **Koptekst fiscaal document**.
6. Selecteer in het veld **Afgeleide tabel** de optie **Koptekst fiscaal document**.
6. Selecteer **Nummer** in het veld **Veld**.
7. Voer in het veld **Criteria** het nummer in van het fiscale document dat moet worden ingediend.
8. Selecteer **OK** om het dialoogvenster **Query** te sluiten.
8. Klik op **OK** om de geselecteerde documenten in te dienen.

> [!NOTE]
> Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met de invoegtoepassing voor elektronische facturering te bevestigen. Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.

### <a name="view-all-submission-logs"></a>Alle indieningslogboeken weergeven

Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, is er een nieuwe pagina beschikbaar waarmee u het indieningsproces voor documenten kunt opvolgen. U kunt deze pagina gebruiken om de indieningslogboeken voor alle ingediende documenten weer te geven.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** de optie **Koptekst fiscaal document** om alleen op fiscale documenten te filteren.
3. Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.

![Details van indieningslogboeken weergeven](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Voor NF-e fiscale documenten geeft de kolom **Foutcode** de retourcode weer die is geretourneerd door de SEFAZ-webservices.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Indieningslogboeken weergeven via de pagina fiscaal document

Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kunt u ook de indieningslogboeken weergeven via de pagina fiscaal document.

1. Ga naar **Grootboek \> Query's en rapporten \> Fiscale documenten \> Alle fiscale documenten**.
2. Selecteer een fiscaal document dat eerder is ingediend via de invoegtoepassing voor elektronische facturering.
3. Selecteer in het actievenster op het tabblad **NF-e federaal** de optie **Logboek elektronische documenten**.

![Indieningslogboeken weergeven vanuit de pagina fiscaal document](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Goedgekeurde NF-e fiscale documenten voor SEFAZ-annulering indienen

Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld, kan het oude proces voor het annuleren van NF-e fiscale documenten niet meer worden gebruikt. Deze wordt vervangen door een nieuw annuleringsproces dat is ingesloten op de pagina **Indieningslogboek voor elektronische documenten**.

> [!NOTE]
> Controleer of u de annulering van het fiscale document van de klant voor een goedgekeurd NF-e fiscaal document hebt uitgevoerd. Zie [Belastingdocument voor klant annuleren (Brazilië)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents) voor meer informatie.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer het fiscale document en selecteer **Functies \> Gerelateerde indieningen verzenden**.
3. Voer een omschrijving voor de gerelateerde indiening in en selecteer **OK**.

### <a name="view-cancellation-submission-logs"></a>Indieningslogboeken van annuleringen weergeven

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** de optie **Koptekst fiscaal document** om alleen op fiscale documenten te filteren.
3. Selecteer het fiscale document en selecteer in het actievenster **Query's \> Gerelateerde indiening**.

    Gerelateerde indieningen hebben betrekking tot een hoofdindiening die het eerst is gedaan. De indiening waarmee bijvoorbeeld een specifieke NF-e wordt geautoriseerd, is de hoofdindiening. De indiening waarmee de annulering van dezelfde NF-e in SEFAZ wordt aangevraagd, is een gerelateerde indiening. Het bestaat alleen omdat het de annulering van de taak aanvraagt die via een andere indiening is uitgevoerd.

    De pagina **Gerelateerde indieningen** toont alle gerelateerde indieningen en de bijbehorende status voor een bepaald fiscaal document. In de volgende afbeelding staat de eerste regel voor de indiening waarin om goedkeuring van het fiscale document is gevraagd. De tweede regel staat voor de indiening waarmee dat fiscale document is geannuleerd.

    ![Indieningslogboeken van annuleringen weergeven](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.

    ![Details van indieningslogboeken van annuleringen weergeven](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Privacyverklaring
Voor het inschakelen van de functie BR-00053 (NF-e Federaal) moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-ID voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Een beheerder kan de functie BR-00053 (NF-e Federaal) in- en uitschakelen door te navigeren naar **Organisatiebeheer \> Instellingen \> Parameters voor elektronische documenten**. Selecteer het tabblad **Functies** en selecteer de rij met de functie BR-00053 en maak de gewenste selectie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.


## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)
- [De invoegtoepassing voor elektronische facturering instellen](e-invoicing-setup.md)
