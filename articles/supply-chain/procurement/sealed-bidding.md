---
title: Verzegelde biedingen voor offerteaanvragen
description: In dit onderwerp wordt beschreven hoe u verzegelde biedingen kunt instellen om antwoorden op offertes van leveranciers geheim te houden totdat deze worden ontgrendeld door inkooppersoneel.
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578075"
---
# <a name="sealed-bidding-for-rfqs"></a>Verzegelde biedingen voor offerteaanvragen

[!include [banner](../includes/banner.md)]

Met verzegelde biedingen kunt u antwoorden op offertes van leveranciers geheim houden totdat deze worden ontgrendeld door inkooppersoneel. Alle biedingen die betrekking hebben op een offerteaanvraag worden pas ontzegeld bij het vervallen van het bod. Voordat een bieding wordt ontgrendeld, hebben alleen gebruikers toegang die specifieke gebruikersrollen hebben en die de leverancier vertegenwoordigen.

> [!IMPORTANT]
> Formulieren wijzigen of uitbreiden of nieuwe formulieren of bedrijfslogica maken, kan de bescherming omzeilen die Microsoft biedt voor verzegelde biedingen. U draagt het risico van het gebruik van wijzigingen, uitbreidingen, nieuwe formulieren of bedrijfslogica, of het onvermogen om de functie voor verzegelde biedingen te gebruiken als gevolg van dergelijke wijzigingen, extensies, nieuwe formulieren of bedrijfslogica.  Microsoft is niet verantwoordelijk voor enige schade die voortvloeit uit enige wijziging of uitbreiding van formulieren, of uit nieuwe formulieren of bedrijfslogica die u maakt of die derden voor u maken. Microsoft biedt geen technische of andere ondersteuning voor wijzigingen, uitbreidingen, nieuwe formulieren of bedrijfslogica die door u of door derde partij namens u zijn aangebracht. U bent al enige verantwoordelijk voor het voldoen aan alle toepasselijke wet- en regelgeving met betrekking tot verzegelde biedingen.

## <a name="how-bids-are-kept-secure"></a>Hoe biedingen worden beveiligd

Bij verzegelde biedingen wordt asymmetrische codering gebruikt om de coderingssleutel (KEK) van de bieding te coderen en symmetrisch codering om de feitelijke bieding te coderen. Het systeem kan worden geïntegreerd met de Microsoft Azure Key Vault om de coderingssleutels te genereren en te beheren die worden gebruikt om verzegelde biedingen te coderen. Elke bieding heeft een eigen coderingssleutel. Deze codering wordt veilig bewaard in een sleutelkluis die het eigendom is van de organisatie die Dynamics 365 Supply Chain Management uitvoert. Het systeem gebruikt de sleutelkluis op aanvraag wanneer codering en decodering zijn vereist.

## <a name="setup-and-configuration"></a>Instellingen en configuratie

In dit gedeelte worden de vereisten beschreven waaraan moet worden voldaan voordat u offerteaanvragen kunt verzenden waarvoor verzegelde bieding moet worden gebruikt.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Stap 1: Gebruikerstoegang instellen voor verzegeld bieden

Wanneer u verzegeld bieden gebruikt, kunnen alleen gebruikers die zijn ingesteld als contactpersoon voor een leverancier, biedingen voor die leverancier weergeven, bewerken en indienen totdat de biedingsperiode verloopt. Deze gebruikers moeten de rol **Leverancier (extern)** hebben en ze moeten worden ingesteld als contactpersoon voor de leveranciersrekening. De contactpersoon moet ook over een machtiging voor samenwerking met leveranciers hebben, zoals beschreven in [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).

Omdat gebruikers die over de juiste machtigingen beschikken en zijn ingesteld als contactpersonen voor de leverancier, toegang hebben tot de verzegelde biedingen voor een leverancier, is het belangrijk om bij te houden wie die gebruikers zijn. De systeembeheerder die gebruikers en beveiligingsrollen instelt, is verantwoordelijk voor het beperken van de toegang tot verzegelde biedingen tot die gebruikers die deze daadwerkelijk kunnen bekijken.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>Stap 2: De functie voor verzegelde biedingen inschakelen

Voordat u deze functie instelt of gebruikt, moet u controleren of deze beschikbaar is in uw systeem. Beheerders kunnen het werkgebied **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** gebruiken om de status van de functie te controleren en de functie desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Inkoopbeheer*
- **Functienaam:** *Verzegelde bieding voor offerteaanvraag*

