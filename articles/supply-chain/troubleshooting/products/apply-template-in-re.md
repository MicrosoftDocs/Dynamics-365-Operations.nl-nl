---
title: U kunt een sjabloon niet toepassen op een vrijgegeven product
description: U kunt een sjabloon niet toepassen op een vrijgegeven product.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026398"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a>U kunt een sjabloon niet toepassen om een vrijgegeven product te maken

KB-nummer: 4612097

## <a name="symptoms"></a>Symptomen

Wanneer u een nieuw vrijgegeven product maakt met behulp van het dialoogvenster **Nieuw vrijgegeven product**, kunt u een sjabloon selecteren. De sjabloon moet standaardinstellingen geven voor een groot aantal velden van het nieuwe vrijgegeven product. Sommige of alle velden worden echter niet ingesteld nadat u de sjabloon hebt geselecteerd.

## <a name="cause"></a>Oorzaak

Op veel pagina's in Microsoft Dynamics 365 Supply Chain Management kunt u een sjabloon maken die de begininstellingen vastlegt voor de records die op die pagina's worden weergegeven. U kunt een van deze sjablonen maken door **Recordinfo** te selecteren op het tabblad **Opties** van het actievenster. Vrijgegeven producten zijn echter veel complexer dan de meeste andere typen records. Hoewel u **Recordinfo** op de pagina **Vrijgegeven producten** kunt selecteren om een sjabloon te maken en hoewel u die sjabloon kunt selecteren wanneer u een vrijgegeven product maakt, levert de sjabloon niet de verwachte veldwaarden voor het nieuwe vrijgegeven product. U kunt daarom geen recordinfo-sjablonen gebruiken voor vrijgegeven producten. In plaats daarvan moet u specifieke productsjablonen maken.

## <a name="resolution"></a>Oplossing

Als u een productsjabloon wilt maken, gebruikt u het menu **Sjabloon** op het tabblad **Product** van het actievenster en niet de knop **Recordinfo** op het tabblad **Opties**.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer **Sjabloon** in het actievenster op het tabblad **Product** in de groep **Nieuw** en selecteer **Persoonlijke sjabloon maken** of een **Gedeelde sjabloon maken**.
