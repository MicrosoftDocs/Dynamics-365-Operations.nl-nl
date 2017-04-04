---
title: Gebruik het Excel-invoegtoepassing
description: In dit onderwerp wordt uitgelegd hoe entiteitsgegevens in Microsoft Excel openen en vervolgens bekijken, bijwerken en de gegevens bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel. U opent de entiteitsgegevens, kunt u starten vanuit Excel of Microsoft Dynamics 365 voor bewerkingen.
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Gebruik het Excel-invoegtoepassing

In dit onderwerp wordt uitgelegd hoe entiteitsgegevens in Microsoft Excel openen en vervolgens bekijken, bijwerken en de gegevens bewerken met behulp van de Microsoft Dynamics Office-invoegtoepassing voor Excel. U opent de entiteitsgegevens, kunt u starten vanuit Excel of Microsoft Dynamics 365 voor bewerkingen.

Als u entiteitsgegevens in Microsoft Excel opent, kunt u snel en eenvoudig weergeven en bewerken van de gegevens via de Microsoft Dynamics Office-invoegtoepassing voor Excel. Deze invoegtoepassing moet Microsoft Excel 2016. **opmerking:** als uw pachters Microsoft Azure Active Directory (AD Azure) is geconfigureerd voor het gebruik van Active Directory Federation Services (AD FS), moet u ervoor zorgen dat de mei 2016-update is toegepast, zodat de Excel-invoegtoepassing kunt correct aanmelden.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Entiteitsgegevens in Excel geopend bij het starten van Dynamics 365 for Operations
1.  Klik op een pagina in Microsoft Dynamics 365 voor bewerkingen op **openen in Microsoft Office**. Als de hoofdgegevensbron (tabel) voor de pagina gelijk aan de hoofdgegevensbron voor alle entiteiten is, standaard **openen in Excel** opties voor de pagina worden gegenereerd. **Open in Excel** opties kunnen u vinden op veelgebruikte pagina's, zoals **alle leveranciers** en **alle klanten**.
2.  Klik op een **in Excel geopend** optie en open de werkmap die wordt gegenereerd. Deze werkmap heeft bindende gegevens voor de entiteit, een verwijzing naar uw omgeving en een verwijzing naar de Excel-invoegtoepassing.
3.  In Excel, klikt u op **bewerken inschakelen** waarmee de Excel-invoegtoepassing moet worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4.  Als u de Excel-invoegtoepassing voor de eerste keer uitvoert, klikt u op **deze invoegtoepassing vertrouwt**.
5.  Als u wordt gevraagd aan te melden, klikt u op **inloggen**, en meld u vervolgens aan met behulp van dezelfde referenties die u gebruikt voor aanmelding bij Dynamics 365 for Operations. De Excel-invoegtoepassing gebruikt een vorige teken in context vanuit Internet Explorer en automatisch aanmelden, als dat mogelijk is. Controleer daarom of de gebruikersnaam in de rechterbovenhoek van het Excel-invoegtoepassing.

