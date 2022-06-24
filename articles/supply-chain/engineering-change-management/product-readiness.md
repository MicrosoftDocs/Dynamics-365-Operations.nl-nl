---
title: Productgereedheid
description: In dit artikel wordt beschreven hoe u de gereedheidscontroles kunt gebruiken om ervoor te zorgen dat de vereiste hoofdgegevens voor een product zijn voltooid voordat deze in transacties worden gebruikt.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a8e76d5fc786b6f4cac7cd0430399ca3ad13a7bc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856217"
---
# <a name="product-readiness"></a>Productgereedheid

[!include [banner](../includes/banner.md)]

U kunt de gereedheidscontroles gebruiken om beter te waarborgen dat alle vereiste hoofdgegevens voor een product zijn gespecificeerd voordat deze in transacties worden gebruikt. Wanneer de gereedheidscontroles worden gebruikt, wordt de gebruiker of het team verantwoordelijk gemaakt voor het valideren van specifieke, vooraf gedefinieerde, productgerelateerde gegevens.

U kunt het selectievakje **Actief** inschakelen voor een technisch product, een variant of een versie nadat alle vereiste gegevens zijn ingevoerd en geverifieerd, en nadat alle gereedheidscontroles zijn verwerkt. Als een of meer controles niet zijn verwerkt voor het product, de versie of variant, verschijnt er een waarschuwing dat niet alle controles zijn uitgevoerd wanneer u het selectievakje **Actief** probeert te markeren.

