---
title: Artikelen en grondstoffen in voorraad, productie en verkoop traceren
description: Dit onderwerp beschrijft hoe u artikeltracering kunt gebruiken om te bepalen waar de artikelen of de grondstoffen zijn gebruikt, worden gebruikt, of gebruikt gaan worden in productie- en verkoopprocessen.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f45c39769b71832afe531db8a55097ede8a3c769
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562525"
---
# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Artikelen en grondstoffen in voorraad, productie en verkoop traceren

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft hoe u artikeltracering kunt gebruiken om te bepalen waar de artikelen of de grondstoffen zijn gebruikt, worden gebruikt, of gebruikt gaan worden in productie- en verkoopprocessen.

De functionaliteit van de artikeltracering is beschikbaar op de pagina **Traceren artikel**. De volgende secties beschrijven hoe u artikeltracering kunt gebruiken, en welke opties en beperkingen er zijn.

## <a name="what-is-item-tracing"></a>Wat is artikeltracering?
Artikeltracering is een BI-hulpmiddel (business intelligence) dat inzicht geeft in de bron en eindbestemming van artikelen en grondstoffen in de leveringsketen. Fabrikanten kunnen de leverancier van artikelen, grondstoffen of ingrediënten traceren en de productie en verkoop van het eindproduct doorsturen. De artikeltracering helpt fabrikanten aan regelgevende vereisten te voldoen, en helpt ook kwaliteitsambtenaren en productiemanagers afwijkingen in de kwaliteit van producten en materialen te analyseren en daarop actie te ondernemen. Hier volgen enkele voorbeelden van de manier waarop fabrikanten artikeltracering kunnen gebruiken:

