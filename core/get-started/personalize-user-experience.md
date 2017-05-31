---
title: De gebruikerservaring aanpassen
description: In dit artikel wordt uitgelegd hoe u Microsoft Dynamics 365 for Operations kunt aanpassen.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 689efef6ffa10bbee30cd734f3f09ba20957834d
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="personalize-the-user-experience"></a>De gebruikerservaring aanpassen

[!include[banner](../includes/banner.md)]


In dit artikel wordt uitgelegd hoe u Microsoft Dynamics 365 for Operations kunt aanpassen.

Er bestaan veel typen persoonlijke instellingen in Microsoft Dynamics 365 for Operations. Sommige aanpassingen zijn selecties die u in een lijst met opties op een instellingenpagina maakt. Sommige aanpassingen zijn impliciet. Dynamics 365 for Operations houdt bijvoorbeeld de breedte van rasterkolommen bij als u deze aanpast, en de status van uitgevouwen of samengevouwen sneltabbladen. Andere aanpassingen zijn expliciet. Voor expliciete aanpassingen activeert u een interactieve aanpassingsmodus en wijzigt u de weergave van een pagina door direct te beheren hoe elementen worden weergegeven of zich op de pagina gedragen. 

Alle persoonlijke instellingen van elk type die een gebruiker aanbrengt in Dynamics 365 for Operations, zijn alleen voor die gebruiker, ongeacht het bedrijf waarmee de gebruiker communiceert. Wijzigingen die een gebruiker op een pagina aanbrengt, beïnvloeden andere gebruikers in het systeem niet.

## <a name="systemwide-options-for-the-current-user"></a>Systeembrede opties voor de huidige gebruiker
Op de navigatiebalk vindt u een afbeelding van een tandwiel. Dat is de menuknop **Instellingen**. Bij het openen van het **Instellingen** menu wordt een aantal keuzen weergeven. Door **Opties** te selecteren opent de gebruiker de pagina **Opties**. Hier vindt u vier optietabbladen: **Zichtbaar**, **Voorkeuren**, **Rekening** en **Werkstroom**.

-   **Zichtbaar:**Gebruiken om een kleurenthema en de standaardgrootte van de elementen op uw pagina's te kiezen.
-   **Voorkeuren:** Hier kunt u standaardwaarden kiezen voor wanneer u Dynamics 365 for Operations opstart, inclusief het bedrijf, de oorspronkelijke pagina en standaardweergave/bewerkingsmodus (die bepaalt of een pagina is vergrendeld voor weergave of voor bewerking wordt geopend telkens wanneer u deze opent). U vindt ook opties voor de taal, tijdzone en datum, tijd en getalnotatie. Ten slotte bevat deze pagina een aantal verschillende voorkeuren die van versie tot versie variëren.
-   **Account:** Gebruiken om uw gebruikers-ID op te geven en andere opties die op de rekening betrekking hebben.
-   **Werkstroom:**Hier kiest u opties met betrekking tot workflows.

## <a name="implicit-personalizations"></a>Impliciete aanpassingen
Impliciete aanpassingen zijn aanpassingen die u eenvoudig aanbrengt door met bepaalde besturingselementen te werken die hun huidige zichtbare status onthouden. 

**Rasterkolommen:** U kunt de breedte van een kolom in een lijst aanpassen door de formaatbalk links of rechts van de kolomkop te selecteren en deze naar links of rechts te schuiven voor de gewenste breedte. Dynamics 365 for Operations slaat de gewenste breedte op en geeft die kolom steeds met die breedte weer als u de pagina met die lijst opent. 

