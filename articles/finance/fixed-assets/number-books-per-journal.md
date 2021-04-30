---
title: Aantal boeken per journaal
description: Dit onderwerp beschrijft de relatie tussen journalen en activaboeken wanneer u een voorstel voor verwerving of afschrijving van vaste activa maakt met behulp van een batchtaak. U kunt het maximumaantal boeken definiëren dat voor elke verwerving en afschrijving wordt opgenomen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb2a25d9e2ffc26f0a37a09cdf3e28a7ca4b84bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892402"
---
# <a name="number-of-books-per-journal"></a>Aantal boeken per journaal

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de relatie tussen journalen en activaboeken wanneer u een voorstel voor verwerving of afschrijving van vaste activa maakt met behulp van een batchtaak. U kunt het maximumaantal boeken definiëren dat voor elke verwerving en afschrijving wordt opgenomen met behulp van de velden in de sectie **Aantal boeken per journaal** op het tabblad **Algemeen** van de pagina **Parameters voor vaste activa** (**Vaste activa \> Instellingen \> Parameters voor vaste activa**). Met deze velden kunt u het aantal activaboeken per verwervingsjournaal en afschrijvingsjournaal verdelen.

Voor een verwervingsvoorstel is de standaardwaarde minimaal 10.000 boeken. Voor een afschrijvingsvoorstel is de standaardwaarde minimaal 2.000 boeken.

Als er bijvoorbeeld 4.000 vaste activa zijn en er twee boeken aan elk activum zijn gekoppeld, wordt één boek op de huidige laag geboekt en wordt het andere boek op de belastingslaag geboekt. Als u 4.000 vaste activa verwerft via batchverwerking, bevat de batchtaak waarmee één verwervingsjournaal voor vaste activa wordt gemaakt met 4.000 activaboeken.

> [!NOTE]
> Het journaal dat wordt gemaakt, wordt gebruikt totdat de batchtaak is voltooid.
>
> De afgeleide boeken worden niet opgenomen in het maximumaantal boeken per journaal.

U kunt batchverwerking gebruiken om afschrijving uit te voeren voor dezelfde reeks verworven activa. Met een batchtaak worden bijvoorbeeld twee afschrijvingsjournalen gemaakt die elk uit 2.000 activaboeken bestaan. Het eerste journaal bevat boeken die zijn gekoppeld aan de vaste activa die zijn genummerd van 1 tot en met 2.000. Het tweede journaal bevat boeken die zijn gekoppeld aan de vaste activa die zijn genummerd van 2.001 tot en met 4.000.

De batchverwerkingstaak sluit afgesloten boeken uit. In een batchtaak voor afschrijving worden bijvoorbeeld 10 van de eerste 2.000 boeken afgesloten. In dit geval bevat het eerste journaal boeken die zijn gekoppeld aan de vaste activa die zijn genummerd van 1 tot en met 2.011. Het tweede journaal bevat boeken die zijn gekoppeld aan de vaste activa die zijn genummerd van 2.012 tot en met 4.000.

> [!NOTE]
> Als u vaste-activa-id's hebt met verschillende scheidingstekens (zoals – of /) en u vaste-activatransacties maakt in batchtaken, moet u voor elk type scheidingsteken een afzonderlijke batchtaak uitvoeren. Het systeem kan niet verschillende scheidingstekens in dezelfde batchtaak verwerken.

De limiet van het aantal boeken wordt toegepast als er geen dubbele activa-id's in hetzelfde journaal aanwezig zijn. Als de activa-id echter hetzelfde is als de boek-id, kan het aantal boeken per journaal worden overschreden om de activa-id in hetzelfde journaal te houden.

Er zijn bijvoorbeeld 5.001 vaste-activa-id's, drie boeken worden gekoppeld aan elke vaste-activa-id en elk activaboek wordt naar dezelfde boekingslaag geboekt. U voert de afschrijving uit voor drie opeenvolgende maanden, zonder samenvatting.  Het afschrijvingsjournaal wordt gemaakt via een batch taak en er worden zeven journalen gemaakt met 667 vaste-activa-id's en drie boeken voor elke vaste-activa-id. Het resultaat is 2.001 boeken. Over drie maanden zijn er dus 6.003 journaalregels om dezelfde activa-id's in hetzelfde journaal te behouden. Er wordt ook één journaal gemaakt met 332 vaste-activa-id's en drie boeken voor elke vaste-activa-id. Over drie maanden zijn er 2.988 regels.

> [!NOTE] 
> Als de parameter **Afschrijving samenvatten** is ingeschakeld wanneer u een afschrijvingsvoorstel maakt, heeft de waarde in het veld **Aantal boeken per journaal - Afschrijvingsvoorstel** geen effect. In dit geval is het aantal boeken per journaal 6000. Dit is de intern gedefinieerde limiet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
