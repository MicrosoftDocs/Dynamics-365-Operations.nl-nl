---
title: Uitgebreide garanties maken en configureren
description: In dit artikel wordt beschreven wat uitgebreide garanties zijn en hoe u ze maakt en configureert in Microsoft Dynamics 365 Commerce.
author: sijoshi
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9ed9851a9609e8a87ae0ffadc5cdd20c03fa17ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886979"
---
# <a name="create-and-configure-extended-warranties"></a>Uitgebreide garanties maken en configureren

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat uitgebreide garanties zijn en hoe u ze maakt en configureert in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Klanten kiezen steeds vaker voor uitgebreide ondersteuning en services wanneer ze producten kopen, met name bij consumentenproducten die worden verkocht tegen een premium prijspunt, zoals telefoons en computers. Door uitgebreide garanties te bieden voor aankopen kunnen detailhandelaren de klantloyaliteit versterken. De uitgebreide garantie geeft aan waar klanten service en ondersteuning kunnen krijgen. Zo kunnen zij erop vertrouwen dat hun problemen effectief worden afgehandeld.

Uitgebreide garanties kunnen worden verkocht aan klanten in een detailhandelkanaal tijdens de aanschaf van het product. Ze kunnen ook gedurende een beperkte tijd na de eerste aankoop worden verkocht.

### <a name="warranty-item-setup"></a>Garantieartikel instellen

Dynamics 365 Commerce biedt functies waarmee u een garantieartikel kunt maken en kenmerken hiervoor kunt instellen. Deze kenmerken omvatten de koppeling tussen een product en een garantieartikel, de prijs van de garantie en de duur van de garantie. Nadat een garantieartikel is geconfigureerd en vrijgegeven aan de organisatie-eenheid, kan een detailhandelaar garantie verkopen via MPOS-verkooppunten, online winkels en andere detailhandelkanalen.

### <a name="warranty-item-sales"></a>Garantieartikel verkopen

Uitgebreide garanties worden verkocht in een detailhandelkanaal tijdens de aanschaf van het product. Ze kunnen ook gedurende een beperkte tijd na de eerste aankoop worden verkocht.

Op het verkooppunt (POS) wordt verkoopmedewerkers gevraagd om een uitgebreide garantie toe te voegen wanneer de klant een gerelateerd product in de winkelwagen heeft geplaatst. Daarom wordt een verkoopkans voor meer-/bijverkoop aangeboden aan verkoopmedewerkers als onderdeel van de verkoopstroom.

Klanten kunnen ook later terugkomen en een uitgebreide garantie aanschaffen voor een product dat ze eerder hebben gekocht. In deze gevallen kan een verkoopmedewerker de oorspronkelijke transactie opzoeken en de klant het bijbehorende uitgebreide garantieartikel verkopen.

### <a name="warranty-terminology"></a>Garantieterminologie

In de volgende tabel worden enkele termen gedefinieerd die betrekking hebben op garantie.

| Voorwaarde | Omschrijving |
|------------------------------|--------------|
| Uitgebreide garantie/garantie | Een *uitgebreide garantie* verwijst naar een serviceovereenkomst of -contract met een langdurige garantie voor klanten. De uitgebreide garantie omvat de extra service voor het vervangen of repareren van artikelen tijdens de dekkingsperiode van de uitgebreide garantie. |
| Fabrieksgarantie | Een *fabrieksgarantie* (vaak een *beperkte garantie* genoemd) is de garantie die klanten ontvangen wanneer ze een product kopen. Hier volgen enkele kenmerken van de fabrieksgarantie:<ul><li>De garantiekosten zijn opgenomen in de kosten van het product. Klanten hoeven geen extra bedrag te betalen voor een fabrieksgarantie.</li><li>Afhankelijk van de productcategorie, duurt de fabrieksgarantie doorgaans 30 dagen, zes maanden of één jaar. (Voor de meeste elektronica is de garantie één jaar).</li><li>De garantie betreft eventuele defecten die worden veroorzaakt door mechanische of elektrische storingen. De dekking is beperkt en omvat geen ongevalsschade aan het gekochte product. Klanten die de aangeschafte producten tegen dagelijkse schade willen beschermen, moeten in een uitgebreide garantie investeren. Uitgebreide garanties duren twee tot tien jaar, afhankelijk van de productcategorie. Ze hebben ook een bredere dekking voor bijvoorbeeld alledaagse ongelukjes, zoals druppels, morsen en vlekken.</li></ul> |
| Garantieartikel | Een *garantieartikel* is een artikel met uitgebreide garantie die wordt verkocht voor een verzekerbaar artikel. Een voorbeeld is een schadedekking van twee jaar voor laptops. |
| Verzekerbaar artikel | Een *verzekerbaar artikel* is een geserialiseerd product waarvoor een garantie wordt verkocht. Een laptop is bijvoorbeeld een verzekerbaar artikel waarvoor een uitgebreide garantie van twee jaar en drie jaar wordt verkocht. |
| Garantiegroep | Een *garantiegroep* is een relatie tussen garantieartikelen en verzekerbare artikelen. Het POS gebruikt garantiegroepen om te bepalen welke garantieartikelen door verkoopmedewerkers kunnen worden toegevoegd wanneer een verzekerbaar artikel in de winkelwagen van een klant wordt geplaatst. |
| Garantiebeleid | Een *garantiebeleid* is een entiteit die in Commerce wordt gemaakt wanneer een garantiebeleid wordt verkocht. Een garantiebeleid bevat informatie zoals de begin- en einddatum van het aangeschafte garantieartikel, de algemene voorwaarden en het serienummer van het product onder garantie. Garantiebeleidsnummers kunnen worden gedeeld met klanten, zodat ze beschikken over een verwijzing naar het uitgebreide garantieartikel dat ze hebben gekocht. |

