---
title: Leaseparameters configureren (preview)
description: In dit onderwerp worden de configuratie-instellingen voor Activa leasen beschreven, zoals beveiligingsinformatie en boekhoudinstellingen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 77caf751f9baf4abef534bac97e226484df7acf7
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881271"
---
# <a name="configure-lease-parameters"></a>Leaseparameters configureren

[!include [banner](../includes/banner.md)]

Verschillende configuratie-instellingen zijn van invloed op de werking van de Activa leasen. Deze instellingen omvatten de journaalnamen, algemene parameters en instellingen voor boekingsprofielen.

1. Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.
2. Selecteer het sneltabblad **Algemeen** op het tabblad **Leases**.

    De parameter **Overschrijven van handmatige classificaties toestaan** bepaalt of de leaseclassificatie kan worden overschreven voordat het betalingsschema wordt bevestigd.

    De parameter **Cross-entiteitbatches** bepaalt of u kunt boeken naar andere rechtspersonen vanuit de huidige rechtspersoon. Als deze parameter is ingeschakeld, kunt u journaalboekingen maken voor de rechtspersonen waartoe u toegang hebt.

3. Stel de optie **Verwijderen van bevestigde leases toestaan** in op **Ja** om toe te staan dat leases met bevestigde betalingsschema's worden verwijderd. Leases kunnen niet worden verwijderd als er geboekte of niet-geboekte transacties aan zijn gekoppeld, ongeacht de instelling van deze optie. U kunt een leaserecord niet herstellen nadat deze is verwijderd. Als u records uploadt voor een verwijderde lease, handmatig of via gegevensentiteiten, wordt de geüploade informatie behandeld als nieuw, niet als een update voor een bestaande lease.

    Als u deze optie instelt op **Ja** en het overgangstype van het boek is ingesteld op **optie A of B voor cumulatief verzamelen**, stelt het systeem het veld **Verhoogd leningtarief** in op de waarde van het veld **Verhoogd leningtarief bij overgang** op de pagina **Instellingen voor boeken**. Als deze optie is ingesteld op **Nee**, wordt het tarief op de hoofdlease ingesteld op de waarde van het veld **Verhoogd leningtarief** op de pagina **Boekdetails**, ongeacht het overgangstype van het boek.

4. Stel de optie **Afschrijvingsomkeringen voor afgesloten boekversie toestaan** in op **Ja** om het terugboeken van onkostentransacties voor afschrijving toe te staan. Onkostentransacties kunnen worden omgekeerd, zelfs als de boekversie is afgesloten.

    > [!NOTE]
    > U kunt deze optie het beste op **Nee** instellen. De instelling van deze optie wordt gebruikt als validatie en controle om te voorkomen dat een gesloten boekversie onbedoeld wordt afgeschreven. U kunt de nettoboekwaarde en de toekomstige afschrijvingsberekeningen nauwkeurig bijhouden door de optie op **Nee** in te stellen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
