---
title: De invoegtoepassing voor microservices in Lifecycle Services installeren
description: In dit artikel wordt uitgelegd hoe u de invoegtoepassing Elektronische facturering kunt installeren in Microsoft Dynamics Lifecycle Services (LCS).
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 26f92262eff07ded3e894ee5513dd8dbaa6f94a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849800"
---
# <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>De invoegtoepassing voor microservices in Lifecycle Services installeren

[!include [banner](../includes/banner.md)]

Voor de verificatie in de elektronische factureringsservice moet u de Microsoft Dynamics 365 Finance- of Dynamics 365 Supply Chain Management-omgeving registreren op het serviceplatform door de invoegtoepassing voor uw omgeving in Microsoft Dynamics Lifecycle Services (LCS) te installeren.

Ga als volgt te werk om een omgeving te registreren.

1. Meld u aan bij uw LCS-account.
2. Selecteer een LCS-project op uw projectdashboard.
2. Selecteer in het project op het dashboard **Omgevingen** uw geïmplementeerde omgeving. De omgeving die u selecteert, moet actief zijn.
3. Selecteer op het tabblad **Power Platform-integratie** in de sectie **Omgevingsinvoegtoepassingen** de optie **Een nieuwe invoegtoepassing installeren**.
4. Selecteer **Elektronische facturering**.
5. Voer in het veld **AAD-toepassings-id** **091c98b0-a1c9-4b02-b62c-7753395ccabe** in. Dit is een vaste waarde. Zorg ervoor dat u alleen een Globally Unique Identifier (GUID) opgeeft. Voeg geen andere symbolen toe, zoals spaties, komma's, punten of aanhalingstekens.
6. Voer in het veld **AAD-tenant-id** de tenant-id van uw Azure-abonnementsaccount in. De tenant Azure Active Directory (Azure AD) die u opgeeft, moet dezelfde tenant zijn die wordt gebruikt voor RCS (Regulatory Configuration Service).
7. Neem de algemene voorwaarden door en schakel vervolgens het selectievakje in.
8. Selecteer **Installeren**. Na enkele minuten verandert de status van **Bezig met installeren** in **Geïnstalleerd**. U moet de pagina mogelijk vernieuwen om deze wijziging te bekijken.

Elektronische facturering kan nu worden gebruikt.

> [!NOTE]
> Bedrijven hebben doorgaans verschillende Finance- of Supply Chain Management-omgevingen. Deze omgevingen omvatten productieomgevingen, UAT-omgevingen (User Acceptance Test) en ontwikkelomgevingen (sandbox). U moet de voorgaande procedure voltooien voor alle omgevingen die u wilt verbinden met Elektronische facturering.
