---
title: Validatie van aangepast certificaat NF-e
description: Dit onderwerp bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813963"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="3183d-103">Validatie van aangepast certificaat NF-e</span><span class="sxs-lookup"><span data-stu-id="3183d-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3183d-104">Wanneer u de functie voor verificatie van aangepaste certificaat NF-e inschakelt, kan met aangepaste validatie een verbinding met de webservices tot stand worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="3183d-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="3183d-105">Deze verbinding is vereist voor het verzenden van NF-e en het ontvangen van autorisatie van SEFAZ.</span><span class="sxs-lookup"><span data-stu-id="3183d-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="3183d-106">De eigenschap **Doel van serververificatie** van certificaat V5 wordt uitgegeven door de Braziliaanse basiscertificeringsinstantie.</span><span class="sxs-lookup"><span data-stu-id="3183d-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="3183d-107">Deze eigenschap is standaard uitgeschakeld en moet handmatig worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3183d-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="3183d-108">In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="3183d-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="3183d-109">In dat geval wordt de TLS-verbinding beïnvloed en wordt deze niet meer vertrouwd.</span><span class="sxs-lookup"><span data-stu-id="3183d-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="3183d-110">Ook de mogelijkheid om NF-e te verlenen aan productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR) wordt beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="3183d-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="3183d-111">Met deze update is een alternatieve oplossing voor certificaatvalidatie mogelijk, wat inhoudt dat beveiligde communicatie tot stand kan worden gebracht.</span><span class="sxs-lookup"><span data-stu-id="3183d-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]