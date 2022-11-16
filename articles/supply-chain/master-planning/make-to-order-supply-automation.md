---
title: Aanbodautomatisering voor maken-naar-order
description: In dit artikel wordt beschreven hoe u de verschillende verbeteringen kunt instellen en gebruiken die zijn toegevoegd door de functie voor het automatiseren van maken-naar-order.
author: t-benebo
ms.date: 07/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-27
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d376c2f4d8514a4e6122e2e94455d57a39d2babf
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740189"
---
# <a name="make-to-order-supply-automation"></a>Aanbodautomatisering voor maken-naar-order

[!include [banner](../includes/banner.md)]

De functie *Aanbodautomatisering voor maken-naar-order* voegt verschillende verbeteringen toe aan Microsoft Dynamics 365 Supply Chain Management. Met deze verbeteringen kunt u de volgende taken uitvoeren:

- De capaciteitsbelasting van resources voor een door de gebruiker gedefinieerde periode weergeven zodat de capaciteitsbelasting op lange termijn kan worden geëvalueerd.
- Flexibiliteit verbeteren door de vertragingstolerantie (negatieve dagen) voor elke hoofdplanning te beheren.
- Zorgen dat producten beschikbaar zijn voor orders van het laatste moment en het gebruik van bestaande voorraad optimaliseren door het laatst mogelijke aanbod met een reeks voor tracering van de behoefte te koppelen aan een vraag in plaats van het eerst mogelijke aanbod te gebruiken.
- Componenttoewijzing flexibel houden voor productieorders na fiattering, wat ervoor zorgt dat het systeem wordt geoptimaliseerd voor wijzigingen in de vraag van het laatste moment. Markering kan met andere woorden tot één niveau worden beperkt.
- Afhandelingsbeleid voor elke verkooporder beheren. De standaardinstellingen worden overgenomen uit de instellingen van de klant.
- De intercompany-gegevensstroom verbeteren. Inkooporders worden bijgewerkt om velden op te nemen voor de leveringsmodus, leveringsvoorwaarden en extern artikelnummer. Door deze wijziging wordt gegarandeerd dat gedetailleerde vraaggegevens naar het leverende bedrijf stromen.

In dit artikel wordt beschreven hoe elke verbetering in wordt gesteld en wordt gebruikt.

## <a name="turn-on-the-make-to-order-supply-automation-feature"></a>Inschakelen van de aanbodautomatiseringsfunctie voor maken naar order

