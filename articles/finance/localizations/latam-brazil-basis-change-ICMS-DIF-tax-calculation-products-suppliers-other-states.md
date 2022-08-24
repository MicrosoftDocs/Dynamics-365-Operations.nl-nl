---
title: Basiswijziging in belastingberekeningen van ICMS-DIF voor producten van leveranciers in andere staten
description: In dit artikel wordt de configuratie beschreven voor berekeningen van het ICMS-DIF-belastingtype wanneer een belastingdocument wordt ontvangen in de Braziliaanse staat Rio Grande do Sul (RS) of São Paulo (SP).
author: Kai-Cloud
ms.date: 06/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218644"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Basiswijziging (dubbele basis) in belastingberekeningen van ICMS-DIF voor producten van leveranciers in andere staten

In dit artikel wordt de configuratie beschreven voor berekeningen van het **ICMS-DIF**-belastingtype wanneer een belastingdocument wordt ontvangen in de Braziliaanse staat Rio Grande do Sul (RS) of São Paulo (SP).

Volgens de bepalingen van de staatswetten moet voor de geïnde Imposto sobre Circulação de Mercadorias e Serviços (ICMS) deze regel worden gevolgd:

*Te innen ICMS* = ([(*Bewerkingsbedrag* – *ICMS van bron*) ÷ (1 – *ICMS % intern*)] × *ICMS % intern*) – *ICMS-bedrag van bron*

## <a name="example"></a>Voorbeeld

Een Braziliaans bedrijf in de staat RS ontvangt een belastingdocument voor een inkoop van een leverancier in de staat SP. Het bedrijf moet het percentageverschil van ICMS tussen de staat RS (18 procent) en de staat SP (12 procent) innen. De basis moet echter worden berekend volgens de voorgaande regel.

- **Bewerkingsbedrag:** 1.000,00 Braziliaanse real (R$ 1.000,00)
- **ICMS interstate:** R$ 120,00
- **ICMS-percentage in de staat RS:** 18 procent
- **Te innen ICMS in de staat de RS:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18 ) – 120 = R$ 73,17 

## <a name="resolution"></a>Oplossing

Als u het ICMS-verschil (ICMS-DIF) wilt berekenen volgens de regels van de staat RS, moet u btw-codes en een btw-groep als volgt instellen:

1. Maak een btw-code om 12 procent ICMS (voor de andere staat) te ontvangen. Deze code wordt gebruikt om het te ontvangen btw-bedrag van de leverancier te registreren.
2. Maak een btw-code om ICMS-DIF te innen. Deze btw-code moet een percentagebedrag van 18 procent (voor uw eigen staat) hebben om het verschil tussen 18 procent en 12 procent te definiëren. Stel het btw-type in op **ICMS-DIF**. Deze btw-code moet als volgt worden gedefinieerd in de berekeningsparameters:

    - Selecteer in het veld **Oorsprong** de optie **Percentage van brutobedrag**.
    - Selecteer in het veld **Marginale basis** **nettobedrag per regel**.
    - Definieer de belastingcode zodat deze een fiscale waarde van **3** heeft. Op deze manier wordt de correctietransactie automatisch gemaakt wanneer de module **Belastingboeken** wordt ingeschakeld.
    - Selecteer in de configuratie van de btw-groep de optie **Gebruiksbelasting** voor de btw-code **ICMS-DIF**.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Het deltabelastingtarief gebruiken in de configuratie van de ICMS-DIF-btw-code voor dubbele basis

Wanneer de eerder beschreven instellingen worden gebruikt, wordt de **ICMS-DIF**-btw-code berekend in de dubbele basisregel. Het nominale btw-percentage wordt echter 18 procent, wat verschilt van het percentage van 6 procent in de eenvoudige basisregel. Dit verschil veroorzaakt inconsistentieproblemen in fiscale documenten en belastingaangifte. Vanaf Microsoft Dynamics 365 Finance versie 10.0.29 kunt u de functie **(Brazilië) Configureer het deltabelastingtarief in de ICMS-DIF-belastingcode voor de aanvraag met dubbele basis** inschakelen in **Functiebeheer** om de inconsistenties te verwijderen.

- Selecteer niet alleen de stappen in het voorgaande gedeelte, maar ook de btw-code **ICMS 12** in het v eld **btw op btw**.
- Stel het btw-percentage van de **ICMS-DIF**-btw-code in op 18 procent. Het veld **Percentage/bedrag** toont het nominale btw-tarief van 6 procent.

> [!NOTE]
> De btw-codes **ICMS-DIF** en **ICMS 12** moeten in dezelfde btw-groep worden toegewezen.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Basiswijziging (dubbele basis) in belastingberekeningen van ICMS-DIF voor producten van niet-belastingplichtige consumenten (DIFAL) in andere staten

Schakel de functie **(Brazilië) Berekening met dubbele basis voor ICMS-DIFAL in verkooptransacties** in **Functiebeheer** in ter ondersteuning van de basiswijziging van ICMS-DIF bij handel voor niet-belastingbetalers vanuit een andere staat. De voorbeeld-ICMS-DIF-btw-code is van kracht voor verkooporder- en vrije-tekstfactuurtransacties.

Schakel de functie **(Brazilië) Berekening met dubbele basis voor ICMS-DIFAL in verkooptransacties** in **Functiebeheer** in om scenario's te ondersteunen waarbij handel met niet-belastingbetalers uit een andere staat ook verplicht is voor IPI (Imposto sobre Produtos Industrializados). Het btw-bedrag van de IPI-btw-code wordt herkend en toegepast in de ICMS-DIFAL-btw-basis.

- In de header van de verkooporder of vrije-tekstfactuur moet op het sneltabblad **Fiscale informatie** de optie **Uiteindelijke gebruiker** op **Ja** worden ingesteld.
- In de header van de inkooporder of leveranciersfactuur moet op het sneltabblad **Fiscale informatie** de optie **Uiteindelijke gebruiker** op **Ja** worden ingesteld.
