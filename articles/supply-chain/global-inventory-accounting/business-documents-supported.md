---
title: Bedrijfsdocumenten die worden ondersteund door Algemene voorraadboekhouding
description: Dit onderwerp geeft een overzicht van de bedrijfsdocumenten die worden ondersteund door Algemene voorraadboekhouding. Het bevat ook een gedetailleerd voorbeeld van inkooporderdocumenten.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 311c894d709985d0d053b0ec3a317142aa582c39
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273139"
---
# <a name="business-documents-supported-by-global-inventory-accounting"></a>Bedrijfsdocumenten die worden ondersteund door Algemene voorraadboekhouding

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Nadat de invoegtoepassing Algemene voorraadboekhouding volledig is ingesteld, kunnen voorraadgerelateerde documenten worden verwerkt die zijn ingevoerd in Microsoft Dynamics 365 Supply Chain Management.

## <a name="supported-business-documents"></a>Ondersteunde bedrijfsdocumenten

Er zijn twee typen bedrijfsdocumenten:

- **Documenten met een journaal**: deze documenten omvatten productontvangstbon-, inkoopfactuur-, pakbon- en verkoopfactuurdocumenten.
- **Documenten die geen journaal hebben**: deze documenten omvatten tellings-, verplaatsings- en voorraadcorrectiedocumenten.

Verder in dit onderwerp worden inkooporders gebruikt als voorbeeld om het proces te illustreren.

In de volgende tabel worden de documenten vermeld die door de huidige versie worden ondersteund.

| Documenttype      | Document        |
|--------------------|-----------------|
| Inkooporder     | Productontvangst |
| Inkooporder     | Factuur         |
| Verkooporder        | Pakbon    |
| Verkooporder        | Factuur         |
| Voorraadjournalen | Mutatie        |
| Voorraadjournalen | Correctie      |
| Voorraadjournalen | Tellen        |
| Voorraadjournalen | Overboeking        |
| Transferorder     | Zending        |
| Transferorder     | Ontvangen         |

> [!IMPORTANT]
> In Algemene voorraadboekhouding worden de documenten die in Supply Chain Management zijn ingevoerd asynchroon verwerkt. Voor problematische documenten worden geen foutberichten weergegeven.

## <a name="example-purchase-order"></a>Voorbeeld: inkooporder

### <a name="product-receipt"></a>Ontvangst van producten

Boek productontvangstbonnen op de gebruikelijke manier. Selecteer op de pagina **Alle inkooporders** een inkooporder en selecteer vervolgens in het actievenster op het tabblad **Ontvangen** de optie **Productontvangstbon** om de pagina **Productontvangstbonjournaal** te openen. Voor elke regel worden een bewerkingsgebeurtenis en een Algemene voorraadboekhouding-gebeurtenis gegenereerd. Daarom selecteert u het tabblad **Regels** en selecteert u **Voorraad \> Gebeurtenissen en -metingen** om de pagina **Gebeurtenissen en metingen** te openen.

Algemene voorraadboekhouding is een boekhoudsysteem dat is gebaseerd op gebeurtenissen en metingen. Het metingregelraster op de pagina **Gebeurtenissen en metingen** geeft een lijst met metingen weer. Elke meting heeft een lijst met dimensies.

Voor elke bewerkingsgebeurtenis zijn er twee typen metingen:

- **Bewerkingsmetingen**: deze metingen beschrijven bedrijfsdocumenten in algemene termen. Eén meting is de producthoeveelheid die gebruik maakt van de maateenheid die in het document wordt gebruikt. Er zijn ook metingen die van invloed zijn op de voorraadwaarde, zoals totaalprijs, korting, kortingspercentage en regeltoeslag.
- **Metingen van bedrijfsmiddelenboekhouding**: deze metingen zijn afkomstig van het voorraadregisterperspectief. Ze beschrijven de impact van het document op de voorraad in de voorraadmaateenheid. Als er meerdere voorraadregistraties zijn, zijn er meerdere regels voor metingen van de bedrijfsmiddelenboekhouding.

