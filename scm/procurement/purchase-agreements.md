---
title: Inkoopovereenkomsten
description: Dit artikel biedt informatie over inkoopovereenkomsten. Een inkoopovereenkomst is een contract dat een organisatie ertoe verbindt een opgegeven aantal of bedrag in te kopen via meerdere inkooporders in een bepaalde periode. De koper ontvangt in ruil voor deze toezegging speciale prijzen en kortingen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AgreementClassification, AgreementLine, AgreementLinePrompt, PurchAgreement, PurchAgreementCreate, PurchAgreementGenerateReleaseOrder, PurchAgreementHistory, PurchAgreementInvoiceJournal
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11634
ms.assetid: 8ac20adf-7412-4929-be8c-aaedf23a76ad
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3d02a15387231160f5b8a237aa11008b91ef1223
ms.openlocfilehash: 3f96d12960e90bb05497d1bc2900d4477551c091
ms.lasthandoff: 03/31/2017


---

# <a name="purchase-agreements"></a>Inkoopovereenkomsten

Dit artikel biedt informatie over inkoopovereenkomsten. Een inkoopovereenkomst is een contract dat een organisatie ertoe verbindt een opgegeven aantal of bedrag in te kopen via meerdere inkooporders in een bepaalde periode. De koper ontvangt in ruil voor deze toezegging speciale prijzen en kortingen. 

Inkoopovereenkomsten kunnen gelden voor een bepaalde hoeveelheid van een product, een bepaald bedrag van een product of een bepaald bedrag van de producten in een aanschaffingscategorie. De prijzen en kortingen van de inkoopovereenkomst vervangen de prijzen en kortingen die worden genoemd in eventuele bestaande handelsovereenkomsten.  

Op de pagina **Inkoopovereenkomsten** kunt u inkoopovereenkomsten maken, toepassen en opvolgen die tussen uw organisatie en de leveranciers bestaan. Zo kunt na de aanmaak van een inkoopovereenkomst direct vanuit de overeenkomst een order plaatsen. Elke inkoopovereenkomst heeft een geldigheidsduur die is gedefinieerd door de persoon die de inkoopovereenkomst maakt. De afleverdatum van een inkoop moet binnen de werkelijke data van deze geldigheidsperiode vallen.  

Nadat u een inkoopovereenkomst maakt, moet u deze activeren voordat het van kracht wordt. Om een inkoopovereenkomst te activeren, stelt u de optie **Overeenkomst als effectief markeren** in op **Ja**.

## <a name="commitment-types"></a>Toezeggingstypen
Elke regel in een inkoopovereenkomst staat voor een toezegging om iets te kopen. U kunt regels uit meerdere inkooporders gebruiken om te voldoen aan de verbintenis. Er zijn vier typen toezeggingen:

-   **Toezegging producthoeveelheid**: U koopt een specifieke hoeveelheid producten.
-   **Toezegging productwaarde**: U koopt voor een specifiek bedrag in een bepaalde valuta van een product.
-   **Waardetoezegging productcategorie**: U koopt voor een specifiek bedrag in een bepaalde inkoopcategorie. Het bedrag kan voor een catalogusartikel of een niet-catalogusartikel zijn.
-   **Waardetoezegging**: U koopt voor een bepaald bedrag van eender welk product/producten in een inkoopcategorie.

## <a name="pricing-terms-for-purchase-agreements"></a>Prijsvoorwaarden voor inkoopovereenkomsten
Prijsvoorwaarden kunnen variëren, afhankelijk van het type verbintenis. De prijsvoorwaarden van inkoopovereenkomsten vervangen eventuele andere prijsvoorwaarden die zijn ingesteld voor handelsovereenkomsten. De volgende tabel beschrijft de prijsgerelateerde velden die worden beïnvloed door elk toezeggingstype. Velden met **Ja** kunnen worden bijgewerkt op een orderregel.

| Toezeggingstype                   | Eenheidsprijs | Prijseenheid | Kortingspercentage | Contantkortingsbedrag |
|-----------------------------------|------------|------------|------------------|----------------------|
| Toezegging producthoeveelheid       | Ja        | Ja        | Ja              | Ja                  |
| Toezegging productwaarde          |            |            | Ja              |                      |
| Waardetoezegging productcategorie |            |            | Ja              |                      |
| Waardetoezegging                  |            |            | Ja              |                      |

## <a name="policies-for-purchase-agreements"></a>Beleid voor inkoopovereenkomsten
Het volgende beleid beïnvloedt de manier waarop de koppeling tussen een inkoopovereenkomst en de bijbehorende inkooporderregels werkt:

-   **Max is afgedwongen**: Het totale aantal of bedrag voor alle orderregels mag niet meer dan de hoeveelheid of het bedrag zijn dat is opgegeven op de gerelateerde toezegging.
-   **Prijs en korting zijn vast**: De prijs op een orderregel en de prijs op de bijbehorende toezegging moeten hetzelfde zijn. Als de prijs op de orderregel wordt gewijzigd, wordt de koppeling naar de toezegging verbroken. Als de koppeling wordt verbroken, draagt de orderregel niet bij aan het voldoen aan de toezegging.
-   **Minimale vrijgavebedrag en Maximale vrijgavebedrag**: Als een bedrag wordt opgegeven, krijgt u een melding als u een wijziging aanbrengt in een orderregel, waardoor de orderregel afwijkt van de gerelateerde toezegging.