Voordat u de in dit artikel beschreven functie kunt gebruiken, moet u deze voor het systeem inschakelen. Beheerders kunnen de werkruimte [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken, waar de functie op de volgende manier wordt weergegeven:

- **Module:** *Hoofdplanning*
- **Naam functie:** *Aanbodautomatisering voor maken naar order*

## <a name="set-the-number-of-days-to-show-on-capacity-load-page"></a>Het aantal dagen instellen dat moet worden weergegeven op de pagina Capaciteitsbelasting

Met de pagina **Capaciteitsbelasting** kunt u de beschikbare capaciteit van een resource controleren. De functie *Aanbodautomatisering voor maken-naar-order* verbetert de pagina **Capaciteitsbelasting** door een veld **aantal dagen** toe te voegen. U kunt dit veld gebruiken om het aantal dagen te beperken dat het raster **Overzicht** laat zien. De waarde die u instelt, wordt in het geheugen opgeslagen. Als u de pagina verlaat en later terugkomt, blijft in het raster **Overzicht** dus het aantal dagen staan dat u de laatste keer hebt opgegeven.

Volg deze stappen om de pagina **Capaciteitsbelasting** te openen, zodat u de beschikbare capaciteit voor een afzonderlijke resource kunt controleren.

1. Ga naar **Organisatiebeheer \> Resources \> Resources**.
1. Selecteer een resource om te inspecteren.
1. Selecteer in het deelvenster Actie op het tabblad **Resource** in de groep **Weergave** de optie **Capaciteitsbelasting**.
1. Gebruik het veld **Aantal dagen** om het aantal dagen te beperken dat het raster **Overzicht** laat zien.

Volg deze stappen om de pagina **Capaciteitsbelasting** te openen, zodat u de beschikbare capaciteit voor een resourcegroep kunt controleren.

1. Ga naar **Organisatiebeheer \> Resources \> Resourcegroepen**.
1. Selecteer een resourcegroep om te inspecteren.
1. Selecteer in het deelvenster Actie op het tabblad **Resourcegroep** in de groep **Weergave** de optie **Capaciteitsbelasting**.
1. Gebruik het veld **Aantal dagen** om het aantal dagen te beperken dat het raster **Overzicht** laat zien.

## <a name="apply-a-single-level-of-marking-when-you-firm-planned-orders"></a>Pas een enkel markeringsniveau toe wanneer u geplande orders fiatteert

*Markering* wordt gebruikt om vraag en aanbod te koppelen. Het lijkt op *tracering van de behoefte* waarmee wordt aangegeven hoe de hoofdplanning de vraag verwacht te dekken. Markeren is echter permanenter dan traceren van de behoefte. De functie *Aanbodautomatisering voor maken naar order* voegt de mogelijkheid toe om het markeren van de voorraad te beperken tot een enkel niveau wanneer geplande orders worden gefiatteerd. Deze voegt de volgende nieuwe opties toe aan het veld **Markering bijwerken** in het dialoogvenster **Fiatteren** wanneer u een geplande order fiatteert:

- *Standaard met één niveau*: er wordt markering op één niveau gebruikt. Markering op één niveau markeert alleen het hoofdartikel en niet de stuklijstonderdelen. Zo kunt u na de goedkeuring componenttoewijzing voor productieorders flexibel houden. Markering op één niveau stelt het systeem in staat om te optimaliseren voor vraagwijzigingen op het laatste moment. In de *standaardmarkering op één niveau* worden behoefteorders gemarkeerd tegen hun afhandelingsorders, maar afhandelingsorders worden niet gemarkeerd als er een hoeveelheid resteert.
- *Eén niveau uitgebreid*: er wordt markering op één niveau gebruikt. In de *markering op één niveau uitgebreid* worden behoefteorders gemarkeerd tegen hun afhandelingsorders en worden afhandelingsorders altijd gemarkeerd, of er nu wel of niet een hoeveelheid resteert.

Deze opties zijn ook beschikbaar in het veld **Markering bijwerken** op het tabblad **Standaardupdate** van de pagina **Parameters hoofdplanning**, waar u de standaardselectie voor het dialoogvenster **Fiatteren** definieert.

Zie [Voorraad markeren](planning-optimization/marking.md) voor meer informatie.

## <a name="set-delay-tolerance-negative-days-at-the-master-plan-level"></a>De vertragingstolerantie (negatieve dagen) instellen op het niveau van het hoofdplan

De functie *Aanbodautomatisering voor maken naar order* voegt de mogelijkheid toe om vertragingstolerantie (negatieve dagen) te configureren op het niveau van het hoofdplan. De instelling is ook beschikbaar op de niveaus van artikelbehoefteplanning en dekkingsgroep. Als negatieve dagen op meer dan één niveau worden toegewezen, past het systeem de volgende hiërarchie toe om te bepalen welke instelling moet worden gebruikt:

- Als er negatieve dagen zijn geconfigureerd op de pagina met **Hoofdplannen**, heeft die instelling voorrang op alle andere instellingen voor negatieve dagen wanneer het plan wordt uitgevoerd.
- Als er negatieve dagen zijn geconfigureerd op de pagina **Artikelbehoefteplanning**, heeft die instelling voorrang op de instelling van de dekkingsgroep.
- Negatieve dagen die zijn geconfigureerd op de pagina **Dekkingsgroepen** zijn alleen van toepassing als er geen negatieve dagen zijn geconfigureerd voor een relevant artikel of relevant hoofdplan.

Volg deze stappen om negatieve dagen in te stellen voor een hoofdplan.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een hoofdplan in de het lijstvenster of maak een nieuwe aan.
1. Stel op het sneltabblad **Time fences in dagen** de optie **Negatieve dagen** in op *Ja*.
1. Voer in het bijbehorende veld het toegestane aantal negatieve dagen in.

Raadpleeg [Vertragingstolerantie (negatieve dagen)](planning-optimization/delay-tolerance.md) voor meer informatie over het gebruik van negatieve dagen.

## <a name="control-the-pegging-sequence-used-during-master-planning"></a>De reeks van de tracering van de behoefte beheren die wordt gebruikt tijdens de hoofdplanning

Hoofdplanning gebruikt een *reeks voor tracering van de behoefte* om te bepalen welk aanbod wordt gebruikt voor welke vraag. De functie *Aanbodautomatisering voor maken-naar-order* voegt een nieuwe optie **Laatst mogelijke voorraad gebruiken** toe waarmee u meer controle hebt over de reeks van de tracering van de behoefte. Met deze nieuwe optie blijven producten beschikbaar voor orders van het laatste moment en wordt het gebruik van bestaande voorraad geoptimaliseerd door het laatst mogelijke aanbod met een reeks voor tracering van de behoefte te koppelen aan een vraag in plaats van het eerst mogelijke aanbod te gebruiken.

U kunt de reeks voor tracering van de behoefte instellen op het niveau van hoofdplan, artikelbehoefteplanning of dekkingsgroepen. Als er op meer dan één niveau een reeks voor tracering van de behoefte is ingesteld, past het systeem de volgende hiërarchie toe om te bepalen welke instelling moet worden gebruikt:

- Als er een reeks voor de tracering van de behoefte is ingesteld op de pagina **Hoofdplannen**, heeft die instelling voorrang op alle andere instellingen voor de reeks voor de tracering van de behoefte wanneer het plan wordt uitgevoerd.
- Als er een reeks voor tracering van de behoefte is geconfigureerd op de pagina **Artikelbehoefteplanning**, heeft die instelling voorrang op de instelling van de dekkingsgroep.
- De reeks voor tracering van de behoefte die is ingesteld op de pagina **Dekkingsgroepen** is alleen van toepassing als er geen instellingen voor een reeks voor tracering van de behoefte zijn geconfigureerd voor een relevant artikel of hoofdplan.

Volg deze stappen om tracering van de behoefte op het niveau van de dekkingsgroep in te stellen.

1. Ga naar **Hoofdplanning \> Instellen \> Behoefteplanning \> Behoefteplanningsgroepen**.
1. Selecteer een groep in de het lijstvenster of maak een nieuwe aan.
1. Gebruik op het sneltabblad **Algemeen** in het gedeelte **Reeks voor tracering van de behoefte** de velden **Voorhanden voorraad verbruiken** en **Meest recente aanbod** om de reeks voor tracering van de behoefte te configureren. De tabel verderop in dit gedeelte laat zien hoe deze instellingen worden gecombineerd om de reeks voor tracering van de behoefte te definiëren.

Volg deze stappen om tracering van de behoefte op het niveau van de dekkingsgroep in te stellen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Selecteer een product in het raster of maak een nieuw product aan.
1. Selecteer in het actievenster op het tabblad **Plan** **Artikelbehoefteplanning**.
1. De pagina **Artikelbehoefteplanning** voorziet in rijen voor het definiëren van regels voor behoefteplanning die van toepassing zijn op het artikel in elk magazijn. Selecteer een bestaande rij in het raster of maakt een nieuwe aan.
1. Schakel op het tabblad **Algemeen** het selectievakje **Reeks voor tracering van de behoefte overschrijven** in.
1. Gebruik de velden **Voorhanden voorraad verbruiken** en **Meest recente aanbod gebruiken** om de reeks voor tracering van de behoefte te configureren. De tabel verderop in dit gedeelte laat zien hoe deze instellingen worden gecombineerd om de reeks voor tracering van de behoefte te definiëren.

Volg deze stappen om tracering van de behoefte op het niveau van het hoofdplan in te stellen.

1. Ga naar **Hoofdplanning \> Instellen \> Plannen \> Hoofdplannen**.
1. Selecteer een hoofdplan in de het lijstvenster of maak een nieuwe aan.
1. Stel op het sneltabblad **Algemeen** de optie **Reeks voor tarcering van de behoefte overschrijven** in op *Ja*.
1. Gebruik de velden **Voorhanden voorraad verbruiken** en **Meest recente aanbod gebruiken** om de reeks voor tracering van de behoefte te configureren. De tabel verderop in dit gedeelte laat zien hoe deze instellingen worden gecombineerd om de reeks voor tracering van de behoefte te definiëren.

De volgende tabel toont hoe de instellingen voor **Voorhanden voorraad verbruiken** en **Meest recente aanbod gebruiken** worden gecombineerd om de reeks voor tracering van de behoefte vast te stellen.

| | Meest recente aanbod gebruiken = Ja | Meest recente aanbod gebruiken = Nee |
|---|---|---|
| **Voorhanden voorraad verbruiken** = *Vóór alle aanbod* | <ol><li>Voorhanden</li><li>Bestaand aanbod dat aan de vraagdatum kan voldoen</li><li>Bestaand aanbod dat niet aan de vraagdatum kan voldoen, maar nog steeds binnen negatieve dagen</li><li>Nieuw aanbod aanmaken (geplande order)</li></ol> | <ol><li>Voorhanden</li><li>Bestaand aanbod dat aan de vraagdatum kan voldoen</li><li>Bestaand aanbod dat niet aan de vraagdatum kan voldoen, maar nog steeds binnen negatieve dagen</li><li>Nieuw aanbod aanmaken (geplande order)</li></ol> |
| **Voorhanden voorraad verbruiken** = *Na alle aanbod* | <ol><li>Bestaand aanbod dat aan de vraagdatum kan voldoen</li><li>Voorhanden</li><li>Bestaand aanbod dat niet aan de vraagdatum kan voldoen, maar nog steeds binnen negatieve dagen</li><li>Nieuw aanbod aanmaken (geplande order)</li></ol> | <ol><li>Bestaand aanbod dat aan de vraagdatum kan voldoen</li><li>Bestaand aanbod dat niet aan de vraagdatum kan voldoen, maar nog steeds binnen negatieve dagen</li><li>Voorhanden</li><li>Nieuw aanbod aanmaken (geplande order)</li></ol> |

## <a name="review-and-set-the-fulfillment-policy-that-applies-to-each-sales-order"></a>Het afhandelingsbeleid controleren en instellen dat geldt voor elke verkooporder

Afhandelingsbeleid beheert het percentage van de totale prijs of hoeveelheid van een order die fysiek gereserveerd moet zijn voordat u een verkooporder kunt vrijgeven naar het magazijn. U kunt een globaal standaard afhandelingsbeleid instellen en dit vervolgens waar nodig overschrijven voor specifieke klanten. De functie *Aanbodautomatisering voor maken naar order* voegt de mogelijkheid toe om te bekijken welk standaardbeleid werkelijk van toepassing is op elke order en om orderspecifiek overschrijven toe te passen.

- Ga voor het instellen van de standaard voor algemeen afhandelingsbeleid voor verkooporders naar **Klanten \> Instellingen \> Parameters klanten**. Stel vervolgens op het tabblad **Magazijnbeheer** het veld **Afhandelingsbeleid verkooporder** in op de naam van het beleid dat u wilt gebruiken. 
- Ga naar **Klanten \> Klanten \> Alle klanten** om een klantspecifiek afhandelingsbeleid voor verkooporders in te stellen. Stel vervolgens op het tabblad **Magazijn** het veld **Afhandelingsbeleid** in op de naam van het beleid dat u wilt gebruiken.

Volg deze stappen als u het standaardbeleid wilt weergeven dat op een order van toepassing is en een orderspecifieke overschrijving wilt toepassen.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
1. Open de verkooporder die u wilt inspecteren of bewerken.
1. Selecteer de weergave **Header**.
1. Controleer en bewerk op het sneltabblad **Magazijn** waar nodig de volgende velden:

    - **Orderafhandelingsbeleid**: selecteer het afhandelingsbeleid dat voor de geselecteerde order moet worden gebruikt. Het standaardbeleid wordt overschreven. Laat dit veld leeg om het standaardafhandelingsbeleid te gebruiken dat wordt getoond in het veld **Standaardafhandelingsbeleid**.
    - **Standaardafhandelingsbeleid**: dit veld toont het standaardafhandelingsbeleid dat van toepassing is als het veld **Orderafhandelingsbeleid** leeg is. Dit veld is alleen-lezen. Als het leeg is, wordt geen klantspecifiek of globaal standaardafhandelingsbeleid gedefinieerd.

    Als de velden **Orderafhandelingsbeleid** en **Standaardafhandelingsbeleid** allebei leeg zijn, is er geen afhandelingsbeleid van toepassing. Er kunnen echter andere beperkingen gelden en vereisen dat er wordt voldaan aan reserveringen of andere voorwaarden voordat de verkooporder kan worden vrijgegeven.

## <a name="set-the-delivery-mode-and-terms-on-individual-purchase-order-lines"></a>De leveringsmodus en voorwaarden voor afzonderlijke inkooporderregels instellen

Alle inkooporders bevatten instellingen voor de **leveringsvoorwaarden** en de **leveringsmodus** in de header van de order. De functie *Aanbodautomatie voor maken naar order* voegt deze instellingen toe aan elke orderregel. Daarom kunt u waar nodig overschrijvingen definiëren voor de waarde van **leveringsvoorwaarden** en/of **leveringsmodus** voor een of meer orderregels. Voor regels waarbij geen overschrijving is gedefinieerd, wordt de waarde uit de header gebruikt. U kunt opgeven of een wijziging in de waarde van een van deze velden of beide velden in de header van de order ook alle regels moet bijwerken.

Volg deze stappen om op te geven wat er moet gebeuren met de regelinstellingen als een gebruiker de waarde voor **leveringsvoorwaarden** en/of de **leveringsmodus** in de header van een order wijzigt.

1. Ga naar **Inkoop en sourcing \> Instellen \> Parameters voor Inkoopbeheer**.
1. Selecteer op het tabblad **Algemeen** op het sneltabblad **Standaardwaarden en parameters** de koppeling **Orderregels bijwerken**.
1. Selecteer in het dialoogvenster **Orderregels bijwerken** in de velden **Leveringsvoorwaarden bijwerken** en **Leveringsmodus bijwerken** een van de volgende waarden:

    - *Nooit*: werk de orderregels nooit bij nadat de instellingen in de header van de order zijn gewijzigd.
    - *Altijd*: werk altijd alle orderregels bij nadat de instellingen in de header van de order zijn gewijzigd.
    - *Vragen* : als een gebruiker een of beide instellingen in de header van de order wijzigt, wordt een dialoogvenster geopend waarin wordt gevraagd of de gebruiker alle regels wil bijwerken zodat deze overeenkomen met de wijziging in een of beide instellingen.

Volg deze stappen om leveringsgegevens in de header van een inkooporder in te stellen.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Open de inkooporder die u wilt bewerken.
1. Selecteer de weergave **Header**.
1. Stel op het sneltabblad **Levering** de velden **Leveringsmodus** en **Leveringsvoorwaarden** in zoals vereist.
1. Afhankelijk van de instellingen op de pagina **Parameters voor inkoop en sourcing** kan gevraagd worden of u de wijzigingen op alle orderregels wilt toepassen.

Volg deze stappen om overschrijvingen voor leveringsgegevens in een inkooporderregel in te stellen.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Open de inkooporder die u wilt bewerken.
1. Selecteer de weergave **Regels**.
1. Selecteer op het sneltabblad **Inkooporderregels** de regel die moet worden bewerkt.
1. Stel op het sneltabblad **Regelgegevens** op het tabblad **Levering** de velden **Leveringsmodus** en **Leveringsvoorwaarden** in zoals vereist. Schakel een of beide velden uit om de overeenkomende instellingen voor de header te gebruiken.

Bij intercompany-orders worden de waarden voor de velden **Leveringsmodus** en **Leveringsvoorwaarden** op elke inkooporderregel gesynchroniseerd tussen de inkooporder en de gerelateerde verkooporder.

## <a name="sync-external-item-ids-and-descriptions-for-intercompany-orders"></a>Externe artikel-IDs en omschrijvingen synchroniseren voor intercompany-orders

Bij intercompany-orders maakt de functie *Aanbodautomatisering voor maken naar order* het mogelijk om externe artikel-ID's en tekstomschrijvingen op inkooporderregels te synchroniseren met de gerelateerde intercompany-verkooporderregels, ongeacht of de inkooporder voor directe levering is. De functie voegt ook de mogelijkheid toe om de uiteindelijke externe klantaccount op te geven op een intercompany-inkooporder. Vervolgens neemt het systeem automatisch externe artikel-ID's en tekstomschrijvingen over uit de externe klantrecord in plaats van de (interne) intercompany-leveranciersrecord.

Volg deze stappen om een intercompany-leverancier in te stellen om externe artikel-ID's en artikelnamen te synchroniseren tussen intercompany-inkooporders en de gerelateerde intercompany-verkooporders.

1. Ga naar **Inkoop en sourcing \> Leveranciers \> Alle leveranciers**.
1. Selecteer de intercompany-leverancier die u wilt instellen.
1. Selecteer in het deelvenster Actie op het tabblad **Algemeen** in de groep **Instellen** op **Intercompany**.
1. Schakel op de pagina **Intercompany** op het tabblad **Inkooporderbeleid** in het gedeelte **Intercompany-inkooporder -\> Intercompany-verkooporder** het selectievakje **Extern-artikel-ID en artikelnaam** in.

Volg deze stappen om de uiteindelijke externe klantaccount op te geven voor een intercompany-inkooporder. Het veld **Klantaccount** is alleen van toepassing op intercompany-inkooporders. Gebruik dit om het accountnummer op te geven van de klant die de goederen uiteindelijk zal ontvangen. Wanneer dit veld is ingesteld, nemen inkooporderregels externe artikelomschrijvingen en -nummers over van het opgegeven klantaccount in plaats van de intercompany-leverancier die op de inkooporder is opgegeven. Als u het klantaccount later wijzigt, worden externe artikelomschrijvingen en -IDs bijgewerkt zodat ze overeenkomen met de waarden voor het nieuwe account. Externe artikelomschrijvingen en -ID's voor elke regel worden ook gesynchroniseerd met de overeenkomende intercompany-verkooporder.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Open de inkooporder die u wilt instellen of maak een nieuwe aan.
1. Selecteer de weergave **Header**.
1. Stel in het gedeelte **Verwijzing** het veld **Klantaccount** in op het relevante externe klantaccount.

Volg deze stappen om externe artikel-ID's en tekstomschrijvingen op te geven voor een inkooporderregel voor een intercompany-order. De waarden die u instelt, worden gesynchroniseerd met de gerelateerde intercompany-verkooporderregels, ongeacht of de inkooporder voor directe levering is.

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Open de inkooporder die u wilt instellen of maak een nieuwe aan.
1. Selecteer de weergave **Regels**.
1. Selecteer op het sneltabblad **Inkooporderregels** de regel die moet worden bewerkt.
1. Geef op het sneltabblad **Regelgegevnes** op het tabblad **Algemeen** in het gedeelte **Orderregel** in het veld **Tekst** een externe omschrijving op van het artikel dat is opgegeven op de geselecteerde orderregel. Deze waarde wordt gesynchroniseerd met de gerelateerde intercompany-verkooporderregel.
1. Geef in het gedeelte **Verwijzing** in het veld **Extern** een externe artikel-ID op voor het artikel dat op de geselecteerde orderregel is opgegeven. Deze waarde wordt gesynchroniseerd met de gerelateerde intercompany-verkooporderregel.

Raadpleeg [Een intercompany-verkooporder voor een externe klant aanmaken en factureren](../sales-marketing/intercompany-sales-order-for-external-customer.md) voor meer informatie.
