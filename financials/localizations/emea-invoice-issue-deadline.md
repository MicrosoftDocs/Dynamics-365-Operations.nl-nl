---
title: Deadline voor uitgeven van facturen
description: In dit artikel wordt uitgelegd hoe u parameters voor de berekening van de vervaldatums voor het uitgeven van klantfacturen en leveranciersfacturen in de Europese Unie (EU) instelt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10923
ms.assetid: 64ea3343-df94-4a52-b839-6328c8a282bd
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 6121be0dd02659e4e8466b0c1381678be64fefc2
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-issue-deadline"></a>Deadline voor uitgeven van facturen

In dit artikel wordt uitgelegd hoe u parameters voor de berekening van de vervaldatums voor het uitgeven van klantfacturen en leveranciersfacturen in de Europese Unie (EU) instelt.

Richtlijn 45/2010 van de Europese Unie (EU) en andere richtlijnen vereisen dat zendingen in de EU op of vóór de vijftiende dag van de maand moet worden gefactureerd nadat de levering is uitgevoerd. Tegelijkertijd kan elk EU-land verschillende deadlines voor facturering hebben binnenlandse leveringen. Met de vervaldatumfunctionaliteit voor het uitgeven van facturen kunt u het datuminterval afstemmen op het type land/regio. Vervolgens wordt voor alle zendingen naar en van een land/regio van een bepaald type de vervaldatum voor het uitgeven van facturen berekend aan de hand van regels die in het opgegeven datuminterval worden ingesteld. Bovendien kunt u alle pakbonnen die een specifieke vervaldatum voor het uitgeven van facturen hebben, filteren op de vervaldatum voor het uitgeven van facturen tijdens periodieke verkoopfacturering en de uitgiftedatum van verkoopfacturen tijdens het boeken van facturen bepalen. U kunt een datumintervalcode instellen en vervolgens een berekeningsregel voor de vervaldatum voor het uitgeven van facturen instellen door de datumintervalcode aan een type land/regio toe te wijzen. De berekeningsregel wordt gebruikt om de vervaldatum wilt berekenen voor het uitgeven van facturen voor de volgende transacties:

-   Zendingen in de EU
-   Binnenlandse zendingen in een EU-lidstaat

U kunt ook datumcontroles instellen om ervoor te zorgen dat klantfacturen en creditnota's voor klanttransacties in de opgegeven periode worden gegenereerd nadat de levering is uitgevoerd.

## <a name="prerequisites"></a>Vereisten
In de volgende tabel worden de vereisten weergegeven waaraan moet worden voldaan voordat u de vervaldatumfunctionaliteit voor het uitgeven van facturen kunt gebruiken.

| Categorie            | Vereiste                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/regio      | Het primaire adres van de rechtspersoon moet in een EG-lidstaat zijn.                                                                                                                                                                                                                                                                                                                    |
| Verwante taken instellen | Op de pagina **Datumintervallen** stelt u een datuminterval in dat wordt gebruikt om de vervaldatum voor het uitgeven van facturen te berekenen. (Klik op **grootboek**&gt;**instellingen van grootboek**&gt;**datum intervallen**.) Op de **parameters buitenlandse handel** pagina eigenschappen van de buitenlandse handel voor verschillende landen/regio's instellen. (Klik op **btw**&gt;**Setup**&gt;**buitenlandse handel**&gt;**parameters buitenlandse handel**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Regel voor vervaldatums voor het uitgeven van facturen
Gebruik de pagina **Berekening instellen voor vervaldatum factuuruitgifte** om een berekeningsregel voor de vervaldatum voor het uitgeven van facturen in te stellen door een datumintervalcode aan een type land/regio toe te wijzen.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Parameters voor datumcontrole voor klantfacturen en creditnota's
U kunt datumcontroleparameters instellen om ervoor te zorgen dat klantfacturen en creditnota's voor klanttransacties in de opgegeven periode worden gegenereerd nadat de levering is uitgevoerd. U kunt deze parameters vinden in het gebied **Controle van factuurdatums** van de pagina **Parameters van module Klanten**.

## <a name="example"></a>Voorbeeld
Instellen van Microsoft Dynamics 365 voor bewerkingen voor het berekenen van de factuur probleem vervaldagen voor intracommunautaire verzendingen op de vijftiende dag van de maand na de levering van de levering, een datum interval code en berekening regel maken met de volgende instellingen.

### <a name="date-interval-code"></a>Datumintervalcode

