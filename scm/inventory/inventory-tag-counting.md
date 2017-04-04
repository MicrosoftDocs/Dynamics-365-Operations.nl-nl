---
title: Voorraadlabeltelling
description: Dit artikel bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 896b91647b65843bf67211cab68b4dd08e379b18
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-tag-counting"></a>Voorraadlabeltelling

Dit artikel bevat informatie over labeltelling, dat u gebruikt om de werkelijke inhoud van een magazijn te vergelijken met de voorhanden voorraad. 

Met behulp van regels op de **labeltelling** pagina, plaats van een labelnummer op elk voorraadartikel, zoals een getal tussen 1 en 500. Tijdens de telling voert u het artikelnummer en de hoeveelheid op een bijbehorend label. Dit label kan vervolgens als basis voor invoer in de labeltellijst worden gebruikt. Nadat u de labeltellijst hebt geboekt, wordt een nieuwe tellijst gemaakt op de pagina **Tellen**. De nieuwe lijst wordt gebaseerd op de regels van de labeltellijst die u hebt gemaakt. Als u een labeltelling op artikelen uitvoert op basis van een specifieke voorraaddimensie, selecteert u de dimensie op de pagina **Dimensie weergeven** die wordt weergegeven wanneer u de labeltellijst maakt. Als u bijvoorbeeld artikelen in een specifiek magazijn wilt tellen, schakelt u het selectievakje **Magazijn** in. Als de schuifregelaar **Artikelen vergrendelen tijdens telling** op de pagina **Parameters voor voorraad- en magazijnbeheer** wordt geselecteerd, kunnen artikelen niet fysiek tijdens het tellen worden bijgewerkt. Artikelen in labeltellijsten worden echter niet vergrendeld tijdens het tellen. Voorraadtransacties worden pas gemaakt als labeltelregels worden geboekt en overgeboekt naar een tellijst. Als labels willekeurig worden ingevoerd en u wilt bepalen of er labels ontbreken, klikt u op de kolomkoptekst **Label** om de regels op label te sorteren.

<a name="see-also"></a>Zie ook
--------

[Cycle counting](../warehousing/cycle-counting.md)


