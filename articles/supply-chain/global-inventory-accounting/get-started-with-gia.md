---
title: Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)
description: In dit artikel wordt beschreven hoe u aan de slag gaat met Algemene voorraadboekhouding.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 463a66002ec7a6536c9ff829f9ea2c3734138eae
ms.sourcegitcommit: 6221a25f81aa83ab335de7cb6b6c3014dbec0116
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177143"
---
# <a name="get-started-with-global-inventory-accounting"></a>Aan de slag met Algemene voorraadboekhouding (Global Inventory Accounting)

[!include [banner](../includes/banner.md)]

Met Algemene voorraadboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor Algemene voorraadboekhouding die u hebt ingesteld. U moet elk grootboek voor Algemene voorraadboekhouding aan een *conventie* koppelen. Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:

- Kostenobject
- Basis van invoermeting
- Veronderstelling van kostenstroom
- Kostenelement

> [!NOTE]
> Zelfs nadat u Algemene voorraadboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.

Algemene voorraadboekhouding is een invoegtoepassing. Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS). U kunt ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.

Algemene voorraadboekhouding ondersteunt momenteel niet alle kostenbeheerfuncties die in Supply Chain Management zijn ingebouwd. Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Procedure voor het ophalen van de invoegtoepassing Algemene voorraadboekhouding

> [!IMPORTANT]
> Als u Algemene voorraadboekhouding wilt gebruiken, moet u een omgeving met hoge beschikbaarheid voor LCS hebben (niet in een OneBox-omgeving). Daarnaast moet u Supply Chain Management versie 10.0.19 of hoger uitvoeren.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management versie 10.0.19 tot 10.0.26

Als u Algemene voorraadboekhouding voor Supply Chain Management versie 10.0.19 tot en met 10.0.26 wilt installeren, [installeert u eerst de invoegtoepassing](#install). Verzend vervolgens uw LCS-omgevings-id en bedrijfsnaam per e-mail naar het [team voor Algemene voorraadboekhouding](mailto:GlobalInvAccount@microsoft.com). U ontvangt van het team een opvolgings-e-mail met uw service-eindpunten voor Algemene voorraadboekhouding.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Management versie 10.0.27 en hoger

Als u Algemene voorraadboekhouding voor Supply Chain Management versie 10.0.27 en hoger wilt installeren, hoeft u alleen [de invoegtoepassing te installeren](#install). Voor deze versies van Supply Chain Management worden de service-eindpunten voor Algemene voorraadboekhouding automatisch ingesteld, zodat u deze niet handmatig hoeft te vinden. Als er tijdens het instellen van de invoegtoepassing wel problemen zijn, kunt u contact opnemen met het [team van Algemene voorraadboekhouding](mailto:GlobalInvAccount@microsoft.com).

## <a name="licensing"></a>Licenties

Algemene voorraadboekhouding wordt samengevoegd met de standaardfuncties van kostenbeheer die beschikbaar zijn voor Supply Chain Management. U hoeft geen extra licentie aan te schaffen voor het gebruik van Algemene voorraadboekhouding.

## <a name="prerequisites"></a>Vereisten

### <a name="set-up-microsoft-power-platform-integration"></a>Microsoft Power Platform-integratie instellen

Voordat u de functionaliteit van de invoegtoepassing kunt inschakelen, moet u deze als volgt integreren in Microsoft Power Platform.

1. Open de LCS-omgeving waar u de service wilt toevoegen.
1. Ga naar **Volledige details**.
1. Selecteer **Instellingen** in de sectie **Power Platform**-integratie.
1. Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**. Het instellen duurt doorgaans tussen de 60 en 90 minuten.
1. Nadat de instelling van de Microsoft Power Platform-omgeving is voltooid, wordt op de pagina de naam van uw omgeving weergegeven. Verder wordt in de sectie **Power Platform-integratie** de melding 'De instelling van de Power Platform-omgeving is voltooid' weergegeven. Voor Algemene voorraadboekhouding is geen toepassing voor twee keer wegschrijven vereist.

Zie [Inschakelen na de implementatie van de omgeving](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy) voor meer informatie.

## <a name="install-or-update-the-add-in-and-solution"></a><a name="install"></a>De invoegtoepassing en oplossing installeren of bijwerken

Gebruik de volgende procedure om de invoegtoepassing en oplossing Algemene voorraadboekhouding te installeren of bij te werken. Het gedeelte van de procedure dat u moet volgen, is afhankelijk van de vraag of u de installatie voor het eerst uitvoert of dat u de oplossing voor een bestaande installatie alleen moet bijwerken.

- Als u de invoegtoepassing nooit eerder hebt geïnstalleerd, volgt u de volledige procedure voor het installeren van zowel de invoegtoepassing als de oplossing.
- Als u Algemene voorraadboekhouding al gebruikt maar de oplossing in het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com) moet bijwerken, hoeft u alleen stap 6 uit te voeren en alle andere stappen over te slaan.

De invoegtoepassing en oplossing installeren of bijwerken:

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index).
1. Open de LCS-omgeving waar u de service wilt toevoegen.
1. Ga naar **Volledige details**.
1. Ga naar **Power Platform-integratie** en selecteer **Instelling**.
1. Schakel het selectievakje **Power Platformomgeving instellen** in het dialoogvenster in en selecteer **Instellingen**. Het instellen duurt doorgaans tussen de 60 en 90 minuten.
1. Nadat de instelling van de Microsoft Power Platform-omgeving is voltooid, meldt u zich aan bij het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com) en installeert u de oplossing Algemene voorraadboekhouding of werkt u deze bij door de volgende stappen uit te voeren:
   1. Selecteer de omgeving waar u de oplossing wilt installeren of bijwerken.
   1. Selecteer **Dynamics 365-apps**.
   1. Selecteer **App installeren**.
   1. Selecteer **Algemene voorraadboekhouding Dynamics 365**.
   1. Selecteer **Volgende** om te installeren.