**Sneltabbladen:** Sommige lijstpagina's bevatten uitvouwbare secties genaamd sneltabbladen. Dynamics 365 for Operations slaat op welke sneltabbladen uitgevouwen zijn en welke sneltabbladen u hebt samengevouwen. Telkens als u terugkeert naar de pagina, worden die dezelfde sneltabbladen uitgevouwen of samengevouwen gebaseerd op de laatste keer dat u ze gebruikte. In dit artikel wordt beschreven hoe u de volgorde van uw sneltabbladsecties wijzigt. In sommige gevallen verbetert samenvouwen van een sneltabblad de prestaties omdat Dynamics 365 for Operations de informatie voor dat sneltabblad pas hoeft op te halen als het sneltabblad wordt uitgevouwen. 

**Feitenvakken:** Sommige lijstpagina's hebben een onderdeel genaamd het feitenvak. Dit deelvenster bevat alleen-lezen gegevens met betrekking tot het huidige onderwerp van de pagina. Elke sectie in het feitenvakvenster wordt een feitenvak genoemd. U kunt een feitenvak uitvouwen en samenvouwen en Dynamics 365 for Operations slaat uw voorkeuren op. In sommige gevallen kan het samenvouwen van een feitenvak de prestaties van Dynamics 365 for Operations verbeteren, doordat de gegevens voor dat feitenvak pas opgehaald hoeven te worden wanneer het feitenvak wordt uitgevouwen.

## <a name="explicit-personalizations-using-the-personalization-toolbar"></a>Expliciete aanpassingen met de werkbalk Aanpassing
Elke persoon en bedrijf heeft een ander perspectief op welke gegevens het belangrijkst zijn of welke gegevens niet nodig zijn voor hoe zij hun bedrijf runnen. De mogelijkheid om de manier aan te passen waarop uw informatie wordt geordend, gebruikt of verborgen maakt Dynamics 365 for Operations tot een persoonlijke en productieve ervaring. 

Expliciete aanpassingen zijn aanpassingen die u expliciet aanbrengt met de bedoeling de weergave of werking van een element of pagina te wijzigen door een aanpassingsmenu te kiezen. Het meest elementaire type expliciete aanpassing is met de rechtermuisknop op een element klikken en **Aanpassen** selecteren. Houd er rekening mee dat niet alle elementen op uw pagina kunnen worden aangepast. Wanneer u deze methode van persoonlijke instellingen selecteert, ziet u het eigenschappenvenster van het element. 

[![Eigenschappen van een element aanpassen](./media/personalization-element-properties.jpg)](./media/personalization-element-properties.jpg) 

U past een element op uw pagina zo aan als u eenvoudigweg het label van het element wilt wijzigen, het element wilt verbergen zodat het niet wordt weergegeven op de pagina (dit verandert geen gegevens, maar u ziet de informatie niet), de informatie wilt opnemen in de overzichtssectie van het sneltabblad (als het element zich op een sneltabblad bevindt), het veld wilt overslaan als op Tab wordt gedrukt of wilt voorkomen dat de gegevens worden gewijzigd, door het element te markeren als 'Niet bewerken'. 

Wanneer u elementen wilt verplaatsen of verbergen of meerdere wijzigingen wilt aanbrengen, kunt u de werkbalk Aanpassing gebruiken. Deze is beschikbaar vanuit het venster Elementeigenschappen door **Dit formulier aanpassen** te kiezen. De werkbalk Aanpassing is ook beschikbaar in het Actievenster van het formulier, onder de groep Aanpassing van het tabblad **Opties**. Selecteer **Dit formulier aanpassen** om de werkbalk Aanpassing weer te geven. 

[![De werkbalk Aanpassing](./media/personalization-personalizationtoolbar.jpg)](./media/personalization-personalizationtoolbar.jpg)

