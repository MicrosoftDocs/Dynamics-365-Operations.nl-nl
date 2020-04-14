---
title: Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen
description: In dit onderwerp wordt uitgelegd hoe u antwoorden op een offerteaanvraag invoert, biedingen met elkaar vergelijkt en vervolgens het contract toekent aan een van de leveranciers.
author: mkirknel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 888b8ea8a4ca0c48706442308309588bf25d47d9
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149545"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a>Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u antwoorden op een offerteaanvraag invoert, biedingen met elkaar vergelijkt en vervolgens het contract toekent aan een van de leveranciers. U kunt deze procedure gebruiken in het demobedrijf **USMF**.

Voordat u met deze procedure begint, moet u een offerteaanvraag hebben met twee regels die aan ten minste twee leveranciers is verzonden. Voltooi de procedure [Een offerteaanvraag maken](create-request-quotation.md) om deze offerteaanvraag te maken. Ook moeten er beoordelingscriteria worden ingesteld voordat u deze procedure kunt voltooien.

U kunt het bod invoeren als leverancier of als inkoopmedewerker. Zie voor meer informatie [Samenwerking met leveranciers instellen en onderhouden](../set-up-maintain-vendor-collaboration.md).

## <a name="enter-a-reply-as-a-vendor"></a>Een antwoord invoeren als leverancier

1. Selecteer op het dashboard de optie **Biedingen van leverancier**.
2. Zoek in de lijst **Uitnodigingen voor nieuw bod** een offerteaanvraag die zojuist is verzonden. Selecteer de offerteaanvraag om te controleren wat er is aangevraagd.
3. Selecteer **Bijlagen voor offerteaanvraag** om bijlagen te controleren die zijn toegevoegd.
4. Selecteer **bieding** om de velden bewerkbaar te maken. Zoals u ziet, is het veld **Voortgang bieding** ingesteld op **Leverancier is bezig met bijwerken**.
5. Voer in de kop en in de regels de waarden van het antwoord op de bieding in.
6. Selecteer **Bijlagen bij biedingen** als er bijlagen moeten worden toegevoegd aan de bieding.
7. Selecteer het sneltabblad **Biedrichtlijnen voor artikelen** om te bekijken of documenten zijn vereist.
8. Selecteer het sneltabblad **Aanpassingen** om te bekijken of de offerteaanvraag is gewijzigd.
9. Selecteer het sneltabblad **Vragenlijst**. Eventuele vragenlijsten die hier worden weergegeven, moeten worden beantwoord.
10. Selecteer het sneltabblad **Regeldetails** om uitgebreide informatie over de regel weer te geven.
11. Selecteer **Opnieuw instellen vanuit offerteaanvraag** alleen als u de waarden die zijn ingevoerd moet terugzetten naar de oorspronkelijke waarden voor de offerteaanvraag.
12. U kunt het bod op elk gewenst moment opslaan en later extra verwerkingen uitvoeren, mits de vervaldatum en -tijd niet zijn verstreken. In dit geval kunt u de bieding vinden in de lijst **Biedingen in uitvoering** in het werkgebied **Biedingen van leverancier**.
13. Selecteer de bieding al is verzonden, selecteert u **Verzenden**. Als u geen bod wilt doen, selecteert u **Weigeren**. Aangeboden biedingen zijn beschikbaar in de lijst **Ingediende biedingen** in het werkgebied **Biedingen van leverancier**.  
14. Nadat het bod is ingediend, kunt u dit op elk gewenst moment vóór de vervaldatum en -tijd intrekken. Houd er rekening mee dat wanneer een bod wordt ingetrokken, het niet als ingediend wordt behandeld. Wanneer het bod wordt geaccepteerd of afgewezen door de inkoopafdeling, verschijnt het in de lijst **Toegekende biedingen** of **Verloren biedingen** in het werkgebied **Biedingen van leverancier**.  

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a>Een antwoord van een leverancier invoeren als inkoopmedewerker

1. Controleer of de machtiging voor het bewerken van leveranciersbiedingen is ingesteld. Ga naar **Inkoop en sourcing \> Instellen \> Parameters voor Inkoopbeheer**. Stel op het tabblad **Offerteaanvragen** de optie **Inkoper kan bieding van leveranciers bewerken** in op **Ja**.
2. Ga naar **Inkoopbeheer \> Offerteaanvragen \> Alle offerteaanvragen**.
3. Selecteer een offerteaanvraag met de status **Verzonden** en selecteer vervolgens de koppeling in het veld **Aanvraag voor offertecase**.
4. Selecteer **Reacties beheren**. Op de pagina die wordt weergegeven, wordt een offerteaanvraag weergegeven voor elke leverancier die u hebt uitgenodigd om te bieden.
5. Selecteer een offerteaanvraag die nog niet is beantwoord. (Het veld **Voortgang van reactie** moet zijn ingesteld op **Niet gestart**.)
6. Selecteer **Bewerken \> Reactie op offerteaanvraag bewerken**. De pagina **Antwoord op offerteaanvraag** wordt weergegeven. Als inkoopmedewerker kunt u nu de reactie invoeren namens de leverancier. Zoals u ziet, is het veld **Voortgang bieding** ingesteld op **Inkoper is bezig met bijwerken**.  
7. Voer de biedgegevens in. Wanneer u klaar bent, selecteert u **Verzenden**.

