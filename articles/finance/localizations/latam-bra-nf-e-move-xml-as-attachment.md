---
title: NF-e XML-bestanden als bijlagen verplaatsen
description: In dit artikel wordt uitgelegd hoe u NF-e XML-bestanden uit uw Microsoft Microsoft Dynamics 365 Finance- of Dynamics 365 Supply Chain Management-database verplaatst en ze in plaats daarvan beschikbaar maakt als bijlagen.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 7bb0fb975c6d73cc4e990b39ea9b5a0c0455db74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270619"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML-bestanden als bijlagen verplaatsen

[!include [banner](../includes/banner.md)] 


Wanneer elektronische belastingdocumenten (NF-e) worden uitgegeven, worden XML-bestanden gemaakt en opgeslagen in de Microsoft Dynamics 365 Finance- en Dynamics 365 Supply Chain Management-databases. In de Braziliaanse lokalisatie kunt u de functie **NF-e XML verplaatsen als bijlage** gebruiken om de databaseruimte vrij te maken die door deze XML-bestanden wordt verbruikt.

Voor een bepaald datumbereik en voor fiscale vestiging verplaatst de functie de NF-e XML-bestanden van uw Finance- of Supply Chain Management-database naar de Blob-opslag van uw Azure-abonnement. Door deze verplaatsing worden de bestanden alleen als bijlagen beschikbaar. Nadat de XML-bestanden zijn verplaatst naar de Blob-opslag, worden de oorspronkelijke bestanden verwijderd uit de Finance- of Supply Chain Management-database. Daarom wordt de databaseruimte vrijgegeven die door de gebruikte bestanden werd ingenomen.

Volg deze stappen om de functie **NF-e XML verplaatsen als bijlage** in te schakelen.

1. In Finance of Supply Chain Management opent u het werkgebied **Functiebeheer**.
2. Zoek op het tabblad **Alle** naar de functie **NF-e XML verplaatsen als bijlage** en selecteer deze.
3. Selecteer **Nu inschakelen**.

Volg deze stappen om NF-e XML-bestanden te verplaatsen als bijlagen.

1. Ga naar **Klanten** \> **Fiscale documenten** \> **Elektronische fiscale documenten** \> **NF-e XML verplaatsen als bijlagen**.
2. Selecteer de begin- en einddatum in het veld **Begindatum** en **Einddatum**.
3. Selecteer een waarde in het veld **Id fiscale instelling**.
4. Selecteer **OK**.

> [!IMPORTANT]
> Dit proces is onomkeerbaar. Nadat u de NF-e XML-bestanden hebt verplaatst, kunnen gebruikers deze alleen weergeven door **Bijlagen** boven aan de pagina **Fiscaal document** te selecteren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