-   De kwantiteit van een artikel of een grondstof die momenteel in voorraad is identificeren, en bepalen waar dit is opgeslagen.
-   Bepalen hoeveel van het artikel of de grondstof is verzonden en naar welke klanten als het is verzonden.
-   Geplande zendingen identificeren die het artikel of de grondstof bevatten.
-   Productieorders zoeken die het artikel of de grondstof gebruiken en die worden gepland, in uitvoering zijn of gereed zijn gemeld.
-   Te weten komen waar het artikel of de grondstof is ingekocht.
-   Onderzoeken waar een artikel of een grondstof in de productie van een ander artikel is verbruikt.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Wat kan ik traceren, en zijn er eventuele beperkingen?
U kunt historische voorraadtransacties voor artikelen en grondstoffen traceren via een artikelnummer en een traceringsdimensie, zoals een serienummer, batchnummer of een leveranciersbatchnummer. U kunt een artikel of grondstof alleen traceren als er een traceringsdimensie aan is toegewezen. Omdat de tracering is gebaseerd op voorraadtransacties, zijn er bepaalde beperkingen tijdens het traceren van artikelen. Er zijn bijvoorbeeld beperkingen wat betreft transacties voor projecten, vaste activa en detailhandel. Bovendien worden de co-producten weergegeven in de traceringsdetails, maar zijn de bijproducten niet opgenomen. De tracering bevat alle magazijntransacties van de ene locatie naar een andere. Daarom kan de hoeveelheid informatie overweldigend zijn. De tracering wordt weergegeven voor één rechtspersoon tegelijk. Er zijn geen capaciteiten voor meerdere bedrijven in een intercompany-context. U moet een nieuwe tracering voor elk bedrijf starten waar een artikel wordt ontvangen of uitgegeven.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Welke criteria kan ik voor een artikeltracering opgeven?
De criteria die voor een artikeltracering vereist zijn, zijn het artikelnummer, een traceringsdimensie (zoals een of batchnummer of een serienummer) en de richting. De volgende tabel beschrijft de criteria die u in een artikeltracering kunt gebruiken.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Veldgroep</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Artikelnummer</td>
<td>Voer de ID van het artikel of de grondstof in dat u traceert.</td>
</tr>
<tr class="even">
<td>Productdimensies</td>
<td>Optioneel: Tracering-specifieke aspecten van de productdefinitie, zoals een configuratie, een grootte, kleur, een of een stijl.</td>
</tr>
<tr class="odd">
<td>Traceerdimensies</td>
<td>Voer een leveranciersbatchnummer, batchnummer of serienummertraceringsdimensie in. Wanneer u het batchnummer als criterium gebruikt, wordt het leveranciersbatchnummer weergegeven als u die informatie hebt vastgelegd.</td>
</tr>
<tr class="even">
<td>Opslagdimensies</td>
<td>Optioneel: Traceringsartikelen die in een specifieke locatie zijn opgeslagen.</td>
</tr>
<tr class="odd">
<td>Periode</td>
<td>Optioneel: Voer datums in om de tracering tot een specifieke periode te beperken. De traceringsdetails geven alleen documenten en transacties weer die tussen die datums zijn gemaakt.</td>
</tr>
<tr class="even">
<td>Vooruit of achteruit</td>
<td>Selecteer de richting voor de tracering. U kunt voorwaarts of achterwaarts traceren:
<ul>
<li><strong>Achteruit</strong> – Traceer downstream voor bepaling van de bron, de hoeveelheid die op voorraad blijft en alle productieorders die tenminste gedeeltelijk zijn gereedgemeld.</li>
<li><strong>Vooruit</strong> – Traceer upstream om het eindpunt te identificeren. Het is mogelijk te zoeken naar de verkooporders en de klanten naar wie het getraceerde artikel of grondstof tenminste gedeeltelijk is verzonden.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>De informatie is opgenomen in de traceringsdetails?
De resultaten van een tracering worden weergegeven in chronologische volgorde in de structuur op het sneltabblad **Details** van de pagina **Traceren artikel**. De volgorde kan verschillen, afhankelijk van de traceringsrichting. De details omvatten alle transacties van de inkoop van het artikel van de leverancier tot de verkoop van het artikel aan de klant. De traceringsresultaten bevatten ook tussentijdse producten die aan het artikel zijn gekoppeld of aan de traceringsdimensie, zoals opgegeven in de traceringscriteria. Het hoofdknooppunt geeft de artikelhoeveelheid in de voorraadeenheid weer die er volgens de opslagdimensies die in de traceringscriteria zijn opgegeven nog is. **Opmerking:** De traceringsdetails bieden een momentopname van de informatie die beschikbaar is toen de tracering werd uitgevoerd. De traceringsdetails worden niet bijgewerkt als gegevens zijn gewijzigd nadat de tracering is uitgevoerd.

## <a name="why-dont-some-nodes-contain-any-details"></a>Waarom bevatten sommige knooppunten geen gegevens?
Om de hoeveelheid informatie in de traceringsdetails te beperken, bevat alleen het knooppunt voor het eerste exemplaar van het artikel of de grondstof details. Als een geselecteerd knooppunt geen details bevat, kunt u het knooppunt dat wel details bevat, weergeven door op **Ga naar getraceerde regel** te klikken. U kunt vervolgens teruggaan naar het knooppunt dat u verliet door op **Ga terug** te klikken.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Kan ik alleen een bepaald type document inzien? Kan ik bijvoorbeeld alleen productieorders, klanten of leveranciers inzien?
Ja, u kunt vanuit de traceringsdetails lijstpagina's openen die alleen een bepaald type document of transactie bevatten. U kunt deze pagina's vanuit het menu-item **Tracering** in het actievenster in de groepen **Artikel**, **Verkoop**, **Inkoop**, **Productie** en **Kwaliteit** openen. Als u bijvoorbeeld een lijst met de leveranciers in de traceringsdetails wilt weergeven, klikt u op **Tracering** &gt; **Inkoop** &gt; **Leveranciers**. De lijstpagina's zijn een samenvatting van de documenten of de transacties van de traceringsdetails. De lijstpagina's **Transacties in behandeling**, **Orders in behandeling** en **Verkooporders die niet zijn verzonden** geven ook informatie die niet is opgenomen in de traceringsdetails. Bovendien tonen ze altijd resultaten vanaf de huidige datum, ongeacht of een datumbereik is opgegeven. De volgende tabel beschrijft aanvullende details die deze pagina's kunnen bevatten.

