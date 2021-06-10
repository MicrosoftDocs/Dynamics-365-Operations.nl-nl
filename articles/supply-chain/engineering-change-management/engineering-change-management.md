---
title: Wijzigingen in technische producten beheren
description: Dit onderwerp bevat informatie over technisch wijzigingsbeheer. Technisch wijzigingsbeheer biedt gestructureerde processen voor het beheren van wijzigingen in technische producten, van het voorstellen, aanvragen en aanbrengen van wijzigingen en het evalueren en goedkeuren van wijzigingen tot het beoordelen van de invloed op bestaande transacties en het opvolgen van de wijzigingen.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcmRequestSelection,EngChgEcmRequestProducts,EngChgEcmRequestPriorityChart,EngChgEcmRequestListPage,EngChgEcmRequestFilteredPart,EngChgEcmRequestDetails,EngChgEcmReason,EngChgEcmProjTableInformation,EngChgEcmProductRoute,EngChgEcmProductRelease,EngChgEcmProductPreview, EngChgEcmWhereUsed, EngChgEcmInventTrans,EngChgEcmHeaderSelection,EngChgEcmHeaderPreviewPart,EngChgEcmHeaderFilteredPart,EngChgEcmHeaderDetails, EngChgCaseWhereUsedAnalysis, EngChgCaseValidatorMessage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d31c73964877aeb1556c93b03d276698e8d84d30
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/28/2021
ms.locfileid: "6114994"
---
# <a name="manage-changes-to-engineering-products"></a>Wijzigingen in technische producten beheren

[!include [banner](../includes/banner.md)]

Technisch wijzigingsbeheer biedt gestructureerde processen voor het beheer van wijzigingen in technische producten. U kunt het proces voor het *aanvragen van technische wijzigingen* gebruiken om wijzigingen voor te stellen en aan te vragen. Vervolgens kunt u het proces *order voor technische wijziging* gebruiken om deze wijzigingen daadwerkelijk door te voeren. Gebruikers kunnen aanvragen van of orders voor technische wijzigingen maken. Vervolgens wordt een proces voor het beoordelen en goedkeuren, het bepalen van de impact op bestaande transacties en de opvolging hiervan uitgevoerd.

## <a name="engineering-change-requests"></a>Technische-wijzigingsaanvragen

Met het proces voor het aanvragen van technische wijzigingen kunt u aanvragen voor wijzigingen vastleggen van alle relevante afdelingen in uw bedrijf. Het maakt niet uit of u werkt als technicus of op de afdeling Productie, Sourcing, Magazijn of Verkoop: iedereen kan een aanvraag voor technische wijzigingen gebruiken om een wijziging aan te vragen. Deze wijziging kan een idee zijn voor een nieuw product, een probleem dat u hebt ontdekt tijdens het werken met een bestaand product, een suggestie voor het verbeteren van een bestaand product of iets anders.

Nadat iemand een wijzigingsaanvraag heeft ingediend, wordt het proces voor *revisie en goedkeuring* beheerd via een werkstroom waarmee wordt aangegeven wie de wijziging moet goedkeuren (bijvoorbeeld de eigenaar van het product).

Als u een werkstroom wilt instellen voor orders voor of aanvragen van technische wijzigingen, gaat u naar **Technisch wijzigingsbeheer \> Technische werkstromen**. Selecteer **Nieuw**, selecteer of de werkstroom wordt gebruikt om orders voor of aanvragen van technische wijzigingen te controleren en configureer vervolgens de werkstroom.

Zie [Overzicht van werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) voor meer informatie over werkstromen. Zie [Producteigenaren](product-owner.md) voor meer informatie over producteigenaren.

### <a name="create-a-new-engineering-change-request"></a>Een nieuwe technische-wijzigingsaanvraag maken

Voer een van de volgende stappen uit om een aanvraag voor een technische wijziging te maken.

