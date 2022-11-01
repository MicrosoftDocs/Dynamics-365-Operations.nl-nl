---
title: Regulatory Configuration Service (RCS) instellen
description: In dit artikel wordt uitgelegd hoe u Regulatory Configuration Service (RCS) instelt.
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710776"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Regulatory Configuration Service (RCS) instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u Regulatory Configuration Service (RCS) instelt.

## <a name="turn-on-globalization-features"></a>De globalisatiefuncties inschakelen

1. Meld u aan bij uw RCS-account.
2. Selecteer de tegel **Functiebeheer**.
3. Selecteer in het werkgebied **Functiebeheer** de optie **Globalisatiefuncties** in de lijst en selecteer **Nu inschakelen**.

Er moet een tegel voor het werkgebied **Globalisatiefuncties** worden weergegeven op het RCS-hoofddashboard.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>De parameters voor RCS-integratie met Elektronisch facturering instellen

1. Selecteer in het werkgebied **Globalisatiefuncties** in het gedeelte **Verwante instellingen** **Parameters elektronische rapportage**.
2. De eerste keer dat u de parameters instelt, wordt u gevraagd verbinding te maken met Life Cycle Services (LCS). Selecteer **Hier klikken om verbinding te maken met Lifecycle Services** en selecteer **OK** nadat de verbinding is gemaakt.

    > [!IMPORTANT]
    > In landen of regio's waar de gegevensresidentie wordt afgedwongen en als uw RCS was ingericht in een andere regio dan waar LCS wordt ingericht, kunt u het volgende foutbericht over de verbinding in RCS ontvangen: 'Er is geen HTTP-resource gevonden die overeenkomt met de aanvraag-URI'. Selecteer **OK**. U kunt een ander foutbericht krijgen in RCS: 'Kan het gebruikerstoken voor Dynamics Lifecycle Services niet genereren in opdracht van gebruiker '(). Neem contact op met uw systeembeheerder.'
    >  
    > Dit gebeurt omdat LCS een internationale service is en wordt ingericht in een Amerikaanse regio. De RCS uit uw huidige regio kan in verband met het gegevensresidentiebeleid geen verbinding maken met LCS. Er zijn dan twee mogelijke oplossingen:
    > - Verwijder RCS uit uw huidige regio en maak het opnieuw in de Amerikaanse regio.
    > - Negeer de fouten en ga door met de instelling voor elektronische facturering. Deze fouten hebben geen invloed op de functionaliteit voor elektronische facturering.

3. Voer op het tabblad **Elektronisch factureren** in het veld **Service-eindpunt URI** het juiste service-eindpunt in voor uw geografische Microsoft Azure-regio, zoals wordt weergegeven in de volgende tabel.

    | Datacenter Azure-geografie | URI van service-eindpunt |
    |----------------------------|----------------------|
    | Verenigde Staten              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Europa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Verenigd Koninkrijk             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Azië                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Japan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Zwitserland                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brazilië                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Verenigde Arabische Emiraten       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Australië                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Canada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Frankrijk                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | India                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Noorwegen                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Zuid-Afrika               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Controleer en typ in het veld **Toepassings-id** de vaste waarde **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Zorg ervoor dat alleen een GUID-identificatie (Globally Unique Identifier) is ingevoerd en dat de waarde geen andere symbolen bevat, zoals spaties, komma's, perioden of aanhalingstekens.
4. Voer in het veld **LCS-omgevings-id** de id van uw Microsoft Dynamics Lifecycle Services-omgeving (LCS) in. Deze waarde is de verwijzing naar de Finance- of Supply Chain Management-omgeving die u met de elektronische factureringsservice gaat gebruiken. U krijgt de id door u aan te melden bij [LCS](https://lcs.dynamics.com/), het projec te openen en vervolgens op het tabblad **Omgeving beheren** in de sectie **Omgevingsdetails** te zoeken in het veld **Omgevings-id**.

    > [!IMPORTANT]
    > Als de invoegtoepassing Elektronische facturering is geïnstalleerd in meerdere Finance- of Supply Chain Management-omgevingen in LCS, gebruikt u altijd de id van de omgeving die het meest recent is geïnstalleerd. Als u besluit de invoegtoepassing in een nieuwe omgeving te installeren nadat u de elektronische factureringsfunctionaliteit hebt ingesteld en gebruikt, werkt u het veld **LCS-omgevings-id** in RCS bij naar de laatste waarde.

5. Selecteer **Opslaan** en sluit de pagina.

## <a name="configuration-providers"></a>Configuratieproviders

U kunt configuratieproviders gebruiken om onderscheid te maken tussen de eigenaren van de ER-configuraties (elektronische rapportage) die worden gebruikt in elektronische factureringsprocessen en de globalisatiefuncties van de eigenaren. Voor alle globalisatiefuncties die door Microsoft worden geleverd en gepubliceerd in de Algemene opslagplaats, wordt de configuratieprovider ingesteld op **Microsoft** (`http://microsoft.com`).

U kunt alleen ER-configuraties en globalisatiefuncties aanpassen die bij de actieve configuratieprovider horen. U kunt deze configuraties en functies gebruiken als sjablonen om configuraties en functies te maken die bij de actieve configuratieprovider horen, zodat u ze kunt aanpassen.

Maak eerst de configuratieproviders. Stel vervolgens een provider in als actief. U kunt niet de **Microsoft**-configuratieprovider als actief instellen.

### <a name="create-a-configuration-provider"></a>Een configuratieprovider maken

1. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Configuratieproviders**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Naam** een unieke naam voor de configuratieprovider in.
4. Voer in het veld **Internetadres** de unieke URL in van de configuratieprovider.
5. Selecteer **Opslaan** en sluit de pagina.

### <a name="select-a-configuration-provider-as-active"></a>Een configuratieprovider als actief selecteren

1. Selecteer in de lijst met configuratieproviders de configuratieprovider die u wilt instellen als actief.
2. Selecteer **Instellingen als actief**.

## <a name="import-er-configurations-from-the-global-repository"></a>ER-configuraties importeren uit de algemene opslagplaats

1. Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Configuratieproviders**.
2. Selecteer **Microsoft** in de lijst met configuratieproviders en selecteer vervolgens **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer in het actievenster de optie **Openen**.
4. Importeer de volgende ER-modellen:

    - **Contextmodel klantfactuur**
    - **Factuurmodel**
    - **Fiscale documenten** (voor Braziliaanse scenario's, indien nodig)
    - **Model responsbericht**

5. Als **Factuurmodeltoewijzing** niet automatisch is geïmporteerd, importeert u deze.
6. Sluit de pagina.
