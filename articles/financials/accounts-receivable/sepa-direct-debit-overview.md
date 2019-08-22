---
title: Overzicht SEPA-automatische overschrijvingen
description: De gemeenschappelijke betalingsruimte voor de euro (SEPA) is ingesteld door de Europese Commissie en dicteert dat alle elektronische betalingen als binnenlands worden beschouwd, ongeacht het land/de regio waar de persoon, het bedrijf of organisatie en bank zich bevinden. Er een verschil tussen nationale en grensoverschrijdende betalingen. De SEPA omvat de 28 lidstaten van de Europese Unie (EU), en ook IJsland, Liechtenstein, Noorwegen, Zwitserland, Monaco en San Marino. De SEPA helpt met de opbouw van een markt voor betalingstransacties in de Europese Economische Ruimte (EEA). Uiteindelijk moet SEPA het aantal betaalindelingen verminderen waar banken, bedrijven en personen mee moeten werken.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 11144
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcb7585d344988e00093231f785c1a746226e4e0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836634"
---
# <a name="sepa-direct-debit-overview"></a>Overzicht SEPA-automatische overschrijvingen

[!include [banner](../includes/banner.md)]

De gemeenschappelijke betalingsruimte voor de euro (SEPA) is ingesteld door de Europese Commissie en dicteert dat alle elektronische betalingen als binnenlands worden beschouwd, ongeacht het land/de regio waar de persoon, het bedrijf of organisatie en bank zich bevinden. Er een verschil tussen nationale en grensoverschrijdende betalingen. De SEPA omvat de 28 lidstaten van de Europese Unie (EU), en ook IJsland, Liechtenstein, Noorwegen, Zwitserland, Monaco en San Marino. De SEPA helpt met de opbouw van een markt voor betalingstransacties in de Europese Economische Ruimte (EEA). Uiteindelijk moet SEPA het aantal betaalindelingen verminderen waar banken, bedrijven en personen mee moeten werken.   

<a name="what-is-the-goal-of-sepa-direct-debits"></a>Wat is het doel van de automatische incasso van SEPA?
---------------------------------------

Een automatische incasso van SEPA maakt het mogelijk voor een crediteur om fondsen te innen van de bankrekening van een klant, mits een ondertekend mandaat door de klant aan de crediteur is verleend. De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen. 

De automatische incasso van SEPA maakt, voor het eerst, een betaalmiddel dat gebruikt kan worden voor zowel nationale als grensoverschrijdende automatische incasso's in de 32 landen/regio's van SEPA. 

Er zijn twee beschikbare schema's: het schema Kern Automatische Incasso van SEPA en Business to Business (B2B) Automatische Incasso van SEPA. Beide schema's gebruiken dezelfde bestandsindeling.