## <a name="score-the-bids"></a>De biedingen beoordelen

1. Selecteer op de pagina **Alle aanvragen voor offertes** de offerteaanvraagcase waarvoor u de antwoorden wilt beoordelen.
2. Selecteer **Reacties beheren**.
3. Selecteer het antwoord dat u wilt beoordelen.
4. Selecteer **Koptekst** zodat u de beoordeling voor het bod kunt weergeven.
5. Voer op het sneltabblad **Scoring bieding** een nummer in het veld **Score** in voor een van de scoringscriteria. Als u de muis boven een scoringscriterium plaatst, wordt met knopinfo het bereik weergegeven waarbinnen de score moet vallen. In deze demo kunt u een getal tussen 1 en 5 invoeren voor elke van de scoringscriteria.  
6. Herhaal stap 5 voor een ander scoringscriterium.
7. Als de offerteaanvraagcase een vragenlijst heeft die naar de leveranciers is verzonden, kunt u de leveranciersantwoorden invoeren op het sneltabblad **Vragenlijsten**.
8. Sluit de pagina.
9. Herhaal stap 1 tot en met 8 voor alle andere biedingen.

## <a name="compare-the-replies"></a>De antwoorden vergelijken

1. Selecteer in het actievenster op het tabblad **Algemeen** de optie **Antwoorden vergelijken**.
2. Voer een getal in het veld **Positie** in.  
    - Deze pagina bevat de biedingen, samen met de koptekst en de regelinformatie en de totale score op koptekstniveau. U kunt de regels vergelijken door het raster zo te sorteren dat vergelijkbare regels zich naast elkaar bevinden. De volgende informatie wordt eveneens opgenomen:
    - **Hoeveelheid**: de hoeveelheid die door de leverancier is aangeboden. Deze hoeveelheid komt mogelijk niet overeen met de hoeveelheid die is opgegeven in de offerteaanvraag.
    - **Nettobedrag**: de prijs die door een leverancier is opgegeven voor de artikelen op de regel, na aftrek van eventuele kortingen.
    - **Afwijking**: het aantal dagen dat de leveringsdatum in de koptekst of de regel van de bieding afwijkt van de gevraagde leveringsdatum in de koptekst van de offerteaanvraag of de offerteaanvraagregel. U kunt voor elke bieding een positie invoeren:  
3. Selecteer de koptekstregel voor de andere bieding waaraan u een positie wilt toekennen.
4. Voer een getal in het veld **Positie** in.
5. Selecteer **Opslaan**.

## <a name="reject-a-bid"></a>Een bieding afwijzen

1. Selecteer de koptekstregel voor de bieding die u wilt afwijzen. U kunt slechts de regels in één bieding of één bieding tegelijk accepteren, afwijzen of retourneren.
2. Schakel het selectievakje **Markeren** in.  
    - Als u het selectievakje **Markeren** in de koptekst van de bieding inschakelt, worden ook alle regels gemarkeerd. Als u slechts een deel van de regels van het bod wilt weigeren of accepteren, kunt u alleen die regels markeren. Bovendien kunt u een bod van een leverancier accepteren voor sommige regels van een offerteaanvraag en andere regels toekennen aan een andere leverancier. U moet echter wel telkens één bod tegelijk doen.  
    - Als er alternatieve regels aanwezig zijn, kunt u de originele biedingsregel accepteren of het bijbehorende alternatief, maar niet beide.  
3. Selecteer **Afwijzen**.
4. Selecteer **Parameters** en voer vervolgens in het veld **Reden afwijzing** uw reden voor het afwijzen van het bod in of selecteer deze. De reden wordt opgeslagen in het antwoord.  
5. Selecteer **OK**.
6. Selecteer **OK**.

## <a name="accept-a-bid"></a>Een bieding accepteren

1. Selecteer de bieding die u wilt accepteren en selecteer vervolgens de koppeling in het veld **Offerteaanvraag**. Als u zich op de pagina **Antwoorden op offerteaanvraag vergelijken** bevindt, is het gemarkeerde bod met focus het bod dat het systeem in overweging zal nemen tijdens de actie Accepteren. U kunt telkens slechts regels van één bod accepteren.  
2. Selecteer **Beantwoorden** in het actievenster.
3. Selecteer **Accepteren**. Als u alleen specifieke regels hebt gemarkeerd, bevat de actie Accepteren alleen die regels. Als u alle regels in de bieding wilt accepteren, hoeft u de regels niet te markeren.  
4. Selecteer **Parameters** en voer vervolgens in het veld **Reden accepteren** uw reden voor het accepteren van het bod in of selecteer deze. De reden wordt opgeslagen in het bod.  
5. Selecteer **OK**.
6. Selecteer **OK**. Wanneer u **OK** selecteert, wordt een inkooporder gegenereerd op basis van de regels die in de acceptatie van de offerteaanvraag zijn opgenomen. Als er andere biedingen zijn die niet zijn verwerkt (geaccepteerd, afgewezen of geretourneerd), wordt u door het systeem gevraagd deze te weigeren.  

## <a name="view-the-purchase-order-that-is-generated"></a>De inkooporder weergeven die wordt gegenereerd.

Selecteer in het actievenster op het tabblad **Algemeen** de optie **Inkooporder**. Op de pagina die wordt weergegeven ziet u de inkooporder die is gegenereerd toen u de bieding accepteerde.
