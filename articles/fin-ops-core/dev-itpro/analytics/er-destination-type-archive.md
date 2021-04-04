---
title: ER-bestemmingstype voor archief
description: Dit onderwerp bevat informatie over het configureren van een archiefbestemming voor elke map- of bestandscomponent van een ER-indeling (Electronic Reporting).
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72b896ca692a54200ff79b14d0b5dc6ab4b0fe27
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562041"
---
# <a name="archive-er-destination-type"></a>ER-bestemmingstype voor archief

[!include [banner](../includes/banner.md)]

U kunt een archiefbestemming configureren voor elk onderdeel **Map** of **Bestand** van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten. Op basis van de doelinstelling wordt een gegenereerd document opgeslagen als een bijlage van een record van de ER-takenlijst. U kunt de resultaten weergeven door naar **Organisatiebeheer** \> **Elektronische aangifte** \> **Elektronische rapportagetaken** te gaan.

Met deze optie kunt u het gegenereerde document naar een Microsoft SharePoint-map of naar de Microsoft Azure-opslag verzenden. Stel **Ingeschakeld** in op **Ja** om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype. Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie. U definieert document [typen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) onder **Organisatiebeheer** \> **Documentbeheer** \> **Documenttypen**. De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.

[![Pagina Documenttypen](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

De locatie bepaalt waar het bestand wordt opgeslagen. Nadat de bestemming **Archief** is ingeschakeld, kunnen de resultaten worden opgeslagen in het taakarchief. U kunt de resultaten weergeven via **Organisatiebeheer** \> **Elektronische aangifte** \> **Gearchiveerde taken elektronische aangifte**.

> [!NOTE]
> Selecteer een documenttype voor het taakarchief via **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische aangifte** \> **Elektronische rapportparameters**. Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup) voor meer informatie.

## <a name="sharepoint"></a>SharePoint

U kunt een bestand opslaan in een aangewezen SharePoint-map. Als u de standaard-SharePoint-server wilt definiëren, gaat u naar **Organisatiebeheer** \> **Documentbeheer** \> **Parameters voor documentbeheer**. Configureer op het tabblad **SharePoint** de SharePoint-map. Vervolgens kunt u deze selecteren als de map waarin de ER-uitvoer wordt opgeslagen. De **SharePoint**-locatie moet worden geselecteerd in dit documenttype.

[![Een SharePoint-map selecteren](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>Azure-opslag

Als de locatie van het documenttype is ingesteld op **Azure-opslag**, kunt u een bestand opslaan in Azure-opslag.

> [!NOTE] 
> In het huidige ER-raamwerk worden bestanden in de Azure Blob-opslag opgeslagen, in tegenstelling tot het raamwerk voor gegevensbeheer waarin het bewaarbeleid van zeven dagen wordt toegepast voor documenten die moeten worden verwerkt. Zie [API voor ophalen van berichtstatus](../data-entities/recurring-integrations.md#api-for-getting-message-status) en [API voor statuscontrole](../data-entities/data-management-api.md#status-check-api) voor meer informatie . De ER-gerelateerde bestanden worden in de Azure Blob-opslag zo lang als nodig is opgeslagen als bijlagen van toepassingstabelrecords. Een enkel bestand wordt verwijderd uit de Azure Blob-opslag, samen met de toepassingstabelrecord waaraan dit bestand is gekoppeld.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
- [Documentbeheer configureren](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]