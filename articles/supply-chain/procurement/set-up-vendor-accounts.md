---
title: Leveranciersaccounts instellen
description: In dit onderwerp worden de soorten gegevens beschreven, die u moet opgeven wanneer u een nieuwe leverancieraccount maakt.
author: GalynaFedorova
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendBankAccounts, VendTable, VendOnHoldUpdate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 191053
ms.assetid: 06168199-7c54-40e9-a038-4eb274ca958d
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d524ff99cba733fdd607d9708abba440248d6cc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676969"
---
# <a name="set-up-vendor-accounts"></a>Leveranciersaccounts instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de soorten gegevens beschreven, die u moet opgeven wanneer u een nieuwe leverancieraccount maakt.

Wanneer u een leverancieraccount maakt, voert u informatie over de leverancier in. Deze informatie wordt gebruikt om automatisch gegevens in documenten in te voeren en activiteiten te volgen waarbij de leverancier is betrokken. U kunt bijvoorbeeld de volgende informatie voor een leverancier configureren:

-   Een leveranciersgroep toewijzen. Aan elk leverancier moet een leveranciersgroep worden toegewezen. Elke leverancier in een leveranciersgroep heeft parameters gemeenschappelijk met anderen. Ze kunnen bijvoorbeeld dezelfde betalingsvoorwaarden hebben.
-   Configureer de leveranciers voor het importeren van catalogi. De leveranciers kunnen een bestand aanleveren, dat de catalogus van hun artikelen en services bevat. Dit bestand kan worden geüpload, zodat uw werknemers bij de leverancier kunnen bestellen.
-   De everancier aan aanschaffingscategorieën toewijzen.
-   Toestaan dat een bestaande leverancier zaken doet met een andere rechtspersoon in uw organisatie.
-   Een leverancier in de wachtstand zetten (deactiveren) voor bepaalde typen transacties.
-   Bankgegevens voor de leverancier instellen zodat u betalingen elektronisch kunt verzenden.
-   BTW, levering, factuur- en betalingsgegevens voor de leverancier instellen. Standaard worden deze instellingen gekopieerd naar de nieuwe documenten die u voor de leverancier maakt.
-   Standaard financiële dimensies instellen die worden gebruikt voor het automatisch boeken van transacties met de leverancier naar financiële rekeningen.

Om het proces voor het aanmaken van leveranciersaccounts te versnellen, kunt u sjablonen maken. Om een sjabloon te maken, klikt u op de pagina **Leverancier** in het deelvenster Actie op **Opties** &gt; **Recordinfo**. Klik vervolgens op **Bedrijfsrekeningsjabloon**. De bedrijfsaccountjablonen worden gedeeld met andere gebruikers.  

U kunt ook een gebruikerssjabloon voor uw eigen gebruik maken. U kunt een leverancier niet verwijderen als deze aan andere records is gekoppeld, zoals contactpersonen en producten.

## <a name="vendor-account-numbers"></a>Leverancieraccountnummers
Het accountnummer is een unieke ID voor een leverancier. U kunt accountnummers zodanig configureren dat ze automatisch worden gegenereerd wanneer u een leverancier maakt. U kunt de nummerreeks ook zo configureren dat de accountnummers handmatig worden ingevoerd. U kunt bijvoorbeeld het telefoonnummer van de leverancier als ID gebruiken.

## <a name="vendor-organizations-and-individual-vendors"></a>Leveranciersorganisaties en individuele leveranciers
Wanneer u een nieuwe leverancieraccount maakt, moet u aangeven of de leverancier een persoon of een organisatie is. Uw selectie bepaalt welke informatie u voor de leverancier moet invullen. Voor een persoon omvat deze informatie de voornaam, de achternaam en de titel. Voor een organisatie omvat deze informatie het organisatienummer en het aantal werknemers.

## <a name="addresses"></a>Adressen
Voor elke leverancier kunt u meerdere adressen definiëren, elk waarvan voor een ander doel wordt gebruikt. U kunt bijvoorbeeld een adres maken met het doel **Factuur**. Of als u de leverancier betaalt met cheques, kunt u een alternatief adres instellen met het doel **Betalen aan**. Als u een adres moet opgeven voor geldoverboekingen naar buitenlandse banken, wordt het doel **SWIFT**.

## <a name="vendor-contacts"></a>Leveranciercontacten
U kunt contactpersonen opslaan voor een leverancier. Deze contactpersonen kunnen vervolgens voor documenten zoals inkooporders of offerteaanvragen (offerteaanvragen) worden gebruikt.  