- Ga naar **Technisch wijzigingsbeheer \> Algemeen \> Technisch wijzigingsbeheer \> Aanvragen van technische wijzigingen** en selecteer **Nieuw** in het actievenster.
- Open de pagina **Productdetails** voor een bestaand technisch product. Selecteer vervolgens in het actievenster op het het tabblad **Technicus** in de groep **Technisch wijzigingsbeheer** de optie **Aanvraag voor technische wijziging \> Nieuwe aanvraag voor technische wijziging**.

Er wordt een nieuwe wijzigingsaanvraag gemaakt. U kunt nu de velden op elk sneltabblad instellen zoals wordt beschreven in de volgende subsecties.

#### <a name="general-fasttab"></a>Het sneltabblad Algemeen

Op het sneltabblad **Algemeen** kunt u een basisomschrijving voor de wijzigingsaanvraag invoeren. In de volgende tabel worden de velden op dit sneltabblad beschreven.

| Veld | Beschrijving |
|---|---|
| Wijzigingsaanvraag | Voer een naam in voor de aanvraag voor de technische wijziging. |
| Titel | Voer tekst in die de wijzigingen in de aanvraag kort beschrijft of identificeert. |
| Prioriteit | Selecteer een waarde om aan te geven hoe hoog de prioriteit van de wijziging is. U kunt de beschikbare waarden voor uw bedrijf zo nodig aanpassen. (Zie voor meer informatie [Algemene waarden voor het beheer van technische wijzigingen vaststellen](engineering-change-management-setup.md).) |
| Categorie | Selecteer een waarde om het type wijziging te beschrijven dat u aanvraagt. U kunt de beschikbare waarden voor uw bedrijf zo nodig aanpassen. (Zie voor meer informatie [Algemene waarden voor het beheer van technische wijzigingen vaststellen](engineering-change-management-setup.md).) |
| Ernst | Selecteer een waarde om de ernst van het probleem aan te geven dat moet worden opgelost door de aanvraag te implementeren. U kunt de beschikbare waarden voor uw bedrijf zo nodig aanpassen. (Zie voor meer informatie [Algemene waarden voor het beheer van technische wijzigingen vaststellen](engineering-change-management-setup.md).) |
| Aangevraagd door | De naam van de gebruiker die de aanvraag heeft gemaakt. |
| Aan | De datum waarop de aanvraag is gemaakt. |
| Status | De status van de aanvraag. Wanneer een aanvraag wordt gemaakt, krijgt deze de status *Gemaakt*. Wanneer de aanvraag wordt goedgekeurd, wordt de status gewijzigd in *Goedgekeurd*. Als er een gerelateerde wijzigingsorder is gemaakt voor de aanvraag, wordt de status gewijzigd in *Opvolging*. |
| Wijzigingsorder | Het wijzigingsordernummer, als de wijzigingsaanvraag via een wijzigingsorder is opgevolgd. |

#### <a name="information-fasttab"></a>Sneltabblad Informatie

Op het sneltabblad **Informatie** kunt u meer informatie over de aanvraag toevoegen.

Als u een rij aan het raster wilt toevoegen, selecteert u **Nieuw** op de werkbalk boven het raster en selecteert u een van de volgende opties:

- **Bestand**: upload een bestand.
- **Afbeelding**: upload een afbeeldingsbestand.
- **Notitie**: voer rechtstreeks in het raster een notitie in.
- **URL**: voer rechtstreeks in het raster een URL in.

In de volgende tabel worden de velden voor elke rij beschreven.

| Veld | Beschrijving |
|---|---|
| Aanmaakdatum en -tijd | De datum en het tijdstip waarop de rij is gemaakt. |
| Type | Het type informatie waarvoor de rij is gemaakt (bestand, afbeelding, notitie of URL). |
| Beschrijving | Voer een beschrijving voor de rij in. |
| Beperking | Een waarde die aangeeft of de toegevoegde informatie afkomstig is van een interne of externe bron. |
| Gekoppeld | Een ingeschakeld selectievakje geeft aan dat de rij een bijlage (bestand of afbeelding) bevat. Als u de bijlage wilt downloaden, selecteert u de rij en vervolgens **Openen** op de werkbalk boven het raster. |

#### <a name="products-fasttab"></a>Het sneltabblad Producten

