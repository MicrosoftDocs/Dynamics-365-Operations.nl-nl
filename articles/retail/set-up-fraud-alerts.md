---
title: Fraudewaarschuwingen instellen
description: "Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt. U kunt speciale codes definiëren die automatisch of handmatig verdachte orders stopzetten."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Fraudewaarschuwingen instellen

[!include[banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u criteria en regels instelt om mogelijk frauduleuze verkooporders in de wachtstand te plaatsen voor verder onderzoek. De functie voor fraudebeoordeling wordt gebruikt om de geldigheid van de gegevens in een verkooporder te bepalen. Als de informatie in de verkooporder dubieus lijkt op basis van de fraudecriteria en -regels van een organisatie, kan de order door een beheerder in de wachtstand worden geplaatst voor nader onderzoek.

> [!NOTE]
> Deze functie kan alleen worden gebruikt met de functie voor verkooporderverwerking in Callcenterafzetkanaal. 

Als het callcenterafzetkanaal is gedefinieerd, moet **Ordervoltooiing inschakelen** worden ingesteld op **Ja**. Wanneer ordervoltooiing is ingeschakeld, kunnen gebruikers de samenvatting van de order bekijken en op **Indienen** klikken om de order te voltooien. Gebruikers kunnen de verkooporder ook handmatig in de wachtstand plaatsen voor fraudebeoordeling. Verkooporders die door een callcentergebruiker worden ingetoetst, worden tijdens het indieningsproces verwerkt op basis van fraudecontroleregels en -criteria.

Er zijn twee soorten fraudecriteria die door het systeem worden gebruikt om te controleren of de order moet worden vastgehouden voor fraudebeoordeling:

-   **Statische regels** gebruiken een specifieke waarde, zoals een telefoonnummer dat op een zwarte lijst is geplaatst of een e-mailadres dat is gemarkeerd omdat het in het verleden is gebruikt voor frauduleuze transacties. Op de pagina **Statische fraudegegevens** kunnen fraudegegevens handmatig worden toegevoegd of via een gegevensimport, waarbij scores worden gekoppeld aan de frauduleuze informatie. Als fraudecontrole is ingeschakeld, wordt elke ingevoerde verkooporder vergeleken met de statische gegevens. Als de gegevens in het factuur- of afleveradres van de klant worden gevonden, of als de gegevens worden gevonden in het afleveradres op de verkoopregel, worden de scores van alle unieke resultaten getotaliseerd.  
-   **Dynamische regels** bestaan uit variabelen en gedefinieerde voorwaarden voor die variabelen. Met dynamische regels kunnen andere criteria worden gecontroleerd die niet zijn gedefinieerd in de statische regels. Complexere EN/OF-instructies kunnen worden gebruikt als u meerdere voorwaarden wilt gebruiken om te bepalen of er een overeenkomst bestaat op basis van de regelcriteria en de verkooporder die wordt ingediend. Als een gebruiker in het kader van fraudebeoordeling bijvoorbeeld alle orders wil vasthouden voor klanten die aan een specifieke klantgroepwaarde zijn gekoppeld en die een specifiek product hebben besteld, worden de voorwaarden om klanten en producten te valideren op de pagina **Regels** gedefinieerd met een EN-voorwaarde. De order wordt alleen vastgehouden voor fraudebeoordeling als beide voorwaarden waar zijn en de totale fraudescore van de order door de toegewezen score boven de minimale fraudescore, zoals gedefinieerd in de callcenterparameters, uitkomt.

Een callcentergebruiker kan een order ook handmatig in de wachtrij voor de fraudewachtstand zetten. Als de gebruiker die de order invoert de klant die de order plaatst van fraude verdenkt en wil dat iemand anders de geldigheid van de order onderzoekt voordat deze wordt verwerkt, kan de gebruiker die de order invoert de optie **Handmatige fraudewachtstand** in het vervolgkeuzemenu **Blokkeringen** op de pagina **Overzicht van verkooporder** selecteren (deze pagina wordt weergegeven als de orderfunctie **Voltooien** wordt aangeroepen). De gebruiker wordt gevraagd verder toe te lichten waarom hij of zij fraude vermoedt, zodat de controleur meer context heeft.

Alle orders die handmatig of op basis van een systematische berekening van fraudescores in de fraudewachtstand zijn geplaatst, worden weergegeven op de pagina **Orderwachtstanden**. Hier kan de order worden gecontroleerd en vervolgens worden geannuleerd of vrijgegeven voor verwerking.

> [!NOTE]
> Het gebruik van meerdere of te complexe regels leidt tot slechte systeemprestaties wanneer verkooporders worden ingediend. De functie voor fraudewaarschuwingen is niet geoptimaliseerd voor het verwerken van grote hoeveelheden statische fraudegegevens en veel actieve regels. Het is belangrijk om te weten dat elke regel wordt geëvalueerd tijdens de functie voor het indienen van de verkooporderinvoer via het callcenter. De regels worden geëvalueerd op basis van de verkooporderkoptekst en alle orderregels. De verwerking duurt langer bij een groter aantal regels en complexere regelinstructies. Als uw order een groot aantal regelartikelen en een groot aantal actieve regels en statische gegevensitems bevat, kan dit systematische proces van beoordeling en validering van alle gegevens en het berekenen van een fraudescore de prestaties sterk beïnvloeden.  Organisaties die deze functie gebruiken, moeten altijd testen of de verwerkingstijd van orderindieningen acceptabel is voordat ze wijzigingen op regels of statische fraudecriteria toepassen in de productieomgeving.