### <a name="step-3-set-up-azure-key-vault"></a>Stap 3: De Azure Key Vault instellen

Supply Chain Management gebruikt coderingssleutels om alle verzegelde biedingen te beschermen en ze geheim te houden tot de juiste tijd. Hierbij wordt gebruikgemaakt van de mogelijkheden van Key Vault om de vereiste sleutels te genereren en te beheren. U moet daarom een verbinding instellen vanuit Supply Chain Management naar een sleutelkluis om het systeem in te schakelen.

> [!IMPORTANT]
> De belangrijkste sleutelkluizen die u voor verzegelde biedingen gebruikt, moeten aan de volgende vereisten voldoen:
>
> - Als u een sandbox gebruikt voor ontwikkelen en testen, moet u één toegewezen sleutelkluis voor de sandbox hebben en een afzonderlijke kluis voor productie.
> - Elke sleutelkluis moet worden gemaakt in een Azure-abonnement dat eigendom is van uw organisatie (niet het abonnement waarin u Supply Chain Management uitvoert).
> - Elke sleutelkluis moet uitsluitend voor verzegelde biedingen worden gebruikt. U moet uw sleutelkluizen voor verzegelde biedingen niet voor andere doeleinden gebruiken.

Elke bieding haalt een eigen sleutel op. Deze sleutel wordt gebruikt telkens als een gebruiker de bieding bekijkt, bijwerkt of de bieding ontgrendelt.

Met Key Vault wordt de sleutel gegenereerd die wordt gebruikt om het geheim op te halen wanneer de leverancier **Bieding** selecteert in de interface voor leverancierssamenwerking. De sleutel vervalt vervolgens na een bepaalde tijd die de inkoopmanager op de pagina **Parameters voor inkoopbeheer** in Supply Chain Management heeft ingesteld. Nadat de sleutel is verlopen, kan niemand de bieding bekijken, bewerken of ontgrendelen. Het is daarom belangrijk dat u configureert wanneer sleutels vervallen, zodat er voldoende tijd is om het biedingsproces te voltooien.

In de volgende drie stappen stelt u de verbinding met Key Vault in. Eerst stelt u een sleutelkluis in die moet worden gebruikt bij verzegelde biedingen. Vervolgens configureert u Supply Chain Management om te communiceren met de sleutelkluis. Tot slot stelt u de vervaltijd voor de sleutel in.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Stap 4: Een sleutelkluis instellen die moet worden gebruikt bij verzegelde biedingen

Ga als volgt te werk om uw sleutelkluis in te stellen. De volgorde van de stappen is belangrijk.

1. Als u nog geen Azure-abonnement hebt ingesteld dat los staat van het abonnement waarin u Supply Chain Management uitvoert, stelt u dit in.
1. Stel een sleutelkluis in uw afzonderlijke Azure-opslag in. Zie [Azure Key Vault-opslag](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage) voor meer informatie.
1. Stel de Supply Chain Management-app zo in dat deze werkt als een client voor uw sleutelkluis. Zie [Azure Key Vault-client instellen](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client) voor meer informatie.

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Stap 5: Key Vault-parameters configureren in Supply Chain Management

Volg deze stappen om Supply Chain Management te configureren voor communicatie met de sleutelkluis tijdens verzegeld bieden.

1. Meld u aan bij Supply Chain Management en ga naar **Systeembeheer \> Instellen \> Parameters voor sleutelkluis**.
1. Selecteer **Nieuw** om een record te maken en stel de volgende velden voor de record in:

    - **Naam**: voer een naam in.
    - **Beschrijving**: voer een beschrijving in.
    - **URL sleutelkluis**: geef de standaard URL voor uw sleutelkluis op.
    - **Client sleutelkluis**: geef de interactieve client-id op van de Active Directory-toepassing die voor verificatie aan de sleutelkluis is gekoppeld.
    - **Geheime sleutel sleutelkluis**: voer de geheime verwijzing voor het certificaat in.
    - **Ingeschakeld voor verzegeld bieden**: stel deze optie in op *Ja*.

![Pagina Parameters voor sleutelkluis](media/sealed-bidding-key-vault-param.png "Pagina Parameters voor sleutelkluis")