Om contactpersonen voor een leverancier toe te voegen, gaat u naar de pagina **Alle leveranciers**. Op het tabblad **Leverancier** klikt u in de groep **Instellen** op **Contacten** &gt; **Contacten toevoegen**.  

U kunt leverancierscontactpersonen helemaal nieuw aanmaken. Maar u kunt ook details kopiëren van een andere persoon die al in Supply Chain Management is geregistreerd, en de informatie waar nodig bewerken.  

**Opmerking:** Een contactpersoon voor een leverancier toevoegen is niet hetzelfde als het toevoegen van contactgegevens voor die leverancier. Hoewel u algemene contactgegevens voor een leverancier kunt toevoegen, zijn er waarschijnlijk ook verschillende specifieke personen die optreden als contactpersonen voor dat bedrijf en die hun eigen contactgegevens hebben.  

U kunt een contactpersoon niet verwijderen als in een document naar deze contactpersoon wordt verwezen. In plaats daarvan kunt u de contactpersoon inactief maken.  

U kunt contactpersonen aan uw persoonlijke contacten in Microsoft 365 toevoegen. U moet echter eerst de synchronisatie instellen tussen Supply Chain Management en Microsoft 365, zowel in de Microsoft Exchange Server-synchronisatie als in de Microsoft Outlook-installatiewizard.

## <a name="vendors-in-different-legal-entities"></a>Leveranciers in verschillende rechtspersonen
Als een leverancier voor slechts één rechtspersoon in uw organisatie is geregistreerd en andere rechtspersonen dezelfde leverancier moeten registreren, kunt u op de pagina **Leverancier toevoegen aan andere rechtspersoon** de leverancier configureren om zaken te doen met een andere rechtspersoon. U moet een leveranciersgroep, valuta en wachtstand voor de leverancier selecteren in de geselecteerde rechtspersoon.  

Als meerdere rechtspersonen binnen uw organisatie zaken doen met dezelfde leverancier en elke rechtspersoon een afzonderlijke leverancieraccount onderhoudt voor die leverancier, kunt u de partij-ID's van de leverancieraccounts samenvoegen. Op deze manier kan informatie zoals het adres en het aantal werknemers worden gedeeld, zodat u deze slechts op één plaats moet bijwerken.  

Om partij-ID's samen te voegen, volgt u de volgende stappen.

1.  Op de pagina **Algemeen adresboek** selecteert u de adresboekrecords die de leverancier in elke rechtspersoon vertegenwoordigen en die in de toewijzing moeten worden opgenomen.
2.  Klik in het actievenster op **Records samenvoegen**.

## <a name="agreements"></a>Overeenkomsten
Wanneer u een leverancieraccount configureert, wilt u mogelijk ook de overeenkomsten registreren die u met de leverancier hebt afgesloten. U kunt prijs- en kortingsovereenkomsten instellen via de acties in de leverancierrecord. U kunt ook een inkoopovereenkomst instellen op de pagina **Inkoopovereenkomsten**.

## <a name="putting-a-vendor-on-hold"></a>Een leverancier in de wachtstand plaatsen
U kunt een leverancier in de wachtstand zetten voor diverse transactietypen. De volgende opties zijn beschikbaar:

-   **Nee**: de leverancier is voor geen enkel type transactie in de wachtstand geplaatst.
-   **Factuur**: voor de leverancier kunnen geen facturen worden gemaakt of geboekt.
-   **Alle**: De leverancier is voor alle transactietypes in de wachtstand geplaatst. Deze transactietypen zijn onder andere opdrachten tot inkoop, facturen en betalingen.
-   **Betaling**: er kunnen geen betalingen worden gegenereerd voor de leverancier.
-   **Inkoop**: Opdrachten tot inkoop kunnen niet worden gemaakt voor de leverancier en de inkoopregels die al zijn gemaakt voordat de leverancier in de wachtstand werd gezet, kunnen niet worden omgezet naar een inkooporder. De inkoopregels voor de leverancier worden geannuleerd als uw beleid is ingesteld op het automatisch maken van inkooporders.
-   **Nooit**: de leverancier wordt nooit inactief gemaakt.

Wanneer u een leverancier in de wachtstand zet, kunt u ook een reden opgeven en de datum waarop de wachtstandstatus eindigt. Als u geen einddatum invoert, blijft de blokkeringsstatus van de leverancier voor onbepaalde tijd actief.

U kunt bulksgewijs de wachtstandstatus **Alle** bijwerken voor leveranciers op basis van de geselecteerde criteria op de pagina **Deactivering leverancier** en een reden toewijzen waarom de leverancier in de wachtstand staat.