U kunt gereedheidscontroles maken voor nieuwe engineeringproducten, varianten en versies. U kunt ook gereedheidscontroles toepassen op standaardproducten (niet-engineering) (zie ook [Gereedheidscontroles op standaardproducten](#standard-products)). 

U kunt standaardproducten in transacties gebruiken, ook als niet alle controles op gereedheid zijn voltooid. Als u een product moet blokkeren om te voorkomen dat het in transacties wordt gebruikt, gebruikt u de levenscyclusstatus. U kunt een levenscyclusstatus toewijzen die blokkeert dat een product wordt gebruikt in transacties, en vervolgens, nadat alle controles op gereedheid zijn voltooid, kunt u een nieuwe levenscyclusstatus toewijzen die de vereiste transacties toestaat.

## <a name="types-of-readiness-checks"></a>Typen gereedheidscontroles

Er zijn drie typen gereedheidscontroles:

- **Systeem controle**: het systeem controleert of er een geldig record is. De record kan bijvoorbeeld een actieve stuklijst zijn.
- **Handmatige controle**: een gebruiker verifieert of de record geldig is. Een gereedheidscontrole kan bijvoorbeeld een validatie van de standaard orderinstellingen vereisen. In sommige gevallen, bijvoorbeeld wanneer het product nog steeds wordt ontworpen en niet in de voorraad wordt geplaatst, zijn er geen standaard orderinstellingen vereist. Er zijn echter mogelijk standaard orderinstellingen vereist voor een ander product van hetzelfde type, omdat het product in de voorraad kan worden gehouden. De gebruiker is verantwoordelijk voor het goed beslissen of een gereedheidscontrole is vereist.
- **Controlelijst**: de gebruiker beantwoordt een reeks vragen vanuit een controlelijst en het systeem bepaalt of de antwoorden aan de verwachtingen voldoen. De controlelijst kan elk onderwerp omvatten. Het kan bijvoorbeeld worden gebruikt om te bepalen of marketingmateriaal of productdocumentatie is voltooid.

<a name="checks-engineering"></a>

## <a name="how-readiness-checks-are-created-for-a-new-engineering-product-variant-or-version"></a>Hoe gereedheidscontroles worden gemaakt voor een nieuw technisch product, een nieuwe variant of een nieuwe versie

Het beleid voor gereedheidscontroles kan worden toegepast op het niveau van het vrijgegeven product, het niveau van de vrijgegeven variant en het niveau van de technische versie.

Wanneer u een nieuw *technisch product* maakt, bepaalt het systeem of er een [gereedheidscontrolebeleid op van toepassing is](#assign-policy). Als een gereedheidscontrolebeleid van toepassing is, treden de volgende gebeurtenissen op:

- Gereedheidscontroles worden gemaakt voor het product op basis van het toepasselijke beleid.
- De technische versie wordt ingesteld op inactief om te voorkomen dat het product wordt gebruikt. Alle technische versies voor het product zijn ingesteld op inactief.

Als voor een product een nieuwe *variant* wordt gemaakt, controleert het systeem of er een gereedheidscontrolebeleid op van toepassing is. (Gereedheidscontroles kunnen worden toegepast op het niveau van de vrijgegeven variant en het niveau van de technische versie.) Als er een gereedheidscontrole van toepassing is vinden de volgende gebeurtenissen plaats:

- Gereedheidscontroles worden gemaakt voor het product op basis van het toepasselijke beleid.
- De technische versie en variant worden ingesteld op inactief om te voorkomen dat het product wordt gebruikt.

Als voor een product een nieuwe technische *versie* wordt gemaakt, controleert het systeem of er een gereedheidscontrolebeleid op van toepassing is. (Gereedheidscontroles kunnen worden toegepast op het niveau van de technische versie.) Als er een beleid van toepassing is, vinden de volgende gebeurtenissen plaats:

- Gereedheidscontroles worden gemaakt voor het product op basis van het toepasselijke beleid.
- De technische versie wordt ingesteld op inactief om te voorkomen dat het product wordt gebruikt.

> [!NOTE]
> U kunt gereedheidscontrolebeleid ook instellen voor standaardproducten (niet-technisch). Zie het gedeelte [Gereedheidscontroles op standaardproducten](#standard-products) verderop dit artikel voor meer informatie.

## <a name="view-readiness-checks"></a>Gereedheidscontroles weergeven

### <a name="view-open-readiness-checks-for-a-product-or-product-version"></a>Openstaande gereedheidscontroles voor een product of productversie weergeven

Als u de openstaande gereedheidscontroles voor een product wilt zoeken, opent u de pagina **Details van vrijgegeven producten**. Selecteer vervolgens in het Actievenster het tabblad **Product** in de groep **Gereedheidscontroles** en selecteer **Gereedheidscontroles**.

Als u de openstaande gereedheidscontroles voor een productversie wilt zoeken, opent u de pagina **Technische versies** voor een vrijgegeven product en kiest u een versie. Selecteer vervolgens in het Actievenster het tabblad **Product** in de groep **Controlelijst** en selecteer **Gereedheidscontroles**.

### <a name="view-open-readiness-checks-that-are-assigned-to-you"></a>Openstaande gereedheidscontroles weergeven die aan u zijn toegewezen

Voer een van de volgende stappen uit om de openstaande gereedheidscontroles weer te geven die aan u zijn toegewezen.

- Ga naar **Beheer van technische wijzigingen \> Algemeen \> Productgereedheid \> Mijn openstaande gereedheidscontroles**.
- Ga naar **Productinformatiebeheer \> Werkruimten \> Productgereedheid voor afzonderlijke productie**.

De instellingen waarmee wordt opgegeven aan wie de gereedheidscontrole wordt toegewezen, worden bepaald voor het gereedheidsbeleid. Gereedheidscontroles kunnen worden toegewezen aan een persoon of een team. Als een gereedheidscontrole is toegewezen aan een team, is er één persoon in het team die de gereedheidscontrole moet verwerken.

## <a name="process-open-readiness-checks"></a>Openstaande gereedheidscontroles verwerken

### <a name="process-system-and-manual-readiness-checks"></a>Systeemgereedheidscontroles en handmatige gereedheidscontroles verwerken

Nadat u de pagina **Gereedheidscontroles** hebt geopend, kunt u het onderwerp van de systeemgereedheidscontroles en handmatige gereedheidscontroles weergeven door **Verwante informatie weergeven** te selecteren in het actievenster. Vervolgens kunt u de gegevens voor de gereedheidscontrole voltooien en/of valideren. Openstaande gereedheidscontroles hebben de waarde *In behandeling* voor **Status**. Deze status geeft aan dat de gereedheidscontrole nog moet worden verwerkt. Als u een gereedheidscontrole wilt verwerken, volgt u een van de volgende stappen.

- Selecteer **Controleren/voltooien** in het actievenster om de gereedheidscontrole te beoordelen en te voltooien. Wanneer u klaar bent, wordt het veld **Status** bijgewerkt naar *Geslaagd*.
- Selecteer de optie **Overslaan** in het actievenster als u een niet verplichte gereedheidscontrole wilt overslaan. U kunt bijvoorbeeld een gereedheidscontrole voor prijsberekeningen instellen. U besluit deze controle echter over te slaan terwijl het product zich nog in de ontwerpfase bevindt. In dit geval wordt het veld **Status** bijgewerkt naar *Overgeslagen*.

Afhankelijk van de configuratie van het gereedheidsbeleid, kan een extra stap nodig zijn om de gereedheidscontrole goed te keuren wanneer het veld **Status** van een gereedheidscontrole is bijgewerkt naar *Geslaagd*. Selecteer in dit geval **Goedkeuring** om de gereedheidscontrole te voltooien. Deze goedkeuringsstap is altijd verplicht wanneer de gereedheidscontrole wordt overgeslagen.

Wanneer alle openstaande gereedheidscontroles voor een nieuw product, een nieuwe variant of een nieuwe versie zijn verwerkt en goedgekeurd, wordt het artikel automatisch actief en is het dus klaar voor gebruik.

### <a name="process-checklist-readiness-checks"></a>Controlelijst met gereedheidscontroles verwerken

Als u een controlelijst wilt openen, opent u de pagina **Gereedheidscontroles** en selecteert u in het actievenster de optie **Controlelijst starten**. Wanneer u de controlelijst hebt voltooid, controleert het systeem of de gereedheidscontrole is geslaagd op basis van de instellingen in de vragenlijst. Als de controle slaagt, wordt het veld **Status** bijgewerkt naar *Geslaagd*. Als de gereedheidscontrole niet verplicht is, kunt u deze overslaan. In dit geval wordt het veld **Status** bijgewerkt naar *Overgeslagen*.

Afhankelijk van de configuratie van het gereedheidsbeleid, kan een extra stap nodig zijn om de gereedheidscontrole goed te keuren wanneer het veld **Status** van een gereedheidscontrole is bijgewerkt naar *Geslaagd*. Selecteer in dit geval **Goedkeuring** om de gereedheidscontrole te voltooien. Deze goedkeuringsstap is altijd verplicht wanneer de gereedheidscontrole wordt overgeslagen.

Wanneer alle openstaande gereedheidscontroles voor een nieuw product, een nieuwe variant of een nieuwe versie zijn verwerkt en goedgekeurd, wordt het artikel automatisch actief en is het dus klaar voor gebruik.

## <a name="create-and-manage-product-readiness-policies"></a>Gereedheidsbeleid voor producten maken en beheren

Gebruik het productgereedheidsbeleid om de gereedheidscontroles te beheren die van toepassing zijn op een product. Elk gereedheidsbeleid bevat een set gereedheidscontroles. Wanneer een gereedheidsbeleid wordt toegewezen aan een technische productcategorie of een gedeeld product, hebben alle producten die zijn gerelateerd aan die categorie of dat gedeelde product de gereedheidscontroles die in het gereedheidsbeleid zijn opgenomen.

Als u wilt werken met de productgereedheidsbeleid, gaat u naar **Beheer van technische wijzigingen \> Instellingen \> Productgereedheidsbeleid**. Voer vervolgens een van deze stappen uit.

- Als u een nieuw beleid wilt maken, selecteert u **Nieuw** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaand beleid wilt bewerken, selecteert u deze in het lijstvenster, selecteert u **Bewerken** in het actievenster en stelt u de velden in op de wijze die wordt beschreven in de volgende subsecties.
- Als u een bestaand beleid wilt verwijderen, selecteert u het in het lijstvenster, selecteert u **Bewerken** in het actievenster en controleert u op het sneltabblad **Algemeen** of de optie **Actief** is ingesteld op *Nee*. Selecteer vervolgens in het actievenster **Verwijderen**.

### <a name="header"></a>Koptekst

Stel de volgende velden in de koptekst van een productgereedheidsbeleid in.

| Veld | Beschrijving |
|---|---|
| Naam | Voer een naam voor het beleid in. |
| Beschrijving | Voer een omschrijving van het beleid in. |

### <a name="general-fasttab"></a>Het sneltabblad Algemeen

Stel de volgende velden in het sneltabblad **Algemeen** van een productgereedheidsbeleid in.

| Veld | Beschrijving |
|---|---|
| Producttype | Selecteer of het beleid van toepassing is op producten van het type *Artikel* of *Service*. U kunt deze instelling niet wijzigen nadat u de record hebt opgeslagen. |
| Actief | Gebruik deze optie om uw gereedheidsbeleid te beheren. Stel deze in op *Ja* voor elk gereedheidsbeleid dat u gebruikt. Stel deze in op *Nee* als u een gereedheidsbeleid wilt markeren als inactief wanneer het niet wordt gebruikt. U kunt een gereedheidsbeleid dat is toegewezen aan een technische productcategorie of een gedeeld product niet deactiveren en u kunt alleen inactief vrijgavebeleid verwijderen. |

### <a name="readiness-control-fasttab"></a>Het sneltabblad Gereedheidsbeheer

Voeg voor elke type gereedheidscontrole die u in het beleid wilt opnemen een rij toe op het sneltabblad **Gereedheidsbeheer**. Gebruik de volgende knoppen op de werkbalk met sneltabbladen om naar behoefte rijen toe te voegen en te verwijderen:

- **Controle toevoegen**: een standaard gereedheidscontrole toevoegen aan het beleid. Wanneer u deze knop selecteert, wordt het dialoogvenster **Controle toevoegen** weergegeven. Hier kunt u kiezen uit een lijst met beschikbare controles.
- **Bestaande vragenlijst toevoegen**: een lege rij toevoegen aan het raster. U kunt vervolgens een bestaande vragenlijst toewijzen door de velden in de volgende tabel in te stellen.
- **Kopiëren**: een kopie van de geselecteerde rij toevoegen aan het raster.
- **Verwijderen**: de geselecteerde rij uit het raster verwijderen.

Stel de volgende velden in voor elke rij die u toevoegt.

| Veld | Beschrijving |
| --- | --- |
| Procesgebied | Selecteer het gebied waarop de controle betrekking heeft. |
| Type | Selecteer of de controle een systeemcontrole, handmatige controle of een controlelijst (vragenlijst) is. |
| Naam | Als de controle een controlelijst is, voert u een naam in. Voor systeemcontroles en handmatige controles wordt dit veld automatisch ingesteld. |
| Beschrijving | Als de controle een controlelijst is, voert u een omschrijving in. Voor systeemcontroles en handmatige controles wordt dit veld automatisch ingesteld en geeft de omschrijving de focus van de controle. |
| Controles toepassen op | Selecteer of in de rij gereedheidscontroles moeten worden gegenereerd als reactie op een nieuw vrijgegeven product, een vrijgegeven variant of een vrijgegeven versie. |
| Uitvoeren in | Selecteer of gereedheidscontroles die worden gegenereerd in de rij van toepassing zijn op alle bedrijven of een enkel bedrijf. |
| Bedrijf | Als u het veld **Uitvoeren in** instelt op *Eén bedrijf*, selecteert u het bedrijf. |
| Type eigenaar | Selecteer of gereedheidscontroles die worden gegenereerd in de rij moeten worden toegewezen aan een persoon of een team. |
| Eigenaar | Selecteer de persoon of het team waaraan de gereedheidscontroles die worden gegenereerd in de rij moeten worden toegewezen. |
| Vragenlijst | Selecteer de vragenlijst die voor de controlelijst moet worden gebruikt. De controlelijst is een lokale controlelijst in het bedrijf waar de gereedheidscontrole is uitgevoerd. Het systeem moet kunnen beoordelen of de controlelijst correct is beantwoord. Daarom moet de controlelijst zo zijn ingesteld dat een evaluatie wordt uitgevoerd op basis van juiste antwoorden. Zie [Vragenlijsten gebruiken](/dynamicsax-2012/appuser-itpro/using-questionnaires) en verwante artikelen voor meer informatie over het maken van vragenlijsten. |
| Automatische goedkeuring | Records voor gereedheidscontroles bevatten een selectievakje **Goedgekeurd** waarmee de goedkeuringsstatus wordt aangegeven. Selecteer het selectievakje **Automatische goedkeuring** voor controles die direct op Goedgekeurd moeten worden gezet nadat de toegewezen gebruiker ze voltooid. Wis dit selectievakje uit als u expliciete goedkeuring als extra stap verplicht wilt maken. |
| Verplicht | Schakel dit selectievakje in voor controles die door de toegewezen gebruiker moeten worden voltooid. Verplichte controles kunnen niet worden overgeslagen. |

<a name="assign-policy"></a>

## <a name="assign-readiness-policies-to-standard-and-engineering-products"></a>Gereedheidsbeleid toewijzen aan standaard en technische producten

Wanneer u een nieuw product maakt op basis van een technische categorie, maakt u zowel een *vrijgegeven product* als een gerelateerd *gedeeld product*. De manier waarop gereedheidsbeleid voor een vrijgegeven product wordt opgelost, is afhankelijk van of de functie *Controles op productgereedheid* is ingeschakeld voor het systeem (zie de sectie [Gereedheidscontroles op standaardproducten](#standard-products) verderop in dit artikel voor informatie over deze functie en hoe u deze kunt in- of uitschakelen).

- Wanneer de functie *Productgereedheidscontroles* op uw systeem is *uitgeschakeld*, wordt het gereedheidsbeleid ingesteld en alleen weergegeven in [records van technische categorieën](engineering-versions-product-category.md). Om te weten te komen welk beleid van toepassing is op een vrijgegeven product, controleert het systeem het veld **Productgereedheidsbeleid** voor de gerelateerde technische categorie. U kunt het gereedheidsbeleid voor een bestaand product wijzigen door de gerelateerde technische categorie (niet het gedeelde product) te bewerken.
- Wanneer de functie *Productgereedheidscontrole* is *ingeschakeld*, wordt het veld **Productgereedheidscontrole** toegevoegd aan de pagina **Product** (waar gedeelde producten worden ingesteld) en aan de pagina **Vrijgegeven product** (waar de waarde alleen-lezen is en uit het gerelateerde gedeelde product wordt gehaald). Het gereedheidsbeleid voor een vrijgegeven product wordt gevonden door het gerelateerde gedeelde product te controleren. Wanneer u een technische categorie gebruikt om een nieuw technisch product te maken, worden zowel een gedeeld product als een vrijgegeven product gemaakt en wordt een instelling voor **Productgereedheidsbeleid** voor de technische categorie gekopieerd naar het nieuwe gedeelde product. Vervolgens kunt u het gereedheidsbeleid voor een bestaand product wijzigen door het gerelateerde gedeelde product (niet de vrijgegeven technische categorie) te bewerken.

Als u een gereedheidsbeleid aan een gedeeld product wilt toewijzen, voert u de volgende stappen uit.

1. Ga naar **Productgegevensbeheer \> Producten \> Producten**.
1. Open of maak het product waaraan u een gereedheidsbeleid wilt toewijzen.
1. Stel op sneltabblad **Algemeen** het veld **Productgereedheidsbeleid** in op de naam van het beleid dat op het product moet worden toegepast.

Als u een gereedheidsbeleid aan een technische categorie wilt toewijzen, voert u de volgende stappen uit.

1. Ga naar **Technisch wijzigingsbeheer \> Instellen \> Details van categorieën voor technische producten**.
1. Open of maak de technische categorie waaraan u een gereedheidsbeleid wilt toewijzen.
1. Stel op het sneltabblad **Productgereedheidsbeleid** het veld **Productgereedheidsbeleid** in op de naam van het beleid dat op de technische categorie moet worden toegepast.

<a name="standard-products"></a>

## <a name="readiness-checks-on-standard-products"></a>Gereedheidscontroles op standaardproducten

U kunt gereedheidcontroles van producten inschakelen voor standaardproducten (niet-technisch) door de functie *Productgereedheidscontrole* in te stellen in Functiebeheer. Met deze functie worden enkele kleine wijzigingen in het gereedheidscontrolesysteem aangebracht zodat standaardproducten worden ondersteund.

### <a name="enable-or-disable-readiness-checks-on-standard-products"></a>Gereedheidscontroles op standaardproducten in- of uitschakelen

Voor deze functie moeten de functies *Beheer voor technische wijzigingen* en *Controles op productgereedheid* zijn ingeschakeld voor uw systeem. Zie [Overzicht van technisch wijzigingsbeheer](product-engineering-overview.md) voor meer informatie over het in- of uitschakelen van deze functies.

### <a name="create-readiness-policies-for-standard-products"></a>Gereedheidsbeleid voor standaardproducten maken

U maakt gereedheidsbeleid voor standaardproducten op dezelfde manier als u dat voor technische producten doet. Zie de informatie eerder in dit artikel.

### <a name="assign-readiness-policies-to-standard-products"></a>Gereedheidsbeleid aan standaardproducten toewijzen

Als u een gereedheidsbeleid aan een standaardproduct wilt toewijzen, opent u het gerelateerde gedeelde product en stelt u het veld **Productgereedheidsbeleid** in op de naam van het beleid dat moet worden toegepast. Zie [Gereedheidsbeleid toewijzen aan standaard en technische producten](#assign-policy) eerder in dit artikel voor meer informatie.

### <a name="view-and-process-readiness-checks-on-standard-products"></a>Gereedheidscontroles op standaardproducten weergeven en verwerken

Wanneer deze functie is ingeschakeld, kunt u gereedheidscontroles voor standaardproducten weergeven en verwerken net als u dat voor een technisch product doet. Zie de informatie eerder in dit artikel.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