## <a name="create-a-warranty-item"></a>Een garantieartikel maken

Voer de volgende stappen uit om een garantieartikel te maken in Commerce.

1. Ga naar **Detailhandel en commerce \> Producten en categorieën \> Producten**.
1. Selecteer **Nieuw** om een garantieartikel te maken.
1. Selecteer **Service** in het veld **Producttype** in het dialoogvenster **Nieuw product**.
1. Selecteer in het veld **Subtype van product** de optie **Product**.
1. Selecteer in het veld **Productservicetype** de optie **Service**.
1. Voer in het veld **Productnaam** de productnaam in.
1. Selecteer in het veld **Detailhandelscategorie** een waarde in het dialoogvenster met vervolgkeuzemenu en selecteer vervolgens **OK**.
1. Voer in het veld **Productnummer** het productnummer in.
1. Selecteer **OK**.
1. Stel op de pagina **Productgegevens** op het sneltabblad **Garantie** de velden **Tijdseenheid** en **Tijdsduur** in.

    | Veldnaam | Waarde | Omschrijving |
    |------------|-------|-------------|
    | Tijdseenheid | **Dagen**, **Weken**, **Maanden** of **Jaren** | Dit veld bevat de tijdseenheid die voor de garantie wordt gebruikt. |
    | Tijdsduur | Een positieve gehele waarde | In dit veld wordt de duur van de garantie in de geselecteerde tijdseenheid opgegeven. |

    Voor een garantieperiode van twee jaar stelt u bijvoorbeeld het veld **Tijdseenheid** in op **Jaren** en het veld **Tijdsduur** op **2**. U kunt ook het veld **Tijdseenheid** instellen op **Maanden** en het veld **Tijdsduur** op **24**, zoals wordt weergegeven in de volgende afbeelding.

    ![De pagina met productgegevens voor een garantieartikel.](./media/ew-time-properties.png)

1. Selecteer **Opslaan** om het garantieartikel op te slaan.
1. Geef het garantieproduct vrij aan het bedrijf zodat het kan worden verkocht. Zie voor meer informatie [Detailhandelproducten instellen](set-up-retail-products.md).
1. Stel op de pagina **Vrijgegeven productdetails** op het sneltabblad **Garantie** de velden **Basis prijsbereik**, **Ondergrens** en **Bovengrens** in.

    | Veldnaam | Waarde | Omschrijving |
    |------------|-------|-------------|
    | Basis prijsbereik | **Geen**, **Basisprijs** of **Verkoopprijs** | <ul><li>**Geen**: de waarden voor de **ondergrens** en de **bovengrens** van het prijsbereik zijn niet van toepassing.</li><li>**Basisprijs** : een bepaalde garantie is van toepassing als de basisprijs (dat wil zeggen de prijs zonder kortingen) van het verzekerbare artikel zich tussen de hier opgegeven waarden voor **Ondergrens** en **Bovengrens** bevindt, op basis van de prijs van het verzekerbare artikel.</li><li>**Verkoopprijs**: deze waarde is gereserveerd voor toekomstig gebruik.</li></ul> |
    | Ondergrens, Bovengrens | Een positieve gehele waarde | Met deze velden definieert u de hoogste en laagste prijslimieten van het verzekerbare artikel, en hoe het huidige garantieartikel van toepassing is op het verzekerbare artikel. Deze limieten kunnen zijn gebaseerd op de basisprijs van het verzekerbare artikel (ook bekend als de adviesprijs van de fabrikant \[MSRP\]). Als het veld **Basis prijsbereik** wordt ingesteld op **Basisprijs**, wordt alleen bij een verzekerbaar artikel (product) met een basisprijs tussen de waarden voor **Ondergrens** en **Bovengrens** de prompt weergegeven om een garantieartikel op het POS toe te voegen. |

    In de volgende afbeelding ziet u een voorbeeld van het veld **Basis prijsbereik** ingesteld op **Basisprijs**, waarbij het veld **Ondergrens** is ingesteld op $ 500 en het veld **Bovengrens** op $ 1000.
    
    ![De pagina met vrijgegeven productgegevens voor een garantieartikel.](./media/ew-release-product-details.png)