De Excel-invoegtoepassing leest automatisch de gegevens voor de entiteit die u hebt geselecteerd. Houd er rekening mee dat er geen gegevens in de werkmap worden totdat wordt gelezen in de Excel-invoegtoepassing.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Entiteitsgegevens in Excel geopend bij het starten van Excel
1.  In Excel op de **invoegen** tabblad in het **Add-ins** groep, klikt u op **winkel** de Office-winkel wilt openen.
2.  In de winkel Office het trefwoord 'Dynamics', en klik op **Add** naast de **Microsoft Dynamics Office-invoegtoepassing** (de Excel-invoegtoepassing).
3.  Als u de Excel-invoegtoepassing voor de eerste keer uitvoert, klikt u op **deze invoegtoepassing vertrouwt** zodat de Excel-invoegtoepassing moet worden uitgevoerd. De Excel-invoegtoepassing wordt uitgevoerd in een deelvenster aan de rechterkant van het Excel-venster.
4.  Klik op **servergegevens toevoegen** opent de **opties** deelvenster.
5.  De browser-URL van uw doel Dynamics 365 voor bewerkingen exemplaar kopiëren en plakken, deze in de **Server-URL** veld en verwijdert u alle informatie na de hostnaam (bijvoorbeeld verwijderen **/? cmp = usmf & mi = CustTableListPage**). De resulterende URL moet de host-naam (bijvoorbeeld **https://xxx.dynamics.com**).
6.  Klik op **OK**, en klik vervolgens op **Ja** de wijziging te bevestigen. De Excel toevoegen opnieuw opstarten en metagegevens worden geladen. De **ontwerp** knop is nu beschikbaar. Als de Excel-invoegtoepassing heeft een **Laad toepassingen** knop, u waarschijnlijk niet zijn aangemeld als de juiste gebruiker. Zie 'de knop laden invoegtoepassingen weergegeven' in de sectie 'Problemen oplossen' van dit onderwerp voor meer informatie.
7.  Klik op **ontwerp**. De Excel-invoegtoepassing haalt entiteit metagegevens.
8.  Klik op **tabel toevoegen**. Een lijst met entiteiten weergegeven. De entiteiten worden weergegeven in de indeling 'Label naam:'.
9.  Selecteer een entiteit in de lijst, zoals **klant - klanten**, en klik vervolgens op **volgende**.
10. Toevoegen van een veld uit de **beschikbare velden** lijst aan de **velden geselecteerd** lijst, klik op het veld en klik vervolgens op **toevoegen**. Ook dubbelklikken op het veld.
11. Nadat u de gewenste velden hebt toegevoegd de **velden geselecteerd** lijst, zorgen dat de cursor op de juiste plaats in het werkblad (bijvoorbeeld cel A1) en klik vervolgens op **doen**. Klik vervolgens op **doen** om af te sluiten van de ontwerper.
12. Klik op **vernieuwen** ophalen van gegevens.

## <a name="view-and-update-entity-data-in-excel"></a>Gegevens van de entiteit wilt weergeven en bijwerken in Excel
Nadat u de Excel-invoegtoepassing leest entiteitsgegevens in de werkmap, kunt u de gegevens op elk gewenst moment bijwerken door te klikken op **vernieuwen** in de Excel-invoegtoepassing.

## <a name="edit-entity-data-in-excel"></a>Entiteitsgegevens in Excel bewerken
Wijzigt u entiteitsgegevens die u nodig en deze vervolgens publiceren weer door te klikken op **publiceren** in de Excel-invoegtoepassing. Een record bewerken, selecteer een cel in het werkblad en wijzig de celwaarde. Als u wilt een nieuwe record toevoegt, volgt u een van deze stappen:

-   Klik ergens in het werkblad en klik vervolgens op **New** in de Excel-invoegtoepassing.
-   Klik in de laatste rij van het werkblad en druk vervolgens op de Tab-toets totdat de cursor uit de laatste kolom van die rij verplaatst en een nieuwe rij wordt gemaakt.
-   Klik in de rij direct onder het werkblad en beginnen met het invoeren van gegevens in een cel. Wanneer u de focus uit die cel verplaatst, uitgebreid het werkblad met de nieuwe rij.

Als u wilt een record verwijdert, volgt u een van deze stappen:

-   Met de rechtermuisknop op het rijnummer naast de rij in het werkblad wilt verwijderen en klik vervolgens op **verwijderen**.
-   Met de rechtermuisknop in de rij in het werkblad wilt verwijderen en klik vervolgens op **verwijderen**&gt;**tabelrijen**.

## <a name="add-or-remove-columns"></a>Kolommen toevoegen of verwijderen
U kunt de ontwerper gebruiken als u de kolommen die automatisch worden toegevoegd aan het werkblad.

1.  De ontwerper van de bron van de invoegtoepassing voor Excel starten door te klikken op de **opties** knop (het symbool van de versnelling) en vervolgens te klikken op de **ontwerp schakelen** selectievakje.
2.  Klik op **ontwerp** in de Excel-invoegtoepassing. Alle gegevensbronnen worden weergegeven.
3.  Naast de gegevensbron, klikt u op de **bewerken** knop (het potloodsymbool).
4.  Aanpassen van de lijst in de **velden geselecteerd** als u nodig hebt:
    -   Toevoegen van een veld uit de **beschikbare velden** lijst aan de **velden geselecteerd** lijst, klik op het veld en klik vervolgens op **toevoegen**. Ook dubbelklikken op het veld.
    -   Als u wilt verwijderen van een veld uit de **velden geselecteerd** lijst, klik op het veld en klik vervolgens op **verwijderen**. Ook dubbelklikken op het veld.
    -   De volgorde van velden, klikt u op het veld in de **velden geselecteerd** lijst en klik vervolgens op **van** of **omlaag**.

5.  De wijzigingen toepassen op de gegevensbron door te klikken op **Update**. Klik vervolgens op **doen** om af te sluiten van de ontwerper. Als u een veld (kolom) toegevoegd, klikt u op **vernieuwen** ophalen van een bijgewerkte set gegevens.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Er zijn enkele problemen die kunnen worden opgelost door enkele eenvoudige stappen.

-   **De knop laden invoegtoepassingen wordt weergegeven.** Als de Excel-invoegtoepassing heeft een **Laad toepassingen** knop na inloggen, u waarschijnlijk niet zijn aangemeld als de juiste gebruiker. Controleer of de juiste gebruikersnaam verschijnt in de rechterbovenhoek van het Excel-invoegtoepassing dit probleem op te lossen. Als een onjuiste gebruikersnaam wordt weergegeven, klikt u erop, meldt u af en vervolgens opnieuw aanmelden.
-   **U ontvangt een bericht ''.** Als het foutbericht '' weergegeven wanneer de Excel-invoegtoepassing wordt geladen metagegevens, de rekening die is aangemeld bij de Excel-invoegtoepassing niet gemachtigd om te gebruiken de beoogde service, de instantie of de database. Controleer of de juiste gebruikersnaam verschijnt in de rechterbovenhoek van het Excel-invoegtoepassing dit probleem op te lossen. Als een onjuiste gebruikersnaam wordt weergegeven, klikt u erop, meldt u af en vervolgens opnieuw aanmelden.
-   **Een lege webpagina wordt weergegeven via Excel.** Als een lege webpagina wordt geopend tijdens het aanmelden, wordt de account is vereist voor AD FS, maar de versie van Excel met de invoegtoepassing niet recent genoeg om te laden in het dialoogvenster aanmelden. Werk de versie van Excel die u gebruikt dit probleem op te lossen. Gebruiken om te werken de versie van Excel in een onderneming die zich op het uitgestelde kanaal, de [Office deployment tool](https://technet.microsoft.com/library/jj219422.aspx) naar [van de uitgestelde kanaal verplaatsen naar het huidige kanaal](https://technet.microsoft.com/library/mt455210.aspx).



