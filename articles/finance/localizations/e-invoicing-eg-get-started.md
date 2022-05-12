---
title: Elektronische facturering voor Egypte
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Egypte in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
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
ms.openlocfilehash: e21c4ce4d676c3194665672a078dc1e3d0492799
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661717"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektronische facturering voor Egypte

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Egypte. U wordt door de configuratiestappen geleid die land-/regioafhankelijk zijn in de Regulatory Configuration Service (RCS). Hiermee vult u de stappen aan die worden beschreven in [Elektronische facturering instellen](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp start, moet aan de volgende vereisten zijn voldaan:

- Zorg dat u weet hoe elektronische facturering werkt zoals beschreven in [Overzicht van Elektronische facturering](e-invoicing-service-overview.md).
- Meld u aan bij RCS en stel Elektronische facturering in. Zie de volgende onderwerpen voor meer informatie:

    - [Aanmelden voor Elektronische facturering en de service installeren](e-invoicing-sign-up-install.md)
    - [Azure-resources instellen voor Elektronische facturering](e-invoicing-set-up-azure-resources.md)
    - [De invoegtoepassing voor microservices in Lifecycle Services installeren](e-invoicing-install-add-in-microservices-lcs.md)
    
- De integratie activeren tussen Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management en de elektronische factureringsservice zoals beschreven in [De integratie met Elektronische facturering activeren en instellen](e-invoicing-activate-setup-integration.md).
- Maak een digitaal certificaatgeheim in de Azure Key Vault en stel dit in zoals wordt beschreven in [Klantcertificaten en geheimen](e-invoicing-customer-certificates-secrets.md). Voor testdoeleinden levert de Egyptische belastingdienst specifieke digitale testcertificaten die alleen tijdens de test- en oplossingvalidatiefasen mogen worden gebruikt. Ga naar de website van de Egyptische belastingdienst via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.invoicing.eta.gov.eg/faq/) voor meer informatie.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Landspecifieke configuratie voor de functie Egyptische elektronische factuur (EG)

Sommige parameters van de elektronische factureringsfunctie **Egyptische elektronische factuur (EG)** worden met standaardwaarden gepubliceerd. Controleer de standaardwaarden en werk ze zo nodig bij zodat deze beter aansluiten bij uw zakelijke bewerking voordat u de functie Elektronische facturering in de serviceomgeving implementeert.