1. Deel het garantieartikel in bij het kanaal waar het wordt verkocht. Zie [Assortimenten instellen](set-up-assortments.md) voor meer informatie.

### <a name="example"></a>Voorbeeld

Een verzekerbare laptop (product) heeft een basisprijs van $ 999 en er zijn twee garantieartikelen voor laptops:

- Garantie\_1 heeft een ondergrens van $ 500 en een bovengrens van $ 1.000 en het veld **Basis prijsbereik** wordt ingesteld op **Basisprijs**.
- Garantie\_2 heeft een ondergrens van $ 1.001 en een bovengrens van $ 2.000 en het veld **Basis prijsbereik** wordt ingesteld op **Basisprijs**.

Wanneer het verzekerbare laptopartikel aan de winkelwagen van een klant wordt toegevoegd, wordt de prompt om garantie\_1 toe te voegen in het POS weergegeven, omdat de prijs van de laptop tussen de onder- en bovengrens voor garantie\_1 ligt.

> [!NOTE]
> Voor dit voorbeeld kunt u het veld **Basis prijsbereik** instellen op **Geen** als u prompts wilt weergeven voor zowel garantie\_1 als garantie\_2, ongeacht de prijs van het verzekerbare artikel.

## <a name="configure-channel-specific-settings"></a>Kanaalspecifieke instellingen configureren

Met kanaalspecifieke instellingen kunt u opgeven of u wilt dat er een prompt voor het toevoegen van een garantieartikel wordt weergegeven op het POS wanneer een verzekerbaar artikel wordt toegevoegd aan de winkelwagen van de klant.

Voer deze stappen uit om een kanaalspecifieke instelling te configureren voor Commerce.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Garantie \> Instellingen garantie**.
1. Voer op het tabblad **Kanaalspecifiek** in de kolom **Vragen voor garantie** voor uw kanaal een van de volgende stappen uit:

    - Schakel het selectievakje in als er een prompt voor het garantieartikel moet worden weergegeven op het POS wanneer het verzekerbare artikel aan de winkelwagen wordt toegevoegd.
    - Schakel het selectievakje uit als er geen prompt voor het garantieartikel moet worden weergegeven op het POS wanneer het verzekerbare artikel aan de winkelwagen wordt toegevoegd.

1. Voer de taak **1070** uit om de gegevens te synchroniseren met het kanaal.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Een nummerreeks voor garantiebeleid configureren

Elk garantiebeleid wordt uniek geïdentificeerd door een garantiebeleidsnummer dat door een nummerreeks wordt gegenereerd. Zie [Overzicht van nummerreeksen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) voor meer informatie over nummerreeksen.

Voer de volgende stappen uit om een nummerreeks voor garantiebeleid in Commerce te configureren.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Garantie \> Instellingen garantie**.
1. Typ of selecteer een waarde op het tabblad **Nummerreeksen** in de rij voor de verwijzing **Garantiebeleid** in het veld **Nummerreekscode**.

## <a name="set-up-a-warranty-group"></a>Een garantiegroep instellen

Een garantiegroep is een relatie tussen garantieartikelen en verzekerbare artikelen. Het POS gebruikt garantiegroepen om te bepalen welke garantieartikelen door verkoopmedewerkers kunnen worden toegevoegd wanneer een verzekerbaar artikel in de winkelwagen van een klant wordt geplaatst.

