---
title: Gebruikersaccounts voor mobiele apparaten
description: In dit onderwerp wordt beschreven hoe u gebruikersaccounts instelt en beheert waarmee werknemers zich kunnen aanmelden en de magazijn-app kunnen gebruiken.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f3a930814a1fb98e3b1611adf309c10e66b49b9d
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902092"
---
# <a name="mobile-device-user-accounts"></a>Gebruikersaccounts voor mobiele apparaten

[!include [banner](../includes/banner.md)]

Telkens wanneer een medewerker de magazijnapp wil gebruiken, moet deze zich aanmelden met een gebruikersnaam en een wachtwoord. Aan elke werknemer in het systeem kan een willekeurig aantal gebruikers van een magazijnapp worden gekoppeld. Magazijnen zijn doorgaans gekoppeld aan elk van deze gebruikers van de magazijnapp. ook voor elke medewerker worden verschillende opties geconfigureerd om standaardinstellingen en andere instellingen op te geven die relevant zijn voor het gebruik van de magazijnapp.

## <a name="set-up-the-required-worker-and-employee-records"></a>De vereiste werknemer en werknemersrecords instellen

Voordat u gebruikers van magazijnapps kunt instellen, moet iedere werknemer al bestaan als een Supply Chain Management-werknemer of een medewerker in de module **Human Resources**.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Gebruikersaccounts voor mobiele apparaten instellen

Nadat de vereiste medewerkers en werknemers in Human Resources zijn ingesteld, kunt u gebruikers van de magazijnapp toewijzen aan elk van deze medewerkers en werknemers en andere opties instellen die van invloed zijn op de manier waarop ze de app kunnen gebruiken.

1. Ga naar **Warehouse Management \> Instellen \> Medewerker**.
1. Als u een bestaande medewerker wilt bewerken, selecteert u deze in het lijstvenster. Selecteer **Nieuw** in het actievenster om een nieuwe record toe te voegen.
1. Als u een nieuwe medewerker instelt, volgt u deze stappen:

    1. Selecteer in het veld **Medewerker** de doelgebruiker in de lijst met werknemers.
    1. Selecteer **Selecteren**.
    1. Selecteer **Opslaan** in het actievenster.

1. Er kan een standaardprofiel worden gebruikt om de magazijnmedewerker op het inpakstation te begeleiden bij het proces dat daar is vereist. U kunt het standaardprofiel ook gebruiken om de voorkeursprofielinstellingen voor de medewerker op te slaan. Stel op het sneltabblad **Profiel** de volgende velden in:

    - **Containerverpakkingsbeleid**: selecteer een containerverpakkingsbeleid dat bepaalt hoe containers op het inpakstation moeten worden verwerkt. Het containerverpakkingsbeleid dat hier wordt geselecteerd, wordt vooraf geselecteerd voor de medewerker wanneer ze het inpak openen. Zie het volgende blogbericht voor meer informatie: [Verbeterde inpakfunctionaliteit](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611) voor meer informatie.
    - **Verpakkingsprofiel-id**: selecteer een verpakkingsprofiel-id waarmee het verpakkingsbeleid en de containerinstellingen worden gedefinieerd die worden gebruikt. Als de geselecteerde verpakkingsprofiel-id is gekoppeld aan een containerverpakkingsbeleid, kunt u de instelling **Containerverpakkingsbeleid** op deze pagina niet wijzigen.

1. Stel op het sneltabblad **Standaard inpakstation** de volgende velden in om het standaard inpakstation te definiëren dat van toepassing is wanneer de werknemer zich aanmeldt. De werknemer kan nog steeds een ander inpakstation selecteren als dat nodig is.

    - **Site**: selecteer de site waar het standaard inpakstation zich bevindt.
    - **Magazijn**: selecteer het magazijn waar het standaard inpakstation zich bevindt.
    - **Locatie**: selecteer de locatie van het standaard inpakstation.

1. Op het sneltabblad **Gebruikers** kunt u elk willekeurig aantal gebruikersaccounts voor de magazijnapp maken voor de geselecteerde medewerker. Elk account is gekoppeld aan een specifiek magazijn of specifieke magazijnen. Gebruik de werkbalk om gebruikersaccounts toe te voegen of te verwijderen, het wachtwoord voor een geselecteerd account opnieuw in te stellen of magazijnen toe te wijzen aan een geselecteerd account. Stel voor elk gebruikersaccount de volgende velden in:

    - **Gebruikers-id**: voer een unieke id in.
    - **Gebruikersnaam**: voer een naam in voor de id.
    - **Standaardmagazijn**: stel het standaardmagazijn in waar de werknemer doorgaans werkt. U kunt de werkbalk gebruiken om extra magazijnen toe te wijzen en de medewerker kan schakelen tussen magazijnen met de indirecte activiteit **Magazijn wijzigen** van het menu-item van het mobiele apparaat.
    - **Menunaam**: selecteer het basismenu dat de beginpagina voor de medewerker is. Het is handig om een basismenu in te stellen voor elke werknemer, omdat u hiermee de menustructuur kunt bepalen die elke medewerker kan gebruiken. Het menu voor werknemers die bijvoorbeeld alleen in het gebied voor uitgaande bewerkingen actief zijn, kan worden afgestemd op taken die betrekking hebben op uitgaande bewerkingen voor dat gebied.
    - **Inactief**: een ingeschakeld selectievakje geeft aan dat het gebruikersaccount inactief is. Het gebruikersaccount wordt automatisch gedeactiveerd als een medewerker vijf keer achter elkaar het verkeerde wachtwoord in de magazijnapp invoert. U kunt dit selectievakje echter ook handmatig selecteren. Schakel het selectievakje uit om de gebruiker weer actief te maken.

