---
title: Voorraadplanning
description: Dit artikel bevat informatie over de pagina Voorraadschema en de mogelijkheden ervan.
author: t-benebo
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0e3937dd4cffc464f38b5770674364579bdb06d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851734"
---
# <a name="supply-schedule"></a>Voorraadschema

[!include [banner](../includes/banner.md)]

De pagina **Voorraadschema** geeft een uitgebreid overzicht van vraag en aanbod voor een product of productfamilie. De informatie wordt gefilterd op locatie, hoofdplan en perioden. U kunt de pagina ook gebruiken om nieuwe orders te maken, bestaande geplande orders te wijzigen en de hoofdplanning uit te voeren.

## <a name="open-the-supply-schedule-page"></a>De pagina Voorraadschema openen

U kunt de pagina **Voorraadschema** op een van de volgende manieren openen:

- Ga naar **Hoofdplanning \> Hoofdplanning \> Voorraadschema**. Geef in het dialoogvenster **Filter wijzigen** het plan en het product op dat u wilt zoeken door filterwaarden in te voeren in de beschikbare velden. (In de rest van dit artikel wordt de verzameling filterwaarden die u invoert, het 'filter' of 'huidige filter' genoemd.) Wanneer u klaar bent, selecteert u **OK**.
- Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**. Selecteer of open een product. Selecteer vervolgens in het deelvenster Actie, op het tabblad **Plan**, in de groep **Weergeven**, de optie **Leverschema**.
- Ga naar **Hoofdplanning \> Instellen \> Vraagprognose \> Artikeltoewijzingssleutels**. Selecteer een artikeltoewijzingssleutel die als productfamilie wordt gebruikt. Selecteer vervolgens in het actiepaneel de optie **Leverschema**.
- Ga naar **Hoofdplanning \> Hoofdplanning \> Geplande orders**. Selecteer of open een geplande verkooporder. Selecteer vervolgens in het deelvenster Actie, op het tabblad **Weergeven**, in de groep **Weergeven**, de optie **Leverschema**.

> [!NOTE]
> Wanneer u de pagina **Leverschema** opent vanuit een product, productfamilie of geplande order, hoeft u geen filterwaarden in te voeren. De standaardperiodesjabloon wordt gebruikt.

## <a name="use-the-supply-schedule-page"></a>De pagina Voorraadschema gebruiken

De pagina **Voorraadschema** bestaat uit een bovenste sectie, het sneltabblad **Periode einde voorraad**, een extra sneltabblad waarvan de zichtbaarheid is gebaseerd op de regel die in het bovenste gedeelte is geselecteerd, en het deelvenster Feitenvak. (Als u het deelvenster Feitenvak wilt openen en een feitenvak wilt weergeven, selecteert u **Verwante informatie** aan de rechterkant van de pagina.)

### <a name="upper-section"></a>Bovenste gedeelte

De bovenste sectie van de pagina **Leverschema** bevat een raster met de volgende gegevens voor een product of productfamilie. Deze gegevens worden opgesplitst in perioden die worden gedefinieerd door de waarde **Periodesjabloon** van het filter.

- **Periode begin voorraad** – Deze regel toont het verwachte voorraadsaldo aan het begin van de periode als alle orders in het systeem worden uitgevoerd.
- **Periode einde voorraad** – Deze regel toont het verwachte voorraadsaldo aan het einde van de periode als alle orders in het systeem worden uitgevoerd.
- **Periode einde tracering voorraadbehoefte** – Deze regel toont het voorraadbedrag aan het einde van de periode dat wordt vastgehouden voor de vraag in de toekomst.
- **Periode nettovoorraad** – Deze regel toont het verschil tussen vraag en aanbod in de periode.
- **Minimumvoorraad** - Dit knooppunt toont veiligheidsvoorraad voor een product of productfamilie. Als u dit knooppunt wilt uitvouwen of invouwen, selecteert u dit en selecteert u vervolgens **Uitvouwen** of **Invouwen** op de werkbalk. Dit knooppunt wordt alleen weergegeven als er veiligheidsvoorraad is voor het product of de productfamilie.
- **Vraag** – Dit knooppunt toont vraag voor een product of productfamilie. De vraag wordt gegroepeerd op transactietype. Als u dit knooppunt wilt uitvouwen of invouwen, selecteert u dit en selecteert u vervolgens **Uitvouwen** of **Invouwen** op de werkbalk. Typen vraagtransacties zijn verkoop, overboekingen en voorraadjournalen. Dit knooppunt wordt alleen weergegeven als er vraag is voor het product of de productfamilie.
- **Aanbod** – Dit knooppunt toont aanbod voor een product of productfamilie. Het aanbod wordt gegroepeerd op transactietype. Als u dit knooppunt wilt uitvouwen of invouwen, selecteert u dit en selecteert u vervolgens **Uitvouwen** of **Invouwen** op de werkbalk. Typen leveringstransacties zijn onder andere productie, aankoop en overboekingen. Dit knooppunt wordt alleen weergegeven als er aanbod is voor het product of de productfamilie.

