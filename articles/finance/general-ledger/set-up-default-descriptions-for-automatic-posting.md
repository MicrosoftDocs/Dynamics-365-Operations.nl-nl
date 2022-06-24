---
title: Standaard beschrijvingen voor automatische boeking instellen
description: Dit artikel verklaart hoe u de standaardtekst kunt instellen die wordt gebruikt om boekhoudinvoeringen te beschrijven die automatisch in het grootboek zijn geboekt. U kunt een standaard beschrijvingstekst instellen met vrije tekst of door vaste variabelen te selecteren.
author: aprilolson
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71982a7d5b1bb08d3e238646ea0b15f17260bdcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904494"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a>Standaard beschrijvingen voor automatische boeking instellen

[!include [banner](../includes/banner.md)]

Dit artikel verklaart hoe u de standaardtekst kunt instellen die wordt gebruikt om boekhoudinvoeringen te beschrijven die automatisch in het grootboek zijn geboekt. U kunt een standaard beschrijvingstekst instellen met vrije tekst of door vaste variabelen te selecteren.

> [!NOTE]
> Voor een aantal transactietypes in een aantal landen of regio's kunt u ook tekst invoegen uit velden die aan deze transactietypes zijn gerelateerd. Zie voor een lijst met transactietypen en de landen en regio's het gedeelte [Optioneel: andere tekst aan standaardbeschrijvingen toevoegen](#optional-add-other-text-to-default-descriptions), verderop in dit artikel.

## <a name="set-up-default-descriptions"></a>Standaardbeschrijvingen opzetten

1. Ga naar **Organisatiebeheer** \> **Instellen** \> **Standaardbeschrijvingen**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het veld **Beschrijving** het transactietype waarvoor een standaardbeschrijving moet worden gemaakt.
4. Selecteer in het veld **Taal** de taal waarop de beschrijving van toepassing is.
5. Voer in het veld **Tekst** de standaardbeschrijving in. U kunt ook tekst in het veld typen of u kunt een of meer van de volgende tekstvariabelen gebruiken:

    - **%1**: hiermee voegt u de transactiedatum toe.
    - **%2**: hiermee voegt u een id toe die overeenkomt met het type document dat naar het grootboek wordt geboekt. Voor transactietypes die zijn gerelateerd aan facturen, voegt u met de variabele **%2** bijvoorbeeld het factuurnummer toe.
    - **%3**: hiermee voegt u een id toe die is gerelateerd aan het type document dat naar het grootboek wordt geboekt. Voor transactietypes die zijn gerelateerd aan facturen, voegt u met de variabele **%3** bijvoorbeeld het klantaccountnummer toe.

## <a name="optional-add-other-text-to-default-descriptions"></a>Optioneel: Voeg andere tekst aan standaard beschrijvingen

Voor een aantal transactietypes in een aantal landen of regio's kunnen standaardbeschrijvingen tekst bevatten die afkomstig is uit velden in de database die zijn gerelateerd aan deze transactietypes. De volgende lijsten bevatten de transactietypes en de landen en regio's waarvoor deze optie beschikbaar is.

**Transactietypen**

U kunt andere tekst voor standaardbeschrijvingen toevoegen voor transactietypen die aan de volgende documenttypes worden gekoppeld:

- Klantfacturen
- Creditnota's van de klant
- Contact betalingen van de klant
- Leveranciersbetalingen
- Verkooporders
- Inkooporders
- Voorraadjournalen
- Hoofdplanning (MRP)
- Vaste activa

**Landen en regio's**

Deze optie is beschikbaar voor de volgende landen en regio's:

- Brazilië
- China
- Tsjechische Republiek
- Oost-Europa
- Hongarije
- India
- Japan
- Litouwen
- Letland
- Polen
- Rusland

### <a name="add-text-to-default-descriptions"></a>Voeg tekst toe aan standaard beschrijvingen

Wanneer u de stappen in het gedeelte [Standaardbeschrijvingen instellen](#set-up-default-descriptions), eerder in dit artikel hebt voltooid, volgt u deze stappen om andere tekst aan de standaardbeschrijvingen toe te voegen.

1. Selecteer op het sneltabblad **Parameters** de optie **Toevoegen**.
2. Selecteer in het veld **Referentietabel** de databasetabel met de parametergegevens die u aan de beschrijving wilt toevoegen.
3. Selecteer in het veld **Referentieveld** het veld met de parametergegevens die u aan de beschrijving wilt toevoegen.
4. Herhaal stappen 1 tot 3 als u nog meer parameters wilt toevoegen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
