---
title: Veelgestelde vragen over inkoop
description: Dit onderwerp bevat antwoorden op veelgestelde vragen over de inkoopfunctionaliteit van Supply Chain Management
author: Henrikan
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 99d44f2409d8207ed7a0fb1fc92a99de42240e86
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577187"
---
# <a name="procurement-faq"></a>Veelgestelde vragen over inkoop

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat antwoorden op veelgestelde vragen over de inkoopfunctionaliteit van Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>Kan ik alleen inkooporders weergeven die ik heb gemaakt?

Deze functionaliteit is momenteel niet beschikbaar.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>Kan ik voorraad reserveren en transacties maken voor geregistreerde voorraad op een inkooporder?

### <a name="issue-description"></a>Probleembeschrijving

Zelfs wanneer artikelen de status *Geregistreerd* in een inkooporder hebben, kunt u nog steeds de voorraad reserveren. Met andere woorden, u kunt transacties maken voor de geregistreerde voorraad.

### <a name="reproduce-the-issue"></a>Het probleem reproduceren

In de volgende procedure wordt één manier weergegeven om het probleem te reproduceren.

1. Inkooporder maken.
2. Registreer de inkooporderregel.
3. U ziet dat u reserveringen of transacties voor de geregistreerde voorraad kunt genereren.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen. De verwachting is dat de geregistreerde artikelen fysiek zijn aangekomen in het magazijn of voorraad en dat ze daarom beschikbaar zijn voor reservering.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>Kan ik de gebruiker vinden die een inkooporder heeft geannuleerd?

Deze informatie wordt alleen bijgehouden als de inkooporder onder wijzigingsbeheer valt. Als u wijzigingsbeheer gebruikt, kunt u zien wie de wijziging heeft ingediend (de annulering) en wie deze heeft goedgekeurd.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>Waarom kan ik een inkoopovereenkomst niet aan een bestaande inkooporder koppelen?

Een inkoopovereenkomst moet aan een inkooporderregel worden gekoppeld wanneer de inkooporder wordt gemaakt. Anders kunnen inkooporderregels niet aan inkoopovereenkomstregels worden gekoppeld.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>Welke controle activeert het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'?

Wanneer u de verzenddatum wijzigt, ontvangt u mogelijk het bericht 'Prijzen en kortingen bijwerken die handmatig zijn ingevoerd of extern document'. U ontvangt dit bericht omdat er mogelijk een andere handels- of verkoopovereenkomst wordt geactiveerd als de verzenddatum wordt gewijzigd, wat een prijswijziging kan veroorzaken. Een wijziging van de verzenddatum kan ook van invloed zijn op magazijnplanningen en andere gerelateerde informatie.

Het bericht wordt geactiveerd wanneer een van de datums of andere parameters wordt gewijzigd. Het doel van het bericht is er zeker van te zijn dat u op de hoogte bent van prijswijzigingen die kunnen optreden als gevolg van deze wijzigingen.

Het bericht is de TAE-prompt (handelsovereenkomst). Zie [Evaluatiebeleid voor handelsovereenkomsten](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) voor een volledige beschrijving.

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>Waarom kan ik niet meer dan één factuur boeken voor een inkooporderregel die op categorieën gebaseerde artikelen bevat?

Een hoeveelheid is verplicht als u facturen wilt boeken. Als de volledige hoeveelheid van een regel slechts voor een gedeeltelijk bedrag is gefactureerd, kunt u het resterende bedrag niet op een andere factuur factureren.