De werkbalk Aanpassing bevat een aantal aanpassingsacties. Kies het hulpmiddel **Selecteren** als u de eigenschappen van veel elementen één voor één wilt selecteren en wijzigen. Klik eerst op het hulpmiddel Selecteren en klik vervolgens op het element waarvan u de eigenschappen wilt wijzigen. Wanneer u een element selecteert, wordt de het eigenschappenvenster van het element geopend en kunt u eventuele eigenschappen voor dat element wijzigen. U kunt het proces herhalen voor andere elementen op uw formulier die aanpasbaar zijn. In sommige gevallen selecteert u een element en ziet u dat sommige eigenschappen niet kunnen worden gewijzigd. Dit betekent dat op basis van de manier waarop het huidige element wordt gebruikt, Dynamics 365 for Operations u die eigenschap niet kan laten wijzigen. U kunt bijvoorbeeld geen veld verbergen dat vereist is. 

Kies het hulpmiddel **Verplaatsen** wanneer u een element wilt selecteren en wilt verplaatsen naar een andere locatie in de huidige groep elementen. (U kunt een element buiten de bovenliggende groep plaatsen.) Klik eerst op het hulpmiddel Verplaatsen en klik vervolgens op het element dat u wilt verplaatsen. Wanneer u klikt op het element dat u wilt verplaatsen, scant Dynamics 365 for Operations het formulier om te begrijpen waar dit element naartoe kan worden verplaatst en maakt een reeks neerzetgebieden aan. Deze worden weergegeven als een gekleurde vette regel, naast het gebied waarin het element kan worden neergezet, terwijl u het element binnen de huidige groep sleept. 

Kies het hulpmiddel **Verbergen** om een element te selecteren en te verbergen. Om een element te verbergen, kies eenvoudigweg het hulpmiddel Verbergen en klik op het element dat u wilt verbergen. Wanneer u het hulpmiddel Verbergen kiest, worden alle elementen die momenteel zijn verborgen zichtbaar gemaakt en in een grijze container weergegeven, zodat u kunt kiezen welke elementen u zichtbaar wilt maken. Kies het hulpmiddel Selecteren om te zien hoe de pagina eruit zal zien met de geselecteerde elementen verborgen. Kies het hulpmiddel **Overzicht** wanneer u wilt dat een numeriek of tekenreeksveld wordt weergegeven in het overzichtsgebied van het sneltabblad. Het hulpmiddel Overzicht heeft alleen betrekking op velden binnen een sneltabblad-sectie. Als u het hulpmiddel Overzicht kiest, toont Dynamics 365 for Operations alle velden die als overzichtsvelden zijn geselecteerd door deze in een grijze container in te sluiten. U kunt velden interactief toevoegen en verwijderen uit een sneltabblad-overzicht door op het veld te klikken. 

Kies het hulpmiddel **Overslaan** om een element te verwijderen uit de volgorde van de toetsenbordtoets Tab van de pagina. Wanneer u het hulpmiddel Overslaan kiest, worden alle huidige overgeslagen elementen in een gearceerde container weergegeven, zodat u ze opnieuw kunt kiezen om ze deel te maken van de Tab-volgorde door een overgeslagen element te selecteren. 

Kies het hulpmiddel **Bewerken** wanneer u een element als bewerkbaar of niet bewerkbaar wilt markeren. Wanneer u het hulpmiddel Bewerken kiest, worden alle elementen die momenteel niet kunnen worden bewerkt in een grijze container weergegeven, zodat u ervoor kunt kiezen om ze bewerkbaar te maken. Merk op dat sommige velden zijn verplicht en niet niet-bewerkbaar kunnen worden gemaakt. Deze velden worden met een hangslotpictogram ernaast weergegeven. 

Kies het hulpmiddel **Toevoegen** om een veld toe te voegen aan uw pagina. Met het hulpmiddel Toevoegen kunt u geen nieuw veld maken, maar u kunt wel velden toevoegen die deel uitmaken van de huidige paginadefinitie, maar momenteel niet worden weergegeven op de pagina. Wanneer u het hulpmiddel Toevoegen kiest, moet u eerst de groep of het gebied selecteren waar u een veld wilt toevoegen. Er wordt een dialoogvenster weergegeven met de lijst met velden die gerelateerd zijn aan de sectie die u hebt geselecteerd. Vanuit dit dialoogvenster kunt u een of meer velden selecteren om toe te voegen en op Invoegen klikken. Als u later een veld wilt verwijderen dat u eerder hebt toegevoegd, herhaalt u het proces, maar wist u het veld dat u eerder hebt toegevoegd. 

