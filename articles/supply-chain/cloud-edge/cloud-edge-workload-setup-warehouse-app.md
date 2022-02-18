---
title: De mobiele app Warehouse Management configureren voor cloud- en randschaaleenheden
description: In dit onderwerp wordt uitgelegd hoe u uw de mobiele apps voor Warehouse Management instelt voor magazijnen waarvoor een cloud- of randschaaleenheid wordt gebruikt.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071636"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>De mobiele app Warehouse Management configureren voor cloud- en randschaaleenheden

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u uw mobiele apps voor Warehouse Management instelt zodat ze kunnen worden gebruikt voor magazijnen waarvoor een cloud- of randschaaleenheid wordt gebruikt.

## <a name="prerequisites"></a>Vereisten

Voordat u begint met het instellen van uw mobiele apparaten om verbinding te maken met een cloud- of randschaaleenheid, moet u controleren of ze verbinding kunnen maken met de bedrijfshub. Zie [De mobiele app Warehouse Management installeren en verbinden](../warehousing/install-configure-warehouse-management-app.md) voor instructies.

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Aanvullende instellingen wanneer u de mobiele app Warehouse Management uitvoert voor een schaaleenheid

Als onderdeel van het [implementatieproces voor workload van magazijnbeheer voor schaaleenheden](cloud-edge-landing-page.md#scale-unit-manager-portal) worden de meeste gegevens die nodig zijn om verbinding te maken met uw apparaten voor de mobiele app Warehouse Management, automatisch gesynchroniseerd vanuit de bedrijfshub met de schaaleenheid. U moet de gegevens echter invoeren op de pagina **Azure Active Directory-toepassingen** (**Systeembeheer \> Instellingen \> Azure Active Directory-toepassingen**) in de implementatie van de schaaleenheid. Daarnaast moet u mogelijk de standaardwaarde van **Bedrijf** bijwerken voor de gebruikers-id of een nieuwe gebruiker maken. Gebruikers die zijn gekoppeld aan een bedrijf dat niet voorkomt in een implementatie van de schaaleenheid, kunnen zich niet aanmelden als de mobiele app Warehouse Management is verbonden met die schaaleenheid.

> [!NOTE]
> Omdat de gegevens op de pagina **Azure Active Directory-toepassingen** niet worden gesynchroniseerd, moet u deze gegevens handmatig onderhouden als u uw magazijnworkloads naar een andere schaaleenheid wilt verplaatsen.

Houd er rekening mee dat, als onderdeel van de verbindingsinstelling van elke mobiele app voor Warehouse Management, de opgegeven resource-URL van Azure Active Directory voor de schaaleenheid moet zijn en niet voor de bedrijfshub.
