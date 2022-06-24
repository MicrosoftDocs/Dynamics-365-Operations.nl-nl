---
title: Callcenterkanalen instellen
description: Dit artikel biedt informatie over het verwerken van procesorders voor callcenters met gebruik van Dynamics 365 Commerce.
author: josaw1
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c6d21385d956534c799af5b9e20a54c9970da368
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854866"
---
# <a name="set-up-call-center-channels"></a>Callcenterkanalen instellen

[!include [banner](includes/banner.md)]

Een bedrijf kan meerdere callcenterkanalen definiëren in Dynamics 365 Commerce. Callcenterkanalen worden geconfigureerd via **Detailhandel en commerce** \> **Kanalen** \> **Callcenters** \> **Alle callcenters**, en zijn specifiek voor een rechtspersoon.

Wanneer een nieuwe callcenterkanaal wordt gemaakt, wordt hieraan systematisch een nummer van een operationele eenheid toegewezen. Omdat callcenters worden gemaakt als operationele eenheden, kunnen gebruikers het callcenterkanaal koppelen aan verschillende Commerce-functies, zoals assortimenten, catalogi en specifieke leveringsmethoden.

Een standaardmagazijn kan worden geconfigureerd voor het callcenterkanaal. Wanneer verkooporders worden gemaakt voor dat kanaal, wordt het standaardmagazijn automatisch ingevoerd in de verkooporderkoptekst, tenzij een ander magazijn is gedefinieerd voor de klant die is geselecteerd voor de verkooporder. Standaard wordt in dat geval het magazijn van de klant ingevoerd.

Gebruikers moeten worden gekoppeld aan een callcenterkanaal om de functies van het callcenter te gebruiken. Een verkooporder die door een gebruiker wordt gemaakt, wordt automatisch gekoppeld aan het callcenterkanaal. Op dit moment kan er niet één gebruiker worden gekoppeld aan meerdere callcenterkanalen tegelijk.

Ook kan een profiel voor e-mailmelding worden geconfigureerd op het callcenterkanaal. Het profiel definieert de set met e-mailsjablonen die wordt gebruikt wanneer e-mail wordt verzonden aan klanten die orders plaatsen via het callcenterkanaal. Het activeren van de e-mail kan worden geconfigureerd voor systeemgebeurtenissen, zoals het indienen van de order of een zending.

Voor het correct verwerken van verkopen via een callcenterkanaal, moeten de juiste [betalingsmethoden](/dynamics365/unified-operations/retail/work-with-payments) en leveringsmethoden worden gedefinieerd voor het kanaal.

U kunt op het niveau van het callcenterkanaal andere standaardwaarden definiëren die zijn gerelateerd aan de financiële dimensies die wordt gekoppeld aan orders die zijn gemaakt door dat kanaal.

## <a name="options-for-order-processing-behavior"></a>Opties voor gedrag bij orderverwerking

Drie instellingen van de configuratie van een callcenter hebben veel invloed op de voorzieningen en functies die beschikbaar zijn voor verkooporders die zijn gemaakt voor dat callcenter: **Ordervoltooiing inschakelen**, **Rechtstreekse verkoop inschakelen** en **Orderprijscontrole inschakelen**.

### <a name="enable-order-completion"></a>Ordervoltooiing inschakelen

De instelling **Ordervoltooiing inschakelen** voor het callcenterkanaal heeft een groot effect voor de orderverwerkingstroom van verkooporders die zijn ingevoerd voor dat kanaal. Als deze instelling is ingeschakeld, moeten alle verkooporders een set validatieregels doorlopen voordat deze kunnen worden bevestigd. U voert deze regels uit door het selecteren van de knop **Voltooien** die wordt toegevoegd aan het actievenster van de verkooporderpagina. Alle verkooporders die worden gemaakt als de instelling **Ordervoltooiing inschakelen** is ingeschakeld, moeten het ordervoltooiingsproces doorlopen. Dit proces zorgt voor de opname van betalingen en validatielogica voor betalingen. Naast het uitvoeren van de betaling activeert het orderverzendproces [fraudecontroles](/dynamics365/unified-operations/retail/set-up-fraud-alerts) die u in het systeem configureert. Orders waarvoor de betaling mislukt of frauduleuze validaties worden in de wachtstand geplaatst en kunnen niet worden vrijgegeven voor verdere verwerking (zoals orderverzamelen of verzending) totdat het probleem van de blokkering opgelost is.

