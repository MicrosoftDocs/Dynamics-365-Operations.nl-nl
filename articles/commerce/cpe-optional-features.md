---
title: Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren
description: In dit artikel wordt uitgelegd hoe u optionele functies voor een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39d4784e21c4fb42ca218d507616d49eff309ee1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861909"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren

[!include [banner](includes/banner.md)]

In dit artikel wordt uitgelegd hoe u optionele functies voor een evaluatieomgeving van Microsoft Dynamics 365 Commerce configureert.

## <a name="prerequisites"></a>Vereisten

Als u de transactionele e-mailfuncties wilt evalueren, moet aan de volgende voorwaarden worden voldaan:

- U hebt een e-mailserver beschikbaar (\[SMTP\]-server), die kan worden gebruikt vanuit het Microsoft Azure-abonnement waarin u de evaluatieomgeving inricht.
- U hebt het FQDN/IP-adres, het SMTP-poortnummer en de verificatiegegevens van de server beschikbaar.

## <a name="configure-the-image-back-end"></a>De backend van de afbeelding configureren

### <a name="find-your-media-base-url"></a>Uw basis-URL voor media vinden

> [!NOTE]
> Voordat u deze procedure kunt uitvoeren, moet u de stappen in [Uw site instellen in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce) voltooien.

1. Meld u aan bij de Commerce Site Builder met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).
1. Open de site **Fabrikam**.
1. Selecteer **Mediabibliotheek** in het linkermenu.
1. Selecteer één afbeeldingsactivum.
1. Zoek in de eigenschappencontrole aan de rechterkant de eigenschap **Openbare URL**. De waarde is een URL. Dit is een voorbeeld:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Vervang de laatste id in de URL (**MA1nQC** in het voorbeeld hierboven) door de volgende tekenreeks: **search?fileName=**. De voorbeeld-URL ziet er zo uit nadat deze wijziging is doorgevoerd:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Deze URL is uw basis-URL voor media. Noteer deze.

### <a name="update-the-media-base-url"></a>De basis-URL voor media bijwerken

1. Meld u aan bij Commerce Headquarters.
1. Ga in het menu links naar **Modules \> Detailhandel en commerce \> Afzetkanaalinstellingen \> Afzetkanaalprofielen**.
1. Selecteer **Bewerken**.
1. Vervang onder **Profieleigenschappen** de waarde voor **Basis-URL voor mediaserver** door de basis-URL voor media die u eerder hebt gemaakt.
1. Selecteer het kanaal met de naam **scXXXXXXXXX**.
1. Selecteer onder **Profieleigenschappen** de optie **Toevoegen**.
1. Voor de eigenschap die is toegevoegd, selecteert **Basis-URL voor mediaserver** als de eigenschapssleutel. Voer als de waarde van de eigenschap de basis-URL voor de media in die u eerder hebt gemaakt.
1. Selecteer **Opslaan**.

## <a name="configure-and-test-the-email-server"></a>De e-mailserver configureren en testen

> [!NOTE]
> De SMTP-server of e-mailservice die u hier invoert, moet toegankelijk zijn vanuit het Azure-abonnement dat u voor de omgeving gebruikt.

1. Meld u aan bij Commerce Headquarters.
1. Ga via het menu links naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailparameters**.
1. Voer op het tabblad **SMTP-instellingen** in het veld **Naam SMTP-relaisserver** de FQDN-naam of het IP-adres in van de SMTP-server of e-mailservice.
1. Voer in het veld **SMTP-poortnummer** het poortnummer in. (Als u SSL \[Secure Sockets Layer \] gebruikt, is het standaardpoortnummer **25**.)
1. Als verificatie vereist is, voert u waarden in de velden **Gebruikersnaam** en **Wachtwoord** in.
1. Selecteer **Opslaan**.
1. Selecteer **Vernieuwen**.
1. Selecteer op het tabblad **Testbericht** in het veld **E-mailprovider** de optie **SMTP**.
1. Voer in het veld **Verzenden naar** het e-mailadres in waar u het testbericht wilt afleveren.
1. Selecteer **Testbericht verzenden**.

## <a name="configure-email-templates"></a>E-mailsjablonen configureren

Voor elke transactionele gebeurtenis waarvoor u e-mailberichten wilt verzenden, moet u de e-mailsjabloon bijwerken met een geldig e-mailadres van de afzender.

