---
title: Wervingsprocessen beheren
description: In dit artikel wordt een concept beschreven dat recruiters kunnen gebruiken om de stappen in een wervingsproces bij te houden.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMApplication, HRMRecruitingTable
audience: Application User
ms.reviewer: anbichse
ms.custom: 7501
ms.assetid: 1ad725bf-20e2-42a1-8068-111f7ddddad9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adf873a58900fa86d068d9ebc75f4f389e7d8359cc685d4635e083437c55ae56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752985"
---
# <a name="manage-recruiting-processes"></a>Wervingsprocessen beheren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt een concept beschreven dat recruiters kunnen gebruiken om de stappen in een aanwervingsproces op te volgen, waaronder inspanningen om vacatures te adverteren en sollicitanten aan te werven, het opvolgen van gegevens van sollicitanten en sollicitaties, het interviewen van sollicitanten en een of meerdere kandidaten selecteren om de openstaande posities in uw organisatie in te vullen.

## <a name="overview"></a>Overzicht

Wervingsprojecten kunnen u helpen de stappen te organiseren die u zult voltooien bij het invullen van openstaande posities in een rechtspersoon. Een sollicitant is een persoon die solliciteert op een dienstverband in uw onderneming. De sollicitatie is een blĳken van belangstelling van een sollicitant om in dienst van een bedrijf te werken en kan gekoppeld zijn aan een wervingsproject om blijk te geven van belangstelling voor een specifieke vacature. Eén sollicitant kan meerdere sollicitaties binnen dezelfde rechtspersoon of verdeeld over meerdere bedrijven in uw organisatie hebben.

## <a name="recruitment-projects"></a>Wervingsprojecten

Dankzij wervingsprojecten kunnen recruiters de voortgang voor het invullen van een of meer openstaande posities volgen. Het wervingsproject identificeert de afdeling en de functie waarvoor één of meerdere posities openstaan. Wervingsprojecten houden ook de volgende informatie voor openstaande posities bij:

- Het specifieke aantal openstaande posities
- De wervingsbeheerder en een andere contactpersoon voor de positie
- De datum waarop de bestelopdracht werd goedgekeurd
- De sollicitatiedeadline
- De geschatte begindatum

Het wervingsproject bevat de **Personeelsadvertentie** die wordt gebruikt op de **Werknemerselfservice** om de vacature te adverteren. Als u de vacature voor werknemers wilt weergeven, moet het wervingsproject een **Personeelsadvertentie** hebben, moet het veld **Weergeven in werknemersselfservice** op Ja zijn ingesteld, moet **Sollicitatietermijn** op een toekomstige datum zijn ingesteld en moet de **Projectstatus** van het wervingsproject op Gestart zijn ingesteld. De volgende tabel geeft de mogelijke wervingsprojectstatussen en hun beschrijving weer.

| Status    | Geeft aan dat...                                                                         |
|-----------|-----------------------------------------------------------------------------------------|
| Gepland | Inspanningen voor werving worden voorbereid. Werving is nog niet gestart voor dit project. |
| Gestart   | Sollicitaties worden nu geaccepteerd voor de vacatures in dit project.                   |
| Gereed  | Alle vacatures voor dit project zijn ingevuld.                                         |
| Geannuleerd  | Werving is geannuleerd voor dit project.                                          |

Recruiters kunnen ook de **Media** registreren die worden gebruikt om de vacature te adverteren via externe kanalen en **Ontwikkelingen** volgen van het project of de sollicitaties.

## <a name="applicants"></a>Sollicitanten

Een sollicitant is een persoon die solliciteert op een functie in uw onderneming. Sollicitanten worden gedeeld door alle rechtspersonen in uw organisatie zodat u een grote verzameling van talent krijgt waarin u kunt zoeken. U kunt competenties, referenties, accommodatieaanvragen en persoonlijke gegevens bijhouden voor sollicitanten. Wanneer u sollicitatieregistratie maakt, wordt er een persoonlijke registratie voor die sollicitant in het globale adresboek gemaakt. U kunt de pagina **Sollicitant** gebruiken voor het bijwerken van de volgende globale adresboekinformatie voor sollicitanten:

- Adresgegevens
- Contactgegevens
- Identificatiegegevens
- Details naam
- Persoonlijke gegevens

## <a name="applications"></a>Toepassingen

U kunt informatie over ontvangen sollicitaties vastleggen op de pagina **Sollicitatie**. De sollicitatie is de blijken van belangstelling van de sollicitant in een vacature in uw organisatie. Om een sollicitatie te maken, moet de sollicitant al als sollicitant of persoon in uw systeem voorkomen.

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

Een correspondentieactie van een **sollicitant** bepaalt de document- of e-mailsjabloon die u gebruikt om te communiceren met de sollicitant die heeft gesolliciteerd. U kunt **Sollicitatiebladwijzers** koppelen aan correspondentieacties zodat u waarden van de pagina's Sollicitatie, Sollicitant, Gesprek en Wervingsproject kunt gebruiken in uw communicatie met sollicitanten. **E-mailsjabloon** kan voor de correspondentieacties worden gemaakt om snel e-mails te verzenden naar sollicitanten die een sollicitatie hebben met een bepaalde combinatie van status en correspondentieactie. U kunt bijvoorbeeld een bevestigings-e-mail verzenden naar alle sollicitaties met de **Status** van Ontvangen en een **Correspondentieactie** van Ontvangen. Na het verzenden van de e-mail hebt u de optie om de status van de sollicitaties automatisch bij te werken.

## <a name="application-routing"></a>Sollicitatieroutering

Als een sollicitatie moet worden geëvalueerd door verschillende werknemers, kunt u met de pagina **Sollicitatieroutering** een rondzendlijst maken om het proces te beheren.

## <a name="interviews"></a>Sollicitatiegesprekken

**Sollicitatiegesprekken** kunnen worden gepland via de pagina **Sollicitaties**. Gebruik de knop **Vergaderingsgegevens verzenden** om een kalenderbestand met de planningsinformatie van het gesprek naar de sollicitant en de interviewer te verzenden.

## <a name="skill-mapping"></a>Vaardigheidstoewijzing

**Vaardigheidstoewijzing** en **Profielen voor vaardigheidstoewijzing** kunnen worden gebruikt om de kandidaten te identificeren die geschikt lijken voor een vacature.

## <a name="hiring-applicants"></a>Sollicitanten aannemen

Gebruik de pagina **Sollicitaties** om een sollicitant aan te stellen. Wanneer u een sollicitant aanneemt, heeft de sollicitatierecord de status **Aangesteld** en wordt de persoonlijke registratie voor het globale adresboek van de sollicitant gekoppeld aan de nieuwe werknemerregistratie. Wijzigingen in de globale adresboekgegevens voor nieuwe werknemersregistratie worden tevens weergegeven in de sollicitatieregistratie. Dit kan helpen bij het verminderen van gegevensinvoer als de nieuwe werknemer weer solliciteert voor een andere baan binnen uw onderneming. Om een bestaande werknemer voor een andere positie aan te werven, klikt u op **Positie wijzigen** in de vervolgkeuzelijst **Sollicitatiestatus** om het overdrachtsproces te starten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]