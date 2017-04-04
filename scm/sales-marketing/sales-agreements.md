---
title: Verkoopovereenkomsten
description: In dit artikel vindt u informatie over verkoopovereenkomsten. Een verkoopovereenkomst is een contract waarmee een klant toezegt specifieke hoeveelheden van producten te kopen of het product gedurende een specifieke periode te kopen, in ruil voor speciale prijzen en kortingen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4dd1eae27ae33837fbab16f764083168578d0a29
ms.lasthandoff: 03/31/2017


---

# <a name="sales-agreements"></a>Verkoopovereenkomsten

In dit artikel vindt u informatie over verkoopovereenkomsten. Een verkoopovereenkomst is een contract waarmee een klant toezegt specifieke hoeveelheden van producten te kopen of het product gedurende een specifieke periode te kopen, in ruil voor speciale prijzen en kortingen.

Een verkoopovereenkomst is een contract waarmee een klant toezegt om producten in een specifieke hoeveelheid of een specifiek bedrag in de loop der tijd te kopen in ruil voor speciale prijzen, speciale kortingen, en andere speciale voorwaarden, zoals betaling en leveringsvoorwaarden. De prijzen en kortingen van de verkoopovereenkomst vervangen de prijzen en kortingen die worden genoemd in eventuele bestaande handelsovereenkomsten.  

De geldigheidsperiode van een verkoopovereenkomst wordt bepaald door de velden **Begindatum** en **Vervaldatum** in de overeenkomst. De verkooporder van een klant kwalificeert voor de overeenkomstvoorwaarden als de gewenste verzenddatum van de order in de geldigheidsperiode ligt. Alle verkooporderregels die aan een verkoopovereenkomst zijn gekoppeld dragen bij aan afhandeling van die verkoopovereenkomst.  

U kunt een verkooporder direct van een verkoopovereenkomst maken door de actie **Vrijgaveorder** te gebruiken. Als alternatief kunt u een geldige verkoopovereenkomst selecteren wanneer u orders aanneemt (zie de sectie "Verkoopovereenkomsten toepassen in het bestelproces" van dit artikel).  

**opmerking:** In eerdere versies verkoopovereenkomsten zijn aangeduid als afroeporders voor verkoop.

## <a name="commitment-types"></a>Toezeggingstypen
Elke regel in een verkoopovereenkomst staat voor een toezegging om iets te verkopen. In het algemeen zijn er twee soorten toezegging:

-   **Waardetoezegging **- de klant gaat ermee akkoord om producten voor een specifiek bedrag te kopen.
-   **Hoeveelheidstoezegging **- de klant gaat ermee akkoord om een specifieke hoeveelheid producten te kopen.

Bovendien kan met een contract worden toegezegd dat de klant een bepaald product of producten in een productcategorie koopt. Door deze twee factoren (waarde versus hoeveelheid, en specifieke producten versus productcategorieën) te combineren, hebben we vier typen toezeggingen:

-   **Toezegging producthoeveelheid** - de klant gaat ermee akkoord om een specifieke hoeveelheid producten te kopen. Regels die dit toezeggingstype gebruiken, worden gedefinieerd door een artikelnummer en door de overeengekomen hoeveelheid en eenheid. Het veld **Bedrag** is niet beschikbaar.
-   **Toezegging productwaarde** - de klant gaat ermee akkoord om specifieke producten voor een specifiek bedrag te kopen. Regels die dit toezeggingstype gebruiken, worden gedefinieerd door een artikelnummer en het overeengekomen bedrag. De velden **Hoeveelheid** en **Eenheid** zijn niet beschikbaar.
-   **Waardetoezegging productcategorie** - de klant gaat ermee akkoord om producten van een specifieke verkoopcategorie voor een specifiek bedrag te kopen. Regels die dit toezeggingstype gebruiken, worden gedefinieerd door een verkoopcategorie in de hiërarchie van verkoopcategorieën en een bedrag. De velden **Hoeveelheid** en **Eenheid** zijn niet beschikbaar.
-   **Waardetoezegging** - de klant gaat ermee akkoord om willekeurige product(en) in een willekeurige categorie voor een specifiek bedrag te kopen. De velden **Hoeveelheid** en **Eenheid** zijn niet beschikbaar.

Regels in dezelfde verkoopovereenkomst kunnen verschillende typen toezeggingen hebben.

## <a name="pricing-terms-for-sales-agreements"></a>Prijsvoorwaarden voor verkoopovereenkomsten
Prijsvoorwaarden kunnen variëren, afhankelijk van het type verbintenis. Op een verkooporder die aan een verkoopovereenkomst is gekoppeld, overschrijven de prijsvoorwaarden van die verkoopovereenkomst alle andere prijsvoorwaarden die van toepassing zijn op basis van handelsovereenkomsten. De volgende tabel beschrijft de prijsgerelateerde velden die worden beïnvloed door elk toezeggingstype. "Ja" geeft aan dat het veld kan worden bijgewerkt op een orderregel.