1. Importeer de laatste versie van de globalisatiefunctie **Egyptische elektronische factuur (EG)** zoals beschreven in [Functies importeren uit de Algemene opslagplaats](e-invoicing-import-feature-global-repository.md).
2. Maak een kopie van de geïmporteerde globalisatiefunctie en selecteer uw configuratieprovider, zoals wordt beschreven in [Een Globalisatiefunctie maken](e-invoicing-create-new-globalization-feature.md).
3. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
4. Selecteer op het tabblad **Instellingen** de functie **Afgeleide verkoopfactuur** in het raster.
5. Selecteer **Bewerken**.
6. Selecteer op het tabblad **Verwerkingspijplijn** in de veldgroep **Verwerkingspijplijn** de optie **Json-document ondertekenen voor Egyptische belastingdienst**.
7. Selecteer in de sectie **Parameters** **Certificaatnaam** en selecteer vervolgens de naam van het digitale certificaat dat u hebt gemaakt.
8. Selecteer in de sectie **Verwerkingspijplijn** de optie **Integreren met de Egyptische ETA-service**. Herhaal deze stap voor de twee voorvallen van deze actie.
9. Selecteer in de sectie **Parameters** de **URL van de webservice** en de **URL van de aanmeldingsservice**. Controleer vervolgens de URL-parameters. Voor het ophalen van de test- en productie-URL gaat u naar de website van de Egyptische belastingdienst via de koppeling die is verstrekt in de [Egyptische SDK voor e-facturering](https://sdk.invoicing.eta.gov.eg/faq/).
10. Selecteer **Opslaan** en sluit de pagina.
11. Herhaal stap 4 tot en met 10 voor de instelling van de functie **Afgeleide projectfactuur**.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Landspecifieke configuratie voor de toepassinginstelling voor Egyptische elektronische factuur (EG)

Er zijn parameters die moeten worden ingesteld in uw Finance- of Supply Chain Management-omgeving. U kunt deze instelling op een van de volgende twee locaties voltooien:

- Rechtstreeks in uw Finance- of Supply Chain Management-omgeving. Zie [Parameters voor Elektronische facturering instellen](e-invoicing-set-up-parameters.md) voor meer informatie.
- In RCS. Bij het instellen van de elektronische factureringsfunctie kunt u alle parameters definiëren en deze vervolgens rechtstreeks implementeren in uw Finance- of Supply Chain Management-omgeving wanneer u de elektronische factureringsfunctie implementeert.

Voor beide opties zijn de parameters gelijk. Als u uw eerste functie in de elektronische factureringsservice instelt, raden we u aan om deze stappen uit te voeren om de parameters in te stellen in RCS en ze vervolgens in uw verbonden toepassing te implementeren.

> [!NOTE]
> Sommige versies van de elektronische factureringsfunctie kunnen een vooraf gedefinieerde set toepassingsspecifieke parameters bevatten voor Finance of Supply Chain Management. In dit geval moet u controleren of de gegevens juist zijn. Anders stelt u de parameters handmatig in.

1. Zoek de kopie van de globalisatiefunctie **Elektronische factuur Egypte (EG)** die u hebt gemaakt.
2. Controleer op het tabblad **Versies** of de **concept** versie is geselecteerd.
3. Selecteer op het tabblad **Setups** de optie **Setup van de toepassing**.
4. Selecteer in het veld **Verbonden toepassingen** de toepassing waarvoor u de parameters wilt implementeren.
5. Selecteer **Toevoegen** om een record te maken op de pagina **Elektronische documenttypen**.
6. Voeg **CustInvoiceJour** toe in het veld **Tabelnaam**.
7. Voeg in het veld **Context** een verwijzing toe aan de toewijzingsnaam **Klantfactuurcontext**. De configuratie is het **Contextmodel klantfactuur**.
8. Voeg in het veld **Elektronische documenttoewijzing** een verwijzing toe aan de toewijzingsnaam **Klantfactuur**. De configuratie is **Factuurmodeltoewijzing**.
9. Selecteer **Opslaan**.
10. Selecteer op de pagina **Responstypen** de optie **Toevoegen**.
11. Voer in het veld **Antwoordtype** de waarde **Antwoord** in.
12. Voer in het veld **Beschrijving** **Respons verwerken** in.
13. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
14. Selecteer **Responsbericht importeren** in het veld **Modeltoewijzing**. De configuratie is **Responsbericht importeren voor Egypte (EG)**.
15. Selecteer **Opslaan**.
16. Selecteer **Toevoegen**.
17. Voer in het veld **Antwoordtype** de waarde **ResponseData** in.
18. Voer in het veld **Beschrijving** **Responsgegevens verwerken** in.
19. Selecteer in het veld **Indieningsstatus** de optie **In behandeling**.
20. Selecteer in het veld **Gegevensentiteitsnaam** de optie **SalesInvoiceHeaderV2Entity**.
21. Selecteer **Responsgegevens importeren** in het veld **Modeltoewijzing**. De configuratie is **importindeling van responsgegevens voor Egypte (EG)**.
22. Selecteer **Opslaan** en sluit de pagina.
23. Sluit de pagina.

Zie [Een globalisatiefunctie voltooien, publiceren en implementeren](e-invoicing-complete-publish-deploy-globalization-feature.md) om een functie in de serviceomgeving en de instellingen voor de gekoppelde Finance- of Supply Chain Management-toepassing te implementeren.

## <a name="privacy-notice"></a>Privacyverklaring

Als u de functie **Elektronische factuur Egypte (EG)** wilt inschakelen, moeten mogelijk beperkte gegevens worden verzonden. Deze gegevens omvatten de belastingregistratie-id van de organisatie. De gegevens worden verzonden naar instanties van derden die door de belastingdienst zijn gemachtigd elektronische facturen naar die belastingdienst te verzenden in de vooraf gedefinieerde indeling die vereist is voor integratie met de webservice van de overheid. Een beheerder kan de functie in- en uitschakelen via **Organisatiebeheer** \> **Instellingen** \> **Parameters voor elektronische documenten**. Selecteer op het tabblad **Functies** de rij met de functie **Egyptische elektronische factuur (EG)** en maak de juiste selectie. Op gegevens die zijn geïmporteerd van externe systemen naar deze Dynamics 365 online service, is de [privacyverklaring](https://go.microsoft.com/fwlink/?LinkId=512132) van toepassing. Zie de sectie 'Privacyverklaring' in de documentatie over land-/regiospecifieke functies voor meer informatie.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van Elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer voor Elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met Elektronische facturering](e-invoicing-get-started.md)
- [Elektronische klantfacturen in Egypte](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