| Lijsten                    | Beschrijving                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verkooporders die niet zijn verzonden | Bekijk verkooporderregels die niet zijn gepickt en daarom niet zijn weergegeven in de traceringsdetails.                                                                                                                                                                                                                        |
| Orders in behandeling           | Bekijk alle openstaande productieorders voor het getraceerde artikel, ongeacht de traceringsdimensies die in de traceringscriteria zijn gebruikt. U kunt ook openstaande productieorders inzien waar het getraceerde artikel een ingrediënt is, en waar er geen registraties zijn gemaakt en er geen transacties gereed zijn gemeld voor de order. |
| Transacties in behandeling     | Openstaande voorraadtransacties inzien voor het getraceerde artikel dat de opgegeven traceringsdimensies of een lege traceringsdimensie bevat. U kunt ook openstaande voorraadtransacties voor artikelen en traceringsdimensiecombinaties, of een lege waarde in de traceringsdetails inzien.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Hoeveel niveaus kan ik omhoog of omlaag traceren in een stuklijst of formule?
U kunt één niveau omhoog of omlaag traceren in een stuklijst of formule. Stel, u voert een tracering voor grondstoffen uit. Dan kunt u het eindproduct en eventuele coproducten zien. Als u echter een co-product traceert, bevatten de traceringsdetails het eindproduct niet.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Hoe kan ik meer details over een document of transactie in de traceringsdetails zien?
Op het sneltabblad **Details** kunt u op twee manieren meer gegevens over een geselecteerd document of transactie in de traceringsdetails weergeven:

-   Als u een knooppunt in de traceringsdetails op het sneltabblad **Details** selecteert, geven de andere Sneltabbladen op de pagina informatie over het document of transactie in het knooppunt.
-   Open de detailpagina voor het document in een geselecteerd knooppunt door op **Details weergeven** te klikken. Stel, als u een knooppunt selecteert dat een productieorder beschrijft en u klikt op **Details weergeven**, dan wordt de pagina **Details van productieorders** weergegeven.

Een aantal sneltabbladen biedt toegang tot extra informatie over het geselecteerde knooppunt. Bijvoorbeeld, op het sneltabblad **Non-conformiteiten** kunt u controleren of er een historie van niet-conformering is door op **Query's** te klikken. Op het sneltabblad **Batch** kunt u klikken op **Voorhanden lijst** om de hoeveelheid voorraad die er momenteel voorhanden is in te zien, en alle voorraadtransacties die met de batch te maken hebben.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Kan ik meer dan een tracering uitvoeren en vervolgens de details vergelijken?
Nadat u de tracering hebt uitgevoerd, kunt u de volgende opties op de knop **Tracering vanaf knooppunt** gebruiken om een nieuwe tracering van de transactie in het geselecteerde knooppunt uit te voeren:

-   **Achteruit** of **Vooruit** – Start een nieuwe tracering voor het geselecteerde knooppunt en overschrijf de details van de huidige tracering.
-   **Nieuw achterwaarts** of **Nieuw voorwaarts** – Start een nieuwe tracering in een nieuw venster en houdt de details van de huidige tracering.

Als u de optie **Nieuw achterwaarts** of **Nieuw voorwaarts** wilt gebruiken, moet u de functie **Openen in een nieuw venster** gebruiken om een nieuwe te tracering in een nieuw venster weer te geven.

