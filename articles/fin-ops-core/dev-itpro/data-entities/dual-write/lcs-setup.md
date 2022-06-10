---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783196"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Instellingen voor twee keer wegschrijven van Lifecycle Services

[!include [banner](../../includes/banner.md)]



In dit onderwerp wordt uitgelegd hoe u twee keer wegschrijven kunt inschakelen vanuit Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Vereisten

Klanten moeten de integratie van Power Platform voltooien zoals beschreven in de volgende onderwerpen:

- Als u Microsoft Power Platform nog niet gebruikt en uw Finance and Operations-omgevingen wilt uitbreiden door platformmogelijkheden toe te voegen, raadpleegt u [Power Platform-integratie: inschakelen tijdens de implementatie van de omgeving](../../power-platform/enable-power-platform-integration.md#enable-during-deploy).
- Als u al Dataverse- en Power Platform-omgevingen hebt en deze wilt verbinden met Finance and Operations-omgevingen, raadpleegt u [Power Platform-integratie: inschakelen tijdens de implementatie van de omgeving](../../power-platform/enable-power-platform-integration.md#enable-after-deploy).

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>Twee keer wegschrijven instellen voor nieuwe of bestaande Dataverse-omgevingen

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

8. Wanneer de koppeling is voltooid, wordt er een hyperlink weergegeven. Gebruik de koppeling om u aan te melden bij het beheergebied voor twee keer wegschrijven in de client voor financiële en bedrijfsactiviteiten. Vanaf hier kunt u entiteitstoewijzingen instellen.

## <a name="linking-mismatch"></a>Koppeling aan een verkeerde instantie

Het is mogelijk dat uw omgeving voor twee keer wegschrijven wordt gekoppeld aan een Dataverse-exemplaar terwijl LCS niet is ingesteld voor Power Platform-integratie. Deze onjuiste koppeling kan tot onverwachte gedragingen leiden. Het wordt aangeraden de details van de LCS-omgeving te laten overeenkomen met de gegevens waarmee u bent verbonden via twee keer wegschrijven, zodat dezelfde verbinding kan worden gebruikt door zakelijke gebeurtenissen, virtuele tabellen en invoegtoepassingen.

Als er in uw omgeving een verkeerde koppeling voorkomt, wordt in LCS een waarschuwing weergegeven die lijkt op het volgende voorbeeld op de detailpagina van uw omgeving: 'Microsoft heeft gedetecteerd dat uw omgeving via Twee keer wegschrijven is gekoppeld aan een andere bestemming dan is opgegeven in de Power Platform-integratie. Dit wordt niet aanbevolen.'

Verkeerde :::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform-integratiekoppeling.":::

Als u deze waarschuwing ontvangt, kunt u een van de volgende oplossingen proberen:

- Als uw LCS-omgeving nooit is ingesteld voor Power Platform-integratie, kunt u verbinding maken met het Dataverse-exemplaar dat voor twee keer wegschrijven is geconfigureerd door de instructies in dit artikel te volgen.
- Als uw LCS-omgeving al is ingesteld voor Power Platform-integratie, moet u de koppeling met twee keer wegschrijven ongedaan maken en deze opnieuw koppelen aan de integratie die met de LCS-omgeving is opgegeven met behulp van de [koppeling Scenario: Opnieuw instellen of wijzigen](relink-environments.md#scenario-reset-or-change-linking).

In het verleden was er een handmatige ondersteuningsticketoptie beschikbaar, maar dat was vóór optie 1 hierboven bestond.  Microsoft ondersteunt geen aanvragen voor handmatige herkoppeling via ondersteuningstickets meer.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
