---
title: De Excel-invoegtoepassing gebruiken
description: In dit onderwerp wordt uitgelegd hoe u entiteitsgegevens in Microsoft Excel kunt openen en deze vervolgens bekijken, bijwerken en bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 06fc9f8dda83fddea9ae331bb82c8874b15d76b9
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="use-the-excel-add-in"></a>De Excel-invoegtoepassing gebruiken

[!include[banner](../includes/banner.md)]


In dit onderwerp wordt uitgelegd hoe u entiteitsgegevens in Microsoft Excel kunt openen en deze vervolgens bekijken, bijwerken en bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel. Om de entiteitsgegevens te openen, kunt u beginnen vanuit Excel of Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.

Als u entiteitsgegevens in Microsoft Excel opent, kunt u deze snel en eenvoudig bekijken en bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel. Voor deze invoegtoepassing is Microsoft Excel 2016 vereist. **Opmerking:** Als uw Microsoft Azure AD-tenant (Azure Active Directory) is geconfigureerd voor het gebruik van Active Directory Federation Services (AD FS), moet u ervoor zorgen dat de update van mei 2016 is toegepast, zodat de Excel-invoegtoepassing u correct kan aanmelden.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-finance-and-operations"></a>Entiteitsgegevens in Excel openen vanuit Dynamics 365 for Finance and Operations
1.  Klik op een pagina in Microsoft Dynamics 365 for Finance and Operations op **Openen in Microsoft Office**. Als de hoofdgegevensbron (tabel) voor de pagina dezelfde is als de hoofdgegevensbron voor enige entiteiten, worden standaardopties voor **Openen in Excel** voor de pagina gegenereerd. **Openen in Excel**-opties vindt u op veelgebruikte pagina's, zoals **Alle leveranciers** en **Alle klanten**.
2.  Klik op een **Openen in Excel**-optie en open de werkmap die wordt gegenereerd. Deze werkmap heeft bindingsgegevens voor de entiteit, een verwijzing naar uw omgeving en een verwijzing naar de Excel-invoegtoepassing.
3.  Klik in Excel op **Bewerken inschakelen** zodat de Excel-invoegtoepassing kan worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4.  Als u de Excel-invoegtoepassing voor de eerste keer uitvoert, klikt u op **Deze invoegtoepassing vertrouwen**.
5.  Als u wordt gevraagd om u aan te melden, klikt u op **Aanmelden**. Vervolgens meldt u zich aan met dezelfde referenties die u gebruikt voor aanmelding bij Dynamics 365 for Finance and Operations. Als dat mogelijk is, gebruikt de Excel-invoegtoepassing een vorige aanmeldingscontext van Internet Explorer om u automatisch aan te melden. Controleer daarom de gebruikersnaam in de rechterbovenhoek van de Excel-invoegtoepassing.

