---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Egypte
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Egypte in Finance en Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592593"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Aan de slag met de invoegtoepassing voor elektronische facturering voor Egypte

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Egypte. Dit onderwerp liedt u door de configuratiestappen die landafhankelijk zijn in Regulatory Configuration Services (RCS) en vullen de stappen aan die worden beschreven in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspecifieke configuratie voor Egyptische elektronische factuur (EG) voor elektronische facturering

U moet enkele stappen voltooien om de functie Egyptische elektronische factuur (EG) voor elektronisch factureren te configureren. Sommige parameters van de configuraties worden met standaardwaarden gepubliceerd, dus ze moeten worden gecontroleerd en bijgewerkt om beter bij uw bedrijfsactiviteiten te passen.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie kunt uitvoeren, moet u het volgende doen:

- Een digitaal certificaat maken zoals wordt beschreven in de sectie **Digitaal certificaatgeheim maken** in [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md). Voor testdoeleinden levert de Egyptische belastingdienst specifieke digitale testcertificaten die alleen tijdens de test- en oplossingvalidatiefasen mogen worden gebruikt. Raadpleeg de website van de Egyptische belastingdienst via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.sit.invoicing.eta.gov.eg/faq/) voor meer informatie.
- Maak een Egyptische elektronische factuur (EG) voor de functie voor elektronische facturering voor uw organisatie, zoals beschreven in de sectie **Een functie voor elektronische facturering maken onder uw organisatieprovider** in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Invoegtoepassing voor functies voor elektronische facturering** of de functie voor elektronische facturering **Egyptische elektronische factuur (EG)** die u hebt gemaakt is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Selecteer op het tabblad **Instellingen** de functie **Verkoopfactuur** in het raster.
5. Selecteer **Bewerken** en selecteer op het tabblad **Acties** in de veldgroep **Acties** de optie **Json-document ondertekenen voor Egyptische belastingdienst**.
6. Selecteer in de veldgroep **Parameters** de parameter, **Certificaatnaam** en selecteer de naam van het digitale certificaat dat is gemaakt voor gebruik met de functie voor elektronische facturering.
7. Selecteer in de veldgroep **Acties** de optie **Integreren met de Egyptische ETA-service**. Herhaal deze stap voor de twee voorvallen van deze actie.
8. Selecteer in de veldgroep **Parameters** de optie **URL van webservice** en **URL van aanmeldingsservice** en controleer indien nodig de URL-parameters. Raadpleeg de website van de Egyptische belastingdienst voor de test- en productie-URL via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Selecteer **Opslaan** en sluit de pagina.
10. Zie [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te configureren.

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspecifieke configuratie van de toepassingsinstellingen voor de functie Egyptische elektronische factuur (EG) voor elektronische facturering

De configuratie van de toepassingsinstellingen voor de functie **Egyptische elektronische factuur (EG)** voor elektronische facturering vereist het uitvoeren van specifieke stappen. U moet deze stappen voltooien voordat u de functie Elektronische facturering implementeert in de serviceomgeving voor uw invoegtoepassing Elektronische facturering.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie voltooit, maakt en initieert u een functie **Egyptische elektronische factuur (EG)** voor elektronische facturering om de toepassingsinstellingen te configureren voor de functie **Egyptische elektronische factuur (EG)** voor elektronische facturering zoals beschreven in de sectie **De toepassingsinstellingen configureren** in het onderwerp [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS, in de sectie **Functies** van het werkgebied **Globalisatiefunctie** de tegel **Invoegtoepassing voor elektronische facturering**.
2. Controleer op de pagina **Invoegtoepassing voor functies voor elektronische facturering** of de functie voor elektronische facturering **Egyptische elektronische factuur (EG)** die u hebt gemaakt is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Selecteer op het tabblad **Instellingen** de optie **Toepassingsinstellingen** en selecteer in het veld **Verbonden toepassing** de toepassing waarin u wilt implementeren.
5. Controleer in het veld **Tabelnaam** of het klantfactuurjournaal is geselecteerd.
6. Selecteer **Responstypen** en selecteer vervolgens **Nieuw**.
7. Voer in het veld **Responstype** de tekst "Respons" in en voer in het veld **Beschrijving** de tekst "Beschrijving" in.
8. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
9. Selecteer in het veld **Modeltoewijzing** de optie **Modeltoewijzing van responsbericht** bij **(Preview) Importindeling responsbericht** en selecteer vervolgens **Opslaan**.
10. Selecteer **Nieuw** en voer in het veld **Responstype** de tekst "Responsgegevens" in als vaste waarde. Voer in het veld **Beschrijving** de tekst "Beschrijving" in.
11. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
12. Selecteer in het veld **Gegevensentiteitsnaam** de optie **Verkoopfactuurkopteksten V2**.
13. Selecteer in het veld **Modeltoewijzing** de optie **Responsgegevens voor Egypte importeren** bij **(Preview) Importindeling responsgegevens voor Egypte** en selecteer vervolgens **Opslaan**.
14. Zie [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md) voor de implementatie van de functie Elektronische facturering.

## <a name="privacy-notice"></a>Privacyverklaring

Voor het inschakelen van de functie **Egyptische elektronische factuur (EG)** moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-id voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Een beheerder kan de functie in- en uitschakelen door te navigeren naar **Organisatiebeheer** > **Instellingen** > **Parameters voor elektronische documenten**. Selecteer op het tabblad **Functies** de rij met de functie **Egyptische elektronische factuur (EG)** en maak de juiste selectie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)
- [Elektronische klantfacturen in Egypte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
