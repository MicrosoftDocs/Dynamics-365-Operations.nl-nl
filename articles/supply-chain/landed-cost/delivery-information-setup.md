---
title: Instelling van leveringsgegevens
description: In dit onderwerp wordt beschreven hoe u leveringsgegevens kunt instellen voor de module Francoprijzen.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7b65e1c6bb1b6bf345fdde0f4de7015190052efa
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500521"
---
# <a name="delivery-information-setup"></a>Instelling van leveringsgegevens

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u leveringsgegevens kunt instellen voor de module **Francoprijzen**.

## <a name="shipping-ports"></a>Verzendhavens

Expeditiehavens geven aan waar goederen van en naar worden verzonden. Voor elke reis wordt een aankomst- en een vertrekhaven gedefinieerd, gebaseerd op het traject dat voor het vaartuig voor de reis is geselecteerd. Expeditiehavens worden gebruikt om de etappes van een traject en ook de activiteiten van de reis op te bouwen. Deze worden meestal gedefinieerd met de naam van de plaats en het land of de regio waar de fysieke haven zich bevindt.

Als u wilt werken met expeditiehavens, gaat u naar **Francoprijzen \> Leveringsgegevens \> Expeditiehavens**. Hier kunt u records voor uw expeditiehavens weergeven, toevoegen en verwijderen. In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke record.

| Veld | Beschrijving |
|---|---|
| Verzendhaven | Voer een unieke identificatienaam/-nummer voor de expeditiehaven in. |
| Beschrijving | Over een omschrijving van de expeditiehaven in. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Controlecentrum voor tracering

Via het traceringscontrolecentrum kunt u de levertijden, statusupdates en informatiestroom instellen die aan een traject worden gekoppeld terwijl de verzendcontainers van de ene etappe naar de volgende gaan. Wanneer u een traceringscontrolerecord maakt, wordt deze gekoppeld aan een specifieke etappe van een traject voor een reis. Wanneer een traject een etappe bijwerkt, wordt de gekoppelde record bijgewerkt en ingevuld volgens de definitie. U kunt traceringsgegevens voor afzonderlijke trajecten bijwerken op de pagina **Alle trajecten**.

Als u het controlecentrum voor tracering wilt openen, gaat u naar **Francoprijzen \> Leveringsgegevens instellen \> Controlecentrum voor tracering**.

Het traceringscontrolecentrum toont een van drie paginaweergaven, afhankelijk van de waarde die is geselecteerd in het veld **Type maken** in het lijstdeelvenster: *Leeg*, *Doorlooptijd* of *Status*. Elk maaktype werkt een andere set gegevens bij die is gekoppeld aan de voortgang van een traject vanaf het beginpunt naar de eindbestemming.

### <a name="common-rule-settings"></a>Instellingen voor algemene regels

De volgende tabel bevat de velden die beschikbaar zijn voor de drie maaktypen in het traceringscontrolecentrum.

| Veld | Beschrijving |
|---|---|
| Brontabel, bronveld | Deze velden identificeren een brontabel en -veld in de database. De regel laadt de waarde in het veld en gebruikt deze vervolgens op de manier die door andere instellingen van de regel is gedefinieerd. |
| Doeltabel, doelveld | Deze velden identificeren een doeltabel en -veld in de database. De regel laadt de waarde in het veld en gebruikt deze vervolgens (of overschrijft deze) op de manier die door andere instellingen van de regel is gedefinieerd. |
| Activiteit | In dit veld wordt het type activiteit aangegeven dat moet worden toegepast op een verzendingscontainer die wordt gematcht door een regel. |
| Afstemmingscriteria | Dit veld bepaalt hoe het systeem een overeenkomst voor een regel identificeert. In elk geval controleert het systeem de gegevens in de bron- en doeltabellen om te bepalen of en wanneer een veld in de doeltabel moet worden bijgewerkt.<p>De brontabel is bijvoorbeeld *Trajecten* en de doeltabel is *Inkoopkoptekst* of *Inkoopregels*. De tabel *Trajecten* heeft als waarde voor **Vertrekhaven** *Hongkong* en de tabel *Inkoopkoptekst* heeft als de waarde voor **Vertrekhaven** *Hongkong*. Er wordt vervolgens een regel gemaakt met *Hongkong* als vertrekhaven. In dit geval werken de waarden van het veld **Criteria voor overeenkomst** als volgt:</p><ul><li>**Beide**: het doelveld wordt niet bijgewerkt, omdat een van de twee havens niet overeenkomt.</li><li>**Bron**: het doelveld wordt bijgewerkt, omdat de vertrekhaven uit de brontabel *Hongkong* is.</li><li>**Doel**: het doelveld wordt niet bijgewerkt, omdat de vertrekhaven van de doeltabel *Shanghai* is (niet *Hongkong*).</li></ul> |
| Actie kopiëren | De beschikbare waarden zijn *Kopiëren* en *Standaard*. Selecteer *Kopiëren* om de waarde in het bronveld naar het doelveld te kopiëren. Selecteer *Standaard* om een statische waarde voor het doelveld in te stellen. |
| Standaard | Wanneer het veld **Actie kopiëren** is ingesteld op *Standaard*, definieert het veld **Standaard** de standaardwaarde van het doelveld. Als de actie bijvoorbeeld is gerelateerd aan een havenupdate en het veld **Actie kopiëren** is ingesteld op *Standaard*, dan identificeert het veld **Standaard** een haven. |
| Etappe | Dit veld duidt de etappe aan van de reis waarvoor de opgegeven actie plaatsvindt, zoals laden of douane. |
| Serviceprovider | Als er een specifieke serviceprovider wordt gebruikt voor de huidige statusupdate/etappe van de reis, wordt de serviceprovider geïdentificeerd in dit veld. Serviceproviders worden gedefinieerd in de leveranciersrekening. |

