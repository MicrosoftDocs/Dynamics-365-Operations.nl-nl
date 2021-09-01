---
title: Veelgestelde vragen over adresboeken
description: Dit onderwerp bevat antwoorden op veelgestelde vragen met betrekking tot de adresboeken.
author: msftbrking
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5809d4a29c4209d8fb42bdfd441a3a4fb201ca6c6318abc0315a02ead7c551de
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759156"
---
# <a name="address-books-faq"></a>Veelgestelde vragen over adresboeken

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Hoe controleer ik op dubbele registraties?

U kunt op dubbele registraties controleren vanuit de lijstpagina **Algemeen adresboek**. Klik in het actievenster op het tabblad **Partij** in de groep **Onderhouden** op **Controleren op duplicaten**. Selecteer vervolgens de waarden die u in de controle op dubbele items wilt opnemen.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Kan ik partijregistraties bulksgewijs toevoegen aan of verwijderen uit een adresboek?

Ja, u kunt meerdere partijregistraties toevoegen aan en verwijderen uit een adresboek.

- Als u meerdere partijregistraties wilt toevoegen aan een adresboek, selecteert u op de lijstpagina **Algemeen adresboek** de partijen in de lijst. Klik in het actievenster op het tabblad **Partij** in de groep **Onderhouden** op **Partijen toewijzen**. Selecteer de adresboeken waaraan de geselecteerde partijregistraties moeten worden toegevoegd en klik op **OK**. Alle geselecteerde partijregistraties worden toegevoegd aan de geselecteerde adresboeken.
- Als u meerdere partijregistraties wilt verwijderen uit een adresboek, selecteert u op de lijstpagina **Algemeen adresboek** de partijen in de lijst. Klik in het actievenster op het tabblad **Partij** in de groep **Onderhouden** op **Partijen verwijderen**. Selecteer de adresboeken waaruit de partijen moeten worden verwijderd en klik vervolgens op **OK**. Alle geselecteerde partijregistraties worden verwijderd uit de geselecteerde adresboeken.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Kan ik het partijtype van een registratie wijzigen of moet ik de oude registratie verwijderen en een nieuwe registratie maken?

Het kan voorkomen dat u het partijtype van een registratie van persoon in organisatie of van organisatie in persoon moet wijzigen. Nancy is bijvoorbeeld lid van het verkoopteam voor Fabrikam, Groot-Brittannië Ze ontmoet zes nieuwe prospecten op een beurs in Londen. Nancy maakt een prospect partijregistratie voor elke prospect aan. Als Nancy de registraties opslaat, wordt elke registratie ook in het algemene adresboek gemaakt. Fabrikam heeft het standaardpartijtype op organisatie ingesteld, maar twee van de nieuwe prospects moeten het registratietype persoon hebben. Daarom moet Nancy het partijtype van de twee prospectrecords wijzigen wanneer ze terugkeert van de beurs. Als u het type van een partijregistratie wilt wijzigen, moet u eerst een nieuwe partijregistratie van het juiste type in het algemene adresboek maken. U koppelt vervolgens de oude partijregistratie aan deze nieuwe registratie. Nadat u de nieuwe partijkoppeling hebt gemaakt, verwijdert u de oorspronkelijke partijregistratie met het onjuiste registratietype.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Hoe wijzig ik de naam of het adres van een partijregistratie?

U kunt de naam van een partijregistratie en de bijbehorende adressen op elk moment bijwerken.

- Als u de naam van een partijregistratie wilt bijwerken, opent u de partijregistratie en klikt u in het actievenster op **Bewerken**. Op het sneltabblad **Algemeen** voert u de nieuwe naam voor de partij in en vervolgens slaat u de registratie op.
- Als u een adres voor een partijregistratie wilt bijwerken, opent u de partijregistratie en selecteert u op het sneltabblad **Adressen** de adressen die u wilt bijwerken. Klik op **Bewerken** en voer op de pagina **Adres bewerken** de vereiste wijzigingen in het adres of de adresparameters door.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Kan ik twee of meer partijregistraties samenvoegen in één registratie?

Soms wilt u mogelijk twee of meer partijregistraties in één registratie samenvoegen. Dit kan gebeuren als u, bewust of per ongeluk, een of meer dubbele partijregistraties maakt. Wanneer u partijregistraties samenvoegt, selecteert u één registratie die u wilt houden. De informatie uit de overige registraties wordt dan in deze registratie samengevoegd. Stel dat u ontdekt dat gegevens over Fabrikam in drie partijregistraties zijn opgeslagen die A, B en C heten. U wilt partijregistratie A houden. De gegevens in partijregistraties B en C worden dan samengevoegd in partijregistratie A. In sommige situaties kunt u partijregistraties niet samenvoegen:

- U kunt partijregistraties niet samenvoegen als ze aan dezelfde partijrol zijn gekoppeld, zoals een klant of leverancier in dezelfde rechtspersoon. Partij A is bijvoorbeeld gekoppeld aan een klant in rechtspersoon 123 en partij B is gekoppeld aan een andere klant in rechtspersoon 123. Deze partijregistraties kunnen niet worden samengevoegd, omdat de samengevoegde partijrecord aan meerdere klanten in dezelfde rechtspersoon zou zijn gekoppeld, wat niet is toegestaan. De registraties kunnen echter wel worden gekoppeld als partij B is gekoppeld aan een leverancier in rechtspersoon 123 of een klant in een andere rechtspersoon.
- U kunt interne partijorganisatieregistraties niet samenvoegen in dezelfde rechtspersoon, operationele eenheid of hetzelfde team.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Moet ik een partijregistratie in het algemene adresboek maken of ergens anders, zoals de pagina klant of Leverancier?