Op het sneltabblad **Producten** kunt u alle producten vermelden waarop de wijzigingsaanvraag van toepassing is. Gebruik de knoppen op de werkbalk om producten aan het raster toe te voegen of uit het raster te verwijderen.

Deze lijst is alleen bedoeld voor informatieve doeleinden. Daarom kunt u zoveel gerelateerde producten toevoegen als u nodig vindt. Als u een wijzigingsaanvraag maakt via de pagina **Productdetails** voor een bestaand product, moet dat product worden vermeld op het sneltabblad **Producten** nadat u de aanvraagrecord hebt opgeslagen.

#### <a name="source-fasttab"></a>Het sneltabblad Bron

Op het sneltabblad **Bron** kunt u het beginpunt van de wijzigingsaanvraag bijhouden. Dit is handig als u bijvoorbeeld wilt zien of de wijzigingsaanvraag is gemaakt op basis van een verkooporder, wie deze heeft gemaakt en in welk bedrijf deze is gemaakt.

### <a name="evaluate-the-business-impact-of-a-change-request-and-send-notifications"></a>De bedrijfsimpact van een wijzigingsaanvraag evalueren en meldingen verzenden

Wanneer u een wijzigingsaanvraag bekijkt, kunt u naar afhankelijkheden zoeken. Op deze manier kunt u het effect beoordelen van de aangevraagde wijziging op openstaande transacties, zoals verkooporders, productieorders en voorhanden voorraad. Tijdens het controleren van wijzigingsaanvragen kunt u meldingen verzenden naar de personen die verantwoordelijk zijn voor het uitvoeren van de verschillende typen gerelateerde orders.

#### <a name="review-affected-transactions-block-selected-transactions-and-send-notifications"></a>Beïnvloede transacties controleren, geselecteerde transacties blokkeren en meldingen verzenden

Als u beïnvloede transacties wilt controleren, geselecteerde transacties wilt blokkeren en gerelateerde meldingen wilt verzenden, gaat u als volgt te werk.

1. Ga naar **Technisch wijzigingsbeheer \> Algemeen \> Technisch wijzigingsbeheer \> Aanvragen van technische wijzigingen**.
1. Open een bestaande wijzigingsaanvraag of selecteer **Nieuw** in het actievenster om een nieuwe wijzigingsaanvraag te maken.
1. Selecteer in het actievenster op het tabblad **Wijzigingsaanvraag** in de groep **Bedrijfsimpact** een van de volgende knoppen:

    - **Zoeken**: alle openstaande transacties scannen en vervolgens het dialoogvenster **Bedrijfsimpact op openstaande transacties** openen met alle transacties die door de wijziging worden beïnvloed.
    - **Vorige zoekopdracht weergeven**: het dialoogvenster **Bedrijfsimpact op openstaande transacties** met de resultaten van de vorige zoekopdracht openen. (Een nieuwe zoekopdracht wordt niet uitgevoerd.)