1. Ga terug naar de LCS-omgeving nadat de oplossing volledig is geïnstalleerd. Selecteer op het sneltabblad **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
1. Selecteer **Global Inventory Accounting** (Algemene voorraadboekhouding).
1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
1. Selecteer **Installeren**.
1. Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat Algemene voorraadboekhouding wordt geïnstalleerd. Na enkele minuten verandert de status van *Bezig met installeren* in *Geïnstalleerd*. (Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is Algemene voorraadboekhouding klaar voor gebruik.

Als de standaardtaal van uw Dataverse-installatie niet Engels is, volgt u deze stappen:

1. Ga naar **Geavanceerde instelling \> Beheer \> Talen**.
1. Selecteer *Engels* (*LanguageCode=1033*) en selecteer vervolgens **Toepassen**.

## <a name="set-up-the-integration"></a>De integratie instellen

Volg deze stappen om de integratie in te stellen tussen Global Inventory Accounting en Supply Chain Management.

1. Meld u aan bij Supply Chain Management.
1. Ga naar **Systeembeheer \> Functiebeheer**.
1. Selecteer **Controleren op updates**.
1. Zoek op het tabblad **Alle** naar de functie genaamd *(Preview) Algemene voorraadboekhouding*.
1. Selecteer **Nu inschakelen**.
1. Ga naar voor **Algemene voorraadboekhouding \> Instellen \> Parameters algemene voorraadboekhouding \> Integratieparameters**.
1. Ga als volgt te werk, afhankelijk van welke versie van Supply Chain Management wordt uitgevoerd:
    - **Supply Chain Management versie 10.0.19 tot en met 10.0.26**: voer in de velden **Eindpunt gegevensservice** en **Eindpunt van algemene voorraadboekhouding** de URL's in die per e-mail naar u zijn verzonden vanuit het team voor Algemene voorraadboekhouding (zie ook [Procedure voor het ophalen van de invoegtoepassing Algemene voorraadboekhouding](#sign-up)).
    - **Supply Chain Management versie 10.0.27 en nieuwer**: u hoeft de eindpunten niet in te voeren, dus u kunt deze stap overslaan.

Global Inventory Accounting is nu klaar voor gebruik.
