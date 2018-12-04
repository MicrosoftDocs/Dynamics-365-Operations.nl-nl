---
title: Samenwerken met leveranciers met behulp van de leveranciersportal
description: In dit onderwerp wordt uitgelegd hoe inkoopmedewerkers de leveranciersportal kunnen gebruiken om tijdens het inkooporderbevestigingsproces samen te werken met externe leveranciers. Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2fa152c5586a1122a109762780d23fd8c2240702
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="collaborate-with-vendors-by-using-the-vendor-portal"></a>Samenwerken met leveranciers met behulp van de leveranciersportal

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe inkoopmedewerkers de leveranciersportal kunnen gebruiken om tijdens het inkooporderbevestigingsproces samen te werken met externe leveranciers. Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.

De informatie in dit onderwerp geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX. De functionaliteit Leveranciersportal is vervangen door de verbeterde functionaliteit voor leverancierssamenwerking in Dynamics 365 for Operations versie 1611. Meer informatie over de nieuwe functionaliteit voor leverancierssamenwerking vindt u in [Leverancierssamenwerking gebruiken voor het werken met externe leveranciers](vendor-collaboration-work-external-vendors.md).  

De leveranciersportal is bedoeld voor leveranciers die geen EDI-integratie (Electronic Data Interchange) met Microsoft Dynamics AX hebben voor het uitwisselen van inkoopordergegevens. Met de portal kunnen inkoopmedewerkers een IO (inkooporder) sturen naar de leverancier en vervolgens direct een antwoord met de status Bevestigd of Afgewezen in Dynamics AX ontvangen.  

Het proces kan zo worden geconfigureerd dat de order automatisch met een bevestiging van de leverancier wordt bevestigd. In dit geval is opvolging alleen af en toe is vereist wanneer een order wordt geweigerd of als de bevestiging van de leverancier wordt geregistreerd als een antwoord, maar de status van de inkooporder niet wordt bijgewerkt in **Bevestigd** vanwege een probleem tijdens het bevestigingsproces.

## <a name="po-confirmation-and-rejection"></a>Bevestiging en afwijzing van inkooporder
Inkooporders worden voorbereid in Dynamics AX. Wanneer u een inkooporder hebt met de status **Goedgekeurd**, verzendt u deze naar de leverancier door een bevestigingsaanvraag te genereren. Als u de aandacht van de leverancier naar de nieuwe inkooporder wilt trekken, kunt u de inkooporder ook via e-mail verzenden met behulp van het afdrukbeheersysteem. De inkooporder wordt weergegeven in de leveranciersportal en bevat een optie die de leverancier kan gebruiken om de inkooporder te bevestigen of af te wijzen. De leverancier kan ook opmerkingen toevoegen om informatie zoals wijzigingen in de inkooporder door te geven.  

In de leveranciersportal kan de leverancier orderregels zien. Deze regels bevatten informatie zoals extern productnummer, afmetingen, prijsgegevens, hoeveelheid, leverdatum en afleveradres. De leverancier kan een rapport genereren waarin de inkoopordergegevens en ook de totale prijs worden weergegeven. Toeslagen relevant voor de leverancier worden weergegeven als de leverancier op de knop **Toeslagen** in de koptekst of op de regels klikt. Leveranciers kunnen IO-gegevens in hun eigen systeem importeren met de functionaliteit **Exporteren Naar Excel**.  

De volgende tabel bevat de normale uitwisseling van gegevens, afhankelijk van de wijze waarop de leverancier reageert wanneer u een IO stuurt voor bevestiging.

| Type antwoord                                                                                                  | Resultaat                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De leverancier bevestigt de order. Het systeem is geconfigureerd om PO´s automatisch te bevestigen wanneer de leverancier bevestigt.    | De status van de order verandert in **Bevestigd**. Als bijwerking van de order door iets wordt voorkomen, wordt het antwoord van de leverancier wel geregistreerd als **Bevestigd**, maar blijft de inkooporder de status **Externe controle** behouden.                                                                       |
| De leverancier bevestigt de order. Het systeem is niet geconfigureerd om PO´s automatisch te bevestigen wanneer de leverancier bevestigt. | Het leveranciersantwoord wordt geregistreerd als **Bevestigd**, maar de inkooporder behoudt de status **Externe controle**.                                                                                                                                                                                      |
| De leverancier wijst de order af.                                                                                     | Het leveranciersantwoord wordt geregistreerd als **Afgewezen**, maar de inkooporder behoudt de status **Externe controle**. De afwijzing wordt ontvangen samen met de reden en een voorstel voor wijziging, zoals een alternatieve leveringsdatum. U kunt de inkooporder bijwerken en vervolgens een nieuwe versie voor bevestiging verzenden. |