1. Het dialoogvenster **Bedrijfsimpact op openstaande transacties** bevat een set tabbladen waarbij elk tabblad een lijst met beïnvloede transacties van een bepaald type bevat (**Verkooporders**, **Inkooporders**, **Productieorders**, **Voorraad** enzovoort). Op elk tabblad wordt ook een nummer weergegeven dat het aantal beïnvloede transacties van dat type aangeeft. Selecteer een tabblad om de relevante lijst weer te geven.
1. Als u met een transactie in de lijst wilt werken, selecteert u deze en selecteert u vervolgens een van de volgende knoppen op de werkbalk:

    - **Transactie weergeven**: de geselecteerde transactierecord openen.
    - **Order blokkeren**: deze knop is alleen beschikbaar op het tabblad **Verkooporders**. Selecteer deze optie om de geselecteerde verkooporder te blokkeren.
    - **Regel blokkeren**: deze knop is alleen beschikbaar op het tabblad **Inkooporders**. Selecteer deze optie om de geselecteerde inkooporderregel te blokkeren.
    - **Verantwoordelijke persoon waarschuwen**: deze knop is alleen beschikbaar op het tabblad **Verkooporders**. Selecteer deze knop om een melding over de wijziging te verzenden naar de gebruiker die is ingesteld als verantwoordelijke voor de geselecteerde verkooporder.
    - **Besteller waarschuwen**: deze knop is alleen beschikbaar op het tabblad **Inkooporders**. Selecteer deze knop om een melding over de wijziging te verzenden naar de gebruiker die is ingesteld als de besteller voor de geselecteerde inkooporder.
    - **Productie waarschuwen**: deze knop is alleen beschikbaar op het tabblad **Productieorders**. In tegenstelling tot verkoop- en inkooporders hebben productieorders geen enkele gebruiker die van begin tot eind is ingesteld als verantwoordelijke voor deze orders. In plaats daarvan nemen verschillende supervisors of planners meestal de verantwoordelijkheid voor een bepaalde locatie of voor een bepaald deel van de productie (bijvoorbeeld voor specifieke resources of resourcegroepen). Wanneer u deze knop selecteert, ontvangen alle gebruikers die verantwoordelijk zijn voor een resource die is gerelateerd aan de geselecteerde productieorder daarom een wijzigingsmelding.
    - **Voorbereider waarschuwen**: deze knop is alleen beschikbaar op het tabblad **Opdracht tot inkoop**. Selecteer deze knop om een melding over de wijziging te verzenden naar de gebruiker die is ingesteld als de voorbereider van de geselecteerde opdracht tot inkoop.
    - **Verantwoordelijke verkoper waarschuwen**: deze knop is alleen beschikbaar op het tabblad **Offertes**. Selecteer deze knop om een melding over de wijziging te verzenden naar de gebruiker die is ingesteld als verantwoordelijke voor de geselecteerde offerte.
    - **Uitval**: deze knop is alleen beschikbaar op het tabblad **Voorraad**. Selecteer deze knop om de geselecteerde voorraad voor uitval te selecteren.
    - **Historie weergeven**: open een historie van acties die zijn ondernomen voor de geselecteerde transactie met behulp van het dialoogvenster **Bedrijfsimpact op openstaande transacties**. (De historie geeft bijvoorbeeld aan of meldingen zijn verzonden of transacties zijn geblokkeerd.) 
    - **Alle transacties weergeven**: open de volledige lijst met alle transacties, niet alleen de openstaande transacties.

#### <a name="review-and-process-change-notifications-for-transactions"></a>Meldingen over wijzigingen voor transacties controleren en verwerken

U kunt de wijzigingsmeldingen die u ontvangt op de volgende manieren lezen en verwerken:

- Behalve voor productieorders worden wijzigingsmeldingen voor de transacties waarvoor u verantwoordelijk bent in het actiecentrum weergegeven. De knop **Berichten weergeven** (belsymbool) aan de rechterkant van de navigatiebalk geeft aan wanneer een bericht voor u beschikbaar is in het actiecentrum. Selecteer de knop **Berichten weergeven** om het actiecentrum te openen en de berichten te bekijken.
- Als u alle productieorders wilt weergeven waarvoor een technische melding is verzonden, gaat u naar **Productieorders \> Productieorders \> Alle productieorders**. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Technische-wijzigingsaanvraag** de optie **Technische meldingen** om de pagina **Technische meldingen** te openen.
- Voor productieorders kunt u ervoor kiezen alleen de meldingen over de wijziging te bekijken die van toepassing zijn op de productiebronnen die u beheert. Selecteer in het werkgebied **Productiebeheer** in het actievenster **Mijn werkgebied configureren** om de pagina te filteren zodat alleen informatie wordt weergegeven over de productie-eenheden, groepen en/of resources die u beheert. In de sectie **Overzicht** wordt op een tegel met de naam **Productieorders met gewijzigde producten** een aantal meldingen weergegeven die overeenkomen met uw filterinstellingen. Selecteer deze tegel om de pagina **Technische meldingen** te openen, die de volledige lijst met transacties bevat die voldoen aan de criteria van uw filter.