De Excel-invoegtoepassing leest automatisch de gegevens voor de entiteit die u hebt geselecteerd. Houd er rekening mee dat de werkmap geen gegevens bevat, totdat de Excel-invoegtoepassing deze inleest.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Entiteitsgegevens in Excel openen vanuit Excel
1.  Klik in Excel op het tabblad **Invoegen** in de groep **Invoegtoepassingen** op **Store** om de Office-store te openen.
2.  Zoek in de Office Store op het trefwoord 'Dynamics' en klik op **Toevoegen** naast de **Microsoft Dynamics Office-invoegtoepassing** (de Excel-invoegtoepassing).
3.  Als u de Excel-invoegtoepassing voor de eerste keer uitvoert, klikt u op **Deze invoegtoepassing vertrouwen** zodat de Excel-invoegtoepassing kan worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4.  Klik op **Servergegevens toevoegen** om het deelvenster **Opties** te openen.
5.  Kopieer de browser-URL van uw doel-exemplaar van Dynamics 365 for Finance and Operations, plak deze in het veld **Server-URL** en verwijder alle gegevens achter de hostnaam. De resulterende URL moet de hostnaam hebben.
Bijvoorbeeld: als de URL is https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage, verwijdert u alles behalve **https://xxx.dynamics.com**.
6.  Klik op **OK** en vervolgens op **Ja** om de wijziging te bevestigen. De Excel-invoegtoepassing wordt opnieuw opgestart en metagegevens worden geladen. De knop **Ontwerpen** is nu beschikbaar. Als de Excel-invoegtoepassing een knop **Applets laden** bevat, bent u waarschijnlijk niet aangemeld als de juiste gebruiker. Zie voor meer informatie de paragraaf 'De knop Applets laden wordt getoond' in de sectie 'Problemen oplossen' in dit onderwerp.
7.  Klik op **Ontwerpen**. De Excel-invoegtoepassing haalt entiteit metagegevens op.
8.  Klik op **Tabel toevoegen**. Een lijst met entiteiten wordt geopend. De entiteiten worden weergegeven in de indeling 'Naam - label'.
9.  Selecteer een entiteit in de lijst, zoals **Klant - Klanten** en klik op **Volgende**.
10. Als u een veld uit de lijst **Beschikbare velden** wilt toevoegen aan de lijst **Geselecteerde velden**, klikt u op het gewenste veld en vervolgens op **Toevoegen**. U kunt ook dubbelklikken op het gewenste veld.
11. Nadat u het toevoegen van velden aan de lijst **Geselecteerde velden** hebt voltooid, controleert u of de cursor op de juiste plaats in het werkblad staat (bijvoorbeeld cel A1) en klikt u op **Gereed**. Klik daarna op **Gereed** om de ontwerper af te sluiten.
12. Klik op **Vernieuwen** om een reeks gegevens op te halen.

## <a name="view-and-update-entity-data-in-excel"></a>Entiteitsgegevens weergeven en bijwerken in Excel
Nadat u de Excel-invoegtoepassing entiteitsgegevens in de werkmap heeft ingelezen, kunt u deze op elk gewenst moment bijwerken door te klikken op **Vernieuwen** in de Excel-invoegtoepassing.

## <a name="edit-entity-data-in-excel"></a>Entiteitsgegevens in Excel bewerken
U kunt naar wens entiteitsgegevens bewerken en deze vervolgens weer publiceren, door te klikken op **Publiceren** in de Excel-invoegtoepassing. Om een record te bewerken, selecteert u een cel in het werkblad en wijzigt u de celwaarde. Als u een nieuwe record wilt toevoegen, volgt u een van deze stappen:

-   Klik ergens in de gegevensbrontabel en klik vervolgens op **Nieuw** in de Excel-invoegtoepassing.
-   Klik in de laatste rij van de gegevensbrontabel en druk vervolgens op de Tab-toets totdat de cursor uit de laatste kolom van die rij wordt verplaatst en een nieuwe rij wordt gemaakt.
-   Klik in de rij direct onder de gegevensbrontabel en begin gegevens in te voeren in een cel. Wanneer u de focus uit die cel verplaatst, wordt de tabel uitgebreid met de nieuwe rij.
-   Klik op een van de velden voor veldbindingen van koptekstrecords en klik vervolgens op **Nieuw** in de Excel-invoegtoepassing.

Houd er rekening mee dat alleen een nieuwe record kan worden gemaakt als alle belangrijke en verplichte velden in het werkblad zijn gekoppeld of als standaardwaarden zijn ingevuld met behulp van de filtervoorwaarde.
Als u een record wilt verwijderen, volgt u een van deze stappen:

-   Klik met de rechtermuisknop op het rijnummer naast de rij in het werkblad die u wilt verwijderen en klik vervolgens op **Verwijderen**.
-   Klik met de rechtermuisknop in de rij in het werkblad die u wilt verwijderen en klik vervolgens op **Verwijderen** &gt; **Tabelrijen**.
Als gegevensbronnen als gerelateerd zijn toegevoegd, wordt de koptekst gepubliceerd vóór de regels. Als er afhankelijkheden zijn tussen andere gegevensbronnen, moet u wellicht de standaardpublicatievolgorde wijzigen. U wijzigt de publicatievolgorde door in de invoegtoepassing voor Excel op de knop **Opties** (het tandwielsymbool) te klikken. Klik vervolgens op het sneltabblad **Gegevensconnector** op **Publicatieorder configureren**.

