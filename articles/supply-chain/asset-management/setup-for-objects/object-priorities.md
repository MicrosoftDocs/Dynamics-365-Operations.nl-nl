---
title: Serviceniveaus van activa
description: In dit onderwerp worden serviceniveaus voor activa in Activabeheer uitgelegd.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e2f8d2ac0c48d4f92b15ec345ffa650b71df0b
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571019"
---
# <a name="asset-service-levels"></a>Serviceniveaus van activa

[!include [banner](../../includes/banner.md)]

 

In dit onderwerp worden serviceniveaus voor activa in Activabeheer uitgelegd. Serviceniveaus van activa zijn gerelateerd aan activa en worden overgebracht naar onderhoudsaanvragen en werkorders. Ze worden gebruikt om de prioriteit van werkorders te berekenen tijdens de planning van de werkorder. Serviceniveaus van activa kunnen worden gewijzigd als er wijzigingen nodig zijn.

Zie [Parameters voor Activabeheer](../setup-for-objects/enterprise-asset-management-parameters.md) voor meer informatie over de instellingen die zijn gerelateerd aan de berekening van beoordelingsscores voor de planning van werkorders. U moet ten minste één standaardrecord instellen voor het serviceniveau van de activa. Deze standaardrecord wordt gebruikt als er geen andere overeenkomst wordt gevonden tijdens de planning van de werkorder.

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
