---
title: Uitgavencontroleurs configureren
description: In dit onderwerp wordt beschreven hoe uitgavencontroleurs worden gebruikt om dynamisch de gebruiker te selecteren aan wie een werkstroomtaak, goedkeuring of handmatige beslissing is toegewezen.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070141"
---
# <a name="configure-expenditure-reviewers"></a>Uitgavencontroleurs configureren
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

U kunt dynamische uitgavencontroleurs instellen om uitgaven door te sturen ter beoordeling op basis van de gebruiker die aan een projectrol is toegewezen of de financiële dimensie waar de uitgave wordt aangerekend. Het workflowproces gebruikt de opgegeven projectrol of eigenaar van de financiële dimensie om te bepalen naar wie de uitgave moet worden doorgestuurd.

U kunt een of meer configuraties voor uitgavencontroleurs definiëren en vervolgens een configuratie selecteren wanneer u een werkstroom maakt. U kunt de waarden voor de uitgavencontroleurs configureren voor elke rechtspersoon in uw organisatie. Nadat u de configuraties voor uitgavencontroleurs hebt gedefinieerd, wijst u de configuratie toe. Uitgavencontroleurs kunnen worden toegewezen aan werkstroomtaken, goedkeuringen en handmatige beslissingen.

> [!NOTE]
> Hoewel uitgavencontroleurs niet verplicht zijn, kunnen ze de configuratie van uw werkstroom helpen vereenvoudigen. U hoeft bijvoorbeeld geen voorwaardelijke beslissing te maken om te controleren voor elke kostenplaatsdimensie en vervolgens een ander element te maken om de goedkeuring of taak toe te wijzen aan een specifieke gebruiker of groepen van gebruikers. In plaats daarvan kunt u de eigenaar van de kostenplaatsdimensie configureren en een uitgavencontroleur gebruiken om op dynamische wijze de juiste gebruiker te selecteren. Op deze manier hoeft u, wanneer het eigendom of de toewijzing van kostenplaatsen verandert, alleen het veld **Eigenaar** voor de financiële dimensie bijwerken.

## <a name="types-of-expenditure-reviewers"></a>Typen uitgavencontroleurs

Niet alle werkstromen ondersteunen het concept van uitgavencontroleurs. Standaard kunt u uitgavencontroleurs configureren voor opdrachten tot inkoop, inkooporders, leveranciersfacturen en onkostennota's. Elk van deze werkstroomtypen vereist dat u de uitgavencontroleurs configureert op een aparte pagina die specifiek is voor de functie en module. Voor elk ondersteund document kunnen uitgavencontroleurs worden gebruikt met werkstromen op koptekstniveau of werkstromen op regelniveau.

De volgende tabel laat zien waar u naartoe gaat om een uitgavencontroleur te configureren voor elk ondersteund document.

| Document | Navigatiepad |
|----------|-----------------|
| Onkostennota's | Onkostenbeheer \> Instellingen \> Beleid \> Uitgavencontroleurs |
| Inkooporders | Inkoopbeheer \> Instellingen \> Beleid \> Uitgavencontroleurs voor inkooporders |
| Opdrachten tot inkoop | Inkoopbeheer \> Instellingen \> Beleid \> Uitgavencontroleurs voor opdrachten tot inkoop |
| Leveranciersfacturen | Ga naar Leveranciers \> Beleidsinstelling \> Uitgavencontroleurs voor leveranciersfacturen |

## <a name="expenditure-reviewer-assignments"></a>Toewijzingen van uitgavencontroleurs

Er zijn twee typen toewijzing beschikbaar voor elke uitgavencontroleur: *projectverdelingen* en *organisatieverdelingen*. Voor een projectverdeling kunt u kiezen tussen projectinstanties en financiële dimensies. Voor een organisatieverdeling kunt u financiële dimensies selecteren.

Projectinstanties omvatten de projectmanager, projectcontroleur en projectverkoopleider. U definieert deze instanties direct voor uw project door een medewerker te selecteren in de juiste velden.

Financiële dimensies worden beheerd door de rekeningstructuren in elke rechtspersoon. Voor elke rechtspersoon kunt u selecteren welke financiële dimensies worden gebruikt met de uitgavencontroleur. De dimensies kunnen afkomstig zijn van het project (in dit geval selecteert u de dimensies op het tabblad **Projectverdelingen**) of het document (in dit geval selecteert u de dimensies op het tabblad **Organisatieverdelingen**). In het veld **Eigenaar** op de pagina **Financiële dimensiewaarden** kunt u de medewerker selecteren voor elke financiële dimensie.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Voorbeeld 1: uitgavencontroleurs op basis van organisatieverdelingen

