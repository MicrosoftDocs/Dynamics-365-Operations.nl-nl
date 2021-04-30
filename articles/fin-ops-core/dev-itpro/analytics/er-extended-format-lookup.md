---
title: Uitgebreide indelingszoekactie voor elektronische rapportering (ER)
description: In dit onderwerp wordt beschreven hoe een ER-indelingsverwijzing kan worden ingesteld in de ER-indelingszoekactie wanneer de vereiste indeling is opgeslagen in de algemene opslagplaats.
author: NickSelin
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 62bc6587ad80fd318038f5dfc5ff68821b2a65cd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893927"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Gebruikers toestaan om een ER-indelingsverwijzing in te stellen die informatie opvraagt uit de algemene opslagplaats

[!include [banner](../includes/banner.md)]

U kunt het ER-raamwerk ([elektronische rapportage](general-electronic-reporting.md)) gebruiken om [indelingen](general-electronic-reporting.md#FormatComponentOutbound) te configureren voor uitgaande documenten in overeenstemming met de wettelijke voorschriften van verschillende landen/regio's. U kunt ook het ER-raamwerk gebruiken om [indelingen](general-electronic-reporting.md#FormatComponentInbound) te configureren voor het parseren van inkomende documenten en om toepassingsgegevens toe te voegen of bij te werken met de informatie in deze documenten. Elk van deze indelingen kan in uw Dynamics 365 Finance-exemplaar worden gebruikt voor het verwerken van inkomende of uitgaande bedrijfsdocumenten als onderdeel van een bepaald bedrijfsproces.

Gewoonlijk moet u opgeven welke ER-indeling in een bepaald bedrijfsproces moet worden gebruikt. Selecteer hiervoor één ER-indeling in een opzoekveld dat is geconfigureerd als onderdeel van specifieke parameters voor het bedrijfsproces. Deze opzoekvelden worden meestal geïmplementeerd met behulp van de toepasselijke API van het ER-raamwerk. Zie [ER-raamwerk-API: code om een zoekactie voor indelingstoewijzing weer te geven](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Wanneer u bijvoorbeeld [parameters voor de buitenlandse handel](../../../finance/localizations/emea-intrastat.md#set-up-foreign-trade-parameters) configureert, moet u de verwijzingen naar afzonderlijke ER-indelingen instellen die worden gebruikt om de Intrastat-aangifte en het controlerapport Intrastat-aangifte te genereren. In de screenshots hieronder ziet u hoe het opzoekveld voor ER-indelingen eruitziet op de pagina **Parameters buitenlandse handel**.

Dit opzoekveld is leeg als het huidige Finance-exemplaar geen aan het Intrastat-bedrijfsproces gerelateerde ER-indelingen bevat.

[![Pagina Parameters buitenlandse handel](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Dit opzoekveld biedt de ER-indelingen als het huidige Finance-exemplaar aan het Intrastat-bedrijfsproces gerelateerde ER-indelingen bevat.

[![Pagina Parameters buitenlandse handel](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Deze zoekactie biedt alleen de ER-indelingen die al zijn geïmporteerd naar de huidige Finance-instantie. Als u ER-oplossingen wilt [importeren](./tasks/er-import-configuration-lifecycle-services.md) in het huidige Finance-exemplaar, moet u over machtigingen beschikken om de juiste functie van het ER-raamwerk uit te voeren die de [levenscyclus](general-electronic-reporting-manage-configuration-lifecycle.md) ondersteunt van ER-oplossingen die ER-indelingen bevatten.

Vanaf de Finance-versie 10.0.9 (april 2020 release) is de gebruikersinterface van de zoekopdracht voor ER-indelingen die is geïmplementeerd met behulp van de ER-raamwerk-API, uitgebreid. U kunt nog steeds de bestaande ER-indelingen selecteren, die u vindt op het sneltabblad **Indelingsconfiguratie selecteren**. Daarnaast bevat de uitgebreide zoekfunctie de nieuwe optie voor het doorzoeken van de algemene opslagplaats (GR) om specifieke ER-indelingen te zoeken. Op het sneltabblad **Importeren vanuit algemene opslagplaats** worden alle ER-indelingen van de GR aangeboden.

[![Pagina Parameters buitenlandse handel](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Vergelijkbaar met het sneltabblad **Indelingsconfiguratie selecteren** bevat het sneltabblad **Importeren uit algemene opslagplaats** alleen de ER-indelingen die van toepassing zijn op het bedrijfsproces waarvoor een ER-indeling is geselecteerd in dit opzoekveld. In dit voorbeeld wordt de Intrastat-aangifte gegenereerd. De ER-indeling is van toepassing op het bedrijf waarbij de gebruiker momenteel is aangemeld, afhankelijk van de bedrijfslandcontext.

Wanneer u een ER-indeling selecteert op het sneltabblad **Importeren uit algemene opslagplaats**, wordt de geselecteerde ER-indelings[configuratie](general-electronic-reporting.md#Configuration) geïmporteerd van de GR naar de huidige Finance-instantie.

[![Pagina Parameters buitenlandse handel](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Als de import is voltooid, wordt de verwijzing naar de geïmporteerde ER-indeling in dit opzoekveld opgeslagen. Wanneer u de GR voor de eerste keer opent, moet u de geboden koppeling volgen om u aan te melden voor de [Regulatory Configuration Service](https://aka.ms/rcs) (RCS) die wordt gebruikt om de toegang tot de GR-opslag te beheren.

[![Pagina Parameters buitenlandse handel](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Standaard bevat het sneltabblad **Importeren uit algemene opslagplaats** de lijst met ER-indelingen van de tijdelijke opslag die automatisch wordt gemaakt op basis van de GR-inhoud, voor betere prestaties. Dit is het geval wanneer het sneltabblad **Importeren uit algemene opslagplaats** de eerste keer wordt geopend. Dit kan enkele seconden duren.

Als de vereiste ER-indeling niet wordt weergeven in het sneltabblad **Importeren uit algemene opslagplaats**, maar u er zeker van bent dat deze ER-indeling is opgeslagen in de GR, selecteert u de optie **Synchroniseren**. Met deze optie wordt de tijdelijke opslag bijgewerkt en gesynchroniseerd met de huidige inhoud van de GR.

## <a name="feature-activation"></a>Functieactivering

De beschikbaarheid van deze functionaliteit wordt bepaald door de functie **Uitgebreide opzoekactie van ER-indelingsconfiguraties om te zoeken in de algemene opslagplaats** in het **Functiebeheer**. Deze functie is standaard ingeschakeld.

[![Pagina Functiebeheer](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Beveiligingsoverwegingen

Met de bevoegdheid **Configuratieopslagplaatsen onderhouden** (**ERMaintainSolutionRepositories**) wordt de toegang tot de GR beheerd voor een gebruiker die de opzoekfunctie voor ER-indelingen opent met het ingeschakelde sneltabblad **Importeren uit algemene opslagplaats**. Als u wilt dat gebruikers toegang tot de GR-inhoud kunnen krijgen vanuit de ER-indelingszoekopdrachten, moet u de beveiligingsinstellingen wijzigen door de bevoegdheid **ERMaintainSolutionRepositories** te verlenen aan gebruikers, hetzij rechtstreeks of door al toegewezen rollen en taken te gebruiken.

Het volgende screenshot geeft aan hoe deze bevoegdheid kan worden verleend aan gebruikers die zijn toegewezen aan de rol **Accountant**. Deze rol stelt gebruikers in staat om parameters voor buitenlandse handel te configureren en verwijzingen in te stellen naar de ER-indelingen in de velden **Toewijzing van bestandsindeling** en **Toewijzing van rapportindeling** op de pagina **Parameters buitenlandse handel**.

[![Pagina Beveiligingsconfiguratie](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Beperkingen

De toegang tot de GR in de ER-indelingszoekopdracht wordt momenteel alleen ondersteund voor de selectie van ER-indelingen die worden gebruikt om uitgaande documenten te genereren.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Waarom kan ik de algemene opslagplaats niet openen vanuit de opzoekfunctie voor ER-indelingen?

Als u de functie **Uitgebreide opzoekactie van ER-indelingsconfiguraties om te zoeken in de algemene opslagplaats** hebt ingeschakeld op de pagina **Functiebeheer**, maar gebruikers geen ER-indelingen kunnen zien op het sneltabblad **Importeren uit algemene opslagplaats** en de optie **Synchronisatie** zichtbaar is maar is uitgeschakeld, moet u ervoor zorgen dat de bevoegdheid **Configuratieopslagplaatsen onderhouden** (**ERMaintainSolutionRepositories**) is verleend voor de gebruiker. Om deze bevoegdheid te krijgen neemt u contact op met uw systeembeheerder.

## <a name="additional-resources"></a>Aanvullende resources

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Raamwerk voor ER API (elektronische rapportage)](er-apis-app73.md)
- [De levenscyclus van ER-configuraties (elektronische rapportage) beheren](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]