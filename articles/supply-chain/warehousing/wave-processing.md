---
title: Waves maken en verwerken
description: In dit artikel wordt beschreven hoe u handmatig een wave kunt maken, verwerken en vrijgeven om verzamelwerk te maken voor een lading, zending, productieorder of kanbanorder.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0466019990773ee93e063a255c15a7d64eecdf78
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336000"
---
# <a name="wave-creation-and-processing"></a>Waves maken en verwerken

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u handmatig een wave kunt maken, verwerken en vrijgeven om verzamelwerk te maken voor een lading, zending, productieorder of kanbanorder. U kunt waves maken voor de volgende typen orders:

- **Verkooporders**: gebruik zendingwaves om regels van verkooporders op te nemen. Wanneer een verkooporder aan het magazijn wordt vrijgegeven, kunnen de verkooporderregels in de wave worden opgenomen.
- **Productieorders**: gebruik productiewaves om regels van de stuklijst (BOM) voor een product op te nemen.
- **Kanbanorders**: kanbanwaves bevatten regels van orderverzamellijsten van kanbanorders.

Bij verkooporders en kanbanorders moet de voorraad zijn gereserveerd voordat de order aan het magazijn wordt vrijgegeven. Anders kunnen artikelen of toewijzingsregels niet in een wave worden verwerkt. Productieorders zijn echter iets flexibeler. Voor productieorders kunt u een van de volgende opties kiezen:

- Vereisen dat alle materialen moeten zijn gereserveerd voordat een order kan worden vrijgegeven aan het magazijn.
- Toestaan dat productieorders worden vrijgegeven aan het magazijn, ook al kunnen niet alle materialen worden gereserveerd. Als u deze optie selecteert, moet u de vrijgave naar het magazijnproces handmatig herhalen wanneer de aanvullende materialen beschikbaar worden. Dit is bijvoorbeeld handig als u de materialen hebt die u nodig hebt om een productie te starten en kunt wachten tot extra materialen beschikbaar zijn.

U kunt opgeven welke van deze opties voor productieorders standaard moet worden gebruikt met behulp van het veld **Vereiste voor materiaalreservering** op de pagina **Parameters van productiebeheer**. U kunt echter de instelling voor elke specifieke productieorder op elk gewenst moment wijzigen. Zie [Magazijnparameters voor waveverwerking](wave-warehouse-parameters.md) voor meer informatie.

## <a name="create-and-process-a-wave"></a>Een wave maken en verwerken

In het volgende diagram ziet u de stroom voor het maken, verwerken en vrijgeven van zendingwaves. De nummers stemmen overeen met de secties verderop in dit gedeelte.

![Proces voor het maken van een wave.](media/wave-processing-diagram.png "Proces voor het maken van een wave")

### <a name="prerequisites"></a>Vereisten

Voordat u begint, moet er een wavesjabloon beschikbaar zijn voor het type wave dat u wilt maken (zending, productie of kanban). De wavesjabloon stelt veel instellingen in voor hoe de wave wordt gegenereerd en verwerkt, inclusief welke stappen handmatig moeten worden uitgevoerd en welke automatisch plaatsvinden. Zie [Wavesjablonen](wave-templates.md) voor meer informatie.

### <a name="create-a-wave"></a>Een wave maken

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automatisch waves maken op basis van magazijn- en ordertype

Als u automatisch waves wilt maken, stelt u [Wavesjablonen](wave-templates.md) in die van toepassing zijn op elk relevant ordertype en magazijn. Zorg ervoor dat voor elke sjabloon de optie **Het maken van waves automatiseren** is ingesteld op *Ja*.

#### <a name="manually-create-waves"></a>Handmatig waves maken

Volg deze stappen om handmatig een wave te maken:

1. Zorg ervoor dat de relevante [wavesjablonen](wave-templates.md) niet zijn ingesteld om automatisch een wave te maken voor het magazijn en de ordertypen waarvoor u dit handmatig wilt doen.
1. Afhankelijk van het type wave dat u wilt maken, voert u een van de volgende acties uit:

    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Zendingwaves** \> **Alle waves**. Selecteer **Wave** in het actievenster.
    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Productiewaves** \> **Alle productiewaves**. Selecteer **Productiewave** in het actievenster.
    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Kanbanwaves** \> **Alle kanbanwaves**. Selecteer **Wave maken** in het actievenster.