## <a name="what-is-the-core-direct-debit-scheme"></a>Wat is het schema Kern Automatische Incasso?
Het SEPA-schema Kern Automatische Incasso is het basisschema. Het heeft de volgende kenmerken:
-   De overboeking van fondsen is in euro's (ook al hebben bankrekeningen mogelijk fondsen in verschillende valuta).
-   De klant en de crediteur moeten elk een rekening bij een kredietinstelling hebben die binnen SEPA valt.
-   De klant moet een ondertekend mandaat aan de crediteur verlenen.
-   De mandaten verlopen 36 maanden na de laatst uitgevoerde inning.
-   De crediteur moet mandaten bewaren zolang het mandaat geldig is en tenminste 14 maanden na de laatste inning.
-   Het schema kan voor één (enkelvoudig) of terugkerende automatische incasso's worden gebruikt.
-   Klanten hebben het recht op restitutie, zonder vragen, maximaal acht weken nadat hun rekening is gedebiteerd.

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>Wat is het Business to Business (B2B) Automatische Incassoschema van SEPA?
Het SEPA-schema B2B Automatische Incasso is van toepassing op business-to-business transacties en is gebaseerd op het SEPA-schema Kern Automatische Incasso. De belangrijkste verschillen zijn:
-   Het SEPA-schema B2B Automatische Incasso is niet toegestaan wanneer de klant een particulier (consument) is.
-   De klant heeft niet het recht om een restitutie van een geautoriseerde transactie te krijgen.
-   De banken van de klant moet ervoor zorgen dat de inning is geautoriseerd door de inning met de mandaatinformatie te controleren. De banken van klanten en klanten moeten akkoord gaan met de verificatie die voor elke automatische incasso wordt uitgevoerd.
-   Het schema biedt een kortere tijdlijn voor het presenteren van automatische incasso's en het verkleint de retourperiode.

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>Kan ik het schema COR1 gebruiken voor mandaten voor automatische afschrijving?
Ja. U kunt het COR1-schema voor automatische afschrijvingsmandaten van SEPA gebruiken in Oostenrijk, België, Duitsland, Frankrijk, Italië, Spanje en Nederland. Het schema geeft een korte pre-meldingsperiode voor de automatische afschrijving voor de crediteur.

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>Wat zijn de Internationale Bankrekeningnummers (IBAN) en Bankidentificatiecodes (BIC)?
Het Internationale bankrekeningnummer (IBAN) en de Bankidentificatiecode (BIC) worden gebruikt om elke rekening in de 32 landen/regio's van SEPA te identificeren. Voer de BIC in in het veld SWIFT-code en de IBAN in het veld IBAN. Beide velden staan op het sneltabblad Aanvullende identificatie in het tabblad Bankrekening op de pagina Bankrekeningen. Dit is waar voor zowel de bankrekening van de crediteur als de bankrekening van de klant.

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>Waar voer ik crediteuridentificaties in (Incasso-ID's)?
In SEPA wordt elke crediteur aangegeven met een unieke crediteuridentificatie. Deze identificatie laat de klant en diens bank elke automatische afschrijving filteren en de automatische incasso verwerken danwel afwijzen volgens klantinstructies. De leveranciers moeten om deze ID op hun bank vragen. In het veld Incasso-ID geeft u deze identificatie op voor de bankrekening van de rechtspersoon.

## <a name="what-are-mandates"></a>Wat zijn mandaten?
De klant tekent een mandaat dat de crediteur autoriseert om een betaling te innen en dat de bank van de klant opdraagt om de inning te betalen. De klant kan het mandaat in papier uitgeven of elektronisch. Standaard vervalt het mandaat 36 maanden nadat het automatische afschrijving voor het laatst is uitgevoerd.

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>Waar specificeer ik de Automatische incassobestandsindeling van SEPA (ISO 20022)?
De SEPA-gegevensindelingen zijn gebaseerd op de berichtnormen ISO 20022. Selecteer het selectievakje Algemene elektronische rapportage en selecteer de SEPA-kredietoverdrachtindeling wanneer u betalingsmethoden voor Klanten configureert. U gebruikt die betalingsmethode wanneer u een betalingsbestand in een journaal met klantbetalingen genereert.

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>In welke bestandsformaten kan ik bestanden voor SEPA automatische afschrijving maken?
U kunt elektronische betalingsbestanden genereren voor automatische incasso's van SEPA in de volgende bestandsindelingen:
-   Bestanden voor incassobetalingen van SEPA in de bestandsindeling PAIN.008.001.02 XML voor België, Duitsland, Spanje, Frankrijk, Italië en Nederland.
-   Bestanden voor incassobetalingen van SEPA in de bestandsindeling PAIN.008.001.02 XML voor Oostenrijk, en in de bestandsindeling PAIN.008.003.02 XML voor Duitsland.

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>Hoe werken restituties en teruggaven bij SEPA-incasso's?
Onder beide Automatische incassoschema's van SEPA hebben klanten bepaalde rechten op restituties. De klant kan elke geautoriseerde transactie tijdens een periode van acht weken na de vervaldatum intrekken, zonder daarvoor een reden geven. In het geval van ongeautoriseerde transacties is de periode uitgebreid tot 13 maanden na de vervaldatum. Gedane betalingen maakt u handmatig ongedaan met de knop Betaling annuleren op de pagina Klanttransacties.





