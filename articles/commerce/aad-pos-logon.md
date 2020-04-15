---
title: Azure Active Directory-verificatie inschakelen voor POS-aanmelding
description: In dit onderwerp wordt uitgelegd hoe u de aanmeldingservaring voor het Microsoft Dynamics 365 Commerce-verkooppunt (POS) zo configureert dat Azure Active Directory-verificatie wordt gebruikt.
author: boycezhu
manager: annbe
ms.date: 03/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: f030e8382627191dd32d855e15432fc85dca4bbd
ms.sourcegitcommit: 1789a78de1cbeac19d96767812df653a191c67e9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100375"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>Azure Active Directory-verificatie inschakelen voor POS-aanmelding
[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Veel klanten die Microsoft Dynamics 365 Commerce gebruiken, gebruiken ook andere Microsoft-cloudservices en ze kunnen Azure Active Directory (Azure AD) gebruiken om gebruikersreferenties voor deze services te beheren. In deze gevallen willen de klanten mogelijk dezelfde Azure AD-account gebruiken voor verschillende toepassingen. In dit onderwerp wordt uitgelegd hoe u de aanmeldingservaring voor het Commerce-verkooppunt (POS) zo configureert dat Azure AD-verificatie wordt gebruikt.

## <a name="configure-azure-ad-authentication"></a>Azure AD-verificatie configureren

Als u Azure AD beschikbaar wilt maken als de verificatiemethode voor POS-aanmelding voor een winkel, moet u de instellingen van het functionaliteitsprofiel van de winkel configureren en deze instelling vervolgens toepassen op POS-clients.

Volg deze stappen om een functionaliteitsprofiel te configureren.

1. Ga naar **Retail en Commerce** \> **Kanaalinstellingen** \> **POS-instellingen** \> **POS-profielen** \> **Functionaliteitsprofielen**.
1. Selecteer het functionaliteitsprofiel dat u wilt wijzigen.
1. Wijzig op het sneltabblad **Functies** in de sectie **Aanmelding POS-personeel** de waarde van het veld **Verificatiemethode bij aanmelding** van **Personeels-id en wachtwoord** in **Azure Active Directory**.

Standaard gebruiken alle functionaliteitsprofielen **Personeels-id en wachtwoord** als de POS-verificatiemethode. Daarom moet u de waarde van het veld **Verificatiemethode bij aanmelding** wijzigen als u Azure AD wilt gebruiken. Elke detailhandelwinkel die is gekoppeld aan het geselecteerde functionaliteitsprofiel wordt beïnvloed door deze wijziging.

Voer de volgende stappen uit om de instellingen toe te passen op POS-clients.

1. Ga naar **Retail en Commerce** \> **Retail en Commerce IT** \> **Distributieplanning**.
1. Voer de distributieplanning **1070** (**Kanaalconfiguratie**) uit.

> [!NOTE]
> Voor Azure AD-verificatie is een internetverbinding vereist. Het werkt niet als POS zich in de offlinemodus bevindt.

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Een Azure AD-account aan een werknemer koppelen

Voordat een winkelmedewerker een Azure AD-account kan gebruiken om zich aan te melden bij de POS-toepassing, moet de Azure AD-account worden gekoppeld aan die werknemer.

Voer de volgende stappen uit om een Azure AD-account aan een werknemer te koppelen.

1. Ga naar **Detailhandel en commerce** \> **Werknemers** \> **Werknemers**.
1. De gegevenspagina voor een werknemer.
1. Selecteer in het actievenster op het tabblad **Commerce** in de groep **Externe identiteit** de optie **Bestaande identiteit koppelen**.
1. Selecteer in het dialoogvenster **Bestaande externe identiteit gebruiken** de optie **Zoeken met behulp van e-mail**, voer een Azure AD-e-mailadres in en selecteer **Zoeken**.
1. Selecteer de Azure AD- account die wordt geretourneerd en klik op **OK**.

De velden **Alias**, **UPN** en **Externe sub-id** op het tabblad **Commerce** van de pagina met werknemersgegevens wordt ingevuld.

## <a name="additional-resources"></a>Aanvullende bronnen

[Uitgebreide aanmeldingsfunctionaliteit instellen voor MPOS en Cloud POS](extended-logon.md)

[Een functionaliteitsprofiel voor detailhandel maken](retail-functionality-profile.md)

[ Een medewerker configureren](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)