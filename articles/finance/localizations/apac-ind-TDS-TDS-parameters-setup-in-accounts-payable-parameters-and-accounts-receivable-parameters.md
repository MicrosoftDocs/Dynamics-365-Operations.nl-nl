---
title: TDS-parameters voor Leveranciers en Klanten instellen
description: In dit artikel wordt uitgelegd hoe u parameters kunt instellen in Leveranciers en Klanten om TDS-inhoudingen (belasting ingehouden op bron) te ondersteunen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e547b92f9f7e0ccc5b92df4cd991ce402369b568
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883145"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>TDS-parameters voor Leveranciers en Klanten instellen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u parameters kunt instellen in Leveranciers en Klanten om TDS-inhoudingen (belasting ingehouden op bron) te ondersteunen.

1. Ga naar **Belasting \> Instellen \> Parameters \> Parameters van module Klanten**.
2. Selecteer **Orderregels bijwerken** op het tabblad **Updates** om het dialoogvenster **Orderregels bijwerken** te openen.
3. Geef in de sectie van de **TDS-groep** in het veld **TDS-groep bijwerken** de methode op die u wilt gebruiken om de TDS-groep bij te werken op regelniveau. Deze instelling wordt gebruikt wanneer de TDS-groep wordt bijgewerkt in een orderkoptekst. De volgende opties zijn beschikbaar:

    - **Nooit**: de TDS-groep wordt niet bijgewerkt op de orderregels wanneer deze wordt bijgewerkt in de orderkoptekst.
    - **Altijd**: de TDS-groep wordt automatisch bijgewerkt op de orderregels wanneer deze wordt bijgewerkt in de orderkoptekst.
    - **Vragen**: gebruikers ontvangen een bericht waarin ze worden gevraagd de TDS-groep op de orderregels bij te werken.
4. Selecteer **OK**.

    [![Dialoogvenster Orderregels bijwerken.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Ga naar **Belasting \> Instellen \> Parameters \> Parameters van module Leveranciers**.
6. Stel op het tabblad **Algemeen** op het sneltabblad **Splitsen op basis van aflevergegevens** de optie **Productontvangstbon** in op **Ja** om een productontvangstbon met verschillende afleveradressen en belastingrekeningnummers te boeken en te splitsen. Als deze optie is ingesteld op **Nee**, kunt u geen inkooppakbon met verschillende afleveradressen en belastingrekeningnummers boeken.
7. Stel de optie **Factuur** in op **Ja** om een inkoopfactuur met verschillende afleveradressen en belastingrekeningnummers te maken en te splitsen.

    [![Sneltabblad Splitsen op basis van aflevergegevens.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Sluit de pagina.