U werkt voor Contoso Appliances en uw organisatie heeft zes afdelingen en 10 kostenplaatsen. Wanneer een nieuwe opdracht tot inkoop wordt ingediend, moet eerst goedkeuring worden verleend door de afdelingsmanager en vervolgens door de kostenplaatsmanager.

Voor dit voorbeeld configureert u twee *uitgavencontroleurs voor opdrachten tot inkoop*:

- Voor de eerste controleur geeft u de afdeling een naam en selecteert u vervolgens de financiële dimensie **Afdeling** op het tabblad **Organisatieverdelingen**. 
- Voor de tweedte controleur geeft u de kostenplaats een naam en selecteert u vervolgens de financiële dimensie **Kostenplaats** op het tabblad **Organisatieverdelingen**.

Wanneer u de werkstroom configureert, maakt u twee goedkeuringsstappen. De eerste is voor de afdeling en de tweede voor de kostenplaats. Voor elk goedkeuringselement selecteert u **Deelnemer** in het veld **Toewijzingstype** op het tabblad **Rolgebaseerd**, selecteert u **Uitgavendeelnemers** in het veld **Type deelnemer** en selecteert u vervolgens de desbetreffende deelnemer in het veld **Deelnemer**.

Wanneer de opdracht tot inkoop wordt gemaakt, worden de financiële dimensies afdeling en kostenplaats toegewezen aan de regels van de opdracht tot inkoop. Wanneer de werkstroom wordt ingediend, evalueert het systeem eerst de afdeling op de opdracht tot inkoop en wijst het goedkeuringselement toe aan de gebruiker die betrekking heeft op de medewerker die u voor de afdeling hebt geselecteerd. Nadat de eerste goedkeuringsstap is voltooid, evalueert het systeem de tweede goedkeuringsstap en wijst het tweede goedkeuringselement toe aan de gebruiker die betrekking heeft op de medewerker die u voor de kostenplaats hebt geselecteerd.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Voorbeeld 2: uitgavencontroleurs op basis van projectverdelingen

U werkt voor de servicesafdeling van Contoso Appliances. De organisatie vereist dat de projectmanager voor elke inkooporder de onkostenpost moet goedkeuren. Daarnaast moet de kostenplaatsmanager voor het project deze goedkeuren. De goedkeuringen kunnen tegelijkertijd worden uitgevoerd. In elk geval moeten beide gebruikers de inkooporder goedkeuren voordat de werkstroom verder kan gaan.

Voor dit voorbeeld maakt u één *uitgavencontroleur voor inkooporders* die **PM en kostenplaats** wordt genoemd. U selecteert het selectievakje **Projectmanager** en stelt de optie **Kostenplaatsdimensie** in op **Ja** op het tabblad **Projectverdelingen** van de pagina **Uitgavencontroleur voor inkooporders**. Als onderdeel van de configuratie moet u ervoor zorgen dat het veld **Projectmanager** is ingesteld voor alle projecten en dat een eigenaar is opgegeven voor alle kostenplaatsen op de pagina **Waarden van financiële dimensies**.

Wanneer u de werkstroom configureert, hebt u één goedkeuringselement nodig. U selecteert **Deelnemer** in het veld **Toewijzingstype**. Selecteer vervolgens **Uitgavendeelnemers** in het veld **Type deelnemer** op het tabblad **Rolgebaseerd** en selecteer de projectmanager en kostenplaats in het veld **Deelnemer**. U stelt het veld **Voltooiingsbeleid** in op **Alle fiatteurs** om ervoor te zorgen dat de werkstroom pas verder kan gaan wanneer de projectmanager en de eigenaar van de kostenplaats de werkstroom hebben goedgekeurd.

Wanneer de inkooporder wordt gemaakt, moet het veld **Project** worden opgegeven. Als u geen project hoeft te maken voor al uw inkooporders, moet u een voorwaardelijke beslissing aan uw werkstroom toevoegen om te controleren op een project voordat de goedkeuringsstap wordt uitgevoerd. Het systeem evalueert vervolgens het project dat is opgegeven voor de inkooporder en wijst het goedkeuringselement toe aan de gebruiker die betrekking heeft op de werknemer in het veld **Projectmanager**. Daarnaast wordt een taak gemaakt en toegewezen aan de gebruiker die is gerelateerd aan de werknemer die u selecteert in het veld **Eigenaar** voor de kostenplaats van het project. In dit voorbeeld wordt de kostenplaats van het project gebruikt, niet de kostenplaats van de inkooporder.

