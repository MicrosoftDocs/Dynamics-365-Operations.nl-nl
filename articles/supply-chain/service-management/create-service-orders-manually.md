---
title: Handmatig serviceorders maken
description: U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fbcdaa50a8f13247c13c1885cdb4ab7f5f39a47
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "310916"
---
# <a name="create-service-orders-manually"></a>Handmatig serviceorders maken    

[!include [banner](../includes/banner.md)]


U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken. U kunt ook een serviceorder vanuit een project maken.

> [!TIP]
> <P>U kunt geautomatiseerde processen gebruiken om serviceorders te maken. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Handmatig een serviceorder maken vanuit een serviceovereenkomst

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer een serviceovereenkomst of maak een nieuwe serviceovereenkomst.

3.  Klik op het tabblad **Leveren** en in de groep **Maken** op **Geplande serviceorders** om het formulier **Serviceorders maken** te openen.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Handmatig een serviceorder maken in het formulier Serviceorders

1.  Klik op **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Druk op Ctrl+N om een nieuwe serviceorder te maken.

3.  Maak serviceorderregels voor de serviceorder.

> [!NOTE]
> <P>Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen. Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</P>

## <a name="create-a-service-order-from-a-project"></a>Een serviceorder vanuit een project maken

1.  Klik op **Projectbeheer en boekhouding** \> **Algemeen** \> **Projecten** \> **Alle projecten**.

2.  Klik in het formulier **Projecten** in het **Actievenster** op het tabblad **Beheren** \> op **Service** \> **Serviceorders**.

3.  Volg de vorige procedure voor het handmatig maken van een serviceorder in het formulier **Serviceorders**. In het veld **Project-ID** wordt de projectverwijzing weergegeven.

> [!NOTE]
> <P>Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen. Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Een serviceorder maken op basis van het formulier Verkooporder

U kunt een serviceorder maken in het formulier **Verkooporders** met behulp van de wizard **Een nieuwe serviceorder maken op basis van de verkooporder**.

1.  Klik op **Verkoop en marketing** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**.

2.  Open de relevante verkooporder.

3.  Klik op het tabblad **Verkooporder** op **Serviceorder** om de wizard **Een nieuwe serviceorder maken op basis van de verkooporder** te starten.

4.  Klik op **Volgende \>** en voltooi de volgende stappen op de pagina **Overeenkomst selecteren voor serviceorder**:
    
      - Gebruik het veld **Serviceovereenkomst** om de serviceovereenkomst te selecteren waaraan de nieuwe serviceorder moet worden gekoppeld.
    
      - Optioneel: gebruik het veld **Project-ID** om deze serviceorder te koppelen aan een bepaald project.

5.  Klik op **Volgende \>** en voltooi de volgende stappen op de pagina **Serviceorder maken**:
    
      - Geef in het veld **Voorkeurstijd service** een datum en een tijd op waarop u wilt dat het serviceverzoek begint.
    
      - Optioneel: wijzig de tekst in het veld **Beschrijving**. Dit veld bevat standaard de omschrijving van de serviceovereenkomst die u hebt geselecteerd op de vorige pagina.
    
      - Selecteer in het veld **Verantwoordelijk** de ID van de werknemer die verantwoordelijk is voor de overeenkomst en voer, als u dit weet, de ID van de voorkeurstechnicus van de klant in voor het serviceverzoek.
    
      - Selecteer in het veld **Contact-ID** de persoon in het bedrijf van de klant met wie contact moet worden opgenomen over de serviceorder.

6.  Klik op **Volgende\>** en klik vervolgens op **Voltooien**.


## <a name="see-also"></a>Zie ook

[Serviceorders](service-orders.md)

[Automatisch serviceorders maken](create-service-orders-automatically.md)

[Serviceorders maken (klasseformulier)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\)) 

