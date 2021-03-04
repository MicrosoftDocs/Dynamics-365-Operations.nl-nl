---
title: Overzicht van clienteling
description: Dit onderwerp biedt een overzicht van de nieuwe clienteling-functies die beschikbaar zijn in de winkeltoepassing.
author: bebeale
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: d76668fa16a7634e7fbd953afaa6c89eed5457a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411372"
---
# <a name="clienteling-overview"></a>Clientelingoverzicht

[!include [banner](includes/banner.md)]


Veel detailhandelaren, vooral gespecialiseerde detailhandelaren met hoogwaardige producten, willen dat hun verkoopmedewerkers langdurige relaties aangaan met hun belangrijkste klanten. Van de medewerkers wordt verwacht dat zij op de hoogte zijn van waar deze klanten van houden en waar zij niet van houden, hun inkoophistorie, productvoorkeuren en belangrijke datums, zoals jubilea en verjaardagen. Verkoopmedewerkers moeten over een locatie beschikken waar zij deze informatie kunnen vastleggen en gemakkelijk terugvinden wanneer deze nodig is. Als deze informatie in één weergave beschikbaar is, kunnen de verkoopmedewerkers zich op eenvoudige wijze op klanten richten die aan bepaalde criteria voldoen. Zo kunnen ze bijvoorbeeld alle klanten vinden die op zoek zijn naar handtasjes of klanten die voor een belangrijke gebeurtenis staan, zoals een verjaardag of jubileum.

## <a name="client-book"></a>Klantenboek

In Microsoft Dynamics 365 Commerce kunnen detailhandelaren de klantenboekfunctionaliteit gebruiken om winkelmedewerkers te helpen langdurige relaties op te bouwen met belangrijke klanten.

Het klantenboek bevat klantkaarten die contactgegevens voor elke klant weergeven, samen met drie aanvullende eigenschappen die door de detailhandelaar zijn gedefinieerd en geconfigureerd in Headquarters. Detailhandelaren kunnen de drie belangrijkste zaken kiezen die verkoopmedewerkers moeten weten over klanten. Zo kan bijvoorbeeld een sieradenwinkel belangrijke datums, zoals jubilea of verjaardagen, opnemen, omdat deze datums gelegenheden zijn waarbij mensen mogelijk sieraden willen kopen. Evenzo kan een detailhandelaar in een modezaak de interesses en merken opnemen waar de klant de voorkeur aan geeft.

Het klantenboek stelt verkoopmedewerkers tevens in staat de lijst te filteren, zodat alleen klanten worden weergegeven die aan bepaalde criteria voldoen. Stel bijvoorbeeld dat een nieuwe collectie schoenen is aangekomen in de winkel en dat een verkoopmedewerker klanten wil informeren die graag schoenen willen kopen. In dat geval kan de medewerker het klantenboek filteren om de relevante klanten te vinden en vervolgens verdere actie ondernemen.

Als klanten om een bepaalde reden niet meer als belangrijke klanten worden beschouwd en daarom niet nauwkeurig hoeven te worden beheerd, kunnen verkoopmedewerkers hun uit hun klantenboek verwijderen.

Sommige detailhandelaren willen geen klanten beheren op het niveau van de verkoopmedewerker. In plaats daarvan willen zij een lijst met belangrijke klanten op het winkelniveau beheren. Deze detailhandelaren kunnen klanten weergeven vanuit winkelklantenboeken. Met deze optie kunnen detailhandelaren de klanten bekijken uit de klantenboeken van alle verkoopmedewerkers wier adresboek overeenkomt met het adresboek van de huidige winkel. Op deze manier worden, als een verkoopmedewerker in verschillende winkels van de rechtspersoon werkt, de klanten van al deze winkels in het klantenboek weergegeven. Deze functionaliteit ondersteunt extra mogelijkheden. Zo kunnen klanten bijvoorbeeld opnieuw worden toegewezen van de ene medewerker aan een andere. Deze mogelijkheid is nuttig wanneer medewerkers worden overgeplaatst of het bedrijf verlaten.

Elke verkoopmedewerker kan één klantenboek per rechtspersoon hebben en verkoopmedewerkers kunnen een of meer klanten aan hun klantenboek toevoegen. In Commerce kan elke klant momenteel aan slechts één klantenboek worden toegevoegd. Microsoft wil echter functionaliteit toevoegen waarmee een enkele klant aan meerdere klantenboeken kan worden toegevoegd.

