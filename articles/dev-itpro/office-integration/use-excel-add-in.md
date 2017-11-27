---
title: De Excel-invoegtoepassing gebruiken
description: In dit onderwerp wordt uitgelegd hoe u entiteitsgegevens in Microsoft Excel kunt openen en deze vervolgens bekijken, bijwerken en bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel.
author: ChrisGarty
manager: AnnBe
ms.date: 11/06/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b1f25f3630ad5126edd20c5508b83a9811a65f8
ms.openlocfilehash: dd986d8f82c42c4e229e6e60bdfe8d15a273e149
ms.contentlocale: nl-nl
ms.lasthandoff: 11/07/2017

---

# <a name="use-the-excel-add-in"></a>De Excel-invoegtoepassing gebruiken

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u entiteitsgegevens in Microsoft Excel kunt openen en deze vervolgens bekijken, bijwerken en bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel. Om de entiteitsgegevens te openen, kunt u beginnen vanuit Excel of Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Door entiteitsgegevens in Excel te openen, kunt u deze snel en eenvoudig bekijken en bewerken met de Excel-invoegtoepassing. Voor deze invoegtoepassing is Microsoft Excel 2016 vereist.

> [!NOTE]
> Als uw Microsoft Azure AD-tenant (Azure Active Directory) is geconfigureerd voor het gebruik van Active Directory Federation Services (AD FS), moet u ervoor zorgen dat de Office-update van mei 2016 is toegepast, zodat u correct kunt worden aangemeld voor de Excel-invoegtoepassing.

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Entiteitsgegevens in Excel openen vanuit Finance and Operations
1. Selecteer op een pagina in Finance and Operations de optie **Openen in Microsoft Office**.

    Als de hoofdgegevensbron (tabel) voor de pagina dezelfde is als de hoofdgegevensbron voor enige entiteiten, worden standaardopties voor **Openen in Excel** voor de pagina gegenereerd. **Openen in Excel**-opties vindt u op veelgebruikte pagina's, zoals **Alle leveranciers** en **Alle klanten**.
 
2. Selecteer de optie **Openen in Excel** en open de werkmap die wordt gegenereerd. Deze werkmap heeft bindingsgegevens voor de entiteit, een verwijzing naar uw omgeving en een verwijzing naar de Excel-invoegtoepassing.
3. Selecteer in Excel de optie **Bewerken inschakelen** zodat de Excel-invoegtoepassing kan worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4. Als u de Excel-invoegtoepassing voor het eerst uitvoert, selecteert u **Deze invoegtoepassing vertrouwen**.
5. Als u wordt gevraagd om u aan te melden, selecteert u **Aanmelden**. Vervolgens meldt u zich aan met de referenties waarmee u zich ook hebt aangemeld bij Finance and Operations. Als dat mogelijk is, gebruikt de Excel-invoegtoepassing een vorige aanmeldingscontext van Internet Explorer om u automatisch aan te melden. Controleer daarom de gebruikersnaam in de rechterbovenhoek van de Excel-invoegtoepassing.

De Excel-invoegtoepassing leest automatisch de gegevens voor de entiteit die u hebt geselecteerd. Houd er rekening mee dat de werkmap geen gegevens bevat, totdat de Excel-invoegtoepassing deze inleest.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Entiteitsgegevens in Excel openen vanuit Excel
1. Selecteer in Excel op het tabblad **Invoegen** in de groep **Invoegtoepassingen** de optie **Store** om de Office Store te openen.
2. Zoek in de Office Store op het trefwoord **Dynamics** en selecteer **Toevoegen** naast **Microsoft Dynamics Office-invoegtoepassing** (de Excel-invoegtoepassing).
3. Als u de Excel-invoegtoepassing voor het eerst uitvoert, selecteert u **Deze invoegtoepassing vertrouwen** zodat de Excel-invoegtoepassing kan worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4. Selecteer **Servergegevens toevoegen** om het deelvenster **Opties** te openen.
5. Kopieer de URL van uw doel-exemplaar van Finance and Operations in uw browser, plak deze in het veld **Server-URL** en verwijder alle gegevens achter de hostnaam. De resulterende URL moet alleen de hostnaam bevatten.

    Als de URL bijvoorbeeld `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` is, verwijdert u alles behalve `https://xxx.dynamics.com`.

