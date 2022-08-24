---
title: De service voor elektronische facturering gebruiken om leveranciersfacturen te importeren
description: Dit artikel bevat informatie over het importeren van leveranciersfacturen met de service voor elektronische facturering.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: c98f33345b37a72c4099f01e37c82e27002ac687
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283140"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>De service voor elektronische facturering gebruiken om leveranciersfacturen te importeren

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Dit artikel bevat informatie waarmee u aan de slag kunt met het importeren van leveranciersfacturen met de service voor elektronische facturering. Dit artikel helpt u bij de uitvoering van de configuratiestappen in RCS (Regulatory Configuration Services), Dynamics 365 Finance en Dynamics 365 Supply Chain Management om elektronische leveranciersfacturen van de leveranciers te ontvangen.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Importeren van leveranciersfacturen in RCS instellen
Voer de volgende stappen uit om het importeren van leveranciersfacturen in RCS in te stellen:

1. Raadpleeg de lijst met [over het algemeen beschikbare functies voor elektronische facturering](e-invoicing-configuration-rcs.md#generally-available-features).
2. Selecteer en importeer de functie voor elektronische facturering. Zie [Een functie voor elektronische facturering vanuit de Microsoft-configuratieprovider importeren](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) voor meer informatie.
3. Maak een functie voor elektronische facturering voor uw organisatie. Zie [Een functie voor elektronische facturering onder uw organisatieprovider maken](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider) voor meer informatie.

## <a name="configure-an-email-account-channel"></a>Een e-mailaccountkanaal configureren

Configureer een e-mailaccountkanaal als met de functie voor elektronische facturering die u hebt gemaakt, elektronische leveranciersfacturen worden geïmporteerd uit bijgevoegde bestanden die per e-mail worden ontvangen.

1. Selecteer in RCS de functie voor elektronische facturering die u hebt gemaakt. Selecteer de versie met de status **Concept**.
2. Selecteer op het tabblad **Instellingen** in het raster een functie-instelling en selecteer vervolgens **Bewerken**.
3. Voer op het tabblad **Gegevenskanaal** in de veldgroep **Parameters** in het veld **Gegevenskanaal** de naam van het kanaal in. De kanaalnaam mag niet langer zijn dan tien tekens.
4. Voer in het veld **Serveradres** de provider van het e-mailaccount in. Het serveradres voor **https://outlook.live.com/** is bijvoorbeeld **imap-mail.outlook.com**.
5. Voer in het veld **Serverpoort** de poort in die door de provider van het e-mailaccount wordt gebruikt. De serverpoort voor **https://outlook.live.com/** is bijvoorbeeld **993**.
6. Voer in het veld **Geheim gebruikersnaam** de naam in van het KeyVault-geheim dat de ID van de e-mail van het gebruikersaccount bevat. Dit geheim moet worden aangemaakt in de Azure Key Vault en worden ingesteld in uw serviceomgeving. 
7. Voer in het veld **Geheim gebruikerswachtwoord** de naam in van het KeyVault-geheim dat het wachtwoord van de e-mail van het gebruikersaccount bevat.
8. Optioneel - voer waarden in de velden **Afzenderfilter**, **Onderwerpfilter** en **Datumfilter** in.
9. Voer de namen in van de postvakmappen waarin e-mails worden weergegeven:

    - Geïmporteerd uit: **Hoofdmap**
    - Opgeslagen na een geslaagde verwerking: **Archiefmap**
    - Opgeslagen nadat de verwerking niet is gelukt: **Foutmap** U hoeft deze mappen niet in het postvak aan te maken. De mappen worden automatisch aangemaakt na het importeren en de verwerking van de eerste e-factuur. 
   
10. Voeg in de veldgroep **Bijlagenfilter** de informatie voor het filteren van bestanden in. Alleen bijlagen die voldoen aan het gedefinieerde filter worden verwerkt. U kunt bijvoorbeeld '\*.xml' instellen voor bijlagen met een xml-extensie. De naam van de bijlage wordt in Dynamics 365 Finance of Dynamics 365 Supply Chain Management gebruikt tijdens het instellen. 
11. Controleer de criteria en werk deze zo nodig bij op het tabblad **Toepasbaarheidsregels**. Het veld **Kanaal** moet gelijk zijn aan het eerder opgegeven **Gegevenskanaal**. Meer informatie over dit onderwerp vindt u in [Toepasbaarheidsregels](e-invoicing-configuration-rcs.md#applicability-rules).
12. Selecteer **Opslaan** en sluit de pagina.

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

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Import van leveranciersfacturen instellen in Finance of Supply Chain Management
Voer de stappen in de volgende twee secties uit om verschillende typen import van leveranciersfacturen in te stellen.

### <a name="import-brazilian-nf-e-from-email"></a>NF-e importeren uit e-mail (BR) (Brazilië)

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
2. Selecteer **Contextmodel klantfactuur** en selecteer vervolgens **Configuratie aanmaken** > **Afleiden van naam: Contextmodel klantfactuurcontextmodel, Microsoft** om een afgeleide configuratie aan te maken.
3. Selecteer in de **Concept**-versie **Ontwerper** en selecteer in de structuur **Gegevensmodel** **Model toewijzen aan gegevensbron**.
4. Selecteer in de structuur **Definities** **Gegevenskanaal** en selecteer vervolgens **Ontwerper**.
5. Vouw in de structuur **Gegevensbronnen** de container **$Context\_kanaal** uit. Selecteer in het veld **Waarde** **Bewerken** en voer de naam van het gegevenskanaal in. Dit is de naam van het kanaal dat is opgegeven in de configuratie van het gegevenskanaal voor de functie voor elektronische facturering in RCS. 
7. Selecteer **Opslaan** en sluit de pagina.
8. Sluit de pagina.
9. Selecteer de afgeleide configuratie die u zojuist hebt aangemaakt op basis van het **Contextmodel klantfacturen** en selecteer op het sneltabblad **Versies** de optie **Status wijzigen** > **Voltooid**.
10. Ga naar **Organisatiebeheer** > **Instellen** > **Parameters elektronisch document** en zorg ervoor dat op het tabblad **Functies** **PEPPOL - algemene elektronische facturen** is geselecteerd. 
11. Selecteer op het tabblad **Externe kanalen** in de veldgroep **Kanalen** de optie **Toevoegen**.
12. Voer in het veld **Kanaal** de naam van het gegevenskanaal in en in het veld **Omschrijving** een omschrijving.
13. Selecteer de rechtspersoon in het veld **Bedrijf**. 
14. Selecteer in het veld **Documentcontext** de nieuwe afgeleide configuratie van het **Contextmodel klantfactuur**. De toewijzingsbeschrijving moet **Context gegevenskanaal** zijn.
15. Selecteer **Toevoegen** in de veldgroep **Bronnen importeren**.
16. Voer in het veld **Naam** de **Filternaam bijlagen** in en selecteer in het veld **Naam gegevensentiteit** de **Koptekst leveranciersfactuur**.
17. Selecteer in het veld **Modeltoewijzing** **Leveranciersfactuur imprt - Leveranciersfactuur importeren**.
18. Klik op **Opslaan** en sluit vervolgens de pagina.


## <a name="receive-electronic-invoices"></a>Elektronische facturen ontvangen

De elektronische factureringsservice voert twee stappen uit tijdens het importeren van facturen vanuit de gegevenskanalen:

1. Geeft toegang tot het postvak en e-mail lezen.
2. Verwerkt de e-mails. 
    
Als u deze twee stappen wilt uitvoeren, moet de client de service voor elke stap handmatig aanroepen. Het is echter raadzaam een batch in te stellen voor de ontvangst van elektronische documenten.

Voer de volgende stappen uit om elektronische facturen te ontvangen:

1. Ga naar **Organisatiebeheer** > **Periodiek** > **Elektronische documenten** > **Elektronische documenten ontvangen**.
2. Selecteer **OK** en sluit de pagina.


## <a name="view-receive-logs-for-electronic-invoices"></a>Ontvangstlogboeken voor elektronische facturen weergeven

Als u de ontvangstlogboeken voor elektronische facturen wilt weergeven, gaat u naar **Organisatiebeheer** > **Periodiek** > **Elektronische documenten** > **Ontvangstlogboek elektronische documenten**.
Als u geen facturen verwerkt ziet worden, verwijdert u het tabelfilter.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
