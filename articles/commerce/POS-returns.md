---
title: Retouren maken in POS
description: In dit artikel wordt beschreven hoe u retouren voor contante transacties of klantorders start in de toepassing Microsoft Dynamics 365 Commerce POS (Point of Sale).
author: hhainesms
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: a49e9abd0143d480cc1cafb05be5e995fb3cebdd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856993"
---
# <a name="create-returns-in-pos"></a>Retouren maken in POS

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u retouren voor contante transacties of klantorders start in de app Microsoft Dynamics 365 Commerce POS (Point of Sale).

> [!NOTE]
> In versie 10.0.20 en hoger van Commerce is een nieuwe functie met de naam **Uniforme retourverwerkingservaring in POS** beschikbaar. Deze functie biedt een consistenter en uniform retourproces in POS, ongeacht het transactietype (contante transactie of klantorder) of het oorspronkelijke kanaal waarin de order is gemaakt. Het wordt aangeraden dat alle organisaties deze nieuwe functie inschakelen om de algehele betrouwbaarheid van retourverwerking via POS te verbeteren.
>
> Nadat de functie is ingeschakeld, kan deze niet meer worden uitgeschakeld.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Retouren verwerken met de retourtransactiebewerking

Het is raadzaam om de retourtransactiebewerking toe te voegen aan de [schermindeling](pos-screen-layouts.md) van uw POS. In releases vóór de release van Commerce versie 10.0.20 ondersteunt de retourtransactiebewerking alleen de verwerking van retouren voor contante transacties op de juiste manier. Nadat u de functie **Uniforme retourverwerkingservaring voor POS** hebt ingeschakeld in Commerce versie 10.0.20 of hoger, ondersteunt de retourtransactiebewerking ook de verwerking van retouren die afkomstig zijn van klantorders, zoals "ophalen"- of "thuis laten bezorgen-orders" die reeds zijn gefactureerd.

Via de retourtransactiebewerking kunnen gebruikers zoeken naar een contante transactie of een klantorder waarvoor een retour moet worden uitgevoerd door een van de volgende vier zoekcriteria in te voeren. Gebruikers kunnen deze criteria invoeren met een apparaattoetsenbord, toetsenbord op het scherm of een streepjescodescanner.

- Ontvangstbewijs-ID
- Ordernummer
- Referentie-ID van kanaal (ook wel orderbevestigings-ID genoemd)
- Factuur-id

Als een transactie of order wordt gevonden die overeenkomt met de zoekcriteria, wordt de pagina **Retourneerbare producten** weergegeven. Hier kunnen gebruikers opgeven welke artikelen worden geretourneerd. Ze kunnen ook retourhoeveelheden en redencodes invoeren.

Voor elke orderregel in de lijst met retourneerbare producten wordt in POS informatie weergegeven over de oorspronkelijke inkoophoeveelheid en de hoeveelheden van eventuele retouren die eerder zijn verwerkt. De retourhoeveelheid die een gebruiker invoert voor een orderregel, moet kleiner zijn dan of gelijk zijn aan de waarde van het veld **Beschikbaar voor retour**.

![Pagina Retourneerbare producten.](media/returnslist.png)

Als een gebruiker tijdens de retourverwerking het fysieke product heeft en dat product heeft een streepjescode, kan de gebruiker de streepjescode scannen om de retour te registreren. Elke scan van de streepjescode verhoogt de retourhoeveelheid met één artikel. Als het streepjescodelabel echter een ingesloten hoeveelheid heeft, wordt die hoeveelheid ingevoerd in het veld **Nu retourneren**.

Gebruikers kunnen ook handmatig artikelen selecteren om te retourneren op de pagina **Retourneerbare producten** en vervolgens het veld **Nu retourneren** bijwerken met behulp van het detaildeelvenster aan de rechterkant.

Als de maximaal beschikbare hoeveelheid **Nu retourneren** wordt opgegeven voor een transactie, kan de gebruiker de bewerking **Alles selecteren** op de POS-appbalk selecteren om de maximale retourneerbare hoeveelheid in te stellen op alle regels.

