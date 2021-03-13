---
title: Financiële dimensies en hoofdrekeningen in talen die van rechts naar links worden geschreven
description: In dit onderwerp worden de beslissingen beschreven die u moet nemen wanneer u een van rechts naar links geschreven taal gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2bdf1b99ae7be6c9d9c43c91c9273e18ce9b1093
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127642"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Financiële dimensies en hoofdrekeningen in talen die van rechts naar links worden geschreven

[!include [banner](../includes/banner.md)]

In dit onderwerp worden enkele implementatiebeslissingen beschreven waarmee u rekening moet houden wanneer u een van rechts naar links geschreven taal gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt.

Financiële dimensies en hoofdrekeningen zijn belangrijke onderdelen van de planningsfase voor een implementatie. Nadat financiële dimensies en hoofdrekeningen in het systeem zijn gemaakt, worden deze gebruikt op de pagina's **Rekeningstructuren configureren**, **Geavanceerde regelstructuren** en **Configuratie van financiële dimensies voor integrerende toepassingen**. De gedefinieerde volgorde op die pagina's wordt gebruikt in het systeem voor gegevensinvoer en -verbruik. Op sommige locaties in het systeem worden de financiële dimensies en hoofdrekeningen in afzonderlijke velden weergegeven. Op andere locaties, zoals in journalen, worden de financiële dimensies en hoofdrekeningen als één reeks weergegeven.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Aanbevolen procedures voor het instellen van financiële dimensies en hoofdrekeningen in een systeem van rechts naar links

- Als u het scheidingsteken voor rekeningschema's selecteert, kunt u een van de opties voor dubbele scheidingstekens selecteren: dubbel koppelteken (`--`), dubbele balk (`||`), dubbele punt (`..`) of dubbel onderstrepingsteken (`\\`).
- Wanneer u de waarden voor financiële dimensies en hoofdrekeningen maakt, moet u alleen cijfers en tekens voor talen gebruiken die van rechts naar links worden geschreven.
- Gebruik niet het geselecteerde scheidingsteken voor rekeningschema's in waarden voor financiële dimensie en hoofdrekeningen.

Door deze aanbevolen procedures te volgen, zorgt u ervoor dat de door de gebruiker gedefinieerd volgorde consistent wordt weergegeven in het systeem.
