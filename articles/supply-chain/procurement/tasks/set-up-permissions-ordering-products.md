---
title: Machtigingen instellen voor het bestellen van producten namens iemand anders
description: Dit artikel laat zien hoe u medewerkers machtigingen kunt verlenen om opdrachten tot inkoop voor te bereiden namens andere medewerkers.
author: GalynaFedorova
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3053f28fdf97637b1da5f644f64676bfd10fb6a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854205"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a>Machtigingen instellen voor het bestellen van producten namens iemand anders

[!include [banner](../../includes/banner.md)]

Dit artikel laat zien hoe u medewerkers machtigingen kunt verlenen om opdrachten tot inkoop voor te bereiden namens andere medewerkers. Met andere woorden, een opdracht tot inkoop voor voorbereider kan een opdracht tot inkoop maken voor een andere aanvrager. De procedure laat ook zien hoe u een werknemer kunt machtigen om artikelen en diensten in verschillende rechtspersonen of operationele eenheden te bestellen. Deze taken worden gewoonlijk uitgevoerd door een inkoopmanager. U kunt deze procedure gebruiken voor gegevens voor het USMF-demobedrijf of voor uw eigen gegevens.


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a>Machtiging verlenen om opdrachten tot inkoop in te voeren namens een andere medewerker
1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Instellingen > Beleid > Machtigingen voor inkoopbestelopdrachten**. Controleer of het veld **Huidige weergave** is ingesteld op **Op voorbereider**. De lijst in het linkerdeelvenster laat de personen zien die kunnen worden gemachtigd om opdrachten namens andere mensen voor te bereiden.  
2. Selecteer de persoon die u wilt machtigen (de voorbereider).
3. Selecteer **Toevoegen**.
4. Zoek en selecteer de persoon die u als aanvrager wilt toevoegen.
    - De aanvrager is de persoon namens wie de voorbereider bestelopdrachten kan maken.  
    - Selecteer in het veld **Autorisatie** de optie **Specifiek** als de voorbereider opdrachten tot inkoop moet kunnen maken namens de geselecteerde medewerker. Selecteer **Rapportage** als de voorbereider ook opdrachten tot inkoop moet kunnen maken namens alle medewerkers die aan die medewerker rapporteren.  
5. Voer een datum in het veld **Ingangsdatum** in.
6. Voer in het veld **Vervaldatum** een datum in.

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a>Voorbereiders weergeven die zijn gemachtigd om opdrachten tot inkoop te maken voor een geselecteerde medewerker
1. Selecteer **Op aanvrager** in het veld **Huidige weergave**. Deze weergave laat een lijst zien met voorbereiders aan wie machtiging vis verleend voor het maken van opdrachten tot inkoop namens een geselecteerde medewerker.  
2. Gebruik het snelfilter om de medewerker te zoeken die zojuist als aanvrager hebt toegevoegd.
3. Selecteer de aanvrager. De lijst Voorbereider bevat de personen die zijn gemachtigd om artikelen te bestellen namens de aanvrager die is geselecteerd in het linkerdeelvenster.  U kunt hier extra voorbereiders toevoegen. In deze weergave kunt u ook de aanvrager verlenen machtiging om opdrachten te maken in rechtspersonen en operationele eenheden die niet de primaire rechtspersoon of operationele eenheid van die persoon zijn.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]