Volg deze stappen als u de garantie in Commerce wilt instellen.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Garantie \> Garantiegroepen**.
1. Selecteer **Nieuw** om een garantiegroep te maken.
1. Geef in het veld **Naam** een naam op voor de nieuwe groep.
1. Typ op het sneltabblad **Algemeen** in het veld **Beschrijving** een beschrijving van de groep.
1. Selecteer op het sneltabblad **Garantieproducten** de optie **Regel toevoegen** om een garantieartikel toe te voegen.
1. Voer in het veld **Weergavevolgorde** een nummer in om de garantiegroep op het POS te rangschikken. Op het POS worden garantieartikelen weergegeven in oplopende volgorde in de garantieprompt.
1. Selecteer op het sneltabblad **Verzekerbare producten** de optie **Regel toevoegen** om verzekerbare producten toe te voegen.
1. Als het garantieartikel van toepassing is op een hele categorie met verzekerbare artikelen (producten), selecteert u de categorie in het veld **Categorie**. Als het garantieartikel van toepassing is op een specifiek verzekerbare artikel (product), selecteert u het product in het veld **Product**.
1. Selecteer op het sneltabblad **Relevante kanalen** de optie **Regel toevoegen** om het kanaal toe te voegen waarin u het garantieartikel wilt verkopen.
1. Selecteer **Opslaan** om de configuratie op te slaan.
1. Selecteer **Publiceren** om de garantiegroep te publiceren.
1. Voer de taak **1040** uit om de gegevens te synchroniseren met het kanaal.

## <a name="sell-warranty-items-at-the-pos"></a>Garantieartikelen op het POS verkopen

Er zijn twee POS-bewerkingen voor verkoopmedewerkers om garantieartikelen te verkopen tijdens de werkstroom voor klantaankopen:

- **Garantie toevoegen**: met deze bewerking wordt een prompt geactiveerd waarin toepasselijke garanties worden weergegeven voor een verzekerbaar artikel dat is geselecteerd in de winkelwagen.
- **Garantie toevoegen aan bestaande transactie**: met deze bewerking kunnen verkoopmedewerkers garantie verkopen voor verzekerbare artikelen die eerder zijn verkocht. Verkoopmedewerkers kunnen de oorspronkelijke transactie voor een verzekerbaar artikel vinden door het ontvangstnummer van de transactie in te voeren.

In de volgende afbeelding ziet u een voorbeeld van een POS-terminalpagina met een prompt om een garantieartikel toe te voegen voor de huidige aankoop van een verzekerbaar artikel.

![Voorbeeld van een prompt om een garantieartikel toe te voegen voor de huidige aankoop.](./media/ew-sell-warranty.png)

In de volgende afbeelding ziet u een voorbeeld van de functie voor het toevoegen van een garantieartikel aan een verzekerbaar artikel dat eerder is verkocht.

