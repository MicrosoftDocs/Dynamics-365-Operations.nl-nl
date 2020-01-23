---
title: Optionele functies voor een preview-omgeving van Commerce configureren
description: In dit onderwerp wordt uitgelegd hoe u optionele functies voor een preview-omgeving van Microsoft Dynamics 365 Commerce configureert.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906111"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a>Optionele functies voor een preview-omgeving van Commerce configureren

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u optionele functies voor een preview-omgeving van Microsoft Dynamics 365 Commerce configureert.

## <a name="prerequisites"></a>Vereisten

Als u de transactionele e-mailfuncties wilt evalueren, moet aan de volgende voorwaarden worden voldaan:

- U hebt een e-mailserver beschikbaar (\[SMTP\]-server), die kan worden gebruikt vanuit het Microsoft Azure-abonnement waarin u de preview-omgeving inricht.
- U hebt het FQDN/IP-adres, het SMTP-poortnummer en de verificatiegegevens van de server beschikbaar.

Als u functies voor beheer van digitale activa wilt evalueren door nieuwe Omnichannel-afbeeldingen op te nemen, moet u de naam van uw CMS-tenant (contentmanagementsysteem) beschikbaar hebben. Instructies voor het vinden van deze naam vindt u verderop in dit onderwerp. >>>(V: waar zijn de instructies?)

## <a name="configure-the-image-back-end"></a>De backend van de afbeelding configureren

### <a name="find-your-media-base-url"></a>Uw basis-URL voor media vinden

> [!NOTE]
> Voordat u deze procedure kunt uitvoeren, moet u de stappen in [Uw site instellen in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce) voltooien.

1. Meld u aan bij het beheerhulpprogramma van de e-Commerce-site met de URL die u hebt genoteerd tijdens de initialisatie van e-Commerce tijdens het inrichten (zie [e-Commerce initialiseren](provisioning-guide.md#initialize-e-commerce)).
1. Open de site **Fabrikam**.
1. Selecteer **Activa** in het linkermenu.
1. Selecteer één afbeeldingsactivum.
1. Zoek in de eigenschappencontrole aan de rechterkant de eigenschap **Openbare URL**. De waarde is een URL. Dit is een voorbeeld:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Vervang de laatste id in de URL (**MA1nQC** in het voorbeeld hierboven) door de volgende tekenreeks: **search?fileName=**. De voorbeeld-URL ziet er zo uit nadat deze wijziging is doorgevoerd:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Deze URL is uw basis-URL voor media. Noteer deze.

### <a name="update-the-media-base-url"></a>De basis-URL voor media bijwerken

1. Meld u aan bij Dynamics 365 Retail.
1. Ga in het menu links naar **Modules \> Detailhandel \> Afzetkanaalinstellingen \> Afzetkanaalprofielen**.
1. Selecteer **Bewerken**.
1. Vervang onder **Profieleigenschappen** de waarde voor **Basis-URL voor mediaserver** door de basis-URL voor media die u eerder hebt gemaakt.
1. Selecteer het andere kanaal in de lijst aan de linkerkant, onder het **standaardkanaal**.
1. Selecteer onder **Profieleigenschappen** de optie **Toevoegen**.
1. Voor de eigenschap die is toegevoegd, selecteert **Basis-URL voor mediaserver** als de eigenschapssleutel. Voer als de waarde van de eigenschap de basis-URL voor de media in die u eerder hebt gemaakt.
1. Selecteer **Opslaan**.

## <a name="configure-the-email-server"></a>De e-mailserver configureren

> [!NOTE]
> De SMTP-server of e-mailservice die u hier invoert, moet toegankelijk zijn vanuit het Azure-abonnement dat u voor de omgeving gebruikt.

1. Meld u aan bij Retail.
1. Ga in het menu links naar **Modules \> Systeembeheer \> Instellingen \> E-mail \> E-mailparameters**.
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

1. Meld u aan bij Retail.
1. Ga in het menu links naar **Modules \> Organisatiebeheer \> Instellingen \> E-mailsjablonen van organisatie**.
1. Selecteer **Lijst weergeven**.
1. Volg deze stappen voor elke sjabloon in de lijst:

    1. Voer in het veld **E-mailadres afzender** het e-mailadres van de afzender in.
    1. Optioneel: voer in het veld **Naam van afzender** de naam in die moet worden gebruikt als de naam van de afzender.

1. Selecteer **Opslaan**.

## <a name="customize-email-templates"></a>E-mailsjablonen aanpassen

Mogelijk wilt u de e-mailsjablonen aanpassen zodat deze verschillende afbeeldingen gebruiken. U kunt ook de koppelingen in de sjablonen bijwerken, zodat deze naar uw preview-omgeving leiden. In deze procedure wordt uitgelegd hoe u de standaardsjablonen kunt downloaden, aanpassen en bijwerken in het systeem.

1. Download via een webbrowser [het zipbestand met standaard e-mailsjablonen voor Microsoft Dynamics 365 Commerce Preview](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) naar uw lokale computer. Dit bestand bevat de volgende HTML-documenten:

    - Sjabloon voor orderbevestiging
    - Sjabloon voor uitgifte van geschenkbon
    - Sjabloon voor nieuwe order
    - Sjabloon voor verpakkingsorder
    - Sjabloon voor orderverzameling

1. Pas de sjablonen aan met een tekst- of HTML-editor. Zie de lijst met [ondersteunde tokens](#supported-tokens-in-the-email-template) verderop in dit onderwerp.
1. Meld u aan bij Retail.
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

| Naam van token | Token  |
|-------------------|-------|
| Ordernummer      | %salesid% |
| Naam van klant   | %customername% |
| Afleveradres  | %deliveryaddress% |
| Factureringsadres   | %customeraddress% |
| Besteldatum        | %shipdate% |
| Bezorgingsmodus     | %modeofdelivery% |
| Korting          | %discount% |
| Btw         | %tax% |
| Ordertotaal       | %total% |

#### <a name="sales-line"></a>Verkoopregel

De volgende tokens worden voor elk product in de order vervangen door waarden.

> [!NOTE]
> Plaats het token **Productlijst - begin** aan het begin van het HTML-blok dat wordt herhaald voor elk product en plaats het token **Productlijst - eind** aan het einde van het blok.

| Naam van token      | Token  |
|------------------------|-------|
| Productlijst - begin   | \<!--%tablebegin.salesline% --\> |
| Productlijst - eind     | \<!--%tableend.salesline%--\> |
| Productnaam           | %lineproductname% |
| Beschrijving            | %lineproductdescription% |
| Hoeveelheid               | %linequantity% |
| Regel met eenheidsprijs        | %lineprice% (controleren) |
| totaal regelartikel        | %linenetamount% |
| regelkorting          | %linediscount% |
| Verzenddatum              | %lineshipdate% |
| Aanschaffingsmethode     | %linedeliverymode% |
| afleveradres       | %linedeliveryaddress% |
| Verkoopeenheid van regel | %lineunit% |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Commerce preview-omgeving](cpe-overview.md)

[Een preview-omgeving van Commerce inrichten](provisioning-guide.md)

[Een preview-omgeving van Commerce configureren](cpe-post-provisioning.md)

[Veelgestelde vragen over de preview-omgeving van Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure-portal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce-website](https://aka.ms/Dynamics365CommerceWebsite)

[Help-bronnen voor Dynamics 365 Retail](../retail/index.md)
