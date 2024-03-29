---
title: Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft
description: 'Producten kunnen verschillende bronnen hebben: ze kunnen worden geproduceerd of worden aangeschaft (ingekocht). Dit artikel beschrijft sommige algemene punten om na te gaan wanneer u producten configureert om multi-sourcing te ondersteunen.'
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4910faa2e66cb61f6064e686c49369d14526cc1f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674500"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Producten instellen die kunnen worden geproduceerd of kunnen worden aangeschaft

[!include [banner](../includes/banner.md)]

Producten kunnen verschillende bronnen hebben: ze kunnen worden geproduceerd of worden aangeschaft (ingekocht). Dit artikel beschrijft sommige algemene punten om na te gaan wanneer u producten configureert om multi-sourcing te ondersteunen. 

Multi-sourcing wordt meestal gebruikt voor een ingekocht artikel dat soms wordt gefabriceerd, of wanneer een artikel dat hoofdzakelijk een gefabriceerd artikel was, is gewijzigd zodat het nu in eerste instantie een ingekocht artikel is. Het artikel wordt eerst aangemerkt als een gefabriceerd artikel, zodat de stuklijsten en routegegevens kunnen worden gedefinieerd en om de productieorders voor het artikel te ondersteunen. Het productietype moet worden ingesteld op **Stuklijst** (of voor procesproductie **Formule** of **Co-product**).

Wanneer u standaardkosten gebruikt, kan de kostprijsrecord voor het gefabriceerde artikel worden berekend. De kostprijsrecord komt echter mogelijk niet overeen met de gewenste standaardkosten voor inkoopdoeleinden. In dat geval moeten de standaardkosten handmatig voor de artikelkostprijsrecord worden ingevoerd en geactiveerd. Overweeg voor de kostenberekening het gebruik van een speciale stuklijst en route die de leveringsmix van het product in de loop van een boekperiode vertegenwoordigen, om de afwijkingen in de loop der tijd te minimaliseren. Bovendien kan een artikel dat op de ene site wordt gefabriceerd, naar een andere worden overgebracht. Dat betekent dat de kosten van het artikel handmatig moeten worden ingevoerd en geactiveerd voor de site waarnaar het artikel wordt overgebracht. Als u een gefabriceerd artikel gebruikt als onderdeel van een product op hoger niveau, moeten de kosten van dat onderdeel worden behandeld als een ingekocht product. Deze richtlijn geldt, ongeacht of de kosten van het onderdeel zijn berekend of handmatig ingevoerd. Dat wil zeggen dat bij een stuklijstberekening de artikelkosten moeten worden behandeld als een ingekocht onderdeel in plaats van de stuklijst- en routegegevens van het artikel te gebruiken om kosten te berekenen. 

U kunt voorkomen dat deze berekening wordt uitgevoerd door de markering **Explosie stoppen** in te schakelen die is ingesloten in de stuklijstberekeningsgroep die aan het artikel is toegewezen. U kunt explosievereisten buiten hoofdplanningsberekeningen via het artikel voorkomen door de time fence van explosie op 0 (nul) dagen in te stellen in artikelbehoefteplanning of in de dekkingsgroep. Bij de hoofdplanningsberekening wordt het artikel dan behandeld als ingekocht artikel en worden er geen verdere berekeningen uitgevoerd voor de stuklijst- en routegegevens van het artikel.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]