## <a name="changes-to-a-po"></a>Wijzigingen in een inkooporder
Wanneer u een inkooporder moet wijzigen die al is bevestigd, kunt u een nieuwe inkooporder naar de leverancier verzenden via de leveranciersportal. De nieuwe inkooporder heeft een versieachtervoegsel om aan te geven dat het om een gewijzigde versie van een inkooporder gaat die eerder is doorgegeven. Met de leveranciersportal kunnen leveranciers de historie van elke order volgen. De eerder bevestigde versie van de inkooporder blijft in de lijst met bevestigde PO´s tot de nieuwe inkooporder is bevestigd.  

Wanneer u een inkooporder annuleert, wordt de status weer gewijzigd in **Goedgekeurd**. U moet de inkooporder via de leveranciersportal terug naar de leverancier sturen zodat de leverancier de annulering kan bevestigen of afwijzen. Nadat de annulering is bevestigd, wordt de inkooporder in de lijst met bevestigde PO´s van de leverancier weergegeven als **Geannuleerd**.

## <a name="versions-status-transitions-and-change-management"></a>Versies, statusovergangen en wijzigingsbeheer
Wanneer een inkooporder naar de leverancier wordt verzonden, wordt deze in het systeem geregistreerd als een specifieke versie van de inkooporder en wordt de status gewijzigd van **Goedgekeurd** in **Externe controle**. Als de inkooporder later wordt gewijzigd, wordt een nieuwe versie van de inkooporder gemaakt en verandert de status weer in **Goedgekeurd** (of de status verandert in **Concept** als wijzigingsbeheer is ingeschakeld).  

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat.

| Actie                                                   | Status en versie                                                                                    |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| De oorspronkelijke versie van de IO is gemaakt in Dynamics AX. | De status is **Goedgekeurd**.                                                                           |
| De IO is verzonden naar de leveranciersportal.                     | Er wordt een versie geregistreerd in de leveranciersportal en de status wordt gewijzigd in **Externe controle**.    |
| U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd.  | De status wordt weer gewijzigd in **Goedgekeurd**.                                                            |
| U verzendt de nieuwe versie van de inkooporder naar de leveranciersportal. | Er wordt een nieuwe versie geregistreerd in de leveranciersportal en de status wordt gewijzigd in **Externe controle**. |
| De leverancier keurt de nieuwe versie van de inkooporder goed           | De status wordt gewijzigd in **Bevestigd**.                                                                |

Als u de naar de leverancier verzonden versies van de inkooporder en de antwoorden van de leverancier wilt bekijken, klikt u op **Journalen** &gt; **Bevestigingsaanvragen** van de inkooporder.  

Orders die voor een antwoord naar de leverancier zijn verzonden en de status **Externe controle** hebben, worden weergegeven in de lijst **Inkooporders die naar de leveranciersportal zijn verzonden, in afwachting van antwoord** of in de lijst **Inkooporders die naar de leveranciersportal zijn verzonden, antwoord vereist actie**. Wanneer u een order wijzigt die naar de leverancier is verzonden, zodat de status weer wordt gewijzigd in **Goedgekeurd**, wordt deze niet meer in deze lijsten weergegeven. Als u wilt zien of de leverancier eerder op de order heeft gereageerd, klikt u op **Journalen** &gt; **Bevestigingsaanvragen**.  