## <a name="set-up-expenditure-reviewers"></a>Uitgavencontroleurs instellen

Dit voorbeeld laat zien hoe u een uitgavencontroleur voor opdrachten tot inkoop configureert. Als u andere typen uitgavencontroleurs wilt configureren, vervangt u het navigatiepad in stap 1 door het juiste pad van de tabel in de sectie [Typen uitgavencontroleurs](configure-expenditure-reviewers.md#types-of-expenditure-reviewers), eerder dit onderwerp.

1. Ga naar **Inkoopbeheer \> Instellingen \> Beleid \> Uitgavencontroleurs voor opdrachten tot inkoop**.
2. Selecteer **Nieuw** op de pagina **Uitgavencontroleurs voor opdrachten tot inkoop**.
3. Voer in het veld **Naam** een naam in voor de configuratie van de uitgavencontroleur, bijvoorbeeld **kostenplaats**.
4. Selecteer op het sneltabblad **Uitgavencontroleurs per rechtspersoon** de rechtspersoon die u wilt configureren.
5. Schakel voor een projectverdeling het selectievakje voor elke projectinstantie in en selecteer **Ja** voor elke financiële dimensie die u wilt inschakelen. 
6. Selecteer **Ja** voor elke financiële dimensie die u wilt inschakelen voor een organisatieverdeling op het tabblad **Organisatieverdelingen**.
7. Herhaal stap 4 tot en met 6 voor elke extra rechtspersoon.

## <a name="assign-owners-to-financial-dimensions"></a>Eigenaren toewijzen aan financiële dimensies

Als u een eigenaar wilt toewijzen aan een financiële dimensie, volgt u deze stappen.

1. Ga naar **Grootboek \> Rekeningschema \> Dimenies \> Financiële dimensies**.
2. Selecteer in de lijst de financiële dimensie waaraan u eigenaren wilt toewijzen.
3. Selecteer **Dimensiewaarden**.
4. Selecteer **Bewerken** om wijzigingen in de dimensiewaarden aan te brengen.
5. Selecteer in de lijst de dimensiewaarde waaraan u een eigenaar wilt toewijzen.
6. Selecteer in het veld **Eigenaar** de medewerker aan wie u de dimensiewaarde wilt toewijzen.

## <a name="configure-project-distributions"></a>Projectverdelingen configureren

Voer deze stappen uit om projectinstanties toe te wijzen aan een project.

1. Ga naar **Projectbeheer en boekhouding \> Projecten \> Alle projecten**.
2. Selecteer het project waaraan u instanties wilt toewijzen.
3. Selecteer **Bewerken** om wijzigingen in het project aan te brengen.
4. Selecteer op het sneltabwerk **Algemeen** in de sectie **Verantwoordelijk** een medewerker voor de velden **Verkoopmanager**, **Projectmanager** en **Projectcontroleur** waar nodig.
5. Selecteer de vereiste financiële dimensies voor uw project op het sneltabblad **Financiële dimensies**.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Uitgavencontroleurs toewijzen aan een werkstroomtaak

Dit voorbeeld laat zien hoe u een werkstroom voor een opdracht tot inkoop configureert zodat deze een uitgavencontroleur voor opdrachten tot inkoop gebruikt. Als u andere werkstroomtypen wilt configureren, staat de werkstroompagina die u in stap 1 moet openen mogelijk in de module **Onkostenbeheer** of **Crediteuren** in plaats van in de module **Inkoopbeheer**.

Als u uitgavencontroleurs aan een werkstroomtaak wilt toewijzen, volgt u deze stappen.

1. Ga naar **Inkoopbeheer \> Instellingen \> Workflows voor inkoop en sourcing**.
2. Dubbeltip (of dubbelklik) op een bestaande werkstroom of maak een nieuwe werkstroom.
3. Selecteer in de werkstroomeditor in het deelvenster **Werkstroom** de taak die u aan de configuratie van de uitgavencontroleur wilt toewijzen. Selecteer vervolgens in het **Actievenster**, in de groep **Weergeven** de optie **Eigenschappen**.
4. Selecteer in het linkerdeelvenster van de pagina **Eigenschappen** de optie **Toewijzing**.
5. Selecteer **Deelnemer** op het tabblad **Toewijzingstype**.
6. Selecteer op het tabblad **Rolgebaseerd** in het veld **Type deelnemer** de optie **Uitgavendeelnemers**. Selecteer vervolgens in het veld **Deelnemer** de configuratie voor uitgavencontroleurs die u voor de werkstroomtaak wilt gebruiken.
