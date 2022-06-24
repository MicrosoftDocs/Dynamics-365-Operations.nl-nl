---
title: Het kortetermijngedeelte van een leaseverplichting opnieuw classificeren
description: In dit artikel wordt uitgelegd hoe u een maandelijkse journaalboeking maakt om een gedeelte van de leaseverplichting opnieuw te classificeren als korte termijn.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886337"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Het kortetermijngedeelte van een leaseverplichting opnieuw classificeren

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een maandelijkse journaalboeking maakt om een gedeelte van de leaseverplichting opnieuw te classificeren als korte termijn. Wanneer het schema dat is geselecteerd in het batchproces **Herclassificatie kortlopende leaseverplichtingen** is, wordt er een journaalboeking gemaakt. Deze invoer wordt gebruikt om het huidige gedeelte van de leaseverplichtingen te boeken op de laatste dag van de maand. Tegelijkertijd wordt een omkeerregel geboekt vanaf de eerste dag van de volgende maand.

Het kortetermijngedeelte van de leaseverplichting wordt vermeld in het aflossingsschema voor de passiva. Wanneer de journaalboeking wordt geboekt, wordt de kolom **Journaal voor herclassificatie van verplichtingen gemaakt** beschikbaar en wordt de journaal-id ook in de planning ingevuld.

Voer de volgende stappen uit om de journaalboeking voor herclassificatie van kortlopende verplichtingen te maken en te boeken.

1. Ga naar **Activa leasen \> Periodiek \> Batchjournaal maken**.
2. Selecteer in het dialoogvenster **Batchjournaal maken** in het veld **Schema selecteren** en selecteer **Herclassificatie kortlopende leaseverplichtingen**.
3. Selecteer een leasegroep in het veld **Leasegroep**. U kunt ook in het veld **Boek-id** de boek-id selecteren.
4. Schakel de parameter **Boeken** in. Indien de invoer moet worden gemaakt, maar niet worden geboekt, dient u deze parameter uit te schakelen.
5. Selecteer **OK**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
