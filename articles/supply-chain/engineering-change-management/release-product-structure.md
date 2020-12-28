---
title: Productstructuren van de vrijgave
description: In dit onderwerp wordt beschreven hoe u volledige productstructuren kunt vrijgeven naast het vrijgeven van producten in combinatie met hun technische versies. Op deze manier kunt u ervoor zorgen dat productgegevens die technisch relevant zijn gemakkelijk kunnen worden hergebruikt in verschillende rechtspersonen.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 68f091cca9c3c2baa03813553127ee41abe6d522
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425898"
---
# <a name="release-product-structures"></a>Productstructuren van de vrijgave

[!include [banner](../includes/banner.md)]

Om ervoor te zorgen dat productgegevens die technisch relevant zijn in verschillende rechtspersonen kunnen worden hergebruikt, kunt u naast het vrijgeven van producten met hun technische versies volledige productstructuren vrijgeven. Daarom kunt u stuklijststructuren met meerdere niveaus samen met het bovenliggende item in één vrijgaveactie vrijgeven. In dit geval worden de stuklijst en de producten op een lager niveau ook vrijgegeven.

Technische producten worden op zodanige wijze gemaakt en onderhouden door hun technische bedrijf dat ze voldoen aan de kwaliteitsvereisten als ze worden ontworpen. Elk operationeel bedrijf dat een product fabriceert, heeft hetzelfde product en een onderliggende stuklijst nodig. Afhankelijk van de productiefaciliteit kan de route lokaal worden gemaakt. In dat geval geeft u een route niet samen met het product vrij. Voor rechtspersonen die de producten verkopen maar niet produceren, is de stuklijst mogelijk niet vereist.

Om het proces efficiënter te laten uitvoeren, kunnen alle relevante technische gegevens op hetzelfde moment worden vrijgegeven aan andere operationele bedrijven. Deze gegevens bevatten de productstructuur. Tijdens het vrijgaveproces kunt u kiezen welk deel van de productgegevens moet worden vrijgegeven.

Zie [Technische bedrijven en regels voor gegevenseigendom](engineering-org-data-ownership-rules.md) voor meer informatie over technische bedrijven en operationele bedrijven.

U kunt zowel standaardproducten als technische producten tegelijk met de productstructuur van de vrijgave vrijgeven. Tijdens dit proces wordt de gehele productstructuur vrijgegeven, zelfs de stuklijst en route van het bedrijf waarin de producten worden vrijgegeven.

