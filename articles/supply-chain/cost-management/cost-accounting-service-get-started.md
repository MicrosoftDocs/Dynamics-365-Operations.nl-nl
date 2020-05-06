---
title: Aan de slag met de service kostprijsboekhouding
description: In dit onderwerp vindt u informatie over licenties en installatie-instructies voor de service kostprijsboekhouding.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: cbbce7eaac264973bf0b95ad5175bf70ed2b4ae9
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276904"
---
# <a name="get-started-with-the-cost-accounting-service"></a>Aan de slag met de service kostprijsboekhouding

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> De functionaliteit die in dit onderwerp wordt vermeld, is beschikbaar als onderdeel van een beperkte preview-versie. De inhoud van dit onderwerp en de functionaliteit die dit onderwerp beschrijft, kunnen worden gewijzigd. Meer informatie over preview-versies vindt u in [Veelgestelde vragen over updates van service met één versie](../../fin-ops-core/fin-ops/get-started/one-version.md).

Met de service kostprijsboekhouding kunt u meerdere voorraadboekingen uitvoeren in de grootboeken voor kostprijsboekhouding die u hebt ingesteld. U koppelt alle grootboeken voor de kostenboekhouding aan een *conventie*. Een conventie is een verzameling van de volgende typen boekhoudbeleidsregels:

- Kostenobject
- Basis van invoermeting
- Veronderstelling van kostenstroom
- Kostenelement

> [!NOTE]
> Zelfs nadat u de service kostprijsboekhouding hebt ingeschakeld, kunt u nog gewoon voorraadboekhouding uitvoeren in Microsoft Dynamics 365 Supply Chain Management.

De service kostprijsboekhouding is een invoegtoepassing. Om de functies beschikbaar te maken, moet u deze installeren vanuit Microsoft Dynamics Lifecycle Services (LCS). Daarom kunt u ervoor kiezen om deze te evalueren in een testomgeving voordat u ze voor productie-omgevingen inschakelt.

De kostprijsboekhouding biedt momenteel geen ondersteuning voor alle functies voor kostenbeheer die in Dynamics 365 Supply Chain Management zijn ingebouwd. Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is, voldoet aan uw behoeften.

## <a name="licensing"></a>Licenties

De service voor kostprijsboekhouding wordt samengevoegd met de standaardfuncties van voorraadboekhouding die beschikbaar zijn voor Supply Chain Management. U hoeft geen extra licentie aan te schaffen voor het gebruik van de service kostprijsboekhouding.

## <a name="install-the-add-in"></a>De invoegtoepassing installeren

> [!IMPORTANT]
> Als u de service kostprijsboekhouding wilt gebruiken, moet u beschikken over een omgeving met hoge beschikbaarheid voor LCS (geen OneBox-omgeving) en moet u Dynamics 365 Supply Chain Management versie 10.0.11 of hoger uitvoeren.

Als u de service kostprijsboekhouding wilt gebruiken, installeert u de invoegtoepassing voor kostprijsboekhouding in Supply Chain Management, zoals wordt beschreven in de volgende procedure.

1. Meld u aan bij LCS.

1. Ga naar **Beheer van previewfuncties**.

1. Selecteer het plusteken (**+**).

1. Voer in het veld **Code** de bètasleutel van de invoegtoepassing voor de kostprijsboekhouding in. (U hebt de sleutel per e-mail ontvangen.)

1. Selecteer **Deblokkeren**.

1. Open de LCS-omgeving waar u de service wilt toevoegen.

1. Ga naar **Volledige details**.

1. Schuif omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.

1. Selecteer **Een nieuwe invoegtoepassing installeren**.

1. Selecteer **Service kostprijsboekhouding**.

1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.

1. Selecteer **Installeren**.

1. Op het sneltabblad **Invoegtoepassingen voor omgeving** ziet u dat de service kostprijsboekhouding wordt geïnstalleerd. Na enkele minuten verandert de status van **Bezig met installeren** in **Geïnstalleerd**. (Mogelijk moet u de pagina vernieuwen om deze wijziging te zien.) Op dat moment is de service voor kostprijsboekhouding klaar voor gebruik.

## <a name="set-up-the-integration"></a>De integratie instellen

De integratie instellen tussen de service kostprijsboekhouding en Dynamics 365 Supply Chain Management:

1. Ga naar **Systeembeheer > Functiebeheer**.

1. Selecteer **Controleren op updates**.

1. Open het tabblad **Alles** en zoek de functie met de naam *Service kostprijsboekhouding*.

1. Selecteer **Nu inschakelen**.

1. Ga naar **Kostenbeheer > Service kostprijsboekhouding > Instellen > Parameters service kostprijsboekhouding > Integratieparameters**.

1. Voer in het veld **Toepassings-id** de volgende code in:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Voer in het veld **Eindpunt gegevensservice** de volgende URL in:<br>https://operationsdataservice.operations365.dynamics.com/

1. Voer in het veld **Eindpunt service kostenboekhouding** de volgende URL in:<br>https://costaccountingservice.operations365.dynamics.com/

1. De service kostprijsboekhouding is nu klaar voor gebruik.

## <a name="related-resources"></a>Gerelateerde bronnen

[Startpagina van service Kostprijsboekhouding](cost-accounting-service-home.md)
