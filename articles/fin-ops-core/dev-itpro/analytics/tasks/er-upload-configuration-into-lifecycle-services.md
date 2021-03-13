---
title: Een configuratie in Lifecycle Services uploaden
description: In dit onderwerp wordt uitgelegd hoe u een nieuwe configuratie voor Elektronische rapportage (ER) maakt en uploadt in Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92fc6d7a8b2508c9a1f7b56ca8115adbd6ae00ea
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092536"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Een configuratie in Lifecycle Services uploaden

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) kan maken en uploaden in de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).

In dit voorbeeld maakt u een configuratie en uploadt u deze in LCS voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). Ook is toegang tot LCS vereist.

1. Meld u aan bij de toepassing met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer **Litware, Inc.** en markeer dit als **Actief**.
4. Selecteer **Configuraties**.

<a name="accessconditions"></a>
> [!NOTE]
> Zorg ervoor dat de huidige Dynamics 365 Finance-gebruiker lid is van het LCS-project dat de [activabibliotheek](../../lifecycle-services/asset-library.md#asset-library-support) bevat die wordt gebruikt voor het importeren van ER-configuraties.
>
> U hebt geen toegang tot een LCS-project vanuit een ER-opslagplaats voor een ander domein dan het domein dat in Finance wordt gebruikt. Als u het probeert, wordt een lege lijst met LCS-projecten weergegeven en kunt u geen ER-configuraties importeren uit de activabibliotheek op projectniveau in LCS. Als u activabibliotheken op projectniveau wilt openen vanuit een ER-opslagplaats die wordt gebruikt voor het importeren van ER-configuraties, meldt u zich aan bij Finance met de referenties van een gebruiker die hoort bij de tenant (domein) waarvoor het huidige Finance-exemplaar is ingericht.

## <a name="create-a-new-data-model-configuration"></a>Een nieuwe gegevensmodelconfiguratie maken

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** de optie **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen.

    In dit voorbeeld maakt u een configuratie die een voorbeeldgegevensmodel voor elektronische documenten bevat. Deze gegevensmodelconfiguratie wordt later in LCS geüpload.

3. Typ **Voorbeeldmodelconfiguratie** in het veld **Naam**.
4. Typ **Voorbeeldmodelconfiguratie** in het veld **Beschrijving**.
5. Selecteer **Configuratie maken**.
6. Selecteer **Modelontwerper**.
7. Selecteer **Nieuw**.
8. Voer in het veld **Naam** de waarde **Invoerpunt** in.
9. Selecteer **Toevoegen**.
10. Selecteer **Opslaan**.
11. Sluit de pagina.
12. Selecteer **Status wijzigen**.
13. Selecteer **Voltooien**.
14. Selecteer **OK**.
15. Sluit de pagina.

## <a name="register-a-new-repository"></a>Een nieuwe opslagplaats registreren

1. Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.

2. Selecteer in de sectie **Configuratieproviders** de tegel **Litware, Inc.**

3. Klik op de tegel **Litware, Inc.** op **Opslagplaatsen**.

    U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.

4. Selecteer **Toevoegen** om het dialoogvenster met vervolgkeuzemenu te openen.

    U kunt nu een nieuwe opslagplaats toevoegen.

5. Selecteer **LCS** in het veld **Opslagplaats van configuratie**.
6. Selecteer **Opslagplaats maken**.
7. Typ of selecteer een waarde in het veld **Project**.

    Selecteer voor dit voorbeeld het gewenste LCS-project. U moet [toegang](#accessconditions) tot het project hebben.

8. Selecteer **OK**.

    Voer een nieuwe opslagplaats in.

9. Markeer in de lijst de geselecteerde rij.

    Selecteer voor dit voorbeeld de opslaglocatierecord **LCS**.

    Een geregistreerde opslagplaats wordt gemarkeerd door de huidige provider. Met andere woorden, alleen configuraties die eigendom van die provider zijn, kunnen in deze opslagplaats worden geplaatst en dus naar het geselecteerde LCS-project worden geüpload.

10. Selecteer **Openen**.

    U opent de opslagplaats om de lijst met ER-configuraties weer te geven. Als het geselecteerde project nog niet voor delen van ER-configuraties is gebruikt, is de lijst leeg.

11. Sluit de pagina.
12. Sluit de pagina.

## <a name="upload-a-configuration-into-lcs"></a>Een configuratie uploaden naar LCS

1. Ga naar **Organisatiebeheer \> Elektronische rapportage \> Configuraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Voorbeeldmodelconfiguratie**.

    U moet een gemaakte configuratie selecteren die al is voltooid.

3. Zoek en selecteer de gewenste record in de lijst.

    Selecteer voor dit voorbeeld de versie van de geselecteerde configuratie met de status **Voltooid**.

4. Selecteer **Status wijzigen**.
5. Selecteer **Delen**.

    De status van de configuratie wordt gewijzigd van **Voltooid** in **Gedeeld** wanneer de configuratie wordt gepubliceerd in LCS.

6. Selecteer **OK**.
7. Zoek en selecteer de gewenste record in de lijst.

    Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.

    De status van de geselecteerde versie is gewijzigd van **Voltooid** in **Gedeeld**.

8. Sluit de pagina.
9. Selecteer **Opslagplaatsen**.

    U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.

10. Selecteer **Openen**.

    Selecteer voor dit voorbeeld de opslaglocatierecord **LCS** en open deze.

    De geselecteerde configuratie wordt getoond als een activum van het geselecteerde LCS-project.

11. Open LCS door naar <https://lcs.dynamics.com> te gaan.
12. Open een project dat eerder is gebruikt voor de registratie van de opslagplaats.
13. Open de activabibliotheek van het project.
14. Selecteer het activumtype **GER-configuratie**.

    De ER-configuratie die u hebt geüpload, moet worden vermeld.

    De geüploade LCS-configuratie kan naar een ander exemplaar worden geïmporteerd als providers toegang tot dit LCS-project hebben.
