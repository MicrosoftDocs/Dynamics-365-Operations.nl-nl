---
title: Aanbiedingen maken, goedkeuren en ondertekenen
description: In dit onderwerp wordt beschreven hoe u een aanbieding voor een kandidaat maakt, goedkeurt en ondertekent met Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-19
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: acc484ea57ce13d8a7c48a0ca7a2aa8723558dc9
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551044"
---
# <a name="create-approve-and-sign-offers"></a>Aanbiedingen maken, goedkeuren en ondertekenen

[!include[banner](../includes/banner.md)]

In veel gevallen moet het maken van een aanbiedingspakket voor een kandidaat een zeer snel proces zijn.
Met de sjablonen die zijn ingesteld door de beheerder worden de tijd en inspanning verminderd voor de makers van de aanbieding om aanbiedingen te maken en naar een kandidaat te sturen.

## <a name="create-an-offer"></a>Een aanbieding maken

Wanneer de app Aanbiedingsbeheer is ingeschakeld, kan een gebruiker met de rol aanstellend manager of werver een aanbiedingspakket voor de kandidaat maken. Als u de aanbieding wilt maken,doet u het volgende.

1.  Navigeer naar de functie en de kandidaatsollicitatie waarvoor u de aanbieding maakt.

1.  Ga naar **Aanbiedingsfase** en klik op **Aanbieding voorbereiden**.

    U wordt omgeleid naar de app Aanbieding, waar u de kandidaat kunt zien met de status **Nieuw**. U ziet ook andere aanbiedingen waaraan u bijdraagt, hetzij als maker, hetzij als fiatteur.

1.  Klik op **Aanbieding voorbereiden**. 
    
    U ziet een keuze uit verschillende aanbiedingspakketten die beschikbaar zijn gemaakt door de beheerder.

1.  Selecteer een pakket en klik op **Gereed** om te beginnen met het maken van de aanbieding.

    De aanbiedingspakketsjabloon wordt geladen met de corresponderende functie en kandidaatdetails ingevuld in de aanbieding.

1.  Alle tijdelijke aanduidingen voor aanbiedingsgegevens die deel uitmaken van het aanbiedingspakket, zijn zichtbaar op de landingspagina. U kunt alle waarden in het pakket invullen op deze pagina.

    Op de landingspagina ziet u ook alle aanbiedingsdocumentsjablonen die deel uitmaken van het aanbiedingspakket.

1.  U kunt nu mogelijk de inhoud bewerken van de aanbieding, afhankelijk van hoe de sjabloon door de beheerder is geconfigureerd.

1.  Als u documenten moet verwijderen die zijn gemarkeerd als niet-vereist, kunt u dat doen.

1. Wanneer alle tijdelijke aanduidingen voor aanbiedingsgegevens zijn ingevuld, klikt u op **Opslaan** om een concept van de aanbieding op te slaan.

>[!NOTE]
> Nadat een concept is opgeslagen, kunt u de conceptversie van de aanbieding verwijderen of indien nodig een nieuwe pakketsjabloon selecteren.


## <a name="approve-an-offer"></a>Een aanbieding goedkeuren

De meeste aanbiedingen moeten een goedkeuringsproces doorlopen om ervoor te zorgen dat de aanbieding voldoet aan de vereiste standaarden. Als een aanbieding niet aan standaarden voldoet, bijvoorbeeld als de maker van de aanbieding de regels voor aanbiedingsgegevens niet heeft gevolgd en de waarde in de aanbieding heeft overschreven, is het goedkeuringsproces verplicht. Ga als volgt te werk om een aanbieding voor goedkeuring te verzenden.

1.  Wanneer de aanbieding de conceptstatus heeft, voegt u fiatteurs toe in het **deelvenster Fiatteur**. 
    >[!NOTE]
    > Aanstellend managers worden standaard als fiatteur toegevoegd. U kunt elke gebruiker van uw organisatie als goedkeurder voor de aanbieding kiezen.