Voor elke regel met een hoeveelheid **Nu retourneren** moet de gebruiker via het detaildeelvenster een redencode voor retour selecteren. Voor retouren van contante transacties worden de redencodes voor retouren geconfigureerd als informatiecodes in het functionaliteitsprofiel van de winkel. Voor retouren van klantorders worden de redencodes voor retouren geconfigureerd op de pagina **Redencodes retour** in Dynamics 365 Commerce Headquarters.

Nadat de retourhoeveelheid en redencode zijn ingesteld voor elk artikel dat moet worden geretourneerd, kan de gebruiker de bewerking **Retour** selecteren op de balk van de POS-app om door te gaan met de verwerking. De pagina van de POS-transactie wordt weergegeven, waar de retourneerbare artikelen die zijn geselecteerd op de vorige pagina, aan het winkelwagentje zijn toegevoegd. De hoeveelheden **Nu retourneren** voor de artikelen worden weergegeven als regels met een negatieve hoeveelheid op de transactie, en de totale terugbetaling wordt berekend.

Gebruikers kunnen regels aan een retourtransactie toevoegen als ze een ruilorder maken. Gebruikers kunnen ook meer ad-hoc retourartikelen aan een retourtransactie toevoegen door de bewerking **Product retourneren** te gebruiken voor een geselecteerde verkoopregel met een positieve hoeveelheid die is toegevoegd.

> [!NOTE]
> Met de bewerking **Product retourneren** in POS wordt geen validatie uitgevoerd voor oorspronkelijke transacties en kan elk product worden geretourneerd. Daarom is het raadzaam dat alleen geautoriseerde gebruikers deze bewerking mogen uitvoeren of dat een manager deze gegevens moet overschrijven als deze bewerking wordt gebruikt.

Als een restitutie tijdens afhandeling moet worden betaald, kunnen organisaties het [betalingsbeleid voor restituties](refund_policy_returns.md) configureren die de betalingsmethoden beperken die kunnen worden gebruikt om klanten terug te betalen. Als de oorspronkelijke transactie is betaald met een creditcard, kunnen gebruikers afhankelijk van de betalingsverwerker en de systeemconfiguratie, een [restitutie van de oorspronkelijke kaart uitgeven](dev-itpro/linked-refunds.md). In dit geval kan de restitutie worden verwerkt zonder dat de klant de creditcard opnieuw moet doorhalen. Het token van de oorspronkelijke betaling wordt gebruikt om de restitutie uit te geven.

## <a name="other-return-options-in-pos"></a>Overige retouropties in POS

Wanneer de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, kunnen gebruikers ook de bewerking **Journaal weergeven** in POS gebruiken om een retour te starten voor een contante transactie of een klantorder. Vervolgens kunnen ze een transactie in het journaal selecteren en vervolgens de bewerking **Retourneren** selecteren op de POS-appbalk. Deze bewerking is alleen beschikbaar als er retourneerbare regels op de order staan. Hiermee wordt dezelfde gebruikerservaring als de bewerking **Transactie retourneren** geïnitieerd.

Gebruikers kunnen ook de bewerking **Order intrekken** in POS gebruiken om klantorders te zoeken en in te trekken. (Deze bewerking kan niet worden gebruikt voor contante transacties). In dit geval kan nadat een klantorder is geselecteerd, de bewerking **Retourneren** op de POS-appbalk worden gebruikt om een retour voor de klantorder te initiëren. Deze bewerking is alleen beschikbaar als er retourneerbare regels op de order staan. Hiermee wordt dezelfde gebruikerservaring als de bewerking **Transactie retourneren** of **Journaal weergeven** geïnitieerd.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Retourorders worden als verkooporders naar Commerce Headquarters geboekt 

Wanneer de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, worden alle retouren die in POS worden gemaakt, naar Commerce Headquarters geschreven als verkooporders met negatieve regels. In releases vóór de release van Commerce versie 10.0.20 kunnen gebruikers selecteren of retourorders moeten worden geboekt als verkooporders met negatieve regels, of dat deze retourorders moeten zijn die worden gemaakt via het RMA-proces (Return Merchandise Authorization). 

In de functie **Uniforme retourverwerkingservaring in POS** is de optie afgeschaft om met het RMA-proces retouren in POS te maken. Nadat deze functie is ingeschakeld, worden alle retouren gemaakt als verkooporders met negatieve regels.

