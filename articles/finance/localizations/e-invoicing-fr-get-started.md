---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Frankrijk
description: Dit artikel bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Frankrijk.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220646"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Aan de slag met de invoegtoepassing voor elektronische facturering voor Frankrijk

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dit artikel bevat informatie waarmee u aan de slag kunt met Elektronische facturering voor Frankrijk. U wordt door de configuratiestappen geleid die land-/regioafhankelijk zijn in de Regulatory Configuration Service (RCS). Deze stappen vullen de stappen aan die worden beschreven in [Aan de slag met de invoegtoepassing Elektronische facturering](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landspecifieke configuratie voor Franse Chorus Pro-indiening (FR) voor elektronische facturering

Een aantal stappen is vereist voor het configureren van de functie **Franse Chorus Pro-indiening (FR)** voor elektronisch factureren. Sommige van de parameters van de configuratie worden gepubliceerd met standaardwaarden. Deze waarden moeten worden gecontroleerd en bijgewerkt zodat ze beter uw bedrijfsactiviteiten weergeven.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit artikel start, moet aan de volgende vereisten zijn voldaan:

- Vertrouwd raken met elektronische facturering. Raadpleeg [Overzicht elektronische facturering](e-invoicing-service-overview.md) voor meer informatie.
- Meld u aan bij RCS en stel Elektronische facturering in. Zie de volgende artikelen voor meer informatie:

    - [Aanmelden voor Elektronische facturering en de service installeren](e-invoicing-sign-up-install.md)
    - [Azure-resources instellen voor Elektronische facturering](e-invoicing-set-up-azure-resources.md)
    - [De invoegtoepassing voor microservices in Lifecycle Services installeren](e-invoicing-install-add-in-microservices-lcs.md)
    - [De integratie met elektronische facturering instellen en activeren](e-invoicing-activate-setup-integration.md): gebruik de informatie in dit artikel om de integratie tussen uw app voor Microsoft Dynamics 365 Finance of Dynamics 365 Supply Chain Management en de elektronische factureringsservice in te stellen.
    - [NAF-codes en siret-nummers](emea-fra-naf-codes-siret-numbers.md) en [NAF-codes en Siret-nummers instellen](tasks/fr-00003-naf-codes-siret-numbers.md): gebruik de informatie in deze artikelen om NAF-codes en Siret-nummers in uw rechtspersonen in te stellen. 

- Uw organisatie moet zijn geregistreerd om te werken met Chorus Pro. Microsoft biedt integratie met Chorus Pro in OAuth2-modus via een API (Application Programming Interface). Raadpleeg de [officiële documentatie](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/) voor gedetailleerde informatie over de registratie van Chorus Pro en het activeren van de toepassing.

    Ga als volgt te werk om te registreren bij Chorus Pro.

    1. Ga naar de [PISTE-portal](https://piste.gouv.fr/en/component/apiportal/registration) om de registratie te starten. 
    2. Een toepassing registreren en gegevens voor OAuth (Open Authorization) activeren.
    3. Kopieer de client-ID van de OAuth-referenties en de geheime sleutel en sla deze op. U gebruikt deze informatie in latere stappen.
    4. Ga naar de portal voor [worden kassa ingeen Pro](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment). 
    5. Maak een technische account aan voor API-toegang. Raadpleeg [Het aanmaken van een technische account voor API-toegang in de productie](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/) voor meer informatie.
    6. Kopieer de gebruikers-ID van de technische account en het wachtwoord. U gebruikt deze informatie in latere stappen.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landspecifieke configuratie van de toepassingsinstellingen voor de functie Franse Chorus Pro-indiening (FR) voor elektronische facturering

Sommige parameters van de functie voor elektronische facturering **Franse Chorus Pro-indiening (FR)** worden met standaardwaarden gepubliceerd. Controleer de standaardwaarden en werk ze zo nodig bij zodat deze beter aansluiten bij uw bedrijfsvoering voordat u de functie Elektronische facturering in de serviceomgeving implementeert.

1. Maak in de Azure sleutelkluis geheimen aan met de bijbehorende referenties. Raadpleeg [Klantcertificaten en geheimen](e-invoicing-customer-certificates-secrets.md) voor meer informatie.
2. Importeer de laatste versie van de globalisatiefunctie **Franse Chorus Pro-indiening (FR)** zoals beschreven in [Functies importeren uit de Algemene opslagplaats](e-invoicing-import-feature-global-repository.md).
3. Maak een kopie van de geïmporteerde globalisatiefunctie en selecteer de configuratieprovider. Raadpleeg [Een globalisatiefunctie aanmaken](e-invoicing-create-new-globalization-feature.md) voor meer informatie.
4. Controleer op het tabblad **Versies** of de **concept**-versie is geselecteerd.
5. Selecteer op het tabblad **Instellingen** de functie **Afgeleide UBL-verkoopfactuur** in het raster.
6. Selecteer **Bewerken** en selecteer vervolgens op het tabblad **Verwerkingspijplijn** in het gedeelte **Verwerkingspijplijn** **(Voorbeeld) Integreren met Franse Chorus Pro** met de actienaam **Franse Chorus Pro indienen**.
7. Selecteer in het gedeelte **Parameters** in het veld **Naam geheim client-ID** de geheime naam die u voor de client-ID hebt aangemaakt in de sleutelkluis.
8. Selecteer in het veld **Geheime naam clientgeheim** de geheime naam die u voor het client-geheim hebt aangemaakt in de sleutelkluis.
9. Selecteer in het veld **Geheime naam van technische aanmelding** de geheime naam die u voor het aanmelden van de technische account hebt aangemaakt in de sleutelkluis.
10. Selecteer in het veld **Geheime naam van technisch wachtwoord** de geheime naam die u voor het wachtwoord van de technische account hebt aangemaakt in de sleutelkluis.
11. Selecteer op het tabblad **Verwerkingspijplijn** in het gedeelte **Verwerkingspijplijn** **Integreren met Franse Chorus Pro** met de actienaam **status Franse Chorus Pro-aanvraag**.
12. Selecteer in het gedeelte **Parameters** in het veld **Naam geheim client-ID** de geheime naam die u voor de client-ID hebt aangemaakt in de sleutelkluis.
13. Selecteer in het veld **Geheime naam clientgeheim** de geheime naam die u voor het client-geheim hebt aangemaakt in de sleutelkluis.
14. Selecteer in het veld **Geheime naam van technische aanmelding** de geheime naam die u voor het aanmelden van de technische account hebt aangemaakt in de sleutelkluis.
15. Selecteer in het veld **Geheime naam van technisch wachtwoord** de geheime naam die u voor het wachtwoord van de technische account hebt aangemaakt in de sleutelkluis.
16. Selecteer **Opslaan** en sluit de pagina.
17. Herhaal stap 6 tot en met 16 voor het instellen van de functies **Afgeleide UBL-projectfactuur**, **Afgeleide UBL-verkoopcreditnota** en **Afgeleide UBL-projectcreditnota**.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van de invoegtoepassing voor elektronische facturering](e-invoicing-service-overview.md)
- [Aan de slag met servicebeheer via de invoegtoepassing voor elektronische facturering](e-invoicing-get-started-service-administration.md)
- [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md)
