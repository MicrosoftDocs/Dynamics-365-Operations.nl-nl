---
title: Uitgestelde verwerking van magazijnwerk
description: In dit onderwerp wordt de functionaliteit beschreven die uitgestelde verwerking van wegzetbewerkingen in magazijnwerk beschikbaar maakt in Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 470b1d947c3ead862dad8f5d40fb14e45ecc71a6
ms.sourcegitcommit: 4398fdf783b8557029284bf95ce95d389fcf4162
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100202"
---
# <a name="deferred-processing-of-warehouse-work"></a>Uitgestelde verwerking van magazijnwerk

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de functionaliteit beschreven die uitgestelde verwerking van wegzetbewerkingen voor magazijnwerk beschikbaar maakt in Dynamics 365 Supply Chain Management.

Met de functionaliteit voor uitgestelde verwerking kunnen magazijnmedewerkers doorgaan met ander werk terwijl de wegzetbewerking op de achtergrond wordt verwerkt. Uitgestelde verwerking is nuttig wanneer veel werkregels moeten worden verwerkt en de werknemer dat werk asynchroon kan laten verwerken. Het is ook handig wanneer de server ad-hoc of niet-geplande verhogingen in verwerkingstijd kan hebben, en de toegenomen verwerkingstijd kan invloed hebben op de productiviteit van de gebruiker.

Verwerking in de achtergrond wordt bereikt met het SysOperation-Framework. Zie [Overzicht SysOperation Framework](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview) voor meer informatie.

## <a name="configuring-the-work-processing-policies"></a>Het beleid voor werkverwerking configureren

Om uitgestelde verwerking te gebruiken, moet u beleid voor werkverwerking configureren.

Beleid wordt geconfigureerd op de pagina **Werkverwerkingsbeleid**. In de volgende tabel worden de velden op deze pagina beschreven.

| Veld                           | Beschrijving |
|---------------------------------|-------------|
| Naam van verwerkingsbeleid voor werk     | De naam van het werkverwerkingsbeleid. |
| Werkordertype                 | Het type werkorder waarop het beleid wordt toegepast. |
| Bewerking                       | De bewerking die wordt verwerkt met behulp van het beleid. |
| Methode voor werkverwerking          | De methode die wordt gebruikt om de werkregel te verwerken. Als de methode is ingesteld op **Direct**, lijkt het erop dat er geen werkverwerkingsbeleid wordt gebruikt om de regel te verwerken. Als de methode is ingesteld op **Uitgesteld**, wordt uitgestelde verwerking gebruikt die gebruikmaakt van het batchframework. |
| Drempel voor uitgestelde verwerking   | De waarde **0** (nul) betekent dat er geen drempel is. In dit geval wordt uitgestelde verwerking gebruikt waar dat kan. Als de specifieke drempelberekening onder de drempelwaarde ligt, wordt de methode Direct gebruikt. Anders wordt de methode Uitgesteld gebruikt waar dat kan. Voor verkoop- en overdrachtsgerelateerd werk wordt de drempel berekend als het aantal gekoppelde bronbelastingsregels dat voor het werk wordt verwerkt. Voor aanvullingswerk wordt de drempel berekend als het aantal werkregels dat door het werk wordt aangevuld. Door een drempelwaarde van bijvoorbeeld **5** in te stellen voor verkoop, gebruiken kleinere werken met minder dan vijf oorspronkelijke bronbelastingsregels geen uitgestelde verwerking, maar grotere werken gebruiken deze wel. De drempelwaarde heeft alleen effect als de werkverwerkingsmethode is ingesteld op **Uitgesteld**. |
| Batchgroep voor uitgestelde verwerking |De batchgroep die wordt gebruikt voor verwerking. |

Voor uitgestelde opslagbewerkingen worden de volgende typen werkorders ondersteund: verkooporder, uitgifte van overboekingsorder en aanvulling.

## <a name="assigning-the-work-creation-policy"></a>Het beleid voor het maken van werk toewijzen

Het beleid voor het maken van werk kan worden toegewezen in de parameters voor magazijnbeheer. Het kan ook worden toegewezen op het niveau van afzonderlijke magazijnen. Als het beleid is toegewezen aan een magazijn, wordt het alleen toegepast op werk dat voor dat magazijn is gemaakt. Als er geen beleid is toegewezen op magazijnniveau, wordt het beleid van de parameters voor magazijnbeheer toegepast.

## <a name="viewing-the-deferred-put-processing-tasks"></a>De uitgestelde wegzetverwerkingstaken weergeven

U kunt uitgestelde wegzetverwerkingstaken weergeven op de pagina **Uitgestelde wegzetverwerkingstaken**.

Standaard worden de **Voltooide** taken weergegeven.

| Veld            | Beschrijving |
|------------------|-------------|
| Status           | De status van de taak. |
| Status batchtaak | De status van de verwante batchtaak. Als de batchtaak is verwerkt, bevat de batchhistorie het logboek en de gegevens uit de batchtaak. |

