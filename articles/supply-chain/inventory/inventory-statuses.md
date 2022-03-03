---
title: Voorraadstatussen
description: In dit artikel wordt beschreven hoe u voorraadstatussen kunt gebruiken om voorraad te categoriseren en te traceren.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db15ad94355823c699e83c9e3f47660f813e1c9a
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103458"
---
# <a name="inventory-statuses"></a>Voorraadstatussen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u voorraadstatussen kunt gebruiken om voorraad te categoriseren en te traceren.

## <a name="set-up-and-use-inventory-statuses"></a>Voorraadstatussen instellen en gebruiken

U kunt voorraadstatussen gebruiken om voorraad te categoriseren. U kunt vervolgens de juiste acties initiëren, zoals aanvulling of wegzetwerk.

Hieronder staan enkele voorbeelden van manieren waarop u voorraadstatussen kunt gebruiken:

- Maak voorraadstatussen voor voorhanden voorraad, inkomende en uitgaande transacties.
- Geef een standaardvoorraadstatus voor magazijntransacties op.
- Wijzig een voorraadstatus voor artikelen voor ontvangsten, tijdens ontvangsten, of wanneer de artikelen worden weggezet. tijdens voorraadmutatie
- Gebruik een voorraadstatus om artikelen te prijzen die worden geretourneerd en om artikelbehoefteplanning te plannen tijdens de hoofdplanning.

Een voorraadstatus is een van de dimensies in de opslagdimensiegroep. Voorraadstatussen kunnen worden gecategoriseerd als beschikbaar of als niet-beschikbaar en u kunt de parameter **Voorraadblokkering** gebruiken om artikelen te blokkeren met een niet-beschikbare voorraadstatus. De artikelen met een geblokkeerde status worden beschouwd als fysieke voorraad en kunnen niet op een productieorder, een verkooporder, een overboekingsorder of een uitgaande transactie worden gebruikt.

U kunt magazijnartikelen met beschikbare of niet-beschikbare voorraadstatussen voor inkomend werk gebruiken. U maakt bijvoorbeeld een beschikbare status met de naam *Gereed*, een niet-beschikbare status met de naam *Beschadigd* en een geblokkeerde status met de naam *Geblokkeerd*. Wanneer u een inkooporder voor ontvangen of geretourneerde artikelen maakt als er artikelen gebroken zijn of beschadigd, kunt u de voorraadstatus van deze artikelen wijzigen in *Beschadigd* op de inkooporderregel. Nadat deze artikelen zijn ontvangen, wordt de status automatisch ingesteld op *Geblokkeerd*. Als u de beschadigde artikelen met een mobiel apparaat scant, kan Supply Chain Management locatierichtlijnen en werksjablonen gebruiken om informatie over een geschikte locatie of een bereik met locaties weer te geven waar u die artikelen kunt wegzetten. Voor geretourneerde artikelen wordt een uitgiftetype van *Reservering* gemaakt op de pagina **Voorraadtransacties**.

U kunt opgeven welke voorraadstatussen blokkeringsstatussen zijn door de selectievakjes **Voorraadblokkering** op de pagina **Voorraadstatussen** te gebruiken. U kunt geen voorraadstatussen als blokkeringsstatus gebruiken voor verkooporders, overboekingsorders of projectintegraties.

Voor uitgaand werk kunt u verschillende niet-blokkerende voorraadstatussen gebruiken om te bepalen tegen welke voorraad u moet reserveren. Als u artikelen met de status van *Blokkering* hebt en de hoofdplanning op deze artikelen wordt uitgevoerd, worden de artikelen als ontbrekend beschouwd en wordt de voorraad automatisch aangevuld. Bovendien is het voor kwaliteitsorders die zijn gekoppeld aan uitgaand werk niet mogelijk om de **voorraadstatus** bij te werken als onderdeel van de validatie van kwaliteitsorders.

