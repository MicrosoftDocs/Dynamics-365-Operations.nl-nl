---
title: Instellingen voor twee keer wegschrijven van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen tussen een nieuwe Finance and Operations-omgeving en een nieuwe Common Data Service-omgeving via Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172987"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Instellingen voor twee keer wegschrijven van Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een verbinding voor twee keer wegschrijven kunt instellen tussen een nieuwe Finance and Operations-omgeving en een nieuwe Common Data Service-omgeving via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Vereisten

U moet een beheerder zijn om een verbinding voor twee keer wegschrijven instelt.

+ U moet toegang tot de tenant hebben.
+ U moet een beheerder zijn in Finance and Operations- en Common Data Service-omgevingen.

## <a name="set-up-a-dual-write-connection"></a>Een verbinding voor twee keer wegschrijven instellen

Voer de onderstaande stappen uit om de verbinding voor twee keer wegschrijven in te stellen.

1. Ga in LCS naar uw project.
2. Selecteer **Configureren** om een nieuwe omgeving te implementeren.
3. Selecteer de versie. 
4. Selecteer de topologie. Als er slechts één topologie beschikbaar is, wordt deze automatisch geselecteerd.
5. Voer de eerste stappen in de wizard **Implementatie-instellingen** uit.
6. Voer een van deze stappen uit op het tabblad **Common Data Service**:

    - Als al een Common Data Service-omgeving is ingericht voor uw tenant, kunt u deze selecteren.

        1. Stel de optie **Common Data Service configureren** in op **Ja**.
        2. Selecteer in het veld **Beschikbare omgevingen** de omgeving die u met uw Finance and Operations-gegevens wilt integreren. De lijst bevat alle omgevingen waarvoor u beheerdersbevoegdheden hebt.
        3. Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.

        ![Het tabblad Common Data Service als al een Common Data Service-omgeving is ingericht voor uw tenant](../dual-write/media/lcs_setup_1.png)

    - Als voor uw tenant nog geen Common Data Service-omgeving bestaat, wordt een nieuwe omgeving ingericht.

        1. Stel de optie **Common Data Service configureren** in op **Ja**.
        2. Geef een naam op voor de Common Data Service-omgeving.
        3. Selecteer de regio waarin u de omgeving wilt implementeren.
        4. Selecteer de standaardtaal en -valuta voor de omgeving.

            > [!NOTE]
            > U kunt de taal en valuta later niet wijzigen.

        5. Schakel het selectie **Akkoord** in om aan te geven dat u akkoord gaat met de voorwaarden.

        ![Het tabblad Common Data Service wanneer uw tenant nog geen Common Data Service-omgeving heeft](../dual-write/media/lcs_setup_2.png)

7. Voer de resterende stappen in de wizard **Implementatie-instellingen** uit.
8. Als de omgevingsstatus **Geïmplementeerd** is, opent u de pagina met omgevingsdetails. In de sectie **Common Data Service-omgevingsgegevens** worden de namen weergegeven van de gekoppelde Finance and Operations-omgeving en Common Data Service-omgeving.

    ![De sectie Common Data Service-omgevingsgegevens](../dual-write/media/lcs_setup_3.png)

9. Een beheerder van de Finance and Operations-omgeving moet zich aanmelden bij LCS en **Koppeling naar CDS for Apps** selecteren om de koppeling te voltooien. Op de pagina met omgevingsgegevens worden de contactgegevens van de beheerder weergegeven.

    Als de koppeling is voltooid, wordt de status bijgewerkt naar **Omgevingskoppelingen voltooid**.

10. Selecteer **Koppeling naar CDS for Apps** om het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving te openen en de beschikbare sjablonen te beheren.

    ![De knop Koppeling naar CDS for Apps in de sectie Common Data Service-omgevingsgegevens](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> U kunt omgevingen niet ontkoppelen met behulp van LCS. Als u een omgeving wilt ontkoppelen, opent u het werkgebied **Gegevensintegratie** in de Finance and Operations-omgeving en selecteert u **Koppeling verbreken**.