### <a name="lead-time-rules"></a>Regels voor doorlooptijd

De doorlooptijd is de geschatte tijd die een gebruiker nodig heeft om een gedefinieerde etappe van een traject voor een reis te voltooien. De doorlooptijd van elke etappe van een reis wordt gebruikt om de geschatte leveringsdatum van de reis te berekenen. Die datum wordt vervolgens ingevoerd in het veld **Bevestigde leveringsdatum** op elke inkoopregel in de reis.

U gebruikt doorlooptijdregels om updates van datums te beheren. Activiteiten worden automatisch gegenereerd wanneer een trajectsjabloon voor een reis wordt gebruikt.

Volg deze stappen om een doorlooptijdregel toe te voegen aan het traceringscontrolecentrum.

1. Volg één van deze stappen:

    - Ga naar **Francoprijzen \> Een traject met meerdere etappes instellen \> Etappes**. Selecteer de etappe die u wilt instellen voor de doorlooptijden en selecteer vervolgens **Controlecentrum voor tracering** in het actiedeelvenster. Het traceringscontrolecentrum wordt vooraf geladen met informatie over de geselecteerde etappe.
    - Ga naar **Francoprijzen \> Leveringsgegevens instellen \> Controlecentrum voor tracering**. U moet vervolgens handmatig een etappe selecteren bij stap 4 van deze procedure.

1. Stel in het lijstdeelvenster het veld **Type maken** in op *Doorlooptijd*.
1. Selecteer **Nieuw** in het actievenster.
1. Als u in stap 1 vanuit het traceringscontrolecentrum bent begonnen, stelt u het veld **Etappe** in op de etappe waarvoor u een doorlooptijdregel wilt maken. Als u bent begonnen vanaf de pagina **Etappes**, wordt het veld **Etappe** vooraf ingesteld op het been dat u hebt geselecteerd voordat u het traceringscontrolecentrum hebt geopend.

    Op basis van de waarde van het veld **Etappe** worden automatisch verschillende velden ingesteld, zoals hier wordt weergegeven:

    - **Brontabel:** *Containeractiviteiten*
    - **Bronveld:** *Begindatum*
    - **Doeltabel:** *Containeractiviteiten*
    - **Doelveld:** *Geschatte einddatum*

1. Selecteer in het veld **Activiteit** de activiteit waarop de huidige regel moet worden toegepast.
1. Geef in het veld **Doorlooptijd** de doorlooptijd (in dagen) op die moet worden toegepast wanneer de huidige regel wordt geactiveerd.

### <a name="status-update-rules"></a>Regels voor statusupdates

Records waarbij het veld **Type maken** is ingesteld op *Status bijwerken*, worden bijgewerkt op de status van inkooporderregels of de status op het niveau reis, verzendcontainer of folio. De statussen kunnen onafhankelijk worden ingesteld. Gebruik deze om de gebruiker of afdeling te informeren over de fase van een reis (zoals ontvangen documenten of goederen in transit).

