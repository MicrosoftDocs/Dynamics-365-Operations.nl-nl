---
title: Service-intervallen
description: In dit onderwerp wordt beschreven hoe u met service-intervallen werkt. Met serviceovereenkomstintervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u automatisch serviceorders maakt.
author: sorenva
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df15340a82bf36f67baa7195e2e318a4216d2c56
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675622"
---
# <a name="service-intervals"></a>Service-intervallen

[!include [banner](../includes/banner.md)]

Met serviceovereenkomstintervallen wordt aangegeven hoe vaak er serviceorderregels voor serviceovereenkomstregels worden gemaakt wanneer u automatisch serviceorders maakt.

Wanneer serviceorders automatisch worden gemaakt, worden serviceorderregels gemaakt vanaf de begindatum van de overeenkomstregel volgens het interval dat u voor de serviceovereenkomstregel hebt opgegeven.

Als het veld **Interval** van een serviceovereenkomstregel op de pagina **Serviceovereenkomsten** leeg is, gaat het om een eenmalige gebeurtenis en wordt de regel niet gebruikt om steeds opnieuw serviceorders te maken.

## <a name="example"></a>Voorbeeld

Dit voorbeeld illustreert de invloed van een service-interval op serviceovereenkomstregels en die van serviceorderregels op een serviceorder.

### <a name="create-a-service-agreement"></a>Een serviceovereenkomst maken

U maakt eerst een serviceovereenkomst en stelt de optie **Serviceorders combineren** in op **Per serviceovereenkomst**.

1. Klik op **Serviceovereenkomsten**.
2. Klik in het **actievenster** op het tabblad **Serviceovereenkomst** in de groep **Nieuw** op **Serviceovereenkomst** om een nieuwe serviceovereenkomst te maken.
3. Voer een beschrijving in, selecteer een project in het veld **Project-id** en voer een datum in het veld **Begindatum** in.
4. In het veld **Serviceorders combineren** selecteert u **Per serviceovereenkomst**.

U hebt nu de volgende serviceovereenkomst gemaakt:

| Project      | Begindatum                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Uw project | De datum die u voor het project hebt opgegeven. In dit voorbeeld wordt de huidige datum gebruikt. |

### <a name="create-a-service-agreement-line"></a>Een serviceovereenkomstregel maken

Vervolgens maakt u een serviceovereenkomstregel die het transactietype **Uur** heeft.

U voltooit dit deel van het voorbeeld door op de pagina **Service-intervallen** een service-interval van 10 dagen te maken. 

1. Selecteer de serviceovereenkomst die u zojuist hebt gemaakt. 
2. Ga naar het sneltabblad **Regels** en klik op de knop **Toevoegen** om een nieuwe regel te maken in het onderste deelvenster van de pagina **Serviceovereenkomsten**.
3. In het veld **Transactietype** selecteert u **Uur**.
4. Selecteer in het veld **Werknemer** de werknemer die de service zal verzorgen.
5. Selecteer het interval van 10 dagen in het veld **Service-interval**.

U hebt nu een serviceovereenkomstregel gemaakt met de volgende informatie:

| Transactietype | Begindatum                               | Dienstinterval |
|------------------|------------------------------------------|------------------|
| Uur             | De huidige datum.                        | Om de 10 dagen    |
| Werknemer           | De werknemer die de service uitvoert. |                  |

Er is geen tijdvenster voor de regel opgegeven. 

### <a name="create-planned-service-orders"></a>Geplande serviceorders maken

U kunt nu geplande serviceorders en serviceorderregels voor de volgende maand maken.

1. Klik op de pagina **Serviceovereenkomsten** in het **actievenster** op het tabblad **Leveren** op **Geplande serviceorders**.
2. Geef op de pagina **Serviceorders maken** de huidige datum in het veld **Begindatum** en een datum die één maand na de huidige datum ligt in het veld **Einddatum** op.
3. Stel de schuifregelaar **Uur** in op **Ja**. 
4. Klik tot slot op **OK**.

Omdat er geen groepering voor de serviceorder beschikbaar is (gedefinieerd via de optie **Per serviceovereenkomst** in het veld **Serviceorders combineren**), wordt voor elke serviceorder een serviceorderregel gemaakt.

### <a name="service-orders-created"></a>Gemaakte serviceorders

Er zijn drie serviceorderregels gemaakt binnen het tijdsbestek dat u hebt opgegeven in het dialoogvenster **Serviceorders maken**. U kunt de serviceorderregels bekijken op de pagina **Serviceovereenkomsten** (**actievenster** \> **Leveren** (tabblad) \>**Weergeven** (knop)).

## <a name="related-topics"></a>Verwante onderwerpen

[Service-intervallen instellen](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]