1.  Wijs indien nodig fiatteurs toe met een sequentiële goedkeuringsmethode of een parallelle goedkeuringsmethode. Deze optie is alleen beschikbaar als deze als zodanig is geconfigureerd door de beheerder.
    >[!NOTE]
    > Als het goedkeuringsproces sequentieel is, kunt u de volgorde van fiatteurs indien nodig bewerken.

1.  Wanneer u klaar bent met het definiëren van de goedkeuringsketen, kunt u de inhoud van de goedkeuringse-mail bewerken en vervolgens de melding naar de fiatteurs sturen. Klik op **Verzenden naar fiatteurs**.
    >[!NOTE]
    > Als de aanbieding niet-standaard is, moet u een verantwoording verschaffen.

1.  Als de maker van de aanbieding een fiatteur overslaat, kan hij of zij een notitie invoeren en doorgaan naar de volgende fiatteur.

Fiatteurs ontvangen een e-mailbericht waarin hun wordt gevraagd de aanbieding goed te keuren. Ze kunnen in de e-mail klikken op de koppeling om de aanbieding te openen, het hele aanbiedingspakket bekijken en het goedkeuren of terugsturen naar de maker van de aanbieding. Andere fiatteurs moeten een extra notitie toevoegen als ze het aanbiedingspakket afwijzen voor verdere bewerkingen. 

In gevallen wanneer er een nieuwe versie van de aanbieding wordt gemaakt voordat de fiatteur iets doet, kan de fiatteur de aanbieding niet goedkeuren of afwijzen.

## <a name="offer-versioning"></a>Aanbiedingsversies 

Wanneer de aanbieding is goedgekeurd of teruggestuurd voor verdere bewerkingen, kunt u de optie **Bewerken inschakelen** kiezen om een nieuwe versie van de aanbieding te maken. De nieuwe versie van de aanbieding bevat alle aanbiedingsgegevenswaarden en de lijst met fiatteurs, overgenomen van de laatste versie. 

Fiatteurs kunnen schakelen tussen verschillende aanbiedingsversies als de versies met hen ter goedkeuring zijn gedeeld. Bovendien kan een fiatteur of de maker van de aanbieding ervoor kiezen een specifieke conceptaanbiedingsversie te verwijderen om terug te gaan naar de vorige status.


## <a name="send-an-offer-to-a-candidate"></a>Een aanbieding verzenden naar een kandidaat 

Wanneer de aanbieding wordt opgeslagen, goedgekeurd en klaar is voor verzending naar de kandidaat, klikt u op **Verzenden naar kandidaat**.

Er zijn verschillende acties die u uitvoeren kunt voordat de aanbieding naar de kandidaat wordt verzonden.
-  U kunt de lijst met documenten weergeven die deel uitmaken van het aanbiedingspakket dat wordt verzonden naar de kandidaat.

-  U kunt de vervaldatum van een aanbieding opgeven. Van kandidaten wordt verwacht dat ze de aanbieding accepteren of afwijzen vóór de vervaldatum.  De kandidaat ontvangt een herinnering 48 uur voordat de aanbieding verloopt.

-  Er zijn mogelijk extra documenten die u wilt opnemen in het proces voor aanbiedingsacceptatie. U kunt het vereiste documenttype vermelden.

- De optie Elektronische handtekening: er zijn twee manieren om verbinding maken met de gewenste provider van elektronische handtekeningen. Ga naar **Gebruikersinstellingen** in **Aanbieding** onder **Verbindingen** en maak verbinding met **Adobe Sign** of **DocuSign**. U kunt ook gevraagd worden om de pagina **Aanbieding verzenden naar de kandidaat** te verbinden als de verbinding nog niet tot stand is gebracht op basis van de gebruikersinstellingen. Het account met de elektronische handtekening hoeft slechts eenmaal te worden verbonden. Dezelfde gebruikerslicentie wordt gebruikt voor alle toekomstige aanbiedingspakketten die door dezelfde gebruiker worden verzonden. 

### <a name="adobe-sign"></a>Adobe Sign
Als Adobe Sign is gekozen als voorkeursmethode voor elektronisch ondertekenen, moeten makers van aanbiedingen hun licentie voor Adobe Sign in deze stap verbinden. 