U kunt partijregistraties invoeren in het algemene adresboek of op de pagina van de betreffende rechtspersoon. Wanneer u een registratie op één locatie toevoegt, wordt dezelfde registratie altijd ook op de andere locatie toegevoegd. Als u een partijregistratie voor een klant in het algemene adresboek toevoegt, wordt de registratie bijvoorbeeld ook toegevoegd op de pagina **Klant**. En als u een partijregistratie voor een klant op de pagina **Klant** toevoegt, wordt de registratie ook toegevoegd in het algemene adresboek. Gebruik de volgende richtlijnen om te bepalen waar u nieuwe partijregistraties moet invoeren:

- **Een partijregistratie maken als u het type rechtspersoon niet weet** – Als u een partijregistratie moet maken en het type rechtspersoon niet weet (bijvoorbeeld als u niet weet of het een klant of verkoopkans is), maakt u de registratie in het algemene adresboek. U kunt het entiteittype later selecteren.
- **Een partijregistratie maken wanneer u het type rechtspersoon weet** – Als u het type rechtspersoon voor de partij weet, kunt u een registratie maken op de betreffende pagina voor dat type. Voor een klant maakt u bijvoorbeeld een registratie op de pagina **Klant**. Wanneer u een registratie maakt en opslaat via de betreffende pagina, wordt de record ook automatisch gemaakt in het algemene adresboek.

## <a name="can-i-translate-address-information-for-party-records"></a>Kan ik adresgegevens voor partijregistraties vertalen?

U kunt vertalingen van adresgegevens zo instellen dat u de gegevens in uw gebruikerstaal (systeemtaal) kunt bekijken in uw programma, terwijl de gegevens in documenten, zoals verkooporders, in een andere taal worden weergegeven. U kunt vertalingen invoeren voor landen/regionamen, adresdoeleinden en naamvolgordes. Stel dat uw systeemtaal Deens is en u een verkooporder voor een klant in Frankrijk maakt. In dit geval kunt u de klantregistratie in het programma in het Deens weergeven, maar worden de adresgegevens in het Frans weergegeven op de afgedrukte verkooporder. Als u vertalingen instelt, moet u een vertaling voor elk artikel in de lijst invoeren. Elk artikel waarvoor u geen vertaling invoert, verschijnt in de systeemtaal. Als uw systeemtaal bijvoorbeeld Deens is, en u verstuurd een document naar een klant in Spanje. Als u geen Spaanse (ESP) vertalingen voor de adresgegevens hebt ingevoerd, worden die gegevens zowel in het programma als op het afgedrukte document in het Deens weergegeven.

## <a name="after-importing-addresses-when-i-access-the-records-why-am-i-unable-to-edit-imported-addresses"></a>Waarom kan ik geïmporteerde adressen niet bewerken wanneer ik na het importeren van de adressen de records open?

Bij het importeren van adressen is er een veld met de naam **IsLocationOwner**, waarmee wordt aangegeven of de partij die aan de locatie (adres) is gekoppeld, de eigenaar van het adres is. Als de partij de eigenaar van het adres is, kan het adres worden bewerkt wanneer het wordt geopend door de partij in het globale adresboek of vanuit het hoofdrecordformulier (zoals klant, leverancier of medewerker). Als de partij niet de eigenaar van het adres is, kan de record niet worden bewerkt vanuit de eerder vermelde formulieren. Bij het importeren van adressen moet **IsLocationOwner** worden ingesteld op **Ja** als u wilt dat het adres kan worden bewerkt met de gekoppelde partij. Soms wordt dit veld echter onjuist geïmporteerd. Om dit probleem op te lossen, kan de eigenaar van de locatie worden bijgewerkt in het globale adresboek van de partijrecord of via de pagina **Locatie-eigenaars bevestigen**. Als u een enkele partijrecord wilt bijwerken, gaat u naar **Globaal adresboek > Adres**. Selecteer **Bewerken** om de pagina **Adres bewerken** te starten om de eigenaar van de locatie te wijzigen. Selecteer **Locatie-eigenaar wijzigen** om de vorige locatie-eigenaar weer te geven met de geselecteerde partij als nieuwe eigenaar van de locatie. Als de vorige locatie-eigenaar leeg is, betekent dit dat er nog geen locatie-eigenaar is ingesteld. Als u de optie **Geavanceerd** selecteert, wordt de pagina **Adressen beheren** geopend waarop de eigenaar van de locatie eveneens kan worden ingesteld. Selecteer de locatie die u wilt laten bijgewerken en selecteer vervolgens **Locatie-eigenaar instellen** in het menu. Als u de locatie-eigenaar voor meerdere records wilt bijwerken, gaat u naar **Globaal adresboek > Locaties > Locatie-eigenaars bevestigen**. De lijst bevat locaties die aan een enkele partij zijn gekoppeld, maar die partij is niet de eigenaar. Als u **Eigenaar bevestigen** selecteert, wordt de **id van de voorgestelde eigenaar van de partij** ingesteld op de eigenaar van het gekoppelde adres. Nadat de partij is ingesteld als eigenaar, kan het gekoppelde adres worden bewerkt vanuit de partijrecord. Als u de eigenaar van de locatie wilt wijzigen, moet aan u de bevoegdheid **Locatie-eigenaar instellen** zijn toegewezen op de pagina **Beveiligingsconfiguratie**.  De systeembeheerder krijgt deze bevoegdheid standaard toegewezen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

