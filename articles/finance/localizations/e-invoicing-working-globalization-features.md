---
title: Onderdelen van globalisatiefunctie
description: Dit artikel geeft een overzicht van de onderdelen van de globalisatiefunctie.
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
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891483"
---
# <a name="globalization-feature-components"></a>Onderdelen van globalisatiefunctie

[!include [banner](../includes/banner.md)]

Een globalisatiefunctie is een set onderdelen die de regels voor gegevenstransformatie in ER-configuraties (Electronic Reporting) definiëren. Deze onderdelen bevatten onder andere instructies voor het verwerken van elektronische documenten en het verzenden naar of ontvangen van documenten vanuit externe kanalen. Deze bevatten ook voorwaarden waarmee wordt bepaald wanneer een functie moet worden uitgevoerd voor de binnenkomende bedrijfsgegevens.

Alle onderdelen zijn van elkaar afhankelijk. Met globalisatiefuncties kunt u deze afhankelijkheid eenvoudig maken en onderhouden, en levenscyclusbeheer en versiebeheer van de set componenten ondersteunen.

## <a name="access-electronic-invoicing-feature-components"></a>Toegang tot onderdelen van de elektronische factureringsfunctie 

1. Meld u aan bij uw RCS-account (Regulatory Configuration Service).
2. Selecteer in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.

    Globalisatiefuncties bestaan uit verschillende onderdelen. De pagina **Elektronische factureringsfuncties** bevat een afzonderlijk tabblad voor elk onderdeel.

    - **Versie**: dit onderdeel ondersteunt levenscyclusbeheer van de functie. U kunt de functie gebruiken om de status te beheren voor verschillende versies van de functie.
    - **Configuraties**: met dit onderdeel kunt u gerelateerde ER-indelings- en indelingstoewijzingsconfiguraties beheren, weergeven en bewerken die in de verwerkingspijplijn worden gebruikt.
    - **Instellingen**: hiermee kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de instellingen van de gerelateerde functieversie beheren. Daarom ondersteunt deze de flexibele constructie van communicatie- en antwoordregels.
    - **Omgevingen**: met dit onderdeel kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de omgeving beheren waarin de versie-instellingen van de functie worden gebruikt. Ze kunnen ook machtigingen toekennen aan gebruikers die toegang hebben tot de versie-instellingen van de functie.
    - **Organisaties**: met dit onderdeel kunnen gebruikers de functie delen met externe organisaties.
    - **Labels**: met dit onderdeel kunt u labelfuncties gebruiken in de globalisatieblauwdruk voor de verwijzing.