1. Voer in het veld **Beschrijving** een korte beschrijving van de wave in. Dit moet aangeven wat u in de wave verwerkt.

1. Selecteer in het veld **Wavesjabloon** de wavesjabloon voor het type wave dat u wilt maken. De wavesjabloon bevat de wavemethoden die acties uitvoeren zoals het maken van werk voor de wave. De wavesjabloon voor zendingwaves kan bijvoorbeeld methoden bevatten voor het maken van ladingen, het toewijzen van waves, aanvullingen en het maken van verzamelwerk voor de wave.

1. Als u wavekenmerken wilt gebruiken als aanvullende querycriteria voor de wave, selecteert u de kenmerken in de velden **Wavekenmerken**.

### <a name="specify-what-to-include-in-a-wave"></a>Opgeven wat moet worden opgenomen in een wave

Nadat een wave is gemaakt, bent u klaar om er inhoud aan toe te voegen.

> [!NOTE]
> Indien nodig kunt u regels aan een wave toevoegen, zelfs nadat deze is verwerkt, zolang deze niet is vrijgegeven.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automatisch opgeven wat moet worden opgenomen in een wave

Als u automatisch waves wilt maken, stelt u [Wavesjablonen](wave-templates.md) in die van toepassing zijn op elk relevant ordertype en magazijn. Zorg ervoor dat voor elke sjabloon de optie **Het maken van waves automatiseren** is ingesteld op *Ja*. Als alternatief kan uw sjabloon automatisch regels toewijzen aan elke in aanmerking komende open wave als de optie **Toewijzen aan open waves** is ingesteld op *Ja*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Handmatig opgeven wat moet worden opgenomen in een wave

Wanneer een wave is gemaakt maar nog niet is vrijgegeven, kunt u handmatig opgeven wat u erin wilt opnemen. Regels handmatig toevoegen aan een wave:

1. Afhankelijk van het type wave waaraan u regels wilt toevoegen, voert u een van de volgende handelingen uit:

    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Zendingwaves** \> **Alle waves**. Selecteer **Wave** in het actievenster.
    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Productiewaves** \> **Alle productiewaves**. Selecteer **Productiewave** in het actievenster.
    - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Kanbanwaves** \> **Alle kanbanwaves**. Selecteer **Wave maken** in het actievenster.

1. Selecteer de wave. Selecteer een van de volgende opties in het actievenster:

      - **Zendingen onderhouden**
      - **Producties onderhouden**
      - **Orderverzamellijsten voor kanbantaak onderhouden**

1. In het bovenste gedeelte van het venster selecteert u de regel om aan de wave toe te voegen en selecteert u vervolgens **Toevoegen aan wave**. Het regel wordt verplaatst naar het sneltabblad **Waveregels**.

    Herhaal deze stap voor elke toe te voegen regel. Als u alle regels wilt toevoegen, selecteert u **Alles toevoegen**.

    > [!TIP]
    > Voor zendingwaves kunt u snel een specifieke order zoeken door een aangepast filter te selecteren in het veld **Code van wavefilter**. Wavefiltercodes bevatten zoekcriteria voor zendingen, die in het formulier **Wavefilters** worden gemaakt. Dit veld is niet beschikbaar voor productiewaves of kanbanwaves.
    > Een groen vinkje in de kolom **In wave** geeft aan dat de zending aan de wave is toegevoegd.

### <a name="process-the-wave-to-create-the-picking-work"></a>De wave verwerken om het verzamelwerk te maken

Nadat een wave is gemaakt en alle vereiste regels bevat, bent u klaar om deze te verwerken om het bijbehorende orderverzamelwerk te maken.

#### <a name="automatically-process-a-wave"></a>Automatisch een wave verwerken

Als u een wave automatisch wilt verwerken, stelt u de relevante [wavesjablonen](wave-templates.md) in met de vereiste automatische verwerkingsopties.

#### <a name="manually-process-a-wave"></a>Handmatig een wave verwerken

