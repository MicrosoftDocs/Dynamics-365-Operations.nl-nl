---
title: Deelleveringen van geretourneerde artikelen ontvangen
description: Gedeeltelijke leveringen worden gedefinieerd aan de hand van retourorderregels en niet aan de hand van retourorderleveringen.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf35169d8afd6e88b8ebe921514ed6d55607a4dd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975723"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>Deelleveringen van geretourneerde artikelen ontvangen    

[!include [banner](../includes/banner.md)]


Gedeeltelijke leveringen worden gedefinieerd aan de hand van retourorderregels en niet aan de hand van retourorderleveringen.

Dit betekent dat wanneer u de volledige hoeveelheid ontvangt die is aangegeven op één retourorderregel, maar u niets van de andere regels in de retourorder ontvangt, de levering geen gedeeltelijke levering is. Als echter voor een retourorderregel bijvoorbeeld tien eenheden van een bepaald artikel moeten worden geretourneerd en u maar vier eenheden ontvangt, is dit een gedeeltelijke levering.

Als een retourzending minder bevat dan de volledige hoeveelheid van een retourorderregel, kunt u wachten totdat u de rest van de te retourneren hoeveelheid ontvangt of u kunt de gedeeltelijke hoeveelheid registreren en boeken.

## <a name="register-and-post-a-partial-quantity"></a>Een gedeeltelijke hoeveelheid registreren en boeken

1.  Nadat u een retourorder voor aankomst in het formulier **Aankomstoverzicht - Magazijn: %1, Dok: %2, Journaalnaam: %3** hebt geselecteerd, klikt u op **Begin aankomst** om het aankomstjournaal te maken en klikt u vervolgens op **Journalen** \> **Aankomsten van ontvangsten tonen** om het formulier **Locatiejournaal** te openen.

2.  Selecteer de regel van het journaal waarmee u wilt werken en klik op **Regels** om het formulier **Journaalregels, locaties** te openen.

3.  Selecteer de regel van het artikelnummer waarvoor slechts een gedeeltelijke hoeveelheid is gearriveerd en klik op **Functies** \> **Splitsen** om het formulier **Splitsen** te openen.

4.  Voer in het veld **Gesplitste hoeveelheid** de hoeveelheid in voor het totaal aantal artikelen dat is ontvangen en klik op **OK**.

5.  Selecteer in het formulier **Journaalregels, locaties** de regel voor de hoeveelheid artikelen die is ontvangen en klik op **Boeken**. U kunt de regel voor de extra hoeveelheid boeken nadat de artikelen zijn ontvangen.