Kies de knop **Beheren** om een lijst met beheeropties te bekijken met betrekking tot alle aanpassingen voor de huidige pagina. 

Kies **Wissen** om de pagina weer op de standaard, geïnstalleerde toestand in te stellen. Alle aanpassingen op de huidige pagina worden gewist. Er is geen actie voor ongedaan maken. Gebruik deze optie dus alleen als u zeker weet dat u uw pagina opnieuw wilt instellen. 

Kies **Importeren** om een aanpassing uit een aanpassingsbestand te gebruiken die u of iemand anders eerder voor deze pagina heeft gemaakt. Het importeren van een aanpassing wist eventuele aanpassingen die u hebt aangebracht op de pagina en gebruikt in plaats daarvan de aanpassingen uit het geselecteerde bestand. Als u persoonlijke instellingen wilt opslaan of delen, moet u de optie **Exporteren** selecteren om de persoonlijke instellingen naar een bestand op te slaan. 

Kies de knop **Sluiten** om de werkbalk te sluiten en de pagina terug te brengen naar de vorige interactieve status. 

Met de werkbalk Aanpassing, is opslaan impliciet. Uw aanpassingen zijn direct van kracht en het is niet nodig om op een knop **Opslaan** te klikken. In sommige gevallen ziet u een hangslotpictogram naast een element wanneer u een hulpmiddel selecteert. Dit betekent dat om de pagina goed te laten werken, u de eigenschappen met betrekking tot het geselecteerde hulpmiddel niet kunt wijzigen. Wanneer werkbalk Aanpassing wordt geopend, wordt de pagina niet-interactief. U kunt geen gegevens invoeren of secties uit- of samenvouwen.

## <a name="explicit-personalization-adding-a-tile-or-list-to-a-workspace"></a>Expliciete aanpassing: een tegel of lijst toevoegen aan een werkruimte
Sommige pagina's met lijsten hebben een aanvullende afpassingsfunctie beschikbaar binnen het actievenster, onder de groep Aanpassing op het tabblad Opties. Selecteer **Toevoegen aan werkruimte** om de vervolgkeuzelijst te openen die u de mogelijkheid geeft om de informatie in de huidige lijst (gefilterd en gesorteerd of standaard) op een werkruimte als een lijst of tegeloverzicht (dat kan worden gebruikt om het aantal artikelen in de lijst weer te geven) weer te geven. 