## <a name="offline-return-processing-improvements"></a>Verbeteringen in offline retourverwerking

In de meeste gevallen probeert het systeem wanneer een retour in POS wordt verwerkt, een RTS-aanroep (Real-time Service) uit te voeren naar Commerce Headquarters om de huidige hoeveelheden te valideren die beschikbaar zijn voor retour. Met deze validatie voorkomt u frauduleuze scenario's waarbij een klant hetzelfde artikel op meerdere locaties probeert te retourneren.

Voor de afhandeling van situaties waarin de RTS-aanroep niet kan worden uitgevoerd vanwege netwerk- of verbindingsproblemen, is er nu een proces om periodiek retourhoeveelheidgegevens van Commerce Headquarters te synchroniseren met de kanaaldatabase van een winkel. Deze tracering van retouren aan kanaalzijde zorgt ervoor dat de hoeveelheden **Beschikbaar voor retour** die in het POS worden weergegeven, redelijk nauwkeurig zijn, zelfs wanneer POS offline is. Daarnaast wordt ervoor gezorgd dat POS de kanaalgegevens kan blijven valideren om frauduleuze retouren te voorkomen.

Om het offline retourproces op de juiste manier te gebruiken, moeten organisaties de batchtaak **Retourhoeveelheden bijwerken** plannen in Commerce Headquarters, zodat deze vaak wordt uitgevoerd. Het wordt aangeraden deze taak met dezelfde frequentie uit te voeren als de P-taak waarmee nieuwe transacties vanuit Commerce-kanalen naar Commerce Headquarters worden gehaald.

Met de taak **Retourhoeveelheden bijwerken** wordt de hoeveelheid berekend die beschikbaar is voor retour voor alle verkooporders die in Commerce Headquarters zijn gevonden. De gegevens die met de taak worden berekend, moeten vervolgens worden verzonden naar kanaaldatabases, zodat de winkelkanalen kunnen worden bijgewerkt. De distributietaak **Retourhoeveelheden** (1200) wordt hiervoor gebruikt. Omdat gegevens over de retourneerbare hoeveelheid worden gesynchroniseerd vanuit Commerce Headquarters, kan, als een retour in POS wordt verwerkt maar de RTS-aanroep niet kan worden uitgevoerd, de informatie over retouren aan de kanaalzijde worden gebruikt om de hoeveelheden **Beschikbaar voor retour** voor een bepaalde verkoopregel te valideren.

Wanneer RTS-aanroepen niet kunnen worden uitgevoerd en POS kanaalgegevens voor retourvalidatie gebruikt, meldt een waarschuwingsbericht gebruikers dat ze een 'offline' retour maken. Daardoor zijn de gebruikers zich ervan bewust dat de hoeveelheid **Beschikbaar voor retour** die in POS wordt weergegeven, mogelijk verouderd en niet meer nauwkeurig is, afhankelijk van de vraag wanneer de taak **Retourhoeveelheden bijwerken** voor het laatst is verwerkt en gesynchroniseerd met het kanaal.

Een klant heeft bijvoorbeeld onlangs een retour voor een orderregel in een ander kanaal verwerkt, maar die gegevens zijn nog niet gesynchroniseerd met de kanaaldatabases via de taak **Retourhoeveelheden bijwerken**. De klant gaat vervolgens naar een andere winkel en probeert hetzelfde artikel opnieuw te retourneren. Als de winkel in dat geval geen RTS-aanroep naar Commerce Headquarters kan uitvoeren om real-time retourgegevens op te halen, staat POS toe dat het artikel opnieuw wordt geretourneerd. De gebruiker wordt echter gewaarschuwd dat de gegevens die worden gebruikt om de retour te valideren, mogelijk verouderd zijn. Het bericht dat de gebruiker ontvangt, is slechts een waarschuwingsbericht. Dit neemt niet weg dat de gebruiker de retour nog steeds kan verwerken.

Als de informatie aan de kanaalzijde om de een of andere reden niet is bijgewerkt en als een offline retour wordt verwerkt voor een hoeveelheid die groter is dan de werkelijke hoeveelheid **Beschikbaar voor retour**, wordt er mogelijk een fout gegenereerd wanneer een overzichtsboeking wordt uitgevoerd om de transactie te maken in Commerce Headquarters.

