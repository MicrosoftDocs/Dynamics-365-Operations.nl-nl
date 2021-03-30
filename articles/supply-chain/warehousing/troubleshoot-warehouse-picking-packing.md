---
title: Problemen met verzamelen en verpakken oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het verzamelen en verpakken in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223237"
---
# <a name="troubleshoot-picking-and-packing"></a>Problemen met verzamelen en verpakken oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens het verzamelen en verpakken in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>Het volgende foutbericht wordt weergegeven: "Dimensielocatie kan niet leeg worden gelaten als het serienummer van de dimensie is ingesteld."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven als u een transferorder maakt voor een serieartikel met behulp van een magazijn dat is ingeschakeld voor geavanceerd magazijnbeheer (WMS) en vervolgens, als het werk is voltooid, probeert u de zending te bevestigen.

### <a name="issue-resolution"></a>Probleemoplossing

Het veld **Standaardlocatie voor ontvangst** is leeg voor een transitmagazijn van het van-magazijn. U kunt dit probleem oplossen door een standaardlocatie voor ontvangst op te geven in het transitmagazijn. Zorg ervoor dat deze locatie een door nummerplaten beheerde locatie is.

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>Het volgende foutbericht wordt weergegeven: "Ongeldige nummerplaat."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven in de magazijn-app wanneer u een nummerplaat-id scant.

### <a name="issue-resolution"></a>Probleemoplossing

Controleer of de nummerplaat-id in de tabel met nummerplaten voorkomt en of de artikelen en hoeveelheden op de nummerplaat beschikbaar zijn (met andere woorden: ze worden niet geblokkeerd).

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>Het volgende foutbericht wordt weergegeven: "Het veld 'Ladinggewicht' (=-%1) kan alleen positieve getallen bevatten. Update is geannuleerd."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven als er openstaand werk is wanneer u werk verwerkt vanuit verpakkingslocaties naar faseringslocaties of vanuit faseringslocaties naar doklocaties.

### <a name="issue-resolution"></a>Probleemoplossing

Als u dit probleem wilt verhelpen, gaat u naar **Systeembeheer \> Periodieke taken \> Database \> Consistentiecontrole** en voert u het proces uit voor **Consistentiecontrole capaciteit magazijn**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Het volgende foutbericht wordt weergegeven: "De hoeveelheid is niet geldig voor eenheid %1."

### <a name="issue-description"></a>Probleembeschrijving

Dit foutbericht wordt weergegeven wanneer u een *gesplitste verzameling* over meerdere batches wilt uitvoeren.

### <a name="issue-resolution"></a>Probleemoplossing

De magazijnmedewerker moet het proces *Korte verzameling* in de magazijn-app gebruiken. Als u meerdere batches vanaf dezelfde locatie wilt verzamelen, kunt u ook de optie **Volledig** in de magazijn-app gebruiken.

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>Ik kan geen voorraad verplaatsen naar een locatie die is door nummerplaten wordt beheerd.

### <a name="issue-description"></a>Probleembeschrijving

U kunt verzamelde hoeveelheden niet verminderen op een lading.

### <a name="issue-resolution"></a>Probleemoplossing

In eerdere versies kunt u verzamelde hoeveelheden niet verminderen op een lading. U kunt de opname van een door nummerplaten beheerde locatie nu echter opheffen. U moet zowel een waarde voor **Locatie** als een waarde voor **Nummerplaat** opgeven voor de ladingsregel op de pagina **Opgenomen hoeveelheid reduceren**.

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>Kan ik een afleveringsbewijs of verpakkingsinhoud afdrukken per magazijn?

### <a name="issue-description"></a>Probleembeschrijving

U wilt een afleveringsbewijs of verpakkingsinhoud afdrukken per magazijn of site op de pagina **Werkauditsjabloonregel bijwerken**.

### <a name="issue-resolution"></a>Probleemoplossing

Wanneer u een document afdrukt met behulp van de instellingen van afdrukbeheer, beperkt u het bereik (site/magazijn) via afdrukbeheer in plaats van door **Afdrukinstellingen bewerken** te selecteren op de pagina **Werkauditsjabloonregel bijwerken**.

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Ik kan een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder.

### <a name="issue-description"></a>Probleembeschrijving

Wanneer orderverzamelings- en verzendprocessen zijn ingeschakeld voor WMS, kunt u een pakbon niet annuleren nadat deze is geboekt vanuit een verkooporder.

### <a name="issue-resolution"></a>Probleemoplossing

Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor WMS, moet u de boeking uitvoeren vanuit de lading, niet vanuit de order. Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. In het algemeen kan een verkooporder die is verzameld en verzonden via magazijnbeheerprocessen met de pakbon worden bijgewerkt vanuit de lading of zending en het verkooporderdocument zelf. Als u de verkooporder echter met de pakbon bijwerkt vanuit het verkooporderdocument, kan de pakbon nog steeds niet worden teruggeboekt vanuit de lading of verkooporder. Daarom wordt u aangeraden de pakbonboeking uit de lading te gebruiken. In dit geval wordt de terugboeking ingeschakeld die moet worden uitgevoerd vanuit de lading.

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>Het volgende foutbericht wordt weergegeven: "Er is niet genoeg werk gevonden voor het cluster."

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u het proces *Door systeem gestuurde clusterverzameling* gebruikt en een clusterprofiel configureert waarbij bijvoorbeeld tien posities kunnen worden verzameld, werkt het proces zoals gepland wanneer er voldoende werk is om te worden verzameld tot tien posities. Als er echter slechts acht posities moeten worden verzameld, ontvangt u dit foutbericht, omdat er onvoldoende werk voor één cluster is.

### <a name="issue-resolution"></a>Probleemoplossing

U kunt dit probleem oplossen door het clusterprofiel te bewerken en de optie **Posities activeren** in te stellen op *Nee*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]