Hier volgt een uitleg van de mogelijke statussen:

- **In afwachting** - De gerelateerde batchtaak wacht op verwerking op de batchserver.
- **Mislukt** – De verwerking is mislukt. De taak kan opnieuw worden verwerkt met de actie **Uitgesteld wegzetten verwerken** of kan worden geannuleerd met de actie **Uitgesteld wegzetten annuleren**.
- **Voltooid** – De taak is voltooid.

## <a name="impact-on-closed-work-dates"></a>Impact op datums waarop het werk is gesloten

Wanneer uitgestelde wegzetverwerking wordt gebruikt, wordt de sluitdatum voor het werk ingesteld als de datum/tijd van het maken van de uitgestelde wegzetverwerkingstaken. De datum voor sluiting van het werk wordt gebruikt omdat dit de beste schatting is voor wanneer de wegzetbewerking is voltooid.

## <a name="reprocessing-a-failed-task"></a>Een mislukte taak opnieuw verwerken

U kunt een mislukte taak opnieuw verwerken door deze op de pagina te selecteren en vervolgens **Uitgesteld wegzetten verwerken** te selecteren. Opnieuw verwerken komt overeen met een situatie waarin de gebruiker het wegzetten vanaf het mobiele apparaat voltooit alsof het is ingesteld voor onmiddellijke verwerking.

## <a name="canceling-failed-tasks"></a>Mislukte taken annuleren

Alleen mislukte taken kunnen worden geannuleerd. Wanneer u een taak annuleert, kunt u deze toewijzen aan een nieuwe gebruiker. De taak kan ook toegewezen blijven aan de gebruiker die het werk heeft verwerkt. Annulering komt overeen met een situatie waarin het werk wordt teruggebracht naar het mobiele apparaat alsof de laatste verzamelstap zojuist is voltooid en het werk moet worden weggezet. De gebruiker kan echter bepalen dat het werk 'anders' is, omdat het maar één wegzetstap heeft en de locatie overeenkomt met de locatie die de eerste gebruiker die het werk heeft verwerkt, als een definitieve wegzetlocatie had.

Wanneer een taak wordt geannuleerd, wordt het werk niet langer geblokkeerd door de reden voor het blokkeren van uitgestelde verwerking. Het kan opnieuw worden verwerkt via het mobiele apparaat.

De taakrecord wordt verwijderd wanneer de taak is geannuleerd.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Het menu voor het mobiele apparaat configureren zodat het beleid voor uitgestelde verwerking wordt overgeslagen

U kunt de menuopdracht voor het mobiele apparaat zo configureren dat het beleid voor uitgestelde verwerking niet wordt gebruikt. Het werk wordt dan verwerkt zoals wanneer er geen beleid voor uitgestelde verwerking wordt gebruikt. Met deze functionaliteit kan een supervisor een specifieke menuopdracht gebruiken waarbij uitgesteld wegzetten niet wordt gebruikt. Als u dit wilt configureren, stelt u het veld **Beleid voor uitgestelde wegzetverwerking** in op **Instellingen negeren en wegzetten synchroon verwerken**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Beperkingen wanneer uitgestelde wegzetverwerking niet wordt toegepast

Er zijn verschillende scenario's waarbij uitgestelde wegzetverwerking niet wordt toegepast, ook al is het beleid geconfigureerd. Hieronder vindt u enkele voorbeelden:

- Het werk wordt dan handmatig voltooid.
- Het werk wordt voltooid met behulp van automatisch aanvullen.
- Controlesjablonen worden gebruikt.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>De uitgestelde verwerkingstaken bewaken vanuit de werkruimte voor bewaking van uitgaand werk

De werkruimte **Uitgaand werk bewaken** bevat twee tegels waarmee u uitgestelde wegzetverwerkingstaken kunt bewaken:

- **Mislukte uitgestelde wegzetverwerkingstaken** – Op deze tegel ziet u het aantal mislukte taken. Als er mislukte taken zijn, moet de magazijnbeheerder deze opnieuw verwerken of annuleren, omdat deze niet automatisch opnieuw worden verwerkt.
- **Wacht op uitgestelde wegzetverwerkingstaken** – Op deze tegel ziet u het aantal taken dat al meer dan 10 minuten de status **In afwachting** heeft. Als de tegel een getal weergeeft, kan dit erop duiden dat er een probleem is opgetreden tijdens de batchverwerking. U kunt de taken met de status **In afwachting** handmatig verwerken. Als de batchtaak voor een taak later wordt verwerkt, zal dit mislukken, omdat de taak al is verwerkt. Er zal geen impact zijn.

## <a name="deleting-completed-tasks"></a>Voltooide taken verwijderen

U kunt uitgestelde wegzetverwerkingstaken die zijn voltooid verwijderen door ze op de pagina te selecteren en te verwijderen.
