---
title: Voorraadprognoses
description: In dit onderwerp worden de functies voor aanbod- en vraagprognose beschreven die kunnen worden gebruikt om voorraadprognoses te maken in Microsoft Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 5ce997a0bb3d6766b801f3f4dea8ab3f19085d02
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577547"
---
# <a name="inventory-forecasts"></a>Voorraadprognoses

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u voorraadprognoses maakt en bekijkt. U kunt aanbod- en vraagprognoseregels maken en weergeven voor artikelen, artikelgroepen, artikeltoewijzingssleutels, klantrekeningen, klantgroepen, leveranciersrekeningen en leveranciersgroepen.

Voor elke prognoseregel kunt u het prognosemodel selecteren dat wordt gebruikt. U kunt vervolgens het artikel of de artikelgroep plus de hoeveelheid of het transactiebedrag opgeven. U kunt ook een tijdschema instellen voor toewijzing van de prognosehoeveelheid.

De aanbod- en vraagprognoseregels produceren een voorraadprognose voor dezelfde combinatie van een artikel en een model. Deze voorraadprognose geeft een saldo weer tussen het aanbod en de vraag die voor hetzelfde artikel zijn ingevoerd. Deze waarde kan niet worden bewerkt. De voorraadprognose helpt het voorraadbeheerteam om verwachte wijzigingen in de voorhanden voorraad van een artikel tijdens de komende periode die is geprognosticeerd te controleren.

Nadat u uw vraag en/of aanbod hebt ingesteld, kunt u prognoseplanning uitvoeren om de brutobehoeften voor de materialen en capaciteit te berekenen en om geplande orders te genereren.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Prognoseregels weergeven en handmatig invoeren

Gebruik deze procedure om prognoseregels voor producten handmatig te maken.

Er zijn ook andere manieren om prognoseregels te maken:

- [Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md).
- [Historische gegevens voor vraagprognoses importeren](import-historical-data.md).
- [De prognose genereren met behulp van een Microsoft Azure Machine Learning-webservice](demand-forecasting-setup.md).
- [Vraag- of aanbodprognoseregels importeren met behulp van het gegevensbeheerraamwerk (gegevensentiteiten ForecastDemandForecastEntryStaging en ForecastSupplyForecastEntryStaging)](../../dev-itpro/data-entities/data-entities-data-packages.md).

Zoals de tabel in stap 1 aangeeft, zijn er verschillende manieren om de gebruikte pagina's te openen.

1. Afhankelijk van het entiteitstype waarvoor u een prognose wilt maken en het prognosetype dat u wilt maken, opent u een aanbod-, vraag- of voorraadprognosepagina, zoals wordt beschreven in de volgende tabel.

    | Entiteit | Instructies |
    |---|---|
    | Vrijgegeven producten | <ol><li>Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</li><li>Selecteer het product waarvoor u een prognose wilt maken.</li><li>Selecteer in het actievenster op het tabblad **Plan** in de groep **Prognose** **Vraagprognose**, **Aanbodprognose** of **Voorraadprognose**, afhankelijk van het prognosetype waarmee u wilt werken.</li></ol> |
    | Vrijgegeven productvarianten | <ol><li>Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven productvarianten**.</li><li>Selecteer de variant waarvoor u een prognose wilt maken.</li><li>Selecteer in het actievenster op het tabblad **Plan** in de groep **Prognose** **Vraagprognose**, **Aanbodprognose** of **Voorraadprognose**, afhankelijk van het prognosetype waarmee u wilt werken.</li></ol> |
    | Artikelengroepen | <ol><li>Ga naar **Voorraadbeheer \> Instellingen \> Voorraad \> Artikelgroepen**.</li><li>Selecteer de artikelgroep waarvoor u een prognose wilt maken.</li><li>Selecteer in het actievenster **Prognose \> Vraag**, **Prognose \> Aanbod** of **Prognose \> Voorraadprognose**, afhankelijk van het prognosetype waarmee u wilt werken.</li></ol> |
    | Artikeltoewijzingssleutels | <ol><li>Ga naar **Voorraadbeheer \> Instellen \> Prognose**.</li><li>Selecteer de artikeltoewijzingssleutel waarvoor u een prognose wilt maken.</li><li>Selecteer **Vraagprognose** in het actievenster.</li></ol> |
    | Klanten | <ol><li>Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Klanten**.</li><li>Selecteer de klant waarvoor u een prognose wilt maken.</li><li>Selecteer **Vraagprognose definiëren** in het actievenster.</li></ol> |
    | Klantengroepen | <ol><li>Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Klantgroepen**.</li><li>Selecteer de klantgroep waarvoor u een prognose wilt maken.</li><li>Selecteer **Vraagprognose definiëren** in het actievenster.</li></ol> |
    | Leveranciers | <ol><li>Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Leveranciers**.</li><li>Selecteer de leverancier waarvoor u een prognose wilt maken.</li><li>Selecteer in het actievenster **Invoer** om de pagina **Aanbodprognose** te openen.</li></ol> |
    | Leveranciersgroepen | <ol><li>Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Leveranciersgroepen**.</li><li>Selecteer de leveranciersgroep waarvoor u een prognose wilt maken.</li><li>Selecteer in het actievenster **Invoer** om de pagina **Aanbodprognose** te openen.</li></ol> | 
    | Alle regels | <ul><li>Ga naar **Hoofdplanning \> Prognose \> Vraagprognoseregels** of **Hoofdplanning \> Prognose \> Aanbodprognoseregels**, afhankelijk van het prognosetype waarmee u wilt werken.</li></ul> |

    Afhankelijk van wat u hebt geselecteerd, verschijnt de pagina **Aanbodprognose** of **Vraagprognose**. Hier worden bestaande prognoseregels weergegeven voor de record die u hebt geselecteerd voordat u de pagina hebt geopend.