Leveranciers hoeven de inkooporder niet in de leveranciersportal te bevestigen. Ze kunnen ook een e-mailbericht verzenden of hun acceptatie van een inkooporder via andere kanalen laten weten. U kunt de order vervolgens handmatig in Dynamics AX bevestigen. In dit geval ontvangt u een waarschuwing dat de order wordt bevestigd zelfs als er geen antwoord van de leverancier is. De inkooporder wordt vervolgens in de bevestigingshistorie in de leveranciersportal weergegeven als een openstaande bevestigde order die geen antwoorden heeft. Daarnaast heeft de leverancier niet meer de mogelijkheid om de inkooporder te bevestigen of af te wijzen.  

**Opmerking:** de versie van de inkooporder die beschikbaar is voor andere processen in Dynamics AX, is altijd de laatste versie zelfs als deze versie nog niet is geregistreerd.

### <a name="change-management"></a>Wijzigingsbeheer

Als u wijzigingsbeheer hebt ingeschakeld voor een inkooporder, doorloopt de inkooporder een goedkeuringsworkflow om de status **Goedgekeurd** te bereiken. Dit proces is niet zichtbaar voor de leverancier.  

Wanneer wijzigingsbeheer voor een inkooporder is ingeschakeld, wordt de versie geregistreerd wanneer de inkooporder wordt goedgekeurd, niet wanneer de inkooporder naar de leverancier wordt verzonden of wordt bevestigd.  

De volgende tabel bevat een voorbeeld van de status- en versiewijzigingen die een inkooporder mogelijk ondergaat als wijzigingsbeheer is ingeschakeld.


|                                                    Actie                                                     |                                                                                                                                                                                                                      Status en versie                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           De oorspronkelijke versie van de IO is gemaakt in Dynamics AX.                            |                                                                                                                                                                                                            De status is <strong>Concept</strong>.                                                                                                                                                                                                             |
| De IO wordt verzonden naar het goedkeuringsproces. (Dit is een intern proces waarin de leverancier niet is betrokken.) |                                                                                                                        De status wordt gewijzigd van <strong>Concept</strong> in <strong>Wordt gecontroleerd</strong> in <strong>Goedkeuring</strong> als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. De goedgekeurde inkooporder wordt geregistreerd als een versie.                                                                                                                        |
|                                      De IO is verzonden naar de Leveranciersportal.                                      |                                                                                                                                                                      De versie wordt geregistreerd in de leveranciersportal en de status wordt gewijzigd in <strong>Externe controle</strong>.                                                                                                                                                                       |
|                            U brengt enkele wijzigingen aan die door de leverancier zijn aangevraagd.                            |                                                                                                                                                                                                    De status wordt weer gewijzigd in <strong>Concept</strong>.                                                                                                                                                                                                     |
|                              De IO wordt weer naar het goedkeuringsproces verzonden.                               | De status wordt gewijzigd van <strong>Concept</strong> in <strong>Wordt gecontroleerd</strong> in <strong>Goedkeuring</strong> als de inkooporder niet tijdens het goedkeuringsproces wordt afgewezen. Het systeem kan ook zo worden geconfigureerd dat voor bepaalde veldwijzigingen geen nieuwe goedkeuring is vereist. In dit geval wordt de status eerst gewijzigd in <strong>Concept</strong> en vervolgens automatisch bijgewerkt in <strong>Goedgekeurd</strong>. De goedgekeurde inkooporder wordt geregistreerd als een nieuwe versie. |
|                           U verzendt de nieuwe versie van de inkooporder naar de leveranciersportal.                            |                                                                                                                                                                    De nieuwe versie wordt geregistreerd in de leveranciersportal en de status wordt gewijzigd in <strong>Externe controle</strong>.                                                                                                                                                                     |
|                                De leverancier keurt de nieuwe versie van de inkooporder goed                                 |                                                                                                                                                     De status wordt gewijzigd in <strong>Bevestigd</strong>. Dit gebeurt automatisch of wanneer u het antwoord van de leverancier ontvangt en vervolgens de inkooporder bevestigt.                                                                                                                                                     |

<a name="additional-resources"></a>Aanvullende resources
--------

[Configuratie van de beveiliging voor gebruikers van de leveranciersportal](configure-security-vendor-portal-users.md)

[Werkgebied voor samenwerkingsfacturering van leveranciers](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md)