6. Selecteer **OK** en vervolgens **Ja** om de wijziging te bevestigen. De Excel-invoegtoepassing wordt opnieuw gestart en metagegevens worden geladen.

    De knop **Ontwerpen** is nu beschikbaar. Als de Excel-invoegtoepassing een knop **Applets laden** bevat, bent u waarschijnlijk niet aangemeld als de juiste gebruiker. Zie voor meer informatie 'De knop Applets laden wordt getoond' in de sectie [Problemen oplossen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) in dit onderwerp.

7. Selecteer **Ontwerp**. De Excel-invoegtoepassing haalt entiteit metagegevens op.
8. Selecteer **Tabel toevoegen**. Een lijst met entiteiten wordt geopend. De entiteiten worden weergegeven in de indeling 'Naam - label'.
9. Selecteer een entiteit in de lijst, zoals **Klant - Klanten**, en selecteer **Volgende**.
10. Als u een veld uit de lijst **Beschikbare velden** wilt toevoegen aan de lijst **Geselecteerde velden**, selecteert u het veld en vervolgens **Toevoegen**. U kunt ook dubbelklikken op het veld in de lijst **Beschikbare velden**.
11. Nadat u het toevoegen van velden aan de lijst **Geselecteerde velden** hebt voltooid, controleert u of de cursor op de juiste plaats in het werkblad staat (bijvoorbeeld cel A1) en selecteert u **Gereed**. Selecteer **Gereed** om de ontwerper af te sluiten.
12. Selecteer **Vernieuwen** om een reeks gegevens op te halen.

## <a name="view-and-update-entity-data-in-excel"></a>Entiteitsgegevens weergeven en bijwerken in Excel
Nadat de Excel-invoegtoepassing entiteitsgegevens in de werkmap heeft ingelezen, kunt u de gegevens op elk moment bijwerken door **Vernieuwen** te selecteren in de Excel-invoegtoepassing.

## <a name="edit-entity-data-in-excel"></a>Entiteitsgegevens in Excel bewerken
U kunt entiteitsgegevens naar wens wijzigen en deze vervolgens weer publiceren door **Publiceren** in de Excel-invoegtoepassing te selecteren. Om een record te bewerken, selecteert u een cel in het werkblad en wijzigt u de celwaarde. Als u een nieuwe record wilt toevoegen, volgt u een van deze stappen:

- Klik ergens in de gegevensbrontabel en selecteert vervolgens **Nieuw** in de Excel-invoegtoepassing.
- Klik in de laatste rij van de gegevensbrontabel en druk vervolgens op Tab totdat de cursor uit de laatste kolom van die rij wordt verplaatst en er een nieuwe rij wordt gemaakt.
- Klik in de rij direct onder de gegevensbrontabel en begin gegevens in te voeren in een cel. Wanneer u de focus uit die cel verplaatst, wordt de tabel uitgebreid met de nieuwe rij.
- Selecteer een van de velden voor veldbindingen van koptekstrecords en selecteer vervolgens **Nieuw** in de Excel-invoegtoepassing.

Houd er rekening mee dat alleen een nieuwe record kan worden gemaakt als alle belangrijke en verplichte velden in het werkblad zijn gekoppeld of als standaardwaarden zijn ingevuld met behulp van de filtervoorwaarde.

Als u een record wilt verwijderen, volgt u een van deze stappen:

- Klik met de rechtermuisknop op het rijnummer naast de werkbladrij die u wilt verwijderen en selecteer **Verwijderen**.
- Klik met de rechtermuisknop in de werkbladrij die u wilt verwijderen en selecteer **Verwijderen** &gt; **Tabelrijen**.

Als gegevensbronnen als gerelateerd zijn toegevoegd, wordt de koptekst gepubliceerd vóór de regels. Als er afhankelijkheden bestaan tussen andere gegevensbronnen, moet u wellicht de standaardpublicatievolgorde wijzigen. U wijzigt de publicatievolgorde door in de Excel-invoegtoepassing de knop **Opties** (tandwiel) te selecteren en vervolgens op het sneltabblad **Gegevensconnector** de optie **Publicatieorder configureren** te selecteren.

## <a name="add-or-remove-columns"></a>Kolommen toevoegen of verwijderen
Met de ontwerper kunt u de kolommen aanpassen die automatisch worden toegevoegd aan het werkblad.

> [!NOTE]
> Als de knop **Ontwerp** niet wordt weergegeven onder de knop **Filter** in de Excel-invoegtoepassing, moet u de gegevensbronontwerper inschakelen. Selecteer de knop **Opties** (tandwiel) en schakel het selectievakje **Ontwerpen inschakelen** in.