Wanneer u productieordermeldingen controleert op de pagina **Technische meldingen**, kunt u koppelingen naar gerelateerde wijzigingsorders of productieorders volgen door kolomwaarden te selecteren of door de bijbehorende opdrachten in het actievenster te gebruiken. Wanneer u klaar bent met het evalueren van een wijziging en wanneer u productieorders hebt geannuleerd of indien nodig gewijzigd, kunt u een melding markeren als opgelost. Selecteer de melding en selecteer vervolgens **Oplossen** in het actievenster. De melding wordt uit alle weergaven van gebruikers verwijderd.

### <a name="create-a-change-order-from-a-change-request"></a>Een wijzigingsorder maken op basis van een wijzigingsaanvraag

Een technicus die een aanvraag voor een technische wijziging bekijkt, kan een order voor technische wijzigingen maken via de pagina **Aanvragen van technische wijzigingen**. Selecteer in het actievenster op het tabblad **Wijzigingsaanvraag** in de groep **Order voor technische wijziging** de optie **Koppeling en producten kopiëren**.

## <a name="engineering-change-orders"></a>Technische-wijzigingsorders

Orders voor technische wijzigingen bieden een gestructureerd proces voor het aanbrengen van wijzigingen in technische producten. U stelt wijzigingen voor door een kopie van de technisch relevante gegevens te gebruiken. De werkelijke hoofdgegevens blijven ongewijzigd. Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie over technisch relevante gegevens.

U kunt een order voor technische wijzigingen maken die is gebaseerd op een goedgekeurde aanvraag voor een technische wijziging. Technici kunnen ook zelf nieuwe orders voor technische wijzigingen maken. U kunt meerdere producten in één order voor technische wijzigingen opnemen door een van de volgende stappen uit te voeren:

- Selecteer producten handmatig.
- Gebruik de stuklijst om producten op te nemen die lager staan in de productstructuur (onderliggende items).
- Gebruik een zoekopdracht voor de gebruikslocatie om producten hoger in de productstructuur (bovenliggende items) op te nemen.

Nadat het voorstel voor wijzigingen is voltooid, wordt het revisie- en goedkeuringsproces door een werkstroom verwerkt. U kunt verschillende werkstromen instellen, op basis van prioriteit en ernst.

Als u een werkstroom wilt instellen voor orders voor of aanvragen van technische wijzigingen, gaat u naar **Technisch wijzigingsbeheer \> Technische werkstromen**. Selecteer **Nieuw**, selecteer of de werkstroom wordt gebruikt om orders voor of aanvragen van technische wijzigingen te controleren en configureer vervolgens de werkstroom.

Zie [Overzicht van werkstroomsysteem](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) voor meer informatie over werkstromen.

Hier volgen enkele algemene belanghebbenden die mogelijk een order voor technische wijzigingen moeten goedkeuren:

- **Producteigenaren**: zie [Producteigenaren](product-owner.md) voor meer informatie over producteigenaren.
- **Verantwoordelijke teamleider**: het veld **Technicus** in de weergave **Koptekst** van de order voor technische wijzigingen toont de technicus die de order voor technische wijzigingen heeft gemaakt. Als de technicus bij een team hoort dat in het systeem is gedefinieerd, wordt in het veld **Verantwoordelijke** de leider van dat team weergegeven.
- **Financiële afdeling**: de financiële afdeling moet mogelijk gevallen beoordelen waarbij de wijziging tot hoge kosten leidt.

U kunt kiezen of de order voor technische wijzigingen direct na goedkeuring moet worden verwerkt, als onderdeel van de werkstroom, of later moet worden verwerkt, als een handmatige stap. Tijdens de verwerking van een order voor technische wijzigingen worden technische gegevens voor het werkelijke product bijgewerkt.

Terwijl u een aanvraag voor een wijziging bekijkt, selecteert u in het actievenster op het tabblad **Wijzigingsaanvraag** in de groep **Bedrijfsimpact** de optie **Zoeken** om de impact van de voorgestelde wijziging op openstaande transacties, zoals verkooporders, productieorders en voorhanden voorraad, te beoordelen. De resultaten worden weergegeven in het dialoogvenster **Bedrijfsimpact op openstaande transacties**, waarin u beïnvloede transacties kunt selecteren en vervolgens opdrachten op de werkbalk kunt gebruiken om meer informatie weer te geven, de verantwoordelijke gebruiker op de hoogte te stellen of de transactie te blokkeren.

