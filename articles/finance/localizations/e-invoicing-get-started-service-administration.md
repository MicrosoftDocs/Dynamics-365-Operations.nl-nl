---
title: Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de invoegtoepassing voor elektronische facturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104363"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>Aan de slag met de serviceadministratie voor de invoegtoepassing voor elektronische facturering

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp voltooit, moet aan de volgende vereisten zijn voldaan:

- U moet toegang hebben tot uw Microsoft Dynamics Lifecycle Services-account (LCS).
- U moet een LCS-project hebben dat versie 10.0.13 of hoger van Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management bevat. Daarnaast moeten deze apps worden geïmplementeerd in een van de volgende Azure-geografische gebieden:

    - VS - oost
    - VS - west
    - Noordelijke EU
    - Westelijke EU

- U moet toegang hebben tot uw Dynamics 365 Regulatory Configuration Services-account (RCS).
- U moet de functie Globalisatie voor uw RCS-account in Functiebeheer activeren. Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie.
- U moet een Key Vault-resource en een opslagaccount in Azure maken. Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>De invoegtoepassing voor microservices in Lifecycle Services installeren

1. Meld u aan bij uw LCS-account.
2. Selecteer de tegel **Beheer van voorbeeldfuncties**.
3. Selecteer **e-Factureringsservice** in het gedeelte **Openbare voorbeeldfuncties**.
4. Controleer of de optie **Voorbeeldfunctie ingeschakeld** op **Ja** is ingesteld.

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>De parameters voor RCS-integratie met de invoegtoepassing voor elektronisch factureren instellen

1. Meld u aan bij uw RCS-account.
2. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Parameters van elektronische rapportage**.
3. Voer op het tabblad **e-Factureringsservice** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.

    | Datacenter Azure-geografie | URI van service-eindpunt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | VS - oost                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | VS - west                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Noordelijke EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Westelijke EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. Controleer of het veld **Toepassings-id** is ingesteld op **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Dit is een vaste waarde.
5. Voer in het veld **LCS-omgevings-id** de id van uw LCS-abonnementsaccount in.
6. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-key-vault-secret"></a>Key Vault-geheim maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **e-Facturering**.
3. Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving** en selecteer **Key Vault-parameters**.
4. Selecteer **Nieuw** om een Key Vault-geheim te maken.
5. Voer in het veld **Naam** de naam in voor het Key Vault-geheim. Voer in het veld **Beschrijving** een beschrijving in.
6. Plak in het veld **Key Vault-URI** het geheim van Azure Key Vault.
7. Selecteer **Opslaan**.

## <a name="create-storage-account-secret"></a>Een opslagaccountgeheim maken

1. Selecteer op de pagina **Key Vault-parameters** in de sectie **Certificaten** de optie **Toevoegen**.
2. Voer in het veld **Naam** de naam in voor het opslagaccountgeheim. Voer in het veld **Beschrijving** een beschrijving in.
3. Selecteer in het veld **Type** de optie **Certificaat**.
4. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-an-electronic-invoicing-add-on-environment"></a>Een omgeving van de invoegtoepassing voor elektronische facturering maken

1. Meld u aan bij uw RCS-account.
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Omgeving** de tegel **e-Facturering**.

## <a name="create-a-service-environment"></a>Een serviceomgeving maken

1. Selecteer op de pagina **Omgevingsinstellingen** op het actiedeelvenster de optie **Serviceomgeving**.
2. Selecteer **Nieuw** om een nieuwe serviceomgeving te maken.
3. Voer in het veld **Naam** de naam in voor de omgeving voor e-facturering. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer in het veld **Opslag SAS-tokengeheim** de naam van het certificaat dat moet worden gebruikt om toegang tot het opslagaccount te verifiëren.
5. In de sectie **Gebruikers** selecteert u **Toevoegen** om een gebruiker toe te voegen die elektronische facturen via de omgeving mag indienen en ook verbinding mag maken met het opslagaccount.
6. Voer in het veld **Gebruikers-id** het alias van de gebruiker in. Voer in het veld **E-mail** het e-mailadres van de gebruiker in.
7. Selecteer **Opslaan**.
8. Als uw land-/regiospecifieke facturen een keten certificaten vereisen om digitale handtekeningen toe te passen, selecteert u in het actiedeelvenster de optie **Key Vault-parameters** en vervolgens **Keten van certificaten** en voert u deze stappen uit:

    1. Selecteer **Nieuw** om een keten certificaten te maken.
    2. Voer in het veld **Naam** de naam in voor de certificaatketen. Voer in het veld **Beschrijving** een beschrijving in.
    3. Selecteer in het gedeelte **Certificaten** de oiptie **Toevoegen** om een certificaat aan de keten toe te voegen.
    4. Met de knop **Omhoog** of **Omlaag** kunt u de positie van het certificaat in de keten wijzigen.
    5. Selecteer **Opslaan** en sluit de pagina.
    6. Sluit de pagina.
9. Selecteer op de pagina **Serviceomgeving** in het actiedeelvenster de optie **Publiceren** om de omgeving naar de cloud te publiceren. De waarde van het veld **Status** wordt gewijzigd in **Gepubliceerd**.

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

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance and Supply Chain Management

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>De integratie van de invoegtoepassing voor elektronisch factureren inschakelen

1. Meld u aan bij uw Finance of Supply Chain Management-exemplaar.
2. Zoek in de werkruimte **Functiebeheer** naar de functie **Integratie invoegtoepassing voor elektronisch factureren**. Als deze functie niet op de pagina wordt weergegeven, selecteert u **Controleren op updates**.
3. Selecteer de functie en selecteer **Nu inschakelen**.

### <a name="set-up-the-service-endpoint-url"></a>De URL van het service-eindpunt instellen

1. Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.
2. Voer op het tabblad **Indieningsservice** in het veld **Service-eindpunt URL** het juiste service-eindpunt in voor uw geografische Azure-regio, zoals wordt weergegeven in de volgende tabel.

    | Datacenter Azure-geografie | URL van service-eindpunt                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | VS - oost                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | VS - west                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | Noordelijke EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | Westelijke EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. Voer in het veld **Omgeving** de naam in voor de omgeving voor de invoegtoepassing voor e-facturering.
4. Selecteer **Opslaan** en sluit de pagina.
