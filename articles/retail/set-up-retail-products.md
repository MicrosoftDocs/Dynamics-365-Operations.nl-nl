---
title: Detailhandelproducten instellen
description: Dit artikel wordt beschreven hoe u detailhandelproducten instelt in Microsoft Dynamics 365 for Retail.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 991546424a95463315eaa73c2776d0defe66def5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546248"
---
# <a name="set-up-retail-products"></a>Detailhandelproducten instellen

[!include [banner](includes/banner.md)]

Dit artikel wordt beschreven hoe u detailhandelproducten instelt in Microsoft Dynamics 365 for Retail.

Voordat u producten voor doorverkoop kunt aanbieden in uw detailhandelkanalen, moet u ze maken en configureren in Dynamics 365 for Retail. De detailhandel gebruikt de productfuncties in Dynamics 365 for Retail om organisatiebrede producten in het productmodel te maken. U kunt producten maken, de producteigenschappen en -kenmerken definiëren, en de producten toewijzen aan detailhandelcategoriehiërarchieën. Als u de producten beschikbaar wilt maken voor uw detailhandelkanalen en als u deze aan het actieve assortiment wilt toevoegen, moet u de producten vrijgeven aan rechtspersonen waarbij deze verkrijgbaar zijn. Voer de volgende taken uit om de producten die u verkoopt via de detailhandelkanalen, in te stellen.

1. Een detailhandelproducthiërarchie definiëren U kunt met de functies voor categoriehiërarchieën in Dynamics 365 for Retail detailhandelcategoriehiërarchieën definiëren voor het groeperen en categoriseren van de producten die u naar uw detailhandelkanalen distribueert. Er kunnen op elk categorieniveau door de gebruiker gedefinieerde kenmerken en systeemkenmerken worden gedefinieerd. Vervolgens nemen alle producten die aan de categorie zijn toegewezen, deze kenmerken over. Er kunnen meerdere categoriehiërarchieën worden gedefinieerd en elk product kan aan meerdere hiërarchieën worden toegewezen. Binnen één enkele hiërarchie kan elk product echter slechts aan één categorie worden toegewezen.
2. Producten en productvarianten voor het productmodel toevoegen. Producten die aan het productmodel worden toegevoegd, vertegenwoordigen een algemene lijst met producten. U kunt producten een voor een handmatig toevoegen of u kunt productgegevens van uw leveranciers importeren.
3. De producten vrijgeven aan rechtspersonen. Alleen producten die zijn vrijgegeven aan rechtspersonen kunnen aan uw detailhandelkanalen beschikbaar worden gesteld. Wanneer u een product voor het eerst definieert, kunt u dit definiëren op een niveau dat betrekking heeft op een gehele organisatie. U kunt vervolgens een of meer rechtspersonen selecteren waaraan het product moet worden vrijgegeven. Het product wordt vervolgens beschikbaar gesteld voor meerdere detailhandelkanalen in uw organisatie. U kunt deze functionaliteit gebruiken om één product tegelijk te maken, om productkenmerken en -eigenschappen via één locatie toe te voegen en bij te werken en om het product vervolgens binnen uw organisatie te distribueren naar de detailhandelkanalen waar dit beschikbaar is.
4. Producten toevoegen aan assortimenten. Een assortiment vertegenwoordigt een verzameling producten die u via uw detailhandelkanalen aanbiedt. U kunt een of meer assortimenten definiëren en elk product kan aan een of meer assortimenten worden toegewezen. Als u producten aan detailhandelkanalen wil toewijzen, wijst u de assortimenten aan de desbetreffende detailhandelkanalen toe. Wanneer u een assortiment maakt, kunt u producten toevoegen die nog niet aan een rechtspersoon zijn vrijgegeven. Voordat de producten aan de detailhandelkanalen beschikbaar kunnen worden gesteld, moet u de producten echter aan een rechtspersoon vrijgeven.
5. Producten toevoegen aan navigatiehiërarchieën. Voordat producten online of op het verkooppunt (POS) kunnen worden doorgebladerd, moeten ze worden gecategoriseerd in een detailhandelnavigatiehiërarchie.
6. Producten toevoegen aan catalogi. Hoewel deze stap optioneel is voor POS, moeten online winkels de producten opnemen in ten minste één catalogus.