1. Selecteer **Ontwerpen** in de Excel-invoegtoepassing. Alle gegevensbronnen worden vermeld.
2. Selecteer naast de gegevensbron de knop **Bewerken** (potlood).
3. Pas in de lijst **Geselecteerde velden** de lijst met velden naar wens aan:

    - Als u een veld uit de lijst **Beschikbare velden** wilt toevoegen aan de lijst **Geselecteerde velden**, selecteert u het veld en vervolgens **Toevoegen**. U kunt ook dubbelklikken op het veld in de lijst **Beschikbare velden**.
    - Als u een veld wilt verwijderen uit de lijst **Geselecteerde velden**, selecteert u dit veld en vervolgens de optie **Verwijderen**. U kunt ook dubbelklikken op het gewenste veld.
    - Als u de volgorde van velden in de lijst **Geselecteerde velden** wilt wijzigen, selecteert u een veld en vervolgens **Omhoog** of **Omlaag**.

4. Pas uw wijzigingen toe op de gegevensbron door **Bijwerken** te selecteren. Selecteer **Gereed** om de ontwerper af te sluiten.
5. Als u een veld (kolom) hebt toegevoegd, selecteert u **Vernieuwen** om een bijgewerkte set gegevens op te halen.

## <a name="copy-environment-data"></a>Gegevens van omgeving kopiëren
De gegevens die vanuit de ene omgeving worden ingelezen in de werkmap, kunnen naar een andere omgeving worden gekopieerd. U kunt echter niet alleen de verbindings-URL wijzigen omdat de gegevenscache in de werkmap de gegevens dan blijft behandelen als bestaande gegevens. In plaats daarvan moet u de functie Gegevens van omgeving kopiëren om de gegevens naar een nieuwe omgeving te publiceren als nieuwe gegevens.

1. Selecteer de knop **Opties** (tandwiel) en selecteer op het sneltabblad **Gegevensconnector** de optie **Gegevens van omgeving kopiëren**.
2. Geef de server-URL voor de nieuwe omgeving op.
3. Selecteer **OK** en vervolgens **Ja** om de actie te bevestigen. De Excel-invoegtoepassing wordt opnieuw gestart en maakt verbinding met de nieuwe omgeving. De bestaande gegevens in de werkmap worden behandeld als nieuwe gegevens.

    Als de Excel-invoegtoepassing opnieuw is gestart, wordt in een berichtvenster aangegeven dat de werkmap zich in de modus voor omgeving kopiëren bevindt.

4. Selecteer **Publiceren** om de gegevens in de nieuwe omgeving als nieuwe gegevens te kopiëren. Als u de bewerking voor het kopiëren van de omgeving wilt annuleren en de bestaande gegevens in de nieuwe omgeving wilt weergeven, selecteert u **Vernieuwen**.

## <a name="troubleshooting"></a>Problemen oplossen
Er zijn enkele problemen die kunnen worden opgelost met enkele eenvoudige stappen.

- **De knop Applets laden wordt getoond**: als de Excel-invoegtoepassing een knop **Applets laden** bevat nadat u zich hebt aangemeld, bent u waarschijnlijk niet aangemeld als de juiste gebruiker. Controleer of de juiste gebruikersnaam zichtbaar is in de rechterbovenhoek van het Excel-invoegtoepassing. Als een onjuiste gebruikersnaam wordt getoond, selecteert u deze en meldt u zich af en vervolgens weer aan met de juiste gebruiker.
- **U ontvangt een melding 'Verboden'**: als u het foutbericht 'Verboden' krijgt wanneer de Excel-invoegtoepassing metagegevens laadt, is de account die is aangemeld bij de Excel-invoegtoepassing niet gemachtigd om de beoogde service, instantie of database te gebruiken. Controleer of de juiste gebruikersnaam zichtbaar is in de rechterbovenhoek van het Excel-invoegtoepassing. Als een onjuiste gebruikersnaam wordt getoond, selecteert u deze en meldt u zich af en vervolgens weer aan met de juiste gebruiker.
- **Een lege webpagina wordt weergegeven via Excel**: als een lege webpagina wordt geopend tijdens het aanmelden, vereist de account AD FS maar is de versie van Excel waarin u de invoegtoepassing uitvoert niet recent genoeg om het aanmeldingsvenster weer te geven. Werk Excel bij naar een meer recente versie. Als u de versie van Excel wilt bijwerken wanneer u werkt in een onderneming die zich op het Deferred-kanaal bevindt, wijzigt u met het [hulpprogramma Office Deployment](https://technet.microsoft.com/library/jj219422.aspx) van [het Deferred-kanaal naar het Current-kanaal](https://technet.microsoft.com/library/mt455210.aspx).

