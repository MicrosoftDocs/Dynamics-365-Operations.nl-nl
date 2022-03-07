---
title: Een callcenterkanaal instellen
description: In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e89c63c90aa8d46fd23900897a54165e14fb635d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800658"
---
# <a name="set-up-a-call-center-channel"></a>Een callcenterkanaal instellen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuw callcenterkanaal maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht


In Dynamics 365 Commerce is een callcenter een type handelsafzetkanaal dat kan worden gedefinieerd in de toepassing. Door een afzetkanaal voor uw callcenter-entiteiten te definiëren, kan het systeem specifieke gegevens en orderverwerkingsinstellingen koppelen aan verkooporders. Een bedrijf kan meerdere callcenterkanalen in Commerce definiëren, maar het is belangrijk om te weten dat een individuele gebruiker slechts aan één callcenterkanaal kan worden gekoppeld. 

Controleer vóór het maken van een nieuw callcenterkanaal of u de [Vereisten voor het instellen van kanalen](channels-prerequisites.md) hebt voltooid.

## <a name="create-and-configure-a-new-call-center-channel"></a>Een nieuw callcenterafzetkanaal maken en configureren

Voer de volgende stappen uit om een nieuw callcenterafzetkanaal te maken en te configureren.

1. Ga op de navigatiepagina naar **Detailhandel en commerce \> Kanalen \> Callcenters \> Alle callcenters**.
1. Selecteer **Nieuw** in het actievenster.
1. Typ in het veld **Naam** een naam voor het nieuwe kanaal.
1. Selecteer de juiste **Rechtspersoon** in de vervolgkeuzelijst.
1. Selecteer de juiste **Magazijn** locatie in de vervolgkeuzelijst. Deze locatie wordt gebruikt als standaardwaarde voor verkooporders die zijn gemaakt voor dit callcenterkanaal, tenzij er andere standaardwaarden zijn gedefinieerd op het niveau van de klant of het artikel.
1. Geef in het veld **Standaardklant** een geldige standaardklant op. Deze gegevens worden gebruikt om te helpen bij het automatisch vullen van standaardwaarden wanneer er nieuwe klantrecords worden gemaakt. Bij het maken van callcenterorders is het niet raadzaam orders voor de standaardklant te maken.
1. Geef in het veld **Profiel voor e-mailmelding** een geldig profiel voor e-mailmeldingen op. Wanneer orders in het callcenter worden gemaakt en verwerkt, wordt het e-mailprofiel gebruikt om automatische e-mailmeldingen naar klanten te activeren met informatie over hun orderstatus.
1. Geef een infocode op voor **Prijsoverschrijving**. Mogelijk moet u hiervoor eerst een informatiecode maken. Deze informatiecode bevat de set met redencodes die de gebruiker moet kiezen bij het gebruik van de functie voor prijsoverschrijving op een callcenterorder.
1. Geef een infocode op voor **Wachtstandcode**. Mogelijk moet u hiervoor eerst een informatiecode maken. Deze informatiecode bevat de set met optionele redencodes die de gebruiker moet kiezen bij het in de wacht plaatsen van een order.
1. Een infocode op voor **Krediet**. Mogelijk moet u hiervoor eerst een informatiecode maken. Deze informatiecode bevat de set met redencodes waaruit de gebruiker kan kiezen bij gebruik van de orderkredietfunctionaliteit van het callcenter om de klant terug te betalen vanwege redenen van de klantenservice.
1. Optioneel: financiële dimensies instellen op het sneltabblad **Financiële dimensies**. De dimensies die hier worden ingevoerd, worden standaard uitgevoerd op alle verkooporders die in dit callcenterkanaal zijn gemaakt.
1. Klik op **Opslaan**.

De volgende afbeelding toont het maken van een nieuw callcenterafzetkanaal.

![Nieuw callcenterafzetkanaal](media/channel-setup-callcenter-1.png)

In de volgende afbeelding ziet u een voorbeeld van een callcenterafzetkanaal.

