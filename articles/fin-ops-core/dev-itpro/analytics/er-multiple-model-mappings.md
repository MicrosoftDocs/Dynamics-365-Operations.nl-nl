---
title: Verschillende afgeleide toewijzingen voor één modelbasis beheren
description: In dit onderwerp wordt uitgelegd hoe u verschillende afgeleide toewijzingen beheert die voor één modelbasis zijn geconfigureerd.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d71b05b3f2eda93a93f728926e675c040371781e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324107"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Verschillende afgeleide toewijzingen voor één modelbasis beheren

[!include [banner](../includes/banner.md)]

Een component [ER-gegevensmodel](general-electronic-reporting.md) wordt gebruikt in elke geconfigureerde ER-indelingscomponent indeling als gegevensbron voor het genereren van uitgaande documenten. Als u één bedrijfsdomein wilt beschrijven, configureert u een gegevensmodelcomponent die veel basisdefinities heeft. 

Met elke basisdefinitie kunt u gegevens van dat domein vertegenwoordigen op de manier die het meest geschikt is voor specifieke rapportagedoeleinden. Voor elke basisdefinitie kunt u een component ER-modeltoewijzing configureren als de Microsoft Dynamics 365 Finance-specifieke implementatie van uw gegevensmodel. Op deze manier beschrijft u hoe uw gegevensmodel wordt ingevuld tijdens runtime.