U kunt een wave alleen verwerken als **Wavestatus** de waarde *Gemaakt* heeft. Nadat u een wavehebt verwerkt, wordt de **wavestatus** gewijzigd in *Vastgehouden*.

Voer de volgende stappen uit om een wave met alle vereiste inhoud handmatig te verwerken:

1. Afhankelijk van het type golf dat u wilt verwerken, voert u een van de volgende handelingen uit:

    - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Zendingwaves** \> **Alle waves**. Selecteer **Wave** in het actievenster.
    - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Productiewaves** \> **Alle productiewaves**. Selecteer **Productiewave** in het actievenster.
    - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Kanbanwaves** \> **Alle kanbanwaves**. Selecteer **Wave maken** in het actievenster.

1. Selecteer de te verwerken wave. Selecteer **Verwerken** in het actievenster.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Geef de wave vrij aan het magazijn om het orderverzamelen en verpakken te starten

U moet een wave verwerken voordat u deze kunt vrijgeven. Wanneer u de wave vrijgeeft, is het orderverzamelwerk beschikbaar in het magazijn. U kunt een wave annuleren nadat deze is vrijgegeven en meer regels toevoegen, maar u kunt de regels niet wijzigen.

#### <a name="automatically-release-a-wave"></a>Automatisch een wave vrijgeven

Als u een wave automatisch wilt verwerken, stelt u de relevante [wavesjablonen](wave-templates.md) in met de vereiste automatische verwerkingsopties.

#### <a name="manually-release-a-wave"></a>Handmatig een wave vrijgeven

Volg deze stappen om handmatig een wave vrij te geven:

1. Afhankelijk van het type wave u wilt vrijgeven, voert u een van de volgende handelingen uit:

      - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Zendingwaves** \> **Alle waves**. Selecteer **Wave** in het actievenster.
      - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Productiewaves** \> **Alle productiewaves**. Selecteer **Productiewave** in het actievenster.
      - Selecteer **Magazijnbeheer** \> **Uitgaande waves** \> **Kanbanwaves** \> **Alle kanbanwaves**. Selecteer **Wave maken** in het actievenster.

1. Selecteer de vrij te geven wave. Selecteer **Wave vrijgeven** in het actievenster.

## <a name="containerize-a-wave"></a>Een wave in een container opnemen

Bij automatische containervorming worden containers gecreëerd en wordt de orderverzameling uitgevoerd voor zendingen wanneer een wave wordt verwerkt. Zie [Containervorming](wave-containerization.md) voor meer informatie over het instellen ervan.

## <a name="work-with-the-scheduled-work-creation"></a>Werken met de geplande werkcreatie

Wanneer de functie *Werk maken plannen* is ingeschakeld, wordt er door waveverwerking gepland werk gemaakt, dat uiteindelijk wordt gebruikt door het nieuwe werkaanmaakproces. Tijdens het maken van het werk wordt het werk geblokkeerd met de functie *Werk blokkeren voor de hele organisatie*. Zie [Het maken van werk tijdens wave plannen](configure-wave-schedule-work-creation.md) voor meer informatie.

In het volgende stroomdiagram is te zien hoe gepland werk tijdens de verwerking van waves wordt gemaakt.

