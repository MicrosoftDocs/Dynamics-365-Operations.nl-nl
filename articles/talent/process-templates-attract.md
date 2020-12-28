---
title: Een aanstellingsprocessjabloon maken in Attract
description: Dit onderwerp biedt informatie over het maken van een aanstellingsprocessjabloon in Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 82046d43cf7366b760c140bdb8b017337b4f41da
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460848"
---
# <a name="create-a-hiring-process-template-in-attract"></a>Een aanstellingsprocessjabloon maken in Attract

[!include [banner](includes/banner.md)]

Een *aanstellingsprocessjabloon* bevat alle activiteiten die moeten worden opgenomen als onderdeel van het aanstellingsproces voor een functie. In dit onderwerp worden de elementen van een processjabloon in Microsoft Dynamics 365 Talent: Attract beschreven. Ook wordt uitgelegd hoe u een sjabloon maakt.

> [!NOTE]
> Sjabloon maken maakt deel uit van de Uitgebreide invoegtoepassing voor aanstellingen voor Attract.

## <a name="template-management"></a>Sjabloonbeheer

Organisaties kunnen beslissen of teamleden of alleen beheerders processjablonen kunnen maken in Attract. Als u sjabloonbeheer wilt configureren, gaat u naar **Beheercentrum** \> **Sjabloonbeheer**. Als u teamleden hun eigen sjablonen wilt laten maken, schakelt u sjabloonbeheer in. Als u sjabloonbeheer niet inschakelt, kunnen alleen beheerders sjablonen maken.

## <a name="default-template"></a>Standaardsjabloon

Alleen beheerders kunnen de standaardsjabloon instellen. De standaardsjabloon wordt gebruikt als geen sjabloon is geselecteerd wanneer een functie wordt gemaakt. Als u de standaardsjabloon wilt instellen, gaat u naar **Beheercentrum** \> **Sjabloonbeheer**. Op de kaart voor de sjabloon die de standaardsjabloon worden moet, selecteert u de ellipsisknop (**...**) en selecteert u vervolgens **Als standaard instellen**.

## <a name="create-a-process-template"></a>Een processjabloon maken

Beheerders, wervers en aanstellend managers kunnen processjablonen maken. Een processjabloon bestaat uit *fasen* en *activiteiten*. Fasen groeperen een of meer activiteiten. Standaard heeft elke processjabloon Prospect-, Sollicitatie- en Aanbiedingsactiviteiten. De fasen die deze activiteiten bevatten, kunnen worden hernoemd. U kunt meer fasen toevoegen door **+ Nieuwe fase** te selecteren. U kunt activiteiten aan een fase toevoegen door ze naar de juiste fase te slepen of door erop te dubbelklikken in de activiteitenlijst.

> [!NOTE]
> Fasenamen zijn zichtbaar voor kandidaten op de pagina **Sollicitatiestatus**. U moet dit feit overwegen wanneer u namen voor fasen kiest.

Zie voor meer informatie over activiteiten, [Activiteiten in aanstellingsprocessen](./activities-attract.md).

Volg deze stappen om een aanstellingsprocessjabloon te maken.

1. Ga naar **Sjablonen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Sjabloonnaam** een naam in voor de sjabloon en selecteer **Maken**.
4. Selecteer in de lijst **Het goedkeuringsproces kiezen** de optie **Standaard** om goedkeuring te vereisen voor een functie.
5. Selecteer of u prospects inschakelt of uitschakelt.
6. Optioneel: voeg fasen toe of verwijder fasen.

    - Als u een fase wilt toevoegen, selecteert u **+ Nieuwe fase**.
    - Als u een fase wilt verwijderen, plaatst u de aanwijzer boven de fase en selecteert u vervolgens de prullenbakknop die wordt weergegeven.

        > [!NOTE]
        > De fasen Prospect, Sollicitatie en Aanbieding kunnen niet worden verwijderd, maar ze kunnen wel worden hernoemd.

7. Optioneel: voeg activiteiten toe of verwijder activiteiten.

    - Als u een activiteit wilt toevoegen, sleept u deze van de activiteitenlijst aan de rechterkant naar de gewenste fase. Of dubbelklik op de activiteit en selecteer vervolgens de fase waaraan u deze wilt toevoegen.
    - Als u een activiteit wilt verwijderen, vouwt u deze uit en selecteert u de prullenbakknop in de koptekst van de activiteit.

8. Selecteer **Opslaan**.
