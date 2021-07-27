---
title: Aan de slag met servicebeheer voor Elektronische facturering
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met Elektronische facturering.
author: gionoder
ms.date: 05/24/2021
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
ms.openlocfilehash: 8adbe577e5111a6a4afdba6aed32855b2e30b39b
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6335685"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>Aan de slag met servicebeheer voor Elektronische facturering

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:

- U moet toegang hebben tot uw Microsoft Dynamics Lifecycle Services-account (LCS).
- U moet een LCS-project hebben dat versie 10.0.17 of hoger van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management bevat. Daarnaast moeten deze apps worden geïmplementeerd in een van de volgende Azure-geografische gebieden:

    - Verenigde Staten
    - Europa
    - Verenigd Koninkrijk
    - Azië

- U moet toegang hebben tot uw Dynamics 365 Regulatory Configuration Services-account (RCS).
- U moet de functie Globalisatie voor uw RCS-account in Functiebeheer activeren. Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.
- U moet een Key Vault-resource en een opslagaccount in Azure maken. Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>De invoegtoepassing voor microservices in Lifecycle Services installeren

1. Meld u aan bij uw LCS-account en selecteer op het LCS-projectdashboard een LCS-project.
2. Selecteer in het project op het omgevingsdashboard uw LCS-implementatieproject. Het project dat u selecteert, moet worden uitgevoerd.
3. Selecteer op het tabblad **Power Platform-integratie** in de veldgroep **Omgevingsinvoegtoepassingen** de optie **Een nieuwe invoegtoepassing installeren**.
4. Selecteer **Elektronische facturering**.
5. Voer in het veld **AAD-toepassings-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe** in. Dit is een vaste waarde.
6. Voer in het veld **AAD-tenant-id** de tenant-id van uw Azure-abonnementsaccount in.
7. Neem de algemene voorwaarden door en schakel vervolgens het selectievakje in.
8. Selecteer **Installeren**.


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>De parameters voor RCS-integratie met Elektronisch facturering instellen

1. Meld u aan bij uw RCS-account.
2. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.
3. Voer op het tabblad **e-Factureringsservice** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.

    | Datacenter Azure-geografie | URI van service-eindpunt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Verenigde Staten              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Verenigd Koninkrijk             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azië                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. Controleer of het veld **Toepassings-id** is ingesteld op **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Dit is een vaste waarde.
5. Voer in het veld **LCS-omgevings-id** de id van uw LCS-omgeving in.
6. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-key-vault-references"></a>Key Vault-verwijzingen maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.
4. Selecteer **Nieuw** om een Key Vault-verwijzing te maken.
5. Voer in het veld **Naam** de naam in voor de Key Vault-verwijzing. Voer in het veld **Beschrijving** een beschrijving in.
6. Plak in het veld **Key Vault-URI** het Key Vault-geheim van Azure Key Vault. Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.
7. Selecteer **Opslaan**.

## <a name="create-storage-account-secret"></a>Een opslagaccountgeheim maken

1. Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Serviceomgeving** > **Key Vault-parameters**.
2. Selecteer een **Key Vault-verwijzing** en selecteer **Toevoegen** in de sectie **Certificaten**.
3. Voer in het veld **Naam** de naam in voor het opslagaccountgeheim. Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer in het veld **Type** de optie **Geheim**.
6. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-a-digital-certificate-secret"></a>Een digitaal certificaatgeheim maken

1. Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.
2. Selecteer een **Key Vault-verwijzing** en selecteer **Toevoegen** in de sectie **Certificaten**.
3. Voer in het veld **Naam** de naam in voor het digitale certificaatgeheim. Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer in het veld **Type** de optie **Certificaat**.
6. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-a-service-environment"></a>Een serviceomgeving maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **Elektronische facturering**.
3. Selecteer op de pagina **Omgevingsinstellingen** in het actievenster de optie **Serviceomgeving**.
4. Selecteer **Nieuw** om een nieuwe serviceomgeving te maken.
5. Voer in het veld **Naam** de naam in voor de omgeving voor e-facturering. Voer in het veld **Beschrijving** een beschrijving in.
6. Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het opslagaccountgeheim dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.
7. In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en ook verbinding mag maken met het opslagaccount.
8. Voer in het veld **Gebruikers-id** het alias van de gebruiker in. Voer in het veld **E-mail** het e-mailadres van de gebruiker in.
9. Selecteer **Opslaan**.
10. Als uw land-/regiospecifieke facturen een keten certificaten vereisen om digitale handtekeningen toe te passen, selecteert u in het actiedeelvenster de optie **Key Vault-parameters** en vervolgens **Keten van certificaten** en voert u deze stappen uit:
    1. Selecteer **Nieuw** om een keten certificaten te maken.
    2. Voer in het veld **Naam** de naam in voor de certificaatketen. Voer in het veld **Beschrijving** een beschrijving in.
    3. Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.
    4. Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen.
    5. Selecteer **Opslaan** en sluit de pagina.
    6. Sluit de pagina.
11. Selecteer op de pagina **Serviceomgeving** in het actiedeelvenster de optie **Publiceren** om de omgeving naar de cloud te publiceren. De waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.

## <a name="create-a-connected-application"></a>Een verbonden toepassing maken

1. Selecteer op de pagina **Omgevingsinstellingen** in het actiedeelvenster de optie **Verbonden toepassingen**.
2. Selecteer **Nieuw** om een verbonden toepassing te maken.
3. Voer in het veld **Naam** de naam in voor de toepassing die moet worden verbonden.
4. Voer in het veld **Toepassing** de URL in van de Finance and Supply Chain Management-omgeving die u wilt verbinden.
4. Voer in het veld **Tenant** de tenant in van de Finance and Supply Chain Management-omgeving.
5. Selecteer **Opslaan**.
6. Selecteer in het actievenster de optie **Verbinding controleren** om de verbinding met de omgeving te testen. Sluit de pagina vervolgens.

## <a name="link-connected-applications-to-environments"></a>Verbonden toepassingen aan omgevingen koppelen

1. Selecteer op de pagina **Omgevingsinstellingen** de optie **Nieuw** om een verbonden toepassing toe te wijzen aan een omgeving.
2. Selecteer in het veld **Verbonden toepassing** een verbonden toepassing.
3. Selecteer in het veld **Serviceomgeving** een serviceomgeving.
4. Selecteer **Opslaan** en sluit de pagina.

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>De integratie van Elektronische facturering instellen in Finance en Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>De functie voor integratie van Elektronische facturering inschakelen

1. Meld u aan bij uw Finance of Supply Chain Management-exemplaar.
2. Zoek in de werkruimte **Functiebeheer** naar de functie **Integratie voor elektronisch factureren**. Als deze functie niet op de pagina wordt weergegeven, selecteert u **Controleren op updates**.
3. Selecteer de functie en selecteer **Nu inschakelen**.

### <a name="set-up-the-service-endpoint-url"></a>De URL van het service-eindpunt instellen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Voer op het tabblad **Indieningsservice** in het veld **Service-eindpunt URL** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.

    | Datacenter Azure-geografie | URI van service-eindpunt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | Verenigde Staten              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Verenigd Koninkrijk             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azië                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Voer in het veld **Omgeving** de naam in voor de serviceomgeving die is gepubliceerd in Elektronische facturering.
4. Selecteer **Opslaan** en sluit de pagina.

### <a name="enable-flighting-keys"></a>Flighting-codes inschakelen

Schakel flighting-codes in voor Microsoft Dynamics 365 Finance of Microsoft Dynamics 365 Supply Chain Management 10.0.17 of lager. 
1. Voer de volgende SQL-opdracht uit:

    INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INVOEGEN IN SYSFLIGHTING-WAARDEN (FLIGHT-NAAM, INGESCHAKELD) ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. Voer een IISreset-opdracht uit voor alle AOS's.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