![Werk maken plannen.](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Gepland werk

Op de pagina **Details gepland werk** (**Magazijnbeheer \> Werk \> Details gepland werk**) ziet u info over het geplande werk dat aanvankelijk is gemaakt tijdens waveverwerking. De volgende waarden **Processtatus** zijn beschikbaar:

- **In de wachtrij**: het geplande werk wacht om te worden gebruikt om werk te maken.
- **Voltooid** - Het geplande werk is gebruikt om werk te maken.
- **Mislukt:** de waveverwerking is mislukt. Houd er rekening mee dat het geplande werk een status **Mislukt** kan hebben met of zonder bijbehorend werkelijk werk. Wanneer het daadwerkelijke maken van het werk mislukt, blijft de status van het werkelijke werk *Geannuleerd*.

### <a name="batch-job-for-the-work-creation-process"></a>Batchtaak voor werk maken

Als u de batchtaken voor het verwerken van waves wilt weergeven, selecteert u **Batchtaken** in het actievenster op de pagina **Alle waves**.

In deze weergave kunt u alle details van de batchtaak voor elk van de batchtaak-ID´s weergeven.

## <a name="cancel-a-wave"></a>Een wave annuleren

Indien nodig, kunt u een wave annuleren die is verwerkt. Als u een wave en het gemaakte orderverzamelwerk wilt annuleren, volgt u deze stappen:

1. Afhankelijk van het type wave u wilt annuleren, voert u een van de volgende handelingen uit:

      - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Zendingwaves** \> **Alle waves**.
      - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Productiewaves** \> **Alle productiewaves**.
      - Ga naar **Magazijnbeheer** \> **Uitgaande waves** \> **Kanbanwaves** \> **Alle kanbanwaves**.

1. Selecteer de wave die u wilt annuleren. Selecteer in het actievenster op het tabblad **Werk** de optie **Annuleren**.

## <a name="review-wave-batch-job-details"></a>Details van batchtaak voor wave bekijken

Gebruik de pagina **Details van batchtaak voor wave** om de batchtaken en gerelateerde taken te inspecteren die aan een wave zijn gekoppeld. Dit is vooral handig voor het oplossen van problemen met een wave die is mislukt. Zonder deze functie hebben alleen beheerders doorgaans toegang tot batchverwerkingsdetails. De pagina **Details van batchtaken voor wave** kan beschikbaar worden gesteld aan niet-beheerders en biedt een alleen-lezen weergave van batchtaken en gerelateerde taken.

### <a name="turn-the-wave-batch-job-details-page-on-or-off"></a>De pagina Details van batchtaken voor wave in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Details van wavebatchtaken* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-wave-batch-job-details-page"></a>De pagina Details van batchtaken voor wave gebruiken

Op de pagina **Details van batchtaken voor wave** worden batchtaken en batchtaaktaken gecombineerd, waarmee u alle wavestappen onderzoeken zonder heen en weer te hoeven navigeren tussen één batchtaak en de lijst met batchtaken. De pagina biedt ook toegang tot het batchlogboek en biedt, als u over de vereiste machtigingen beschikt, een koppeling naar de pagina **Batchtaken**.

Als u deze pagina wilt openen, selecteert u een wave op een van de verschillende wavepagina's en selecteert u vervolgens **Details van batchtaken voor wave** in het actievenster.

## <a name="review-load-validation-and-error-messages"></a>Validatie- en foutberichten bij laden bekijken

Tijdens de waveverwerking valideert en geeft het systeem de status weer voor elke ladingregel in de wave. Als er geen waarschuwingen optreden, wordt doorgegaan naar de volgende wavestap. Als er wel waarschuwingen optreden, wordt in plaats daarvan de volgende fout weergegeven nadat de hele wave is gevalideerd:

> Ongeldige laadregels in wave gevonden. Verwijder de ongeldige laadregels.

U kunt vervolgens de uiteindelijke status van elke laadregel in de wave controleren en alle waarschuwingen corrigeren voordat u het opnieuw probeert. Hiermee u alle waarschuwingen in één keer aanpakken voordat u de wave opnieuw verwerkt. (In eerdere versies stopte het systeem met het verwerken van de wave na de eerste waarschuwing, zodat u waarschuwingen slechts één voor één kon oplossen.)

De manier waarop het systeem uw waveverwerkingsstatusberichten weergeeft, is afhankelijk van hoe u de optie **Logboek met historie van waveverwerking maken** hebt ingesteld op de pagina **Magazijnbeheerparameters**.

- Wanneer **Logboek met historie van waveverwerking maken** is ingesteld op *Nee*, worden de statusberichten van de laadregel weergegeven in het **infologboek**.
- Wanneer **Logboek met historie van waveverwerking maken** is ingesteld op *Ja*, worden de statusberichten van de laadregel weergegeven op de pagina **Logboek met historie van waveverwerking**. Als u het logboek wilt bekijken, gaat u **Magazijnbeheer \> Uitgaande waves \> Logboek met historie van waveverwerking**.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Voorbeeld van waveverwerking configureren](tasks/configure-wave-processing.md)
- [Wavesjablonen](wave-templates.md)
- [Containervorming](wave-containerization.md)