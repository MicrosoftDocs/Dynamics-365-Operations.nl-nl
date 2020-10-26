---
title: Validatie van aangepast certificaat NF-e
description: Dit onderwerp bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973087"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="f422f-103">Validatie van aangepast certificaat NF-e</span><span class="sxs-lookup"><span data-stu-id="f422f-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f422f-104">Wanneer u de functie voor verificatie van aangepaste certificaat NF-e inschakelt, kan met aangepaste validatie een verbinding met de webservices tot stand worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="f422f-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="f422f-105">Deze verbinding is vereist voor het verzenden van NF-e en het ontvangen van autorisatie van SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="f422f-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="f422f-106">De eigenschap **Doel van serververificatie** van certificaat V5 wordt uitgegeven door de Braziliaanse basiscertificeringsinstantie.</span><span class="sxs-lookup"><span data-stu-id="f422f-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="f422f-107">Deze eigenschap is standaard uitgeschakeld en moet handmatig worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f422f-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="f422f-108">In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="f422f-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="f422f-109">In dat geval wordt de TLS-verbinding beïnvloed en wordt deze niet meer vertrouwd.</span><span class="sxs-lookup"><span data-stu-id="f422f-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="f422f-110">Ook de mogelijkheid om NF-e te verlenen aan productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR) wordt beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="f422f-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="f422f-111">Met deze update is een alternatieve oplossing voor certificaatvalidatie mogelijk, wat inhoudt dat beveiligde communicatie tot stand kan worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="f422f-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


