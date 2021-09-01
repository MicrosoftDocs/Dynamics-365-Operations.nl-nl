---
title: Boekingsrekeningen verwerving vaste activa
description: In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het aanchaffen van activa.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6f2e87404fb7ae6439c2e04dc2ca5e369a58d87ba7743252586620111cfa6ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714467"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a>Boekingsrekeningen verwerving vaste activa

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het aanchaffen van activa.

Rekeningen voor het boeken van verwervingen van vaste activa kunnen verschillen afhankelijk van de methode die wordt gebruikt om het activum te verwerven. Selecteer Verwerving en Verwervingscorrectie op de pagina Boekingsprofielen voor vaste activa op het tabblad Grootboekrekeningen vaste-activarekeningen in te stellen om naar het grootboek te boeken. 

In journalen en op inkooporders is het grootboek gewoonlijk de balansrekening waar de aanschafwaarde van het nieuwe vaste activum wordt gedebiteerd. Deze rekening wordt niet weergegeven in het journaal en kan niet worden vervangen in transacties. 

Tegenrekening is ook een balansrekening. In het algemene journaal en in het vaste-activajournaal is deze rekening vaak de bankrekening die wordt gebruikt om te betalen voor de aanschaf van het activum. De tegenrekening is een standaardrekening, die wordt voorgesteld in de journalen. Deze kan in het journaal worden gewijzigd naar een andere rekening uit het rekeningschema of naar een leveranciersrekening, als het vaste activum van een leverancier is gekocht. 

Als Factuurjournaal of Inkooporders in Leveranciers worden gebruikt voor de verwerving van vaste activa, wordt de tegenrekening voor de vaste-activatransactie vervangen door de leveranciersrekening die voor de transactie is geselecteerd.

Voor verwervingen die zijn geboekt met het Voorraad naar vaste-activajournaal in het grootboek, is het vaste activum niet gekocht van externe bronnen, maar overgebracht uit de eigen voorraad van het bedrijf. Daarom is de tegenrekening een voorraaduitgifterekening voor het voorraadartikel in Voorraadbeheer.

Zie voor meer informatie [Verwerving van activa via inkoop](acquire-assets-procurement.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]