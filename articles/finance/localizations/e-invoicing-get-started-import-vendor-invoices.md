---
title: De service voor Elektronische facturering gebruiken om leveranciersfacturen te importeren
description: Dit onderwerp bevat informatie over het importeren van leveranciersfacturen met de service voor elektronische facturering.
author: gionoder
ms.date: 08/03/2021
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
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751247"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>De service voor Elektronische facturering gebruiken om leveranciersfacturen te importeren

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dit onderwerp bevat informatie waarmee u aan de slag kunt met het importeren van leveranciersfacturen met de service voor elektronische facturering. Dit onderwerp helpt u bij de uitvoering van de configuratiestappen in RCS (Regulatory Configuration Services), Dynamics 365 Finance en Dynamics 365 Supply Chain Management om elektronische leveranciersfacturen van de leveranciers te ontvangen.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Importeren van leveranciersfacturen in RCS instellen
Voer de volgende stappen uit om het importeren van leveranciersfacturen in RCS in te stellen:

1. Raadpleeg de lijst met [over het algemeen beschikbare functies voor elektronische facturering](e-invoicing-configuration-rcs.md#generally-available-features).
2. Selecteer en importeer de functie voor elektronische facturering. Zie [Een functie voor elektronische facturering vanuit de Microsoft-configuratieprovider importeren](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) voor meer informatie.
3. Maak een functie voor elektronische facturering voor uw organisatie. Zie [Een functie voor elektronische facturering onder uw organisatieprovider maken](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider) voor meer informatie.

## <a name="configure-an-email-account-channel"></a>Een e-mailaccountkanaal configureren

Configureer een e-mailaccountkanaal als met de functie voor elektronische facturering die u hebt gemaakt, elektronische leveranciersfacturen worden geïmporteerd uit bijgevoegde bestanden die per e-mail worden ontvangen.

1. Selecteer in RCS de functie voor elektronische facturering die u hebt gemaakt. Selecteer de versie met de status **Concept**.
2. Selecteer op het tabblad **Instellingen** in het raster een functie-instelling en selecteer vervolgens **Bewerken**.
3. Selecteer het **Serveradres** op het tabblad **Gegevenskanaal** in de veldgroep **Parameters** en voer de e-mailaccountprovider in.
4. Selecteer **Serverpoort** en voer de poort in die door de e-mailaccountprovider wordt gebruikt.
5. Selecteer **Geheim gebruikersnaam** en voer de naam in van het Key Vault-geheim dat de ID van de e-mailgebruikersaccount bevat.
6. Selecteer **Geheim gebruikerswachtwoord** en voer de naam in van het Key Vault-geheim dat het wachtwoord van de e-mailgebruikersaccount bevat.
7. Selecteer **Onderwerpfilter**. Controleer en werk de tekenreeks bij die het standaard-e-mailonderwerp bevat ter identificatie van de e-mail die de elektronische leveranciersfactuur bevat die moet worden geïmporteerd.
8. Controleer de criteria en werk deze zo nodig bij op het tabblad **Toepasbaarheidsregels**. Meer informatie over dit onderwerp vindt u in [Toepasbaarheidsregels](e-invoicing-configuration-rcs.md#applicability-rules).
9. Selecteer **Opslaan** en sluit de pagina.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Een Microsoft SharePoint-kanaal configureren

Configureer een Microsoft SharePoint-kanaal als met de functie voor elektronische facturering elektronische leveranciersfacturen worden geïmporteerd uit bestanden die in SharePoint-mappen zijn geplaatst.

1. Selecteer in RCS de functie voor elektronische facturering die u hebt gemaakt. Controleer of u de **Versie** met de status **Concept** hebt geselecteerd.
2. Selecteer op het tabblad **Instellingen** in het raster een functie-instelling en selecteer vervolgens **Bewerken**.
3. Selecteer op het tabblad **Gegevenskanaal** in de veldgroep **Parameters** **SharePoint-adres** en voer de SharePoint-URL in.
4. Selecteer **Serverpoort** en voer de poort in die door de e-mailaccountprovider wordt gebruikt.
5. Selecteer **Toepassings-ID** en voer de naam in van het Key Vault-geheim dat de ID van de SharePoint-client bevat.
6. Selecteer **Geheim toepassing** en voer de naam in van het Key Vault-geheim dat het wachtwoord van de SharePoint-client bevat.
7. Selecteer **Bestandsfilter**. Controleer en werk het masker bij om de bestanden te filteren die de elektronische leveranciersfactuur bevatten die moet worden geïmporteerd.
8. Controleer de criteria en werk deze zo nodig bij op het tabblad **Toepasbaarheidsregels**. Meer informatie over dit onderwerp vindt u in [Toepasbaarheidsregels](e-invoicing-configuration-rcs.md#applicability-rules).
9. Selecteer **Opslaan** en sluit de pagina.

### <a name="deploy-an-electronic-invoicing-feature"></a>Een functie voor elektronische facturering implementeren

Zie [De functie Elektronische facturering in de serviceomgeving implementeren](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) voor de implementatie van de functie voor elektronische facturering.

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Import van leveranciersfacturen in Finance en Supply Chain Management instellen
Voer de stappen in de volgende twee secties uit om verschillende typen import van leveranciersfacturen in te stellen.

### <a name="import-vendor-invoices-from-email"></a>Leveranciersfacturen importeren vanuit e-mail

1. Meld u aan bij uw Finance- of Supply Chain Management-omgeving en controleer of u bij de juiste rechtspersoon bent.
2. Ga naar **Organisatiebeheer** > **Instellen** > **Parameters voor elektronische documenten**.
3. Zorg ervoor dat op het tabblad **Functies** **Federale NF-e - Braziliaanse elektronische factuur** is geselecteerd.
4. Selecteer op het tabblad **Externe kanalen** in de veldgroep **Kanalen** de optie **Toevoegen**.
5. Voer in het veld **Kanaal** **NFe** in (de naam van het kanaal dat is opgegeven in de configuratie van het gegevenskanaal voor de functie voor elektronische facturering in RCS).
6. Voer in het veld **Beschrijving** een beschrijving in. Selecteer de rechtspersoon in het veld **Bedrijf**.
7. Selecteer in het veld **Documentcontext** de optie **Context fiscaal document - contextmodel klantfactuur**.
8. Selecteer **Toevoegen** in de veldgroep **Bronnen importeren**.
9. Voer in het veld **Naam** **XmlFile** in (de naam van het **Bijlagefilter** dat is opgegeven in de configuratie van het gegevenskanaal voor de functie voor elektronische facturering in RCS).
10. Voer in het veld **Omschrijving** een omschrijving in en selecteer in het veld **Naam gegevensentiteit** **Ontvangen NF-e XML-documenten**.
11. Selecteer in het veld **Modeltoewijzing** **NF-e-mailimport – NF-e-mailimport (BR)** en selecteer vervolgens **Opslaan**.
12. Selecteer **Toevoegen** op het tabblad **Elektronisch document** in de veldgroep **Elektronische rapportage** en selecteer **Ontvangen NF-e XML-document** in het veld **Tabelnaam**.
13. Selecteer in het veld **Documentcontext** de optie **Context fiscaal document opvragen - context klantfactuur**.
14. Selecteer in het veld **Toewijzing elektronisch documentmodel** de optie **Toewijzing opvragen – toewijzing fiscaal document**.
15. Selecteer **Responstypen** en selecteer vervolgens **Nieuw**.
16. Voer in het veld **Antwoordtype** de waarde **Antwoord** in. Selecteer in het veld **Indieningsstatus** de optie **Gepland**.
17. Selecteer in het veld **Modeltoewijzing** de optie **Modeltoewijzing van antwoordbericht - importtoewijzing antwoordbericht**.
18. Selecteer **Opslaan** en sluit de pagina.

### <a name="import-peppol-electronic-vendor-invoices"></a>PEPPOL - elektronische leveranciersfacturen importeren

1. Ga naar het werkgebied **Elektronische rapportage** en selecteer **Rapportageconfiguraties**.
2. Selecteer **Contextmodel klantfactuur** en maak een afgeleide configuratie.
3. Selecteer **Ontwerper** in de versie **Concept**.
4. Selecteer **Klantfactuur** in de structuur **Gegevensmodel** en selecteer vervolgens **Model toewijzen aan gegevensbron**.
5. Selecteer in de structuur **Definities** **CustomerInvoice** en selecteer vervolgens **Ontwerper**.
6. Selecteer in de structuur **Gegevensbronnen** **Context\_kanaal**. Selecteer in het veld **Waarde** **PEPPOL**. Dit is de naam van het kanaal dat is opgegeven in de configuratie van het gegevenskanaal voor de functie voor elektronische facturering in RCS. 
7. Selecteer **Opslaan** en sluit de pagina.
8. Sluit de pagina.
9. Selecteer **Contextmodel klantfactuur** en selecteer op het sneltabblad **Versies** **Status wijzigen** > **Voltooid**.
10. Ga naar **Organisatiebeheer** > **Instellen** > **Parameters elektronisch document** en zorg ervoor dat op het tabblad **Functies** **PEPPOL - algemene elektronische facturen** is geselecteerd. 
11. Selecteer op het tabblad **Externe kanalen** in de veldgroep **Kanalen** de optie **Toevoegen**.
12. Voer in het veld **Kanaal** **PEPPOL** in. Voer in het veld **Beschrijving** een beschrijving in.
13. Selecteer de rechtspersoon in het veld **Bedrijf**. Selecteer in het veld **Documentcontext** de optie **Context klantfactuur - contextmodel klantfactuur**.
14. Selecteer **Opslaan** en sluit de pagina.


## <a name="receive-electronic-invoices"></a>Elektronische facturen ontvangen
Voer de volgende stappen uit om elektronische facturen te ontvangen:

1. Ga naar **Organisatiebeheer** > **Periodiek** > **Elektronische documenten** > **Elektronische documenten ontvangen**.
2. Selecteer **OK** en sluit de pagina.

## <a name="view-receive-logs-for-electronic-invoices"></a>Ontvangstlogboeken voor elektronische facturen weergeven

Als u de ontvangstlogboeken voor elektronische facturen wilt weergeven, gaat u naar **Organisatiebeheer** > **Periodiek** > **Elektronische documenten** > **Ontvangstlogboek elektronische documenten**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