## <a name="fulfillment-calculations-for-purchase-agreements"></a>Berekeningen voor het voldoen aan inkoopovereenkomsten
De uitvoeringshoeveelheden en bedragen worden getoond op het tabblad **Uitvoering** op het sneltabblad **Regeldetails** op de pagina **Inkoopovereenkomsten**.  

In het gebied **Vervulling** wordt het resterende bedrag of hoeveelheid weergegeven die nodig is om te voldoen aan de toezegging.  

Het gebied **Overeenkomst** geeft de totale hoeveelheid of het totale bedrag weer waarvoor de verkoopovereenkomstregel geldig is.  

U hebt toegang tot de inkooporderregels en de factuurregels die bijdragen aan de vervullingsberekening door de actie **Verwante informatie** te selecteren in de regels of in de koptekst van een inkoopovereenkomst.

## <a name="confirmations-and-version-history-for-purchase-agreements"></a>Bevestigingen en versiegeschiedenis voor inkoopovereenkomsten
Als u een inkoopovereenkomst bevestigt, wordt de huidige versie van de inkoopovereenkomst opgeslagen in een tabelgeschiedenis. Als u de inkoopovereenkomst wijzigt, kunt u deze opnieuw bevestigen om een andere versie van de inkoopovereenkomst in de geschiedenis op te slaan. Als u een inkoopovereenkomst niet bevestigt, kunt u het maken van POs. Echter, de historische gegevens voor de inkoopovereenkomst is niet opgeslagen. U kunt alle versies van de overeenkomst bekijken of afdrukken. Vervolgens kunt u de wijzigingen delen met uw leverancier voor goedkeuring.

## <a name="applying-purchase-agreements-in-the-ordering-process"></a>Inkoopovereenkomsten toepassen in het bestelproces
Wanneer u een inkooporder maakt, kunt u er een inkoopovereenkomst op toepassen. De informatie van de voorwaarden voor de overeenkomst, zoals de betalingsvoorwaarden, leveringsvoorwaarden en het afleveradres, wordt vervolgens gekopieerd naar de koptekst van de inkooporder. Als de inkooporder een of meer orderregels bevat voor producten of categorieën die de inkoopovereenkomst dekt, worden de prijzen en kortingen van de inkoopovereenkomst gebruikt voor deze regels. Het bedrag of het aantal op de orderregel draagt bij tot de uitvoering van de toezegging in de inkoopovereenkomst. Dezelfde inkooporder kan zowel regels bevatten die niet zijn gerelateerd aan een inkoopovereenkomst en regels waarvoor een inkoopovereenkomst bestaat.  

U kunt een inkoopovereenkomst alleen selecteren wanneer u een inkooporder maakt. U kunt geen inkoopovereenkomst selecteren nadat de inkooporder is gemaakt.  
In sommige situaties waarin verkooporders indirect worden gemaakt, is het mogelijk te bepalen of Microsoft Dynamics 365 for Operations automatisch moet zoeken naar relevante inkoopovereenkomsten. U kunt dit bijvoorbeeld doen wanneer u automatisch geplande inkooporders goedkeurt of inkooporders maakt die zijn gebaseerd op verkooporders.

## <a name="purchase-agreements-and-intercompany-trade"></a>Inkoopovereenkomsten en intercompany-handel
Intercompany-handelsrelaties kunnen worden gemaakt tussen leveranciersrekeningen en klantenrekeningen van verschillende rechtspersonen. Wanneer een verkooporder of inkooporder is gemaakt voor een van de partijen, wordt een intercompany-orderketen gemaakt. In de orderketen worden de verkooporder en inkooporder gemaakt in de juiste rechtspersonen.  

U kunt de inkoopovereenkomst of verkoopovereenkomst maken voor een van de intercompany-partijen. U kunt vervolgens de overeenkomstige verkoopovereenkomst of inkoopovereenkomst maken voor de andere intercompany-partij in de andere rechtspersoon.  

Als u in één rechtspersoon een intercompany-inkooporder maakt die de intercompany-inkoopovereenkomst gebruikt, gebruikt de betreffende intercompany-verkooporder de overeenkomstige intercompany-verkoopovereenkomst in de andere rechtspersoon. De afhandeling van de verkoopovereenkomst en de inkoopovereenkomsten worden gesynchroniseerd, net als de intercompany-verkooporder en intercompany-inkooporder worden gesynchroniseerd.

## <a name="financial-dimensions-on-purchase-agreements"></a>Financiële dimensies op inkoopovereenkomsten
U kunt financiële dimensies kopiëren naar documentkopteksten of naar afzonderlijke regels van een inkoopovereenkomst. Als u de dimensies in de overeenkomstkoptekst of de overeenkomstregel wijzigt, dan beïnvloedt de wijziging niet de vrijgegeven orders, maar werkt door in nieuwe orders die worden aangemaakt.

<a name="see-also"></a>Zie ook
--------

[Een inkoopovereenkomst (taak guide) maken](https://ax.help.dynamics.com/en/wiki/create-a-purchase-agreement/)

[Een vrijgaveorder voor inkoop maken vanuit een inkoopovereenkomst (taak guide)](https://ax.help.dynamics.com/en/wiki/create-a-purchase-release-order-from-a-purchase-agreement/)


