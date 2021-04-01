---
title: Tabelbeperkingen door de gebruiker of door het systeem gedefinieerd
description: 'Dit artikel beschrijft de twee typen tabelbeperkingen voor onderdelen in een productconfiguratiemodel: gedefinieerd door de gebruiker en gedefinieerd door het systeem. Tabelbeperkingen vertegenwoordigen matrixen van de toegestane kenmerkcombinaties, waarbij elke rij één set van mogelijke kenmerkwaarden definieert.'
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e922e7961cad5880e45cb2e86e3c084a52cd6b7c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237443"
---
# <a name="system-defined-and-user-defined-table-constraints"></a>Tabelbeperkingen door de gebruiker of door het systeem gedefinieerd

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft de twee typen tabelbeperkingen voor onderdelen in een productconfiguratiemodel: gedefinieerd door de gebruiker en gedefinieerd door het systeem. Tabelbeperkingen vertegenwoordigen matrixen van de toegestane kenmerkcombinaties, waarbij elke rij één set van mogelijke kenmerkwaarden definieert.

Tabelbeperkingen vertegenwoordigen matrixen van de combinaties van kenmerken die zijn toegestaan voor componenten in een productconfiguratiemodel. Elke rij in de tabel definieert één set met mogelijke kenmerkwaarden. Er zijn twee soorten beperkingen die u in een productconfiguratiemodel kunt declareren:

-   **Expressiebeperking** – Maak een expressie die relaties definieert tussen kenmerken zodat alleen compatibele waarden kunnen worden geselecteerd wanneer u een product configureert.
-   **Tabelbeperking** – Maak een tabel die alle combinaties bepaalt die zijn toegestaan voor een opgegeven set kenmerken. Er zijn twee typen tabelbeperkingen beschikbaar: door de gebruiker gedefinieerde tabelbeperkingen en door het systeem gedefinieerde tabelbeperkingen.

Dit artikel beschrijft tabelbeperkingen die door de gebruiker zijn gedefinieerd en door het systeem zijn gedefinieerd voor onderdelen in een productconfiguratiemodel.

## <a name="user-defined-table-constraints"></a>Door gebruiker gedefinieerde tabelbeperkingen
Een gebruikergedefinieerde tabelbeperking is een type matrix die wordt gebruikt voor het beschrijven van combinaties van kenmerkwaarden die zijn gedefinieerd door kenmerktypen. Als u bijvoorbeeld speakers produceert, kunt u kolommen opnemen voor de afwerking van de behuizing en de voorgrill in de tabelbeperking die door de gebruiker is gedefinieerd. Het type kenmerk voor de afwerking heeft vier waarden, en het type kenmerk voor de voorgrill heeft drie waarden. Daarom zijn er, als de beperkingen niet worden gebruikt, 4 x 3 = 12 mogelijke combinaties. In dit voorbeeld zijn echter slechts zes combinaties toegestaan, zoals in de volgende tabel wordt aangegeven. Deze gegevens worden weergegeven op het tabblad **Toegestane combinaties** op de pagina **Tabelbeperking bewerken**.

| Afwerking behuizing | Voorgrill |
|----------------|-------------|
| Zwart          | Zwart       |
| Zwart          | Metaal       |
| Eiken            | Zwart       |
| Rozenhout       | Wit       |
| Wit          | Zwart       |
| Wit          | Wit       |

Tabelbeperkingen door de gebruiker gedefinieerd, worden gedefinieerd door de statische tabelinvoer die op dezelfde manier werkt als een expressiebeperking. Wanneer u een tabelbeperking door de gebruiker gedefinieerd gebruikt, hebt u het voordeel dat tabellen vaak gemakkelijker te maken, te begrijpen en te onderhouden zijn dan lange expressiebeperkingen.

## <a name="system-defined-table-constraints"></a>Beperkingen door systeem gedefinieerd
Een systeemgedefinieerde tabelbeperking maakt een dynamische toewijzing tussen een kenmerktype en een veld in een tabel. Als een door het systeem gedefinieerde tabelbeperking in een model voor productconfiguratie is opgenomen, garandeert de toewijzing dat de gegevens in de tabel in plaats van de waarden van het type kenmerk worden weergegeven. Het resultaat is een dynamische beperking, omdat de tabelinhoud kan worden gewijzigd, bijvoorbeeld door andere modules.  

Wanneer u een systeemgedefinieerde tabelbeperking maakt, selecteert u een tabel, definieert u desgewenst de query die u wilt gebruiken en koppelt u kenmerktypen aan de velden in de geselecteerde tabel. De typen velden moeten overeenkomen met de kenmerktypen.  

Voordat een tabelbeperking op een productconfiguratiemodel van kracht kan worden, moet de tabelbeperking in een beperking op een van de modelcomponenten worden opgenomen. De procedure is om een nieuwe beperking te maken, het type tabelbeperking te selecteren, en vervolgens de definitie van de tabelbeperking te selecteren die u wilt gebruiken. Tot slot moeten alle velden in de tabelbeperking aan de kenmerken in het productconfiguratiemodel worden toegewezen.

<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht productconfiguratiemodellen](product-configuration-models.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]