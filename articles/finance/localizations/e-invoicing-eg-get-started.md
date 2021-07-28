---
title: Aan de slag met Elektronische facturering voor Egypte
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Egypte in Finance en Supply Chain Management.
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 133c47d52bb301f862888c367d19fd58701ecb3c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6340124"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Aan de slag met Elektronische facturering voor Egypte

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Egypte. Dit onderwerp leidt u door de configuratiestappen die landafhankelijk zijn in Regulatory Configuration Services (RCS) en vullen de stappen aan die worden beschreven in het onderwerp [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspecifieke configuratie voor Egyptische elektronische factuur (EG) voor elektronische facturering

Sommige parameters van de **Egyptische elektronische factuur (EG) voor elektronische facturering** worden met standaardwaarden gepubliceerd. Controleer de waarden en werk ze zo nodig bij zodat deze beter aansluiten bij uw zakelijke bewerkingsbehoeften voordat u de functie Elektronische facturering in de serviceomgeving implementeert.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie voor de functie voor elektronische facturering** in het onderwerp [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

### <a name="prerequisites"></a>Vereisten

Voordat u de procedure in deze sectie kunt uitvoeren, moet u het volgende doen:

- Een digitaal certificaat maken zoals wordt beschreven in de sectie **Digitaal certificaatgeheim maken** in [Aan de slag met servicebeheer via Elektronische facturering](e-invoicing-get-started-service-administration.md). Voor testdoeleinden levert de Egyptische belastingdienst specifieke digitale testcertificaten die alleen tijdens de test- en oplossingvalidatiefasen mogen worden gebruikt. Raadpleeg de website van de Egyptische belastingdienst via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.sit.invoicing.eta.gov.eg/faq/) voor meer informatie.

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Egyptische elektronische factuur (EG)** die u hebt gemaakt is geselecteerd.
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Selecteer op het tabblad **Instellingen** de functie **Verkoopfactuur** in het raster.
5. Selecteer **Bewerken** en selecteer op het tabblad **Acties** in de veldgroep **Acties** de optie **Json-document ondertekenen voor Egyptische belastingdienst**.
6. Selecteer in de veldgroep **Parameters** de parameter, **Certificaatnaam** en selecteer de naam van het digitale certificaat dat is gemaakt voor gebruik met de functie voor elektronische facturering.
7. Selecteer in de veldgroep **Acties** de optie **Integreren met de Egyptische ETA-service**. Herhaal deze stap voor de twee voorvallen van deze actie.
8. Selecteer in de veldgroep **Parameters** de optie **URL van webservice** en **URL van aanmeldingsservice** en controleer indien nodig de URL-parameters. Raadpleeg de website van de Egyptische belastingdienst voor de test- en productie-URL via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Selecteer **Opslaan** en sluit de pagina.
10. Zie [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md) voor de implementatie van de functie Elektronische facturering in de sericeomgeving.

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Landspecifieke configuratie van de toepassingsinstellingen voor de functie Egyptische elektronische factuur (EG) voor elektronische facturering

Voltooi deze stappen voordat u de toepassingsinstellingen implementeert naar uw verbonden toepassing Finance of Supply Chain Management.

Deze sectie is een aanvulling op de sectie **Landspecifieke configuratie van toepassingsinstellingen** in het onderwerp [Aan de slag met Elektronische facturering](e-invoicing-get-started.md).

1. Selecteer in RCS in de werkruimte **Globalisatiefunctie** in de sectie **Functies** de tegel **Elektronische facturering**.
2. Controleer op de pagina **Functies voor elektronische facturering** of de functie voor elektronische facturering **Egyptische elektronische factuur (EG)** die u hebt gemaakt is geselecteerd.
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
14. Zie [Aan de slag met Elektronische facturering](e-invoicing-get-started.md) om de toepassingsinstellingen te implementeren in de verbonden toepassing Finance of Supply Chain Management.

## <a name="privacy-notice"></a>Privacyverklaring

Voor het inschakelen van de functie **Egyptische elektronische factuur (EG)** moeten mogelijk beperkte gegevens worden verzonden, waaronder de belastingregistratie-id voor de organisatie. Deze gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar de belastingdienst te verzenden in de vooraf gedefinieerde indeling die nodig is voor integratie met de webservice van de overheid. Een beheerder kan de functie in- en uitschakelen door te navigeren naar **Organisatiebeheer** > **Instellingen** > **Parameters voor elektronische documenten**. Selecteer op het tabblad **Functies** de rij met de functie **Egyptische elektronische factuur (EG)** en maak de juiste selectie. Op gegevens die zijn geïmporteerd van deze externe systemen naar deze Dynamics 365 online service , is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de secties met betrekking tot de Privacyverklaring in documentatie over landspecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer voor Elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met Elektronische facturering](e-invoicing-get-started.md)
- [Elektronische klantfacturen in Egypte](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
