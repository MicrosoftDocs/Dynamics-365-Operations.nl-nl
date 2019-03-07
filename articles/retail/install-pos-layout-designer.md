---
title: De indelingsontwerper voor Retail-verkooppunten (POS) installeren
description: U kunt de één-klik-ontwerper gebruiken om verschillende Retail Modern POS- (MPOS) en POS Cloud-indelingen, in de modus Liggend of Staand, te ontwerpen voor winkels, kassa's, kassiers en managers.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7fc5b48b71816b662f016f4a2d909526da0595f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "327637"
---
# <a name="install-the-retail-point-of-sale-pos-layout-designer"></a>De indelingsontwerper voor Retail-verkooppunten (POS) installeren

[!include [banner](includes/banner.md)]

U kunt de één-klik-ontwerper gebruiken om verschillende Retail Modern POS- (MPOS) en POS Cloud-indelingen, in de modus Liggend of Staand, te ontwerpen voor winkels, kassa's, kassiers en managers.

De interface voor grafische ontwerpen voor MPOS of Cloud POS wordt bepaald door de kassa-indeling. De positie van diverse objecten wordt bepaald door de indeling. Denk bijvoorbeeld aan de totale indeling, de artikelrasterindeling, de klantindeling, de betalingsindeling en de indeling van diverse menuknoppen. Indelingen omvatten ook het algehele uiterlijk van de verkoopinterface die aan de medewerkers wordt gepresenteerd.

## <a name="install-the-one-click-designer"></a>De één-klik-ontwerper installeren

1. Gebruik in Microsoft Dynamics 365 for Retail het menu in de linkerbovenhoek om naar **Detailhandel** **en commerce** &gt; **Afzetkanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Schermindelingen** te gaan.
2. Selecteer een indeling met als toepassingstype **Moderne POS voor Windows** of **Cloud POS** en klik op **Ontwerper van indeling**.
3. Op de meldingsbalk die onder in het Internet Explorer-venster verschijnt, klikt u op **Openen** om de één-klik-ontwerper te installeren. (De meldingsbalk kan op een andere locatie worden weergegeven in andere browsers.)
4. Klik in het berichtvak **Toepassing uitvoeren - beveiligingswaarschuwing** op **Uitvoeren** om de detailhandelsontwerperhost te installeren. Een voortgangsindicator geeft de voortgang van de installatie aan.
5. Nadat de installatie is voltooid, voert u op de pagina **Aanmelden** uw Microsoft Dynamics 365 for Retail-gebruikersnaam en -wachtwoord in en klikt u op **Aanmelden** om de ontwerper te starten.
6. Nadat uw referenties zijn gevalideerd en de ontwerper is gestart, kunt u beginnen met uw eigen ontwerpen of een bestaande indeling wijzigen.

    [![Indeling in de één-klik-ontwerper](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Problemen met de installatie van de indelingsontwerper oplossen

- Wanneer u op **Ontwerper** klikt, wordt de vraag om het installatieprogramma te downloaden (of uit te voeren) niet weergegeven of uw huidige beveiligingsinstellingen verhinderen dat u het bestand downloadt. 

    **Oplossingen:**

    - Controleer in Internet Explorer of de pop-upblokkering voor deze site is uitgeschakeld. Klik op **Instellingen** &gt; **Opties** &gt; **Privacy** &gt; **Pop-upblokkering zoeken** en wijzig de instelling als dit nodig blijkt.
    - Voeg in Internet Explorer de URL voor Dynamics 365 for Retail aan uw vertrouwde websites toe. Klik op **Instelling** &gt; **Opties** &gt; **Beveiliging** &gt; **Vertrouwde sites** &gt; **Sites** &gt; **Toevoegen**.

- Het programma wordt gestart en u wordt gevraagd contact op te nemen met de leverancier.

    **Oplossing:** voeg in Internet Explorer de URL voor Dynamics 365 for Retail aan uw vertrouwde sites toe. Klik op **Instelling** &gt; **Opties** &gt; **Beveiliging** &gt; **Vertrouwde sites** &gt; **Sites** &gt; **Toevoegen**.

**Bekend probleem:** de ontwerper werkt niet correct in Google Chrome en Mozilla Firefox. We werken aan een oplossing voor dit probleem.

## <a name="additional-resources"></a>Aanvullende bronnen

[Retail Modern POS configureren, downloaden en activeren](retail-modern-pos-device-activation.md)