### <a name="docusign"></a>DocuSign
Als DocuSign is gekozen als voorkeursmethode voor elektronisch ondertekenen, moeten makers van aanbiedingen hun licentie voor DocuSign verbinden. Zodra u bent aangemeld, worden het standaardaccount en de machtigingen die zijn gekoppeld aan het profiel DocuSign van de gebruiker verbonden met Talent: Attract. 

-  U kunt de e-mailsjabloon zo nodig weergeven en bewerken.

Als de aanbieding gereed is en u klikt op **Verzenden naar kandidaat**, ontvangt de kandidaat een e-mailbericht dat een aanbieding op beoordeling wacht.

>[!NOTE]
> Als u Adobe Sign of DocuSign gebruikt en er een fout optreedt tijdens het verzenden van de aanbieding naar de kandidaat, moet u proberen de verbinding van het gebruikersaccount voor de elektronische handtekening te verbreken en opnieuw verbinding te maken via **Gebruikersinstellingen**. Als het probleem zich blijft voordoen, neemt u contact op met onze ondersteuning met behulp van de koppeling **Een probleem melden**.

## <a name="candidates-actions-after-receiving-an-offer"></a>Acties van kandidaat na ontvangst van een aanbieding

Nadat de kandidaat is gemeld dat een aanbieding met hem of haar is gedeeld, kunnen ze in hun e-mail klikken om naar het sollicitatiedashboard te gaan en de aanbieding te bekijken. Het dashboard toont de kandidaat eventuele activiteiten die zij nog moeten voltooien.

1.  Als de kandidaat de aanbieding en alle gerelateerde documenten wil weergeven, klikt hij of zij op **Aanbieding weergeven**.

    Kandidaten kunnen ook het aanbiedingspakket downloaden in een zip-indeling.

1.  Om de aanbieding te accepteren, moeten de kandidaten klikken op **Springen naar handtekening** voor elk document dat deel uitmaakt van het aanbiedingspakket.

1.  Wanneer alle documenten afzonderlijk zijn ondertekend en geaccepteerd, moet de kandidaat ervoor kiezen het acceptatieproces te voltooien door te klikken op **Aanbieding accepteren**, boven aan de pagina.

1.  Als de kandidaat de aanbieding wil afwijzen, moet de kandidaat klikken op **Aanbieding afwijzen**, boven aan de pagina, een geschikte reden selecteren, indien nodig een opmerking toevoegen en vervolgens klikken op **Afwijzen**.

1.  Nadat de kandidaat de aanbieding heeft geaccepteerd of geweigerd, kan de kandidaat in de aanbiedingsweergave blijven of terug gaan naar het sollicitatiedashboard.

1.  Als er andere documenten als onderdeel van het acceptatieproces worden gevraagd, moet de kandidaat zo nodig kiezen voor het uploaden van de documenten en deze markeren aan het gevraagde documenttype.

1.  De maker van de aanbieding wordt gewaarschuwd wanneer de documenten zijn geüpload en het aanbiedingspakket is ondertekend.


## <a name="withdrawing-an-offer"></a>Een aanbieding intrekken

Een aanbod kan op elk moment om verschillende redenen van een kandidaat worden ingetrokken. 
1.  Trek de aanbieding in door te klikken op de ellipsisknop (**...**) en klik vervolgens op **De aanbieding intrekken**. 

2. Er wordt een bericht weergegeven waarin wordt gevraagd of de kandidaat is gecontacteerd over de wijziging in de status. Als de kandidaat nog niet is gecontacteerd, hebt u de optie een e-mailbericht te verzenden naar de kandidaat om hem of haar te informeren over verdere acties. 

   De aanbieding is niet meer toegankelijk voor de kandidaat.


## <a name="closing-an-offer"></a>Een aanbieding afsluiten 

Wanneer een aanbieding is geaccepteerd, geweigerd of ingetrokken zonder dat verdere acties nodig zijn, kunt u de aanbieding sluiten zodat er geen verdere wijzigingen kunnen worden gemaakt in dit aanbiedingspakket.
