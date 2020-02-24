---
title: Voorraadblokkering
description: Dit onderwerp geeft een overzicht van voorraadblokkering, dat deel van het kwaliteitsinspectieproces in Supply Chain Management is. U kunt voorraadblokkering gebruiken om te voorkomen dat artikelen worden verwerkt of verbruikt.
author: perlynne
manager: AnnBe
ms.date: 01/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1a870936619d07db01d5a8fe83b3fab73693187
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971482"
---
# <a name="inventory-blocking"></a>Voorraadblokkering

[!include [banner](../includes/banner.md)]

Dit onderwerp geeft een overzicht van voorraadblokkering, dat deel van het kwaliteitsinspectieproces in Supply Chain Management is. U kunt voorraadblokkering gebruiken om te voorkomen dat artikelen worden verwerkt of verbruikt.

U kunt op de volgende manieren voorraadartikelen blokkeren:
-   Handmatig
-   Door een kwaliteitsorder te maken
-   Door een proces te gebruiken waarmee een kwaliteitsorder wordt gegenereerd
-   Door blokkering van voorraadstatus te gebruiken

## <a name="blocking-items-manually"></a>Door artikelen handmatig te blokkeren
U kunt een hoeveelheid van een artikel blokkeren door een transactie te maken op de pagina **Voorraadblokkering**. Alleen artikelen die beschikbaar zijn als voorhanden voorraad kunnen handmatig worden geblokkeerd. Voor handmatig geblokkeerde hoeveelheden moet u bepalen of verwachte ontvangsten moeten worden opgenomen in planningsactiviteiten als verwachte voorhanden hoeveelheid. Verwachte ontvangsten zijn geblokkeerde artikelen waarvan u verwacht dat ze na inspectie als voorhanden voorraad beschikbaar zijn. U kunt de verwachte datum onderhouden. Standaard is de optie **Verwachte ontvangsten** ingeschakeld voor artikelen die zijn geblokkeerd door een kwaliteitsorder. U kunt een handmatige blokkering van een hoeveelheid annuleren door de transactie te verwijderen op de pagina **Voorraadblokkering**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Artikelen blokkeren door een kwaliteitsorder te maken
U kunt artikelen opgeven die moeten worden geïnspecteerd door een kwaliteitsorder te maken op de pagina **Kwaliteitsorders**. Wanneer u een kwaliteitsorder maakt, wordt de hoeveelheid die u opgeeft voor een artikel geblokkeerd. Het bemonsteringsplan dat is gekoppeld aan een kwaliteitsorder bepaalt alleen de hoeveelheid artikelen die moet worden geïnspecteerd, niet de hoeveelheid die wordt geblokkeerd. De hoeveelheid die wordt ingevoerd in de kwaliteitsorder is de geblokkeerde hoeveelheid, ongeacht de hoeveelheid die volgens het bemonsteringsplan moet worden verzonden voor inspectie.

> [!NOTE]
> Het gebruik van de batchvervaldatum en blokkering van voorraadstatusfuncties worden niet ondersteund door de hoofdplanning. Dit kan leiden tot dubbele uitsluiting van voorhanden voorraad, wat kan optreden tijdens hoofdplanning. Het is raadzaam om in plaats van de voorraad status te vertrouwen op batchbeschikkingscodes voor het blokkeren van vervallen batches.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Artikelen blokkeren via een proces waarmee een kwaliteitsorder wordt gegenereerd
Als in een kwaliteitsinspectieproces wordt opgegeven dat een artikel moet worden geïnspecteerd, wordt een hoeveelheid van het artikel automatisch geblokkeerd. Dus wanneer een kwaliteitsorder automatisch wordt gegenereerd, bepaalt het artikelbemonsteringsplan dat is gekoppeld aan de kwaliteitsorder, zowel de hoeveelheid artikelen die wordt geblokkeerd als de hoeveelheid artikelen die moet worden geïnspecteerd. Als het selectievakje **Volledig blokkeren** op de pagina **Artikelbemonstering** is ingeschakeld, wordt de volledige hoeveelheid van, bijvoorbeeld een inkooporder, geblokkeerd tijdens de inspectie, ongeacht de hoeveelheid voor artikelbemonstering.
### <a name="example"></a>Voorbeeld

In het volgende voorbeeld wordt een kwaliteitsorder gegenereerd wanneer de pakbon van een inkooporder wordt geboekt. Op de pagina **Kwaliteitskoppelingen** hebt u opgegeven dat het boeken van een pakbon voor een inkooporder het proces is waarmee een kwaliteitsorder wordt geactiveerd.

|Instellingen                                                                     |Gebruikersactie                 |Resultaat             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Met een kwaliteitskoppeling wordt opgegeven dat bij het boeken van een pakbon voor een inkooporder een kwaliteitsorder moet worden gegenereerd. Met het artikelbemonsteringsplan van de kwaliteitsorder wordt bepaald dat 10 procent van de hoeveelheid op de inkooporderregel moet worden geïnspecteerd. Verder moet, omdat het selectievakje **Volledige blokkering** is ingeschakeld in de instellingen voor de artikelbemonstering, de volledige hoeveelheid van de inkooporderregel worden geblokkeerd tijdens de inspectie, ongeacht de hoeveelheid die wordt verzonden voor inspectie. | De pakbon wordt geboekt. | Een kwaliteitsorder wordt gegenereerd. Tien procent van de inkooporderhoeveelheid voor het artikel wordt naar inspectie verzonden. De volledige hoeveelheid van de inkooporderregel wordt geblokkeerd. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Artikelen blokkeren via blokkering van voorraadstatus
U kunt opgeven welke voorraadstatussen blokkeringsstatussen zijn door de parameter **Voorraadblokkering** op de pagina **Voorraadstatussen** te gebruiken . U kunt geen voorraadstatussen als blokkeringsstatus gebruiken voor productieorders, verkooporders, transferorders, uitgaande transacties of projectintegraties. Gebruik voor uitgaand werk artikelen met een beschikbare voorraadstatus. Als artikelen de status **Verbroken** hebben en de hoofdplanning op deze artikelen wordt uitgevoerd, worden de artikelen als ontbrekend beschouwd en wordt de voorraad automatisch aangevuld.



<a name="additional-resources"></a>Aanvullende resources
--------

[Voorraadblokkering maken en beheren](tasks/create-maintain-inventory-blocking.md)

[Processen voor kwaliteitsbeheer](quality-management-processes.md)

[Inspecteer de kwaliteit van goederen](tasks/inspect-quality-goods.md)
