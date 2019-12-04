---
title: Toepassingsspecifieke metagegevens voorbereiden voor RCS en ER
description: In dit onderwerp wordt uitgelegd hoe u toepassingsspecifieke metagegevens voorbereidt voor Regulatory Configuration Service (RCS) en Elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 89d36c305bc9210f7906cd4288e33e5028baecdb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771255"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>Toepassingsspecifieke metagegevens voorbereiden voor RCS en ER

[!include[banner](../includes/banner.md)]

In dit onderwerp vindt u een aantal voorbeelden van de volgende taken:

- [Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Toepassingsmetagegevens openen door gebruik van een ER-configuratie](#access-application-metadata-by-using-an-er-configuration)
- [Toepassingsmetagegevens openen door gebruik van verbonden toepassingen](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden

De volgende procedure laat zien hoe een gebruiker met de rol van **Systeembeheerder** of **Ontwikkelaar van elektronische rapportage** een ER-configuratie kan maken die metagegevens bevat voor de toepassing en die wordt gebruikt om ER‑modeltoewijzingsconfiguraties te ontwerpen in de Regulatory Configuration Service (RCS). De configuratie van de voorbeeld ER modeltoewijzingsconfiguratie die in dit voorbeeld wordt gemaakt, wordt gebruikt om transacties van buitenlandse handel te openen.

Voor dit voorbeeld gaat u RCS gebruiken om een ER-oplossing te ontwerpen voor de toepassing die wordt gebruikt om elektronische documenten te genereren die informatie bevatten uit het bedrijfsdomein voor buitenlandse handel. Als u de toewijzing wilt opgeven tussen het ER-gegevensmodel en de bronnen van vereiste gegevens, moet u toegang hebben tot de toepassingsmetagegevens in RCS. Als onderdeel van het ontwerpproces van de ER-oplossing moet u dus een nieuwe ER-metagegevensconfiguratie configureren die alle vereiste metagegevens bevat om ER‑rapporten voor het geselecteerde bedrijfsdomein te genereren.

> [!NOTE]
> In dit voorbeeld maakt u een configuratie voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

1. Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Selecteer **Metagegevensconfiguraties**.
4. Selecteer **Configuratie maken**.
5. Voer in het vervolgkeuzemenu in het veld **Naam** een naam in. Voer voor dit voorbeeld **Metagegevens buitenlandse handel** in.
6. Selecteer **Configuratie maken**.
7. Selecteer **Ontwerper**.
8. Selecteer **Toevoegen**.

    > [!NOTE]
    > U kunt alle metagegevens voor de gehele toepassing of voor geselecteerde modellen of modules selecteren. Houd er in beide gevallen rekening mee dat de volgende metagegevens automatisch worden toegevoegd: tabellen met records, inventarisaties en uitgebreide gegevenstypen (EDT's). Als er aanvullende typen metagegevens nodig zijn, moeten deze handmatig worden toegevoegd.

    U moet metagegevens toevoegen die zijn gerelateerd aan transacties voor buitenlandse handel en handmatig metagegevensitems selecteren.

9. Selecteer **Gegevensbron toevoegen \> Tabelrecords**.
10. Filter op de waarde **Intrastat** in het veld **Naam**.
11. Selecteer de **Intrastat** -tabelrecord.
12. Selecteer **OK**.

    U moet metagegevens over de Intrastat-tabelrecords toevoegen.

13. Selecteer in de structuur **Tabelrecords Intrastat \> \>Relaties \> IntrastatCommodity (tabelrecords EcoResCategory**).
14. Selecteer **Metagegevens toevoegen**.

    > [!NOTE]
    > Metagegevens over vereiste relaties voor de geselecteerde tabelrecords moeten hand matig worden toegevoegd.

15. Selecteer **Gegevensbron toevoegen**.
16. Selecteer **Opsomming**.
17. Filter op de waarde **IntrastatDirection** in het veld **Naam**.
18. Selecteer het **IntrastatDirection** opsommingsrecord.
19. Selecteer **OK**.
20. Selecteer **Opslaan**.
21. Sluit de pagina.
22. De conceptversie van de metagegevensconfiguratie voltooien:

    1. Selecteer **Status wijzigen \> Voltooien**.
    2. Selecteer **OK**.
    3. Selecteer de voltooide versie 1.

23. De voltooide versie van de metagegevensconfiguratie van de toepassing exporteren als een XML-bestand:

    1. Selecteer **Uitwisselen \> Bestand exporteren als XML**.
    2. Selecteer **OK**.

De metagegevensconfiguratie die u hebt gemaakt, wordt opgeslagen als het bestand **Buitenlandse handel metagegevens.xml**. U kunt dit nu importeren in RCS, zodat het kan worden gebruikt als de bron van metagegevens voor het bedrijfsdomein voor buitenlandse handel. Op basis van deze informatie kunt u de toewijzing opgeven tussen de toepassingsmetagegevens en het ER-gegevensmodel.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Toepassingsmetagegevens openen met gebruik van een ER-configuratie

De volgende procedure laat zien hoe een gebruiker met de rol **Systeembeheerder** of **Ontwikkelaar elektronische rapportage** een nieuwe ER-modeltoewijzing kan ontwerpen door metagegevens uit de toepassing te gebruiken. De metagegevens van de toepassing worden benaderd via een ER-metagegevensconfiguratie die een voorbeeldset bevat van metagegevens voor de toegang tot buitenlandse handelstransacties.

Voordat u deze procedure kunt uitvoeren, moet u eerst de volgende procedures voltooien:

- [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [Toepassingsmetagegevens die kunnen worden gebruikt in RCS voorbereiden](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Ga naar **Alle werkgebieden \> Elektronische rapportage**.
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importeer de ER‑metagegevensconfiguratie die metagegevens voor de toepassing bevat en die is geconfigureerd voor het genereren van elektronische documenten voor het domein buitenlandse handel. U hebt deze metagegevensconfiguratie gemaakt en als XML-bestand geëxporteerd in de procedure [Voorbereiden van metagegevens die kunnen worden gebruikt in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) eerder in dit onderwerp.

    1. Selecteer **Metagegevensconfiguraties**.
    2. Selecteer **Uitwisselen**.
    3. Selecteer **Laden uit XML-bestand**.
    4. Blader om het bestand **Buitenlandse handel metagegevens.xml** te selecteren.
    5. Selecteer **OK**.
    6. Sluit de pagina.

4. Een gegevensmodelconfiguratie maken:

    1. Selecteer **Rapportageconfiguraties**.
    2. Selecteer **Configuratie maken**.
    3. Voer in het vervolgkeuzemenu in het veld **Naam** **Model buitenlandse handel** in.
    4. Selecteer **Configuratie maken**.
    5. Selecteer **Ontwerper**.
    6. Selecteer **Nieuw** om het uitklapdialoogvenster te openen.

        1. Typ het veld **Naam** **Basis**.
        2. Selecteer **Toevoegen**.
    
    7. Selecteer **Nieuw** om het uitklapdialoogvenster te openen.

        1. Typ in het veld **Naam** **Transactie**.
        2. Selecteer in het veld **Itemtype** **Recordlijst**.
        3. Selecteer **Toevoegen**.
 
    8. Selecteer **Nieuw** om het uitklapdialoogvenster te openen.

        1. Typ in het veld **Naam** **Code basisproduct**.
        2. Selecteer in het veld **Itemtype** **Tekenreeks**.
        3. Selecteer **Toevoegen**.

    9. Selecteer **Nieuw** om het uitklapdialoogvenster te openen.

        1. Typ in **Gefactureerd bedrag** in het veld Naam.
        2. Selecteer in het veld **Itemtype** **Werkelijk**.
        3. Selecteer **Toevoegen**.

    10. Selecteer **Nieuw** om het uitklapdialoogvenster te openen.

        1. Typ in het veld **Naam** **Datum**.
        2. Selecteer in het veld **Itemtype** **Datum**.
        3. Selecteer **Toevoegen**.
 
    11. Selecteer **Toevoegen \> Basisverwijzing**.
    12. Selecteer **OK**.
    13. Selecteer **Opslaan**.
    14. Sluit de pagina.
    15. Selecteer **Status wijzigen \> Voltooien**.
    16. Selecteer **OK**.

5. Een configuratie modeltoewijzing maken:

    1. Selecteer **Configuratie maken**.
    2. Voer in het uitklapdialoogvenster in het veld **Nieuw** in **Modeltoewijzing gebaseerd op gegevensmodel Buitenlandse handelsmodel**.
    3. Voer in het veld **Naam** in **Toewijzing buitenlandse handel**.
    4. Selecteer **Configuratie maken**.
    5. Selecteer op het sneltabblad **Vereisten** **Bewerken**.
    6. Selecteer **Nieuw**.
    7. Selecteer in het veld **Vereist onderdeeltype** **Configuratie**.
    8. Selecteer de configuratie **Metagegevens buitenlandse handel**.
    9. Selecteer **Opslaan**. Zie dat de verwijzing is toegevoegd aan versie 1 van de configuratie **Metagegevens buitenlandse handel**. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer de modeltoewijzing wordt ontworpen.
    10. Sluit de pagina.
    11. Selecteer **Ontwerper**.
    12. Selecteer **Ontwerper**.
    13. Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.
    14. Selecteer **Basis toevoegen**.
    15. Voer in het veld **Naam** **Intrastat** in.
    16. Selecteer **Intrastat** tabelrecords.
    17. Selecteer **OK**.

        > [!NOTE]
        > Er zijn slechts twee tabellen zijn aangeboden, omdat slechts twee tabellen zijn toegevoegd aan de set metagegevens die momenteel in gebruik is.

    18. Selecteer **Binden**.
    19. Selecteer **Intrastat \> BedragMST** in de structuur.
    20. Selecteer in de structuur **Transactie = Intrastat \> Gefactureerd bedrag**.
    21. Selecteer **Binden**.
    22. Selecteer **Intrastat \> TransDatum** in de structuur.
    23. Selecteer **Transactie = Intrastat \> Datum** in de structuur.
    24. Selecteer **Binden**.
    25. Selecteer in de structuur **Intrastat \> \>Relaties \> IntrastatBasisproduct \> Code**.
    26. Selecteer in de structuur **Transactie = Intrastat \> Basisproductcode**.
    27. Selecteer **Binden**.
    28. Selecteer **Valideren**.

        > [!NOTE]
        > Nadat de validatie is voltooid hebt u elementen van het gegevensmodel gebonden aan items van de gegevensbronnen die worden beschreven met behulp van de toepassingsmetagegevens van de ER metagegevensconfiguratie waarnaar wordt verwezen.

    29. Selecteer **Opslaan**.

Als u wenst, kunt u de bestaande set metagegevens uitbreiden in de toepassing. Vervolgens kunt u de nieuwe, voltooide versie van de ER metagegevensconfiguratie exporteren, en deze importeren in RCS en de vereisten van de geconfigureerde configuratie modeltoewijzing bijwerken om naar een nieuwe versie van de geïmporteerde metagegevensconfiguratie te verwijzen.

> [!NOTE]
> Deze methode om informatie op te halen over de metagegevens van de toepassing is de enige methode voor lokaal geïmplementeerde toepassingen (als een \[LBD\] (Local Business Data) of on-premises implementatiemodel wordt gebruikt voor de toepassing).

## <a name="access-application-metadata-by-using-connected-applications"></a>Metagegevens van de toepassing openen door gebruik van verbonden toepassingen

De volgende procedure laat zien hoe een gebruiker met de rol **Systeembeheerder** of **Ontwikkelaar elektronische rapportage** een nieuwe ER-modeltoewijzing kan ontwerpen door metagegevens van de toepassing te gebruiken. Toepassingsmetagegevens worden online benaderd via een RCS verbonden toepassing. Er wordt een voorbeeld ER modeltoewijzing geconfigureerd voor het openen van transacties van buitenlandse handel.

Als u de stappen in deze procedure wilt voltooien, moet u eerst de stappen in de procedure [Aanbieders van configuraties maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) in RCS voltooien. Als u de procedure [Open toepassingsmetagegevens met gebruik van een ER‑configuratie](#access-application-metadata-by-using-an-er-configuration) eerder in dit onderwerp niet hebt voltooid, gaat u naar de pagina [Taakbegeleiders voor elektronische rapportage voor Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) voor het vooraf downloaden van de volgende ER‑configuratiebestanden en deze lokaal opslaan: **Buitenlandse handel metagegevens.xml**, **Buitenlandse handel model.xml en** en **Buitenlandse handel toewijzing.xml**.


### <a name="get-required-er-configurations"></a>De vereiste ER-configuraties verkrijgen

Als u de stappen in de procedure [Gebruik de toepassingsmetagegevens met gebruik van een ER‑configuratie](#access-application-metadata-by-using-an-er-configuration) al eerder in dit onderwerp hebt voltooid, beschikt u al over alle vereiste ER‑configuraties (de configuraties buitenlandse handel metagegevens, model en toewijzing) in het huidige RCS‑exemplaar. In dat geval kunt u deze procedure overslaan.

1. Ga naar **Alle werkgebieden \> Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Laad de configuratiebestanden **Buitenlandse handel metagegevens.xml**, **Buitenlandse handel model.xml** en **Buitenlandse handel toewijzing.xml** door de volgende stappen voor elk van deze te herhalen:

    1. Selecteer **Uitwisselen**.
    2. Selecteer **Laden uit XML-bestand**.
    3. Selecteer **Bladeren** en selecteer een bestand.
    4. Selecteer **OK**.

### <a name="register-the-connection-with-the-application"></a>De verbinding bij de toepassing registreren

1. Ga naar **Alle werkgebieden \> Elektronische rapportage**.
2. Selecteer **Verbonden toepassingen**.
3. Controleer of de geconfigureerde toepassing is gebaseerd Microsoft Azure en toegankelijk is voor gebruikers van RCS. De huidige RCS-gebruiker moet toegang hebben tot de geconfigureerde toepassing terwijl deze is geregistreerd als gebruiker van deze toepassing in een rol die hem of haar de bevoegdheid geeft om de metagegevens van de toepassing te gebruiken.
4. Selecteer **Nieuw**.
5. Voer in het veld **Naam** in **MyConnectedApp** in als de naam van de verbonden toepassing.
6. Geef in het veld **Toepassing** de URL van de toepassing op.
7. Geef in het veld **Tenant** de provider van de toepassing op.
8. Selecteer **Opslaan**. 
9. Wanneer u de verbinding met de geconfigureerde toepassing controleert, selecteert u op de pagina **Maak verbinding met externe toepassing** de link **Selecteer hier om verbinding te maken met de geselecteerde externe toepassing**. 
10. Selecteer **Verbinding controleren** om de toegang tot de geconfigureerde toepassing te valideren.
11. Selecteer **Sluiten**.

Wanneer u de procedure voltooid en de verbindingsvalidatie slaagt, worden de versie- en tenantgegevens voor de geconfigureerde toepassing bijgewerkt in het huidige raster.

### <a name="review-the-existing-model-mapping-configuration"></a>De bestaande modeltoewijzingsconfiguratie controleren

1. Ga naar **Alle werkgebieden \> Elektronische rapportage**.
2. Selecteer **Rapportageconfiguraties**.
3. Selecteer in de structuur **Buitenlandse handel model \> Buitenlandse handel toewijzing**.
4. Selecteer het sneltabblad **Vereisten**.

    > [!NOTE]
    > Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.

4. Selecteer **Ontwerper**.
5. Selecteer **Ontwerper**.
6. Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.
7. Selecteer **Basis toevoegen**.
8. Typ of selecteer een waarde in het veld **Tabel**.

    > [!NOTE]
    > Deze toewijzing verwijst momenteel naar de metagegevensconfiguratie. De metagegevens van de toepassing van deze configuratie worden aangeboden wanneer deze modeltoewijzing wordt ontworpen.

9. Selecteer **Annuleren**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>De verbonden toepassing toewijzen aan een modeltoewijzing

1. Selecteer **Bewerken**.
2. Selecteer in het veld **Verbonden toepassing** de toepassing **MyConnectedApp**.

    > [!NOTE]
    > Deze toewijzing verwijst naar de metagegevens van de geselecteerde verbonden toepassing. Wanneer een toewijzing tegelijkertijd verwijst naar de configuratie van de metagegevens en de gekoppelde toepassing, dan worden de metagegevens van de verbonden toepassing gebruikt.

3. Selecteer **Ontwerper**.
4. Selecteer **Ontwerper**.
5. Selecteer in de structuur **Dynamics 365 for Operations \> Tabelrecords**.
6. Selecteer **Basis toevoegen**.
7. Typ of selecteer een waarde in het veld **Tabel**.

    > [!NOTE]
    > Op dit punt worden meer dan twee toepassingstabellen aangeboden, omdat deze toewijzing alle metagegevens van de verbonden toepassing gebruikt die hieraan is toegewezen.

8. Selecteer **Annuleren**.
9. Selecteer **Valideren**.

U hebt nu elementen van het gegevensmodel verbonden met items van de gegevensbronnen die worden beschreven met behulp van details van de metagegevens van de verbonden toepassing die is toegewezen voor deze toewijzing.

Wanneer u deze modeltoewijzing moet evalueren door de metagegevens van een andere versie van de applicatie te gebruiken, registreer dan een andere verbonden toepassing, en wijs deze toe aan deze modeltoewijzing en valideer deze tegen de nieuwe metagegevens.

## <a name="additional-resources"></a>Aanvullende resources

U kunt ook de taakbegeleider **Metagegevens van de toepassing die kunnen worden gebruikt in RCS voorbereiden** in de toepassing bekijken, evenals de taakbegeleiders **Metagegevens van de toepassing openen met gebruik van een ER-configuratie** en **Metagegevens van de toepassing openen met gebruik van verbonden toepassingen** in RCS. Deze taakbegeleiders kunt u downloaden van de pagina [Taakbegeleiders voor Elektronische rapportage voor Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).