| Toezeggingstype                   | Eenheidsprijs | Prijseenheid | Kortingspercentage | Contantkortingsbedrag |
|-----------------------------------|------------|------------|------------------|----------------------|
| Toezegging producthoeveelheid       | Ja        | Ja        | Ja              | Ja                  |
| Toezegging productwaarde          |            |            | Ja              |                      |
| Waardetoezegging productcategorie |            |            | Ja              |                      |
| Waardetoezegging                  |            |            | Ja              |                      |

## <a name="policies-for-sales-agreements"></a>Beleid voor verkoopovereenkomsten
Het volgende beleid beïnvloedt de manier waarop de koppeling tussen een verkoopovereenkomsttoezegging en de bijbehorende verkooporderregels werkt:

-   **Max is afgedwongen**: Het totale aantal of bedrag voor alle orderregels mag niet meer dan de hoeveelheid of het bedrag zijn dat is opgegeven op de gerelateerde toezegging.
-   **Prijs en korting zijn vast** – De prijs op een orderregel en de prijs op de bijbehorende toezegging kunnen niet verschillen. Als de prijs op de orderregel wordt gewijzigd, wordt de koppeling naar de toezegging verbroken. Als de koppeling wordt verbroken, draagt de orderregel niet bij aan het voldoen aan de toezegging.
-   **Minimale vrijgavebedrag** en **Maximale vrijgavebedrag** – Als een bedrag wordt opgegeven, wordt een bericht weergegeven als u een wijziging aanbrengt in een orderregel, waardoor de orderregel afwijkt van de gerelateerde toezegging.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Berekeningen voor het voldoen aan verkoopovereenkomsten
Het tabblad **Uitvoering** op het sneltabblad **Regeldetails** op de pagina **Verkoopovereenkomsten** bevat uitvoeringshoeveelheden en bedragen.  

In het gebied **Uitvoering** kunt u de totale aantallen en bedragen voor alle orderregels zien die zijn gekoppeld aan de opgegeven verkoopovereenkomst. U kunt ook het resterende bedrag of hoeveelheid weergeven die nodig is om te voldoen aan de toezegging.  

In het gebied **Overeenkomst** kunt u de aantallen en bedragen weergeven van de opgegeven verkoopovereenkomst. Deze aantallen en bedragen zijn de totale aantallen en bedragen die toegewezen zijn.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Bevestigingen en versiegeschiedenis voor verkoopovereenkomsten
Als u een verkoopovereenkomst bevestigt, wordt de huidige versie van de verkoopovereenkomst opgeslagen in een tabelgeschiedenis. Als u de verkoopovereenkomst wijzigt, kunt u deze opnieuw bevestigen om een andere versie van de verkoopovereenkomst in de geschiedenis op te slaan.  

Als u een verkoopovereenkomst niet bevestigt, kunt u deze nog steeds gebruiken om verkooporders te maken. Geschiedenisinformatie voor de verkoopovereenkomst wordt echter niet opgeslagen.  

U kunt alle versies van de bevestigingen bekijken of afdrukken. Vervolgens kunt u de wijzigingen delen met uw klant voor goedkeuring.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Verkoopovereenkomsten toepassen tijdens het bestelproces
Als u verkooporders niet rechtstreeks voor een verkoopovereenkomst vrijgeeft, kunt u een verkoopovereenkomst nog altijd koppelen aan een order tijdens het invoeren van orders. Wanneer u een nieuwe verkooporder maakt en een verkoopovereenkomst selecteert, worden de voorwaarden van de overeenkomst, zoals betalingsvoorwaarden, leveringsvoorwaarden en het afleveradres, toegepast op de orderkoptekst en wordt de koppeling tussen de overeenkomst en de order gemaakt. Vervolgens worden op de orderregels, wanneer u producten en categorieën kunt selecteren die zijn opgegeven in de verkoopovereenkomst, de prijzen en kortingen van die overeenkomst gekopieerd. Dezelfde verkooporder kan zowel regels bevatten die niet zijn gerelateerd aan een verkoopovereenkomst als regels waarvoor een verkoopovereenkomst bestaat.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Verkooporders wijzigen die aan verkoopovereenkomsten zijn gekoppeld
Als u een verkooporder voor een verkoopovereenkomst hebt gemaakt (vrijgegeven), kunnen bepaalde velden op die verkooporderregels alleen worden gewijzigd als u de koppeling met de bijbehorende verkoopovereenkomstregels verwijdert. In de volgende tabel wordt een aantal van deze velden weergegeven.