De volgende criteria worden gebruikt om leveranciers op te nemen die een periode niet actief zijn geweest, leveranciers op te nemen of uit te sluiten die werknemers zijn en leveranciers uit te sluiten waarvoor een respijtperiode geldt voor de volgende blokkering.

- Op basis van het aantal dagen dat u invoert in het veld **In activiteitperiode** op de pagina **Deactivering leverancier**, berekent de toepassing de laatste datum waarop de leverancier een activiteit moet hebben om als niet-actief te worden beschouwd. Dat is de huidige datum min het aantal dagen dat u invoert. Als er een of meer facturen zijn voor de leverancier waar de datum na de berekende datum valt, wordt de leverancier van de deactivering uitgesloten. Dit gedlt ook als de leverancier betalingen heeft na die datum, opestaande opdrachten tot inkoop, openstaande inkooporders, aanvragen voor offertes of antwoorden.
- Het aantal dagen in het veld **Respijttijd voor volgende blokkering** wordt gebruikt voor het berekenen van de laatste respijtdatum. Dat is de huidige datum min de dagen die u invoert. Dit geldt alleen voor leveranciers die eerder uitgeschakeld zijn geweest. In het geval van een eerdere deactivering controleert de toepassing de historie van andere deactiveringsgebeurtenissen van de leverancier en of de meest recente deactivering heeft plaatsgevonden vóór de laatste datum van de respijtperiode. Als dit het geval is, wordt de leverancier opgenomen in het deactiveringsproces.
- De parameter **Werknemers opnemen** verwijst naar de leveranciers die zijn gekoppeld aan een werknemer. U kunt instellen of u die werknemers wilt opnemen.

In dit proces worden altijd leveranciers uitgesloten voor wie de waarde in het veld **Blokkering van leverancier** op **Nooit** staat.

Leveranciers die voor de validaties slagen, worden in de wachtstand geplaatst. Daarmee wordt het veld **Blokkering van leverancier** op **Alle** ingesteld en wordt de **Reden** geselecteerd. Een record van de wachtstandgeschiedenis wordt gemaakt voor de leverancier.

## <a name="vendor-invoice-account"></a>Te factureren leverancierrekening
Als meerdere leveranciers hetzelfde factuuradres hebben, of als de leverancier via derden wordt gefactureerd, kunt u een factuuraccount opgeven in de leverancierrecord. De factuuraccount is de account waarnaar het factuurbedrag wordt gecrediteerd, wanneer u een leveranciersfactuur maakt op basis van een inkooporder. Als u geen factuuraccount invoert voor de leverancierrecord, wordt de leverancieraccount gebruikt als factuuraccount.

## <a name="vendor-bank-accounts"></a>Bankrekeningen van leverancier
Als u betalingen op een bankrekening van een leverancier moet overmaken, kunt u de gegevens van de bank en bankrekeningen van de leverancier invoeren op de pagina **Bankrekeningen van leverancier**. U kunt ook informatie invoeren voor validatie en betalingen voor de geselecteerde bankrekening. U kunt bijvoorbeeld voorafmeldingen aan de bankrekeningen van de leverancier toevoegen. Door middel van deze voorafmeldingen kan de juistheid van rekeninggegevens, zoals routenummers en rekeningnummers, worden gecontroleerd. U moet een standaardrekening voor betalingen aan de leverancier instellen. Maar wanneer u daadwerkelijk een betaling uitvoert, kunt u deze rekening wijzigen naar een van de andere rekeningen van de leverancier.

## <a name="ledger-accounts"></a>Grootboekrekeningen
U kunt de standaardrekeningen opgeven die automatisch in leveranciersfacturenjournalen voor de gespecificeerde leverancier worden weergegeven. Deze functionaliteit is handig als u normaal gesproken betalingen uitvoert voor dezelfde typen artikelen van dezelfde leveranciers. Wanneer u een standaardrekening opgeeft, kunt u journaalposten in het factuurjournaal snel en efficiënt invoeren. De opgegeven standaardrekeningen worden niet gebruikt voor inkooporders, of voor leveranciersfacturen die worden ingevoerd op de pagina **Leveranciersfactuur**.  

U selecteert standaardrekeningen op de pagina **Instellen van standaardaccount**. Deze opent u vanaf het tabblad **Factuur** in de leveranciersrecord. De in dit deelvenster geselecteerde rekeningen worden weergegeven in de gefilterde lijst met rekeningen voor de leverancieraccount, wanneer u een journaalpost invoert. U kunt een van de rekeningen instellen als de standaardrekening.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]