---
title: Aan de slag met de invoegtoepassing voor elektronische facturering
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 61933bb846383932d7dd73e9c4d3c2db7a515a98
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835934"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Aan de slag met de invoegtoepassing voor elektronische facturering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering. Eerst wordt u door de configuratiestappen geleid in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Services (RCS) en Dynamics 365 Finance. Vervolgens wordt het proces beschreven voor het indienen van documenten via de service met Dynamics 365 Finance of Dynamics 365 Supply Chain Management. Verder leert u hoe u de indieningslogboeken interpreteert.

## <a name="availability"></a>Beschikbaarheid

De invoegtoepassing Elektronische facturering is in eerste instantie beschikbaar voor verschillende landen. De invoegtoepassing ondersteunt het maken van elektronische facturen en het indienen van de volgende zakelijke documenten:

| Land/regio  | Bedrijfsdocument                          |
|-----------------|--------------------------------------------|
| Oostenrijk         | Verkoop- en projectfacturen                 |
| België         | Verkoop- en projectfacturen                 |
| Brazilië          | Elektronisch belastingdocument model 55 (NF-e) |
| Denemarken         | Verkoop- en projectfacturen                 |
| Estland         | Verkoop- en projectfacturen                 |
| Finland         | Verkoop- en projectfacturen                 |
| Frankrijk          | Verkoop- en projectfacturen                 |
| Duitsland         | Verkoop- en projectfacturen                 |
| Italië           | Verkoop- en projectfacturen                 |
| Mexico          | CFDI-factuur                               |
| Nederland     | Verkoop- en projectfacturen                 |
| Noorwegen          | Verkoop- en projectfacturen                 |
| Spanje           | Verkoop- en projectfacturen                 |
| Europa          | PEPPOL Verkoop- en projectfacturen          |
    
## <a name="licensing"></a>Licenties

U kunt de invoegtoepassing Elektronische facturering gebruiken met uw huidige licentie. Er zijn geen extra licenties vereist om de service te gebruiken.

## <a name="prerequisites"></a>Vereisten

Voordat u de stappen in dit onderwerp voltooit, moet u aan de volgende vereisten voldoen:

- Toegang tot uw LCS-account.
- Een LCS-implementatieproject dat Finance of Supply Chain Management versie 10.0.12 of hoger bevat.
- Toegang tot uw RCS-account.
- Schakel de globalisatiefunctie voor uw RCS-account in via de module **Functiebeheer**. Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie
- Maak een Key Vault-resource en een opslagaccount in Azure. Zie [Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.

## <a name="overview"></a>Overzicht

In de volgende afbeelding ziet u de vijf belangrijkste stappen die u in dit onderwerp zult voltooien.

![Overzicht van de vijf stappen in dit onderwerp](media/e-invoicing-services-get-started-overview-5-steps.png)

1. **Azure-resources instellen:** configureer Azure-opslag en het uploaden van digitale certificaten in Azure Key Vault.
2. **LCS-instellingen:** installeer de invoegtoepassing voor microservices.
3. **RCS-instellingen:** de functies voor omgeving, gebruikerstoegang en e-Facturering instellen.
4. **Client instellen:** stel de verbinding in tussen de client en de invoegtoepassing Elektronisch factureren in en schakel de oude functies voor het indienen en ontvangen van respons voor elektronische documenten uit.
5. **Facturen indienen:** dien elektronische documenten in via de invoegtoepassing voor elektronische facturering en ontvang respons.

> [!NOTE]
> Enkele configuratiestappen in dit onderwerp zijn algemeen en niet land-/regiospecifiek. De stappen en instellingsprocedures die specifiek zijn voor landen/regio's worden beschreven in land-/regiospecifieke onderwerpen.

## <a name="lcs-setup"></a>LCS-instellingen

1. Meld u aan bij uw LCS-account.
2. Selecteer het LCS-implementatieproject. Voordat u het project kunt selecteren, moet het actief zijn.
3. Selecteer op het sneltabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
4. Selecteer **Zakelijk document indienen**.
5. Voer in het dialoogvenster **Invoegtoepassing instellen** in het veld **AAD-toepassings-id** het volgende in: **091c98b0-a1c9-4b02-b62c-7753395ccabe**. Dit is een vaste waarde.
6. Voer in het veld **AAD-tenant-id** de id van uw Azure-abonnementsaccount in.

    ![Het dialoogvenster Invoegtoepassing instellen in LCS](media/e-invoicing-services-get-started-lcs-addin-setup.png)

7. Schakel het selectievakje in om de voorwaarden te accepteren.
8. Selecteer **Installeren**.

## <a name="rcs-setup"></a>RCS-instellingen

Tijdens de RCS-instelling voert u de volgende taken uit:

1. Stel de sleutelkluis in RCS in.
2. De RCS-integratie met de server van de invoegtoepassing voor elektronisch factureren instellen.
3. Maak een omgeving voor de invoegtoepassing voor elektronische facturering voor uw organisatie.

### <a name="set-up-the-key-vault-in-rcs"></a>Stel de sleutelkluis in RCS in

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Omgevingen** de tegel **e-Facturering**.
3. Selecteer **Serviceomgevingen**.

    ![Serviceomgevingen selecteren](media/e-invoicing-services-get-started-select-service-environments.png)

> [!NOTE]
> Met de optie **Verbonden toepassingen** wordt toegang verleend voor de automatische configuratie van de invoegtoepassing voor elektronische facturering in Finance of Supply Management via de RCS. Deze functie is echter nog in ontwikkeling.

4. Selecteer **Key Vault-parameters** in het actievenster.

    ![Key Vault-parameter selecteren](media/e-invoicing-services-get-started-select-key-vault-parameters.png)

5. Selecteer **Nieuw** in het actievenster om een sleutelkluis toe te voegen.
6. Voer in het veld **Key Vault-URI** de waarde van het kenmerk **DNS-naam** van de sleutelkluis-resource in die u in Azure hebt geconfigureerd. Zie [Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor informatie over waar u de waarde voor **DNS-naam** kunt vinden.

    ![Het veld Key Vault-URI](media/e-invoicing-services-get-started-enter-key-vault-uri.png)

7. Selecteer op het sneltabblad **Certificaten** de optie **Toevoegen** en voer de namen van de digitale certificaten en de sleutelkluisgeheimen in. Beide waardensets worden geconfigureerd in de sleutelkluis-resource in Azure.

    ![Certificaten toevoegen](media/e-invoicing-services-get-started-add-digital-certificates.png)

8. Als uw land-/regiospecifieke factuur een keten certificaten vereist om een digitale handtekening toe te passen, selecteert u **Keten van certificaten** in het actievenster en voert u de reeks certificaten of sleutelkluisgeheimen in waaruit de keten bestaat.

### <a name="set-up-the-rcs-integration-with-the-electronic-invoicing-add-on-server"></a>De RCS-integratie met de server van de invoegtoepassing voor elektronisch factureren instellen

1. Selecteer in het werkgebied **Globalisatiefuncties** in de sectie **Verwante koppelingen** de koppeling **Parameters van elektronische rapportage**.
2. Selecteer **Klik hier om verbinding te maken met Lifecycle Services**. Als u geen verbinding wilt maken met LCS, selecteert u **Annuleren**.
3. Op het tabblad **Invoegtoepassing Elektronische facturering** in het veld **Service-eindpunt-URI** voert u `https://businessdocumentsubmission.us.operations365.dynamics.com/` in.
4. Controleer of in het veld **Toepassings-id** de id **0cdb527f-a8d1-4bf8-9436-b352c68682b2** wordt weergegeven. Dit is een vaste waarde.
5. Voer in het veld **LCS-omgevings-id** de id van uw LCS-abonnementsaccount in.

![Parameters voor invoegtoepassing Elektronische facturering invoeren](media/e-invoicing-services-get-started-enter-e-invoicing-parameters.png)

### <a name="add-an-electronic-invoicing-add-on-environment"></a>Een omgeving van de invoegtoepassing voor elektronische facturering toevoegen

U kunt verschillende omgevingen maken voor de invoegtoepassing Elektronische facturering, zoals dev-, test- of productieomgevingen.

1. Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Omgevingen** de tegel **e-Facturering**.
2. Selecteer **Nieuw** om een omgeving te maken.
3. Voer in het veld **SAS-tokenaccount voor opslag** de naam van het sleutelkluisgeheim in dat u in de sleutelkluis in RCS hebt geconfigureerd.

    ![Het veld SAS-tokenaccount voor opslag](media/e-invoicing-services-get-started-enter-sas-token-secret.png)

4. Selecteer op het sneltabblad **Gebruikers** de optie **Nieuw** om toegang te verlenen aan gebruikers voor deze omgeving.

    ![Servicegebruikers toevoegen](media/e-invoicing-services-get-started-enter-service-users.png)

5. Selecteer **Publiceren** in het actievenster om de omgeving naar de server voor elektronische facturering te publiceren.

    ![De knop Publiceren](media/e-invoicing-services-get-started-publish-service-environment.png)

### <a name="e-invoicing-feature-setup"></a>Functie e-Facturering instellen

'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server van de invoegtoepassing voor elektronische facturering. Met de instelling van de functie e-Facturering wordt onder andere het gebruik van configuratie-indelingen voor elektronische rapportage (ER) gecombineerd om configureerbare export- en importbestanden te maken, en het gebruik van acties en actiestromen om het maken van configureerbare regels mogelijk te maken voor het verzenden van aanvragen, het importeren van reacties en het parseren van de reactie-inhoud.

Vanwege variaties in factuurindelingen en actiestromen zijn de instellingen van de functie e-Facturering afhankelijk van land/regio.

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance of Supply Chain Management 

Tijdens deze instelling voert u de volgende taken uit:

1. Flighted-functie openen
2. Schakel de functie voor de integratie van de invoegtoepassing Elektronische facturering in om integratie met Financiën mogelijk te maken.
3. De URL van het eindpunt van de invoegtoepassing voor elektronisch factureren instellen.
4. Importeer de ER-configuraties die zijn gerelateerd aan de land-/regiospecifieke functie e-Facturering.
5. Schakel de betreffende land-/regiospecifieke functie e-Facturering in.
6. Importeer de ER-configuraties en stel de responstypen in die nodig zijn om uw land-/regiospecifieke factuurdocument bij te werken als gevolg van het indieningsproces.

### <a name="open-flighted-feature"></a>Flighted-functie openen
De functie voor integratie van elektronisch factureren is ingeschakeld via flighting. Flighting is een concept waarmee een functie standaard kan worden in- of uitgeschakeld. Met de volgende stappen kan een flight in een niet-productieomgeving worden ingeschakeld. 

1. Voer de volgende SQL-opdracht uit:

    INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('ElectronicInvoicingServiceIntegrationFeature', 1)
    
2. Nadat u de bovenstaande wijziging hebt aangebracht, voert u een IISReset uit op alle AOS'en

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>De integratie van de invoegtoepassing voor elektronisch factureren inschakelen

1. Meld u aan bij Finance of Supply Chain Management.
2. Zoek in de werkruimte **Functiebeheer** naar de nieuwe functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren**. Als de functie nog steeds niet wordt weergegeven op de pagina Functiebeheer, voert u **Controleren op updates** uit
3. Selecteer de functie en selecteer **Nu inschakelen**.

### <a name="set-up-the-service-endpoint-url"></a>De URL van het service-eindpunt instellen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Op het tabblad **Indieningsservice** in het veld **Service-eindpunt-URL** voert u `https://businessdocumentsubmission.us.operations365.dynamics.com/` in.
3. Voer in het veld **Omgeving** de naam in van de omgeving voor de invoegtoepassing voor elektronische facturering die u hebt gemaakt tijdens het instellen van de RCS.

![Serviceparameters invoeren](media/e-invoicing-services-get-started-enter-service-endpoint.png)

### <a name="import-the-er-configurations"></a>De ER-configuraties importeren

Als u wilt dat bedrijfsgegevens kunnen worden verzameld en verzonden naar de invoegtoepassing voor elektronische facturering, moet u het ER-gegevensmodel en de ER-gegevensmodelconfiguratie importeren die betrekking hebben op de land-/regiospecifieke functie voor e-facturering die u wilt gebruiken.

1. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**. Controleer of deze configuratieaanbieder is ingesteld op **Actief**. Zie [Aanbieders van configuraties maken en deze als actief markeren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) voor informatie over de manier waarop u een aanbieder als deze als **Actief** kunt instellen.
3. Selecteer **Opslagplaatsen**.
4. Selecteer **Algemene resource** en daarna **Openen**.
5. Selecteer in het dialoogvenster **Verbinding maken met Lifecycle Services** de optie **Klik hier om verbinding te maken met Lifecycle Services**.
6. Afhankelijk van het land of de regio waar u de functie voor e-facturering wilt gebruiken, moet u het toepasselijke gegevensmodel, de gegevensmodeltoewijzing en indelingen importeren. Zie het land-/regiospecifieke onderwerp "Aan de slag met de invoegtoepassing voor elektronische facturering" voor informatie over de ER-configuraties die u moet importeren.
7. Importeer **Contextmodel klantfactuur**. Dit model bevat aanvullende parameters die onder andere de omgeving in Finance beschrijven die wordt gebruikt voor de invoegtoepassing elektronische facturering tijdens het indienen van zakelijke gegevens.

### <a name="turn-on-countryregion-specific-e-invoicing-features"></a><a name="region-specific"></a>De land-/regiospecifieke functies voor e-Facturering inschakelen

Als u land-/regiospecifieke functies voor e-facturering wilt inschakelen, zodat deze werken met de invoegtoepassing Elektronische facturering, moet u de functie inschakelen in elke rechtspersoon waar u deze wilt gebruiken. De oude elektronische factureringsintegratie kan hierna niet meer worden gebruikt en de integratie met de nieuwe invoegtoepassing voor elektronische facturering is ingeschakeld.

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Schakel op het tabblad **Functies** in de rij voor de functie die is gerelateerd aan de land-/regiospecifieke functie voor e-facturering het selectievakje in de kolom **Ingeschakeld** in. Zie het land-/regiospecifieke onderwerp "Aan de slag met de invoegtoepassing voor elektronische facturering" voor informatie over welke functie u moet inschakelen.

![De functie e-Facturering inschakelen](media/e-invoicing-services-get-started-enable-invoicing-feature.png)

> [!NOTE]
> Als u meerdere rechtspersonen hebt geconfigureerd voor verschillende landen of regio's, kunt u de land-/regiospecifieke functie voor e-facturering voor elke rechtspersoon inschakelen.

### <a name="import-er-configurations-and-set-up-the-response-types-to-update-your-countryregion-specific-invoice-document"></a>Importeer ER-configuraties en stel de responstypen in om uw land-/regiospecifieke factuur bij te werken

Als het ingediende factuurdocument moet worden bijgewerkt na de respons van de autorisatiediensten van de overheid, moet u een speciaal ER-datamodel en -configuraties importeren om de status van het factuurdocument of een ander aanvullend veld te kunnen bijwerken.

1. Selecteer in de werkruimte **Elektronische rapportage** in de sectie **Configuratieaanbieders** de tegel **Microsoft**.
2. Selecteer **Opslagplaatsen**.
3. Selecteer **Algemene resource** en daarna **Openen**.
4. Importeer **Model responsbericht**, **Importindeling responsbericht**, **Model responsbericht dat naar bestemming toewijst** en **Importindeling bestandsinhoud**.
5. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
6. Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen** om de naam van de tabel in te voeren die is gerelateerd aan uw land-/regiospecifieke factuurdocument. Zie het land-/regiospecifieke onderwerp "Aan de slag met de invoegtoepassing voor elektronische facturering" voor informatie over welke tabelnamen u moet selecteren.
7. Selecteer **Responstypen** om de responstypen te configureren. Zie het land-/regiospecifieke onderwerp "Aan de slag met de invoegtoepassing voor elektronische facturering" voor informatie over welke tabelnamen u moet selecteren.

![Responstypen instellen](media/e-invoicing-services-get-started-set-up-response-types.png)

## <a name="e-invoicing-feature-names-by-country"></a>De namen voor de functie e-Facturering per land 
In de volgende tabel worden de andere functies voor e-facturering beschreven die u kunt downloaden van de algemene opslagplaats voor elektronische rapportage om elektronische facturen te genereren.
In RCS kunt u de e-factureringsfuncties in deze tabel, de ER-configuraties en de beschikbare instellingen voor de e-factureringsfuncties downloaden.
In Finance kunt u de verwante functieverwijzingen op de pagina **Parameters van elektronische documenten** inschakelen om elektronische facturen voor deze landen uit te geven. Zie de sectie [De land-/regiospecifieke functies voor e-Facturering inschakelen](#region-specific) eerder in dit onderwerp voor meer informatie.

| Functienaam                      | Beschrijving                                 | ER-configuraties                                                                                                  | Instellingen                                                                                                                                                         | Land/regio  | Functieverwijzing      |
|-----------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|------------------------|
| Elektronische facturen Oostenrijk (AT) | Verkoop- en projectfacturen voor Oostenrijk      | - OIOUBL Verkoopfactuur <br>- OIOUBL Projectfactuur <br>- OIOUBL Verkoopcreditnota <br>- OIOUBL Projectcreditnota | - Verkoopfactuur genereren (AT) <br>- Projectfactuur genereren (AT) <br>- Verkoopcreditnota genereren (AT) <br>- Projectcreditnota genereren (AT)         | Oostenrijk         | EUR-00023              |
| Elektronische factuur België (BE)   | Verkoop- en projectfacturen voor België      | - UBL Verkoopfactuur BE <br>- UBL Projectfactuur BE <br>- UBL Projectcreditnota BE <br>- UBL Verkoopcreditnota BE | - Verkoopfactuur genereren (BE)<br>- Projectfactuur genereren (BE) <br>- Verkoopcreditnota genereren (BE) <br>- Projectcreditnota genereren (BE)         | België         | EUR-00023              |
| Elektronische factuur Denemarken (DK)    | Verkoop- en projectfacturen voor Denemarken      | - OIOUBL Verkoopfactuur <br>- OIOUBL Projectfactuur <br>- OIOUBL Verkoopcreditnota <br>- OIOUBL Projectcreditnota | - Verkoopfactuur genereren (DK) <br>- Projectfactuur genereren (DK) <br>- Verkoopcreditnota genereren (DK)<br>- Projectcreditnota genereren (DK)         | Denemarken         | EUR-00023<br> DK-00001 |
| Elektronische factuur Nederland (NL)     | Verkoop- en projectfacturen voor Nederland  | - UBL Verkoopfactuur NL <br>- UBL Projectfactuur NL <br>- UBL Verkoopcreditnota NL <br>- UBL Projectcreditnota NL | - Verkoopfactuur genereren (NL) <br> - Projectfactuur genereren (NL) <br> - Verkoopcreditnota genereren (NL) <br>- Projectcreditnota genereren (NL)          | Nederland | EUR-00023              |
| Elektronische factuur Estland (EE)  | Verkoop- en projectfacturen voor Estland      | - Verkoopfactuur (EE) <br> - Projectfactuur (EE)                                                                     | - Verkoopfactuur genereren (EE) <br>- Projectfactuur genereren (EE)                                                                                           | Estland         | EUR-00023              |
| Elektronische factuur Finland (FI)   | Verkoop- en projectfacturen voor Finland      | - Verkoopfactuur (FI) <br>- Projectfactuur genereren (FI)                                                          | - Verkoopfactuur genereren (FI) <br>- Projectfactuur genereren (FI)                                                                                           | Finland         | EUR-00023              |
| Elektronische factuur Frankrijk (FR)    | Verkoop- en projectfacturen voor Frankrijk    | - UBL Verkoopfactuur FR <br> - UBL Projectfactuur FR <br> - UBL Verkoopcreditnota FR <br>- UBL Projectcreditnota FR | - Verkoopfactuur genereren (FR) <br> - Projectfactuur genereren (FR) <br>- Verkoopcreditnota genereren (FR) <br>- Projectcreditnota genereren (FR)         | Frankrijk          | EUR-00023              |
| Elektronische factuur Duitsland (DE)    | Verkoop- en projectfacturen voor Duitsland      |- Verkoopfactuur (DE) <br> - Projectfactuur <DE>                                                                     | - Verkoopfactuur genereren (DE) <br>- Projectfactuur genereren (DE)                                                                                           | Duitsland         | EUR-00023              |
| Elektronische factuur Noorwegen (NO) | Verkoop- en projectfacturen voor Noorwegen       | - OIOUBL Verkoopfactuur <br>- OIOUBL Projectfactuur <br>- OIOUBL Verkoopcreditnota <br>- OIOUBL Projectcreditnota | - Verkoopfactuur genereren (NO) <br>- Projectfactuur genereren (NO) <br>- Verkoopcreditnota genereren (NO) <br>- Projectcreditnota genereren (NO)          | Noorwegen          | EUR-00023<br> NO-00010 |
| Elektronische factuur Spanje (ES)   | Verkoop- en projectfacturen voor Spanje        | - Verkoopfactuur (ES) <br>- Projectfactuur (ES)                                                                     | - Verkoopfactuur genereren (ES) <br>- Projectfactuur genereren (ES)                                                                                           | Spanje           | EUR-00023 <br>ES-00025 |
| Elektronische factuur Italië (IT)   | Verkoop- en projectfacturen voor Italië        | - (Preview) Verkoopfactuur (IT) <br> - Projectfactuur (IT)                                                           | - Verkoopfactuur <br> - Projectfactuur                                                                                                                           | Italië           | EUR-00023 <br>IT-00036 |
| PEPPOL Elektronische factuur         | PEPPOL Verkoop- en projectfacturen genereren | - PEPPOL Verkoopfactuur <br>- PEPPOL Projectfactuur <br>- PEPPOL Verkoopcreditnota <br> - PEPPOL Projectcreditnota | - PEPPOL Verkoopfactuur genereren <br>- PEPPOL Projectfactuur genereren <br>- PEPPOL Verkoopcreditnota genereren <br>- PEPPOL Projectcreditnota genereren |                 | EUR-00023              |


## <a name="electronic-invoice-processing-in-finance-and-supply-chain-management"></a>Verwerking van elektronische facturen in Finance en Supply Chain Management

Tijdens de verwerking voert u de volgende taken uit:

1. Een bedrijfsdocument (factuur) indienen via de invoegtoepassing Elektronische facturering.
2. De uitvoeringslogboeken voor het indienen weergeven.

### <a name="submit-business-documents"></a>Bedrijfsdocumenten indienen

Tijdens het normale indieningsproces is de communicatie tussen de client en de invoegtoepassing Elektronische facturering in twee richtingen. Het doel is twee hoofdtaken uit te voeren tijdens het indienen van elektronische documenten:

1. Alle elektronische documenten verzenden die moeten worden ingediend vanuit Finance en die de juiste status voor indienen hebben en die voldoen aan de selectiecriteria.
2. Importeer in Finance de respons die de invoegtoepassing Elektronische facturering retourneert voor eerder ingediende elektronische documenten. Na het importeren worden de reacties geparseerd en wordt de status van de bedrijfsdocumenten dienovereenkomstig bijgewerkt.

U kunt bedrijfsdocumenten handmatig of op basis van uw planningsvereisten indienen.

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.
2. Als u een document voor het eerst indient, moet u altijd de optie **Documenten opnieuw indienen** op **Nee** instellen. Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.
3. Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.

![Het dialoogvenster Elektronische documenten indienen](media/e-invoicing-services-get-started-submission-form.png)

### <a name="filter-query"></a>Filterquery

1. Voer in dialoogvenster **Query** op het tabblad **Bereik** filtercriteria in aan de hand van de velden **Tabel**, **Afgeleide tabel**, **Veld** en **Criteria**.
2. Selecteer **Toevoegen** om zo veel criteria toe te voegen als u nodig hebt om de bedrijfsdocumenten te selecteren.

    ![Filtercriteria voor indienen instellen](media/e-invoicing-services-get-started-set-up-submission-filter-criteria.png)

3. Selecteer **OK** om het dialoogvenster **Query** te sluiten.
4. Klik op **OK** om de geselecteerde bedrijfsdocumenten in te dienen bij de invoegtoepassing Elektronische facturering.

    > [!NOTE]
    > Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met de invoegtoepassing voor elektronische facturering te bevestigen. Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.
    >
    > ![Berichtvenster Verbinding maken met de service voor het indienen van elektronische documenten](media/e-invoicing-services-get-started-dialog-form-connect-e-Invoicing-services.png)
    >
    > Als de verbinding is gelukt, ontvangt u een bevestigingsbericht.
    >
    > ![Bevestiging van de verbinding met de invoegtoepassing Elektronische facturering](media/e-invoicing-services-get-started-confirmation-connection-e-invoicing-services.png)

5. Sluit het dialoogvenster.

> [!NOTE]
> Na elke indiening wordt in het actiecentrum het aantal ingediende documenten weergegeven.
>
> ![Actiecentrumberichten](media/e-invoicing-services-get-started-view-action-center-messages.png)

### <a name="submission-by-batch"></a>Indienen per batch

In plaats van handmatig documenten in te dienen, kunt u het indieningsproces automatiseren en op de achtergrond uitvoeren, op basis van een geconfigureerde frequentie van batchuitvoering.

1. Stel in het dialoogvenster **Elektronische documenten indienen** op het sneltabblad **Op de achtergrond uitvoeren** de optie **Batchverwerking** in op **Ja**.
2. Configureer op het tabblad **Terugkeer** de frequentie voor de batchverwerking.

![Indienen per batch instellen](media/e-invoicing-services-get-started-set-up-submission-batch.png)

### <a name="view-all-submission-logs"></a>Alle indieningslogboeken weergeven

1. Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.
2. Selecteer in het veld **Documenttype** het documenttype waarop u wilt filteren.

    ![Het documenttype selecteren waarvoor u de indieningslogboeken wilt weergeven](media/e-invoicing-services-get-started-select-document-type-for-viewing-submission-log.png)

    > [!IMPORTANT]
    > De waarde die wordt weergegeven in de kolom **Indieningsstatus** staat voor de status die is gerelateerd aan de voltooiing van het indieningsproces zelf. Hiermee wordt aangegeven of de volgorde van acties die in RCS is geconfigureerd, tot aan het einde is uitgevoerd, ongeacht of het elektronische document is goedgekeurd of afgewezen. De waarde die wordt weergegeven in de kolom **Indieningsstatus** staat niet voor de status van het ingediende document. U kunt de status van het ingediende document (dat wil zeggen, of het document is goedgekeurd of afgewezen) weergeven op het sneltabblad **Logboek verwerkingsacties** in de details van het indieningslogboek, zoals hierna wordt beschreven.

3. Selecteer **Query's \> Details van indiening** in het actievenster.
4. Geef de details van indieningslogboeken weer.

    ![Details van indieningslogboeken](media/e-invoicing-services-get-started-view-submission-log-form.png)

Welke resultaten die in het indieningslogboek worden weergegeven, is afhankelijk van de instelling van de functie e-Facturering in RCS. Ongeacht de instellingen, heeft het indieningslogboek altijd drie sneltabbladen:

- **Verwerkingsacties**: dit sneltabblad toont het uitvoeringslogboek voor de acties die zijn geconfigureerd in de functieversie die is ingesteld in RCS. De kolom **Status** geeft aan of de actie met goed gevolg is uitgevoerd.
- **Actiebestanden**: dit sneltabblad toont de tussenliggende bestanden die zijn gegenereerd tijdens de uitvoering van de acties. U kunt **Weergeven** selecteren om het bestand te downloaden en de inhoud ervan weer te geven.
- **Logboek verwerkingsacties**: dit sneltabblad toont de resultaten van de communicatie tussen de invoegtoepassing voor elektronische facturering en de doelwebservice. Het toont ook wat er is geretourneerd door de verwerking door de webservice.

## <a name="related-topics"></a>Verwante onderwerpen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Brazilië](e-invoicing-bra-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Mexico](e-invoicing-mex-get-started.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië](e-invoicing-ita-get-started.md)
- [De invoegtoepassing voor elektronische facturering instellen](e-invoicing-setup.md)
