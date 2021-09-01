---
title: Voorraadlabeltelling
description: Dit onderwerp bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad.
author: MarkusFogelberg
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99d2dadf7d49a37b5f06bf08ece5454bf742d5dc6ab001402ace3097d5ec96b6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735202"
---
# <a name="inventory-tag-counting"></a>Voorraadlabeltelling

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad.

Met behulp van regels op de pagina **Telling labels** plaatst u een labelnummer op elk voorraadartikel, zoals een getal tussen 1 en 500. Tijdens de telling voert u het artikelnummer en de hoeveelheid op een bijbehorend label in. Dit label kan vervolgens als basis voor invoer in de labeltellijst worden gebruikt. Nadat u de labeltellijst hebt geboekt, wordt een nieuwe tellijst gemaakt op de pagina **Tellen**. De nieuwe lijst wordt gebaseerd op de regels van de labeltellijst die u hebt gemaakt. Als u een labeltelling op artikelen uitvoert op basis van een specifieke voorraaddimensie, selecteert u de dimensie op de pagina **Dimensie weergeven** die wordt weergegeven wanneer u de labeltellijst maakt. Als u bijvoorbeeld artikelen in een specifiek magazijn wilt tellen, schakelt u het selectievakje **Magazijn** in. Als de schuifregelaar **Artikelen vergrendelen tijdens telling** op de pagina **Parameters voor voorraad- en magazijnbeheer** wordt geselecteerd, kunnen artikelen niet fysiek tijdens het tellen worden bijgewerkt. Artikelen in labeltellijsten worden echter niet vergrendeld tijdens het tellen. Voorraadtransacties worden pas gemaakt als labeltelregels worden geboekt en overgeboekt naar een tellijst. Als labels willekeurig worden ingevoerd en u wilt bepalen of er labels ontbreken, klikt u op de kolomheader **Label** om de regels op label te sorteren.

## <a name="additional-resources"></a>Aanvullende resources

[Cyclustelling](../warehousing/cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]