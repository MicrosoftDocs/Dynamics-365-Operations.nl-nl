---
title: Een klantfactuur maken
description: Een **klantfactuur voor een verkooporder** is een rekening die door een organisatie aan een klant wordt verstrekt in verband met een verkoop.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d278bda917d829caaedc7682ef9bebeb151d2bb9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991227"
---
# <a name="create-a-customer-invoice"></a>Een klantfactuur maken

[!include [banner](../includes/banner.md)]

Een **klantfactuur voor een verkooporder** is een rekening die door een organisatie aan een klant wordt verstrekt in verband met een verkoop. Een dergelijke klantfactuur maakt u op basis van een verkooporder die orderregels en artikelnummers bevat. Artikelnummers worden opgegeven en geboekt in het grootboek. Journaalposten in subadministratie zijn niet beschikbaar voor een klantfactuur voor een verkooporder. Zie [Facturen van verkooporder maken](tasks/create-sales-order-invoices.md) voor meer informatie.

Een **vrije-tekstfactuur** is niet gerelateerd aan een verkooporder. Deze factuur bevat orderregels met grootboekrekeningen, vrije-tekstomschrijvingen en verkoopbedragen die u invoert. U kunt geen artikelnummer invoeren op dit type factuur. U moet de betreffende btw-gegevens invullen. Op een vrije-tekstfactuur wordt een hoofdrekening voor de verkoop vermeld die u over meerdere grootboekrekeningen kunt verdelen door te klikken op **Bedragen verdelen** op de pagina **Vrije-tekstfactuur**. Tevens wordt het klantsaldo naar de totaalrekening van het boekingsprofiel geboekt dat gebruikt wordt voor de vrije-tekstfactuur.

Zie  voor meer informatie.

[Vrije-tekstfacturen maken](../accounts-receivable/create-free-text-invoice-new.md)

[Een sjabloon voor vrije-tekstfacturen maken](../accounts-receivable/create-free-text-invoice-template-new.md)

[Sjabloon voor vrije-tekstfacturen toewijzen aan een klant](tasks/assign-free-text-invoice-template-customer.md)

[Terugkerende vrije-tekstfacturen genereren en boeken](tasks/post-recurring-free-text-invoices.md)


Een **pro forma-factuur** is een factuur die wordt gemaakt als raming van de werkelijke factuurbedragen voordat de factuur wordt geboekt. Een pro forma-factuur kunt u zowel voor een klantfactuur als voor een verkooporder of een vrije-tekstfactuur afdrukken.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Individuele klantfacturen op basis van verkooporders boeken en afdrukken
Via deze procedure kunt u een factuur maken op basis van een verkooporder. U kunt dit bijvoorbeeld doen als u uw klant een factuur stuurt voordat u de goederen of services levert. 

Wanneer u een factuur boekt, wordt de hoeveelheid bij **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de gefactureerde hoeveelheden van de geselecteerde verkooporder. Als de hoeveelheid voor **Resterend gedeelte van factuur** en de hoeveelheid voor **Nog te leveren** voor alle artikelen op de verkooporder 0 (nul) zijn, wordt de status van de verkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid voor **Resterend gedeelte van factuur** niet gelijk is aan 0 (nul), blijft de status van de verkooporder ongewijzigd en kunnen hiervoor extra facturen worden ingevoerd.

Op de lijstpagina **Alle verkooporders** kunt u de status van de verkooporders bekijken. Gebruik de lijstpagina **Openstaande klantfacturen** om de facturen te bekijken die u hebt geboekt.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Individuele klantfacturen op basis van pakbonnen en de datum boeken en afdrukken
Gebruik deze procedure wanneer er minimaal één pakbon is geboekt voor de verkooporder. De klantfactuur is gebaseerd op deze pakbonnen en hieruit worden de hoeveelheden overgenomen. De financiële gegevens voor de factuur zijn gebaseerd op de gegevens die worden ingevoerd wanneer u de factuur boekt. 

U kunt een klantfactuur maken op basis van de artikelen op de pakbonregel die tot op heden zijn verzonden, ook als nog niet alle artikelen voor een bepaalde verkooporder zijn verzonden. U kunt dit bijvoorbeeld doen als uw rechtspersoon één factuur per klant per maand verzendt waarin alle leveringen in de desbetreffende maand zijn opgenomen. Met elke pakbon wordt een gedeeltelijke of gehele levering van de artikelen op de verkooporder aangeduid. 

