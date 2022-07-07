---
title: Een adres aan een serviceorder toevoegen
description: In dit artikel wordt beschreven hoe u een klantadres aan de serviceorder toevoegt.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015720"
---
# <a name="add-an-address-to-a-service-order"></a>Een adres aan een serviceorder toevoegen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een klantadres aan de serviceorder toevoegt. Wanneer u een serviceorder maakt, worden de adresgegevens overgedragen vanuit het project waaraan de serviceorder is gekoppeld. U kunt echter een alternatieve locatie uit adressen selecteren die al in Microsoft Dynamics AX voor klanten, leveranciers, locaties, magazijnen, serviceorders en projecten worden ingevoerd.

U kunt ook nieuw adres maken. Standaard, wordt het nieuwe adres naar het project overgeboekt. Echter, u kunt opgeven dat het nieuwe adres alleen voor dit exemplaar van de service relevant is. Als u dit doet, wordt het nieuwe adres niet naar het project overgeboekt.

## <a name="create-a-customer-address-for-a-service-order"></a>Maak een klantadres voor een serviceorder

Om een adres aan een serviceorder toe te voegen, volgt u deze stappen:

1. Ga naar **Servicebeheer** \> **Serviceorders** \> **Serviceorders**.

1. Open de serviceorder waarvoor u een adres wilt maken.

1. Open het tabblad **Koptekst**.

1. Vouw het sneltabblad **Adres** uit en selecteer vervolgens **Adres toevoegen** op de werkbalk.

1. Voer in het dialoogvenster **Nieuw adres** een unieke naam voor het adres in en vul de resterende velden verder in. 

    > [!WARNING]
    > Als u dezelfde naam als een bestaand adres invoert, zal de informatie die u in de resterende velden invoert informatie voor het bestaande adres overschrijven.

1. Selecteer **OK** om het nieuwe adres naar de serviceorder te kopiëren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Een alternatief adres opgeven op een serviceorder

Om een alternatief adres aan een serviceorder toe te voegen, volgt u deze stappen:

1. Ga naar **Servicebeheer** \> **Serviceorders** \> **Serviceorders**.

1. Open de serviceorder waarvoor u een alternatief adres wilt invoeren.

1. Open het tabblad **Koptekst**.

1. Vouw het sneltabblad **Adres** uit en selecteer vervolgens **Ander adres** op de werkbalk.

1. In het dialoogvenster **Adresselectie** selecteert u **Serviceorders** in de vervolgkeuzelijst boven het raster.

1. Selecteer een adres en **OK** om het naar de serviceorder te kopiëren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]