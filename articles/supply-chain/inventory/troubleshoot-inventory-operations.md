---
title: Problemen met voorraadbewerkingen oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met voorraadbewerkingen.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3a22229106753d265a90f0ef05f5ac82dc745bbd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967150"
---
# <a name="troubleshoot-inventory-operations"></a>Problemen met voorraadbewerkingen oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met voorraadbewerkingen.

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>Ik kan het dialoogvenster met vervolgkeuzemenu "Werkstroom" niet vinden voor voorraadjournalen.

### <a name="issue-description"></a>Probleembeschrijving

U kunt het vervolgkeuzedialoogvenster **Werkstroom** niet vinden op de journaalpagina of er zijn geen gerelateerde werkstroombewerkingen beschikbaar.

Dit probleem kan om drie redenen optreden, zoals wordt beschreven in de volgende subsecties.

### <a name="issue-resolution-1"></a>Probleemoplossing 1

Als het probleem voor alle gebruikers geldt, kan het komen doordat de goedkeuringswerkstroom niet aan de journaalnaam is toegewezen. Volg deze stappen om het probleem op te lossen.

1. Ga naar **Voorraadbeheer &gt; Instellingen &gt; Journaalnamen &gt; Voorraad**.
1. Selecteer een journaalnaam in het lijstdeelvenster om de bijbehorende instellingen te openen.
1. Stel op het sneltabblad **Algemeen** de optie **Goedkeuringswerkstroom** in op *Ja*. Selecteer **Ja** als u wordt gevraagd de wijziging te bevestigen.
1. Selecteer in het veld **Werkstroom** de werkstroom die u voor de geselecteerde journaalnaam wilt gebruiken.

### <a name="issue-resolution-2"></a>Probleemoplossing 2

Als in uw werkstroom aangepaste code wordt gebruikt, kunnen problemen optreden nadat u een upgrade op het systeem hebt uitgevoerd. In de journaalwerkstroom is het bijvoorbeeld mogelijk dat de knop **Indienen** grijs wordt weergegeven, zodat u deze niet kunt selecteren om een indiening goed te keuren.

Als de knop **Indienen** grijs wordt weergegeven, is uw werkstroom mogelijk aangepast. Dit houdt in dat de methode van de werkstroom, `canSubmitToWorkflow()` in `FormDataUtil` is uitgebreid. Om dit probleem op te lossen, wijzigt u de manier waarop u de methode van `canSubmitToWorkflow()` uitbreidt om de structuur in het volgende voorbeeld te gebruiken.

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>Probleemoplossing 3

Als het probleem alleen voor een paar specifieke gebruikers geldt, beschikken deze gebruikers mogelijk niet over de beveiligingsbevoegdheden die zijn vereist om werkstroombewerkingen uit te voeren op voorraadjournalen. Controleer of elke betrokken gebruiker beschikt over de beveiligingsbevoegdheid *Werkstroom voorraadjournaal onderhouden*. Standaard wordt deze bevoegdheid toegewezen aan een taak met dezelfde naam en die taak wordt toegepast op de rollen *Magazijnmedewerker* en *Magazijnbeheerder*.

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>Mijn voorraadjournaal blijft in een door het systeem vergrendelde status en de werkstroombatchtaak werkt niet.

### <a name="issue-description"></a>Probleembeschrijving

Een van uw voorraadjournalen wordt vergrendeld door een bepaalde bewerking en wordt niet vrijgegeven. Als er bijvoorbeeld een onbekende fout optreedt tijdens het boeken (wat een systeemvergrendelingsbewerking is), blijft het journaal mogelijk in de door het systeem vergrendelde status. In dit geval wordt met de handler van het werkstroomwerkitem een fout gegenereerd terwijl de validatie wordt vergrendeld.

### <a name="issue-resolution"></a>Probleemoplossing