Wanneer de instelling **Ordervoltooiing inschakelen** is ingeschakeld voor het callcenterkanaal en er regelitems zijn ingevoerd op een verkooporder, en de gebruiker van het kanaal het verkooporderformulier wil sluiten of verlaten zonder dat **Voltooid** is geselecteerd, zorgt het ordervoltooiingsporces dat de pagina Samenvatting van verkooporder wordt geopend en moet de gebruiker de order correct indienen. Als de order niet correct kan worden ingediend met de betaling, kan de gebruiker de functie [Orderwachtstanden](/dynamics365/unified-operations/retail/work-with-order-holds) toepassen om de order in de wachtstand te plaatsen. Als de gebruiker de order wil annuleren, moet hij of zij juist deze annuleren met behulp van de functie Annuleren of Verwijderen, afhankelijk van de functie die wordt toegestaan door de beveiliging.

Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld voor het callcenterkanaal, wordt het veld **Betalingsstatus** bijgehouden op de order. Het systeem berekent de **betalingsstatus** wanneer de verkooporder wordt ingediend. Alleen orders met een goedgekeurde betalingsstatus mogen verdergaan naar extra orderverwerkingsstappen, zoals verzamelen en verzenden. Als betalingen worden geweigerd, wordt de markering **Niet verwerken** ingeschakeld voor de gedetailleerde orderstatus, waarmee deze order wordt geblokkeerd totdat het betalingsprobleem is opgelost.

Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld wanneer gebruikers verkooporders maken en in de invoermodus regelartikel zijn, is het veld **Bron** beschikbaar op de koptekst van de hoofdverkooporder. het veld **Bron** wordt gebruikt een [catalogusbroncode](/dynamics365/unified-operations/retail/call-center-catalogs) vast te leggen in een verkoopscenario voor direct marketing. Deze code kan vervolgens speciale prijzen en promoties opgeven.

Zelfs als de instelling **Ordervoltooiingi inschakelen** is uitgeschakeld, kunnen gebruikers nog steeds een broncode toepassen op een verkooporder. Maar ze moeten eerst de koptekstgegevens van de verkooporder openen voor toegang tot het veld **Bron**. Er zijn dus een aantal aanvullende muisklikken nodig. Dezelfde situatie is van toepassing op functies zoals zending voltooid en afgehandelde orders. Deze functies zijn beschikbaar voor alle orders die zijn gemaakt in het callcenter. Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld, kunnen gebruikers de configuratie van deze functies zien in de verkoopkoptekst in de weergave voor regelinvoer. Ze hoeven niet in te zoommen naar de koptekstgegevens van de verkooporder om de gewenste instellingen en velden te zien.

> [!NOTE]
> Wanneer de functie **Commerce-orderbetalingen voor meerdere kanalen** is ingeschakeld, wordt de knop **Ordervoltooiing inschakelen** van het callcenter verborgen in het hoofdkantoor op het sneltabblad **Algemeen** van uw kanaal via **Retail en commerce \> Kanalen \> Callcenters**.

### <a name="enable-direct-selling"></a>Rechtstreekse verkoop inschakelen

Als de instelling **Rechtstreekse verkoop inschakelen** is ingeschakeld voor het callcenterkanaal, kunnen gebruikers profiteren van de functies Meerverkoop/bijverkoop van Commerce. In dit geval verschijnen pop-upvensters tijdens het invoeren van orders en worden andere producten voorgesteld die de callcentergebruiker aan de klant kan aanbieden. De producten die worden voorgesteld, zijn gebaseerd op het product dat op de verkooporderregel is besteld. Op dit moment worden de suggesties voor meerverkoop/bijverkoop geconfigureerd op artikelniveau voor producten of catalogi. Als de instelling **Rechtstreekse verkoop inschakelen** is uitgeschakeld voor het callcenterkanaal, worden geen pop-upvensters weergegeven tijdens het invoeren van orders, zelfs niet als een geldige meerverkoop/bijverkoop is gedefinieerd voor een artikel dat wordt besteld.

