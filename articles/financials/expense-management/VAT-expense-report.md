---
title: Btw-restitutie in Onkostenbeheer
description: In dit onderwerp wordt uitgelegd hoe u btw-restituties ontvangt op in aanmerking komende transacties.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bc9e533de40aa8fe8ddfe422cfe0f4078a360c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "359561"
---
# <a name="vat-recovery-in-expense-management"></a>Btw-restitutie in Onkostenbeheer

[!include [banner](../includes/banner.md)]

Om restituties van daarvoor in aanmerking komende btw-transacties te ontvangen, moet een bedrijf of organisatie nauwkeurige informatie opgeven, verzamelen, controleren en indienen. Dit proces bestaat uit meerdere taken waarbij, afhankelijk van de grootte van uw bedrijf, meerdere werknemers of functies betrokken kunnen zijn.

Er moet aan het volgende zijn voldaan om btw te kunnen terugvorderen in Onkostenbeheer:

- Er moeten btw-codes zijn gemaakt voor landen/regio's die aan onkostencategorieën zijn toegewezen.
- Voor elke btw-code moet een btw-groep zijn gemaakt.
- Voor elke btw-groep moet een btw-code voor het artikel zijn gemaakt.

Wanneer aan deze vereisten is voldaan, kunnen werknemers deze stappen uitvoeren om restitutie van btw-transacties aan te vragen.

1. Voer in een onkostennota btw-informatie in over creditcardtransacties om in aanmerking komende btw-restituties te identificeren.
2. Zorg ervoor dat alle btw-informatie volledig is en boek vervolgens de onkostennota.
3. Verwerk onkosten die in aanmerking komen voor internationale btw-restitutie.
4. Verzend btw-restitutiegegevens naar de externe leverancier om internationale restitutieretouren in te dienen.
5. Verwerk onkosten voor nationale btw-restitutie.

De volgende secties bevatten voorbeelden die laten zien hoe dat werknemers van Contoso elke stap uitvoeren.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>In een onkostennota btw-informatie invoeren over creditcardtransacties om in aanmerking komende btw-restituties te identificeren

Nancy, een verkoopvertegenwoordiger van Contoso uit de VS, is onlangs teruggekeerd van een zakenreis naar het Verenigd Koninkrijk. Tijdens haar reis heeft ze enkele kosten voor maaltijden met haar persoonlijke creditcard betaald. Nancy moet nu een onkostennota maken om haar onkosten te declareren.

Wanneer Nancy informatie in haar onkostennota invoert, selecteert ze **Verenigd Koninkrijk** in het veld **Land/regio** op de pagina **Onkostennota bewerken**. De lijst met btw-groepen wordt vervolgens gefilterd zodat alleen de groepen worden weergegeven die voor het Verenigd Koninkrijk van toepassing zijn. Nancy selecteert de btw-groep **Verenigd Koninkrijk 001** en selecteert vervolgens de btw-groep voor artikel **Maaltijden**. Nancy voegt vervolgens een nieuwe transactie toe voor haar verblijf. Omdat er maar één btw-groep en btw-groep voor artikel voor verblijf is in het Verenigd Koninkrijk, wordt deze informatie automatisch in de onkostennota van Nancy ingevuld.

Het is beleid bij Contoso dat alle onkosten een overeenstemmend betaalbewijs hebben. Daarom ontvangt Nancy als zij haar onkostennota opslaat, een bericht dat zij een betaalbewijs moet toevoegen voor elke transactie die zij in haar onkostennota vermeld. Nancy controleert of ze een digitale kopie van elk betaalbewijs bij elke transactie aan haar onkostennota heeft toegevoegd en dient haar onkostennota voor goedkeuring in. Daarna stuurt ze de papieren betaalbewijzen naar het back office-verwerkingsteam. Dit team stuurt de btw-restitutiegegevens naar de leverancier die internationale btw-restitutie voor Contoso archiveert.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Zorgen dat alle btw-informatie volledig is en vervolgens de onkostennota boeken

April, de coördinator voor leverancierbetalingen voor Contoso, moet alle btw-gegevens invoeren die in een onkostennota ontbreken, voordat de nota kan worden geboekt. Ze opent de pagina **Onkostennotagegevens** en ziet de goedgekeurde onkostennota van Nancy. April opent vervolgens de onkostennota om de details van de transacties te bekijken. April ziet dat Nancy voor een van de transacties geen btw-groep voor het artikel heeft ingevoerd. Omdat deze informatie niet is opgegeven, kan April de onkostennota niet boeken. April kijkt daarom op de pagina **Belastingconfiguraties** in Onkostenbeheer en vindt de juiste btw-groep voor het artikel voor het land/de regio en het transactietype. Nu kan April de onkostennota naar het grootboek boeken.

Wanneer April de onkostennota boekt, wordt een werkitem voor btw-restitutie gemaakt. Dit werkitem wordt toegewezen aan een lid van het back office-verwerkingsteam. April ontvangt een bericht waarin wordt bevestigd dat de boeking geslaagd is. Dit bericht bevat ook het nummer van de btw-transacties dat voor restitutie is aangeduid.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Onkosten verwerken die in aanmerking komen voor internationale btw-restitutie

Arnie, een lid van het back office-verwerkingsteam van Contoso, moet controleren of alle vereiste informatie voor btw-restitutie in onkostennota's is opgenomen. Hij opent de pagina **Onkosten belastinginning** en selecteert de onkostennota die Nancy heeft ingediend. Arnie controleert of alle vereiste betaalwijzen zijn bijgevoegd en of de juiste btw-groep en btw-codes voor artikel zijn ingevoerd.

Wanneer Arnie de papieren betaalbewijzen van Nancy ontvangt, vergelijkt hij de papieren ontvangstbewijzen met de digitale ontvangstbewijzen en verandert hij de status van de onkostennota in **Klaar voor terugvordering**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Btw-restitutiegegevens naar de externe leverancier verzenden om internationale restitutieretouren in te dienen

Wanneer Arnie gereed is om de gegevens van de onkostennota te verzenden naar de externe leverancier die de btw-restitutieretouren gaan indienen, opent hij de pagina **Onkosten belastinginning**. Arnie filtert de pagina zo dat alleen de onkostennota's worden weergegeven die zijn gemarkeerd als **Klaar voor terugvordering**. Arnie klikt vervolgens op **Bestand** &gt; **Exporteren naar Excel**. De btw-gegevens uit de onkostennota's worden geëxporteerd naar een Microsoft Excel-werkblad. Arnie dient dit werkblad in bij de externe leverancier en voegt een bericht toe dat de papieren ontvangstbewijzen per koerier zijn verzonden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Onkosten verwerken voor nationale btw-restitutie

Arnie moet controleren of de transacties op de onkostennota in aanmerking komen voor btw-restitutie en of de digitale betaalbewijzen aan de nota's zijn toegevoegd. Om de verwerking van de onkosten voor nationale restitutie te starten, opent Arnie de pagina **Onkosten belastinginning** en selecteert hij de onkostennota die gecontroleerd moet worden. Hij controleert of de betaalbewijzen op naam van het bedrijf staan in plaats van de werknemer. De btw-restitutie moeten de betaalbewijzen op naam van het bedrijf staan. Arnie controleert vervolgens of de juiste btw-groep en btw-codes voor artikel zijn toegepast.

Wanneer Arnie de papieren betaalbewijzen ontvangt, verandert hij de status van de onkostennota naar **klaar voor terugvordering**. Hij kan vervolgens de restitutie bij de juiste belastingdienst indienen. In dit geval is de juiste belastingdienst in de VS de Internal Revenue Service (IRS).
