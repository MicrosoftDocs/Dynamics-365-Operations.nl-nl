---
title: Betalingsmethode van klant vaststellen
description: Maak een betalingsmethode voor klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab035c6268b701c78da32d589e99ece38c31781d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348958"
---
# <a name="establish-customer-method-of-payment"></a>Betalingsmethode van klant vaststellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Maak een betalingsmethode voor klantbetalingen. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Klanten > Betalingsinstelling > Betalingsmethoden.
2. Klik op Nieuw.
3. Voer in het veld Betalingsmethode een id voor de betalingsmethode in.
    * De id voor de betalingsmethode wordt weergegeven op facturen en betalingen. Maak deze dus beschrijvend genoeg om te begrijpen welk type betaling wordt geregistreerd en voor welke bankrekening.  
4. Voer in het veld Beschrijving een omschrijving in.
5. Selecteer welke betalingsstatus is vereist voor het boeken van betalingen.
    * Bij het maken van een klantbetaling kan deze alleen worden geboekt als de betalingsstatus overeenstemt met de betalingsstatus die u hier definieert.  
6. Selecteer hoe betalingen van klanten voor facturen moeten worden gemaakt.
    * Deze optie wordt alleen gebruikt bij het uitvoeren van een betalingsvoorstel. Een betalingsvoorstel kan worden gebruikt voor klantbetalingen bij het doen van automatische afschrijvingen en het afschrijven van de fondsen van de bankrekeningen van klanten.  
7. Selecteer het type betaling.
    * Het betalingstype helpt om te bepalen of al dan niet enige validatie zal plaatsvinden voor de betaling.  
8. Selecteer naar welke betalingen van het rekeningtype zal worden geboekt.
    * Normaal gesproken moet Bank zijn geselecteerd voor deze optie.  
9. Selecteer de bankrekening waarop deze betaling worden geregistreerd.
10. Voer het banktransactietype in die het type betaling aangeeft dat door uw bank wordt gebruikt.
    * Het banktransactietype wordt gebruikt tijdens het bankafstemmingsproces en kan afstemming eenvoudiger maken.  
11. Selecteer of deze betaling tijdelijk naar een overbruggingsrekening zal worden geboekt.
    * Als u wilt weten hoe lang het duurt voordat een betaling wordt vrijgegeven door de bank, gebruikt u de functionaliteit Overbrugging. De betaling wordt tijdelijk naar een grootboekrekening geboekt totdat deze wordt vrijgegeven door de bank. Op dat moment wordt de betaling naar de bankrekening verplaatst die u hier definieert.  
12. Voer de hoofdrekening in die wordt gebruikt voor de overbruggingsboeking.
    * Dit is de hoofdrekening waarnaar de betaling tijdelijk wordt geboekt bij gebruik van overbrugging.  
13. Gebruik het tabblad Bestandsindeling om instelling voor elektronische betalingen te definiëren.
14. Gebruik het tabblad Betalingsbeheer om velden die verplicht zijn te definiëren.
    * Als u bijvoorbeeld vereist dat alle betalingen met deze betalingsmethode worden gestort, kunt u die optie kiezen op dit tabblad.  
15. Gebruik het tabblad Betalingskenmerken om te bepalen welke betalingskenmerken u voor deze betalingsmethode wilt gebruiken.
16. Klik op Opslaan.

