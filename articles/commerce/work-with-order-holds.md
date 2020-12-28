---
title: Configureren en werken met orderwachtstanden voor callcenters
description: In dit onderwerp wordt beschreven hoe u werkt met wachtstanden voor orders met behulp van Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans, MCROrderEventSetup, MCROrderEventTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b11dd48ac629910a82b4d5bfdf9889809b0d829d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411393"
---
# <a name="configure-and-work-with-call-center-order-holds"></a>Configureren en werken met orderwachtstanden voor callcenters

[!include [banner](includes/banner.md)]

Dit onderwerp beschrijft de functies voor orderwachtstanden die Dynamics 365 Commerce heeft voor callcenterorders.

## <a name="configuring-call-center-order-holds"></a>Callcenterorderwachtstanden configureren

Als u functies voor callcenterorderwachtstanden wilt gebruiken, moet u wachtstandcodes definiëren. Als u een set door de gebruiker gedefinieerde wachtstandcodes wilt maken op basis van uw zakelijke behoeften, gaat u naar **Verkoop en marketing** \> **Instellen** \> **Verkooporders** \> **Orderwachtstandcodes**. U kunt desgewenst een van de wachtstandcodes markeren als de standaardwachtstandcode door de optie **Standaard voor verkooporders** ervan op **Ja** in te stellen. Deze wachtstandcode wordt steeds gebruikt wanneer een verkooporder in de wachtstand wordt geplaatst. Als een verkooporder gereserveerde voorraad heeft en de reserveringen automatisch moeten worden verwijderd als de order in de wachtstand wordt geplaatst om een bepaalde reden, stelt u de optie **Voorraadreserveringen verwijderen** in op **Ja** voor de redencodes.

Als u het type notitie wilt opgeven dat wordt vastgelegd wanneer gebruikers die een verkooporder in de wachtstand plaatsen, optionele notities invoeren, gaat u naar **Klanten** \> **Instellen** \> **Parameters van module Klanten** en stelt u op het sneltabblad **Verkoop instellen** op het tabblad **Algemeen** het veld **Notitietype** in. Gebruik het veld **'In wachtstand'-status van de verkooporder** voor het definiëren van de kleur die wordt gebruikt voor het markeren van verkooporders die zijn geblokkeerd wanneer ze worden weergegeven op de pagina **Klantenservice**.

Als u een optionele reeks wachtstandredencodes wilt maken, gaat u naar **Detailhandel en Commerce** \> **Kanaalinstellingen** \> **Infocodes**. Deze informatiecodes kunnen worden gebruikt als een secundaire redencode om de hoofdwachtstandcode verder te definiëren. Selecteer **Nieuw** om een redencodeset te maken en selecteer vervolgens **Subcodes** om de lijst met extra redenen te definiëren. Als u informatiecodes die u definieert, wilt koppelen aan het callcenterkanaal, gaat u naar **Detailhandel en Commerce** \> **Kanalen** \> **Callcenters** \> **Alle callcenters**. Stel op het sneltabblad **Algemeen** het veld **Wachtstandcode** in.

## <a name="putting-orders-on-hold"></a>Verkooporders in de wachtstand plaatsen

Orders die callcentergebruikers maken in het back-office Commerce-programma, kunnen handmatig in de wachtstand worden geplaatst of automatisch in bepaalde situaties.

Tijdens orderinvoer, maar vóór orderindiening en bevestiging kunnen callcentergebruikers een order handmatig in de wachtstand willen plaatsen om te voorkomen dat deze wordt vrijgegeven aan het magazijn voor verdere verwerking. De klant die de order plaatst, is bijvoorbeeld niet klaar om deze in te dienen of er ontbreken belangrijke gegevens die vereist zijn om de order te verwerken.

Op de orderinvoerpagina kan de callcentergebruiker een order in de wachtstand plaatsen met de optie **Orderwachtstanden** op het tabblad **Verkooporder** van het orderinvoermenu. De gebruiker kan ook de menuoptie **Blokkeren** selecteren op de pagina **Overzicht van verkooporder** die wordt weergegeven wanneer hij of zij **Gereed** selecteert in een callcenterverkooporder.

In beide gevallen wordt de pagina **Orderwachtstanden** weergegeven. De gebruiker kan vervolgens **Nieuw** selecteren om een wachtstand voor de order te maken. In het veld **Wachtstandcode** moet de gebruiker de code selecteren die het best de reden voor de wachtstand beschrijft. In het veld **Redencode** kan de gebruiker desgewenst een aanvullende code selecteren om een tweede omschrijvingsniveau van de wachtstand te bieden.