## <a name="can-i-save-the-trace-details"></a>Kan ik de traceringsdetails opslaan?
U kunt de informatie op het tabblad <strong>Details</strong> opslaan als XML-bestand door op <strong>Exporteren</strong> in het actievenster onder de actie *<strong><em>Tracering</em></strong>* te klikken. Naast de traceringsdetails bevat het XML-bestand de traceringscriteria, het bovenliggende knooppunt en de voorhanden hoeveelheid. Het opslaan van de details van een tracering is handig, bijvoorbeeld als u de gegevens aan een kwaliteitsorder of andere conformiteitsdocumentatie wilt koppelen. U kunt opgeven waar het bestand wordt opgeslagen. Als u het bestand meteen wilt weergeven, schakelt u het selectievakje <strong>Document weergeven</strong> in. <strong>Opmerking:</strong> Het bestand wordt altijd opgeslagen, zelfs als u het alleen wilt weergeven. Standaard opent het XML-bestand in een browservenster. U kunt echter met de rechtermuisknop op het bestand klikken, <strong>Openen met</strong> selecteren en vervolgens het programma selecteren om de inhoud weer te geven.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Kan ik een saldo voor een bepaald artikel of een ingrediënt berekenen?
U kunt de informatie van de overzichtspagina´s exporteren naar Microsoft Excel. Open de relevante pagina, klik op het pictogram **Openen in Microsoft Office** en selecteer vervolgens **Exporteren naar Microsoft Excel**. Dit is vooral nuttig wanneer u een massasaldo voor een artikel of een ingrediënt van de pagina **Overzicht van transacties** wilt berekenen. Op de pagina **Overzicht van transacties** kunt u desgewenst op het artikel of het ingrediënt en de batch filteren en vervolgens de informatie naar Excel exporteren. In Excel kunt u bijvoorbeeld de voorhanden hoeveelheid isoleren, de hoeveelheid die is verkocht, en de hoeveelheid die in productie is gebruikt.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Kan ik onderzoeken of er een historie van problemen met artikelen of onbewerkte materialen is?
De traceringsdetails bevatten informatie over kwaliteitsorders en niet-conformeringen betreffende het artikel of de grondstof. U kunt een overzicht van kwaliteitsorders en niet-conformeringen weergeven door op **Kwaliteitsorders** of **Niet-conformeringen** te klikken in het Actievenster. **Opmerking**: Destructieve kwaliteitsorders kunnen meer dan één keer voorkomen in de traceringsdetails. Als een destructieve kwaliteitsorder voor een document wordt aangemaakt, zoals een inkooporder, wordt het weergegeven voor elke transactie voor dat document.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Zijn er rapportagecapaciteiten gerelateerd aan artikeltracering?
U kunt het rapport **Verzonden naar klanten** genereren om de hoeveelheid van het artikel of de grondstof die is verzonden, te identificeren, en de klanten waaraan deze is verzonden. Voor een query die is gerelateerd aan conformiteit kunt u het rapport voor alle klanten genereren. Voor een query die is gerelateerd aan klantenservice kunt u het rapport voor een bepaalde klant genereren. Als het product een grondstof is die in de productie van een voltooid artikel is gebruikt, wordt het voltooide artikel ook opgenomen. **Opmerking:** Als u de functies voor het verwijderen of archiveren van verkooporders gebruikt, bevatten de rapportresultaten ook alle verkooporders die zijn verwijderd of gearchiveerd.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Kan ik co- en bijproducten traceren?
U kunt co-producten traceren, maar u kunt een bijproduct niet traceren omdat traceringsdimensies meestal niet aan hen zijn toegewezen. Wanneer u een artikel traceert, bevatten de traceringsdetails alle gerelateerde co-producten. Een knooppunt dat een coproduct bevat, bevat het woord "coproduct" in de details. U kunt details over een co-product ook weergeven door het knooppunt in de traceringsdetails te selecteren, en vervolgens het sneltabblad **Productie** te openen.