1. Selecteer in het actievenster de optie **Nieuw** om een prognoseregel toe te voegen aan het raster in het bovenste deel van de pagina.
1. Selecteer op de nieuwe regel in het veld **Model** het prognosemodel dat u wilt gebruiken. Voer vervolgens zo nodig andere gegevens in, zoals het artikel, de artikelgroep, de klant- of leveranciersrekening of de groep, de artikelhoeveelheid of het totale transactiebedrag. Zie de volgende gedeelten in dit onderwerp voor volledige details over de velden die beschikbaar zijn op de pagina's **Aanbodprognose** en **Vraagprognose**.
1. Als u de prognose over de periode wilt verdelen, selecteert u op het tabblad **Overzicht** de optie **Prognose toewijzen** op de werkbalk.
1. Controleer in het raster **Toewijzing** de periode en de intervallen die worden gebruikt voor het verdelen van de prognosehoeveelheden.

## <a name="supply-forecast-lines"></a>Aanbodprognoseregels

Met de aanbodprognose kunt u een plan maken voor artikelen die moeten worden ingekocht. Het laat de inkoop- en sourcing-medewerkers weten wat ze moeten bestellen.

U kunt een aanbodprognose invoeren per artikel, artikelgroep, artikeltoewijzingssleutel, leverancier en leveranciersgroep. Zie het gedeelte [Prognoseregels weergeven en handmatig invoeren](#manual-entry) eerder in dit onderwerp voor informatie over alle manieren om de pagina **Aanbodprognose** voor verschillende entiteiten en records te openen.

Het bovenste deel van de pagina **Aanbodprognose** biedt een raster van aanbodprognoseregels en een reeks tabbladen die u kunt gebruiken om meer informatie over een geselecteerde prognoseregel weer te geven en in te stellen. Het onderste deel van de pagina bevat het raster **Toewijzing**.

In de volgende subgedeelten worden alle velden beschreven die beschikbaar zijn op elk tabblad, en alle opdrachten die beschikbaar zijn in het actievenster van de pagina en op de werkbalk op het tabblad **Overzicht**.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Opdrachten in het actievenster op de pagina Aanbodprognose

In de volgende tabel worden de opdrachten beschreven die beschikbaar zijn in het actievenster van de pagina **Aanbodprognose**.

| Opdracht | Beschrijving |
|---|---|
| Opslaan | Sla de huidige instellingen op. |
| Bewerken | Schakel instellingen in op de pagina die moet worden bewerkt. |
| Nieuw | Voeg een prognoseregel aan het bovenste raster toe. |
| Delete | Verwijder de geselecteerde prognoseregel uit het bovenste raster. |
| Saldiprognose | Geef prognosesaldi weer die zijn berekend voor de model-ID van de geselecteerde regel voor het huidige boekjaar. De saldi worden opgesplitst per periode (maand). |
| Cashflowprognoses | Geef prognosetransacties weer die aan het grootboek zijn toegewezen. Zie [Cashflowprognose](../../finance/cash-bank-management/cash-flow-forecasting.md) voor meer informatie. |
| Voorraad \> Dimensies weergeven | Selecteer de voorraaddimensies die moeten worden weergegeven in het raster op het tabblad **Overzicht**. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Werkbalkopdrachten op het tabblad Overzicht van de pagina Aanbodprognose

In de volgende tabel worden de opdrachten beschreven die beschikbaar zijn op de werkbalk van het tabblad **Overzicht** van de pagina **Aanbodprognose**.

| Opdracht | Beschrijving |
|---|---|
| Prognose toewijzen | Als u een toewijzingsmethode gebruikt, genereert u de afzonderlijke schemaregels voor de prognosetransactie. De hoeveelheid van de regel wordt vervolgens verdeeld op datum (op basis van de geselecteerde tijdsintervallen), hoeveelheid en bedrag voor de hele periode. (Zie de sectie [Prognose toewijzen](#allocate-forecast) verderop in dit onderwerp.) |
| Bulkupdate | Open de pagina **Prognosetransacties bewerken**. (Zie het gedeelte [Prognosetransacties groepsgewijs bijwerken](#bulk-update) verderop in dit onderwerp.) |
| Voorraadprognose | Open een weergave van de pagina **Voorraadprognose** die is gefilterd op de geselecteerde combinatie van artikel/model. (Zie het gedeelte [Voorraadprognose](#inventory-forecast) verderop in dit onderwerp.) |
| Artikelbehoefte maken | Open een dialoogvenster waarin u artikelbehoeften en verkooporder- of artikeljournaalregels kunt maken voor projectgerelateerde prognosetransacties. Hoewel deze opdracht beschikbaar is voor zowel aanbodprognoseregels als vraagprognoseregels, kan deze niet worden gebruikt op de pagina **Aanbodprognose**. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Het tabblad Overzicht van de pagina Aanbodprognose

In de volgende tabel worden de velden op het tabblad **Overzicht** van de pagina **Aanbodprognose** beschreven.

| Veld | Beschrijving |
|---|---|
| **Model** | Het prognosemodel waaraan de transactie is gekoppeld. |
| **Datum** | De begindatum van de transactie. |
| **Leverancier** | De leveranciersrekening waaraan de transactie is gekoppeld. |
| **Leveranciersgroep** | De leveranciersgroep waaraan de transactie is gekoppeld. |
| **Artikelnummer** | De ID van het artikel. |
| **Artikelengroep** | De artikelgroep waaraan de transactie is gekoppeld. |
| **Artikeltoewijzingssleutel** | De artikeltoewijzingssleutel die aan de prognose is gekoppeld. |
| **Hoeveelheid variabel gewicht** | De prognosehoeveelheid in de opgegeven catch weight-eenheid. |
| **Eenheid variabel gewicht** | De catch weight-eenheid waarin het artikel wordt ingekocht. De waarde wordt automatisch opgehaald uit de artikelinstellingen. |
| **Hoeveelheid** | De prognosehoeveelheid in de opgegeven inkoopeenheid. |
| **Eenheid** | De eenheid waarin het artikel wordt ingekocht. De waarde wordt automatisch opgehaald uit de artikelinstellingen. U kunt deze eenheid echter wijzigen als er eenheidconversies zijn ingesteld. |
| **Bedrag** | Het brutobedrag minus kortingen dat de prognosetransactie bijdraagt aan de prognose. |
| **Valuta** | De valuta die wordt gebruikt voor de prognosetransactie. De standaardvaluta wordt automatisch ingevoerd, maar u kunt een andere valuta selecteren. |
| (Overige dimensies) | Extra dimensies kunnen als kolommen in het raster worden weergegeven. Selecteer **Dimensies weergeven** in het actievenster om de extra dimensies te selecteren die worden weergegeven. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Het tabblad Algemeen van de pagina Aanbodprognose

Op het tabblad **Algemeen** wordt meer informatie weergegeven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd. Een aantal van deze gegevens wordt herhaald via het tabblad **Overzicht**. In de volgende tabel worden de velden beschreven die uniek zijn voor het tabblad **Algemeen**.

| Veld | Beschrijving |
|---|---|
| Rapport | Stel deze optie in op *Ja* om de transactie op te nemen in de rapportage. |
| Opmerkingen | Voer eventueel opmerkingen in over de prognosetransactie. |
| Actief | Schakel dit selectievakje in om de transactie op te nemen in de budgetrapportage. |
| Opnemen in cashflowprognoses | Schakel dit selectievakje in om de prognosetransactie toe te wijzen aan het Grootboek. De instelling van dit selectievakje kan niet worden gewijzigd voor het rapporteren van transacties. |
| Btw-groep | De belastinggroep die wordt gebruikt voor het opgeven van de belasting voor de prognosetransactie. |
| Btw-groep voor artikel | De artikelbelastinggroep die wordt gebruikt voor het opgeven van de belasting voor de prognosetransactie. |
| methode | <p>Selecteer de methode die wordt gebruikt om de prognosetransactie toe te wijzen:</p><ul><li>**Geen** – Er vindt geen toewijzing plaats.</li><li>**Periode** – Prognose van dezelfde hoeveelheid voor elke periode. Als u deze waarde selecteert, geeft u een hoeveelheid op in het veld **Per** en een tijdseenheid in het veld **Eenheid**.</li><li>**Sleutel** – De prognosehoeveelheid wordt toegewezen aan de periodetoewijzingssleutel die u in het veld **Periodesleutel** opgeeft. U kunt deze methode gebruiken wanneer u rekening wilt houden met de seizoensverschillen.</li></ol>|
| Per | <p>Voer het aantal tijdsintervallen in de toekomst in waarover de prognose zich uitstrekt. Dit veld is alleen beschikbaar als u *Periode* selecteert in het veld **Methode**.</p><p>U selecteert bijvoorbeeld *Periode* in het veld **Methode**, voert *1* in het veld **Per** in en selecteert *Maanden* in het veld **Eenheid**. Geef een einddatum op in het veld **Einde** dat een jaar in de toekomst ligt. In dit geval wordt er wordt één prognoseregel gemaakt voor elke maand van het komende jaar op basis van het artikel en de hoeveelheid die worden opgegeven in de kopregel.</p> |
| Eenheid | Selecteer de eenheid van het tijdsinterval: *Dagen*, *Maanden* of *Jaren*. De toewijzing komt dan overeen met het aantal dagen, maanden of jaren dat u opgeeft in het veld **Per**.|
| Periodesleutel | Geef de periodetoewijzingssleutel op. |
| Einde | Geef de einddatum op wanneer u de velden **Per** en **Eenheid** gebruikt. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Het tabblad Artikel van de pagina Aanbodprognose

Op het tabblad **Artikel** wordt meer artikelinformatie weergegeven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd.

Het raster boven aan het tabblad **Artikel** herhaalt artikelgegevens die ook worden weergegeven op het tabblad **Overzicht**. Bovendien bevat het raster het veld **Eenheidsprijs**, waarin de inkoopprijs wordt aangegeven voor het aantal eenheden dat is opgegeven in het veld **Eenheid**. De eenheidsprijs wordt automatisch opgehaald uit de instellingen van het artikel, maar kan wel worden gewijzigd.

De velden onder het raster bieden meer artikeldetails. Een aantal van deze gegevens wordt herhaald via het tabblad **Overzicht**. In de volgende tabel worden de velden beschreven die uniek zijn op het tabblad **Artikel**.

| Veld | Beschrijving |
|---|---|
| Prijseenheid | Het aantal eenheden waarop de inkoopprijs van toepassing is. De waarde wordt automatisch opgehaald uit de tabel Artikelen, maar kan worden gewijzigd. |
| Toeslagen op inkopen | Vaste kosten in de verkoopprijs. De kosten zijn onafhankelijk van de hoeveelheid. |
| Kortingspercentage | De korting als een percentage. |
| Kortingsbedrag | De korting als een bedrag per verkoopeenheid. |
| Brutobedrag | Het bedrag waarop geen kortingen van toepassing zijn. |
| Hoeveelheid | De transactiehoeveelheid in de voorraadeenheid van het artikel. |
| Substuklijst | Het stuklijstnummer van een specifieke substuklijst. |
| Subroute | Het routenummer van een bepaalde subroute. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Het tabblad Financiële dimensies van de pagina Aanbodprognose

Op het tabblad **Financiële dimensies** worden alle waarden van financiële dimensies weergegeven voor de regel die momenteel is geselecteerd op het tabblad **Overzicht**.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Het tabblad Voorraaddimensies van de pagina Aanbodprognose

Op het tabblad **Voorraaddimensies** worden alle waarden van voorraaddimensies weergegeven voor de regel die momenteel is geselecteerd op het tabblad **Overzicht**.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Het raster Toewijzing van de pagina Aanbodprognose

Als u een artikeltoewijzingssleutel gebruikt of als u een artikelprognose voor een of meer toekomstige perioden hebt ingevoerd, kunt u de prognose toewijzen door **Prognose toewijzen** op de werkbalk op het tabblad **Overzicht** te selecteren. De hoeveelheid wordt vervolgens verdeeld op de manier die wordt aangegeven door de regels in het raster **Toewijzing**.

## <a name="demand-forecast-lines"></a>Vraagprognoseregels

Met de vraagprognose kunt u de vraag voor een klant invoeren of genereren. Het helpt verkoop- en marketingmedewerkers om hoofdplanningsmedewerkers te informeren over de verwachte vraag tijdens de komende prognoseperiode.

U kunt een vraagprognose invoeren per artikel, artikelgroep, artikeltoewijzingssleutel, klant en klantgroep. Zie het gedeelte [Prognoseregels weergeven en handmatig invoeren](#manual-entry) eerder in dit onderwerp voor informatie over alle manieren om de pagina **Vraagprognose** voor verschillende entiteiten en records te openen.

Het bovenste deel van de pagina **Vraagprognose** biedt een raster van vraagprognoseregels en een reeks tabbladen die u kunt gebruiken om meer informatie over een geselecteerde prognoseregel weer te geven en in te stellen. Het onderste deel van de pagina bevat het raster **Toewijzing**.

In de volgende subgedeelten worden alle velden beschreven die beschikbaar zijn op elk tabblad, en alle opdrachten die beschikbaar zijn in het actievenster van de pagina en op de werkbalk op het tabblad **Overzicht**.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Opdrachten in het actievenster op de pagina Vraagprognose

In de volgende tabel worden de opdrachten beschreven die beschikbaar zijn in het actievenster van de pagina **Vraagprognose**.

| Opdracht | Beschrijving |
|---|---|
| Opslaan | Sla de huidige instellingen op. |
| Bewerken | Schakel instellingen in op de pagina die moet worden bewerkt. |
| Nieuw | Voeg een prognoseregel aan het bovenste raster toe. |
| Delete | Verwijder de geselecteerde prognoseregel uit het bovenste raster. |
| Saldiprognose | Geef prognosesaldi weer die zijn berekend voor de model-ID van de geselecteerde regel voor het huidige boekjaar. De saldi worden opgesplitst per periode (maand). |
| Cashflowprognose | Geef prognosetransacties weer die aan het grootboek moeten worden toegewezen. Zie [Cashflowprognose](../../finance/cash-bank-management/cash-flow-forecasting.md) voor meer informatie. |
| Dimensies weergeven | Selecteer product-, opslag- en traceringsdimensies die moeten worden weergegeven in het raster op het tabblad **Overzicht**. |
| Voorbeeld grootboek | Geef de grootboekposten voor de geselecteerde transactie weer. |
| Offerteregels overbrengen | Breng de offerteregels naar het geselecteerde project over. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Werkbalkopdrachten op het tabblad Overzicht van de pagina Vraagprognose

In de volgende tabel worden de opdrachten beschreven die beschikbaar zijn op de werkbalk van het tabblad **Overzicht** van de pagina **Vraagprognose**.

| Opdracht | Beschrijving |
|---|---|
| Prognose toewijzen | Als u een toewijzingsmethode gebruikt, genereert u de afzonderlijke schemaregels voor de prognosetransactie. De hoeveelheid van de regel wordt vervolgens verdeeld op datum (op basis van de geselecteerde tijdsintervallen), hoeveelheid en bedrag voor de hele periode. (Zie de sectie [Prognose toewijzen](#allocate-forecast) verderop in dit onderwerp.)|
| Bulkupdate | Open de pagina **Prognosetransacties bewerken**. (Zie het gedeelte [Prognosetransacties groepsgewijs bijwerken](#bulk-update) verderop in dit onderwerp.) |
| Voorraadprognose | Open een weergave van de pagina **Voorraadprognose** die is gefilterd op de geselecteerde combinatie van artikel/model. (Zie het gedeelte [Voorraadprognose](#inventory-forecast) verderop in dit onderwerp.) |
| Artikelbehoefte maken | Open een dialoogvenster waarin u artikelbehoeften en verkooporder- of artikeljournaalregels kunt maken voor projectgerelateerde prognosetransacties. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Het tabblad Overzicht van de pagina Vraagprognose

In de volgende tabel worden de velden op het tabblad **Overzicht** van de pagina **Vraagprognose** beschreven.

| Veld | Beschrijving |
|---|---|
| **Naam taak** | De naam van de batchtaak die is gebruikt om de prognoseregel te maken. |
| **Model** | Het prognosemodel waaraan de transactie is gekoppeld. |
| **Datum** | De begindatum van de transactie. |
| **Klantrekening** | De klantrekening waaraan de transactie is gekoppeld. |
| **Klantgroep** | De klantgroep waaraan de transactie is gekoppeld. |
| **Artikelnummer** | De ID van het artikel. |
| **Productnaam** | De omschrijving van het artikel. |
| **Artikeltoewijzingssleutel** | De artikeltoewijzingssleutel die tijdens voorraadprognosetoewijzing wordt gebruikt. |
| **Verkoophoeveelheid** | De transactiehoeveelheid in de opgegeven verkoopeenheid. |
| **Eenheid** | De eenheid waarin het artikel wordt verkocht. |
| **Bedrag** | Het brutobedrag exclusief kortingen dat de prognosetransactie bijdraagt aan de prognose. |
| **Verkoopprijs** | De verkoopprijs voor het aantal eenheden dat is opgegeven in het veld **Prijseenheid**. De waarde wordt opgehaald uit de instellingen van het artikel, maar kan wel worden bewerkt. |
| **Verkoopvaluta** | De valuta die wordt gebruikt voor de prognosetransactie. De standaardvaluta wordt automatisch ingevoerd, maar u kunt een andere valuta selecteren. |
| **Hoeveelheid variabel gewicht** | De prognosehoeveelheid in de opgegeven catch weight-eenheid. |
| **Eenheid variabel gewicht** | De catch weight-eenheid waarin het artikel wordt verkocht. De waarde wordt automatisch opgehaald uit de artikelinstellingen. |
| (Overige dimensies) | Extra product-, opslag- en traceringsdimensies kunnen als kolommen in het raster worden weergegeven. Selecteer **Dimensies weergeven** in het actievenster om de extra dimensies te selecteren die worden weergegeven. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Het tabblad Algemeen van de pagina Vraagprognose

Op het tabblad **Algemeen** wordt meer informatie weergegeven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd. Een aantal van deze gegevens wordt herhaald via het tabblad **Overzicht**. In de volgende tabel worden de velden beschreven die uniek zijn voor het tabblad **Algemeen**.

| Veld | Beschrijving |
|---|---|
| Volgnummer vraagprognose | Het unieke nummer van de vraagprognoseregel. Dit nummer wordt gegenereerd aan de hand van de nummerreeks die is geselecteerd voor vraagprognoses op de pagina **Parameters van hoofdplanning**. |
| Artikelengroep | De artikelgroep waaraan de transactie is gekoppeld. |
| Rapport | Stel deze optie in op *Ja* om de transactie op te nemen in de rapportage. |
| Opmerkingen | Voer eventueel opmerkingen in over de prognosetransactie. |
| Actief | Schakel dit selectievakje in om de transactie op te nemen in de budgetrapportage. De instelling van dit selectievakje kan niet worden gewijzigd voor het rapporteren van transacties. |
| Opnemen in cashflowprognoses | Schakel dit selectievakje in om de prognosetransactie toe te wijzen aan het Grootboek. De instelling van dit selectievakje kan niet worden gewijzigd voor het rapporteren van transacties. Zie [Cashflowprognose](../../finance/cash-bank-management/cash-flow-forecasting.md) voor meer informatie. |
| Btw-groep | De belastinggroep die wordt gebruikt voor het opgeven van de belasting voor de prognosetransactie. |
| Btw-groep voor artikel | De artikelbelastinggroep die wordt gebruikt voor het opgeven van de belasting voor de prognosetransactie. |
| methode | <p>Selecteer de methode die wordt gebruikt om de prognosetransactie toe te wijzen:</p><ul><li>**Geen** – Er vindt geen toewijzing plaats.</li><li>**Periode** – Prognose van dezelfde hoeveelheid voor elke periode. Als u deze waarde selecteert, geeft u een hoeveelheid op in het veld **Per** en een tijdseenheid in het veld **Eenheid**.</li><li>**Sleutel** – De prognosehoeveelheid wordt toegewezen aan de periodetoewijzingssleutel die u in het veld **Periodesleutel** opgeeft. U kunt deze methode gebruiken wanneer u rekening wilt houden met de seizoensverschillen.</li><ul>|
| Per | <p>Voer het aantal tijdsintervallen in de toekomst in waarover de prognose zich uitstrekt. Dit veld is alleen beschikbaar als u *Periode* selecteert in het veld **Methode**.</p><p>U selecteert bijvoorbeeld *Periode* in het veld **Methode**, voert *1* in het veld **Per** in en selecteert *Maanden* in het veld **Eenheid**. Geef een einddatum op in het veld **Einde** dat een jaar in de toekomst ligt. In dit geval wordt er wordt één prognoseregel gemaakt voor elke maand van het komende jaar op basis van het artikel en de hoeveelheid die worden opgegeven in de kopregel. |
| Eenheid | Selecteer de eenheid van het tijdsinterval: *Dagen*, *Maanden* of *Jaren*. De toewijzing komt dan overeen met het aantal dagen, maanden of jaren dat u opgeeft in het veld **Per**.|
| Periodesleutel | Geef de periodetoewijzingssleutel op die wordt gebruikt om de prognose toe te wijzen. Zie [Gegevenstoewijzing voor budgetplanning](../../finance/budgeting/budget-planning-data-allocation.md) voor meer informatie. |
| Einde | Geef de einddatum op wanneer u de velden **Per** en **Eenheid** gebruikt. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Het tabblad Artikel van de pagina Vraagprognose

Op het tabblad **Artikel** wordt meer artikelinformatie weergegeven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd. Een aantal van deze gegevens wordt herhaald via het tabblad **Overzicht**. In de volgende tabel worden de velden beschreven die uniek zijn voor het tabblad **Artikel**.

| Veld | Beschrijving |
|---|---|
| Prijseenheid | Het aantal verkoopeenheden waarop de verkoopprijs van toepassing is. De waarde wordt automatisch opgehaald uit de tabel Artikelen, maar kan worden gewijzigd. |
| Verkooptoeslagen | Vaste kosten op de verkoopprijs. De kosten zijn onafhankelijk van de hoeveelheid. |
| Kostprijs | De kostprijs van de huidige prognosetransactie per voorraadeenheid. De waarde wordt opgehaald uit de tabel Artikelen, maar u kunt deze wijzigen. |
| Kortingspercentage | De korting als een percentage. |
| Kortingsbedrag | De korting als een bedrag per verkoopeenheid. |
| Brutobedrag | Het bedrag waarop geen kortingen van toepassing zijn. |
| Voorraadhoeveelheid | De transactiehoeveelheid in de voorraadeenheid van het artikel. |
| Specifieke stuklijst gebruiken | Het stuklijstnummer van een specifieke stuklijst. |
| Specifieke route gebruiken | Het routenummer van een bepaalde subroute. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Het tabblad Project van de pagina Vraagprognose

Op het tabblad **Project** wordt meer projectinformatie weergegeven over de regel die momenteel op het tabblad **Overzicht** is geselecteerd. Een aantal van deze gegevens wordt herhaald via het tabblad **Overzicht**, **Algemeen** of **Artikel**. In de volgende tabel worden de velden beschreven die uniek zijn voor het tabblad **Project**.

| Veld | Beschrijving |
|---|---|
| Projectdatum | De datum van de vraagprognosetransactie. |
| Project-ID | De id van het project waarnaar door de huidige transactie wordt verwezen. |
| Financieringsbron | De financieringsbron waaraan de vraagprognose is gekoppeld. |
| Activiteitsnummer | De activiteit die is gekoppeld aan de vraagprognosetransactie. |
| Categorie | De kostencategorie van de huidige transactie. |
| Regeleigenschap | De status die aan de transactie is gekoppeld. |
| Transactie-ID | De systeem-id voor de vraagprognosetransactie. |
| Kosten | Het bedrag van de vraagprognosetransactie. |
| Eenheidsprijs | De prijs per eenheid. |
| Gewijzigd door | De id van de werknemer die de geselecteerde transactie het laatst heeft gewijzigd. |
| Factuurdatum | Voer de verwachte factuurdatum in. |
| Schrappingsdatum | De schrappingsdatum bekijken of wijzigen. Bij het maken van de prognose wordt de schrappingsdatum ingesteld op de einddatum van het project. Als het project geen einddatum heeft, wordt de projectdatum gebruikt. Dit veld geldt alleen voor projecten met vaste prijzen en investeringsprojecten. |
| Betalingsdatum kosten | Voer de verwachte datum van de inkoopbetaling in. |
| Betalingsdatum verkoop | Voer de verwachte datum van de verkoopbetaling in. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Het tabblad Financiële dimensies van de pagina Vraagprognose

Op het tabblad **Financiële dimensies** worden alle waarden van financiële dimensies weergegeven voor de regel die momenteel is geselecteerd op het tabblad **Overzicht**.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Het tabblad Voorraaddimensies van de pagina Vraagprognose

Op het tabblad **Voorraaddimensies** worden alle waarden van voorraaddimensies weergegeven voor de regel die momenteel is geselecteerd op het tabblad **Overzicht**.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Het raster Toewijzing van de pagina Vraagprognose

Als u een artikeltoewijzingssleutel gebruikt of als u een artikelprognose voor een of meer toekomstige perioden hebt ingevoerd, kunt u de prognose toewijzen door **Prognose toewijzen** op de werkbalk op het tabblad **Overzicht** te selecteren. De hoeveelheid wordt vervolgens verdeeld op de manier die wordt aangegeven door de regels in het raster **Toewijzing**. (Zie de sectie [Prognose toewijzen](#allocate-forecast) verderop in dit onderwerp.)

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Voorraadprognose

De pagina's voor aanbod- en vraagprognoseregels hebben de knop **Voorraadprognose** waarmee een weergave wordt geopend van de pagina **Voorraadprognose** die is gefilterd op dezelfde combinatie van artikel/model. De voorraadprognose geeft een saldo weer tussen het aanbod en de vraag, dat voor hetzelfde artikel is ingevoerd. Deze waarde kan niet worden bewerkt. De voorraadprognose helpt het voorraadbeheerteam om verwachte wijzigingen in de voorhanden voorraad van een artikel tijdens de komende periode die is geprognosticeerd te controleren.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Het actievenster op de pagina Voorraadprognose

In de volgende tabel worden de opdrachten beschreven die beschikbaar zijn in het actievenster van de pagina **Voorraadprognose**.

| Actie | Beschrijving |
|---|---|
| Aanbodprognose | Open een weergave van de pagina **Aanbodprognose** die is gefilterd op de geselecteerde combinatie van artikel/model/datum. |
| Vraagprognose | Open een weergave van de pagina **Vraagprognose** die is gefilterd op de geselecteerde combinatie van artikel/model/datum. |
| Voorraad \> Dimensies weergeven | Selecteer product-, opslag- en traceringsdimensies die moeten worden weergegeven in het raster **Overzicht**. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Het raster op de pagina Voorraadprognose

In de volgende tabel worden de velden in het raster op de pagina **Voorraadprognose** beschreven.

| Veld | Beschrijving |
|---|---|
| **Model** | Het prognosemodel waaraan de transactie is gekoppeld. |
| **Artikelnummer** | De ID van het artikel. |
| **Budgetdatum** | De datum van de prognosetransactie. |
| **Prognosetype** | De bron van de transactie (*Vraagprognose* of *Aanbodprognose*). |
| **Hoeveelheid variabel gewicht** | De prognosehoeveelheid in de catch weight-eenheid. |
| **Hoeveelheid** | De prognosehoeveelheid in de voorraadeenheid. |
| **Cumulatief variabel gewicht** | De samengevoegde prognosehoeveelheid in de catch weight-eenheid wanneer meerdere prognoseregels zijn samengevoegd voor hetzelfde artikel. |
| **Substuklijst** | Het stuklijstnummer van een bepaalde substuklijst. |
| **Subroute** | Het routenummer van een bepaalde subroute. |
| (Overige dimensies) | Extra dimensies kunnen als kolommen in het raster worden weergegeven. Selecteer **Voorraad \> Dimensies weergeven** in het actievenster om de extra dimensies te selecteren die worden weergegeven. |

## <a name="allocate-forecast"></a><a name="allocate-forecast"></a>Prognose toewijzen

Gebruik de volgende procedure om geselecteerde prognosetransactieregels te verwerken. Wanneer u een prognose toewijst, wordt de hoeveelheid verdeeld op basis van de regels in het **toewijzingsraster**.

1. Afhankelijk van het type entiteit waarvoor u een prognose wilt maken en het prognosetype dat u wilt maken, opent u een pagina voor een aanbod- of vraagprognose, zoals wordt beschreven in [Prognoseregels weergeven en handmatig invoeren](#manual-entry).
1. Selecteer op de pagina met vraag- of aanbodprognoseregels een prognoseregel en selecteer vervolgens op het tabblad **Overzicht** de optie **Prognose toewijzen** op de werkbalk.
1. Stel in het dialoogvenster **Prognose toewijzen** de velden in die in de volgende tabel worden beschreven. (De waarde die u selecteert in het veld **Methode**, bepaalt of er andere velden beschikbaar zijn.)

    | Veld | Beschrijving |
    |---|---|
    | methode | <p>Selecteer de methode die wordt gebruikt om de prognosetransactie toe te wijzen:</p><ul><li>**Geen** – Er vindt geen toewijzing plaats.</li><li>**Periode** – Prognose van dezelfde hoeveelheid voor elke periode. Als u deze waarde selecteert, geeft u een hoeveelheid op in het veld **Per** en een tijdseenheid in het veld **Eenheid**.</li><li>**Sleutel** – De prognosehoeveelheid wordt toegewezen aan de periodetoewijzingssleutel die u in het veld **Periodesleutel** opgeeft. U kunt deze methode gebruiken wanneer u rekening wilt houden met de seizoensverschillen.</li><ul>|
    | Per | <p>Voer het aantal tijdsintervallen in de toekomst in waarover de prognose zich uitstrekt. Dit veld is alleen beschikbaar als u *Periode* selecteert in het veld **Methode**.</p><p>U selecteert bijvoorbeeld *Periode* in het veld **Methode**, voert *1* in het veld **Per** in en selecteert *Maanden* in het veld **Eenheid**. Geef vervolgens in het veld **Einde** een einddatum op die één jaar in de toekomst ligt. In dit geval wordt er wordt één prognoseregel gemaakt voor elke maand van het komende jaar op basis van het artikel en de hoeveelheid die worden opgegeven in de kopregel. |
    | Eenheid | Selecteer de eenheid van het tijdsinterval: *Dagen*, *Maanden* of *Jaren*. De toewijzing komt dan overeen met het aantal dagen, maanden of jaren dat u opgeeft in het veld **Per**.|
    | Periodesleutel | Geef de periodetoewijzingssleutel op die wordt gebruikt om de prognose toe te wijzen. Zie [Gegevenstoewijzing voor budgetplanning](../../finance/budgeting/budget-planning-data-allocation.md) voor meer informatie. |
    | Einde | Geef de einddatum op die van toepassing is op uw instellingen in de velden **Per** en **Eenheid**. |

1. Klik op **OK** om uw instellingen te bevestigen.
1. U kunt de resultaten bekijken op het tabblad **Toewijzing** voor dezelfde regel.

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Prognosetransacties groepsgewijs bijwerken

Met deze procedure kunt u bestaande prognosetransactieregels verwerken. U kunt prognosetransactieregels kopiëren, bewerken en verwijderen.

1. Selecteer **Groepsgewijs bijwerken** op de pagina voor aanbod- of vraagprognoseregels.
1. Selecteer **Filteren** in het dialoogvenster.
1. Selecteer op het tabblad **Bereik** de criteria voor de bronprognosegegevens die u wilt kopiëren, bewerken of verwijderen. Deze gegevens kunnen het prognosemodel, het artikelnummer en de klantrekening omvatten.
1. Klik op **OK** om uw selectie te bevestigen.

    Nadat de gegevens zijn geselecteerd, kunt u het dialoogvenster **Prognosetransacties bewerken** gebruiken om te definiëren hoe u de gegevens wilt kopiëren, bewerken of verwijderen.

    > [!NOTE]
    > De filterstap is een vereiste voor het gebruik van de functie **Groepsgewijs bijwerken**. Als u de stap overslaat, worden **alle** prognoseregels geselecteerd en bijgewerkt. Hierdoor kunt u per ongeluk dubbele transacties of verwijdering van transacties veroorzaken.

1. Geef in de sectie **Beheer** aan of u de geselecteerde prognosetransacties wilt kopiëren, bijwerken of verwijderen.
1. Gebruik de sectie **Wijzigingen in veld** om de parameters van de prognose te wijzigen. Schakel het selectievakje van de parameter in en selecteer een van de beschikbare opties. Schakel bijvoorbeeld het selectievakje **Model** in en selecteer vervolgens een prognosemodelnummer. Bestaande prognoseregels worden naar het geselecteerde prognosemodel gekopieerd.
1. Gebruik de sectie **Wijziging van periode** om de begin- en einddatums van de prognose naar voren of naar achteren te verplaatsen. Schakel het selectievakje in en gebruik vervolgens de hoeveelheids- en periodevelden om te bepalen hoe de prognosedatums moeten worden verplaatst. U kunt een negatieve hoeveelheid invoeren om de begindatum naar voren te verplaatsen (eerder dus).

    Als u bijvoorbeeld de begindatum van de prognosetransactie wilt uitstellen met zes maanden, schakelt u het selectievakje in, voert u *6* in als de hoeveelheid en selecteert u *Maanden* als periode.

1. Gebruik het veld **Veld corrigeren** om de werkelijke prognosegegevens bij te werken. Selecteer in het veld **Veld** het criterium dat u wilt wijzigen. Voer in het veld **Factor** een vermenigvuldigingsfactor in die u op het geselecteerde criterium wilt toepassen of voer een constante voor optellen of aftrekken in. Selecteer bijvoorbeeld *Hoeveelheid* als criterium en voer een factor van *1,5* in om de artikelhoeveelheid met 1,5 te vermenigvuldigen. U kunt ook een constante van *-25* invoeren om de artikelhoeveelheid met 25 eenheden te verlagen.
1. Gebruik de sectie **Financiële dimensies** om de financiële dimensies van prognoseregels bij te werken. Selecteer de financiële dimensies die u wilt wijzigen en voer vervolgens een waarde in die moet worden toegepast op de geselecteerde dimensies.
1. Selecteer **OK** om de wijzigingen toe te passen.

## <a name="use-forecasts-with-master-planning"></a>Prognoses met hoofdplanning gebruiken

Nadat u de vraagprognose en/of aanbodprognose hebt uitgevoerd, kunt u de prognoses opnemen tijdens de hoofdplanning om rekening te houden met verwachte vraag en/of aanbod in de hoofdplanningsuitvoering. Wanneer prognoses worden opgenomen in de hoofdplanning, worden de brutobehoeften voor materialen en capaciteit berekend en worden geplande orders gegenereerd.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Een hoofdplan instellen om een voorraadprognose op te nemen

Voer de volgende stappen uit om een hoofdplan zo in te stellen dat het een voorraadprognose bevat.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een bestaand plan of maak een nieuw plan.
1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Prognosemodel**: selecteer het prognosemodel dat moet worden toegepast. Dit model kan worden gebruikt wanneer een aanbodvoorstel wordt gegenereerd voor het huidige hoofdplan.
    - **Aanbodprognose opnemen**: stel deze optie in op *Ja* om de aanbodprognose in het huidige prognoseplan op te nemen. Bij *Nee* worden aanbodprognosetransacties niet opgenomen in het hoofdplan.
    - **Vraagprognose opnemen**: stel deze optie in op *Ja* om de vraagprognose in het huidige prognoseplan op te nemen. Bij *Nee* worden vraagprognosetransacties niet opgenomen in het hoofdplan.
    - **Gebruikte methode om prognosebehoeften te verminderen**: selecteer de methode die moet worden gebruikt om prognosebehoeften te verminderen. Zie [Reductiesleutels van prognose](planning-optimization/demand-forecast.md#reduction-keys) voor meer informatie.

1. Op het sneltabblad **Time fences in dagen** kunt u de volgende velden instellen om de periode op te geven waarin de prognose moet worden opgenomen:

    - **Prognoseplan**: stel deze optie in op *Ja* als u de time fence voor prognoseplannen wilt overschrijven die afkomstig is uit de afzonderlijke behoefteplanningsgroepen. Stel deze optie in op *Nee* als u de waarden uit de afzonderlijke behoefteplanningsgroepen voor het huidige hoofdplan wilt gebruiken.
    - **Prognoseperiode**: als u de optie **Prognoseplan** instelt op *Ja*, geeft u het aantal dagen op (vanaf de datum van vandaag) waarop de vraagprognose moet worden toegepast.

    > [!IMPORTANT]
    > De optie **Prognoseplan** wordt nog niet ondersteund met Planningsoptimalisatie.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Een hoofdplan uitvoeren dat een voorraadprognose bevat

Voer de volgende stappen uit om een hoofdplan uit te voeren dat een voorraadprognose bevat.

1. Ga naar **Hoofdplanning \> Werkgebieden \> Hoofdplanning**.
1. Typ of selecteer in het veld **Hoofdplan** het hoofdplan dat u in de vorige procedure hebt ingesteld.
1. Selecteer de tegel **Hoofdplanning** en selecteer **Uitvoeren**.
1. Stel in het dialoogvenster **Hoofdplanning** de optie **Verwerkingstijd traceren** in op *Ja*.
1. Voer een getal in het veld **Aantal threads** in.
1. Selecteer **Filter** op het sneltabblad **Op te nemen records**.
1. Er wordt een standaarddialoogvenster voor Query-editor weergegeven. Selecteer in het tabblad **Bereik** de rij waarin het veld **Veld** is ingesteld op *Artikelnummer*.
1. Selecteer in het veld **Criteria** het artikelnummer dat u in het plan wilt opnemen.
1. Selecteer **OK**.

Open de pagina **Brutobehoefte** om de berekende behoeften weer te geven. Selecteer bijvoorbeeld **Brutobehoefte** op de pagina **Vrijgegeven producten** in het actievenster op het tabblad **Plan** in de groep **Behoeften**.

Als u de geplande orders wilt weergeven die zijn gegenereerd, gaat u naar **Hoofdplanning \> Algemeen \> Geplande orders** en selecteert u het juiste prognoseplan.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Vraagprognose](introduction-demand-forecasting.md)
- [Instelling van Vraagprognose](demand-forecasting-setup.md)
- [Een statistische basislijnprognose genereren](generate-statistical-baseline-forecast.md)
- [Handmatige correcties aanbrengen in de basislijnprognose](manual-adjustments-baseline-forecast.md)
- [Hoofdplanning met vraagprognoses](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
