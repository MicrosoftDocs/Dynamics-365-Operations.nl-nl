---
title: TDS-berekening op facturen
description: Dit artikel biedt een verwijzing voor transacties waarbij de TDS (belasting ingehouden op bron) wordt berekend op factuurniveau.
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
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855358"
---
# <a name="tds-calculation-on-invoices"></a>TDS-berekening op facturen

[!include [banner](../includes/banner.md)]

Dit artikel biedt een verwijzing voor transacties waarbij de TDS (belasting ingehouden op bron) wordt berekend op factuurniveau.

| Serienummer | Transactietype                                 | Transactiebedrag | Paginanaam en selectiepad                                 | Rekeningtype en type tegenrekening                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | Inkoop die is gedaan van leverancier/registratie van onkosten   | Debet of Credit  | Pagina Algemene journalen (Grootboek > Journaalposten > Algemene journalen), pagina Factuurgoedkeuringsjournaal (Leveranciers > Facturen > Factuurgoedkeuring), pagina Facturenjournaal (Leveranciers > Facturen > Factuurjournaal) | Grootboek (debet), leverancier (credit)  Bronbelasting wordt alleen berekend voor de combinatie Leverancier-grootboek als de grootboekrekening het boekingstype **Contant** **inkopen** heeft. |
| 2.            | Inkoop die is gedaan van klant/registratie van onkosten | Debet of Credit  | De pagina Algemene journalen (Grootboek > Journaalposten > Algemene journalen), pagina Facturenjournaal (Leveranciers > Facturen > Facturenjournaal) | Grootboek (debet), klant (credit)                                 |
| 3.            | Inkoop van vast activum van leverancier              | Debet of Credit  | Pagina Algemene journalen (Grootboek > Journaalposten > Algemene journalen), pagina Facturenregisterjournaal (Leveranciers > Facturen > Factuurregister), pagina Facturenjournaal (Leveranciers > Facturen > Factuurjournaal) | Vaste activa (debet), leverancier (credit)                             |
| 4.            | Inkoop van vast activum van klant            | Debet of Credit  | De pagina Algemene journalen (Grootboek > Journaalposten > Algemene journalen), pagina Facturenjournaal (Leveranciers > Facturen > Facturenjournaal) | Vaste activa (debet), klant (credit)                           |
| 5.            | Inkoopfactuur (TDS te betalen)                  |                    | Pagina Inkooporder (Leveranciers > Inkooporders > Alle inkooporders) |                                                              |
| 6.            | Verkoopfactuur (TDS te ontvangen)                  |                    | Verkooporderpagina (Klanten > Orders > Alle verkooporders), pagina Vrije-tekstfactuur (Klanten > Facturen > Alle vrije-tekstfacturen) |                                                              |
