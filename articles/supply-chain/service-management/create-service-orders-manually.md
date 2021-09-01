---
title: Handmatig serviceorders maken
description: U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05c03cd07599c5ee2e739a785896888c8cfe8822e57529f7603783a2f011c97c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740642"
---
# <a name="create-service-orders-manually"></a>Handmatig serviceorders maken    

[!include [banner](../includes/banner.md)]


U kunt handmatig serviceorders maken door een serviceovereenkomst te gebruiken of door het formulier **Serviceorders** te gebruiken. U kunt ook een serviceorder vanuit een project maken.

> [!TIP]
> <P>U kunt geautomatiseerde processen gebruiken om serviceorders te maken. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Handmatig een serviceorder maken vanuit een serviceovereenkomst

1.  Selecteer **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.

2.  Selecteer een serviceovereenkomst of maak een nieuwe serviceovereenkomst.

3.  Selecteer het tabblad **Leveren** en selecteer in de groep **Maken** de optie **Geplande serviceorders** om het formulier **Serviceorders maken** te openen.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Handmatig een serviceorder maken in het formulier Serviceorders

1.  Selecteer **Servicebeheer** \> **Algemeen** \> **Serviceorders** \> **Serviceorders**.

2.  Selecteer **Nieuw** om een nieuwe serviceorder te maken.

3.  Maak serviceorderregels voor de serviceorder.

> [!NOTE]
> <P>Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen. Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</P>

## <a name="create-a-service-order-from-a-project"></a>Een serviceorder vanuit een project maken

1.  Ga naar **Projectbeheer en boekhouding** \> **Algemeen** \> **Projecten** \> **Alle projecten**.

2.  Selecteer in het formulier **Projecten** in het **actiedeelvenster** op het tabblad **Beheren** \> de optie **Service** \> **Serviceorders**.

3.  Volg de vorige procedure voor het handmatig maken van een serviceorder in het formulier **Serviceorders**. In het veld **Project-ID** wordt de projectverwijzing weergegeven.

> [!NOTE]
> <P>Als het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is ingeschakeld, kunt u de transacties vanuit de serviceorderregels boeken zonder de serviceorder aan een serviceovereenkomst te koppelen. Als het selectievakje is uitgeschakeld, moet u de handmatig gemaakte serviceorder aan een project koppelen voordat u de serviceorderregels boekt.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Een serviceorder maken op basis van het formulier Verkooporder

U kunt een serviceorder maken in het formulier **Verkooporders** met behulp van de wizard **Een nieuwe serviceorder maken op basis van de verkooporder**.

1.  Ga naar **Verkoop en marketing** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**.

2.  Open de relevante verkooporder.

3.  Selecteer op het tabblad **Verkooporder** de optie **Serviceorder** om de wizard **Een nieuwe serviceorder maken op basis van de verkooporder** te starten.

4.  Selecteer **Volgende \>** en voltooi de volgende stappen op de pagina **Overeenkomst selecteren voor serviceorder**:
    
      - Gebruik het veld **Serviceovereenkomst** om de serviceovereenkomst te selecteren waaraan de nieuwe serviceorder moet worden gekoppeld.
    
      - Optioneel: gebruik het veld **Project-ID** om deze serviceorder te koppelen aan een bepaald project.

5.  Selecteer **Volgende \>** en voltooi de volgende stappen op de pagina **Serviceorder maken**:
    
      - Geef in het veld **Voorkeurstijd service** een datum en een tijd op waarop u wilt dat het serviceverzoek begint.
    
      - Optioneel: wijzig de tekst in het veld **Beschrijving**. Dit veld bevat standaard de omschrijving van de serviceovereenkomst die u hebt geselecteerd op de vorige pagina.
    
      - Selecteer in het veld **Verantwoordelijk** de ID van de werknemer die verantwoordelijk is voor de overeenkomst en voer, als u dit weet, de ID van de voorkeurstechnicus van de klant in voor het serviceverzoek.
    
      - Selecteer in het veld **Contact-ID** de persoon in het bedrijf van de klant met wie contact moet worden opgenomen over de serviceorder.

6.  Selecteer **Volgende \>** en **Voltooien**.


## <a name="see-also"></a>Zie ook

[Serviceorders](service-orders.md)

[Automatisch serviceorders maken](create-service-orders-automatically.md)

[Serviceorders maken (klasseformulier)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]