ER-modeltoewijzingscomponenten kunnen zich in ER-gegevensmodel[configuraties](general-electronic-reporting.md#Configuration) en ER-modeltoewijzingsconfiguraties bevinden. Een enkele ER-configuratie kan een groot aantal toewijzingscomponenten bevatten, die elk voor één basisdefinitie zijn geconfigureerd. Ook kan een enkele ER-configuratie slechts één toewijzingscomponent bevatten, die voor één basisdefinitie is geconfigureerd.

Veel configuratieproviders kunnen ER-modeltoewijzingsconfiguraties voor hetzelfde ER-gegevensmodel bieden. Deze modeltoewijzingsconfiguraties kunnen toewijzingscomponenten voor verschillende basisdefinities bevatten. U kunt een modeltoewijzing gebruiken voor één basisdefinitie die wordt geboden door één [provider](general-electronic-reporting.md#Provider) en een modeltoewijzing voor een andere basisdefinitie gebruiken die wordt geboden door een andere provider.

De procedures in dit onderwerp leggen uit hoe u meerdere ER-modeltoewijzingsconfiguraties van een ER-gegevensmodel beheert wanneer ze verschillende modeltoewijzingscomponenten bevatten die voor dezelfde basisdefinitie zijn geconfigureerd. 

Voor de procedures in dit onderwerp moet u de rol Systeembeheerder of Ontwikkelaar elektronische rapportage hebben.

U kunt alle volgende procedures uitvoeren in het bedrijf USMF. U hoeft hiervoor geen code te schrijven.

## <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Als u een gebruiker bent in de rol Ontwikkelaar elektronische rapportage, [configureert u de minimale set](er-quick-start2-customize-report.md#ConfigureFramework) ER-parameters voordat u het ER framework gebruikt om bedrijfsdocumenten te genereren.

## <a name="import-the-standard-er-format-configurations"></a>De standaardconfiguraties voor ER-indeling importeren

Als u de ER-standaardconfiguraties wilt toevoegen aan uw huidige Finance-exemplaar, moet u deze importeren vanuit de ER-opslagplaats die voor dat exemplaar is geconfigureerd. Volg de stappen in [ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](er-download-configurations-global-repo.md) om de volgende ER-indelingsconfiguraties te importeren:

- **Vrije-tekstfactuur (Excel)**, versie 220.106
- **Projectfactuur (Excel)**, versie 226.27

## <a name="review-the-imported-er-configurations"></a>De geïmporteerde ER-configuraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit.

    ![Geïmporteerde configuraties op de pagina Configuraties controleren.](./media/er-multiple-model-mappings-image1.png)

4. Bekijk de indeling **Vrije-tekstfactuur (Excel)**:

    1. Selecteer in de configuratiestructuur in het linkerdeelvenster **Vrije-tekstfactuur (Excel)**.
    2. Selecteer **Ontwerper** in het actievenster.
    3. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** in de gegevensbronnenlijst **Model**.
    4. Selecteer **Weergeven**.
    
       De huidige ER-indeling wordt geconfigureerd voor het gebruik van de basisdefinitie **InvoiceCustomer** van **Factuurmodel**. Wanneer deze indeling wordt uitgevoerd en de gegevensbron **Model** wordt aangeroepen, wordt de modeltoewijzing die is geconfigureerd voor de basisdefinitie **InvoiceCustomer** gebruikt om toegang te krijgen tot toepassingsgegevens en het gegevensmodel in te vullen.

        ![De modelgegevensbron op de pagina Indelingsontwerper controleren.](./media/er-multiple-model-mappings-image2.png)

    6. Sluit de pagina **Indelingsontwerper**.

5. Bekijk de inhoud van de configuratie **Factuurmodeltoewijzing**:

    1. Selecteer in de configuratiestructuur in het linkerdeelvenster **Factuurmodeltoewijzing**.
    2. Selecteer **Ontwerper** in het actievenster.
    3. Op de pagina **Model voor gegevensbrontoewijzing** ziet u dat de huidige ER-modeltoewijzingsconfiguratie verschillende modeltoewijzingscomponenten bevat:

        + De modeltoewijzing **Klantfactuur** wordt geconfigureerd voor de basisdefinitie **InvoiceCustomer** van **Factuurmodel**. Daarom kan bij het uitvoeren van de ER-indeling **Vrije-tekstfactuur (Excel)** de modeltoewijzing **Klantfactuur** van deze ER-configuratie worden gekozen om toegang te krijgen tot toepassingsgegevens en het gegevensmodel in te vullen.
        + De modeltoewijzing **Projectfactuur** wordt geconfigureerd voor de basisdefinitie **InvoiceProject** van **Factuurmodel**. Daarom kan bij het uitvoeren van de ER-indeling **Projectfactuur (Excel)** de modeltoewijzing **Projectfactuur** van deze ER-configuratie worden gekozen om toegang te krijgen tot toepassingsgegevens en het gegevensmodel in te vullen.

        ![Factuurmodeltoewijzing op de pagina Model voor gegevensbrontoewijzing.](./media/er-multiple-model-mappings-image3.png)

    4. Sluit de pagina **Model aan gegevensbrontoewijzing**.
    5. Selecteer op het sneltabblad **Versies** de optie **Verwijderen** om alle versies van deze ER-configuratie die later zijn dan versie 240.175 te verwijderen.

6. Bekijk de inhoud van de configuratie **Projectmodeltoewijzing (RDP)**:

    1. Selecteer in de configuratiestructuur in het linkerdeelvenster **Projectfactuurmodeltoewijzing (RDP)**.
    2. Selecteer **Ontwerper** in het actievenster.
    3. U ziet op de pagina **Model voor gegevensbrontoewijzing** dat de huidige configuratie van ER-modeltoewijzing de **InvoiceProject**-modeltoewijzing bevat en dat deze modeltoewijzing is geconfigureerd voor de basisdefinitie **InvoiceProject** van **Factuurmodel**. Wanneer de ER-indeling **Projectfactuur (Excel)** wordt uitgevoerd, selecteert u de modeltoewijzing **InvoiceProject** van deze ER-configuratie om toegang te krijgen tot toepassingsgegevens en het gegevensmodel in te vullen.

        ![Projectfactuurmodeltoewijzing op de pagina Model voor gegevensbrontoewijzing.](./media/er-multiple-model-mappings-image4.png)

    4. Sluit de pagina **Model aan gegevensbrontoewijzing**.
    5. Selecteer op het sneltabblad **Versies** de optie **Verwijderen** om alle versies van deze ER-configuratie die later zijn dan versie 226.35 te verwijderen.

## <a name="customize-the-imported-er-configurations"></a>De geïmporteerde ER-configuraties aanpassen

In deze sectie wordt uitgelegd hoe u de modeltoewijzingen [aanpast](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) die door Microsoft worden geleverd. Aanpassingen kunnen bijvoorbeeld nodig zijn om uw aangepaste logica te implementeren of ontbrekende bindingen toe te voegen.

### <a name="customize-the-invoice-model-mapping-configuration"></a>De factuurmodeltoewijzingsconfiguratie aanpassen

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodeltoewijzing**.
2. Selecteer **Configuratie maken** in het actievenster.
3. Selecteer in het vervolgvenster **Configuratie maken** in het veld **Nieuw** **Afleiden van naam: Toewijzing factuurmodel, Microsoft**.
4. Voer in het veld **Naam** **Toewijzing factuurmodel Litware** in.
5. Selecteer **Configuratie maken**.
6. [Markeer](er-quick-start2-customize-report.md#MarkFormatRunnable) de [concept](general-electronic-reporting.md#component-versioning)versie van de afgeleide toewijzing als beschikbaar voor gebruik tijdens runtime:

    1. Selecteer in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
    2. Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.
    3. Selecteer zo nodig **Bewerken** om de pagina bewerkbaar te maken.
    4. Stel voor de configuratie **Toewijzing factuurmodel Litware** die momenteel is geselecteerd in de configuratiestructuur de optie **Concept uitvoeren** in op **Ja**.

7. Selecteer In het actievenster **Ontwerper** om de modeltoewijzingen van deze configuratie te controleren.

    ![De factuurmodeltoewijzing op de pagina Model voor gegevensbrontoewijzing controleren.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > U kunt nu elk van de ER-modeltoewijzingscomponenten van deze ER-configuratie in de ontwerper openen om uw aangepaste logica te configureren. Zie [De modeltoewijzingsconfiguratie aanpassen](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) voor meer informatie.

8. Sluit de pagina **Model aan gegevensbrontoewijzing**.

U hebt nu configuraties **Factuurmodeltoewijzing** en **Factuurmodeltoewijzing Litware**, elk met een modeltoewijzing die is geconfigureerd voor de basisdefinitie **InvoiceCustomer**. Wijs expliciet een van de modeltoewijzingen toe als de standaardmodeltoewijzing die wordt gebruikt door de ER-indelingen, zoals de indeling **Vrije-tekstfactuur (Excel)** die een modelgegevensbron bevat met de basisdefinitie **InvoiceCustomer**. Anders ontstaat bij het uitvoeren, bewerken of valideren van een van de ER-indelingen de volgende uitzondering om u op de hoogte te stellen dat geen standaardmodeltoewijzing expliciet is toegewezen:
 
> Er bestaan meerdere modeltoewijzingen voor het gegevensmodel \<model name\> (\<root descriptor\>) in de configuraties \<configuration names separated by commas\>. Stel een van de configuraties als standaard in.

![De indeling voor bewerkingen op de pagina Configuraties openen.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>De projectfactuurmodeltoewijzingsconfiguratie (RDP) aanpassen

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Projectfactuurmodeltoewijzing (RDP)**.
2. Selecteer **Configuratie maken** in het actievenster.
3. Selecteer in het dialoogvenster **Configuratie maken** in het veld **Nieuw** **Afleiden van naam: Toewijzing projectfactuurmodel (RDP), Microsoft**.
4. Voer in het veld **Naam** **Toewijzing projectfactuurmodel Litware** in.
5. Selecteer **Configuratie maken**.
6. Stel voor de configuratie **Toewijzing projectfactuurmodel Litware** die momenteel is geselecteerd in de configuratiestructuur de optie **Concept uitvoeren** in op **Ja**.
7. Selecteer In het actievenster **Ontwerper** om de modeltoewijzingen van deze configuratie te controleren.

    ![De aangepaste projectfactuurmodeltoewijzingen op de pagina Model voor gegevensbrontoewijzing controleren.](./media/er-multiple-model-mappings-image7.png)

8. Sluit de pagina **Model aan gegevensbrontoewijzing**.

U hebt nu configuraties **Factuurmodeltoewijzing**, **Projectfactuurmodeltoewijzing (RDP)** en **Toewijzing projectfactuurmodel Litware**. Elk van deze configuraties heeft een modeltoewijzing geconfigureerd voor de basisdefinitie **InvoiceProject**. Wijs één van de modeltoewijzingen expliciet toe als de standaardmodeltoewijzing die door de ER-indelingen wordt gebruikt. Gebruik bijvoorbeeld de indeling **Projectfactuur (Excel)** die een modelgegevensbron bevat met de basisdefinitie **InvoiceProject**. Anders ontstaat bij het uitvoeren of bewerken van een van de ER-indelingen een uitzondering om u op de hoogte te stellen dat geen standaardmodeltoewijzing expliciet is toegewezen:

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>De afgeleide configuratie Factuurmodeltoewijzing Litware selecteren als de configuratie met standaardmodeltoewijzingen

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodeltoewijzing Litware**.
2. Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.

    ![De modeltoewijzing instellen als de standaardmodeltoewijzing op de pagina Configuraties.](./media/er-multiple-model-mappings-image8.png)

    Door deze instelling wordt de modeltoewijzing **Klantfactuurkopie** gebruikt wanneer u de **Vrije-tekstfactuur (Excel)** uitvoert of wanneer u deze bewerkt of valideert. De modeltoewijzing **Klantfactuur** van de configuratie **Factuurmodeltoewijzing** wordt genegeerd.

    U kunt nu de indeling **Vrije-tekstfactuur (Excel)** voor controle openen in de indelingsontwerper.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>De afgeleide configuratie Projectfactuurmodeltoewijzing Litware selecteren als de configuratie met standaardmodeltoewijzingen

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Projectfactuurmodeltoewijzing Litware**.
2. Stel de optie **Standaard voor modeltoewijzing** in op **Ja**.

    In dit geval kunt u, in tegenstelling tot het geval dat is beschreven voor de configuratie **Factuurmodeltoewijzing Litware** in de vorige sectie, de modeltoewijzing **InvoiceProject-kopie** niet gaan gebruiken vanuit de configuratie **Projectfactuurmodeltoewijzing Litware**. Twee configuraties die een modeltoewijzing voor de basisdefinitie **InvoiceProject** gebruiken, worden momenteel als de standaardconfiguratie gemarkeerd. Daarom hebben ze dezelfde prioriteit voor gebruik. Om dit probleem op te lossen, voltooit u de resterende stappen van deze procedure.

3. Selecteer in de configuratiestructuur in het linkerdeelvenster **Factuurmodeltoewijzing Litware**.
4. Selecteer **Ontwerper** in het actievenster.
5. Selecteer op de pagina **Model naar gegevensbrontoewijzing** de optie **Bewerken** om de pagina bewerkbaar te maken.
6. Selecteer de modeltoewijzing **Projectfactuurkopie** en schakel vervolgens het selectievakje **Is verwijderd** in.

    ![De modeltoewijzing instellen als virtueel verwijderd op de pagina Model voor gegevensbrontoewijzing.](./media/er-multiple-model-mappings-image9.png)

    Door deze instelling wordt de configuratie **Factuurmodeltoewijzing Litware** behandeld alsof deze geen modeltoewijzing heeft voor de basisdefinitie **InvoiceProject**. De modeltoewijzing **InvoiceProject-kopie** die standaard is uitgegeven. De configuratie, **Toewijzing projectfactuurmodel Litware**, die deze modeltoewijzing bevat, wordt gemarkeerd als de standaardconfiguratie. Omdat deze als standaard is gemarkeerd, heeft deze een hogere prioriteit dan de modeltoewijzing **InvoiceProject** van de cconfiguratie **Projectfactuurmodeltoewijzing (RDP)**.

## <a name="other-considerations"></a>Andere overwegingen

De modeltoewijzing **InvoiceProject-kopie** van de configuratie **Toewijzing projectfactuurmodel Litware** is ontworpen voor gebruik met de gegevensbron **ReportDataProvider**. De gegevensbron maakt deel uit van het type *Object* dat verwijst naar de toepassingsklasse **PsaProjInvoiceDP**. Deze klasse wordt geïmplementeerd als de gegevensprovider voor het SQL Server Reporting Services-rapport (projectfactuur) van het afdrukbeheerraamwerk. Selecteer deze gegevensbron als het [ER-integratiepunt](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents). Bij de huidige ER-implementatie voor afdrukbeheerrapporten wordt rekening gehouden met deze instelling. Controleer de broncode van de toepassingsklasse **ERPrintMgmtDataProviderReport** voor meer informatie. Tijdens runtime dwingt de toewijzing van de gegevensbron **ReportDataProvider** als het modeltoewijzingsintegratiepunt Finance deze toewijzingscomponent met een hogere prioriteit te behandelen dan de **InvoiceProject**-toewijzingscomponent van de configuratie **Projectfactuurmodeltoewijzing (RDP)**.

## <a name="see-also"></a>Zie ook

- [ER-modeltoewijzing in afzonderlijke ER-configuraties beheren](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [ER-modeltoewijzingen configureren afhankelijk van landencontext](er-country-dependent-model-mapping.md)
- [Wijzigingen API raamwerk voor elektronische rapportage](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