Wanneer u de factuur maakt, wordt de hoeveelheid voor **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de geleverde hoeveelheden via de geselecteerde pakbonnen. Als de hoeveelheid voor **Resterend gedeelte van factuur** en de hoeveelheid voor **Nog te leveren** voor alle artikelen op de verkooporder 0 (nul) zijn, wordt de status van de verkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid voor **Resterend gedeelte van factuur** niet gelijk is aan 0 (nul), blijft de status van de verkooporder ongewijzigd en kunnen hiervoor extra facturen worden ingevoerd. 

Voorraadtransacties worden bijgewerkt met het factuurnummer en de status in het veld **Regelstatus** van de verkooporder wordt gewijzigd in **Gefactureerd**. 

Op de lijstpagina **Alle verkooporders** kunt u de status van de verkooporders bekijken.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Verkooporders of pakbonnen consolideren voor het boeken
Gebruik deze procedure als een of meer verkooporders kunnen worden gefactureerd en u deze in één factuur wilt consolideren. 

U kunt meerdere facturen op de lijstpagina **Verkooporder** selecteren en vervolgens **Facturen genereren** gebruiken om deze te consolideren. Op de pagina **Factuur wordt geboekt** kunt u de instelling voor **Overzichtsorder** wijzigen om een overzicht op basis van ordernummer (met meerdere pakbonnen voor één verkooporder) of factuurrekening (met meerdere verkooporders voor één factuurrekening) weer te geven. Gebruik de knop **Schikken** om verkooporders in afzonderlijke facturen te consolideren, op basis van de instellingen voor **Overzichtsorder**.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Aanvullende instellingen die het boekingsgedrag wijzigen
De volgende velden wijzigen het gedrag van het boekingsproces.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hoeveelheid</td>
<td>Selecteer de hoeveelheden waarop de boekingen van het document moeten worden gebaseerd. Welke opties worden weergegeven, is afhankelijk van het type document dat u boekt, bijvoorbeeld een pakbon of factuur.
<ul>
<li><strong>Nu leveren</strong>: selecteer alle hoeveelheden die in het veld <strong>Nu leveren</strong> worden ingevoerd. Gebruik deze optie om een gedeeltelijke order te bevestigen of te leveren.</li>
<li><strong>Verzameld</strong>: selecteer alle hoeveelheden die zijn verzameld.</li>
<li><strong>Alle</strong>: selecteer alle hoeveelheden op de verkooporder die nog niet zijn bijgewerkt door het huidige documenttype.</li>
<li><strong>Pakbon</strong>: selecteer alle hoeveelheden die zijn bijgewerkt door een pakbon.</li>
<li><strong>Gepickt aantal en producten niet in voorraad</strong>: selecteer alle hoeveelheden die zijn gepickt en alle producthoeveelheden die niet in voorraad zijn.</li>
</ul></td>
</tr>
<tr class="even">
<td>Boeking</td>
<td><ul>
<li>Selecteer deze optie om de verkooporder te journaliseren.</li>
<li>Schakel deze optie uit om een pro forma-verkooporder af te drukken. <strong>Opmerking</strong>: als u een overeenkomst voor een betalingsschema hebt gesloten, wordt het betalingsschema niet weergegeven op de pro forma-verkooporder. Betalingsschema´s worden alleen weergegeven op echte verkooporders.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Later selecteren</td>
<td>Selecteer deze optie om de geselecteerde query later toe te passen. Deze optie wordt gebruikt voor batchtaken. De query wordt uitgevoerd wanneer de batchtaak wordt uitgevoerd.</td>
</tr>
<tr class="even">
<td>Hoeveelheid verminderen</td>
<td>Selecteer deze optie om de geleverde hoeveelheid automatisch te reduceren wanneer het document wordt geboekt, zodat de geleverde hoeveelheid gelijk is aan de beschikbare voorraad.</td>
</tr>
<tr class="odd">
<td>Afdrukken</td>
<td>Selecteer wanneer u documenten wilt afdrukken:
<ul>
<li><strong>Huidig</strong>: druk documenten af nadat een factuur is bijgewerkt.</li>
<li><strong>Na</strong>: druk documenten af nadat alle facturen zijn bijgewerkt.</li>
</ul>
<strong>Opmerking:</strong> het veld <strong>Afdrukken</strong> is alleen beschikbaar als u de optie <strong>Factuur afdrukken</strong>, <strong>Bevestiging afdrukken</strong>, <strong>Orderverzamellijst afdrukken</strong> of <strong>Pakbon afdrukken</strong> hebt geselecteerd. U stelt bijvoorbeeld op de pagina <strong>Sortering van formulier</strong> in dat de informatie wordt gesorteerd op basis van de factuurrekening. Daarna kunt u <strong>Na</strong> selecteren om de documenten in een batch af te drukken die wordt gesorteerd op factuurrekening. Anders worden de documenten afgedrukt voordat de verwerking is voltooid en worden de documenten niet gesorteerd in de volgorde die op de pagina <strong>Sortering van formulier</strong> is opgegeven.</td>
</tr>
<tr class="even">
<td>Factuur afdrukken</td>
<td>U kunt dit optie selecteren als u de factuur wilt afdrukken. Als deze optie is uitgeschakeld, kunt u een factuur boeken zonder deze af te drukken.</td>
</tr>
<tr class="odd">
<td>E-mail verzenden</td>
<td>Selecteer deze optie om de factuur voor een verkooporder als e-mailbijlage te verzenden naar een klant nadat de factuur is geboekt. Bijlagen worden verzonden als PDF- en XML-bestanden. Deze optie is alleen beschikbaar als u de optie <strong>CFD inschakelen (elektronische facturen)</strong> op de pagina <strong>Parameters voor elektronische facturen </strong>selecteert. <strong>Opmerking:</strong> (MEX) Dit besturingselement is alleen beschikbaar voor rechtspersonen waarvan het primaire adres in Mexico is.</td>
</tr>
<tr class="even">
<td>Doel van afdrukbeheer gebruiken</td>
<td>Selecteer deze optie om de afdrukinstellingen te gebruiken die voor de transactie, het document of de module op de pagina <strong>Instelling afdrukbeheer</strong> zijn opgegeven.</td>
</tr>
<tr class="odd">
<td>Kredietlimiet controleren</td>
<td>Selecteer de informatie die moet worden geanalyseerd wanneer een kredietlimietcontrole wordt uitgevoerd.
<ul>
<li><strong>Geen</strong>: er is geen vereiste voor de controle van de kredietlimiet.</li>
<li><strong>Saldo</strong>: de kredietlimiet wordt gecontroleerd op basis van het saldo van de klant.</li>
<li><strong>Saldo+Pakbon of productontvangstbon</strong>: de kredietlimiet wordt vergeleken met het saldo van de klant en de leveringen.</li>
<li><strong>Saldo+Alle</strong>: de kredietlimiet wordt vergeleken met het saldo, de leveringen en de openstaande orders van de klant.</li>
</ul></td>
</tr>
<tr class="even">
<td>Creditcorrectie</td>
<td>Selecteer deze optie om de creditnota als debet weer te geven in de boekstuktransacties.</td>
</tr>
<tr class="odd">
<td>Krediet van resterende hoeveelheid</td>
<td>Selecteer deze optie als u een creditnota boekt en de resterende hoeveelheid op de order wilt behouden. Als deze optie is uitgeschakeld, wordt de resterende hoeveelheid op 0 (nul) ingesteld.</td>
</tr>
<tr class="even">
<td>Overzicht bijwerken voor</td>
<td>Selecteer de manier waarop meerdere verkooporders moeten worden samengevat:
<ul>
<li><strong>Geen</strong>: er worden geen verkooporders samengevat. U maakt bijvoorbeeld voor elke verkooporder een aparte factuur.</li>
<li><strong>Te factureren rekening</strong>: alle geselecteerde orders worden samengevat op basis van de criteria die zijn ingesteld op de pagina <strong>Overzicht van updateparameters</strong>.</li>
<li><strong>Order</strong>: een geselecteerd bereik aan orders wordt samengevat in een door u opgegeven order. De orders worden samengevat op basis van de criteria die zijn ingesteld op de pagina <strong>Overzicht van updateparameters</strong>. Als u deze optie selecteert, moet u een waarde in het veld <strong>Verkooporder</strong> selecteren.</li>
<li><strong>Automatisch overzicht</strong>: als er overzichtsupdates zijn opgegeven op de pagina <strong>Overzicht bijwerken</strong>, wordt een overzicht van alle geselecteerde orders weergegeven, op basis van de criteria die zijn ingesteld op de pagina <strong>Overzicht van updateparameters</strong>. Als er geen overzichtsupdates zijn opgegeven, wordt de order afzonderlijk geboekt.</li>
<li><strong>Pakbon</strong>: een geselecteerd bereik met orders wordt samengevat in één factuur per pakbon. Deze optie is alleen beschikbaar als de waarde <strong>Pakbon</strong> is geselecteerd in het veld <strong>Hoeveelheid</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>





