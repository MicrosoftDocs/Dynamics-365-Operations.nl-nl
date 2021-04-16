---
title: Regulatory Configuration Services (RCS) - Globalisatiefuncties
description: In dit onderwerp wordt uitgelegd hoe u Microsoft Regulatory Configuration Services (RCS) en de algemene opslagplaats kunt gebruiken om globalisatiefuncties te maken en te gebruiken.
author: JaneA07
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: cbb1d9a53a7a09ab525532f08553898c4e40223a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822776"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a>Regulatory Configuration Services (RCS) - Globalisatiefuncties

[!include [banner](../includes/banner.md)]

U kunt Microsoft Regulatory Configuration Services (RCS) gebruiken om een globalisatiefunctie te maken die kan worden gebruikt in globalisatieservices, zoals een service voor e-facturen. Met RCS kunt u de volgende taken uitvoeren:

- Verwante onderdelen van een functie definiëren.
- De functielevenscyclus beheren via de status van een functie.
- Een functie beschikbaar maken voor gedefinieerde omgevingen.
- Een functie delen met andere organisaties.

In de volgende procedures wordt uitgelegd hoe een gebruiker in RCS een globalisatiefunctie en verwante onderdelen kan toevoegen, de status van de functie kan bijwerken en de functie beschikbaar kan maken zodat deze kan worden gebruikt in globalisatieservices.

Voordat u de procedures uitvoert, moet u de stappen uitvoeren die betrekking hebben op de volgende taken:

- Een RCS-exemplaar openen.
- Een configuratieprovider maken en activeren. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.

Voer de volgende stappen uit in uw exemplaar van Finance and Operations-apps.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Als er geen RCS-omgeving is ingericht voor uw bedrijf, selecteert u **Regulatory services ‑ Configuratie** en volgt u de instructies om een RCS-omgeving in te richten.

> [!NOTE]
> Als er al een RCS-omgeving is ingericht voor uw bedrijf, gebruikt u de pagina-URL om deze te openen door de aanmeldingsoptie te selecteren.

## <a name="turn-on-the-globalization-features"></a>De globalisatiefuncties inschakelen

