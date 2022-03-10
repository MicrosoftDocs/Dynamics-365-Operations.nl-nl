---
title: Magazijnparameters voor waveverwerking
description: In dit onderwerp wordt beschreven hoe u magazijnparameters instelt voor waveverwerking. U kunt waveverwerking gebruiken om verzamelwerk voor meerdere werkorders in een enkele wave te groeperen.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cd7961ae8f4237bcee7ae4c53365d24ab03c5aa9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572213"
---
# <a name="warehouse-parameters-for-wave-processing"></a>Magazijnparameters voor waveverwerking

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u magazijnparameters instelt voor waveverwerking. U kunt waveverwerking gebruiken om verzamelwerk voor meerdere werkorders in een enkele wave te groeperen.

Als u waveverwerking wilt gebruiken, geeft u het volgende op de pagina **Magazijnbeheerparameters** op:

- Of u waves kunt verwerken met een batchtaak.
- Of u gegevens verzamelt in een logbestand wanneer waves worden verwerkt.

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a>Magazijnbeheerparameters instellen voor waveverwerking

Als u magazijnparameters wilt instellen voor waveverwerking, volgt u deze stappen:

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Parameters voor magazijnbeheer**.

1. Voer op het sneltabblad **Waveverwerking** de volgende instellingen uit:

    - **Batchgroep voor waveverwerking**: selecteer de batchgroep die u wilt gebruiken wanneer u golven verwerkt met batchtaken. De batchgroep bepaalt de server waarop batchtaken worden uitgevoerd.
    - **Waves verwerken in batch**: kies of waves automatisch door een batchtaak kunnen worden verwerkt. U moet dit instellen op *Ja* als u parallelle verwerking wilt gebruiken. U stelt de batchtaak in op de pagina **Waves verwerken**. (Zie ook de opmerking aan het einde van deze lijst.)
    - **Voortgangslogboek voor waves maken**: kies of het systeem een logboekrecord moet genereren telkens wanneer de toewijzing voor een artikel en de bijbehorende dimensies begint en eindigt. U moet dit logboek alleen inschakelen wanneer u het nodig hebt, bijvoorbeeld tijdens de eerste tests of voor het oplossen van problemen. Zie [Wavetoewijzing](wave-allocation-method.md) voor meer informatie.
    - **Logboek met historie van waveverwerking maken**: kies of u automatisch informatie over een wave in een logboekbestand wilt opslaan nadat de wave is verwerkt, inclusief tijdens de parallelle verwerking van in behandeling zijnde toewijzingen. Meestal moet u dit alleen inschakelen tijdens het oplossen van problemen, omdat dit extra overhead toevoegt. Als u het logboek wilt bekijken, gaat u **Magazijnbeheer \> Uitgaande waves \> Logboek met historie van waveverwerking**. Zie [Waves maken en verwerken](wave-processing.md) voor meer informatie.
    - **Geschiedenislogboek voor containervorming maken**: kies of u automatisch informatie over containervorming wilt opslaan voor een wave in een logboekbestand nadat de wave is verwerkt. Als u het logboek wilt bekijken, gaat u naar **Magazijnbeheer \> Verpakking en containervorming \> Containervormingshistorie**.
    - **Wachten op vergrendeling (ms)**: voer de tijd, uitgedrukt in milliseconden, in die een toewijzingsstap moet wachten op een systeemresource die door een andere toewijzingsstap wordt vergrendeld. Nadat deze tijd is verstreken, wordt de golf niet verwerkt en wordt er een foutbericht weergegeven.

1. Voer op het sneltabblad **Vrijgeven aan magazijn** de volgende instelling uit:

    - **Fout bij batchstoring**: kies of u een fout wilt genereren wanneer een batchtaak voor vrijgave aan het magazijn mislukt. Als dit is ingeschakeld, worden mislukte taken beëindigd met de status *Fout*. Als dit is uitgeschakeld, worden mislukte taken beëindigd met de status *Beëindigd*.

> [!NOTE]
> Op de golfsjabloon die wordt gebruikt om de golf te verwerken, kunt u de instellingen opgeven die golfverwerking automatiseren. Als u een planning instelt voor de batchtaak, moet u de timing coördineren met de instellingen voor automatisering in de golfsjabloon. Zie [Een wavesjabloon maken](wave-templates.md) voor meer informatie.
>
> Als u *Transportbeheer* en *Geavanceerd magazijnbeheer* gebruikt, kunt u opgeven of u ladingen wilt consolideren wanneer u een wave verwerkt. Dit is bijvoorbeeld handig wanneer verschillende kleine ladingen tegelijk kunnen worden verzonden. Als u ladingen wilt consolideren wanneer u een wave verwerkt, schakelt u op het tabblad **Ladingen** het selectievakje **Ladingen consolideren tijdens waveverwerking** in.</P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a>Gedeeltelijke of volledige reservering instellen voor productiewaves

Bij verkooporders en kanbanorders moet de voorraad zijn gereserveerd voordat de order aan het magazijn wordt vrijgegeven. Anders kunnen artikelen of toewijzingsregels niet in een golf worden verwerkt. Productieorders zijn echter iets flexibeler. Voor productieorders kunt u het volgende opgeven:

- U kunt toestaan dat productieorders worden vrijgegeven, ook al kunnen niet alle materialen worden gereserveerd. Als u deze optie selecteert, moet u de vrijgave naar het magazijnproces handmatig herhalen wanneer de aanvullende materialen beschikbaar worden. Dit is bijvoorbeeld handig als u de materialen hebt die u nodig hebt om een productie te starten en kunt wachten tot extra materialen beschikbaar zijn.
- Vereisen dat alle materialen moeten zijn gereserveerd voordat een order kan worden vrijgegeven aan het magazijn.

Als u een volledige reservering wilt vereisen of gedeeltelijke reservering wilt toestaan, volgt u deze stappen:

1. Ga naar **Productiebeheer** \> **Instellen** \> **Parameters van productiebeheer**.
1. Selecteer op het tabblad **Algemeen** in het veld **Vrijgeven aan magazijn** de standaardinstelling.