Op het sneltabblad **Notities** kan de gebruiker in het veld **Wachtstandnotities** aanvullende, vrije notities invoeren om meer context of informatie over de wachtstand te verschaffen. Deze notities kunnen andere gebruikers helpen die later de wachtstandorder controleren of ermee werken.

Nadat de wachtstandinformatie is ingevoerd en opgeslagen, kan de gebruiker de pagina **Orderwachtstanden** sluiten. De gebruiker gaat vervolgens terug naar de verkooporderinvoerpagina. Als geen verdere acties zijn vereist voor de verkooporder, kan de gebruiker de verkooporderinvoerpagina sluiten.

Als de vlag **Ordervoltooiing inschakelen** is ingeschakeld in het callcenterkanaal, hoeft geen betaling te worden toegepast op een order die in de wachtstand staat. Voor een verkooporder die niet in de wachtstand staat kunnen gebruikers daarentegen de verkooporderinvoerpagina pas verlaten als de betaling is toegepast. Natuurlijk zal betaling vereist zijn voordat de wachtstand van de order wordt vrijgegeven.

Bovendien kunnen callcentergebruikers een handmatige fraudewachtstand plaatsen op orders die om enige reden verdacht zijn. Orders kunnen ook automatisch in de wachtstand worden geplaatst als ze overeenkomen met actieve fraudecriteria en regels. Zie voor meer informatie over dit type orderwachtstand [Fraudewaarschuwingen instellen](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts).

## <a name="viewing-and-managing-orders-that-are-on-hold"></a>Orders weergeven en beheren die in de wachtstand staan

### <a name="viewing-hold-information-for-a-single-sales-order"></a>Wachtstandinformatie weergeven voor één verkooporder

Gebruikers kunnen op de pagina **Klantenservice** visueel orders identificeren die in de wachtstand staan, omdat de orderregels in een specifieke kleur worden gemarkeerd. Deze kleur wordt gedefinieerd door het veld **'In wachtstand'-status van de verkooporder** op de pagina **Parameters van module Klanten**.

> [!NOTE]
> Als de regel is geselecteerd op de pagina, is de markeringskleur niet zichtbaar.

Gebruikers kunnen ook gedetailleerde statusinformatie voor een verkooporder weergeven om te weten of de order in de wachtstand staat. De gedetailleerde statusinformatie kan worden geopend vanaf de pagina **Alle verkooporders** of **Klantenservice**. Als een order in de wachtstand staat, is de vlag **Niet verwerken** ervoor ingesteld en bevat het veld **Gedetailleerde status** **In wachtstand** of **Fraudewachtstand**, afhankelijk van het scenario.

Als ze de details willen weergeven van een afzonderlijke orderwachtstand, kunnen ze een gedetailleerde weergave van de pagina **Orderwachtstand** openen vanaf de pagina **Klantenservice**, met behulp van het menu **Opties** voor de geselecteerde order. Gebruikers hebben ook toegang tot deze weergave vanuit de pagina **Alle verkooporders** door de menuoptie **Orderwachtstanden** te selecteren op het tabblad **Verkooporder**.

### <a name="viewing-all-orders-that-are-on-hold"></a>Alle orders weergeven en beheren die in de wachtstand staan

Als u alle orders wilt weergeven die handmatig of automatisch in de wachtstand zijn gezet, gaat u naar **Detailhandel en commerce** \> **Klanten** \> **Orderwachtstanden**.

De workbench **Orderwachtstanden** biedt een lijstweergave van alle orders die in de wachtstand staan vanwege handmatige of aan fraude gerelateerde wachtstandacties. Door gebruik te maken van standaardopties voor filteren en sorteren op de pagina kunnen gebruikers weergaven maken waarmee ze met specifieke wachtstandcodes kunnen werken of beheren voor de controle waarvan ze verantwoordelijk zijn. De workbench **Orderwachtstanden** geeft ook het aantal dagen aan dat een order in de wachtstand staat. Deze informatie kan gebruikers helpen de wachtrij te prioriteren.

Als ze een gedetailleerdere weergave van de orders in de wachtstand willen, kunnen gebruikers op de optie **Orderwachtstand** klikken in het menu. Deze weergave biedt informatie over de klant, notities die op de order zijn toegepast, klant- of wachtstandacties. De weergave biedt ook details over de reden voor een automatische wachtstand als de order in de wachtstand is geplaatst omdat deze overeenkwam met een frauderegel.