1. Meld u aan bij Commerce Headquarters.
1. Ga via het menu links naar **Modules \> Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie**.
1. Selecteer **Lijst weergeven**.
1. Volg deze stappen voor elke sjabloon in de lijst:

    1. Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.
    1. Optioneel: voer in het veld **Naam van afzender** de naam in die moet worden gebruikt als de naam van de afzender.

1. Selecteer **Opslaan**.

## <a name="customize-email-templates"></a>E-mailsjablonen aanpassen

Mogelijk wilt u de e-mailsjablonen aanpassen zodat deze verschillende afbeeldingen gebruiken. U kunt ook de koppelingen in de sjablonen bijwerken, zodat deze naar uw evaluatieomgeving leiden. In deze procedure wordt uitgelegd hoe u de standaardsjablonen kunt downloaden, aanpassen en bijwerken in het systeem.

1. Download via een webbrowser het [zipbestand met standaard e-mailsjablonen voor Microsoft Dynamics 365 Commerce-evaluatie](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) naar uw lokale computer. Dit bestand bevat de volgende HTML-documenten:

    - Sjabloon voor orderbevestiging
    - Sjabloon voor uitgifte van geschenkbon
    - Sjabloon voor nieuwe order
    - Sjabloon voor verpakkingsorder
    - Sjabloon voor orderverzameling

1. Pas de sjablonen aan met een tekst- of HTML-editor. Zie de lijst met [ondersteunde tokens](#supported-tokens-in-the-email-template) verderop in dit artikel.
1. Meld u aan bij Commerce.
1. Ga in het menu links naar **Modules \> Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.
1. Vouw de lijst links uit om alle sjablonen te bekijken.
1. Voer de volgende stappen uit voor elke sjabloon die u wilt aanpassen:

    1. Selecteer de sjabloon in de lijst.
    1. Selecteer onder **Inhoud van e-mailbericht** de toepasselijke taalversie in de lijst. De standaardtaal is **en-us**.
    1. Selecteer **Bewerken** onder **Inhoud van e-mailbericht**. Het deelvenster **E-mailsjabloon uploaden** wordt weergegeven.
    1. Selecteer **Bladeren** en zoek het HTML-bestand met de aangepaste inhoud.
    1. Selecteer **Uploaden**. De sjabloon wordt geüpload naar het systeem en er wordt een voorbeeld weergegeven.
    1. Selecteer **OK**.
    1. Optioneel: pas de eigenschap **Onderwerp** van de sjabloon aan.
    1. Selecteer **Opslaan**.

### <a name="supported-tokens-in-the-email-template"></a>Ondersteunde tokens in de e-mailsjabloon

Als de e-mail wordt weergegeven, worden deze tokens vervangen door de werkelijke waarden die van toepassing zijn op de klant en de klantorder.

#### <a name="sales-order"></a>Verkooporder

De volgende tokens gelden voor de algehele verkooporder.

| Naam van token | Token |
|-------------------|-------|
| Ordernummer      | %salesid% |
| Naam van klant   | %customername% |
| Afleveradres  | %deliveryaddress% |
| Factuuradres   | %customeraddress% |
| Besteldatum        | %shipdate% |
| Bezorgingsmodus     | %modeofdelivery% |
| Korting          | %discount% |
| Btw         | %tax% |
| Ordertotaal       | %total% |

#### <a name="sales-line"></a>Verkoopregel 

De volgende tokens worden voor elk product in de order vervangen door waarden.

> [!NOTE]
> Plaats het token **Productlijst - begin** aan het begin van het HTML-blok dat wordt herhaald voor elk product en plaats het token **Productlijst - eind** aan het einde van het blok.

| Naam van token      | Token |
|------------------------|-------|
| Productlijst - begin   | \<!--%tablebegin.salesline% --\> |
| Productlijst - eind     | \<!--%tableend.salesline%--\> |
| Productnaam           | %lineproductname% |
| Beschrijving            | %lineproductdescription% |
| Hoeveelheid               | %linequantity% |
| Regel met eenheidsprijs        | %lineprice% (verifiëren) |
| totaal regelartikel        | %linenetamount% |
| regelkorting          | %linediscount% |
| Verzenddatum              | %lineshipdate% |
| Aanschaffingsmethode     | %linedeliverymode% |
| afleveradres       | %linedeliveryaddress% |
| Verkoopeenheid van regel | %lineunit% |

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce](cpe-overview.md)

[Een evaluatieomgeving voor Dynamics 365 Commerce inrichten](provisioning-guide.md)

[Een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-post-provisioning.md)

[BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving](cpe-bopis.md)

[Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]