1. Stel op het sneltabblad **Werk** de volgende velden in:

    - **Overschrijven van orderverzamellocatie toestaan**: stel deze optie in op *Ja* om de medewerker toe te staan de locatie voor orderverzamelingsstappen te overschrijven. Deze mogelijkheid kan handig zijn als de fysieke voorraad niet overeenkomt met de door het systeem voorgestelde locatie.
    - **Overschrijven van neerzetlocatie toestaan**: stel deze optie in op *Ja* om de medewerker toe te staan de locatie voor neerzetstappen te overschrijven. Deze mogelijkheid kan handig zijn als de voorgestelde neerzetlocatie momenteel vol is of niet beschikbaar of als klaarzetlocaties zijn gewijzigd.
    - **Meerverzameling voor verkoop toestaan**: stel deze optie in op *Ja* om de medewerker toe te staan om meer te verzamelen bij het verzamelen van verkooporders. Zie [Meerverzameling voor verkooporders en transferorders](over-picking-for-sales-and-transfer-orders.md) voor meer informatie.
    - **Meerverzameling voor transferorder toestaan**: stel deze optie in op *Ja* om de medewerker toe te staan om meer te verzamelen bij het verzamelen van transferorders. Zie [Meerverzameling voor verkooporders en transferorders](over-picking-for-sales-and-transfer-orders.md) voor meer informatie.
    - **Mutatie van voorraad met gekoppeld werk toestaan**: stel deze optie in op *Ja* om de medewerker toe te staan om voorraad te verplaatsen die al is gereserveerd of al aan ander werk is gekoppeld. Zie [Mutatie van voorraad met gekoppeld werk in Warehouse Management](move-inventory-associated-work.md) voor meer informatie.
    - **Handmatige artikelhertoewijzing toestaan**: stel deze optie in op *Ja* om handmatige hertoewijzing voor de medewerker in te schakelen tijdens kort orderverzamelen. Met artikelhertoewijzing worden medewerkers geleidt om voorraad te verzamelen van een andere locatie. Hoewel automatische hertoewijzing beschikbaar is voor alle medewerkers, moet handmatige hertoewijzing expliciet voor een werknemer worden ingesteld. De mogelijkheid om handmatige hertoewijzing voor elke medewerker te beheren kan nuttig zijn, omdat u hiermee de zichtbaarheid kunt beheren die elke medewerker heeft wanneer het verzamelen van artikelen uit het quarantaine- of bulkgebied is beperkt tot vertrouwde medewerkers. Zie het volgende blogbericht voor meer informatie: [Automatische en handmatige hertoewijzing van artikelen tijdens kort verzamelen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **Is een cyclustellingssupervisor**; stel deze optie in op *Ja* om van de medewerker een cyclustellingssupervisor te maken. In dit geval worden alle cyclustellingen die door de medewerker in de magazijnapp worden uitgevoerd, onmiddellijk goedgekeurd. Met de velden **Maximale percentagelimiet**, **Maximale hoeveelheidslimiet** en **Maximale waardelimiet** wordt geen rekening gehouden voor medewerkers voor wie deze optie is ingesteld op *Ja*.
    - **Maximale percentagelimiet**: voer de hoogste percentagelimiet in die een cyclustelling mag verschillen van de verwachte telling zonder dat er goedkeuring nodig is van een cyclustellingssupervisor.
    - **Maximale hoeveelheidslimiet**: voer de totale hoeveelheid in die de ingevoerde hoeveelheid kan verschillen van de verwachte hoeveelheid (in eenheden) zonder dat er goedkeurig nodig is van een cyclustellingssupervisor.
    - **Maximale waardelimiet**: voer de maximale waarde in die de kosten van de voorraad mag verschillen van de verwachte kosten zonder dat er goedkeuring nodig is van een cyclustellingssupervisor.

1. Selecteer **Opslaan** in het actievenster.
1. Als u een nieuwe gebruiker hebt toegevoegd, wordt het dialoogvenster **Wachtwoord instellen** weergegeven. In dit venster kunt u een eenvoudig wachtwoord maken dat de gebruiker kan gebruiken om zich aan te melden bij de mobiele app. Voer het eenvoudige wachtwoord twee keer in en selecteer vervolgens **Wachtwoord opslaan** om door te gaan.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>De taal, getalnotaties en tijdzone instellen voor elke gebruiker van de magazijnapp

Wanneer een medewerker zich aanmeldt bij de mobiele app Warehouse Management, worden de taal, getalnotaties en tijdzone gewijzigd zodat deze overeenkomen met de voorkeuren van die medewerker. De accountinstellingen voor de medewerker die is geselecteerd in stap 3 in de sectie [Gebruikersaccounts voor mobiele apparaten instellen](#set-wma-users) bepalen welke instellingen worden gebruikt. Als u afzonderlijke instellingen voor elke gebruiker nodig hebt, gebruikt u verschillende medewerkersaccounts. In de volgende procedure wordt getoond hoe u de taal, getalnotaties en tijdzone wijzigt voor elke gebruiker van de magazijnapp.

1. Ga naar **Warehouse Management \> Instellen \> Medewerker**.
1. Zoek naar de naam van de medewerker die u wilt instellen. Zorg ervoor dat de medewerker over alle vereiste gebruikersaccounts voor de magazijnapp beschikt die op het sneltabblad **Gebruikers** worden weergegeven. Maak een nieuwe medewerker en/of voeg indien nodig gebruikersaccounts voor de magazijnapp toe door de stappen in de sectie [Gebruikersaccounts voor mobiele apparaten instellen](#set-wma-users) te volgen.
1. Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.
1. Selecteer de gebruikersaccount waarbij in de kolom **Persoon** de naam van de medewerker wordt weergegeven die u in stap 2 hebt gevonden.

    > [!IMPORTANT]
    > De waarden voor **Gebruikers-id** die op de pagina **Gebruikers** worden weergegeven, zijn *niet* gerelateerd aan de waarde die wordt weergegeven op het sneltabblad **Gebruikers** van de pagina **Medewerker** die u in stap 1 hebt geopend.

1. Selecteer **Gebruikersopties** in het actievenster.
1. Stel op het tabblad **Voorkeuren** de volgende velden in:

    - **Taal**: selecteer de voorkeurstaal van de medewerker. Dit veld bepaalt ook de datumnotatie die wordt weergegeven in de magazijnapp.
    - **Datum, tijd en getalnotatie**: selecteer de taal die de getalnotaties bepaalt die worden weergegeven in de magazijnapp. De datum- en tijdnotaties die worden weergegeven in de magazijnapp, worden feitelijk bepaald door het veld **Taal** en niet door dit veld.
    - **Tijdzone**: selecteer de tijdzone waarin de medewerker werkt. Dit veld is van invloed op het tijdstempel voor alle registraties die de medewerker maakt met de app.

> [!NOTE]
> In sommige gevallen kan de magazijnapp geen specifieke medewerkersinstellingen vinden waarmee de taal, getalnotaties en tijdzone worden bepaald. De volgende regels zijn van toepassing:
>
> - Als de app niet is verbonden met een Supply Chain Management-omgeving (bijvoorbeeld de eerste keer dat de app wordt gestart nadat deze is geïnstalleerd), wordt de taal van het lokale apparaat gebruikt. Wanneer de taal van het apparaat verandert, wordt de taal van de app ook gewijzigd. Zie de documentatie van uw apparaat en/of besturingssysteem voor meer informatie over het configureren van de taal voor het lokale apparaat.
> - Als de app is verbonden met een Supply Chain Management-omgeving zonder dat er voorkeuren zijn ingesteld voor de aangemelde medewerker, worden de taal, getalnotaties en tijdzone geselecteerd op basis van het account dat is gekoppeld aan de client-id die het apparaat gebruikt om verbinding te maken met Supply Chain Management. Zie [Een gebruikersaccount maken en configureren in Supply Chain Management](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Als u ziet dat er onjuiste tijdstempels worden weergegeven voor registraties die worden gemaakt met de magazijnapp, moet u wellicht de tijdzone aanpassen die is ingesteld voor het gebruikersaccount dat werknemers gebruiken om zich aan te melden en/of te verifiëren bij Supply Chain Management. Zoals eerder is aangegeven, is de tijdzone-instelling mogelijk afkomstig van het gebruikersaccount dat wordt gebruikt om zich aan te melden bij de magazijnapp, zoals is ingesteld op de pagina **Medewerker**. Als het gebruikersaccount niet is ingesteld op de pagina **Medewerker**, is de tijdzone afkomstig van het gebruikersaccount dat is gekoppeld aan de client-id die voor verificatie wordt gebruikt, zoals is ingesteld op de pagina **[Azure Active Directory-toepassingen](install-configure-warehouse-management-app.md)**.