Veel van de beschikbare werkbalkknoppen, weergaven in feitenvakken en op sneltabbladen worden weergegeven afhankelijk van uw selecties in het bovenste gedeelte. Doorgaans kiest u een transactietype door een van de rijen onder het knooppunt **Vraag** of **Aanbod** te selecteren. U kiest vervolgens een periode door een specifieke kolom voor de geselecteerde rij te selecteren.

De werkbalk boven het raster in het bovenste gedeelte van de pagina **Toeleveringsplanning** bevat de volgende knoppen:

- **Uitvouwen/Invouwen** - Een geselecteerd knooppunt uitvouwen of invouwen, zoals het knooppunt **Vraag**, het knooppunt **Aanbod** en hun subknooppunten. (Voor knooppunten wordt een voorvoegsel **\[+\]** of **\[-\]** weergegeven om aan te geven of ze zijn samengevouwen of uitgevouwen.)
- **Nieuw** – Een menu openen waarin elke opdracht op zijn beurt een dialoogvenster of pagina opent waarin u een specifiek type item kunt toevoegen voor de selectie. Beschikbare opdracht zijn onder andere **Prognoseaanbod**, **Geplande order**, **Geplande kanban**, **Nieuwe productieorder**, **Inkooporder** en **Transferorder**.
- **Hoofdplanning** – Hoofdplanning uitvoeren. Er verschijnt een dialoogvenster waarin u kunt opgeven welk plan moet worden uitgevoerd. Standaard voldoet het **Hoofdplan** aan het huidige filter.
- **Maximale gereedmelding** – De pagina **Maximale gereedmelding** openen voor het product dat in het huidige filter is gedefinieerd.
- **Geplande orders bijwerken** – De pagina **Geplande orders** openen, waarin geplande orders worden weergegeven voor het product of de productfamilie dat/die in het huidige filter is gedefinieerd.
- **Niveau** – Geplande orders worden verdeeld volgens de instellingen in het dialoogvenster dat verschijnt.
- **Materiaalplanbeleid per locatie** – De pagina **Artikelbehoefteplanning** openen voor het product dat is gedefinieerd in het huidige filter.
- **Kanbanregel** – De pagina **Kanbanregels** openen voor het product dat in het huidige filter is gedefinieerd.

### <a name="fasttabs"></a>Sneltabbladen

De pagina **Voorraadschema** kan de volgende sneltabbladen bevatten:

- **Periode einde voorraad** – Op dit sneltabblad worden de voorraadgegevens aan het einde van de periode weergegeven in een grafische indeling.
- **Aanbodprofiel** – Op dit sneltabblad worden de aanbodgegevens grafisch weergegeven. Dit wordt zichtbaar wanneer u in het bovenste gedeelte een knooppunt **Aanbod** of een regel daaronder selecteert.
- **Overzicht** – Dit sneltabblad toont overzichtsdetails die betrekking hebben op het transactietype dat u hebt geselecteerd in het bovenste gedeelte. Als u bijvoorbeeld **Verkoop** selecteert onder het knooppunt **Vraag**, wordt op dit sneltabblad velden weergegeven die betrekking hebben op verkooporders, zoals **Aangevraagde verkooporderregels** of **Totaalbedrag**. Als u **Productieorders** selecteert onder het subknooppunt **Productie** van het knooppunt **Aanbod**, worden op dit sneltabblad velden getoond die gerelateerd zijn aan productieorders, zoals **Geplande productieorders** of **Totaal gepland**. De veldwaarden zijn afhankelijk van de periode die u in het bovenste gedeelte hebt geselecteerd. 
- **\[Transactietype\] - \[Period\]** – Op dit sneltabblad worden orders weergegeven voor het transactietype en de periode die u in het bovenste gedeelte hebt geselecteerd. De naam van het sneltabblad weerspiegelt deze selecties. Deze naam kan bijvoorbeeld **Verkooporders - achterstallig** of **Productieorders - week 37** zijn.

### <a name="action-pane"></a>Actievenster

De volgende knoppen zijn beschikbaar in het actievenster:

- **Filter wijzigen** - Het dialoogvenster **Filter wijzigen** openen waarin u filterwaarden kunt bijwerken en vervolgens de pagina **Voorraadplanning** kunt heropenen, waarin de bijgewerkte filterinstellingen worden weergegeven.
- **Vertragingen tonen** – De relevante regels markeren in het bovenste gedeelte als er een vertraagde order van dat transactietype is.

### <a name="factbox-pane"></a>Deelvenster Feitenvak

Als u het deelvenster Feitenvak wilt openen en een feitenvak wilt weergeven, selecteert u **Verwante informatie** aan de rechterkant van de pagina. De volgende feitenvakken zijn beschikbaar op de pagina **Voorraadschema**:

- **Artikeldetails** – Dit feitenvak bevat basisinformatie over het product dat in het huidige filter is gedefinieerd. Het is leeg als u een productfamilie in het filter hebt gedefinieerd.
- **Acties** – In dit feitenvak worden acties weergegeven voor de orders van het transactietype dat u in het bovenste gedeelte hebt geselecteerd.
- **Vertragingen** – In dit feitenvak worden vertragingen weergegeven voor de orders van het transactietype dat u in het bovenste gedeelte hebt geselecteerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