1. Selecteer de tegel **Functiebeheer** in uw RCS-exemplaar.
2. Selecteer in het werkgebied **Functiebeheer** de optie **Globalisatiefuncties** in de lijst en selecteer **Nu inschakelen**.

    ![Globalisatiefuncties in Functiebeheer](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a>Globalisatiefuncties

Als u een globalisatiefunctie wilt gebruiken, moet u deze eerst vanuit de globale opslagplaats importeren en uw eigen versie maken. Er zijn twee manieren om globalisatiefuncties toe te voegen:

- Voeg een afgeleide functie toe die is gebaseerd op een bestaande functie die is gepubliceerd of gedeeld.
- Voeg een nieuwe functie toe die u geheel zelf hebt gemaakt.

## <a name="access-globalization-features"></a>Globalisatiefuncties openen

1. Zorg dat de functie **Globalisatiefuncties** is ingeschakeld in Functiebeheer, zoals eerder in dit onderwerp wordt beschreven.
2. Open het nieuwe werkgebied **Globalisatiefuncties** en selecteer vervolgens onder **Functies** de tegel **E-facturering**.

    ![Werkgebied Globale functies](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    De pagina **Functies voor e-Facturering** wordt geopend.

    ![De pagina Functies voor e-Facturering](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a>Een afgeleide globalisatiefunctie toevoegen

U kunt een nieuwe globalisatiefunctie toevoegen door deze af te leiden van een bestaande functie die is gepubliceerd of gedeeld.

1. Selecteer **Importeren** om de pagina **Functie importeren uit algemene opslagplaats** te openen.

    ![De pagina Functie importeren uit algemene opslagplaats](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. Selecteer **Synchroniseren** om de nieuwste functies te downloaden.

    De gesynchroniseerde lijst bevat functies die beschikbaar zijn voor u, omdat deze door Microsoft zijn gepubliceerd of omdat ze door een andere configuratieprovider met u zijn gedeeld.

    ![Gesynchroniseerde lijst met functies](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. Selecteer in de lijst de functies die u wilt importeren en selecteer **Importeren**. U ontvangt een bericht wanneer de geselecteerde functies zijn geïmporteerd.

    ![Bericht over geslaagde import](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. Selecteer **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Op basis van bestaande versie**.
5. Voer een naam en beschrijving voor de functie in.
6. Selecteer de basisversie van de functie in de lijst met beschikbare functies en selecteer vervolgens **Functie maken**.

    ![Een afgeleide functie toevoegen](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    De functie die u hebt toegevoegd, wordt gemaakt met de status **Concept**.

    ![Afgeleide functie met status Concept](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. Controleer de functieonderdelen om te bepalen of er updates nodig zijn:

    - Bekijk de configuraties voor het geval u de ER-indelingen (Elektronische rapportage) en hun binding met indelingstoewijzingen voor de functieversie wilt aanpassen.
    - Controleer de instellingen voor het geval u het tabblad **Acties**, **Toepasbaarheidregels** of **Variabelen** voor de functieversie wilt aanpassen.

8. Selecteer op het tabblad **Versies** een **ingangsdatum** en voer een omschrijving in als het veld **Omschrijving** leeg is.
9. Selecteer **Status wijzigen** om de functie te voltooien. Voltooide functies kunnen voor een specifieke omgeving beschikbaar worden gemaakt, zodat deze kunnen worden gebruikt in globalisatieservices, of kunnen worden gepubliceerd naar de algemene opslagplaats.

> [!NOTE]
> Functies waarvoor **Status van functieversie** is ingesteld op **Gepubliceerd** kunnen worden gedeeld met externe organisaties.

## <a name="add-a-new-globalization-feature"></a>Een nieuwe globalisatiefunctie toevoegen

U kunt een nieuwe globalisatiefunctie toevoegen door deze helemaal opnieuw te maken.

1. Selecteer op de pagina **Functie importeren uit algemene opslagplaats** de optie **Toevoegen** en selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu de optie **Nieuwe functie**.
2. Voer een naam en beschrijving voor de functie in.
3. Selecteer **Functie maken**.

    ![Een nieuwe functie toevoegen](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. Selecteer op het tabblad **Versies** een **ingangsdatum** en selecteer vervolgens **Status wijzigen** om de functie te voltooien. Voltooide functies kunnen voor een specifieke omgeving beschikbaar worden gemaakt, zodat deze kunnen worden gebruikt in globalisatieservices, of kunnen worden gepubliceerd naar de algemene opslagplaats.

> [!NOTE]
> Functies waarvoor **Status van functieversie** is ingesteld op **Gepubliceerd** kunnen worden gedeeld met externe organisaties.

## <a name="feature-component-overview"></a>Overzicht van functieonderdelen

Globalisatiefuncties bestaan uit verschillende onderdelen:

- **Versie**: dit onderdeel ondersteunt het beheer van de functielevenscyclus en stelt gebruikers in staat om de status voor verschillende versies van de functie te beheren.
- **Configuraties**: met dit onderdeel kunnen gebruikers gerelateerde ER-indelingen en indelingstoewijzingen beheren, weergeven en bewerken.
- **Instellingen**: hiermee kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de instellingen van de gerelateerde functieversie beheren. Daarom ondersteunt deze de flexibele constructie van communicatie- en antwoordregels.
- **Omgeving**: met dit onderdeel kunnen gebruikers van globalisatieservices, zoals een e-factureringsservice, de omgeving beheren waarin de versie-instellingen van de functie worden gebruikt en machtigingen toekennen aan gebruikers die toegang hebben tot de service.
- **Organisaties**: met dit onderdeel kunnen gebruikers de functie delen met externe organisaties.

## <a name="configuring-feature-components"></a>Functieonderdelen configureren

### <a name="version-and-status"></a>Versie en status

De versie wordt gebruikt om de levenscyclus van de globalisatiefunctie te beheren.

U kunt de status wijzigen in het veld **Status** op het tabblad **Versie**. De volgende statussen zijn beschikbaar:

- **Concept**: de functie kan alleen worden bewerkt in deze status.
- **Voltooid**: de functie en alle gerelateerde onderdelen zijn voltooid (voltooid) en kunnen niet worden bewerkt.
- **Gepubliceerd**: de functie en alle gerelateerde onderdelen zijn gepubliceerd naar de algemene opslagplaats.
- **Gedeeld**: de functie en alle gerelateerde onderdelen zijn met externe organisaties gedeeld.
- **Ingeschakeld**: de functie en alle gerelateerde onderdelen zijn ingeschakeld voor gebruik in een globalisatieservice, zoals een e-factureringsservice.

> [!NOTE]
> Functies moeten opeenvolgend door een aantal van deze statussen worden geleid. Daarom is mogelijk niet elke status beschikbaar in elke levenscyclus.

### <a name="configurations"></a>Configuraties

De volgende acties zijn beschikbaar voor configuraties:

- **Weergeven**: geef de onderliggende functieconfiguraties weer waarvoor geen updates nodig zijn.
- **Bewerken**: maak een conceptversie van een geselecteerde configuratie, zodat u de indeling of indelingstoewijzing in de indelingsontwerper kunt bewerken.
- **Verwijderen**: verwijder een geselecteerde configuratie uit de functie.
- **Rebase**: rebase de functie. Zie de sectie [Afgeleide globalisatiefuncties rebasen](#rebase) verderop in dit onderwerp voor meer informatie.

### <a name="setups"></a>Instellingen

De volgende acties zijn beschikbaar voor functie-instellingen:

- **Toevoegen**: maak een nieuwe functie-instelling. Deze functie-instelling kan worden afgeleid van een bestaande functie-instelling of geheel nieuw zijn.
- **Verwijderen**: verwijder een geselecteerde functie-instelling.
- **Weergeven**: geef een onderliggende functie-instelling weer waarvoor geen wijzigingen nodig zijn.
- **Bewerken**: maak, verwijder of wijzig de kenmerken van de drie hoofdonderdelen van een functie-instelling:

    - Acties en hun parameters
    - Toepasbaarheidsregels
    - Variabelen

![De pagina voor functieversie-instellingen](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a>Omgevingen

De volgende acties zijn beschikbaar voor omgevingen:

- **Inschakelen**: selecteer voor een geselecteerde versie een gepubliceerde omgeving en selecteer een **ingangsdatum** wanneer deze beschikbaar moet zijn. Zie de sectie [Omgevingen configureren voor inschakelen](#configureenvironment) verderop in dit onderwerp voor meer informatie.
- **Annuleren**: verwijder een omgeving voor een functie-instelling.

### <a name="organizations"></a>Organisaties

Voer de volgende stappen om een globalisatiefunctie te delen met een externe organisatie.

1. Selecteer op de pagina **Functies voor e-Facturering** de functie en de versie van de functie die u wilt delen.
2. Selecteer op het tabblad **Organisaties** de optie **Delen met** en voer vervolgens in het dialoogvenster met vervolgkeuzemenu de domeinnaam van de organisatie in.
3. Selecteer **Delen**.

    ![Een functie delen met een organisatie](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

De functie wordt gedeeld met de geselecteerde organisatie en is beschikbaar voor die organisatie in de algemene opslagplaats. Hier kunt u de functie importeren in het RCS- of Dynamics 365 Finance-exemplaar van de organisatie, zodat dit kan worden gebruikt.

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a>Afgeleide globalisatiefuncties rebasen

U kunt een afgeleide globalisatiefunctie rebasen naar de nieuwe of bijgewerkte versie van de basisfunctie. Op deze manier kunnen wijzigingen die in de basisversie zijn opgetreden automatisch worden bijgewerkt. De bijgewerkte versie van de basisfunctie wordt gemaakt door de oorspronkelijke configuratieprovider en wordt vervolgens gepubliceerd of gedeeld.

![Bijgewerkte versie van basisfunctie](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

Als u bijvoorbeeld de afgeleide versie wilt rebasen van een functie die u hebt gemaakt, haalt u eerst de meest recente versie van de functie op door deze te importeren uit de globale opslagplaats.

1. Selecteer **Importeren** op de pagina **Functies voor e-Facturering**.
2. Selecteer **Synchroniseren** om de nieuwste functies te downloaden.
3. Selecteer in de lijst met functies de functies die u wilt importeren en selecteer **Importeren**.

    ![De nieuwste versie van een functie importeren](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. Selecteer in de lijst met functies de functie die u wilt rebasen.
5. Selecteer op het tabblad **Versie** de optie **Nieuw** om een conceptversie te maken.

    ![Nieuwe conceptversie gemaakt](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. Selecteer **Rebase**.
7. Selecteer in het dialoogvenster **Rebase** de nieuwste versie van de functie waarnaar u wilt rebasen.

    ![Het dialoogvenster Rebase](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. Selecteer **OK**.
9. Controleer de functieonderdelen en breng eventueel vereiste wijzigingen aan.
10. Selecteer **Status wijzigen** om de functie te voltooien waarvoor een rebase is uitgevoerd. Wanneer de rebase is voltooid, kunt u extra acties uitvoeren. U kunt de functie bijvoorbeeld publiceren en beschikbaar maken voor gebruik in globalisatieservices.

    ![Functiestatus bijgewerkt naar Voltooid](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a>Omgevingen configureren voor globalisatiefuncties

Gebruikers van globalisatieservices kunnen de omgeving beheren om een globalisatiefunctie in te stellen en autorisatie te verlenen aan andere gebruikers die hiertoe toegang hebben.

1. In het werkgebied **Globalisatiefuncties** selecteert u onder **Omgevingen** de tegel **E-facturering**.

    ![Het werkgebied Globalisatiefuncties](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. Selecteer **Sleutelkluisparameters** en vervolgens **Nieuw** om een Azure-sleutelkluisgeheim te maken.
3. Voer een naam en omschrijving voor de sleutelkluis in en voer in het veld **URI sleutelkluis** de URL in waarmee de sleutelkluisresource in Azure wordt aangeduid.
4. Selecteer op het sneltabblad **Certificaten** de optie **Toevoegen** om het certificaat toe te voegen en voer een naam en omschrijving voor elk certificaat in.

    ![Certificaat toegevoegd](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. Selecteer **Nieuw** om een nieuwe omgeving te maken.
6. Voer een naam, een beschrijving en het geheime token voor handtekeningen voor gedeelde toegang in dat vereist is voor de opslag.
7. Selecteer op het sneltabblad **Gebruikers** de optie **Nieuw** om een gebruiker toe te voegen die toegang heeft tot deze omgeving.
8. Voer de gebruikers-id en het e-mailadres van de gebruiker in.
9. Herhaal stap 7 en 8 om nog meer gebruikers toe te voegen.
10. Selecteer **Publiceren** om de omgeving te publiceren.

    ![Gepubliceerde omgeving](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]