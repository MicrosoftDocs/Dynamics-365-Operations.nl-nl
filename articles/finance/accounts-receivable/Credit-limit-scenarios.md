---
title: Scenario´s voor kredietlimieten
description: In dit artikel wordt beschreven hoe de kredietlimiet van de klant wordt gecontroleerd wanneer de klant tot een kredietlimietgroep voor klanten behoort.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130253"
---
# <a name="credit-limit-scenarios"></a>Scenario´s voor kredietlimieten

In Kredietbeheer kan een kredietlimiet worden toegewezen aan klanten op klantniveau. Elke klant kan worden toegewezen aan een *kredietlimietgroep voor klanten* en elke groep heeft een kredietlimiet. Daarom kan een kredietlimiet ook worden toegewezen aan klanten op groepsniveau. Alle klanten die aan dezelfde klantkredietgroep zijn toegewezen, hebben dezelfde kredietlimiet.

In het algemeen worden groepskredietlimieten vóór afzonderlijke kredietlimieten gecontroleerd. De afzonderlijke kredietlimiet overschrijft niet altijd de groepskredietlimiet.

In dit artikel worden vijf scenario's beschreven die betrekking hebben op klantkredietgroepen en afzonderlijke kredietlimieten.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>De groepskredietlimiet voor klanten is meer dan de afzonderlijke kredietlimiet.

De klant heeft bijvoorbeeld een afzonderlijk kredietlimiet van € 10.000. De klant wordt aan een klantkredietgroep toegewezen en de groepskredietlimiet is € 15.000. In dit geval is de "effectieve kredietlimiet" van de klant € 10.000, omdat dat bedrag lager is dan de groepslimiet. Met blokkeringsregels wordt eerst de groepslimiet gecontroleerd. Vervolgens wordt de afzonderlijke limiet gecontroleerd. Alle verkooporders van meer dan € 10.000 worden geblokkeerd.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>De afzonderlijke kredietlimiet is meer dan de groepskredietlimiet voor klanten.

De klant heeft bijvoorbeeld een afzonderlijk kredietlimiet van € 20.000. De klant wordt aan een klantkredietgroep toegewezen en de groepskredietlimiet is € 15.000. In dit geval is de "effectieve kredietlimiet" van de klant € 15.000, omdat de groepslimiet altijd eerst wordt gecontroleerd met de blokkeringsregels. Alle verkooporders van meer dan € 15.000 worden geblokkeerd.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>De afzonderlijke kredietlimiet is ingesteld op 0,00 en de Verplichte kredietlimiet is ingesteld op Ja

Als de klant een afzonderlijke kredietlimiet heeft die is ingesteld op **0,00** en de optie **Verplichte kredietlimiet** is ingesteld op **Ja**, is de effectieve kredietlimiet van de klant € 0,00, zelfs als de klant aan een klantkredietgroep is toegewezen. Op deze manier kan de klant deel uitmaken van een groep, maar gaan alle orders naar Kredietbeheer.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>De afzonderlijke kredietlimiet is ingesteld op 0,00 en Onbeperkte kredietlimiet is ingesteld op Ja

Als de klant een afzonderlijke kredietlimiet heeft die is ingesteld op **0,00**, maar de optie **Onbeperkte kredietlimiet** is ingesteld op **Ja**, heeft de klant onbeperkt krediet, zelfs als de klant aan een klantkredietgroep is toegewezen.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>De afzonderlijke kredietlimiet is ingesteld op € 0,00 en de klant maakt deel uit van een klantkredietgroep.

De klant heeft bijvoorbeeld een afzonderlijke kredietlimiet die is ingesteld op **0,00**, de optie **Onbeperkt krediet** is ingesteld op **Nee** en de optie **Verplichte kredietlimiet** is ingesteld op **Nee**. De klant wordt aan een klantkredietgroep toegewezen en de groepskredietlimiet is € 15.000. In dit geval is de effectieve kredietlimiet van de klant de limiet van de groep, € 15.000. Verkooporders boven dit bedrag worden daarom geblokkeerd. Hierdoor kan de kredietlimiet worden beheerd op kredietgroepsniveau van de klant in plaats van op afzonderlijk klantniveau. Alle klanten die aan dezelfde groep zijn toegewezen, hebben dezelfde kredietlimiet.