Meld u aan bij het SQL Server-exemplaar voor Supply Chain Management en controleer of **InventJournalTable.SystemBlocked** is ingesteld op *1*. Als dat het geval is, zorg er dan voor dat de status van het journaal niet vergrendeld is en stel vervolgens **InventJournalTable.SystemBlocked** in op *0*.

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>Mijn voorraadjournaalwerkstroom wordt nooit voltooid en het journaal kan niet worden bewerkt of geboekt.

### <a name="issue-description"></a>Probleembeschrijving

Nadat u een journaalgoedkeuringswerkstroom hebt ingediend, reageert de werkstroomverwerking niet meer en kunt u uw journalen niet bewerken of verwerken.

### <a name="issue-resolution"></a>Probleemoplossing

Er zijn verschillende redenen waarom de verwerking van werkstromen niet kan worden voltooid. Controleer op de volgende problemen:

- Ga naar **Voorraadbeheer &gt; Instellingen &gt; Voorraadbeheerwerkstromen** en controleer de configuratie van de betrokken werkstroom. Zie [Goedkeuringswerkstromen van voorraadjournalen](inventory-journal-workflow.md) voor meer informatie.
- Mogelijk komt een uitzondering of fout in de werkstroom voor. Controleer de werkitemhistorie van de betrokken werkstroom om te zien of er een toepassingsfout is betrokken bij het beëindigen van de werkstroom.
- Het voorraadjournaal kan alleen worden bijgewerkt of bewerkt als het is goedgekeurd. Als terugroepen actief is, kunt u proberen het journaal terug te roepen. De uitvoering van de werkstroombatchtaak kan om meerdere redenen zijn uitgesteld. Een aantal van deze redenen kan worden veroorzaakt door het probleem met het werkstroomraamwerk.

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>Werkstroomvoorwaarden voor voorraadjournaal zijn alleen van toepassing op journaalniveau, niet op regelniveau

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan zich bijvoorbeeld voordoen als u probeert een werkstroomvoorwaarde voor het voorraadjournaal in te stellen voor het kostenbedrag. U stelt de voorwaarde zo in dat stap 1 alleen wordt uitgevoerd wanneer het kostenbedrag lager is dan 100. U stelt vervolgens een andere voorwaarde in zodat stap 2 alleen wordt uitgevoerd wanneer het kostenbedrag meer is dan of gelijk is aan 100. Wanneer de werkstroom wordt uitgevoerd, wordt in de werkstroomhistorie slechts één regel weergegeven en wordt de eerste voorwaarde altijd als *waar* geëvalueerd, ongeacht de waarde die wordt ingediend.

### <a name="issue-workaround"></a>Tijdelijke oplossing voor probleem

In de huidige versie zijn werkstroomvoorwaarden voor de voorraad alleen van toepassing op journaalniveau, niet op regelniveau. Dit is zo ontworpen. We raden u aan om uw voorwaardecriteria alleen in te stellen op kenmerken op journaalniveau.

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>In het filterdeelvenster van de pagina Voorhanden voorraad worden de resultaten niet gefilterd als verwacht.

### <a name="issue-description"></a>Probleembeschrijving

Met de filters in het filterdeelvenster op de pagina **Voorhanden voorraad**  worden de resultaten niet gefilterd als verwacht.

### <a name="issue-resolution"></a>Probleemoplossing

Dit is zo ontworpen.

De pagina  **Voorhanden voorraad**  wordt samengesteld uit een gedetailleerde tabel met voorhanden voorraad waarin alle beschikbare dimensies zijn opgenomen. De lijst op deze pagina is echter een overzicht. Daarom kunnen rijen uit de brontabel worden gecombineerd door waarden te aggregeren op basis van de dimensies die worden weergegeven.

