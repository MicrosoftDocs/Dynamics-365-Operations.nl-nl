---
title: Een wervingsproces beheren
description: In dit artikel wordt een concept beschreven dat recruiters kunnen gebruiken om de stappen in een aanwervingsproces op te volgen, waaronder inspanningen om vacatures te adverteren en sollicitanten aan te werven, het opvolgen van gegevens van sollicitanten en sollicitaties, het interviewen van sollicitanten en een of meerdere kandidaten selecteren om de openstaande posities in uw organisatie in te vullen.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6f4429202efd0506378d681188035c5cc69f56a1
ms.openlocfilehash: 551e15ed31953d6e5fc99a1177c1310194ea95d0
ms.lasthandoff: 03/31/2017


---

# <a name="manage-a-recruiting-process"></a>Een wervingsproces beheren

Dit onderwerp beschrijft een concept dat personeelswerving volgen de stappen in een organisatie voor personeelswerving proces, kunt met inbegrip van inspanningen adverteren vacatures en sollicitanten werven, sollicitant- en traceringsgegevens sollicitatiegesprekken met sollicitanten en een of meer kandidaten voor het vullen van de openstaande posities in uw organisatie selecteren.

<a name="overview"></a>Overzicht
--------

Wervingsprojecten kunnen u helpen de stappen te organiseren die u zult voltooien bij het invullen van openstaande posities in een rechtspersoon. Een sollicitant is een persoon die van toepassing voor een aanstelling voor uw onderneming is.  Een toepassing van de sollicitant expressie is van belang in een bedrijf in dienst wordt en kan worden gekoppeld aan een wervingsproject met uitdrukkelijke belang in een specifieke openen.  Een enkele sollicitant wellicht meerdere toepassingen binnen dezelfde rechtspersoon of voor meerdere bedrijven in uw organisatie.

<a name="recruitment-projects"></a>Wervingsprojecten
--------------------

Wervingsprojecten toestaan personeelswerving voor het bijhouden van voortgang ten opzichte van een of meer openstaande posities invullen.  Het wervingsproject identificeert de afdeling en de taak waarvoor één of meer posities geopend zijn. Wervingsprojecten houden ook de volgende informatie voor openstaande posities bij:
-   Het specifieke aantal openstaande posities
-   De wervingsbeheerder en een andere contactpersoon voor de positie
-   De datum waarop de bestelopdracht werd goedgekeurd
-   De sollicitatiedeadline
-   De geschatte begindatum

Het wervingsproject bevat de **Personeelsadvertentie** die wordt gebruikt op de **Werknemerselfservice** om de vacature te adverteren. Als u de vacature voor werknemers wilt weergeven, moet het wervingsproject een **Personeelsadvertentie** hebben, moet het veld** Weergeven in werknemersselfservice** op Ja zijn ingesteld, moet **Sollicitatietermijn** op een toekomstige datum zijn ingesteld en moet de **Projectstatus** van het wervingsproject op Gestart zijn ingesteld. De volgende tabel bevat de status van een project mogelijk werving en de bijbehorende beschrijvingen.

| **Status**    | **Indicates that…**                                                                  |
|-----------|------------------------------------------------------------------------------------------|
| Gepland | Werven inspanningen nu wordt voorbereid.  Werving is nog niet gestart voor dit project. |
| Gestart   | Sollicitaties worden nu geaccepteerd voor de vacatures in dit project.                    |
| Gereed  | Alle vacatures voor dit project zijn ingevuld.                                          |
| Geannuleerd  | Werving is geannuleerd voor dit project.                                           |

Recruiters kunnen ook de **Media** registreren die worden gebruikt om de vacature te adverteren via externe kanalen en **Ontwikkelingen** volgen van het project of de sollicitaties.

<a name="applicants"></a>Sollicitanten
----------

Een sollicitant is een persoon die van toepassing voor een taak in uw onderneming is.  Sollicitanten worden gedeeld door alle rechtspersonen in uw organisatie zodat u een grote groep talent wilt zoeken. U kunt competenties, referenties, accommodatieaanvragen en persoonlijke gegevens bijhouden voor sollicitanten. Wanneer u sollicitatieregistratie maakt, wordt er een persoonlijke registratie voor die sollicitant in het globale adresboek gemaakt. U kunt de pagina **Sollicitant** gebruiken voor het bijwerken van de volgende globale adresboekinformatie voor sollicitanten:
-   Adresgegevens
-   Contactgegevens
-   Identificatiegegevens
-   Details naam
-   Persoonlijke gegevens

