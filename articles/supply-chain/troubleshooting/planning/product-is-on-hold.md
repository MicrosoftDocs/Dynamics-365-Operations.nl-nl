---
title: Product staat in wachtstand voor transacties
description: Wanneer u planningsorders hebt gefiatteerd, ontvangt u een foutbericht dat een artikel in de wachtstand staat voor transacties.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752605"
---
# <a name="product-is-on-hold-for-transactions"></a>Product staat in wachtstand voor transacties

Foutcode: SYS13295

## <a name="symptoms"></a>Symptomen

Wanneer u geplande orders hebt gefiateerd, wordt het volgende foutbericht weergegeven:

> Artikel %1 is geblokkeerd voor transacties in %2.

## <a name="cause"></a>Oorzaak

Wanneer geblokkeerde artikelen worden beschreven, worden de termen *geblokkeerd*, *gestopt* en *in wachtstand* door elkaar gebruikt. Dit betekent dat het artikel is ingesteld op **Gestopt** in de standaardorderinstellingen.

Als een artikel is geblokkeerd en u voegt het toe aan een inkoop- of verkooporderregel, ontvangt u een waarschuwingsbericht. Als een artikel is geblokkeerd, kunnen voorraadtransacties die zijn gerelateerd aan de inkooporder- of verkooporderregel niet worden gewijzigd, bijvoorbeeld als u een pakbon of factuur boekt. U kunt een ingekocht artikel blokkeren en het artikel tegelijkertijd verkopen. In dit geval is het selectievakje **Gestopt** ingeschakeld op een inkooporder. Het artikel is echter niet geblokkeerd in voorraad of op een verkooporder.

Hieronder staan enkele voorwaarden die ertoe leiden dat een artikelnummer kan worden geblokkeerd voor verkoop:

- Het artikel wordt nog ontwikkeld of gemaakt. Daarom wilt u niet dat het wordt verkocht of gereserveerd.
- U hebt een groot aantal defecte artikelen ontvangen en de defecten moeten worden gecorrigeerd voordat het artikel kan worden verkocht.

U kunt in dit soort gevallen het artikel blokkeren totdat het probleem is opgelost.

Als een artikel is geblokkeerd en u een retourorderregel maakt, ontvangt u een bericht. U kunt niet een reeks of partij van een artikel blokkeren. Als onderdelen van een artikel moeten worden geblokkeerd, kunt u dit doen door voorraad te verplaatsen of de volledige voorraad van het artikel voor de desbetreffende periode te blokkeren.

## <a name="resolution"></a>Oplossing

- Open de pagina **Standaardorderinstellingen** voor het artikel en schakel het selectievakje **Gestopt** uit.