> [!NOTE]
> U kunt slechts één sleutelkluisconfiguratie tegelijk inschakelen voor verzegeld bieden. Voordat u een bestaande sleutelkluisconfiguratie uitschakelt, moet u controleren of alle verzegelde biedingen die deze configuratie gebruiken, niet zijn vergrendeld. Controleer alle offerteaanvragen van het type *Vergrendeld* en controleer of alle antwoorden hierop niet zijn vergrendeld.

### <a name="step-6-set-the-key-expiration-time"></a>Stap 6: De vervaltijd van de sleutel instellen

Volg deze stappen om de vervaltijd in te stellen die wordt toegepast op de sleutel die voor elke nieuwe bieding is gegenereerd.

1. Ga naar **Parameters voor inkoopbeheer \> Instellen \> Parameters voor inkoopbeheer**.
1. Geef op het tabblad **Offerteaanvraag** in het veld **Dagen offset** het aantal dagen op voor de duur van de offerteaanvraag. Wanneer een offerteaanvraag wordt gemaakt, wordt het aantal dagen dat u hier invoert, toegevoegd aan de systeemdatum om de standaardvervaldatum voor de offerteaanvraag te definiëren.
1. Voer in het veld **Vervaldatum offset coderingssleutel** het aantal dagen in dat elke coderingssleutel geldig moet zijn nadat deze is uitgegeven. Nadat de coderingssleutel is verlopen, kan niemand de bieding meer bekijken of de verzegelde bieding die de sleutel gebruikt, ontgrendelen.

> [!TIP]
> De waarde van het veld **Vervaldatum offset coderingssleutel** mag niet minder zijn dan de waarde van het veld **Dagen offset**.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Stap 7: Het standaardbiedingstype instellen

Elke offerteaanvraagcase heeft een biedingstype. Het biedingstype bepaalt of die offerteaanvraagcase het een open of verzegelde bieding is.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Offerteaanvraagcases die geen sollicitatietype hebben

Volg deze stappen om het standaardbiedingstype in te stellen dat is toegewezen aan nieuwe offerteaanvraagcases waaraan geen sollicitatietype is toegewezen wanneer deze worden gemaakt.

1. Ga naar **Parameters voor inkoopbeheer \> Instellen \> Parameters voor inkoopbeheer**.
1. Stel op het tabblad **Offerteaanvraag** het veld **Biedingstype** in op *Verzegeld*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Offerteaanvraagcases die een sollicitatietype hebben

Volg deze stappen om het standaardbiedingstype in te stellen dat is toegewezen aan nieuwe offerteaanvraagcases waaraan geen sollicitatietype is toegewezen wanneer deze worden gemaakt.

1. Ga naar **Inkoopbeheer \> Instellen \> Offerteaanvraag \> Sollicitatietype**.
1. Maak een nieuw sollicitatietype of selecteer een bestaand sollicitatietype waarvoor u het biedingstype *Verzegeld* wilt gebruiken.
1. Stel het veld **Biedingstype** in op *Verzegeld*.
1. Herhaal deze stappen voor elk extra sollicitatietype waarvoor u verzegelde bieding wilt implementeren.

> [!TIP]
> Een sollicitatietype hoeft niet te worden toegewezen wanneer er een nieuwe offerteaanvraag wordt gemaakt. Als er een sollicitatietype is toegewezen, kan het standaardbiedingstype van een offerteaanvraag dit type ophalen. Anders kan het standaardsollicitatietype worden gebruikt dat is gedefinieerd in Parameters voor Inkoopbeheer.

## <a name="the-sealed-bidding-process"></a>Het proces voor verzegelde biedingen

Met Verzegelde biedingen doorloopt u bijna hetzelfde proces als het proces dat wordt beschreven in [Overzicht van Offerteaanvragen](request-quotations.md). Het belangrijkste verschil is dat de biedingsgegevens en de bijbehorende bijlagen worden gecodeerd totdat de bieding wordt ontgrendeld.

> [!IMPORTANT]
> [Vragenlijsten](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) worden niet versleuteld en mogen niet worden gebruikt om gevoelige informatie te verzamelen

Hier volgt een overzicht van het proces:

1. U maakt een offerteaanvraag en verzendt de aanvraag naar een of meer leveranciers.
1. Leveranciers reageren door hun verzegelde bieding in te dienen.
1. U ontgrendelt de biedingen nadat de vervaldatum voor de invoer van biedingen is verstreken.
1. De biedingen worden zichtbaar en u kunt ze beoordelen en vergelijken.
1. Nadat een bieding is geaccepteerd, genereert u een inkooporder, genereert u een inkoopovereenkomst of werkt u een opdracht tot inkoop bij.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Een offerteaanvraagcase maken waarvoor verzegelde bieding wordt gebruikt