### <a name="engineering-change-orders-in-engineering-or-operational-companies"></a>Orders voor technische wijzigingen in technische of operationele bedrijven

Zoals wordt beschreven in [Technische bedrijven en regels voor gegevenseigendom](engineering-org-data-ownership-rules.md), zijn de productgegevens die u kunt bewerken, afhankelijk van het type rechtspersoon waarin u werkt (een technisch bedrijf of een operationeel bedrijf). Regels voor gegevenseigendom worden ook toegepast op orders voor technische wijzigingen. Daarom kunnen verschillende typen wijzigingen worden aangebracht, afhankelijk van de rechtspersoon waar u een order voor technische wijzigingen maakt. Hieronder volgen een aantal voorbeelden:

- Voor orders voor technische wijzigingen in een *technisch bedrijf* kunt u fundamentele wijzigingen aanbrengen in de technische gegevens. U kunt bijvoorbeeld nieuwe versies van een product maken, de structuur van een product wijzigen via de stuklijst en waarden van technische kenmerken wijzigen. Selecteer voor elk betrokken product selecteert u een van de volgende waarden in het veld **Impact**:

    - **Geen**: werk de bestaande productversie bij (update in versie).
    - **Nieuwe versie**: maak een nieuwe versie op basis van de geselecteerde productversie.
    - **Nieuw product**: maak een volledig nieuw product dat is gebaseerd op de geselecteerde productversie.
    - **Nieuwe variant**: maak een nieuwe variant op basis van de geselecteerde productversie. De stuklijst- en routegegevens worden gekopieerd.

- Voor orders voor technische wijzigingen in een *operationeel bedrijf* kunt u de logistieke gegevens van het product wijzigen. U kunt bijvoorbeeld de bestaande stuklijst verrijken met instellingen voor sourcing, lokale routes of lokale stuklijsten toevoegen en zelfs een stuklijst verrijken door nieuwe stuklijst regels toe te voegen voor lokaal verpakkingsmateriaal, smeervloeistoffen of instructies in de lokale taal. Verrijkingen die gebruikers in het operationele bedrijf maken, blijven behouden wanneer nieuwe updates worden verzonden vanuit het technische bedrijf. Zie [Technische bedrijven en regels voor gegevenseigendom](engineering-org-data-ownership-rules.md) voor meer informatie.

    Wanneer orders voor technische wijzigingen in het technische bedrijf worden verwerkt, worden de producten alleen gemaakt en/of bijgewerkt in het technische bedrijf. Als de productmodelgegevens ook moeten worden bijgewerkt, moet u de producten dus ook vrijgeven aan de operationele bedrijven.

- U kunt producten rechtstreeks vanuit orders voor technische wijzigingen vrijgeven. Open de wijzigingsorder en selecteer in het actievenster op het tabblad **Wijzigingsorder** in de groep **Productreleases** de optie **Productstructuur vrijgeven**. Het proces werkt net zoals wanneer u producten vrijgeeft via de pagina **Vrijgegeven producten**. Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie.
- U kunt producten op basis van de volgende factoren automatisch laten vrijgeven vanuit orders voor technische wijzigingen:

    - Nieuwe releases naar bedrijven waar producten eerder zijn vrijgegeven. Selecteer **Zoeken** om alle eerdere versies te scannen en selecteer vervolgens **Weergeven** om de resultaten weer te geven. Op de pagina **Weergeven** worden de vorige productreleases weergegeven en u kunt opgeven welke producten u opnieuw wilt vrijgeven. Sluit vervolgens de pagina **Weergeven** en selecteer **Verwerken** om de geselecteerde producten opnieuw vrij te geven.
    - Instellingen voor automatische vrijgave in het besturingselement voor vrijgeven van de categorie voor technische producten. U kunt deze vrijgave uitvoeren als onderdeel van de werkstroom. Wanneer het blok **vrijgavevoorstel verzamelen** wordt gebruikt, wordt het vrijgavevoorstel gevuld met voorstellen voor hervrijgaven (zie het vorige lijstitem) en worden producten vrijgegeven aan bedrijven als het selectievakje **Automatisch vrijgeven** is ingeschakeld in het besturingselement voor vrijgeven van de categorie voor technische producten. U kunt **Weergeven** selecteren om de resultaten weer te geven, zoals wordt beschreven in het vorige lijstitem. De producten worden ook vrijgegeven wanneer het blok **vrijgavevoorstel verwerken** wordt gebruikt. Als u ervoor kiest alleen het vrijgavevoorstel als onderdeel van de werkstroom te verzamelen, kunt u de vrijgave handmatig starten door **Verwerken** te selecteren, zoals wordt beschreven in het vorige lijstitem.