> [!NOTE]
> Wanneer de functie **Uniforme retourverwerkingservaring in POS** is ingeschakeld, zijn nieuwe optionele functies beschikbaar die ondersteuning bieden voor de validatie van geserialiseerde productretouren. Zie [Producten met serienummers retourneren in POS (Point of Sale)](POS-serial-returns.md) voor meer informatie.

## <a name="version-details"></a>Versiegegevens

De volgende lijst bevat de minimale versievereisten voor de verschillende componenten.
- Commerce Headquarters: versie 10.0.20
- Commerce Scale Unit (CSU): versie 9.30
- Point of sale (POS): versie 9.30

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen

Deze functie zorgt ervoor dat wanneer een order wordt geretourneerd met meerdere facturen, de btw uiteindelijk gelijk is aan het oorspronkelijke aangerekende btw-bedrag.

1. Zoek in het werkgebied **Functiebeheer** naar **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen**.
1. Selecteer de optie **De correcte belastingberekening voor retouren met gedeeltelijke hoeveelheid inschakelen** en selecteer vervolgens **Inschakelen**.

## <a name="set-up-return-locations-for-retail-stores"></a>Retourlocaties voor detailhandelwinkels instellen

In Commerce kunt u retourlocaties instellen die op detailhandelsinfocodes en verkoop- en marketingredencodes zijn gebaseerd. Wanneer een klant een aankoop retourneert, geeft de kassier vaak de reden voor de retour aan. U kunt opgeven dat geretourneerde producten aan verschillende retourlocaties in voorraad worden toegewezen, gebaseerd op de informatie- en redencodes die de kassier selecteert op de POS-kassa.

Stel dat een klant een defect product retourneert en de kassamedewerker de retourtransactie verwerkt. Wanneer in Retail POS de informatiecode voor retouren wordt toont, selecteert de kassier de subcode voor een retour wegens defect. Het geretourneerde product wordt vervolgens automatisch toegewezen aan een specifieke retourlocatie.

Een retourlocatie kan een winkel, een magazijn, een locatie in een magazijn of zelfs een bepaalde pallet zijn, afhankelijk van de voorraadlocaties die uw organisatie heeft ingesteld. U kunt elke retourlocatie koppelen aan een of meer infocodes voor detailhandel en redencodes voor sales en marketing.

### <a name="prerequisites"></a>Vereisten

Voordat u retourlocaties kunt instellen, moet u de volgende elementen instellen:

- **Infocodes detailhandel**: Prompts op de POS-kassa die worden ingesteld in de module **Detailhandel**. Meer informatie over dit onderwerp vindt u in [Infocodes instellen](/dynamicsax-2012/appuser-itpro/setting-up-info-codes).
- **Verkoop- en marketingredencodes**: Prompts op de POS-kassa die worden ingesteld in de module **Verkoop en marketing**. Meer informatie over dit onderwerp vindt u in [Redencodes instellen](/dynamicsax-2012/appuser-itpro/set-up-return-reason-codes).
- **Voorraadlocaties**: De plaatsen waar de voorraad wordt bewaard. Meer informatie over dit onderwerp vindt u in [Voorraadlocaties instellen](/dynamicsax-2012/appuser-itpro/about-locations).
    
### <a name="set-up-return-locations"></a>Retourlocaties instellen

Voer de onderstaande stappen uit om retourlocaties in te stellen.

1. Ga naar **Retail en handel \> Afzetkanaalinstellingen \> Magazijnen** en selecteer een magazijn
1. Selecteer op het sneltabblad **Retail** in het veld **Standaardlocatie voor retournering** de voorraadlocatie die u wilt gebruiken voor retouren waarvoor de infocodes of redencodes niet zijn toegewezen aan retourlocaties.
1. Selecteer in het veld **Standaardretourpallet** de pallet die u wilt gebruiken voor retouren waarvoor de infocodes of redencodes niet zijn toegewezen aan retourlocaties.
1. Ga naar **Retail en Commerce \> Voorraadbeheer \> Retourlocaties**.
1. Selecteer **Nieuw** om een nieuwe beleidsregel voor retourlocaties te maken.
1. Geef een unieke naam en een omschrijving op voor de retourlocatie.

    > [!NOTE]
    > De naam wordt automatisch ingevuld als een nummerreeks voor retourlocaties is ingesteld.

