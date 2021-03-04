---
title: Overzicht van gevaarlijke stoffen
description: Dit onderwerp biedt een overzicht van functies die zijn gerelateerd aan het afhandelen en documenteren van gevaarlijke stoffen tijdens productgegevensbeheer en magazijnbeheer.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 34c0a19308bb5159faa9a4ab06bf65e58da0deb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425196"
---
# <a name="hazardous-materials-overview"></a>Overzicht van gevaarlijke stoffen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Om te voldoen aan de verzend- en transportregels, moeten organisaties die materialen verzenden die zijn geclassificeerd als gevaarlijke goederen, aanvullende documenten opnemen in de zending. Met de functie voor gevaarlijke goederen kunnen klanten gegevens opslaan die betrekking hebben op vrijgegeven artikelen. Deze informatie kan vervolgens worden gebruikt om verzenddocumentatie voor te bereiden. Een organisatie die gevaarlijke goederen verzendt, moet zijn eigen processen en procedures hebben voor het beheer van het verzendproces. Microsoft Dynamics 365 Supply Chain Management is slechts een hulpmiddel waarmee u de vereiste documenten kunt genereren.

Het volgende diagram illustreert de stappen die nodig zijn voor het instellen en gebruiken van de functie voor gevaarlijke goederen.

![De functie voor gevaarlijke goederen instellen en gebruiken](media/hazmat-overview.png "De functie voor gevaarlijke goederen instellen en gebruiken")

De functie voor gevaarlijke goederen wordt ingesteld in Productgegevensbeheer en biedt documenten die kunnen worden afgedrukt via Magazijnbeheer. Daarom zijn deze gebieden in principe de belangrijkste twee gebieden waar u de functionaliteit van deze functie kunt controleert, instelt en gebruikt:

- **Productgegevensbeheer**: stel de codes in die kunnen worden toegepast op een vrijgegeven product.
- **Magazijnbeheer** : werk met aanvullende vervoersdocumenten die voor zendingen worden afgedrukt.

> [!IMPORTANT]
> De functies voor gevaarlijke goederen in Supply Chain Management bevatten een verzameling nuttige productgegevensvelden en gerelateerde functionaliteit die u kunnen helpen bij het registreren van en verwijzen naar informatie met betrekking tot uw gevaarlijke producten. Deze functies kunnen u ook helpen bij het ontwerpen en afdrukken van vervoersdocumenten met dezelfde informatie over gevaarlijke stoffen die u verzendt. Het gebruik van dit systeem betekent echter niet dat u automatisch voldoet aan alle toepasselijke voorschriften uw land of regio. Hoewel deze hulpmiddelen zijn bedoeld om u te helpen te voldoen aan algemene regelgeving, zijn ze niet voldoende en geven ze geen garanties. Uw organisatie is moet er zelf voor zorgen dat men op de hoogte is van alle toepasselijke regelgeving en dat alle nodige maatregelen worden genomen om daaraan te voldoen.

## <a name="product-information-management"></a>Productgegevensbeheer

Productgegevensbeheer bevat een reeks instellingstabellen waarin u referentiegegevens kunt toevoegen voor de diverse lijsten met gevaarlijke goederen voor transport over land, lucht en zee.

Bij het ontwikkelen van deze functie wordt verwezen naar de volgende algemene regelgevingen:

- **ADR**: verordeningen met betrekking tot het internationale vervoer van gevaarlijke goederen over de weg
- **CFR 49**: reglementering in de Verenigde Staten voor het vervoer van gevaarlijke goederen
- **IMDG**: de internationale code voor internationale gevaarlijke goederen over zee (IMDG)
- **IATA**: de IATA-bepalingen (International Air Trans Port Association) inzake gevaarlijke goederen

Elke reeks regelgevingen voorziet in gestandaardiseerde lijsten van gevaarlijke goederen en referentiecodes. Daarin verstrekt Supply Chain Management een referentietabel voor de algemene codes in die lijsten. Elke lijst heeft ook een aantal unieke codes die u kunt definiëren.

Zie de volgende onderwerpen voor meer informatie over het instellen van regels en waarden voor gevaarlijke goederen en over het toewijzen van de waarden aan relevante producten:

- [Gevaarlijke goederen instellen](hazmat-setup.md)
- [Gevaarlijke goederen in producten, orders, zendingen en ladingen](hazmat-items.md)

## <a name="warehouse-management"></a>Magazijnbeheer

Wanneer u een zending voorbereidt in Magazijnbeheer, kunt u verschillende nieuwe rapporten afdrukken waarin de informatie wordt gebruikt die u hebt ingesteld in Productgegevensbeheer. Meer informatie over de beschikbare rapporten en hoe u deze kunt gebruiken vindt u in [Informatie en rapporten voor gevaarlijke stoffen](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]