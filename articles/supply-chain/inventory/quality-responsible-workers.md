---
title: Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen
description: In dit onderwerp wordt beschreven hoe u werknemers configureert die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b764baf0983dbca75d52ea9cdd063cebda80a08d39cf3a5c929f15858e2597c1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768162"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Medewerkers die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u werknemers configureert die verantwoordelijk zijn voor het goedkeuren van niet-conformeringen.

Niet-conformeringen moeten worden goedgekeurd voordat gebruikers kunnen beginnen met het invoeren van details, zoals correcties of bewerkingen. Voordat gebruikers niet-conformeringen kunnen goedkeuren of afwijzen, moet hun gebruikers-id (gebruikersrecord) worden gekoppeld aan een werknemersrecord. U kunt desgewenst werknemers configureren die verantwoordelijk zijn voor de kwaliteit en vervolgens de ene werknemer toestaan om werk goed te keuren namens een andere werknemer.

## <a name="enable-a-user-for-nonconformance-processing"></a>Een gebruiker in staat stellen niet-conformeringen te verwerken

Voordat een gebruiker niet-conformeringen kan goedkeuren of afwijzen, moet u de gebruikers-id van die werknemer koppelen aan een werknemersrecord. De goedkeuringsvelden kunnen vervolgens automatisch worden ingesteld en de huidige gebruiker kan automatisch worden ingevuld voor de urenstaat. Voordat de gebruiker de documentnotities kan gebruiken, moet u de documentverwerking activeren in de gebruikersopties voor die gebruiker.

1. Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.
1. Zoek en open de gebruiker die niet-conformeringen moet kunnen goedkeuren of afwijzen.
1. Stel het veld **Persoon** in op de naam van de werknemer die is gekoppeld aan de huidige gebruikersrecord.
1. Selecteer **Gebruikersopties** in het actievenster.
1. Ga naar de pagina **Opties** voor de huidige gebruikersrecord en stel op het tabblad **Voorkeuren** de optie **Documentverwerking inschakelen** in op *Ja*.
1. Sluit de pagina's.

## <a name="define-workers-that-are-responsible-for-quality"></a>Werknemers definiëren die verantwoordelijk zijn voor de kwaliteit

1. Ga naar **Voorraadbeheer \> Instellen \> Kwaliteitscontrole \> Werknemers die verantwoordelijk zijn voor de kwaliteit**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het veld **Werknemer** de werknemer die kwaliteitsgegevens invoert.
4. Selecteer in het veld **Verantwoordelijke werknemer** de werknemer namens wie de geselecteerde werknemer werk invoert. Wanneer er niet-conformeringen worden gemaakt en bijgewerkt, wordt deze werknemer standaard ingevoerd in de **Werknemer**-velden.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van kwaliteitsbeheer](quality-management-processes.md)
- [Beheer van kwaliteit en niet-conformeringen inschakelen](enable-quality-management.md)
- [Kwaliteitstoeslagen](quality-charges.md)
- [Quarantainezones voor niet-conformeringen](quality-quarantine-zones.md)
- [Typen diagnosen voor niet-conformeringen](quality-diagnostic-types.md)
- [Kwaliteitstoeslagen voor niet-conformeringen](quality-charges.md)
- [Bewerkingen voor niet-conformeringen](quality-operations.md)
- [Kwaliteitsbeheer voor magazijnprocessen](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