Het proces van het maken van een offerteaanvraag voor verzegelde biedingen is bijna hetzelfde als het proces voor niet-verzegelde biedingen. Zie [Een offerteaanvraag maken](tasks/create-request-quotation.md) voor informatie over het maken van beide typen offerteaanvraagcases. In dit gedeelte sectie komen een aantal belangrijke overwegingen aan de orde bij het maken van een offerteaanvraag voor verzegelde biedingen.

Offerteaanvraagcases voor verzegelde biedingen moet voor **Biedingstype** de waarde *Verzegeld* hebben. U kunt deze waarde op drie manieren aan een offerteaanvraagcase toewijzen:

- Stel de waarde rechtstreeks in op de offerteaanvraagcase nadat u deze hebt gemaakt.
- Definieer verzegelde bieding als het standaardbiedingstype voor alle offerteaanvraagcases in de parameters voor Inkoopbeheer. (Zie het gedeelte [Het standaardbiedingstype instellen](#set-default-bid-type) eerder in dit onderwerp.)
- Wanneer u een nieuwe offerteaanvraagcase maakt, selecteert u een sollicitatietype dat is ingesteld voor verzegeld bieden. (Zie het gedeelte [Het standaardbiedingstype instellen](#set-default-bid-type).)

Aan de hand van de waarde van **Vervaldatum en -tijd** voor verzegeld bieden wordt bepaald wanneer de ingediende biedingen kunnen worden ontgrendeld. De waarde van **Vervaldatum en -tijd** op elke regel komt overeen met de waarde in de koptekst.

U kunt het biedingstype niet wijzigen nadat een offerteaanvraagcase is verzonden.

### <a name="vendors-respond-to-an-rfq"></a>Leveranciers reageren op een offerteaanvraag

Leveranciers die op een verzegelde bieding reageren, gebruiken dezelfde procedure als de procedure die zij gebruiken om te reageren op openstaande biedingen, zoals wordt uitgelegd in [Werken met offerteaanvragen in het werkgebied voor biedingen van de leverancier](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Zie [Biedingen op offerteaanvragen en toegekende contracten invoeren en vergelijken](tasks/enter-compare-rfq-bids-award-contracts.md) voor gedetailleerde instructies over het werken met openstaande en verzegelde biedingen. Het enige verschil tussen de verwerking van verzegelde biedingen en het verwerken van openstaande biedingen is dat inkoopprofessionals een verzegelde bieding van een leverancier pas kunnen openen als de biedingsperiode is verstreken. Alleen een contactpersoon voor de leverancier kan de verzegelde bieding van die leverancier openen.

> [!IMPORTANT]
> Voor verzegelde biedingen kunnen leverancier bijlagen alleen in de PDF-indeling uploaden. Andere indelingen worden niet geaccepteerd.

Nadat een geregistreerde gebruiker van een leverancier **Bieding** selecteert op een verzegelde bieding voor een offerteaanvraag, kan de gebruiker de biedingsgegevens invoeren. Deze gegevens worden veilig bewaard. Leveranciers kunnen hun werk opslaan terwijl ze een bieding voorbereiden, zo vaak als nodig is terugkeren naar de bieding en de bieding vervolgens indienen wanneer deze klaar is. Leveranciers kunnen hun bieding ook weergeven nadat ze deze hebben ingediend. Als leveranciers hun bieding moeten wijzigen nadat ze deze hebben ingediend, kunnen ze de bieding intrekken, bijwerken en op elk gewenst moment opnieuw indienen totdat de biedingsperiode is verstreken.

De volgende voorwaarden zijn van toepassing tijdens verzegeld bieden:

- Tijdens verzegeld bieden maakt het systeem een journaal voor een *Offerteaanvraag*.
- Wanneer een leverancier een bieding indient, worden er offerteaanvraagjournalen zonder regels gemaakt met een verzegelde prijs.
- Nadat de case is ontgrendeld, worden er offerteaanvraagjournalen gemaakt met een prijs en een bedrag. U kunt dit journaal openen door **Offerteaanvraagjournalen** te selecteren op de pagina **Alle aanvragen voor offertes**.
- Het systeem slaat een logboek op van elke actie die gebruikers uitvoeren op een verzegelde bieding. Deze acties omvatten het weergeven, bewerken en opslaan van de bieding. Dit logboek is zichtbaar voor de leverancier en voor inkoopprofessionals die toegang hebben tot de bieding.
- Inkoopprofessionals kunnen tijdens de verwerking van de bieding de status bekijken. De status is *Leverancier is bezig met bijwerken* of *Ingediend door leverancier*.
- De status van de regels in een verzegelde bieding blijft *Verzonden* totdat de bieding wordt ontgrendeld.
- Als de leverancier een bieding wil afwijzen, wordt de status van de bieding **Voortgang van reactie** of *Afgewezen door leverancier*. Deze status is zichtbaar voor inkoopmedewerkers.
- Antwoorden in vragenlijsten worden **niet** in gecodeerde vorm in de database opgeslagen. Daarom zijn ze niet verzegeld. Ze zijn pas zichtbaar in de gebruikersinterface van de offerteaanvraag wanneer de case wordt ontgrendeld.

### <a name="all-sealed-bid-activities-are-logged"></a>Alle verzegelde biedingsactiviteiten worden vastgelegd.

In een gedetailleerd logboek worden alle gebruikersactiviteiten en -acties voor een bieding geregistreerd. Met het activiteitenlogboek kunnen organisaties bepalen wie een bieding gedurende de levensduur heeft bijgewerkt en wat er is bijgewerkt. Organisaties kunnen hiermee ook bevestigen dat alleen geautoriseerde personen een verzegelde bieding hebben geopend. Het activiteitslogboek is beschikbaar op de pagina **Activiteit** van elke bieding.

### <a name="review-rfq-activity"></a>Activiteit in de offerteaanvraag controleren

Elke interactie met de bieding wordt vastgelegd en kan worden weergegeven op de pagina **Activiteit**. In de volgende afbeelding ziet u een voorbeeld.

![Voorbeeld van de pagina Activiteit](media/sealed-bidding-rfq-activity.png "Voorbeeld van de pagina Activiteit")

Leveranciers kunnen de pagina **Activiteit** openen door **Activiteit** te selecteren op de pagina **Verzegelde bieding voor offerteaanvraag**. Inkoopmedewerkers hebben toegang tot deze optie door **Activiteit** op de pagina **Offerteaanvraag** te selecteren. Het activiteitenlogboek biedt volledige zichtbaarheid voor leveranciers en voor de inkoopmedewerkers die toegang hebben tot de bieding. Op deze manier kan aan het licht worden gebracht of er iemand ongeoorloofd toegang heeft verkregen.

### <a name="unseal-sealed-bids"></a>Verzegelde biedingen ontgrendelen

Wanneer de waarde **Vervaldatum en -tijd** die voor een verzegelde bieding voor een offerteaanvraag is geconfigureerd, is verstreken, is de knop **Ontgrendelen** beschikbaar. Selecteer **Ontgrendelen** om alle biedingen voor de offerteaanvraagcase te ontgrendelen. Alle biedingsgegevens en bijlagen worden nu zichtbaar zodat antwoorden op de case kunnen worden beheerd. Daarnaast worden er journalen gemaakt die de ingediende biedingsgegevens bevatten.

De ontgrendeling wordt vastgelegd en kan worden weergegeven op de pagina **Activiteit**.

### <a name="process-accepted-bids"></a>Geaccepteerde biedingen verwerken

Het proces van het vergelijken en goedkeuren van eerder verzegelde biedingen is hetzelfde als het proces voor openstaande biedingen. Zie [Offerteaanvraagbiedingen invoeren en vergelijken en contracten toekennen](tasks/enter-compare-rfq-bids-award-contracts.md) voor informatie over het scoren, vergelijken, afwijzen en accepteren van niet-verzegelde biedingen.

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Het activiteitenlogboek voor de offerteaanvraag kan nooit worden verwijderd

Het activiteitenlogboek voor de offerteaanvraag kan door niemand worden bewerkt of verwijderd, zelfs niet door beheerders en Microsoft Ondersteuning. Deze beperking zorgt ervoor dat het proces van het verzegeld bieden eerlijk verloopt. Bovendien zorgt deze beperking ervoor dat er een nauwkeurige audittrail wordt bijgehouden.