## <a name="applications"></a>Toepassingen
U kunt informatie over ontvangen sollicitaties vastleggen op de pagina **Sollicitatie**. De toepassing is de expressie van de sollicitant van belang in een vacature in uw organisatie.  Als u wilt maken van een toepassing, moet de aanvrager al bestaan als een aanvrager of de persoon in uw systeem.
Sollicitaties die door een sollicitant via het web zijn ingediend, zijn of gerichte sollicitaties die zijn ingediend als antwoord op een vacature of ongerichte sollicitaties. Gerichte sollicitaties worden automatisch gekoppeld aan het wervingsproject waarvoor de vacature is gemaakt. Niet-gerichte sollicitaties worden gekoppeld aan het wervingsproject dat is opgegeven in het gebied **Werving** van de pagina **Human resources-parameters**.
### <a name="application-status"></a>Sollicitatiestatus

De sollicitatiestatus geeft aan waar de sollicitatie zich bevindt in het wervingsproces. De volgende tabel geeft de mogelijke sollicitatiestatussen en hun beschrijving weer.

| Status    | Geeft aan dat...                                                                           |
|-----------|-------------------------------------------------------------------------------------------|
| Ontvangen  | De sollicitatie is ontvangen.                                                             |
| Bevestigd | Er kan een mededeling worden verstuurd naar de sollicitant om de ontvangst van hun sollicitatie te bevestigen.            |
| Vraaggesprek | Een uitnodiging voor een gesprek kan naar de sollicitant worden gestuurd.                                     |
| Afwijzing | Er kan een afwijzing worden verstuurd naar de sollicitant.                                          |
| Geannuleerd  | Er kan een intrekkingsbevestiging worden verstuurd naar de sollicitant. Deze status wordt handmatig toegewezen. |
| Aangesteld  | Er kan een baanaanbieding worden verstuurd naar de sollicitant.                                         |

### <a name="correspondence-actions"></a>Correspondentieacties

Een correspondentieactie van een **Sollicitant** bepaalt de document- of e-mailsjabloon die u gebruikt om te communiceren met de sollicitant die heeft gesolliciteerd. U kunt koppelen **sollicitatiebladwijzers** met correspondentieacties zodat u kunt de waarden van de toepassing gebruiken, sollicitant, gesprek en wervingsacties project pagina's in uw communicatie met sollicitanten.  **e-mailsjabloon** kunnen worden gemaakt voor de mailingacties snel e-mailberichten naar sollicitanten met een toepassing met een bepaalde status en correspondentie actie-combinatie te kopiëren. U kunt bijvoorbeeld per e-mail een bevestiging verzenden voor alle toepassingen met een **Status** ontvangen en een **correspondentie actie** ontvangen.  U hebt de optie voor het automatisch bijwerken van de status van de toepassingen na het verzenden van het e-mailbericht.

## <a name="application-routing"></a>Sollicitatieroutering

Als een sollicitatie moet worden geëvalueerd door verschillende werknemers, kunt u met de pagina **Sollicitatieroutering** een rondzendlijst maken om het proces te beheren.

## <a name="interviews"></a>Sollicitatiegesprekken

**Sollicitatiegesprekken** kan worden gepland vanaf de **toepassingen** pagina.  Gebruik de **informatie over vergadering verzenden** knop voor het verzenden van een agenda-bestand met de planningsgegevens gesprek naar de sollicitant en de vragensteller.

## <a name="skill-mapping"></a>Vaardigheidstoewijzing

**Vaardigheidstoewijzing** en **Profielen voor vaardigheidstoewijzing** kunnen worden gebruikt om de kandidaten te identificeren die geschikt lijken voor een vacature.

## <a name="hiring-applicants"></a>Sollicitanten aannemen

Gebruik de pagina **Sollicitaties** om een sollicitant aan te stellen. Wanneer u een sollicitant aanneemt, heeft de sollicitatierecord een status van **Aangesteld** en wordt de persoonlijke registratie voor het globaal adresboek van de sollicitant gekoppeld aan de nieuwe werknemerregistratie. Wijzigingen in de globale adresboekgegevens voor nieuwe werknemersregistratie worden tevens weergegeven in de sollicitatieregistratie. Hierdoor kunt verminderen van gegevensinvoer als de nieuwe werknemer weer voor een andere baan binnen uw onderneming solliciteert.  Als u wilt een bestaande werknemer aannemen voor een nieuwe positie, klikt u op **positie wijzigen** in de **Sollicitatiestatus** neerzetten op het overdrachtsproces initialiseren.