![Voorbeeld van de functie voor het toevoegen van een garantieartikel voor een eerder verkocht verzekerbaar artikel.](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Garantietransacties verwerken

Wanneer garanties worden verkocht in contante transacties, nadat de transacties zijn geboekt in Commerce Headquarters, kunnen Commerce-gebruikers de taak **Garantietransacties verwerken** uitvoeren om de garantietransacties te verwerken en het garantiebeleid te maken.

Voer deze stappen uit om garantietransacties te verwerken in Commerce Headquarters.

1. Ga naar **Retail en Commerce \> Producten en categorieën \> Garantie \> Garantietransacties verwerken**.
1. Selecteer een waarde in het dialoogvenster **Organisatieknooppunten kiezen** in het veld **Organisatiehiërarchie**.
1. Selecteer in de lijst **Beschikbare organisatieknooppunten** een afzonderlijke winkel, of een knooppunt als u de batchtaak voor een groep winkels wilt maken.
1. Selecteer de knop pijl-rechts om uw selectie toe te voegen aan de lijst **Geselecteerde organisatieknooppunten**.
1. Selecteer het tabblad **Op de achtergrond uitvoeren**.
1. Stel de optie **Batchverwerking** in op **Ja** en selecteer vervolgens **Terugkeerpatroon**.
1. Selecteer in het dialoogvenster **Terugkeerpatroon definiëren** in het veld **Begindatum** een begindatum voor het terugkeerpatroon of voer deze in.
1. Selecteer in het veld **Begintijd** een begintijd voor het terugkeerpatroon of voer deze in.
1. Volg één van deze stappen:

    - Selecteer de optie **Geen einddatum** als het terugkeerpatroon nooit moet eindigen.
    - Selecteer de optie **Beëindigen na** als het terugkeerpatroon na een bepaald aantal keer moet eindigen. Als u deze optie selecteert, voert u het aantal keer in.
    - Selecteer de optie **Beëindigen voor** als het terugkeerpatroon op een bepaalde datum moet eindigen. Als u deze optie selecteert, selecteert u de datum of voert u deze in.

1. Selecteer **OK**.
1. Selecteer **OK**.

## <a name="warranty-policies"></a>Garantiebeleid

Wanneer een uitgebreide garantie wordt verkocht, wordt automatisch een entiteit voor een garantiebeleid gemaakt. Garantiebeleidsnummers kunnen worden gedeeld met klanten, zodat ze beschikken over een verwijzing naar het garantieartikel dat ze hebben gekocht. De eigenschappen van garantiebeleid omvatten de ingangsdatum en vervaldatum van de garantie, de voorwaarden en het serienummer van het verzekerbare artikel waarvoor de garantie is verkocht.

> [!NOTE]
> Er worden automatisch eigenschappen van garantiebeleid gegenereerd wanneer entiteiten met garantiebeleid worden gemaakt. Momenteel kunnen ze niet handmatig worden geconfigureerd of bewerkt.

De volgende tabel beschrijft de eigenschappen van het garantiebeleid en de bijbehorende waarden. In Commerce Headquarters heeft de databasetabel de naam WARRANTYPOLICY.

| Naam van eigenschap. | Waarde | Omschrijving |
|---------------|-------|-------------|
| PolicyNumber | Een tekenreeks (maximaal 20 tekens) | Het garantiebeleidsnummer |
| WarrantiedItemId | Een tekenreeks (maximaal 20 tekens) | De id van het verzekerbare artikel. |
| WarrantiedInventoryLotId | Een tekenreeks (maximaal 20 tekens) | De id van de voorraadpartij van het verzekerbare artikel. |
| WarrantiedSerialNumber | Een tekenreeks (maximaal 20 tekens) | Het serienummer van het verzekerbare artikel |
| WarrantiedFulfilledDate | Een datum | De afhandelingsdatum van het verzekerbare artikel |
| WarrantyItemId | Een tekenreeks (maximaal 20 tekens) | De id van het garantieartikel. |
| WarrantyInventoryLotId | Een tekenreeks (maximaal 20 tekens) | De id van de voorraadpartij van het garantieartikel |
| WarrantySalesDate | Een datum | De verkoopdatum van het garantieartikel. |
| WarrantyEffectiveDate | Een datum | De ingangsdatum van het garantiebeleid |
| WarrantyExpirationDate | Een datum | De vervaldatum van het garantiebeleid |
| CustAccount | Een tekenreeks (maximaal 20 tekens) | Het rekeningnummer van de klant |
| Status | **Gemaakt**, **Ongeldig gemaakt**, **Geldig vanaf** of **Vervallen** | De status van het garantiebeleid |
| Opmerkingen | Een tekenreeks (maximaal 255 tekens) | Opmerkingen over het garantiebeleid, zoals de voorwaarden |

## <a name="frequently-asked-questions-faq"></a>Veelgestelde vragen (FAQ)

**Waarom zie ik geen garantieprompt in het POS?**

Controleer of het garantieartikel is ingedeeld bij het kanaal. Controleer ook of de garantiegroep zo is geconfigureerd dat deze het relevante kanaal bevat.

**Waarom zie ik geen transactieregelartikelen als ik probeer een garantie toe te voegen aan een bestaande transactie en het ontvangstnummer van de klantorder opgeef?**

Ontvangstbewijzen zijn alleen beschikbaar als een pull-taak (P-taak) wordt uitgevoerd om de ontvangsten naar Commerce Headquarters te uploaden. Als u de P-taak wilt uitvoeren, gaat u naar **Detailhandel en Commerce \> IT detailhandel en commerce \> Distributieplanning**, selecteert u de taak **P-0001** en selecteert u **Nu uitvoeren**.

**Waarom is de garantiefunctie alleen van toepassing op producten met een serienummer?**

Een garantie is een service die wordt geleverd voor een specifiek uniek product. In Dynamics 365 kan een product uniek worden aangeduid met een serienummer.

## <a name="additional-resources"></a>Aanvullende bronnen

[Detailhandelproducten instellen](set-up-retail-products.md)

[Assortimenten instellen](set-up-assortments.md)

[Overzicht van Nummerreeksen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]