![Voorbeeld van callcenterafzetkanaal](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Aanvullende afzetkanaalinstellingen

Aanvullende taken die nodig zijn voor het instellen van callcenterkanalen, zijn onder andere het instellen van betalingsmethoden en leveringsmethoden.

De volgende afbeelding toont de instellingsopties voor **Leveringsmethoden** en **Betalingsmethoden** op het tabblad **Instellingen**.

![Aanvullende acties voor het instellen van een callcenterkanaal](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Betalingsmethoden instellen

Volg deze stappen om betalingsmethoden in te stellen voor elk betalingstype dat op dit kanaal wordt ondersteund. Gebruikers moeten een keuze maken uit vooraf gedefinieerde betalingsmethoden om ze te koppelen aan het callcenterkanaal. Voordat u uw betalingsmethoden voor callcenters gaat instellen, moet u eerst uw hoofdbetalingsmethoden instellen in **Detailhandel en commerce \> Afzetkanaalinstellingen \> Betalingsmethoden \> Betalingsmethoden**.

1. Selecteer in het actievenster het tabblad **Instellingen** en selecteer **Betalingsmethoden**.
1. Selecteer **Nieuw** in het actievenster.
1. Selecteer in het navigatievenster een betalingsmethode van de beschikbare vooraf gedefinieerde betalingen.
1. Configureer eventuele aanvullende instellingen voor het betalingstype. Voor creditcards, geschenkbonnen of loyaliteitskaarten is aanvullende instelling vereist via de functie **Kaart instellen**. 
1. Configureer de juiste boekingsrekeningen voor het betalingstype in de sectie **Boeking**.
1. Klik in het actievenster op **Opslaan**.

In de volgende afbeelding ziet u een voorbeeld van een contante betalingsgmethode.

![Voorbeeldbetalingsmethoden](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Leveringsmethoden instellen

U kunt de geconfigureerde leveringsmethoden bekijken door **Leveringsmethoden** te selecteren op het tabblad **Instellingen** van het **actievenster**.  

Voer de volgende stappen uit om een leveringsmethode te wijzigen of toe te voegen aan het callcenterkanaal.

1. Selecteer **Leveringsmethoden beheren** in het formulier Leveringsmethoden van het callcenter
1. Selecteer in het actievenster de optie **Nieuw** als u een nieuwe leveringsmethode wilt maken of selecteer een bestaande methode.
1. Klik in de sectie **Detailhandelkanalen** op **Regel toevoegen** om het callcenterkanaal toe te voegen. Als u kanalen toevoegt met organisatieknooppunten in plaats van elk kanaal afzonderlijk toe te voegen, kunt u het toevoegen van kanalen stroomlijnen.
1. Zorg ervoor dat de leveringsmethode is geconfigureerd met gegevens op het sneltabblad **Producten** en op het sneltabblad **Adressen**. Als er geen producten of leveringsadressen geldig zijn voor de leveringsmethode, wordt bij het invoeren van de order fouten geretourneerd.
1. Nadat er wijzigingen zijn aangebracht in de callcentermodus voor leveringsconfiguraties, moet de taak **Leveringsmethoden verwerken** worden uitgevoerd om de wijzigingsmatrix uit te breiden. U vindt deze taak via **Detailhandel en commerce \> IT detailhandel en commerce \> Leveringsmethoden verwerken**.

In de volgende afbeelding ziet u een voorbeeld van een leveringsmethode.

![Leveringsmethoden instellen](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanaalgebruikers instellen

Als u een verkooporder wilt maken die is gekoppeld aan het callcenterkanaal vanuit Commerce-hoofdkantoor, moet de gebruiker die de verkooporder maakt, zijn gekoppeld aan het callcenterkanaal. De gebruiker kan een verkooporder die in Commerce-hoofdkantoor is gemaakt niet handmatig koppelen aan het callcenterkanaal. De koppeling is systematisch en is gebaseerd op de gebruiker en de relatie van de gebruiker met het callcenterkanaal. Een gebruiker kan slechts aan één callcenterkanaal worden gekoppeld.

1. Selecteer in het actievenster het tabblad **Kanaal** en selecteer **Kanaalgebruikers**.
1. Selecteer **Nieuw** in het actievenster.
1. Kies een bestaande **gebruikers-id** uit de vervolgkeuzelijst om deze gebruiker aan het callcenterkanaal te koppelen

Nadat de instellingen voor de kanaalgebruiker zijn ingevoerd en de gebruiker een nieuwe verkooporder maakt in Commerce-hoofdkantoor, moet de verkooporder worden gekoppeld aan het bijbehorende callcenterkanaal. Alle configuraties voor dit kanaal worden systematisch op de verkooporder toegepast. Een gebruiker kan bevestigen aan welk callcenterkanaal de verkooporder is gekoppeld door de kanaalnaamverwijzing in de verkooporderkop weer te geven.


### <a name="set-up-price-groups"></a>Prijsgroepen instellen

Prijsgroepen zijn optioneel, maar als deze worden gebruikt, kunnen ze bepalen welke verkoopprijzen worden aangeboden aan klanten die orders plaatsen in het callcenterkanaal. Als er geen prijsgroep voor de klant is geconfigureerd of als er geen prijsgroepen op de verkooporder worden toegepast (met het veld **Broncode-id** in de koptekst van de callcenterorder), wordt de afzetkanaalprijsgroep gebruikt om artikelprijzen te zoeken. Als er geen prijsgroep wordt gevonden op het callcenterkanaal, worden de standaardprijzen voor de artikelmodellen gebruikt. 

Ga als volgt te werk om een prijsgroep in te stellen.

1. Klik in het actievenster op het tabblad **Kanaal** en selecteer **Prijsgroepen**.
1. Klik in het actievenster op **Nieuw**.
1. Selecteer een **detailhandelsprijsgroep** in de keuzelijst.

## <a name="additional-resources"></a>Aanvullende bronnen

[Vereisten voor het instellen van kanalen](channels-prerequisites.md)

[Verkoopfunctionaliteit callcenter](call-center-functionality.md)

[Orderverwerkingsopties voor callcenter instellen](set-up-order-processing-options.md)

[Callcentercatalogi](call-center-catalogs.md)

[Instellen en werken met fraudewaarschuwingen](set-up-fraud-alerts.md)

[Continuïteitsprogramma's instellen voor callcenters](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]