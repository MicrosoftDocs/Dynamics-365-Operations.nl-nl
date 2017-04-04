---
title: Werkbeleid magazijn
description: "Een nieuw beleid voor magazijnwerk is geïntroduceerd in Microsoft Dynamics AX 7.0.1 (de update van mei 2016 ). Dit werkbeleid bepaalt of er magazijnwerk wordt gemaakt voor magazijnprocessen in productie."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 5660e5c8e3329564fc4262b5ad4f2547347bbb1a
ms.lasthandoff: 03/31/2017


---

# <a name="warehouse-work-policies"></a>Werkbeleid magazijn

Een nieuw beleid voor magazijnwerk is geïntroduceerd in Microsoft Dynamics AX 7.0.1 (de update van mei 2016 ). Dit werkbeleid bepaalt of er magazijnwerk wordt gemaakt voor magazijnprocessen in productie.

Dit werkbeleid bepaalt of er magazijnwerk wordt gemaakt voor magazijnprocessen in productie. U kunt het werkbeleid instellen door een combinatie van **werkordertypen**, een **voorraadlocatie** en een **product** te gebruiken. Bijvoorbeeld: L0101 is gereedgemeld product voltooid tot uitvoerlocatie 001. Het gerede product wordt later in een andere productieorder op uitvoerlocatie 001 verbruikt. U kunt in dit geval een werk-beleid instellen om te voorkomen dat het werk voor opslag eindproducten wordt gemaakt wanneer u L0101 tot uitvoerlocatie 001 gereed product. Het werkbeleid is een afzonderlijke entiteit die kan worden beschreven aan de hand van de volgende informatie:

-   **Werkbeleidsnaam **(de unieke id van het werkbeleid)
-   **Werkordertypen **en** Werkaanmaakmethode**
-   **Voorraadlocaties**
-   **Producten**

## <a name="work-order-types"></a>Werkordertypen
U kunt de volgende werkordertypen selecteren:

-   Eindproducten wegzetten
-   Coproducten en bijproducten wegzetten
-   Orderverzameling van grondstoffen

Het veld **Werkaanmaakmethode** heeft de waarde **Nooit**. Met deze waarde wordt aangegeven dat het werkbeleid voorkomt dat magazijnwerk wordt gemaakt voor het geselecteerde type werkorder.

## <a name="inventory-locations"></a>Voorraadlocaties
U kunt een locatie selecteren waarop het werkbeleid van toepassing is. Als er geen locatie aan een werkbeleid wordt gekoppeld, is het werkbeleid niet van toepassing op enige processen. Op de pagina **Locaties** kunt u ook werkbeleid voor een specifieke locatie selecteren of annuleren.

## <a name="products"></a>Producten
U kunt een product selecteren waarop het werkbeleid van toepassing is. U kunt het werkbeleid op alle producten of bepaalde producten toepassen.

## <a name="example"></a>Voorbeeld
In het volgende voorbeeld zijn er twee productieorders: PRD-001 en PRD-00*2*. Productieorder PRD-001 heeft een bewerking met de naam **Assembly**, waarbij product SC1 aan locatie O1 wordt gereedgemeld. Productieorder PRD-002 heeft een bewerking met de naam **Verven** en verbruikt product SC1 van locatie O1. Productieorder PRD-002 verbruikt ook grondstof RM1 van locatie O1. RM1 is opgeslagen in magazijnlocatie BULK-001 en wordt verzameld op locatie O1 door magazijnwerk voor het verzamelen van grondstoffen. De orderverzameling wordt gegenereerd wanneer productie PRD-002 wordt vrijgegeven. 

