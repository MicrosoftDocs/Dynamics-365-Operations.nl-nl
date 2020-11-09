---
title: Een vast activum maken
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe record voor vaste activa kunt maken op de lijstpagina Vaste activa.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000238"
---
# <a name="create-a-fixed-asset"></a>Een vast activum maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een nieuwe record voor vaste activa kunt maken op de lijstpagina **Vaste activa**.

Het activumnummer wordt toegewezen op basis van de nummerreeks die is toegewezen aan de groep met vaste activa. Als u de sjabloon voor vaste activa gebruikt om activa te importeren via de invoegtoepassing Microsoft Excel of als u een andere importtaak gebruikt, worden automatisch records voor vaste activa gemaakt en wordt het activanummer verhoogd.

Voer de volgende stappen uit om handmatig een activarecord te maken.

1. Ga naar **Navigatievenster \> Modules \> Vaste activa \> Vaste activa \> Vaste activa**.
2. Selecteer **Nieuw** in het **Actievenster**.
3. Typ of selecteer een waarde in het veld **Groep vaste activa**. Het veld **Nummer** wordt standaard ingevuld als u de functionaliteit **Vaste activa automatisch nummeren** in de parameters **Vaste activa** en de **vaste-activagroep** hebt ingeschakeld. Zo niet, dan moet u een uniek nummer invoeren om het vaste activum te identificeren.
4. Voer een waarde in het veld **Naam** in. Voer aanvullende informatie in die uw bedrijf voor dit activum nodig heeft.
5. Selecteer **Boeken** in het **Actievenster**.
6. Voer in het veld **Verwervingsdatum** een datum in.
7. Voer een nummer in het veld **Aanschafprijs** in.

    - Voer aanvullende informatie in die uw bedrijf voor dit boek nodig heeft.
    - Voer aanvullende informatie in die uw bedrijf voor de resterende boeken nodig heeft.

8. Sluit de pagina.

U kunt vaste activa ook importeren met de Excel-invoegtoepassing of door een importtaak uit te voeren vanuit de werkruimte **Gegevensbeheer**. Voer voordat u de import uitvoert de waarden voor vereiste velden in de sjabloon in.

Als u het nummer van de vaste activa niet hebt gedefinieerd in de sjabloon van de Excel-invoegtoepassing of in Gegevensbeheer, wordt een nummer voor vaste activa gemaakt voor elk geïmporteerd activum en wordt de nummerreeks voor elk geïmporteerd activum automatisch verhoogd. Als u echter activa importeert en activanummers definieert in de sjabloon, wordt de nummerreeks **niet** automatisch verhoogd. In dit geval moet een beheerder de nummerreeks mogelijk handmatig bijwerken. Als u het nummer voor vaste activa in de sjabloon van de Excel-invoegtoepassing hebt gedefinieerd, wordt het gedefinieerde nummer voor vaste activa gebruikt en wordt de nummerreeks verhoogd.