Wanneer het veld **Type maken** is ingesteld op *Status bijwerken*, bevat het traceringscontrolecentrum een sneltabblad **Regels** waar u een kostengebied en de bijgewerkte status van de reis kunt definiëren. Stel, u hebt een regel waarop het veld **Kostengebied** is ingesteld op *Container* en het veld **Reisstatus** is ingesteld op *Goederen in transit*. Wanneer een order in dat geval de opgegeven etappe voltooit, wordt het veld **Reisstatus** van de verzendcontainer bijgewerkt naar *Goederen in transit*.

Statusupdates voorzien in de reisstatus op alle reisregels en inkooporderregels die aan die reis zijn gekoppeld. Terwijl een reis het traject aflegt van de haven, de afvaart en de douane, tot het magazijn van bestemming, geeft het veld **Reisstatus** van de reisrecord een beknopt overzicht van de fase waarin de artikelen zich bevinden.

Volg deze stappen om een statusupdateregel toe te voegen aan het traceringscontrolecentrum.

1. Volg één van deze stappen:

    - Ga naar **Francoprijzen \> Een traject met meerdere etappes instellen \> Etappes**. Selecteer de etappe waarvoor u een statusupdate wilt instellen en selecteer vervolgens **Controlecentrum voor tracering** in het actiedeelvenster. Het traceringscontrolecentrum wordt vooraf geladen met informatie over de geselecteerde etappe.
    - Ga naar **Francoprijzen \> Leveringsgegevens instellen \> Controlecentrum voor tracering**. U moet vervolgens handmatig een etappe selecteren bij stap 4 van deze procedure.

1. Stel in het lijstdeelvenster het veld **Type maken** in op *Statusupdate*.
1. Selecteer **Nieuw** in het actievenster.
1. Als u in stap 1 vanuit het traceringscontrolecentrum bent begonnen, stelt u het veld **Etappe** in op de etappe waarvoor u een statusupdateregel wilt maken. Als u bent begonnen vanaf de pagina **Etappes**, wordt het veld **Etappe** vooraf ingesteld op het been dat u hebt geselecteerd voordat u het traceringscontrolecentrum hebt geopend.

    Op basis van de waarde van het veld **Etappe** worden automatisch verschillende velden ingesteld, zoals hier wordt weergegeven:

    - **Brontabel:** *Containeractiviteiten*
    - **Bronveld:** *Werkelijke einddatum*
    - **Doeltabel:** dit veld is leeg.
    - **Doelveld:** dit veld is leeg.

1. Selecteer in het veld **Activiteit** de activiteit waarop uw regel moet worden toegepast.
1. Voer op het sneltabblad **Regels** de statusupdates voor elk kostengebied in.

### <a name="blank-type-rules"></a>Lege typeregels

Records die voor **Type maken** de waarde *Leeg* hebben, gebruikt u om een veldwaarde te overschrijven of in te voeren, afhankelijk van de gegevens in een ander veld. Een veld uit Francoprijzen overschrijft gegevens in andere gebieden van Microsoft Dynamics 365 Supply Chain Management, gebaseerd op regels die in het controlecentrum voor tracering zijn ingesteld.

1. Ga naar **Francoprijzen \> Leveringsgegevens instellen \> Controlecentrum voor tracering**.
1. Stel in het lijstdeelvenster het veld **Type maken** in op *Leeg*.
1. Selecteer **Nieuw** in het actievenster.
1. Definieer de bron- en doelwaarden, overeenkomstcriteria, kopieeractie en andere relevante parameters, zoals vereist is voor de regel.

### <a name="required-tracking-control-setup"></a>Vereiste instellingen voor traceringscontrole

Voor elke sjabloon moeten er twee records worden ingesteld in het traceringscontrolecentrum. Beide records hebben de waarde **Leeg** bij *Type maken* en worden gebruikt in alle Francoprijzen-implementaties. Ze helpen ervoor te zorgen dat de bevestigde inkoopdatum en de verwachte datums van goederen in transit op de verwachte manier worden bijgewerkt voor reizen en op gerelateerde inkooporderregels.

De eerste record is vereist voor het bijwerken van inkoopregels. Hiervoor moeten de volgende instellingen gelden:

- **Brontabel:** *Containeractiviteiten*
- **Bronveld:** *Geschatte einddatum*
- **Doeltabel:** *Inkoopregels*
- **Doelveld:** *Bevestigde leveringsdatum of leveringsdatum*

De tweede record is vereist voor het bijwerken van transacties voor goederen in transit. Hiervoor moeten de volgende instellingen gelden:

- **Brontabel:** *Containeractiviteiten*
- **Bronveld:** *Geschatte einddatum*
- **Doeltabel:** *Order goederen in transit*
- **Doelveld:** *Verwachte datum*