Wanneer de **Rechtstreekse verkoop inschakelen** is ingeschakeld, worden ook de functies voor scripts en afbeeldingen op de invoerpagina voor de verkooporder ingeschakeld. In dit geval is een informatiedeelvenster beschikbaar aan de rechterkant van de pagina tijdens het invoeren van orders. Dit deelvenster kan scripts bevatten die zijn gerelateerd aan het generieke orderinvoerproces, de catalogusbroncode die is toegepast of scripts die zijn gerelateerd aan de bestelde artikelen. Het deelvenster met afbeeldingen kan bovendien een productafbeelding voor de bestelde artikelen weergeven als een afbeelding is gedefinieerd voor het artikel in de productinstellingen.

### <a name="enable-order-price-control"></a>Orderprijscontrole inschakelen

Wanneer de instelling **Orderprijscontrole inschakelen** wordt ingeschakeld, kunnen alleen geautoriseerde gebruikers de verkoopprijs van een artikel wijzen tijdens het invoeren van orders. De wijzigingen moet binnen de gedefinieerde marges liggen. Gebruikers die niet de juiste machtiging hebben, moeten in plaats daarvan een aanvraag voor een prijswijziging indienen. De aanvraag wordt vervolgens verwerkt via systeemwerkstromen voor beoordeling en goedkeuring.

## <a name="channel-users"></a>Kanaalgebruikers

Wanneer u het callcenterkanaal definieert, moet u kanaalgebruikers koppelen aan hun callcenter. Anders kan het callcenter niet worden gebruikt in het systeem. Wanneer gebruikers zich bij Commerce aanmelden en verkooporders of retourorders invoeren op een pagina die is gerelateerd aan het invoeren van orders, wordt hun gebruikers-id gevalideerd op basis van de configuratie van het callcenterkanaal. Als een gebruiker is gekoppeld aan een specifiek callcenterkanaal, krijgen de orders die de gebruiker maakt, de eigenschappen en standaardwaarden van dat kanaal.

Standaard wordt de markering **Verkoop** in de verkooporderkoptekst is ingeschakeld voor alle orders die callcentergebruikers maken. De orders kunnen vervolgens profiteren van de handelsspecifieke prijs- en promotiefuncties van het systeem.


Gebruikers die niet zijn gekoppeld aan een callcenterkanaal gebruiken de standaardfuncties voor orderinvoer van Microsoft Dynamics 365 Finance. Orders die deze gebruikers invoeren via het formulier Verkooporderinvoer, worden niet systematisch aangemerkt als Commerce-orders. Ook worden orders die zijn ingevoerd door deze gebruikers, niet onderworpen aan voltooiingsregels voor orderverwerking, logica voor prijzen of andere ordervalidaties die kunnen worden gedefinieerd in de configuratie van het callcenterkanaal of systeemparameters voor het callcenter.

Nadat u het callcenterkanaal hebt geconfigureerd en kanaalgebruikers hebt gedefinieerd, kunt u het gewenste systeemgedrag bevorderen door te zorgen dat alle vereiste callcenterparameters zijn gedefinieerd in **Detailhandel en commerce** \> **Kanaalinstelling** \> **Instellingen van callcenter** \> **Parameters van callcenter**. Zorg ook dat gerelateerde nummerreeksen zijn gedefinieerd.

> [!NOTE]
> Als u de functionaliteit voor callcenters wilt gebruiken, moet de configuratiesleutel voor **Meerdere verzendadressen** zijn ingeschakeld. Deze configuratiesleutel kunt u vinden in de **handelsconfiguratiesleutels** onder **Systeembeheer**\> **Instellingen** \> **Licentieconfiguratie**. Dit is vereist vanwege de callcenterfunctionaliteit die verschillende validaties uitvoert op basis van het afleveradres dat is geconfigureerd op het niveau van de verkooporderregel. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