De filters die in het filterdeelvenster zijn ingesteld, zijn van toepassing op de brontabel en niet op de samengevoegde lijst. Dit gedrag kan soms onverwachte resultaten opleveren, zoals in [deze voorbeelden](inventory-on-hand-list.md#examples) wordt getoond.

De  [filters die in het raster worden vermeld](inventory-on-hand-list.md#grid-filters) hebben echter  *wel*  betrekking op de samengevoegde lijst. Deze filters bevatten zowel het snelfilter boven aan het raster als het filter voor elke kolomkop.

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>De eenheid en hoeveelheid per eenheid werken niet goed in het voorraadjournaal.

### <a name="issue-description"></a>Probleembeschrijving

Er kunnen een of meer van de volgende problemen voorkomen wanneer u met eenheden en hoeveelheden in een voorraadjournaal werkt:

- U ziet geen eenheden of eenheidshoeveelheden in het voorraadjournaal terwijl er een omrekeningseenheid is ingesteld voor het vrijgegeven product en u kunt de eenheid niet wijzigen in het voorraadjournaal.
- U ziet de velden **Hoeveelheid** en **Eenheid** in het voorraadjournaal, maar het veld **Hoeveelheid per eenheid** niet. Als u de eenheid wijzigt, een hoeveelheid invoert en het journaal boekt, wordt in het journaal nog steeds de oorspronkelijke maateenheid voor die hoeveelheid gebruikt.

### <a name="issue-resolution"></a>Probleemoplossing

Volg deze stappen om dit probleem op te lossen.

1. Zorg er in het werkgebied **Functiebeheer** voor dat de functie *Maateenheid en hoeveelheid per eenheid in voorraadjournalen gebruiken* is ingeschakeld. Met deze functie voegt u de velden **Eenheid** en **Hoeveelheid per eenheid** aan het journaal toe.
1. Nadat de functie is ingeschakeld, gebruikt u de velden **Hoeveelheid**, **Hoeveelheid per eenheid** en **Eenheid** als volgt:

    - **Hoeveelheid**: geef de hoeveelheid op door de standaardeenheid te gebruiken die voor het vrijgegeven product is gedefinieerd. De standaardeenheid zelf wordt hier echter niet weergegeven. Als er een omrekening is ingesteld tussen de standaardeenheid en de eenheid die is geselecteerd in het veld **Eenheid**, wordt het veld **Hoeveelheid** automatisch bijgewerkt op basis van de selecties in de velden **Hoeveelheid per eenheid** en **Eenheid**.
    - **Hoeveelheid per eenheid**: geef de hoeveelheid op met behulp van de eenheid die is geselecteerd in het veld **Eenheid**.
    - **Eenheid**: selecteer de eenheid die moet worden toegepast op de waarde in het veld **Hoeveelheid per eenheid**.

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Het volgende foutbericht wordt weergegeven: "Het maximum aantal decimalen voor de voorraadeenheid is 0."

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een voorraadtransactie of voorraadreservering probeert te boeken, wordt het volgende foutbericht weergegeven: "Het maximum aantal decimalen voor de voorraadeenheid is 0."

Dit probleem treedt op wanneer de voorraadtransactiehoeveelheid is opgegeven als een decimale waarde die onder het nauwkeurigheidsniveau ligt dat het veld ondersteunt. Er is bijvoorbeeld een hoeveelheid van *0,5* opgegeven voor een voorraadtransactie, maar alleen de hoeveelheden in de vorm van een geheel getal worden ondersteund. Daarom moet de waarde *1* zijn in plaats van *0,5*.

### <a name="issue-resolution"></a>Probleemoplossing

1. Voer het volgende script op uw SQL Server-exemplaar uit om hoeveelheden in de voorraadtransacties af te ronden. Met dit script corrigeert u waarden in de tabel **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Voer een handmatige consistentiecontrole uit waarbij de optie **Fout oplossen** is ingeschakeld. Met deze controle worden waarden in de tabel **inventSum** gecorrigeerd.

> [!IMPORTANT]
> Het is raadzaam het script zorgvuldig te bewerken voor uw omgeving, het te testen in een testomgeving en vervolgens de resulterende gegevens te controleren voordat u het script in een productieomgeving uitvoert.