| Veld                                                           | Waarde                           |
|-----------------------------------------------------------------|---------------------------------|
| Datumintervalcode                                              | 15-NM                           |
| Beschrijving                                                     | Vijftiende dag van de volgende maand |
| Vóór (in de veldgroep **Einddatum**)                         | Maand                           |
| Begin/Einde (in de veldgroep **Einddatum**)                      | Beëindigen                             |
| +/- (in de veldgroep **Einddatum**)                            | 15                              |
| Dagen, maanden, jaren of perioden (in de veldgroep **Einddatum**) | Dagen                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Regel voor vervaldatums voor het uitgeven van facturen

| Veld               | Waarde                                                     |
|---------------------|-----------------------------------------------------------|
| Land-/regiotype | **EU**                                                    |
| Begindatum          | Voer de datum in waarop de huidige instellingsregel geldig is. |
| Datumintervalcode  | **15-NM**                                                 |

## <a name="next-steps"></a>Volgende stappen
Nadat u de instelling van de parameters hebt voltooid om de vervaldatums voor het uitgeven van facturen te berekenen, kunt u de volgende transacties maken en boeken om de vervaldatums voor het uitgeven van facturen automatisch te berekenen en bij te werken:

-   **Verkooporders** - Wanneer u een verkooporder maakt en een pakbon boekt, wordt de vervaldatum voor het uitgeven van de factuur en berekend op de pakbon bijgewerkt. De vervaldatum wordt berekend op basis van het datuminterval dat is gekoppeld aan de land/de regio die is opgegeven in het afleveradres van de verkooporder. Nadat u de pakbon boekt, kunt u controleren of het probleem factuur vervaldatum in de **probleem factureren vervaldatum** op de **pakbonjournaal** pagina. (Klik op **verkoop en marketing**&gt;**verkooporder**&gt;**bestellen verzending**&gt;**pakbon**.) U kunt alle pakbonnen die niet zijn gefactureerd en de afgifte van de factuur weergeven vervaldatums op de **niet zijn gefactureerd pakbonnen** pagina. (Klik op **verkoop en marketing**&gt;**verkooporder**&gt;**bestellen verzending**&gt;**pakbonnen die niet zijn gefactureerd**.)
-   **Inkooporders** - Wanneer u een inkooporder maakt en een productontvangstbon boekt, wordt de vervaldatum voor het uitgeven van de factuur en berekend op de productontvangstbon bijgewerkt. De vervaldatum wordt berekend op basis van het datuminterval dat aan het land of de regio is gekoppeld dat/die in het hoofdadres van de leverancier is opgegeven. Nadat u de productontvangstbon hebt geboekt, kunt u de vervaldatum voor de factuuruitgifte in het veld **Vervaldatum voor factuuruitgifte** op de pagina **Productontvangstbonjournaal** verifiëren. (Klik op **voor inkoop en sourcing**&gt;**inkooporders**&gt;**ontvangen van producten**&gt;**productontvangstbon**.) U kunt de productontvangstbonnen die niet zijn gefactureerd en de afgifte van de factuur weergeven vervaldatums op de **productontvangstbonnen die niet zijn gefactureerd** pagina. (Klik op **voor inkoop en sourcing**&gt;**inkooporders**&gt;**ontvangen van producten**&gt;**productontvangstbonnen die niet zijn gefactureerd**.)

## <a name="technical-information-for-system-administrators"></a>Technische informatie voor systeembeheerders
Als u geen toegang hebt tot de pagina's waarmee de in dit artikel vermelde taken worden voltooid, moet u contact opnemen met uw systeembeheerder en de informatie opgeven die in de volgende tabel wordt weergegeven.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categorie</th>
<th>Vereiste</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Configuration Keys</td>
<td>Klik op <strong>Systeembeheer</strong>&gt;<strong>Setup</strong>&gt;<strong>licenties</strong>&gt;<strong>licentieconfiguratie</strong>. Klik op de configuratiesleutel <strong>Grootboek</strong>.</td>
</tr>
<tr class="even">
<td>Veiligheidstaken en -rollen</td>
<td>Om deze taak uit te voeren, moet u lid zijn van een beveiligingsrol met de volgende functies:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Schakel factuur en contant geldproces in)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Schakel factuur en betalingsproces in)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Beveiligingsrollen en bevoegdheden</td>
<td>Om deze taak uit te voeren, moet u lid zijn van een beveiligingsrol met de volgende bevoegdheden:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Bekijk verkooppakbonnen)</li>
<li><strong>VendPackingSlipJournalView</strong> (Het jorunaal van de productontvangstbon bekijken vanuit inkooporder)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (Vervaldatums voor het uitgeven van facturen te berekenen)</li>
</ul></td>
</tr>
</tbody>
</table>




