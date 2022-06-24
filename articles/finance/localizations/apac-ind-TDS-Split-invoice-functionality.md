---
title: Functionaliteit voor factuursplitsing
description: In dit artikel worden de instellingen en functies beschreven voor het splitsen van facturen op afleveradres en belastingrekeningnummer (TAN).
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
ms.openlocfilehash: 7bbeb94429c2c69b7b8ea3089390db676a021b80
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874427"
---
# <a name="split-invoice-functionality"></a>Functionaliteit voor factuursplitsing

[!include [banner](../includes/banner.md)]

In dit artikel worden de instellingen en functies beschreven voor het splitsen van facturen op afleveradres en belastingrekeningnummer (TAN).

Schakel op de pagina **Parameters van module Leveranciers** op het tabblad **Algemeen** het selectievakje **Productontvangstbon** of **Factuur** in om een productontvangstbon of factuur met verschillende afleveradressen en belastingrekeningnummers op de pagina **Inkooporder** te boeken en te splitsen. De geboekte factuur wordt dan opgesplitst per afleveradres en belastingrekeningnummer.

Stel op het tabblad **Overzicht bijwerken** op het sneltabblad **Splitsen op basis van** in de rij **Leveringsgegevens** de optie **Bevestiging**, **Orderverzamellijst**, **Pakbon** of **Factuur** op **Ja** in om een bevestiging, orderverzamellijst, pakbon of factuur te maken waar verschillende afleveradressen en belastingrekeningnummers zijn gedefinieerd voor verschillende factuurregels op de pagina **Verkooporder**. De factuur wordt dan eerst gesplitst op afleveradres en vervolgens op belastingrekeningnummer.

> [!IMPORTANT]
> - Als er geen opties voor **Leveringsgegevens** zijn ingesteld op **Ja**, wordt de factuur als één factuur geboekt. Er vindt geen factuursplitsing plaats.
> - Als u een pakbon wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen en belastingrekeningnummers hebben, moet u de optie **Pakbon** voor **Leveringsgegevens** instellen op **Ja**.
> - Als u een factuur wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen en belastingrekeningnummers hebben, moet u de optie **Factuur** voor **Leveringsgegevens** instellen op **Ja**.
> - Als u een factuur wilt splitsen en boeken waarbij de factuurregels verschillende afleveradressen maar hetzelfde belastingrekeningnummer hebben, moet u de optie **Factuur** voor **Leveringsgegevens** instellen op **Nee**. De factuur wordt dan gesplitst op afleveradres.

## <a name="example"></a>Voorbeeld

In dit voorbeeld is de optie **Factuur** voor **Leveringsgegevens** ingesteld op **Ja** op het tabblad **Overzicht bijwerken** van de pagina **Parameters van module Leveranciers**. Er wordt een inkoopfactuur geboekt die de volgende instellingen heeft voor afleveradressen en belastingrekeningnummers op de regels:

- **Artikelregel 1:** Afleveradres 1, TAN-ABCD12345A
- **Artikelregel 2:** Afleveradres 1, TAN-ABCD12345A
- **Artikelregel 3:** Afleveradres 2, TAN-ABCE12345B
- **Artikelregel 4:** Afleveradres 3, TAN-ABCD12345A

In dit geval wordt de oorspronkelijke factuur in twee facturen gesplitst en op de volgende manier geboekt:

- Factuur 1 wordt geboekt voor artikelregel 1 en artikelregel 2, omdat beide regels hetzelfde afleveradres en belastingrekeningnummer hebben.
- Factuur 2 wordt geboekt voor artikelregel 3.
- Factuur 3 wordt geboekt voor artikelregel 4.