## <a name="follow-up-on-an-engineering-change-request-via-an-engineering-change-order"></a>Een aanvraag voor een technische wijziging opvolgen via een order voor technische wijzigingen

Zodra een aanvraag voor een technische wijziging is goedgekeurd, kunt u deze opvolgen via een order voor technische wijzigingen. U kunt meerdere aanvragen voor technische wijzigingen combineren in één order voor technische wijzigingen. Eén order voor technische wijzigingen kan zelfs meerdere producten bevatten. (U gebruikt deze aanpak meestal wanneer dezelfde wijziging op meerdere producten moet worden toegepast.) U kunt echter niet meerdere orders voor technische wijzigingen maken op basis van één aanvraag voor een technische wijziging.

Als u een wijzigingsaanvraag wilt opvolgen via een wijzigingsorder, opent u de wijzigingsaanvraag en selecteert u in het actievenster op het tabblad **Wijzigingsorder** in de groep **Order voor technische wijziging** de optie **Koppeling en producten kopiëren**. U kunt vervolgens een bestaande order voor technische wijzigingen selecteren om aan de wijzigingsaanvraag te koppelen, maar u kunt ook een order voor technische wijzigingen maken voor die specifieke aanvraag.

## <a name="engineering-change-order-report"></a>Rapport Technische-wijzigingsorders

In rapporten over orders voor technische wijzigingen worden de wijzigingen beschreven die zijn aangebracht in een order voor technische wijzigingen. Deze zijn nuttig, zowel tijdens als na het revisie- en goedkeuringsproces.

Als u een rapport over orders voor technische wijzigingen wilt weergeven, opent u de relevante wijzigingsorder en selecteert u vervolgens in het actievenster op het tabblad **Wijzigingsorder** in de groep **Weergeven** de optie **Rapport over order voor wijzigingsorder**.

## <a name="fields-on-an-engineering-change-order"></a>Velden in een order voor technische wijzigingen

De meeste velden in orders voor technische wijzigingen zijn hetzelfde als de velden voor vrijgegeven producten, technische versies, documenten, stuklijsten (regels) en routes (bewerkingen). De velden in de volgende tabel zijn echter uniek voor wijzigingsorders.

| Veld | Beschrijving |
|---|---|
| Redenen voor technische wijzigingen | De reden voor het wijzigen van het betreffende product selecteren. |
| Beschrijving van de wijziging | Een omschrijving van de wijziging invoeren. |
| Vereiste speciale hulpmiddelen | Opgeven of speciale hulpmiddelen nodig zijn om de wijziging toe te passen. |
| Beschikking van technisch materiaal | Een materiaalbeschikkingscode selecteren voor afval dat wordt geproduceerd wanneer de wijziging wordt toegepast. |
| Goedkeuring van klant vereist | Opgeven of goedkeuring van de klant vereist is voordat de wijziging kan worden toegepast. |
| Goedkeuring van klant ontvangen | De status van de goedkeuring van de klant opgeven. |
| Gezonde werkomgeving en veiligheid | Opgeven of de regels voor een gezonde werkomgeving en veiligheid van toepassing zijn op de wijziging. Als dat zo is, kunt u de toepasselijke regels selecteren. |

Met de knop **Wijzigingsgegevens onderhouden/kopiëren** kunt u de wijzigingsgegevens kopiëren tussen producten waarin dit probleem optreedt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