> [!NOTE]
> U kunt de status van de voorraad niet wijzigen op locaties waar open werk bestaat. Als u bijvoorbeeld een inkoopontvangst voor een artikel hebt aangemaakt, maar het artikel niet hebt weggezet, is er sprake van openstaand werk voor de ontvangende locatie en krijgt u een foutmelding als u de status van de voorraad op die locatie probeert te wijzigen. Als u het gerelateerde werk voltooit of annuleert, kunt u de status wijzigen.
>
> Meestal wordt de status van de voorhanden voorraad met betrekking tot open magazijnwerk alleen gewijzigd door werknemers die de mobiele app Magazijnbeheer gebruiken, bijvoorbeeld tijdens het uitvoeren van een verplaatsingsproces.

Nadat u voorraadstatussen hebt in gesteld, kunt u de standaardvoorraadstatus voor een locatie, artikel en magazijn instellen. U kunt ook een standaardstatus instellen voor verkoop-, transfer- en inkooporders. Voor de standaardstatus voor verkooporders en uitgaande overboekingsorder kan niet de optie **Voorraadblokkering** zijn ingesteld op *Ja*. De voorraadstatus die wordt overgenomen van de standaardinstellingen op een locatie, magazijn, artikel, inkooporder, overboekingsorder of verkooporder kan wordt gewijzigd met behulp van het mobiele apparaat of op de inkooporder-, verkooporder- of overboekingsorderregel.

Als u behoefteplanning voor artikelen wilt plannen met een beschikbare voorraadstatus, selecteert u de optie **In behoefteplan opnemen volgens dimensie** voor een opslagdimensie op de pagina **Opslagdimensiegroepen**. Wanneer u de wizard **Artikelbehoefteplanning** opent, worden artikelen met een beschikbare status op de pagina **Status** weergegeven. Om instellingen voor deze artikelen te maken, selecteer de ID van de voorraadstatus voor de beschikbare voorraadstatussen. Op basis van de instellingen, kunt u de artikelbehoeften berekenen en de vraag en aanbod van beschikbare artikelen maken tijdens de hoofdplanning. U kunt geen instelling voor artikelbehoefteplanning maken met een geblokkeerde voorraadstatus. U kunt ook de pagina **Artikelbehoefteplanning** gebruiken om de parameters voor de artikelbehoefteplanning te maken of te wijzigen.

## <a name="change-inventory-statuses"></a>Voorraadstatussen wijzigen

U kunt voorraadstatussen wijzigen via de pagina **Voorhanden voorraad** of met de periodieke taak *Voorraadstatuswijziging*.

- Wanneer u de periodieke taak *Voorraadstatuswijziging* gebruikt, kunt u opgeven welke records u wilt opnemen en de taak zo instellen dat deze in de batch wordt uitgevoerd met het gewenste interval.
- Als u de voorraadstatus wilt wijzigen als ad-hocproces, gaat u naar de pagina **Voorhanden per locatie**, selecteert u de relevante records en selecteert u vervolgens de knop **Voorraadstatuswijziging**.

> [!NOTE]
> Met de functie *De voorraadstatus wijzigen van artikelen die worden beheerd via traceringsdimensies* kunt u de voorraadstatus van artikelen wijzigen die worden beheerd op basis van traceringsdimensies, waaronder de mogelijkheid om alleen geselecteerde records bij te werken. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *De voorraadstatus van artikelen wijzigen die worden beheerd door traceringsdimensies* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Wanneer de functie is ingeschakeld, kunt u het volgende doen:
>
> - Op de pagina **Voorhanden voorraad** kunt u regels op basis van weergegeven dimensies groeperen met de knop **Weergavedimensies** en de status van de geselecteerde regels wijzigen.
> - Op de pagina **Voorhanden voorraad** kunt u meerdere records selecteren en de knop **Voorraadstatuswijziging** gebruiken om alle records tegelijk te wijzigen.
> - Voor de periodieke taak **Voorraadstatuswijziging** kunt u filteren op traceringsdimensies.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
