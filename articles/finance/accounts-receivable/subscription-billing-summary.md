---
title: Overzicht van facturering van abonnementen
description: In dit artikel wordt de facturering van abonnementen in Microsoft Dynamics 365 Finance beschreven.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 10302e9ae7dff3d018897b666caaf4d4289b4866
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856736"
---
# <a name="subscription-billing-overview"></a>Overzicht van facturering van abonnementen

[!include [banner](../includes/banner.md)]

Met abonnementsfacturering kunnen organisaties verkoopkansen voor abonnementsopbrengsten en terugkerende facturering beheren via factureringsplanningen. Complexe prijs- en factureringsmodellen en opbrengsttoewijzing kunnen eenvoudig worden beheerd en worden gefactureerd en herkend op regelniveau. Dankzij de opbrengsttoewijzing met meerdere elementen voldoet de toewijzing van opbrengsten aan internationale boekhoudstandaarden (International Financial Reporting Standard 15 \[IFRS 15\]) en algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (VS GAAP) (Accounting Standards Codification Topic 606 \[ASC 606\]).

De oplossing omvat drie modules die onafhankelijk kunnen worden gebruikt. U kunt ook alle drie de modules samen gebruiken.

- **Terugkerende contractfacturering**: deze module maakt terugkerende facturering en prijsbeheer mogelijk om de prijs- en factureringsparameters, contractverlenging en geconsolideerde facturering te beheren.
- **Uitgestelde opbrengsten en onkosten**: met deze module worden handmatige processen en de afhankelijkheid van externe systemen geëlimineerd door opbrengst te beheren en realtime inzicht te krijgen in maandelijkse terugkerende opbrengsten.
- **Opbrengsttoewijzing met meerdere elementen**: deze module komt de conformiteit van opbrengsten ten goede door de prijs- en opbrengsttoewijzing voor meerdere artikelen te verwerken.

Meer informatie over facturering van abonnementen vindt u in [Power BI-content voor facturering van abonnementen](sub-bill-power-bi.md).

Facturering van abonnementen wordt ingeschakeld via **Functiebeheer**. Deze functie kan echter niet worden gebruikt met de functie **Opbrengsttoerekening**. U moet deze functie daarom uitschakelen voordat u facturering van abonnementen inschakelt.

1. Voer in de werkruimte **Functiebeheer** op het tabblad **Alle** de naam **Opbrengsttoerekening** in het filter in en selecteer vervolgens de naam van de functie als het filter.
2. Selecteer de functie **Opbrengsttoerekening** en **Uitschakelen**.
3. Geef in het filter **Naam van functie** de naam **Facturering van abonnementen** op en selecteer vervolgens het modulefilter.
4. Selecteer de functie **Facturering van abonnementen** en selecteer vervolgens **Inschakelen**.
5. Selecteer een van de drie modules in de vorige lijst en selecteer vervolgens **Inschakelen**. Herhaal deze stap voor elk van de twee andere modules.

    > [!IMPORTANT]
    > De functie **Facturering van abonnementen** moet zijn ingeschakeld voordat u een van de drie modules kunt inschakelen.