> [!NOTE]
> In tegenstelling tot in de zoekfunctie voor klanten, worden klantrecords niet gefilterd op basis van de adresboeken van de winkel.

## <a name="activities-and-notes"></a>Activiteiten en notities

Online kanalen bieden detailhandelaren manieren om informatie te verkrijgen over voorkeuren van klanten zonder dat klanten deze informatie expliciet hoeven te verstrekken. Als klanten daarentegen contact hebben met verkoopmedewerkers in de winkel, verstrekken zij expliciet informatie over hun voorkeuren. Helaas kan deze informatie verloren gaan nadat de verkoop is afgesloten. Als deze informatie echter wordt vastgelegd, kunnen detailhandelaren beter inzicht krijgen in klanten, zodat ze betere aanbevelingen kunnen en een betere algehele winkelervaring kunnen bieden.

Voor het vastleggen van de cruciale informatie die klanten verstrekken, kunnen verkoopmedewerkers niet alleen de eigenschappen van het klantenboek gebruiken, maar ook de functionaliteit voor activiteiten en notities. Detailhandelaren kunnen de activiteitstypen configureren, zoals informatie over het winkelbezoek, e-mailadres, telefoonnummer en afspraken. Activiteiten die verkoopmedewerkers maken, kunnen worden weergegeven in een tijdlijnindeling op het verkooppunt (POS). Zij kunnen ook worden weergegeven op het tabblad **Activiteiten** op de pagina **Alle klanten \> Algemeen** in Headquarters.

Verkoopmedewerkers kan ook notities gebruiken om algemene klantgegevens vast te leggen waarnaar kan worden verwezen voorafgaand aan elke interactie. Deze notities worden opgeslagen in Headquarters en kunnen worden weergegeven in het klantprofiel of op de pagina met klantgegevens in het callcenter.

> [!NOTE]
> Op dit moment kunnen alle notities en activiteiten worden bekeken door de verkoopmedewerker die voor de rechtspersoon werkt en kunnen de pagina's met klantdetails worden weergegeven. Notities en activiteiten zijn niet beperkt tot de verkoopmedewerker die een klant aan het klantenboek heeft toegevoegd.

## <a name="integration-with-dynamics-365-customer-insights"></a>Integratie met Dynamics 365 Customer Insights

