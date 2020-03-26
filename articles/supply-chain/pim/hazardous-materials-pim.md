---
title: Gevaarlijke materialen
description: Dit onderwerp biedt informatie over gevaarlijke materiaal-documenten en informatie die is opgeslagen in uw omgeving.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092540"
---
# <a name="hazardous-materials"></a>Gevaarlijke materialen

[!include [banner](../includes/banner.md)]

Informatie over gevaarlijke materialen wordt ingesteld in Productgegevensbeheer. Deze module biedt ook documenten die kunnen worden afgedrukt via magazijnbeheer.

Wanneer u materialen verzendt die zijn geclassificeerd als gevaarlijke goederen, moeten extra documenten bij de zendingen worden gevoegd. Met de functionaliteit voor gevaarlijke materialen kunnen klanten classificatiegegevens opslaan en deze relateren aan vrijgaveartikelen. Deze informatie kan vervolgens worden gebruikt om verzenddocumentatie voor te bereiden.

> [!IMPORTANT]
> Voor het beheren van zendingen van gevaarlijke goederen kunt u met Microsoft Dynamics 365 Supply Chain Management aanvullende verwijzingsgegevens instellen die betrekking hebben op producten. U kunt ook extra verzendingsdocumenten instellen. Het systeem voldoet echter niet automatisch aan de voorschriften van uw land of regio. In plaats daarvan is het een hulpprogramma dat uw algehele programma kan ondersteunen.

Voordat u deze functionaliteit kunt gebruiken, moet u de volgende instellingen opgeven:

- **Productgegevensbeheer**: stel codes in die kunnen worden toegepast op vrijgegeven producten.
- **Magazijnbeheer:** gebruik extra verzenddocumenten om verzendgegevens af te drukken.

## <a name="product-information-management"></a>Productgegevensbeheer

In Productgegevensbeheer is er een reeks instellingstabellen waarin u de referentiegegevens kunt toevoegen die worden vermeld in de lijsten met gevaarlijke goederen voor de vracht-, lucht- en zeevracht.

Dit zijn enkele van de reguleringen waarnaar vaak wordt verwezen:

- **ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg
- **CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen
- **IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)
- **IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen

Elk van deze verordeningen heeft een lijst met gevaarlijke goederen waarin referentiecodes zijn opgenomen. De lijsten voor elk type transport worden gecombineerd in gedeelde internationale classificaties. Supply Chain Management biedt een referentietabel voor de gedeelde codes in die lijsten. Elke lijst heeft ook een aantal unieke codes die kunnen worden gedefinieerd.

Als u deze gegevens wilt configureren, maakt u een verordening die u kunt gebruiken om de initiële parameters te configureren.

## <a name="warehouse-management"></a>Magazijnbeheer

Wanneer een zending wordt voorbereid, kunnen verschillende nieuwe rapporten worden afgedrukt. Deze rapporten gebruiken de informatie die u hebt ingesteld in Productgegevensbeheer.