1. Ga naar het sneltabblad **Algemeen** en stel de optie **Etiketten afdrukken** in op **Ja** als u etiketten wilt laten afdrukken voor alle producten die worden toegewezen aan retourlocaties.
1. Stel de optie **Voorraad blokkeren** in op **Ja** om de geretourneerde producten in de standaardretourlocatie uit voorraad te nemen en te voorkomen dat ze worden verkocht.
1. U stelt als volgt specifieke retailinfocodes en -subcodes in voor retourlocaties:

    1. Selecteer op het sneltabblad **Infocodes detailhandel** de optie **Toevoegen**.
    1. Selecteer een infocode voor retouren in het veld **Infocode**.
    1. Selecteer in het veld **Subcode** de subcode voor de reden van retour. In het veld **Beschrijving** wordt de beschrijving voor de geselecteerde subcode getoond.
    1. Selecteer in het veld **Winkel** de winkel waar de infocode wordt gebruikt.
    1. In de velden **Magazijn**, **Locatie** en **Pallet-id** kunt u een retourlocatie opgeven. Om bijvoorbeeld een bepaalde locatie in een winkel op te geven, selecteert u de winkel in het veld **Winkel** en een locatie in het veld **Locatie**.
    1. Schakel het selectievakje **Voorraad blokkeren** in om geretourneerde producten uit voorraad te nemen en te voorkomen dat ze worden verkocht.

1. U stelt als volgt specifieke verkoop- en marketingcodes in voor retourlocaties:

    1. Selecteer op het sneltabblad **Redencodes verkoop en marketing** de optie **Toevoegen**.
    1. Selecteer vervolgens in het veld **Redencode** een redencode voor retouren. In het veld **Beschrijving** wordt de beschrijving voor de geselecteerde redencode getoond.
    1. Selecteer in het veld **Winkel** de winkel waar de redencode wordt gebruikt.
    1. In de velden **Magazijn**, **Locatie** en **Pallet-id** kunt u een retourlocatie opgeven. Om bijvoorbeeld een pallet op een locatie in een magazijn op te geven, selecteert u een magazijn in het veld **Magazijn**, een locatie in het veld **Locatie** en een pallet in het veld **Pallet-id**.
    1. Schakel het selectievakje **Voorraad blokkeren** in om geretourneerde producten uit voorraad te nemen en te voorkomen dat ze worden verkocht.

    > [!NOTE]
    > Als een retourlocatiebeleid wordt gebruikt voor een artikel maar de retourreden die een kassier selecteert niet overeenkomt met een code die is opgegeven in het sneltabblad **Informatiecodes detailhandel** of **Redencodes verkoop en marketing**, wordt het artikel naar de standaard retourlocatie gezonden die is gedefinieerd op de pagina **Magazijn**. Daarnaast bepaalt de instelling van het selectievakje **Voorraad blokkeren** op het sneltabblad **Algemeen** van de pagina **Retourlocaties** of voorraad van het geretourneerde artikel moet worden geblokkeerd.

1. Ga naar **Retail en handel \> Handelproducthiërarchie**.
1. Selecteer op het sneltabblad **Eigenschappen voorraadcategorie beheren** een retourlocatie in het veld **Retourlocatie**. Aangezien voor dezelfde winkel meerdere beleidsregels voor retourlocaties kunnen worden gedefinieerd, bepaalt de waarde die u hier selecteert welke beleidsregel voor retourlocaties wordt gebruikt.

## <a name="additional-resources"></a>Aanvullende bronnen

[Producten met serienummers retourneren in POS (Point of Sale)](POS-serial-returns.md)

[Gekoppelde restituties van eerder goedgekeurde en bevestigde transacties](dev-itpro/linked-refunds.md)

[Beleid voor retouren en restituties voor een afzetkanaal maken en bijwerken](refund_policy_returns.md)

[Weergaveconfiguraties van POS-gebruikersinterface](pos-screen-layouts.md)