Met de toepassing Dynamics 365 Customer Insights kunnen detailhandelaren gegevens verzamelen uit de verschillende systemen die klanten gebruiken om te communiceren met het merk van de detailhandelaar. Zij kunnen deze gegevens vervolgens gebruiken om één weergave van de klant te genereren en hieraan inzichten te ontlenen. De integratie van Customer Insights met Commerce stelt detailhandelaren in staat een of meer metingen te selecteren die moeten worden weergegeven op de klantkaart in het klantenboek. Zo kunnen detailhandelaren bijvoorbeeld de gegevens in Customer Insights gebruiken om de 'waarschijnlijkheid van verloop' voor een klant te berekenen en de beste vervolgactie te definiëren. Als deze waarden zijn gedefinieerd als metingen, kunnen ze worden weergegeven op de klantkaart en kunnen zij cruciale informatie verschaffen aan verkoopmedewerkers. Zie de documentatie van [Dynamics 365 Customer Insights](https://docs.microsoft.com/dynamics365/ai/customer-insights/overview) voor meer informatie over Customer Insights. Zie [Metingen](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures). voor meer informatie over metingen.

## <a name="set-up-clienteling"></a>Clienteling instellen

Voer de volgende stappen uit om de clienteling-functionaliteit in uw omgeving in te schakelen.

1. Filter in de werkruimte **Functiebeheer** de functies via de module **Retail en Commerce**.

    ![Clienteling in de lijst met functies voor de module Commerce](./media/Enable_clienteling.png "Clienteling in de lijst met functies voor de module Retail en Commerce")

2. Schakel de functie **Clienteling** in door **Nu inschakelen** te selecteren.
3. Ga naar de pagina **Commerce-parameters** en selecteer op het tabblad **Nummerreeks** de rij **Klantenboek-id**. Selecteer vervolgens een nummerreeks in het veld **Nummerreekscode**. Het systeem gebruikt deze nummerreeks om een id toe te wijzen aan klantenboeken.
4. Selecteer **Opslaan**.
5. Maak een nieuwe kenmerkgroep die de kenmerken bevat die u wilt vastleggen voor klanten die in klantenboeken worden beheerd. Zie [Kenmerken en kenmerkgroepen](https://docs.microsoft.com/dynamics365/retail/attribute-attributegroups-lifecycle) voor instructies.

    - Definieer de vereiste kenmerken zoals **Kan worden verfijnd**. Verkoopmedewerkers kunnen deze kenmerken vervolgens gebruiken om hun klantenboek te filteren.
    - Stel de weergavevolgorde in voor deze kenmerken. Met deze weergavevolgorde bepaalt u welke kenmerken worden weergegeven op de klantkaart in het klantenboek. Een weergavevolgorde van 1 wordt als hoger beschouwd dan een weergavevolgorde van 2. Daarom wordt het kenmerk met de weergavevolgorde 1 weergegeven vóór het kenmerk met de weergavevolgorde 2.

    > [!NOTE]
    > U kunt Customer Insights beschikbaar maken op dezelfde pagina. Voor verificatiedoeleinden moet echter een Azure-toepassings-id en geheim worden gemaakt. (Zie de sectie [De integratie van Customer Insights met Commerce inschakelen](#turn-on-the-integration-of-customer-insights-with-commerce) verderop in dit onderwerp voor meer informatie over de vereisten.) Als Customer Insights is ingeschakeld en u een of meer eenheden selecteert die op de klantkaart moeten worden weergegeven, worden deze metingen als eerste weergegeven. Vervolgens worden kenmerkgroepen in het klantenboek weergegeven op basis van de weergavevolgorde. Als u bijvoorbeeld twee metingen selecteert uit Customer Insights, worden deze twee metingen en één kenmerk van het klantenboek weergegeven op de klantkaart. (Het kenmerk van het klantenboek dat wordt weergegeven is het kenmerk met de hoogste weergavevolgorde.)

6. Ga op de pagina **Commerce-parameters** naar het tabblad **Clienteling** en selecteer in het veld **Kenmerkgroep klantenboek** de kenmerkgroep die u zojuist hebt gemaakt.

    ![Kenmerkgroep klantenboek geselecteerd](./media/Client%20book%20attributes.png "Kenmerkgroep klantenboek geselecteerd")

7. Als u activiteiten wilt vastleggen die op het POS plaatsvinden, definieert u de activiteitstypen op de pagina **Activiteitstypen** (**Retail en Commerce \> Klanten \> Activiteitstypen**).

    > [!NOTE]
    > Activiteitstypen worden door de Commerce Scale Unit opgehaald wanneer deze voor het eerst een realtime oproep uitvoert. Nadat de activiteiten zijn opgehaald, worden ze enkele uren in de cache geplaatst. Als u de activiteitstypen wijzigt, wacht u totdat de cache niet meer geldig is. Als alternatief kunt u, voor niet-productieomgevingen, de Commerce Scale Unit opnieuw starten.

8. Voeg twee knoppen toe aan de desbetreffende indeling van het POS-scherm, zodat verkoopmedewerkers hun eigen klantenboek kunnen bekijken plus het winkelklantenboek. (Winkelklantenboeken omvatten klanten uit alle klantenboeken van alle verkoopmedewerkers die een adresboek delen met de winkel.) De overeenkomstige bewerkingen worden respectievelijk **Klanten in klantenboek weergeven** en **Klanten in winkelklantenboeken weergeven** genoemd. Er zijn drie extra bewerkingen met betrekking tot klantenboeken beschikbaar. Met deze bewerkingen wordt bepaald welke verkoopmedewerkers klanten in het klantenboek kunnen toevoegen, verwijderen en opnieuw toewijzen. Deze worden respectievelijk **Klant toevoegen aan klantenboek**, **Klanten verwijderen uit klantenboek** en **Klanten opnieuw toewijzen aan een klantenboek** genoemd.
9. Voer de volgende taken voor distributieplanning uit: 1040, 1150, 1110 en 1090.

Nadat u deze procedure hebt voltooid, kunnen verkoopmedewerkers de pagina met klantgegevens op het POS openen en klanten toevoegen aan hun klantenboek, activiteiten en notities voor klanten weergeven en vastleggen, en zich op klanten richten door klant- en klantenboekkenmerken te gebruiken om het klantenboek te filteren. In de volgende afbeelding ziet u een voorbeeld van een klantenboek.

![Voorbeeld van een klantenboek](./media/client_book.png "Voorbeeld van een klantenboek")

## <a name="turn-on-the-integration-of-customer-insights-with-commerce"></a>Integratie van Customer Insights met Commerce inschakelen

Als u de integratie van Customer Insights met Commerce wilt inschakelen, moet u ervoor zorgen dat u een actief exemplaar van Customer Insights hebt in de tenant waarin Commerce is ingericht. U moet ook een Azure Active Directory (Azure AD)-gebruikersaccount hebben met een Azure-abonnement.

Volg deze stappen voor het instellen van de integratie.

1. Registreer een toepassing in de Azure-portal. Deze toepassing wordt gebruikt voor verificatie met Customer Insights. Zie [Snelstart: Een toepassing registreren op het Microsoft-identiteitsplatform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) voor instructies.
2. Genereer een geheim voor de toepassing. Noteer het geheim en bewaar het op een veilige plek, omdat u het later nog nodig zult hebben. Selecteer ook de verlooptermijn voor het geheim.

    > [!IMPORTANT]
    > Onderneem stappen om ervoor te zorgen dat u het geheim wijzigt voordat dit verloopt. Anders wordt de integratie onverwacht beëindigd.

3. Maak een Azure-sleutelkluis en sla het toepassingsgeheim op. Zie [Snelstart: Een geheim instellen en ophalen vanuit Azure Key Vault via de Azure-portal](https://docs.microsoft.com/azure/key-vault/quick-create-portal) voor instructies.
4. Schakel de toegang tot Azure Key Vault in vanuit Commerce. U kunt deze stap alleen uitvoeren als u een toepassings-id en een geheim hebt. De toepassing kan dezelfde toepassing zijn die u in stap 1 hebt gemaakt, maar kan ook een nieuwe toepassing zijn. (Met andere woorden, u kunt de toepassing die u in stap 1 hebt gemaakt, gebruiken voor zowel toegang tot de Key Vault als toegang tot de Customer Insights-service, of u kunt een unieke toepassing maken voor elk type toegang.) Zie [Referenties voor serviceprincipal opslaan in Azure Stack Key Vault](https://docs.microsoft.com/azure-stack/user/azure-stack-key-vault-store-credentials?view=azs-1908#create-a-service-principal)voor instructies.
5. Ga in Headquarters naar **Systeembeheer \> Instellingen \> Parameters voor sleutelkluis** en voer de vereiste informatie voor de sleutelkluis in. Voer vervolgens in het veld **Client sleutelkluis** de toepassings-id in die u in stap 4 hebt gebruikt, zodat Commerce toegang kan krijgen tot de geheimen in de sleutelkluis.
6. Als u de toepassing die u in stap 1 hebt gemaakt wilt toevoegen aan de lijst met veilige toepassingen (ook wel een veilige lijst genoemd), gaat u naar Customer Insights en verleent u de toegangsoptie **Weergeven** aan de toepassing. Zie [Machtigingen](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-permissions) voor instructies.
7. Ga in Commerce naar de pagina **Commerce-parameters** en voer de volgende stappen uit op het tabblad **Clienteling** op het sneltabblad **Dynamics 365 Customer Insights**:

    1. Voer in het veld **Toepassings-id** de toepassings-id in die u in stap 1 hebt gebruikt.
    2. Voer in het veld **Geheime naam** de naam in van het sleutelkluisgeheim dat u in stap 5 hebt gemaakt.
    3. Stel de optie **Customer Insights inschakelen** in op **Ja**. Als de installatie om een of andere reden mislukt, wordt er een foutbericht weergegeven en wordt deze optie ingesteld op **Nee**.
    4. U kunt meerdere omgevingen in Customer Insights hebben, zoals test- en productieomgevingen. Voer in het veld **Omgevingsexemplaar-id** de desbetreffende omgeving in.
    5. Voer in het veld **Alternatieve klant-id** de eigenschap in Customer Insights in die is toegewezen aan het klantrekeningnummer. (Het klantrekeningnummer is de klant-id in Commerce.)
    6. De overige drie eigenschappen zijn de metingen die worden weergegeven op de klantkaart in het klantenboek. U kunt maximaal drie metingen selecteren om op de klantkaart weer te geven. (U hoeft echter geen metingen te selecteren.) Zoals eerder vermeld, geeft het systeem eerst deze waarden weer en worden vervolgens de waarden voor de kenmerkgroep van het klantenboek weergegeven.


[!INCLUDE[footer-include](../includes/footer-banner.md)]