De dimensies worden als volgt ingedeeld:

- **Dualiteit**: dualiteit beschrijft de actoren die aan de economische gebeurtenissen deelnemen. Voor externe bedrijfsdocumenten beschrijven de primaire dimensies de rechtspersoon waar het document wordt ingevoerd, terwijl de dubbele dimensies de leverancier, klant en dergelijke omschrijven. Voor interne bedrijfsdocumenten (bijvoorbeeld transferorders) beschrijven de dubbele dimensies het equivalente magazijn.
- **Dimensietype**: dimensietypen categoriseren de dimensies.
- **Dimensie**: de naam van de dimensie.
- **Dimensiewaarde**: de waarde van de dimensie.

### <a name="global-inventory-accounting-event"></a>Algemene voorraadboekhouding-gebeurtenis

In Algemene-voorraadboekhouding worden de operationele gebeurtenissen en metingen als invoer gebruikt. Vervolgens wordt op basis van de gekoppelde valuta en conventie de juiste boekhouding voor elk gerelateerd grootboek gebruikt. U kunt **Gebeurtenissen en metingen voor Algemene voorraadboekhouding** selecteren om de gebeurtenis voor Algemene voorraadboekhouding weer te geven. De Algemene voorraadboekhouding-gebeurtenis heeft dezelfde methodologie als bewerkingsgebeurtenissen, maar gebruikt verschillende metingen. Er zijn drie belangrijke metingstypen: de hoeveelheid van de productkosten, de productkosten en de afwijking.

Grootboekrekeningen worden gebruikt om de metingen verder te classificeren. Er kunnen meerdere grootboeken zijn. Deze grootboeken zijn gekoppeld aan de rechtspersoon waar het document is ingevoerd. U kunt de gebeurtenissen en metingen voor elk grootboek weergeven door de waarde van het veld **Grootboek** te wijzigen.

### <a name="cost-element"></a>Kostenelement

Op basis van het kostenelementbeleid dat aan het grootboek is gekoppeld, wordt een kostenelement toegewezen aan elke gemaakte bewerkingsgebeurtenismeting die gevolgen heeft voor de voorraadkosten. Deze metingen omvatten totaalprijs, korting, kortingspercentage en regeltoeslag.

### <a name="measurement-line-details"></a>Details van metingregel

Op het tabblad **Overzicht** ziet u de details van het gekoppelde beleid. Het kostenobject wordt in de kostenobjectdimensies op basis van het kostenobjectbeleid getoond. Specifieke identificatiedimensies tonen het batchnummer als de kostenstroomveronderstelling *Specifiek - Batch* is.

### <a name="purchase-invoice"></a>Inkoopfactuur

Boek de factuur op de gebruikelijke manier. Selecteer vervolgens in het actievenster op het tabblad **Factuur** in de groep **Journalen** de optie **Factuur** om het factuurjournaal te openen. Voor elke regel worden een bewerkingsgebeurtenis en een Algemene voorraadboekhouding-gebeurtenis gegenereerd. Daarom selecteert u het tabblad **Regels** en selecteert u **Voorraad \> Gebeurtenissen en -metingen** om de pagina **Gebeurtenissen en metingen** te openen. Op de pagina **Gebeurtenissen en metingen** wordt hetzelfde metingtype weergegeven. Omdat de pagina echter een andere metingrol en metingmodificator toont, is het effect op de actor (rechtspersoon) verschillend.

Selecteer **Gebeurtenissen en metingen voor Algemene voorraadboekhouding** om de Algemene voorraadboekhouding-gebeurtenis weer te geven. De voorraadhoeveelheid en -kosten stromen nu uit van de subgrootboekrekening *Ontvangen niet-gefactureerde voorraad* en naar de subgrootboekrekening *Kosten van ingekochte goederen*.
