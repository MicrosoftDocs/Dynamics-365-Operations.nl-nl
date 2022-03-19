---
title: Azure-resources instellen voor Elektronische facturering
description: Dit onderwerp bevat een overzicht van het proces voor het instellen en configureren van Microsoft Azure-resources voor Elektronische facturering.
author: dkalyuzh
ms.date: 01/26/2022
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
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371559"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Azure-resources instellen voor Elektronische facturering

[!include [banner](../includes/banner.md)]

Het proces voor het instellen van Microsoft Azure-resources voor elektronische facturering heeft drie stappen. De eerste twee stappen "Een Azure Key Vault maken in de Azure-portal" en "Een Azure-opslagaccount maken in de Azure-portal" zijn verplicht. De derde stap "SharePoint-verbinding configureren" is optioneel.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Een Azure Key Vault maken in de Azure-portal

Maak een sleutelkluis in uw Azure-abonnement. Het is raadzaam om een afzonderlijke sleutelkluis voor elektronische facturering te maken en deze niet te combineren met andere toepassingen. Maak zoveel geheimen en certificaten als u voor alle scenario's in elektronische documenten nodig hebt. U moet ten minste één geheim maken om het SAS-token (Shared Access Signature) van het Azure-opslagaccount op te slaan dat u in de volgende stap gaat maken.

Zie [Azure Key Vault maken in de Azure-portal](e-invoicing-create-azure-key-vault-azure-portal.md) voor informatie over het voltooien van deze stap.

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Een Azure-opslagaccount maken in de Azure-portal

U bent eigenaar van alle elektronische documenten en bestanden die worden gegenereerd door de elektronische factureringsservice of die u in de service invoert. Deze documenten en bestanden worden opgeslagen in een Azure-opslagaccount dat u maakt in uw abonnement op Azure. De service krijgt toegang tot uw opslagaccount via het SAS-token dat is overgenomen van uw Key Vault-geheim.

Zie [Azure-opslagaccount maken in de Azure-portal](e-invoicing-create-azure-storage-account-azure-portal.md) voor informatie over het voltooien van deze stap.

## <a name="configure-a-sharepoint-connection"></a>Een SharePoint-verbinding configureren

In sommige scenario's moet u mogelijk elektronische bestanden opslaan om SharePoint en ze uit SharePoint ophalen. Om er zeker van te zijn dat de elektronische factureringsservice toegang heeft tot uw SharePoint-mappen, configureert u de toegang tot SharePoint.

Zie [Een SharePoint-verbinding configureren](e-invoicing-create-sharepoint-connection.md) voor informatie over het voltooien van deze stap.
