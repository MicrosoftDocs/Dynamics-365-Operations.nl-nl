---
title: Een IoT-oplossing implementeren in Azure
description: Sensor Data Intelligence maakt gebruik van sensoren die verbinding hebben met Microsoft Azure. In dit artikel wordt uitgelegd hoe u een IoT-oplossing (Internet of Things) implementeert in uw Azure-abonnement.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreAzureResourceDeploymentWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5f0f49c0f7daaacb85b75dc11b9f015b6aa4e997
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689716"
---
# <a name="deploy-an-iot-solution-on-azure"></a>Een IoT-oplossing implementeren in Azure

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Sensor Data Intelligence maakt gebruik van sensoren die verbinding hebben met Microsoft Azure. Om Azure in staat te stellen om gegevens op te halen uit uw sensoren en deze te delen met Dynamics 365 Supply Chain Management, moet u een IoT-oplossing (Internet of Things) implementeren in Azure-abonnement. In het volgende architectuurdiagram vindt u een overzicht van de oplossing en de componenten ervan.

![Diagram met de architectuur van Sensor Data Intelligence.](media/sdi-architecture.png "Diagram met de architectuur van Sensor Data Intelligence")

## <a name="video-instructions"></a>Video-instructies

De volgende video laat zien hoe u de [functie Sensor Data Intelligence kunt inschakelen](sdi-enable-feature.md) en de vereiste Azure-resources kunt implementeren. In de andere sectie in dit artikel vindt u dezelfde instructies in tekstvorm.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Procedure

Voer de volgende stappen uit om de vereiste resources te implementeren in Azure.

1. Meld u aan bij Supply Chain Management als beheerder.
1. Ga naar **Systeembeheer \> Instellingen \> Sensor Data Intelligence \> Azure-resources implementeren en verbinden** om de implementatiewizard te starten.
1. Lees de informatie op de pagina **Welkom** en selecteer vervolgens **Volgende**.
1. Lees de informatie op de pagina **De voorbeeld-IoT-oplossing implementeren naar Azure** en selecteer  in de sectie **Instructies** de optie **Implementeren**.
1. Er wordt een nieuw browsertabblad geopend en u wordt naar de Azure-portal gebracht, zodat u de Azure-resources kunt implementeren. Meld u aan met uw referenties voor uw Azure-abonnement als hierom wordt gevraagd.
1. Selecteer op de pagina **Aangepaste implementatie** in het veld **Abonnement** uw abonnement.
1. Selecteer onder het veld **Brongroep** de optie **Nieuwe maken** om een resourcegroep te maken voor Azure-componenten die u gaat implementeren.
1. Voer in het vervolgkeuzevenster dat wordt geopend, in het veld **Naam** een naam in voor de nieuwe brongroep (bijvoorbeeld *IoT-demo*). Selecteer vervolgens **OK**.
1. Stel de volgende velden in:

    - **Brongroep**: selecteer de brongroep die u zojuist hebt gemaakt.
    - **Regio**: selecteer een regio, het liefst de regio waar uw Supply Chain Management-omgeving is geïmplementeerd. Houd er rekening mee dat de prijzen voor de Azure-regio's kunnen verschillen. U kunt de geschatte kosten voor uw regio weergeven met de [Prijsrekenprogramma voor Sensor Data Intelligence](https://azure.com/e/c36c4947ebff4215b2e62590c2a24c68).
    - **URL van Supply Chain Management-omgeving**: geef de URL voor uw Supply Chain Management-omgeving op.
    - **Bestaande Azure IoT-hub opnieuw gebruiken**: schakel dit selectievakje niet in.

1. Selecteer **Volgende: controleren en maken**.
1. Controleer op de pagina **Aangepaste implementatie** of de validatie is geslaagd en klik dan op **Maken**.
1. De pagina **Implementatie wordt uitgevoerd** geeft de voortgang van uw implementatie weer. Het implementatieproces kan tot 30 minuten duren. Wanneer op de pagina **Implementatie wordt uitgevoerd** wordt gemeld dat de implementatie is voltooid, selecteert u de koppeling van de resourcegroepnaam om een pagina te openen met de lijst met resources die in de groep zijn geïmplementeerd.
1. Zoek in de lijst met resources de record waar het veld **Type** is ingesteld op *Beheerde identiteit*. Selecteer in de kolom **Naam** de naam om de pagina met gegevens van de bron te openen.
1. Kopieer de waarde in het veld **Client-id** (bijvoorbeeld door te klikken op de knop **Kopiëren naar klembord**).
1. Ga terug naar het browsertabblad waar Supply Chain Management wordt uitgevoerd, *maar sluit niet het tabblad voor de Azure-portal*. De pagina van de wizard **De voorbeeld-IoT-oplossing implementeren naar Azure** moet nog open zijn. 
1. Selecteer **Volgende**.
1. Plak op de pagina **Azure-resources verbinden** in het veld **Client-id Azure AD-toepassing** de waarde van **Client-id** die u net hebt gekopieerd.
1. Ga terug naar het browsertabblad waar de Azure-portal is geopend, *maar sluit niet het tabblad voor Supply Chain Management*. De pagina met details van de bron moet nog steeds open zijn.
1. Klik op de knop **Terug** in de browser om terug te gaan naar de lijst met resources in de nieuwe resourcegroep.
1. Zoek in de lijst met resources de record waarvoor het veld **Type** is ingesteld op *Azure-cache voor Redis*. Selecteer in de kolom **Naam** de naam om de pagina met gegevens van de bron te openen.
1. Selecteer **Toegangssleutels** in het navigatievenster aan de linkerkant.
1. Kopieer op de pagina **Toegangssleutels** de waarde die wordt getoond voor **Primaire verbindingsreeks (StackExchange.Redis)** (bijvoorbeeld door te klikken op de knop **Kopiëren naar klembord**).
1. Ga terug naar het browsertabblad waarop Supply Chain Management wordt uitgevoerd. De pagina **Azure-resources verbinden** moet nog openstaan.
1. In het veld **Verbindingsreeks voor metrische opslag (Redis)** plakt u de waarde uit het veld **Primaire verbindingsreeks (StackExchange.Redis)** die u hebt gekopieerd.
1. Selecteer **Voltooien**.

Azure-bronnen voor Sensor Data Intelligence worden nu geïmplementeerd in uw Azure-abonnement.

> [!NOTE]
> U kunt op elk moment de verbindingsgegevens weergeven of bewerken die in Supply Chain Management zijn opgeslagen, door de pagina **Parameters van Sensor Data Intelligence** te openen. Meer informatie over dit onderwerp vindt u in [Parameters van Sensor Data Intelligence](sdi-parameters.md).
