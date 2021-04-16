---
title: Een adres aan een serviceorder toevoegen
description: Dit onderwerp beschrijft hoe u een klantadres aan de serviceorder toe te voegen.
author: ShylaThompson
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a54ec439fc88dc9688bbb3d6b833b5d80482f024
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824649"
---
# <a name="add-an-address-to-a-service-order"></a>Een adres aan een serviceorder toevoegen    

[!include [banner](../includes/banner.md)]


Dit onderwerp beschrijft hoe u een klantadres aan de serviceorder toe te voegen. Wanneer u een serviceorder maakt, worden de adresgegevens overgedragen vanuit het project waaraan de serviceorder is gekoppeld. U kunt echter een alternatieve locatie uit adressen selecteren die al in Microsoft Dynamics AX voor klanten, leveranciers, locaties, magazijnen, serviceorders en projecten worden ingevoerd.

U kunt ook nieuw adres maken. Standaard, wordt het nieuwe adres naar het project overgeboekt. Echter, u kunt opgeven dat het nieuwe adres alleen voor dit exemplaar van de service relevant is. Als u dit doet, wordt het nieuwe adres niet naar het project overgeboekt.

## <a name="create-a-customer-address-for-a-service-order"></a>Maak een klantadres voor een serviceorder

Om een adres aan een serviceorder toe te voegen, volgt u deze stappen:

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Open de serviceorder waarvoor u een adres wilt maken.

3.  Klik in het **Actievenster** op **Bewerken** en vervolgens op **Koptekstweergave**.

4.  Klik in het sneltabblad **Adres** op **Adres toevoegen**.

5.  Voer in het formulier **Nieuw adres** een unieke naam voor het adres in en vul de resterende velden verder in. 
    

    > [!WARNING]
    > <P>Als u dezelfde naam als een bestaand adres invoert, zal de informatie die u in de resterende velden invoert informatie voor het bestaande adres overschrijven.</P>


6.  Klik op **OK** om het nieuwe adres naar de serviceorder te kopiëren.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Een alternatief adres opgeven op een serviceorder

Om een alternatief adres aan een serviceorder toe te voegen, volgt u deze stappen:

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Open de serviceorder waarvoor u een alternatief adres wilt invoeren.

3.  Klik in het **Actievenster** op **Bewerken** en vervolgens op **Koptekstweergave**.

4.  Klik op het sneltabblad **Adres** op **Ander adres**.

5.  Selecteer in het formulier **Adresselectie** in het veld **Recordtype** **Serviceorders**.

6.  Selecteer een adres, en klik vervolgens op **OK** om het naar de serviceorder te kopiëren.


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]