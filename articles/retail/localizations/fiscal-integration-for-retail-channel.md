---
title: Overzicht van fiscale integratie voor detailhandelskanalen
description: Dit onderwerp biedt een overzicht van de fiscale integratiefuncties die beschikbaar zijn in Microsoft Dynamics 365 for Retail.
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2019-1-16
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2dc977e3c53b1f15b41b095f586861b67c973a6d
ms.sourcegitcommit: 68df883200b5c477ea1799cc28d3ef467cd29202
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/07/2019
ms.locfileid: "377130"
---
# <a name="overview-of-fiscal-integration-for-retail-channels"></a>Overzicht van fiscale integratie voor detailhandelskanalen

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a>Introductie

Dit onderwerp biedt een overzicht van de fiscale integratiefuncties die beschikbaar zijn in Microsoft Dynamics 365 for Retail. Fiscale integratie omvat integratie met verschillende fiscale apparaten en services die fiscale registratie mogelijk maken van detailhandelverkoop, in overeenstemming met de lokale belastingwetgeving die gericht is op het voorkomen van belastingfraude in de detailhandel. Dit zijn enkele veelvoorkomende scenario's die kunnen worden gedekt door fiscale integratie: 

- Registreer een detailhandelverkoop op een fiscaal apparaat dat is verbonden met Retail POS, zoals een fiscale printer, en druk een fiscaal ontvangstbewijs voor de klant af.
- Dien veilig informatie die verband houdt met verkopen en retouren die worden voltooid in Retail POS, in bij een externe webservice die wordt bediend door de belastingdienst.
- Help intactheid van verkooptransactiegegevens garanderen met behulp van digitale ondertekening.