In de lijstweergave en de gedetailleerde weergave van de pagina **Orderwachtstanden** kunnen gebruikers extra ordergerelateerde informatie weergeven of bewerken, zoals betalingen, totalen en notities.

De opties op het tabblad **Uitchecken in wachtstand** kunnen nuttig zijn als meerdere gebruikers in uw bedrijf tegelijkertijd aan de wachtstandwachtrij werken. Door de optie **Uitchecken** te selecteren kunnen gebruikers aangeven dat ze werken aan de controle en het onderzoek van de orderwachtstand. Op deze manier verspillen andere gebruikers geen tijd door te proberen het hetzelfde werk te doen. In de gedetailleerde weergave van de pagina **Orderwachtstanden** kunnen gebruikers informatie weergeven over de uitcheckdatum en -tijd en over de gebruiker die de wachtstandrecord heeft uitgecheckt.

Nadat een wachtstandrecord is uitgecheckt, kan alleen de gebruiker die deze heeft uitgecheckt het uitchecken wissen. Deze beperking is bedoeld om te voorkomen dat gebruikers records nemen waarmee andere gebruikers al bezig zijn. Als u een order weer wilt vrijgeven aan de wachtrij, zodat andere gebruikers eraan kunnen werken, selecteert de gebruiker die de record heeft uitgecheckt, de optie **Uitchecken wissen**.

> [!NOTE]
> De wachtstand wordt niet vrijgegeven wanneer het uitchecken wordt gewist.

In sommige situaties, zoals wanneer een gebruiker ziek afwezig is of het bedrijf heeft verlaten, moeten uitgecheckte records mogelijk worden toegewezen aan een andere gebruiker. Een manager kan records opnieuw toewijzen met de optie **Uitchecken overschrijven**.

## <a name="releasing-orders-that-are-on-hold"></a>Orders vrijgeven die in de wachtstand staan

In de lijstweergave en de gedetailleerde weergave van de pagina **Orderwachtstanden** bevat het tabblad **Wachtstand wissen** de opties die worden gebruikt om een orderwachtstand vrij te geven. Gebruik de optie **Wachtstanden wissen** om een order vrij te geven van de geselecteerde wachtstandcode.

Callcenterorders vereisen betaling. Daarom kan een wachtstand niet volledig worden gewist als geen betaling op de order is toegepast. Zorg op de pagina **Parameters van callcenter** op het tabblad **Blokkeringen** dat de parameter **Indienen wanneer gewist** is ingeschakeld. Deze instelling helpt zorgen dat een vrijgegeven wachtstandorder de juiste logica voor orderindiening doorloopt om betalingen te valideren en autoriseren. Als betalingen ontbreken, krijgt de gebruiker een fout en wordt de wachtstandcode niet gewist.

Als de parameter **Indienen wanneer gewist** niet is ingesteld, moeten gebruikers de optie **Wissen en indienen** in het menu **Wachtstand wissen** selecteren om te helpen garanderen dat de order alle vereiste betalingsvalidaties doorloopt. Als de orderindiening mislukt wanneer de vlag **Ordervoltooiing inschakelen** is ingeschakeld in het callcenterkanaal, wordt de order vrijgegeven uit de wachtstandstatus, maar blijft de vlag **Niet verwerken** ingesteld. De order wordt daarom niet vrijgegeven uit het magazijn totdat de juiste betalingen zijn toegepast en gevalideerd.

Als gebruikers een wachtstand willen wissen maar aanvullende wijzigingen in de order willen aanbrengen voordat deze wordt vrijgegeven voor verdere verwerking, kunnen ze de optie **Wissen en aanpassen** selecteren. Met deze optie wordt de wachtstandcode verwijderd en worden de verkooporderdetails geopend zodat gebruikers extra wijzigingen aan de order aanbrengen kunnen. Gebruikers kunnen ook betaling vereffenen en de verkooporder indienen via logica voor betalingsvalidatie wanneer de vlag **Ordervoltooiing schakelen** is ingeschakeld in het callcenterkanaal.

## <a name="reporting-options"></a>Rapportageopties

Ga naar **Detailhandel en commerce** \> **Query's en rapporten** \> **Callcenterrapporten** \> **Rapport Orderwachtstanden** als u een rapport wilt uitvoeren over orderwachtstanden op datumbereik, wachtstandcode of andere gerelateerde criteria.