[![Toevoegen aan werkgebied](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png) 

Als u een lijst aan een werkgebied wilt toevoegen, sorteert of filtert u de lijst eerst met de informatie zoals u deze in uw werkgebied wilt zien, en selecteert u vervolgens het dialoogvenster Toevoegen aan werkgebied. Selecteer vervolgens de gewenste werkruimte en selecteer **Lijst** van de vervolgkeuzelijst Presentatie. Wanneer u **Lijst** selecteert, wordt een dialoogvenster geopend waarin u de kolommen kunt kiezen die u in de lijst wilt opnemen, en het label voor de lijst zoals dat in de werkruimte zal worden weergegeven. 

Als u een deel aan een werkruimte wilt toevoegen, filtert u eerst de lijst om de gegevens weer te geven waarvan u een overzichyt wilt (of waartoe u snel toegang wilt krijgen). Open daarna het dialoogvenster Toevoegen aan werkgebied. Selecteer vervolgens de gewenste werkruimte en selecteer **Tegel** van de vervolgkeuzelijst Presentatie. Wanneer u **Tegel**selecteert, wordt een dialoogvenster geopend waarin u de tegel een label kunt geven en kunt bepalen of in de tegel een telling wordt weergeven. Wanneer geplaatst op een werkruimte, kunt u met de tegel de huidige pagina van de werkruimte openen, en de lijst van informatie weergeven met betrekking tot de tegel. 

Wanneer uw lijst of tegel aan een werkruimte is toegevoegd, kunt u deze werkruimte openen en vervolgens de lijst of de tegel herschikken in de groep waarin deze is geplaatst.

## <a name="explicit-personalization-adding-a-summary-from-a-workspace-to-a-dashboard"></a>Expliciete aanpassing: een overzicht toevoegen vanuit een werkruimte naar een dashboard
Sommige werkgebieden bevatten teltegels (tegels met cijfers erop) die u ook op uw dashboard zou willen weergeven. Klik in een werkgebied met de rechtermuisknop op een teltegel en selecteer **Aanpassen**. Selecteer **Vastmaken op dashboard**. De volgende keer dat u naar het geselecteerde dashboard navigeert (en vernieuwt), ziet u de telling onder de navigatiedeel van deze werkruimte op het dashboard.

## <a name="explicit-personalization-personalizing-your-dashboard"></a>Expliciete aanpassing: uw dashboard aanpassen
Het dashboard is vaak de eerste pagina die bij het openen Dynamics 365 for Operations wordt weergegeven. U kunt het dashboard personaliseren om de naam van uw werkruimtenavigatietegels te wijzigen, alleen de tegels te tonen die u wilt weergeven, de naam van de tegels te wijzigen of de tegels te ordenen in elke gewenste volgorde. Om het dashboard te personaliseren, selecteert u een tegel en klikt u met de rechtermuisknop om een contextmenu te openen. Selecteer in het contextmenu **Aanpassen**. Als de geselecteerde tegel er een is die u wilt verbergen, hernoemen of overslaan, kunt u die wijziging direct maken in het eigenschappenvenster dat wordt weergegeven. Als u tegels wilt ordenen, selecteert u **Dit formulier aanpassen** in het eigenschapvenster om de werkbalk Aanpassing te openen. U kunt vervolgens de verplaatsingsfunctie gebruiken om de tegels te ordenen.

## <a name="administration-of-personalization"></a>Beheer van aanpassing
Het is mogelijk om een pagina aan te passen en te delen met andere gebruikers door de aangepaste pagina eenvoudigweg te exporteren en de andere gebruikers te vragen naar de aangepaste pagina te navigeren en het aanpassingsbestand te importeren dat u hebt gemaakt. Als een gebruiker beheerdersbevoegdheden heeft, kan deze ook aanpassingen voor andere gebruikers beheren op de pagina **Aanpassingsinstelling**. Navigeer naar de B-pagina. Op de pagina **Aanpassing** vindt u twee tabbladen, één genaamd **Systeem** en één genaamd**Gebruikers**. 

**Systeem:** Dit is waar u tijdelijk alle aanpassingen in het systeem kunt uitschakelen. Hiermee worden geen persoonlijke instellingen verwijderd, maar worden alle formulieren opnieuw ingesteld op hun standaardstatus. U kunt aanpassingen later opnieuw inschakelen om alle aanpassingen opnieuw toe te passen op de formulieren van iedere gebruiker. U kunt ook alle aanpassingen voor alle gebruikers verwijderen. Merk op dat als u aanpassingen verwijdert, er geen manier is om aanpassingen van het systeem automatisch opnieuw in te schakelen. Zorg ervoor dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt importeren voordat u deze stap uitvoert. 

**Gebruikers:** Dit is waar u voor elke gebruiker kunt kiezen of ze impliciete of expliciete aanpassing kunnen uitvoeren. U kunt ook bepalen of elke gebruiker impliciete of expliciete aanpassingen kan maken aan een specifiek formulier. Ten slotte kunt u een aanpassing voor elke gebruiker importeren, exporteren of verwijderen. 

**Opmerking:** In de initiële versie staat aanpassingsbeheer alleen beheer per gebruiker toe.