## <a name="add-or-remove-columns"></a>Kolommen toevoegen of verwijderen
Met de ontwerper kunt u de kolommen aanpassen die automatisch worden toegevoegd aan het werkblad.

1.  Start de gegevensbronontwerper van de Excel-invoegtoepassing door te klikken op de knop **Opties** (het tandwielsymbool). Schakel vervolgens het selectievakje **Ontwerpen inschakelen** in.
2.  Klik op **Ontwerpen** in de Excel-invoegtoepassing. Alle gegevensbronnen worden vermeld.
3.  Klik naast de gegevensbron op de knop **Bewerken** (het potloodsymbool).
4.  Pas de lijst in de lijst **Geselecteerde velden** aan:
    -   Als u een veld uit de lijst **Beschikbare velden** wilt toevoegen aan de lijst **Geselecteerde velden**, klikt u op het gewenste veld en vervolgens op **Toevoegen**. U kunt ook dubbelklikken op het gewenste veld.
    -   Als u een veld wilt verwijderen, selecteert u het veld in de lijst tabblad **Geselecteerde velden** en vervolgens op **Verwijderen**. U kunt ook dubbelklikken op het gewenste veld.
    -   Als u de volgorde van velden wilt wijzigen, klikt u op het veld in de lijst **Geselecteerde velden** lijst en klikt u vervolgens op een veld en op **Omhoog** of **Omlaag**.

5. Pas uw wijzigingen toe op de gegevensbron door op **Bijwerken** te klikken. Klik daarna op **Gereed** om de ontwerper af te sluiten. 
6. Als u een veld (kolom) hebt toegevoegd, klikt u op **Vernieuwen** om een bijgewerkte set gegevens op te halen.

## <a name="troubleshooting"></a>Problemen oplossen
Er zijn enkele problemen die kunnen worden opgelost met enkele eenvoudige stappen.

-   **De knop Applets laden wordt getoond.** Als de Excel-invoegtoepassing een knop **Applets laden** toont nadat u zich hebt aangemeld, bent u waarschijnlijk niet aangemeld als de juiste gebruiker. Controleer of de juiste gebruikersnaam zichtbaar is in de rechterbovenhoek van het Excel-invoegtoepassing. Als een onjuiste gebruikersnaam wordt getoond, klikt u erop, meldt u zich af en vervolgens weer aan met de juiste gebruiker.
-   **U ontvangt een melding 'Verboden'.** Als u het foutbericht 'Verboden' krijgt wanneer de Excel-invoegtoepassing metagegevens laadt, is de account die is aangemeld bij de Excel-invoegtoepassing niet gemachtigd om de beoogde service, instantie of database te gebruiken. Controleer of de juiste gebruikersnaam zichtbaar is in de rechterbovenhoek van het Excel-invoegtoepassing. Als een onjuiste gebruikersnaam wordt getoond, klikt u erop, meldt u zich af en vervolgens weer aan met de juiste gebruiker.
-   **Een lege webpagina wordt weergegeven via Excel.** Als een lege webpagina wordt geopend tijdens het aanmelden, vereist de account AD FS maar is de versie van Excel waarin u de invoegtoepassing uitvoert niet recent genoeg om het aanmeldingsvenster weer te geven. Werk Excel bij naar een meer recente versie. Als u de versie van Excel wilt bijwerken wanneer u werkt in een onderneming die zich op het Deferred-kanaal bevindt, wijzigt u met het [hulpprogramma Office Deployment](https://technet.microsoft.com/library/jj219422.aspx) van [het Deferred-kanaal naar het Current-kanaal](https://technet.microsoft.com/library/mt455210.aspx).





