---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 08/03/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1fd15b5d664fead10949750678a2d3eab967af22
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781387"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Instellingen voor twee keer wegschrijven van Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp wordt uitgelegd hoe u twee keer wegschrijven kunt inschakelen vanuit Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Vereisten

U moet de integratie van Power Platform voltooien zoals beschreven in de volgende onderwerpen:

+ [Power Platform-integratie: inschakelen tijdens de implementatie van de omgeving](../../power-platform/enable-power-platform-integration.md#enable-during-deploy)
+ [Power Platform-integratie: inschakelen na de implementatie van de omgeving](../../power-platform/enable-power-platform-integration.md#enable-after-deploy)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>Twee keer wegschrijven instellen voor nieuwe Dataverse-omgevingen

Voer de volgende stappen uit om twee keer wegschrijven via de pagina **Omgevingsdetails** in LCS in te stellen:

1. Vouw op de pagina **Omgevingsdetails** de sectie **Power Platform-integratie** uit.

2. Selecteer de knop **Toepassing twee keer wegschrijven**.

    ![Power Platform-integratie.](media/powerplat_integration_step2.png)

3. Neem de algemene voorwaarden door en selecteer vervolgens **Configureren**.

4. Selecteer **OK** om door te gaan.

5. U kunt de voortgang controleren door de pagina met details van de omgeving periodiek te vernieuwen. De instelling duurt doorgaans 30 minuten of minder.  

6. Wanneer de instelling is voltooid, wordt u in een bericht geïnformeerd of het proces is geslaagd of dat er een fout is gevonden. Als de instelling is mislukt, wordt een bijbehorend foutbericht weergegeven. U moet alle fouten oplossen voordat u naar de volgende stap gaat.

7. Selecteer **Koppeling naar Power Platform-omgeving** om een koppeling te maken tussen Dataverse en de databases van de huidige omgeving. Dit duurt doorgaans 5 minuten of minder.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Koppeling naar Power Platform-omgeving.":::

8. Wanneer de koppeling is voltooid, wordt er een hyperlink weergegeven. Gebruik de koppeling om u aan te melden bij het beheergebied voor twee keer wegschrijven in de Finance and Operations-omgeving. Vanaf hier kunt u entiteitstoewijzingen instellen.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>Twee keer wegschrijven instellen voor een bestaande Dataverse-omgeving

Als u twee keer wegschrijven wilt instellen voor een bestaande Dataverse-omgeving, moet u een Microsoft-[ondersteuningsticket](../../lifecycle-services/lcs-support.md) maken. Het ticket moet het volgende bevatten:

+ Uw ID voor de Finance and Operations-omgeving.
+ Uw omgevingsnaam van Lifecycle Services.
+ De Dataverse-organisatie-ID of Power Platform-omgevings-ID van Power Platform Beheercentrum. Vraag in uw ticket om de ID te gebruiken voor Power Platform-integratie.

> [!NOTE]
> U kunt omgevingen niet ontkoppelen met behulp van LCS. Als u een omgeving wilt ontkoppelen, opent u de werkruimte **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.

## <a name="linking-mismatch"></a>Koppeling aan een verkeerde instantie

Het is mogelijk dat uw LCS-omgeving aan één Dataverse-instantie gekoppeld is, terwijl uw omgeving voor twee keer wegschrijven aan een andere Dataverse-instantie gekoppeld is. Deze koppeling aan een verkeerde instantie kan tot onverwacht gedrag leiden en kan ertoe leiden dat gegevens naar de verkeerde omgeving worden verzonden. De aanbevolen omgeving voor twee keer wegschrijven is de omgeving die wordt gemaakt als onderdeel van de Power Platform-integratie en op lange termijn is dit de enige manier om een koppeling tussen omgevingen tot stand te brengen.

Als er in uw omgeving een verkeerde koppeling voorkomt, wordt in LCS een waarschuwing weergegeven op de detailpagina van uw omgeving, in de trant van 'Microsoft heeft gedetecteerd dat uw omgeving via Twee keer wegschrijven is gekoppeld aan een andere bestemming dan is opgegeven in de Power Platform-integratie. Dit wordt niet aanbevolen:

Verkeerde :::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-integratiekoppeling.":::

Als deze fout plaatsvindt, kunt u afhankelijk van uw behoeften twee dingen doen:

+ [Omgevingen voor twee keer wegschrijven loskoppelen en opnieuw koppelen (Koppeling opnieuw instellen of wijzigen)](relink-environments.md#scenario-reset-or-change-linking) zoals wordt beschreven op de detailpagina van uw LCS-omgeving. Dit is de ideale optie, omdat u deze kunt uitvoeren zonder Microsoft-ondersteuning.  
+ Als u de koppeling in de omgeving voor twee keer wegschrijven wilt behouden, kunt u bij Microsoft Ondersteuning om hulp vragen om de Power Platform-integratie te wijzigen en uw bestaande Dataverse-omgeving te gebruiken, zoals in de voorgaande sectie wordt beschreven.  

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
