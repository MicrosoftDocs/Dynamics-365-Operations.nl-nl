---
title: Serviceorders
description: Een serviceorder vertegenwoordigt het bezoek van een onderhoudsmonteur aan een klant op een bepaalde datum.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b049b166edf2b5a318a4b1af85e7f74cfe433f2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425128"
---
# <a name="service-orders"></a>Serviceorders   

[!include [banner](../includes/banner.md)]


Een serviceorder vertegenwoordigt het bezoek van een onderhoudsmonteur aan een klant op een bepaalde datum. Elke serviceorder bestaat uit een of meer serviceorderregels. Serviceorderregels vertegenwoordigen de uren werk die moeten worden uitgevoerd door de onderhoudsmonteur en de verwante artikelen, uitgaven en honoraria.

U kunt taken en objecten toevoegen aan een serviceorderregel. U kunt vervolgens serviceorderregels groeperen volgens taak of object. Ook kunt u artikelen uit de voorraad aan serviceorderregels koppelen.

## <a name="create-service-orders"></a>Serviceorders maken

U kunt serviceorders maken aan de hand van serviceovereenkomsten en de regels voor die overeenkomst. U kunt echter alleen serviceorders maken die zijn gekoppeld aan een serviceovereenkomst tijdens de periode die is opgegeven in de overeenkomst. Als een serviceovereenkomst bijvoorbeeld geldig is voor het jaar 2011, kunt u serviceorders voor de overeenkomst maken van 1 januari 2011 en 31 December 2011.

U kunt ook serviceorders afzonderlijk maken, zonder deze te koppelen aan een overeenkomst. Deze serviceorders kunnen worden gebruikt om ongeplande of eenmalige onderhoudsbeurten te verwerken. In maart wil een klant bijvoorbeeld behalve de machines die in de serviceovereenkomst staan opgegeven, nog twee andere machines laten onderhouden. Voor deze taak maakt u serviceorders, maar u koppelt deze niet aan een overeenkomst.


> [!NOTE]
> <P>Om serviceorders te maken die niet zijn gekoppeld aan een serviceovereenkomst, moet u het selectievakje <STRONG>Toestaan zonder serviceovereenkomst</STRONG> in het formulier <STRONG>Parameters voor servicebeheer</STRONG> aanvinken.</P>

**Scenario's**

In het volgende scenario wordt een andere situatie beschreven waarin het handig een serviceorder te maken die niet is gekoppeld aan een serviceovereenkomst.

De verzender van het bedrijf ontvangt een oproep om noodonderhoud uit te voeren aan een lift. Er is geen tijd om een serviceovereenkomst en een project voor de service in te stellen. Daarom maakt de verzender een serviceorder rechtstreeks in het formulier **Serviceorders**, koppelt hij/zij de serviceorder aan een bestaand project en maakt hij/zij de serviceorderregels. De verzender maakt ook een taak- of objectrelatie voor een bestaande serviceorder maken om het werk te registreren dat losstaat van de serviceovereenkomst. Zie voor meer informatie [Handmatig serviceorders maken](create-service-orders-manually.md) en [Servicetaakrelaties maken](create-service-task-relations.md).

## <a name="monitor-the-progress-of-service-orders"></a>De voortgang van serviceorders controleren

U kunt een fasesysteem en redencodes voor serviceorders instellen die een afspiegeling vormen van de voortgang van een serviceorder bij de diverse teams en werkzaamheden in het bedrijf. Voor elk stadium kunt u de acties opgeven die zijn toegestaan. Zie voor meer informatie over redencodes [Redencodes maken](create-reason-codes.md).

**Voorbeeld**

De verzender keurt een serviceorder goed. De verzender werkt de fase van de serviceorder bij en geeft een redencode op die aangeeft dat de serviceorder is vrijgegeven aan de onderhoudsmonteur. De onderhoudsmonteur gaat naar de klant en voert daar de werkzaamheden uit.

## <a name="specify-item-requirements-for-service-orders"></a>Artikelbehoeften voor serviceorders opgeven

U kunt de voorraadartikelen opgeven die vereist zijn voor serviceorders. De serviceorder moet echter gekoppeld zijn aan een project. Artikelbehoeften voor serviceorders worden verwerkt via een project. 

**Voorbeeld**

De serviceorders die van de serviceovereenkomst zijn gemaakt, worden vervolgens verwerkt door de verzender. Bij de eerste serviceorder realiseert de verzender zich dat de onderhoudsmonteur een belangrijk reserveonderdeel nodig heeft dat niet op voorraad is. De verzender maakt rechtstreeks vanuit de serviceorder een artikelbehoefte voor het reserveonderdeel.

## <a name="move-and-post-lines"></a>Regels verplaatsen en boeken

Een onderhoudsmonteur keert terug van een onderhoudsbeurt en wijzigt vervolgens de servicorderregels. Tijdens het servicebezoek voerde de onderhoudsmonteur een onderhoudstaak uit die voor de volgende onderhoudsbeurt was gepland. Daarom verplaatst de onderhoudsmonteur de regels van de volgende onderhoudsbeurt naar de huidige onderhoudsbeurt. De onderhoudsmonteur boekt vervolgens de serviceorder. Zie voor meer informatie [Serviceorderregels verplaatsen](move-service-order-lines.md).

## <a name="cancel-service-orders"></a>Serviceorders annuleren

Een van de andere serviceorders die voor januari was gegenereerd, is vervallen omdat de taak is geannuleerd. De verzender annuleert daarom deze serviceorder. Zie voor meer informatie [Serviceorders annuleren](cancel-service-orders.md).

## <a name="post-from-projects"></a>Boeken vanuit projecten

Aan het einde van elke week wil de verzender alle serviceorders van een bepaald project boeken. Daarom zoekt de verzender het betreffende project in het formulier **Projecten** en boekt deze de serviceorders die zijn voltooid. Zie voor meer informatie [Serviceorders boeken (klasseformulier)](https://technet.microsoft.com/library/aa574685\(v=ax.60\)).

## <a name="delete-service-orders"></a>Serviceorders verwijderen

Tijdens de tweede helft van het jaar geeft de klant aan dat hij vaker een onderhoudsmonteur over de vloer wil hebben. U moet een nieuwe, frequentere reeks onderhoudsbezoeken voor de resterende looptijd van de serviceovereenkomst maken. U dient dus de reeds gemaakte serviceorders te verwijderen en nieuwe serviceorders te maken. Zie voor meer informatie [Serviceorders verwijderen](delete-service-orders.md).

## <a name="see-also"></a>Zie ook

[Serviceorders (formulier)](https://technet.microsoft.com/library/aa554361\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]