---
title: Grote documenten comprimeren die worden gegenereerd in elektronische rapportage
description: In dit onderwerp wordt uitgelegd hoe u grote documenten kunt comprimeren die worden gegenereerd door een ER-indeling (elektronische rapportage).
author: NickSelin
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 899af54fbe34841c9b9b6e96b78db96773cf0203
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894167"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Grote documenten comprimeren die worden gegenereerd in elektronische rapportage 

[!include [banner](../includes/banner.md)]

U kunt het [Raamwerk elektronische rapportage (ER)](general-electronic-reporting.md) gebruiken om een oplossing te configureren waarmee transactiegegevens worden opgehaald om een uitgaand document te genereren. Dit gegenereerde document kan vrij groot zijn. Als dit type document wordt gegenereerd, wordt het geheugen van de [Application Object Server (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) gebruikt om het document op te slaan. Op een bepaald moment moet het document worden gedownload vanuit uw Microsoft Dynamics 365 Finance-toepassing. Momenteel is de maximale grootte van één document dat wordt gegenereerd in ER, beperkt tot 2 gigabytes (GB). Bovendien is de grootte van een gedownload bestand in Finance momenteel [beperkt](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) tot 1 GB. Daarom moet u een ER-oplossing configureren waarmee de kans wordt verkleind dat deze beperkingen worden overschreden en dat u de uitzondering **De stroom is te lang** of **Overloop of negatieve overloop in de rekenkundige bewerking** ontvangt.

Als u een oplossing configureert, kunt u uw ER-indeling in de Operations-ontwerper aanpassen door een hoofdelement van het type **Map** toe te voegen om de inhoud te comprimeren die door een van de bijbehorende geneste elementen wordt gegenereerd. Compressie werkt 'just in time', zodat het piekgeheugengebruik en de grootte van het bestand dat wordt gedownload, kunnen worden gereduceerd.

> [!NOTE]
> Bestandscompressie neemt een extra percentage van CPU-gebruik in beslag.

Voer het voorbeeld in dit onderwerp uit voor meer informatie over deze methode.

## <a name="example-compress-an-outbound-document"></a>Voorbeeld: een uitgaand document comprimeren

In dit voorbeeld wordt aangegeven hoe een gebruiker die is toegewezen aan de rol **Systeembeheerder** of **Functioneel consultant elektronische rapportage** een ER-indeling kan configureren om een gegenereerd document te comprimeren.

### <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp uitvoert, moet u de volgende stappen uitvoeren.

1. [Een configuratieprovider activeren](er-defer-xml-element.md#activate-a-configuration-provider).
2. [De ER-voorbeeldconfiguraties importeren](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [De geïmporteerde indeling controleren](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Op dit moment begint de indelingsstructuur vanaf het element **Rapport** van het type **Bestand** en bevat XML-elementen. Daarom wordt een uitgaand document in XML-indeling gegenereerd en wordt er geen compressie gebruikt.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>Een ER-indeling genereren om een niet-gecomprimeerd document te verkrijgen

1. [De geïmporteerde indeling uitvoeren](er-defer-xml-element.md#run-the-imported-format).
2. U ziet dat de grootte van het gegenereerde document in XML-indeling 3 kilobytes (KB) is.

    ![Voorbeeld van het niet-gecomprimeerde uitgaande document](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>De indeling wijzigen om de gegenereerde uitvoer te comprimeren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur **Model voor het leren van uitgestelde elementen uit**.
3. Selecteer de configuratie **Indeling om uitgestelde XML-elementen te leren**.
4. Selecteer **Ontwerper** om de indelingsstructuur te wijzigen.
5. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Indeling** **Basis toevoegen** om een hoofdindelingselement toe te voegen.
6. Selecteer in het dialoogvenster **Toevoegen** **Common\\Folder**.
7. Selecteer **OK** om de toevoeging van het nieuwe hoofdelement te bevestigen.
8. Selecteer **Opslaan**.

> [!NOTE]
> De indelingsstructuur begint vanaf het element van het type **Map**. Met dit element wordt uitvoer gegenereerd als een gecomprimeerd bestand (zip). Wanneer een document dat wordt gegenereerd door het element **Rapport** in een uitgaand zip-bestand wordt geplaatst, wordt de inhoud ervan gecomprimeerd om de grootte van het uitgaande bestand te verkleinen.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>Een ER-indeling genereren om een gecomprimeerd document te verkrijgen

1. Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.
2. Download het zip-bestand dat de webbrowser biedt en open het bestand ter controle.
3. U ziet dat de grootte van het gegenereerde document in ZIP-indeling 1 KB is.

    > [!NOTE] 
    > De compressiefactor van het XML-bestand dat dit zip-bestand bevat, is 87 procent. De compressiefactor is afhankelijk van de gegevens die worden gecomprimeerd.

    ![Voorbeeld van het gecomprimeerde uitgaande document](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Als de [ER-bestemming](electronic-reporting-destinations.md) is geconfigureerd voor het indelingselement waarmee uitvoer wordt gegenereerd (het element **Rapport** in dit voorbeeld), wordt de compressie van de uitvoer overgeslagen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)

[De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]