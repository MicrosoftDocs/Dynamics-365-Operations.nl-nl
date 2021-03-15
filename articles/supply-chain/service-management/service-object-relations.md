---
title: Serviceobjectrelaties
description: U kunt serviceobjectrelaties maken tussen een serviceobject en een serviceovereenkomst of serviceorder.
author: ShylaThompson
manager: tfehr
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 913b3c30bf972de7cc3dde73280e4f2f2be38507
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974330"
---
# <a name="service-object-relations"></a>Serviceobjectrelaties 

[!include [banner](../includes/banner.md)]

U kunt serviceobjectrelaties maken tussen een serviceobject en een serviceovereenkomst of serviceorder. Wanneer u een relatie maakt, koppelt u het serviceobject aan de serviceovereenkomst of serviceorder.

Nadat de relatie is gemaakt, kunt u het serviceobject koppelen aan de regels in de serviceovereenkomst of serviceorder.

## <a name="template-boms"></a>Sjabloonstuklijsten

U kunt ook een sjabloonstuklijst voor de objectrelatie opgeven. De sjabloonstuklijst is een stuklijst voor het object waarop u service uitvoert. Als u een onderdeel van het serviceobject vervangt tijdens een servicebezoek, kunt u deze wijziging registreren in de servicestuklijst via het formulier Serviceobjecten.

## <a name="example"></a>Voorbeeld

U maakt een serviceovereenkomst voor het onderhoud van twee liften op een klantlocatie.
Het id van de serviceovereenkomst is ID SAL-001.

In het formulier Serviceobjecten zijn de liften ingesteld als de objecten EL-S/1000 en EL-L/1000.

U koppelt de serviceobjecten EL-S/1000 en EL-L/1000 aan de serviceovereenkomst.

U wilt de wijzigingen in de stuklijst registreren voor het serviceobject wanneer u onderdelen van het object vervangt. Daarom koppelt u een servicestuklijst aan de serviceobjectrelatie, zoals wordt beschreven in de volgende tabel.

| Serviceobject | Relatie - Serviceovereenkomst | Servicestuklijst   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | BOM-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | BOM-EL-L/1000 |

Aangezien er serviceobjectrelaties voor de overeenkomst zijn, kunt u nu serviceovereenkomstregels met deze objecten maken, zoals wordt weergegeven in de volgende tabel.

| Transactietype | Categorie           | Serviceobject |
|------------------|--------------------|----------------|
| Uur             | Inspectie         | EL-S/1000      |
| Uur             | Reiniging tandwielkast  | EL-S/1000      |
| Artikel             | Schoonmaakmaterialen | EL-S/1000      |
| Uur             | Inspectie         | EL-L/1000      |
| Uur             | Reiniging tandwielkast   | EL-L/1000      |
| Artikel             | Schoonmaakmaterialen | EL-L/1000      |

Bij een servicebezoek moet u de tandwielkast voor de lift EL-S/1000 vervangen. Als u een onderdeel van het object wilt vervangen, kunt u de stuklijstontwikkelaar openen via de serviceobjectrelatie die u instelt voor de huidige serviceovereenkomst.

De stuklijstontwikkelaar openen via een serviceobjectrelatie

1. Serviceovereenkomsten
2. Dubbelklik op een serviceovereenkomst of klik op Serviceovereenkomst om een nieuwe serviceovereenkomst te maken.
3. Klik op het tabblad Instellingen.
4. Klik op Serviceobjecten om een sjabloonstuklijst te koppelen aan de serviceovereenkomst.
5. Klik in het formulier Serviceobjecten op Ontwerper om het formulier Ontwerper te openen als u de sjabloonstuklijst wilt wijzigen.

## <a name="automatically-created-service-orders"></a>Automatisch gemaakte serviceorders

Indien u automatisch serviceorders voor een serviceovereenkomst maakt, worden de serviceobjectrelaties in de overeenkomst ook in de serviceorders gemaakt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]