De functionaliteit voor fiscale integratie in de detailhandel is een raamwerk dat een gemeenschappelijke oplossing biedt voor verdere ontwikkeling en aanpassing van de integratie tussen Retail POS en fiscale apparaten en services. De functionaliteit bevat ook fiscale integratievoorbeelden die ondersteuning bieden voor elementaire detailhandelscenario's voor specifieke landen of regio's, en die werken met specifieke fiscale apparaten of services. Een fiscaal integratievoorbeeld bestaat uit verschillende uitbreidingen van de detailhandelonderdelen en is opgenomen in de Retail-SDK (Software Development Kit). Zie voor meer informatie over fiscale integratievoorbeelden die beschikbaar zijn in de Retail-SDK [Fiscale integratievoorbeelden in de Retail-SDK](#fiscal-integration-samples-in-the-retail-sdk). Zie voor informatie over het installeren en gebruiken van de Retail-SDK [Overzicht van de Retail-SDK](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Ter ondersteuning van andere scenario's die niet worden ondersteund door een fiscaal integratievoorbeeld, om Retail POS te integreren met andere fiscale apparaten of services of om te voldoen aan vereisten van andere landen of regio's, moet u een bestaand fiscaal integratievoorbeeld uitbreiden of een nieuw voorbeeld maken op basis van een bestaand voorbeeld.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices"></a>Fiscale registratieproces- en fiscale integratievoorbeelden voor fiscale apparaten

Een fiscaal registratieproces in Retail POS kan bestaan uit een of meer stappen. Elke stap omvat fiscale registratie van specifieke detailhandeltransacties of -gebeurtenissen in één fiscaal apparaat of service. De volgende oplossingsonderdelen maken deel uit van de fiscale registratie in een fiscaal apparaat dat is verbonden met een Hardware-station:

- **Extensie Commerce runtime (CRT)**: dit onderdeel serialiseert gebeurtenissen van detailhandeltransacties/-gebeurtenissen in de indeling die ook wordt gebruikt voor interactie met het fiscale apparaat, ontleedt antwoorden van het fiscale apparaat en slaat de antwoorden op in de afzetkanaaldatabase. De extensie definieert ook de specifieke transacties en gebeurtenissen die moeten worden geregistreerd. Naar dit onderdeel wordt vaak verwezen als een *fiscale documentprovider*.
- **Extensie Hardware-station**: dit onderdeel initialiseert de communicatie met het fiscale apparaat, verzendt aanvragen en directe opdrachten naar het fiscale apparaat op basis van de gegevens van detailhandeltransacties/-gebeurtenissen die afkomstig zijn uit het fiscale document en ontvangt antwoorden van het fiscale apparaat. Naar dit onderdeel wordt vaak verwezen als een *fiscale connector*.

Een fiscaal integratievoorbeeld voor een fiscaal apparaat bevat de extensies CRT en Hardware-station voor respectievelijk een fiscale documentprovider en een fiscale connector. Het bevat ook de volgende componentconfiguraties:

- **Configuratie van fiscale documentprovider**: deze configuratie bepaalt een uitvoermethode en een indeling voor fiscale documenten. De configuratie bevat ook een gegevenstoewijzing voor belastingen en betalingsmethoden om gegevens uit Retail POS compatibel te maken met de waarden die vooraf zijn gedefinieerd in de firmware van het fiscale apparaat.
- **Configuratie van fiscale connector**: deze configuratie bepaalt de fysieke communicatie met het specifieke fiscale apparaat.

Een fiscaal registratieproces voor een bepaalde POS-kassa wordt gedefinieerd door een bijbehorende instelling in het POS-functionaliteitsprofiel. Voor meer informatie over het configureren van een fiscaal registratieproces uploadt u configuraties voor de fiscale documentprovider en connector en wijzigt u de parameters ervan. Zie [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

Het volgende voorbeeld toont een gebruikelijke fiscale registratie-uitvoeringsstroom voor een fiscaal apparaat. De stroom begint met een gebeurtenis in het POS (bijvoorbeeld de voltooiing van een verkooptransactie) en implementeert de volgende reeks stappen:

1. Het POS vraagt een fiscaal document aan bij CRT.
2. CRT bepaalt of de huidige gebeurtenis fiscale registratie vereist.
3. Op basis van de instellingen voor het fiscale registratieproces, identificeert CRT een fiscale connector en de bijbehorende fiscale documentprovider die moet worden gebruikt voor de fiscale registratie.
4. CRT wordt uitgevoerd voor de fiscale documentprovider die een fiscaal document genereert (bijvoorbeeld een XML-document) dat staat voor de detailhandeltransactie of gebeurtenis.
5. Het POS verzendt het fiscale document dat CRT voorbereidt naar een Hardware-station.
6. Het Hardware-station voert de fiscale connector uit die het fiscale document verwerkt en doorgeeft aan het fiscale apparaat of service.
7. Het POS analyseert de reactie van het fiscale apparaat of service om te bepalen of de fiscale registratie voltooid is.
8. CRT slaat het antwoord op in de afzetkanaaldatabase.

![Oplossingsschema](media/emea-fiscal-integration-solution.png "Oplossingsschema")

## <a name="error-handling"></a>Foutverwerking

Het fiscale integratieraamwerk biedt de volgende opties voor het afhandelen van fouten tijdens fiscale registratie:

- **Opnieuw**: operators kunnen deze optie gebruiken als de storing snel kan worden opgelost en de fiscale registratie opnieuw kan worden uitgevoerd. Deze optie kan bijvoorbeeld worden gebruikt wanneer het fiscale apparaat niet is verbonden, de fiscale printer geen papier bevat of er papier is vastgelopen in de fiscale printer.
- **Annuleren**: met deze optie kunnen operators de fiscale registratie van de huidige transactie of gebeurtenis uitstellen als deze mislukt. Nadat de registratie is uitgesteld, kan de operator blijven werken op het POS en kan elke bewerking worden voltooid waarvoor geen fiscale registratie vereist is. Wanneer een gebeurtenis de fiscale registratie vereist in het POS (er wordt bijvoorbeeld een nieuwe transactie geopend), wordt het dialoogvenster voor foutafhandeling automatisch weergegeven om de operator te informeren dat de vorige transactie niet correct is geregistreerd en om opties voor foutafhandeling te bieden.
- **Overslaan**: operators kunnen deze optie gebruiken wanneer de fiscale registratie onder bepaalde voorwaarden kan worden weggelaten en normale bewerkingen kunnen doorgaan in het POS. Deze optie kan bijvoorbeeld worden gebruikt wanneer een verkooptransactie waarvoor de fiscale registratie is mislukt, kan worden geregistreerd in een speciaal papieren journaal.
- **Markeren als geregistreerd**: operatoren kunnen deze optie gebruiken als de transactie is geregistreerd in het fiscale apparaat (er is bijvoorbeeld een fiscaal ontvangstbewijs afgedrukt), maar er een fout is opgetreden bij het opslaan van het fiscale antwoord in de afzetkanaaldatabase.

> [!NOTE]
> De opties **Overslaan** en **Markeren als geregistreerd** moeten in het fiscale registratieproces worden geactiveerd voordat ze worden gebruikt. Bovendien moeten bijbehorende machtigingen worden toegekend aan operators.

De opties **Overslaan** en **Markeren als geregistreerd** maken infocodes mogelijk om bepaalde specifieke informatie over de fout op te slaan, zoals de reden voor de fout of een uitleg van waarom de fiscale registratie is overgeslagen of de transactie als geregistreerd is gemarkeerd. Zie voor meer informatie over het instellen van parameters voor foutafhandeling [Instellingen voor het verwerken van fouten kiezen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Fiscaal antwoord opslaan in fiscale transactie

Wanneer fiscale registratie van een transactie of gebeurtenis geslaagd is, wordt een fiscale transactie in de afzetkanaaldatabase gemaakt en gekoppeld aan de oorspronkelijke transactie of gebeurtenis. Als de optie **Overslaan** of **Markeren als geregistreerd** wordt geselecteerd voor een mislukte fiscale registratie, wordt deze informatie ook opgeslagen in een fiscale transactie. Een fiscale transactie bevat de fiscale reactie van het fiscale apparaat of de service. Als het fiscale registratieproces uit meerdere stappen bestaat, wordt een fiscale transactie gemaakt voor elke stap van het proces dat heeft geleid tot een geslaagde of mislukte registratie.

Fiscale transacties worden overgeboekt naar Retail Headquarters door de *P-taak*, samen met detailhandeltransacties. Op het sneltabblad **Fiscale transacties** van de pagina **Transacties detailhandelwinkel** kunt u de fiscale transacties weergeven die zijn gekoppeld aan detailhandeltransacties.

Een fiscale transactie wordt opgeslagen met de volgende gegevens:

- Details van fiscaal registratieproces (proces, connectorgroep, connector, enzovoort). Slaat ook het serienummer van het fiscale apparaat op in het veld **Kassanummer** als deze informatie is opgenomen in het fiscale antwoord.
- De status van de fiscale registratie: **Voltooid** voor succesvolle registratie, **Overgeslagen** als de operator de optie **Overslaan** heeft geselecteerd voor een mislukte registratie of **Gemarkeerd als geregistreerd** als de operator de optie **Markeren als geregistreerd** heeft geregistreerd.
- Infocodetransacties weergeven die zijn gekoppeld aan een geselecteerde fiscale transactie. Als u de infocodetransacties wilt weergeven, selecteert u op het sneltabblad **Fiscale transacties** een fiscale transactie met de status **Overgeslagen** of **Gemarkeerd als geregistreerd** en selecteert u vervolgens **Informatiecodetransacties**.

## <a name="fiscal-texts-for-discounts"></a>Fiscale teksten voor kortingen

Sommige landen of regio's hebben speciale vereisten over aanvullende tekst die moeten worden afgedrukt op fiscale ontvangsten wanneer verschillende soorten kortingen worden toegepast. Met de fiscale integratiefunctionaliteit kunt u een speciale tekst instellen voor een korting die wordt afgedrukt na een kortingsregel in een fiscaal ontvangstbewijs. Voor handmatige kortingen kunt u een fiscale tekst voor de informatiecode configureren die wordt opgegeven als de **Productkorting**-infocode in het POS-functionaliteitsprofiel. Zie voor meer informatie over het instellen van fiscale teksten voor kortingen [Fiscale teksten voor kortingen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Fiscale X- en fiscale Z-rapporten afdrukken

De functionaliteit voor fiscale integratie ondersteunt het genereren van eindedagoverzichten die specifiek zijn voor het geïntegreerde fiscale apparaat of service:

- Nieuwe knoppen die corresponderende bewerkingen uitvoeren, moeten worden toegevoegd aan de POS-schermindeling. Zie voor meer informatie [X/Z-rapporten instellen vanaf het POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- In het fiscale integratievoorbeeld moeten deze bewerkingen worden vergeleken met de bijbehorende bewerkingen van het fiscale apparaat.

## <a name="fiscal-integration-samples-in-the-retail-sdk"></a>Fiscale integratievoorbeelden in de Retail-SDK

De volgende fiscale integratievoorbeelden zijn momenteel beschikbaar in de Retail-SDK die wordt vrijgegeven met Retail:

- [Voorbeeld van integratie van fiscale printer voor Italië](emea-ita-fpi-sample.md)
- [Voorbeeld van integratie van fiscale printer voor Polen](emea-pol-fpi-sample.md)

De volgende fiscale Integratiefunctionaliteit is ook beschikbaar in de Retail-SDK, maar maakt op het moment geen gebruik van het fiscale integratieraamwerk. Migratie van deze functionaliteit naar het fiscale integratieraamwerk is gepland voor latere updates.

- [Digitale handtekening voor Frankrijk](emea-fra-cash-registers.md)
- [Digitale handtekening voor Noorwegen](emea-nor-cash-registers.md)
- [Regeleenheidintegratievoorbeeld voor Zweden](../dev-itpro/retail-sdk/retail-sdk-control-unit-sample.md)