[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Wanneer u een werkbeleid voor magazijnen voor dit scenario configureert, moet u rekening houden met het volgende:

-   Magazijnwerk voor weggezette afgewerkte goederen is niet vereist wanneer u product SC1 van productieorder PRD-001 gereedmeldt voor locatie O1. De bewerking **Verven** voor productieorder PRD-002 verbruikt namelijk SC1 op dezelfde locatie.
-   Magazijnwerk voor het verzamelen van grondstoffen is vereist om grondstof RM1 van de magazijnlocatie BULK-001 naar locatie O1 te verplaatsen.

Hier is een voorbeeld van het werkbeleid dat u kunt instellen, op basis van deze overwegingen.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Work policy name**<br>                 |**Work order types**<br>                               |
| Geen opslaglocaties 01'                    |-Gereed product opslaan<br>                           |
|                                         |**Locations**<br>                                      |
|                                         |-O1   |                                               |
|                                         |**Products** <br>                                      |
|                                         |-SC1                                                  |

In de volgende procedures vindt u stapsgewijze instructies voor het instellen van het beleid voor magazijnwerk voor dit scenario. Daarnaast wordt een voorbeeld gegeven van een configuratie om te laten zien hoe u een productieorder gereedmeldt voor een locatie die niet wordt gecontroleerd op nummerplaat.

## <a name="set-up-a-warehouse-work-policy"></a>Een magazijnwerkbeleid instellen
In magazijnprocessen wordt niet altijd magazijnwerk opgenomen. Door een werkbeleid te definiëren kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties. Voor deze procedure is gebruikgemaakt van het demobedrijf USMF. 

STAPPEN (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Ga naar Magazijnbeheer &gt; Instellen &gt; Werk &gt; Werkbeleid.        |
| 2.  | Klik op Nieuw.                                                                 |
| 3.  | Typ in het veld Werkbeleidsnaam 'Geen weggezet werk'.                    |
| 4.  | Klik op Opslaan.                                                                |
| 5.  | Klik op Toevoegen.                                                                 |
| 6.  | Markeer in de lijst de geselecteerde rij.                                        |
| 7.  | Selecteer in het veld Werkordertype 'Eindproducten wegzetten'.            |
| 8.  | Klik op Toevoegen.                                                                 |
| 9.  | Markeer in de lijst de geselecteerde rij.                                        |
| 10. | Selecteer in het veld Werkordertype 'Coproducten en bijproducten wegzetten'. |
| 11. | Vouw de sectie Voorraadlocaties uit.                                    |
| 12. | Klik op Toevoegen.                                                                 |
| 13. | Markeer in de lijst de geselecteerde rij.                                        |
| 14. | Voer in de magazijnlijst '51' in.                                         |
| 15. | Typ of selecteer '001' in het veld Locatie.                              |
| 16. | Vouw de sectie Producten uit.                                               |
| 17. | Selecteer 'Geselecteerd' in het veld Productselectie.                         |
| 18. | Klik op Toevoegen.                                                                 |
| 19. | Markeer in de lijst de geselecteerde rij.                                        |
| 20. | Typ of selecteer 'L0101' in het veld Artikelnummer.                         |
| 21. | Klik op Opslaan.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Een productieorder gereedmelden voor een locatie die niet wordt gecontroleerd op nummerplaat
Deze procedure toont een voorbeeld van gereedmelding bij een locatie waar geen nummerplaten worden gecontroleerd. Een toepasselijk werkbeleid is de vereiste voor deze taak. In de vorige procedure werd beschreven hoe het werkbeleid wordt ingesteld. 

STAPPEN (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Deeltaak: Een uitvoerlocatie instellen.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Ga naar Organisatiebeheer &gt; Resources &gt; Resourcegroepen.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Selecteer resourcegroep '5102' in de lijst.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klik op Bewerken.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Voer '51' in het veld Uitvoermagazijn in.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Voer '001' in het veld Uitvoerlocatie in.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Locatie 001 is geen locatie waar nummerplaten worden gecontroleerd. U kunt een uitvoerlocatie waar geen nummerplaten worden gecontroleerd alleen instellen als er een toepasselijk werkbeleid voor de locatie bestaat.</td>
</tr>
<tr>
<td colspan="3"><strong>Deeltaak: Een productieorder maken en gereedmelden.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Sluit de pagina.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Ga naar Productiebeheer &gt; Productieorders &gt; Alle productieorders.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Klik op Nieuwe productieorder.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Voer 'L0101' in het veld Artikelnummer in.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Klik op Maken.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Klik in het actievenster op Productieorder.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Klik op Raming.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Klik op OK.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Klik op Start.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Klik op het tabblad Algemeen.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Selecteer 'Nooit' in het veld Automatisch stuklijstverbruik.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Klik op OK.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Klik op Gereedmelden.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Klik op het tabblad Algemeen.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Selecteer Ja in het veld Fout accepteren.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Klik op OK.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Klik in het actievenster op Magazijn.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Klik op Werkdetails.</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Toen de productieorder gereedgemeld werd, is er geen werk gegenereerd voor wegzetten. Dit komt doordat er een werkbeleid is gedefinieerd waarmee wordt voorkomen dat werk wordt gegenereerd wanneer product L0101 wordt gereedgemeld bij locatie 001.</td>
</tr>
</tbody>
</table>


