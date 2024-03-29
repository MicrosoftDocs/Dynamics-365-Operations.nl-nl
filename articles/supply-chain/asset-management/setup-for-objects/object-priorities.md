---
title: Serviceniveaus activum
description: In dit artikel worden serviceniveaus voor activa in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7429b30253f540925e67ff9239667a0a404f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908680"
---
# <a name="asset-service-levels"></a>Serviceniveaus activum

[!include [banner](../../includes/banner.md)]

 

In dit artikel worden serviceniveaus voor activa in Activabeheer uitgelegd. Serviceniveaus van activa zijn gerelateerd aan activa en worden overgebracht naar onderhoudsaanvragen en werkorders. Ze worden gebruikt om de prioriteit van werkorders te berekenen tijdens de planning van de werkorder. Serviceniveaus van activa kunnen worden gewijzigd als er wijzigingen nodig zijn.

Zie [Parameters voor activabeheer](../setup-for-objects/enterprise-asset-management-parameters.md) voor meer informatie over de instellingen die zijn gerelateerd aan de berekening van beoordelingsscores voor de planning van werkorders. U moet ten minste één standaardrecord instellen voor het serviceniveau van de activa. Deze standaardrecord wordt gebruikt als er geen andere overeenkomst wordt gevonden tijdens de planning van de werkorder.

**Voorbeeld 1**: het standaard serviceniveau dat wordt gebruikt als er geen andere overeenkomst wordt gevonden. In deze record selecteert u alleen een serviceniveau.

**Voorbeeld 2**: een hoog serviceniveau dat wordt gebruikt om taken voor een Volvo-truckmotor te plannen. In deze record selecteert u een relevant activumtype (zoals **truckmotor**), een fabrikant (**Volvo**) en een serviceniveau.

## <a name="set-up-asset-service-levels"></a>Serviceniveaus van activa instellen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Serviceniveaus van activa**.
2. Selecteer **Nieuw** om een record te maken.
3. Afhankelijk van het detailniveau dat is vereist voor het activumserviceniveau, moet u relevante selecties maken in de velden **Functionele locatie**, **Type activum**, **Fabrikant**, **Model**, **Activum**, **Type werkorder** en **Serviceniveau**.

    > [!NOTE]
    > Wanneer het serviceniveau voor activa wordt gebruikt voor onderhoudsaanvragen en werkorders, worden in Activabeheer alle activumserviceniveaurecords gecontroleerd op een mogelijke overeenkomst. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Dat wil zeggen dat Activabeheer eerst controleert op een overeenkomst voor het veld **Type werkorder**. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Activum** enzovoort. Zoals u kunt zien in de indeling van de pagina **Serviceniveaus voor activa**, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden. Als er geen overeenkomst wordt gevonden, wordt in deze velden de standaardrecord zonder selecties gebruikt.

4. Selecteer in het veld **Serviceniveau** een getal dat het serviceniveau (prioriteit) aangeeft.


> [!NOTE]
> Als u een activumserviceniveaurecord op de pagina **Serviceniveaus van activa** wijzigt nadat u deze al op een werkorder hebt gebruikt, wordt het serviceniveau voor onderhoudsaanvragen en werkorders niet dienovereenkomstig bijgewerkt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]