| Veld                                                             | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gewenste verzenddatum                                               | Als u de gewenste verzenddatum wijzigt naar een datum die eerder is dan de waarde **Begindatum** op de verkoopovereenkomstregel, moet u de koppeling naar de verkoopovereenkomstregel verwijderen voordat u de gewijzigde verzenddatum kunt opslaan. Als u de gewenste verzenddatum wijzigt naar een datum die later is dan de waarde **Vervaldatum** op de verkoopovereenkomstregel, moet u de koppeling naar de verkoopovereenkomstregel verwijderen voordat u de gewijzigde verzenddatum kunt opslaan. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet amount | Als u de waarde in een van deze velden wijzigt en het selectievakje **Prijs en korting zijn vast** is ingeschakeld op een gekoppelde verkoopovereenkomstregel, verschijnt een bericht waarin u wordt gevraagd om de wijziging op te slaan. Klik op **Ja** om de koppeling met de verkoopovereenkomstregel te verwijderen en de prijs opnieuw te berekenen. Klik op **Nee** om de koppeling met de verkoopovereenkomstregel te verwijderen zonder de prijs opnieuw te berekenen.                                                                   |
| Nettobedrag                                                        | Als u een bedrag opgeeft dat hoger is dan de waarde die op een verkoopovereenkomstregel is opgegeven waar het selectievakje **Max is afgedwongen** is ingeschakeld, verschijnt een bericht waarin u wordt gevraagd om het gewijzigde bedrag op te slaan. Klik op **Ja** om de koppeling met de verkoopovereenkomstregel te verwijderen en de prijs opnieuw te berekenen. Klik op **Nee** om de koppeling met de verkoopovereenkomstregel te verwijderen zonder de prijs opnieuw te berekenen.                                                                 |
| Hoeveelheid                                                          | Als u een hoeveelheid opgeeft die hoger is dan de hoeveelheid die op een verkoopovereenkomstregel is opgegeven waar het selectievakje **Max is afgedwongen** is ingeschakeld, verschijnt een bericht waarin u wordt gevraagd om de gewijzigde hoeveelheid op te slaan. Klik op **Ja** om de koppeling met de verkoopovereenkomstregel te verwijderen en de prijs opnieuw te berekenen. Klik op **Nee** om de koppeling met de verkoopovereenkomstregel te verwijderen zonder de prijs opnieuw te berekenen.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Een item dat is besteld vanuit een verkoopovereenkomst retourneren
Wanneer een klant een product dat is besteld vanuit een verkoopovereenkomst, kan Microsoft Dynamics 365 for Operations kunt zoeken en automatisch bijwerken van de gerelateerde verkoopovereenkomst aan de wijziging in hoeveelheid of bedrag. Door een retourorder te maken die is gebaseerd op de oorspronkelijke verkooporder die is gekoppeld aan een verkoopovereenkomst, bepaalt u een relatie tussen de verkoopovereenkomsttoezegging, de verkooporderregel en de factuur voor de retourorder.  

Als u de hoeveelheid van het geretourneerde artikel niet wilt aftrekken van de verkoopovereenkomsttoezegging, kunt u de optie **Koppeling verwijderen** op de pagina **Retourorder** gebruiken om de koppeling te verwijderen tussen de retourorder en de verkoopovereenkomsttoezegging. Als u de koppeling later opnieuw moet maken, klikt u op **Koppeling maken**.  

**Opmerking:** Een retourorder kan worden gekoppeld aan slechts één verkoopovereenkomst. Als een klant verscheidene producten retourneert die zijn besteld met verscheidene verkoopovereenkomsten, moet u een nieuwe retourorder maken voor elk product en een koppeling maken naar de bijbehorende verkoopovereenkomst.

## <a name="automatic-search-for-sales-agreements"></a>Automatisch verkoopovereenkomsten zoeken
In sommige situaties waarin verkooporders indirect worden gemaakt, zoals wanneer u een creditnota of intercompany-verkooporders maakt, kunt u bepalen of Microsoft Dynamics 365 voor bewerkingen automatisch gezocht naar relevante verkoopovereenkomsten.

## <a name="financial-dimensions-on-sales-agreements"></a>Financiële dimensies op verkoopovereenkomsten
U kunt financiële dimensies kopiëren naar ofwel documentkopteksten of afzonderlijke regels van een verkoopovereenkomst. U kunt de dimensies op een overeenkomstkoptekst of overeenkomstregel op elk gewenst moment wijzigen. In dit geval worden de dimensies automatisch gekopieerd naar de vrijgavekoptekst of de vrijgaveregel van vrijgaveorders.


