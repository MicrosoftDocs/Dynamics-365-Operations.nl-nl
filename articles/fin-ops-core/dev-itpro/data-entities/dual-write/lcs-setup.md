---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103564"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Instellingen voor twee keer wegschrijven van Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp wordt uitgelegd hoe u twee keer wegschrijven kunt inschakelen vanuit Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Vereisten

U moet de integratie van Power Platform voltooien zoals beschreven in de volgende onderwerpen:

+ [Power Platform-integratie: inschakelen tijdens de implementatie van de omgeving](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform-integratie: instellen na de implementatie van de omgeving](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Twee keer wegschrijven instellen voor nieuwe Dataverse-omgevingen

Voer de volgende stappen uit om twee keer wegschrijven via de pagina **Omgevingsdetails** in LCS in te stellen:

1. Vouw op de pagina **Omgevingsdetails** de sectie **Power Platform-integratie** uit.

2. Selecteer de knop **Toepassing twee keer wegschrijven**.

    ![Power Platform-integratie](media/powerplat_integration_step2.png)

3. Neem de algemene voorwaarden door en selecteer vervolgens **Configureren**.

4. Selecteer **OK** om door te gaan.

5. U kunt de voortgang controleren door de pagina met details van de omgeving periodiek te vernieuwen. De instelling duurt doorgaans 30 minuten of minder.  

6. Wanneer de instelling is voltooid, wordt u in een bericht geïnformeerd of het proces is geslaagd of dat er een fout is gevonden. Als de instelling is mislukt, wordt een bijbehorend foutbericht weergegeven. U moet alle fouten oplossen voordat u naar de volgende stap gaat.

7. Selecteer **Koppeling naar Power Platform-omgeving** om een koppeling te maken tussen Dataverse en de databases van de huidige omgeving. Dit duurt doorgaans 5 minuten of minder.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koppeling naar Power Platform-omgeving":::

8. Wanneer de koppeling is voltooid, wordt er een hyperlink weergegeven. Gebruik de koppeling om u aan te melden bij het beheergebied voor twee keer wegschrijven in de Finance and Operations-omgeving. Vanaf hier kunt u entiteitstoewijzingen instellen.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Twee keer wegschrijven instellen voor een bestaande Dataverse-omgeving

Als u twee keer wegschrijven wilt instellen voor een bestaande Dataverse-omgeving, moet u een Microsoft-[ondersteuningsticket](../../lifecycle-services/lcs-support.md) maken. Het ticket moet het volgende bevatten:

+ Uw ID voor de Finance and Operations-omgeving.
+ Uw omgevingsnaam van Lifecycle Services.
+ De Dataverse-organisatie-ID of Power Platform-omgevings-ID van Power Platform Beheercentrum. Vraag in uw ticket om de ID te gebruiken voor Power Platform-integratie.

> [!NOTE]
> U kunt omgevingen niet ontkoppelen met behulp van LCS. Als u een omgeving wilt ontkoppelen, opent u het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
