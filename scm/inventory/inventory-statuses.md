---
title: Voorraadstatussen
description: In dit artikel wordt beschreven hoe u voorraadstatussen kunt gebruiken om voorraad te categoriseren en te traceren.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Voorraadstatussen

In dit artikel wordt beschreven hoe u voorraadstatussen kunt gebruiken om voorraad te categoriseren en te traceren.

U kunt voorraadstatussen gebruiken om voorraad te categoriseren. U kunt vervolgens de juiste acties initiëren, zoals aanvulling of wegzetwerk. 

Hieronder staan enkele voorbeelden van manieren waarop u voorraadstatussen kunt gebruiken:

-   Maak voorraadstatussen voor voorhanden voorraad, inkomende en uitgaande transacties.
-   Geef een standaardvoorraadstatus voor magazijntransacties op.
-   Wijzig een voorraadstatus voor artikelen voor ontvangsten, tijdens ontvangsten, of wanneer de artikelen worden weggezet. tijdens voorraadmutatie
-   Gebruik een voorraadstatus om artikelen te prijzen die worden geretourneerd en om artikelbehoefteplanning te plannen tijdens de hoofdplanning.

Een voorraadstatus is een van de dimensies in de opslagdimensiegroep. Voorraadstatussen kunnen worden gecategoriseerd als beschikbaar of als niet-beschikbaar en u kunt de parameter **Voorraadblokkering** gebruiken om artikelen te blokkeren met een niet-beschikbare voorraadstatus. De artikelen met een geblokkeerde status worden beschouwd als fysieke voorraad en kunnen niet op een productieorder, een verkooporder, een transferorder of een uitgaande transactie worden gebruikt. 

U kunt magazijnartikelen met beschikbare of niet-beschikbare voorraadstatussen voor inkomend werk gebruiken. U maakt bijvoorbeeld een beschikbare status met de naam **Gereed**, een niet-beschikbare status met de naam **Beschadigd** en een geblokkeerde status met de naam **Geblokkeerd**. Wanneer u een inkooporder voor ontvangen of geretourneerde artikelen maakt als er artikelen gebroken zijn of beschadigd, kunt u de voorraadstatus van deze artikelen wijzigen in **Beschadigd ** op de inkooporderregel. Nadat deze artikelen zijn ontvangen, wordt de status automatisch ingesteld op **Geblokkeerd**. Als u de beschadigde artikelen met een mobiel apparaat scant, kan Microsoft Dynamics 365 for Operations locatierichtlijnen en werksjablonen gebruiken om informatie over een geschikte locatie of een bereik met locaties weer te geven waar u die artikelen kunt wegzetten. Voor geretourneerde artikelen wordt een uitgiftetype van **Reservering** gemaakt op de pagina **Voorraadtransacties**. 

Gebruik voor uitgaand werk artikelen met een beschikbare voorraadstatus. Als u artikelen met de status van **Gebroken** hebt en de hoofdplanning op deze artikelen wordt uitgevoerd, worden de artikelen als ontbrekend beschouwd en wordt de voorraad automatisch aangevuld. 

Nadat u voorraadstatussen hebt in gesteld, kunt u de standaardvoorraadstatus voor een locatie, artikel en magazijn instellen. U kunt ook een standaardstatus instellen voor verkoop-, transfer- en inkooporders. Voor de standaardstatus voor verkooporders en uitgaande transferorder kan niet de optie **Voorraadblokkering** zijn ingesteld op **Ja**. De voorraadstatus die wordt overgenomen van de standaardinstellingen op een locatie, magazijn, artikel, inkooporder, transferorder of verkooporder kan wordt gewijzigd met behulp van het mobiele apparaat of op de inkooporder-, verkooporder- of transferorderregel. 

Als u behoefteplanning voor artikelen wilt plannen met een beschikbare voorraadstatus, selecteert u de optie **In behoefteplan opnemen volgens dimensie** voor een opslagdimensie op de pagina **Opslagdimensiegroepen**. Wanneer u de wizard **Artikelbehoefteplanning** opent, worden artikelen met een beschikbare status op de pagina **Status** weergegeven. Om instellingen voor deze artikelen te maken, selecteer de ID van de voorraadstatus voor de beschikbare voorraadstatussen. Op basis van de instellingen, kunt u de artikelbehoeften berekenen en de vraag en aanbod van beschikbare artikelen maken tijdens de hoofdplanning. U kunt geen instelling voor artikelbehoefteplanning maken met een geblokkeerde voorraadstatus. U kunt ook de pagina **Artikelbehoefteplanning** gebruiken om de parameters voor de artikelbehoefteplanning te maken of te wijzigen.