Zie [Een technisch product aan een lokaal bedrijf vrijgeven](engineering-scenarios.md#release) voor een voorbeeld van het vrijgeven van een product

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Vrijgegeven gegevens voor een product wanneer de productstructuur van de vrijgave wordt gebruikt

De volgende gegevens zijn opgenomen in de vrijgave van technische producten:

- **Productgegevens**: er wordt een nieuw vrijgegeven product gemaakt.
- **Technische versiegegevens**: de technische versie en de bijbehorende gegevens worden gemaakt of bijgewerkt. Houd er rekening mee dat de technische gegevens worden overschreven als u dezelfde technische versie weer aan een operationeel bedrijf vrijgeeft.
- **Technische kenmerken**: de technische kenmerken en de bijbehorende waarden worden gemaakt of bijgewerkt.
- **Technische stuklijst**: de technische stuklijst en de bijbehorende regels kunnen worden gemaakt of bijgewerkt. Zie [Producteigenaren](product-owner.md) voor meer informatie over het eigendom van gegevens.
- **Technische routes**: de technische routes en de bijbehorende bewerkingen kunnen worden gemaakt of bijgewerkt. Zie [Producteigenaren](product-owner.md) voor meer informatie over het eigendom van gegevens.
- **Technische documenten**: de technische documenten die zijn gekoppeld aan de technische versie worden gemaakt of bijgewerkt.

Wanneer u Technisch wijzigingsbeheer op uw systeem inschakelt, is de productstructuur van de vrijgave beschikbaar. Bovendien bevatten standaardproducten hun stuklijsten en routes wanneer ze worden vrijgegeven.

## <a name="product-acceptance"></a>Productacceptatie

**Acceptatie van producten** is een belangrijke parameter die van invloed is op het vrijgaveproces. U kunt deze parameter voor elk bedrijf instellen door te gaan naar **Technisch wijzigingsbeheer \> Instellingen \> Parameters voor technisch wijzigingsbeheer**. Zie [Parameters voor technisch wijzigingsbeheer](engineering-parameters.md) voor meer informatie.

### <a name="automatic-product-acceptance"></a>Automatische productacceptatie

Elke vrijgave van technische producten begint wanneer iemand van het technische bedrijf een product selecteert om vrij te geven. Wanneer de parameter **Productacceptatie** is ingesteld op *Automatisch*, bepaalt de gebruiker bij het technische bedrijf welke productgegevens automatisch aan de operationele bedrijven moeten worden vrijgegeven. Het product wordt vervolgens automatisch vrijgegeven aan de bedrijven die zijn geselecteerd in de vrijgavewizard.

### <a name="manual-product-acceptance"></a>Handmatige productacceptatie

Elke vrijgave van technische producten begint wanneer iemand van het technische bedrijf een product selecteert om vrij te geven. Wanneer de parameter **Productacceptatie** is ingesteld op *Handmatig*, bepaalt de gebruiker bij het technische bedrijf welke productgegevens aan de operationele bedrijven moeten worden vrijgegeven. Een gebruiker van elk operationeel bedrijf controleert vervolgens de productgegevens en besluit of de vrijgave moet worden geaccepteerd. De gebruiker bij het operationele bedrijf kan de volgende opties instellen bij het ontvangen van de gegevens:

- Als de producten (updates) niet relevant zijn voor het operationele bedrijf, kan de gebruiker ervoor kiezen de vrijgave niet te accepteren.
- De gebruiker kan de artikelsjabloon voor nieuwe producten wijzigen.
- De gebruiker kan kiezen of het product samen met hun bijbehorende stuklijsten en/of routes moet worden vrijgegeven en of deze moeten worden vrijgegeven als goedgekeurd en actief.
- De gebruiker kan de ingangdatums van de producten wijzigen.

Zie [Het product bekijken en accepteren voordat u het in het lokale bedrijf vrijgeeft](engineering-scenarios.md#accept) voor een voorbeeld van het accepteren van een product.

> [!NOTE]
> Voor standaardproducten kunt u uit elke rechtspersoon aan andere rechtspersoon vrijgeven. Voor technische producten is de enige rechtspersoon waaruit u kunt vrijgeven het technisch bedrijf.

## <a name="release-policies"></a>Vrijgavebeleid

Niet alle operationele bedrijven hebben dezelfde productgegevens nodig. In het algemeen is voor operationele bedrijven die technische producten produceren een stuklijst nodig, terwijl voor operationele bedrijven die alleen technische producten verkopen geen stuklijst nodig is. U kunt het vrijgavebeleid gebruiken om de parameters op te geven die worden gebruikt voor de vrijgave van producten.

Voor technische producten wordt het vrijgavebeleid toegewezen in de categorie technische producten en is het veld verplicht. Voor standaardproducten wordt het beleid toegewezen aan het gedeelde product en is het veld optioneel.

Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie over categorieën voor technische producten.

Tijdens het vrijgaveproces kunt u de instellingen beïnvloeden.

## <a name="create-and-manage-product-release-policies"></a>Vrijgavebeleid voor producten maken en beheren

Als u wilt werken met de beleid voor productvrijgave, gaat u naar **Technisch wijzigingsbeheer \> Instellingen \> Vrijgavebeleid voor producten**. Voer vervolgens een van deze stappen uit.

- Als u een nieuw beleid wilt maken, selecteert u **Nieuw** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaand beleid wilt bewerken, selecteert u deze in het lijstvenster, selecteert u **Bewerken** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaand beleid wilt verwijderen, selecteert u het in het lijstvenster, selecteert u **Bewerken** in het actievenster en controleert u op het sneltabblad **Algemeen** of de optie **Actief** is ingesteld op *Nee*. Selecteer vervolgens in het actievenster **Verwijderen**.

### <a name="header"></a>Koptekst

Stel de volgende velden in de koptekst van een beleid voor productvrijgave in.

| Veld | Beschrijving |
|---|---|
| Naam | Voer een naam voor het beleid in. |
| Beschrijving | Voer een omschrijving van het beleid in. |

### <a name="general-fasttab"></a>Het sneltabblad Algemeen

Stel de volgende velden in het sneltabblad **Algemeen** van een beleid voor productvrijgave in.

| Veld | Beschrijving |
|---|---|
| Producttype | Selecteer of het beleid van toepassing is op producten van het type *Artikel* of *Service*. U kunt deze instelling niet wijzigen nadat u de record hebt opgeslagen. |
| Sjablonen toepassen | Selecteer een van de volgende opties om op te geven of en hoe productvrijgavesjablonen moeten worden toegepast wanneer het beleid wordt gebruikt:<ul><li>**Altijd**: een product met vrijgavesjabloon moet altijd worden gebruikt voor vrijgaven. Als u deze optie selecteert, gebruikt u het sneltabblad **Alle producten** om de sjabloon op te geven die wordt gebruikt voor elk bedrijf waaraan u wilt vrijgeven. Als u geen sjabloon opgeeft voor elk bedrijf dat op het sneltabblad **Alle producten** wordt vermeld, wordt een foutbericht weergegeven wanneer u het beleid probeert op te slaan.</li><li>**Optioneel**: als een product met vrijgavesjabloon is opgegeven voor een bedrijf dat wordt vermeld op het sneltabblad **Alle producten** wordt die sjabloon gebruikt wanneer u vrijgeeft aan dat bedrijf. Anders wordt er geen sjabloon gebruikt. Als u deze optie selecteert, kunt u het beleid opslaan zonder sjablonen toe te wijzen aan alle bedrijven. (Er wordt geen waarschuwing weergegeven.)</li><li>**Nooit**: er wordt geen product met vrijgavesjabloon gebruikt voor bedrijven waaraan u vrijgeeft, zelfs als een sjabloon is opgegeven voor bedrijven die worden vermeld op het sneltabblad **Alle producten**. De sjabloonkolommen zijn niet beschikbaar.</li></ul> |
| Actief | Gebruik deze optie om uw vrijgavebeleid te beheren. Stel deze in op *Ja* voor elk vrijgavebeleid dat u gebruikt. Stel deze in op *Nee* als u een vrijgavebeleid wilt markeren als inactief wanneer het niet wordt gebruikt. U kunt een vrijgavebeleid dat is toegewezen aan een technische productcategorie niet deactiveren en u kunt alleen inactief vrijgavebeleid verwijderen. |

### <a name="all-products-fasttab"></a>Het sneltabblad Alle producten

Voeg op het sneltabblad **Alle producten** een rij toe voor elk operationeel bedrijf waarvoor u dit beleid wilt gebruiken voor vrijgave. Gebruik de knoppen op het sneltabblad **Alle producten** om naar behoefte rijen toe te voegen en te verwijderen. Stel de volgende velden in voor elke rij die u toevoegt.

> [!NOTE]
> De instellingen op het sneltabblad **Alle producten** zijn van toepassing op zowel technische producten als standaardproducten.

| Veld | Beschrijving |
|---|---|
| Bedrijfsrekening-ID | Selecteer het bedrijf waarop de rij van toepassing is. De parameters in de rij zijn van toepassing wanneer producten aan dit bedrijf worden vrijgegeven. |
| Sjabloon vrijgegeven product | Voer een sjabloon in voor het product. |
| Stuklijstgoedkeuring kopiëren | Schakel dit selectievakje in om de goedkeuringsstatus van de stuklijst naar het ontvangende bedrijf te kopiëren. |
| Stuklijstactivering kopiëren | Schakel dit selectievakje in om de activeringsstatus van de stuklijst naar het ontvangende bedrijf te kopiëren. |
| Routegoedkeuring kopiëren | Schakel dit selectievakje in om de goedkeuringsstatus van de route naar het ontvangende bedrijf te kopiëren.|
| Routeactivering kopiëren | Schakel dit selectievakje in om de activeringsstatus van de route naar het ontvangende bedrijf te kopiëren. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Het sneltabblad Optieparameters voor technische producten

Elke keer dat u een rij toevoegt op het sneltabblad **Alle producten**, wordt ook een rij met een overeenkomende waarde **Bedrijfsrekeningen** gemaakt op het sneltabblad **Optieparameters voor technische producten**. Als u vervolgens een rij verwijdert uit het sneltabblad **Alle producten**, wordt ook de rij met de overeenkomende waarde **Bedrijfsrekeningen** verwijderd uit het sneltabblad **Optieparameters voor technische producten**.

Stel de volgende velden in voor elke rij die wordt weergegeven op het sneltabblad **Optieparameters voor technische producten**.

> [!NOTE]
> De instellingen in het sneltabblad **Optieparameters voor technische producten** zijn alleen van toepassing op technische producten.

| Veld | Beschrijving |
|---|---|
| Sjabloon Stuklijst | Wanneer een product met een stuklijst wordt vrijgegeven, worden de regels van de opgegeven sjabloonstuklijst toegevoegd. Dit veld is handig voor het toevoegen van lokale onderdelen, zoals verpakking of instructies in de lokale taal. |
| Sjabloonroute | Wanneer een product met een route wordt vrijgegeven, worden de regels van de opgegeven sjabloon toegevoegd. |
| Geldigheid kopiëren | Selecteer of geldigheidsdatums moeten worden gekopieerd van het technische bedrijf naar het operationele bedrijf wanneer u producten vrijgeeft. |
| Automatisch toevoegen aan het releasevoorstel | Schakel dit selectievakje in voor producten die automatisch moeten worden vrijgegeven via de order voor technische wijzigingen. Op deze manier kunnen producten die behoren tot categorieën van technische producten die dit vrijgavebeleid gebruiken automatisch worden vrijgegeven aan operationele bedrijven waar deze optie is ingesteld. (Zie [Wijzigingen in technische producten beheren](engineering-change-management.md) voor meer informatie.)

### <a name="review-each-product-when-you-release-it"></a>Elk product beoordelen wanneer u het vrijgeeft

Wanneer technische producten met stuklijsten of routes worden vrijgegeven, worden de parameters ingesteld op standaardwaarden, zoals is aangegeven in het vrijgavebeleid. Als gebruiker kunt u dit gedrag aan de vrijgevende kant beïnvloeden wanneer u de productstructuur van de vrijgave gebruikt.

Voor het vrijgeven van technische producten selecteert u op de pagina **Vrijgegeven producten** de producten die u wilt vrijgeven en vervolgens selecteert u **Productstructuur voor vrijgave** om de vrijgavewizard te openen. Op de pagina **Technische producten selecteren voor vrijgave** worden de producten weergegeven. Selecteer een enkel product en selecteer vervolgens **Vrijgavedetails** om de vrijgavegegevens voor het product te controleren.

Op de pagina **Vrijgavedetails** kunt u de waarden wijzigen van de velden **Stuklijst ontvangen**, **Goedkeuring van stuklijst kopiëren**, **Activering van stuklijst kopiëren**, **Stuklijst ontvangen**, **Goedkeuring van route kopiëren** en **Activering van route kopiëren**. In het push-pullscenario kunt u de waarde van dezelfde velden aan de ontvangstzijde wijzigen, mits de stuklijst en de route worden vrijgegeven.

## <a name="product-owners-and-product-releases"></a>Producteigenaars en productvrijgaves

Aangezien de producteigenaren weten welke rechtspersonen hun producten nodig hebben, kan een product alleen worden vrijgegeven door de leden van de groep eigenaren van dat product. Andere gebruikers kunnen geen producten vrijgeven waarvan ze geen eigenaar zijn.

Dit gedrag is alleen van toepassing wanneer een product rechtstreeks voor vrijgave is geselecteerd. Producten die deel uitmaken van de structuur van een ander product via een stuklijst *kunnen* worden vrijgegeven door gebruikers die geen eigenaar zijn wanneer ze het bovenliggende product vrijgeven. Ze moeten dan wel eigenaar zijn van het bovenliggende product.

Product X wordt bijvoorbeeld toegewezen aan de producteigenaarsgroep *Designkasten*. Product X maakt ook deel uit van de stuklijst van product Y, dat is toegewezen aan de producteigenaarsgroep *Design luidsprekers*. Als een gebruiker in de producteigenaarsgroep *Design luidsprekers* product Y en de bijbehorende stuklijst vrijgeeft, wordt product X samen met product Y vrijgegeven.

Zie voor meer informatie [Producteigenaren](product-owner.md).
