---
title: Overzicht fiscale integratie voor Commerce-afzetkanalen
description: Dit onderwerp biedt een overzicht van de fiscale integratiefuncties die beschikbaar zijn in Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 46e0afd5a8cb692da56a7d5f261ca30d9b3aaa80
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388308"
---
# <a name="fiscal-integration-overview-for-commerce-channels"></a>Overzicht fiscale integratie voor Commerce-afzetkanalen

[!include [banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dit onderwerp biedt een overzicht van de fiscale integratiefuncties die beschikbaar zijn in Dynamics 365 Commerce. 

Fiscale integratie omvat integratie met verschillende fiscale apparaten en services die fiscale registratie mogelijk maken van verkoop, in overeenstemming met de lokale belastingwetgeving die gericht is op het voorkomen van belastingfraude in de detailhandel. Dit zijn enkele veelvoorkomende scenario's die kunnen worden gedekt door fiscale integratie:

- Registreer een verkoop op een fiscaal apparaat dat is verbonden met POS, zoals een fiscale printer, en druk een fiscaal ontvangstbewijs voor de klant af.
- Dien veilig informatie die verband houdt met verkopen en retouren die worden voltooid in Retail POS, in bij een externe webservice die wordt bediend door de belastingdienst.
- Help intactheid van verkooptransactiegegevens garanderen met behulp van digitale ondertekening.

De functionaliteit voor fiscale integratie is een raamwerk dat een gemeenschappelijke oplossing biedt voor verdere ontwikkeling en aanpassing van de integratie tussen Retail POS en fiscale apparaten en services. De functionaliteit bevat ook fiscale integratievoorbeelden die ondersteuning bieden voor basisscenario's voor specifieke landen of regio's, en die werken met specifieke fiscale apparaten of services. Een fiscaal integratievoorbeeld bestaat uit verschillende uitbreidingen van de Commerce-onderdelen en is opgenomen in de SDK (Software Development Kit). Zie voor meer informatie over de voorbeelden van fiscale integratie [Voorbeelden van fiscale integratie in de Commerce-SDK](#fiscal-integration-samples-in-the-commerce-sdk). Zie voor informatie over het installeren en gebruiken van de Commerce-SDK [Architectuur van Retail-SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md).

Ter ondersteuning van andere scenario's die niet worden ondersteund door een fiscaal integratievoorbeeld, om Retail POS te integreren met andere fiscale apparaten of services of om te voldoen aan vereisten van andere landen of regio's, moet u een bestaand fiscaal integratievoorbeeld uitbreiden of een nieuw voorbeeld maken op basis van een bestaand voorbeeld.

## <a name="fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services"></a>Voorbeelden van fiscaal registratieproces en fiscale integratie voor fiscale apparaten en services

Een fiscaal registratieproces in Retail POS kan bestaan uit een of meer stappen. Elke stap omvat fiscale registratie van specifieke transacties of gebeurtenissen in één fiscaal apparaat of service. De volgende oplossingsonderdelen maken deel uit van de fiscale registratie in een fiscaal apparaat of fiscale service:

- **Fiscale documentprovider**: met dit onderdeel worden gegevens van transacties/gebeurtenissen geserialiseerd in de indeling die ook wordt gebruikt voor interactie met het fiscale apparaat of de fiscale service, worden antwoorden van het fiscale apparaat of de fiscale service geparseerd en worden de antwoorden in de kanaaldatabase opgeslagen. De extensie definieert ook de specifieke transacties en gebeurtenissen die moeten worden geregistreerd.
- **Fiscale connector**: met dit onderdeel wordt de communicatie geïnitialiseerd met het fiscale apparaat of de fiscale service, worden aanvragen verzonden naar of opdrachten gegeven aan het fiscale apparaat of de fiscale service op basis van de gegevens van transacties/gebeurtenissen die afkomstig zijn uit het fiscale document, en worden antwoorden van het fiscale apparaat of de fiscale service ontvangen.

Een voorbeeld van een fiscale integratie kan de extensies Commerce runtime (CRT), Hardwarestation en POS bevatten voor een fiscale documentprovider en een fiscale connector. Het bevat ook de volgende componentconfiguraties:

- **Configuratie van fiscale documentprovider**: deze configuratie bepaalt een uitvoermethode en een indeling voor fiscale documenten. De configuratie bevat ook een gegevenstoewijzing voor belastingen en betalingsmethoden om gegevens uit Retail POS compatibel te maken met de waarden die vooraf zijn gedefinieerd in de firmware van het fiscale apparaat of de fiscale service.
- **Configuratie van fiscale connector**: deze configuratie bepaalt de fysieke communicatie met het specifieke fiscale apparaat of de specifieke fiscale service.

Een fiscaal registratieproces voor een bepaalde POS-kassa wordt gedefinieerd door een bijbehorende instelling in het POS-functionaliteitsprofiel. Zie voor meer informatie over het configureren van een fiscaal registratieproces, het uploaden van configuraties voor de fiscale documentprovider en fiscale connector en het wijzigen van configuratieparameters [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

> [!NOTE]
> Als u apparaten nodig hebt voor niet-fiscale bewerkingen, zoals zoeken naar productcatalogi, zoeken naar klanten of het maken van concepttransacties, kunt u deze als kassa's selecteren met beperkte fiscale registratie. Zie [Kassa's met fiscale registratiebeperkingen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-registers-with-fiscal-registration-restrictions) voor meer informatie.

De volgende typische fiscale registratiestroom begint met een gebeurtenis in het POS (bijvoorbeeld de voltooien van een verkooptransactie) en implementeert een vooraf gedefinieerde stappenvolgorde die andere Commerce-onderdelen betreft (zoals CRT en Hardwarestation).

1. In het POS wordt een fiscaal document van het FIF (Fiscal Integration Framework) gevraagd.
1. Het FIF bepaalt of voor de huidige gebeurtenis fiscale registratie is vereist.
1. Op basis van de instellingen voor het fiscale registratieproces, identificeert het FIF een fiscale connector en een bijbehorende fiscale documentprovider die moet worden gebruikt voor de fiscale registratie.
1. Het FIF voert de fiscale documentprovider uit waarmee een fiscaal document wordt gegenereerd (bijvoorbeeld een XML-document) dat de transactie of gebeurtenis vertegenwoordigt.
1. Het FIF retourneert het gegenereerde fiscale document naar het POS.
1. Het POS vraagt het FIF het fiscale document naar het fiscale apparaat of de fiscale service te verzenden.
1. Het FIF voert de fiscale connector uit waarmee het fiscale document wordt verwerkt en verzendt het naar het fiscale apparaat of de fiscale service.
1. Het FIF retourneert het fiscale antwoord (het antwoord van het fiscale apparaat of de fiscale service) naar het POS.
1. Het POS analyseert het fiscale antwoord om te bepalen of de fiscale registratie is gelukt. Het POS vraagt het FIF indien nodig om eventuele opgetreden fouten te verwerken. 
1. Het POS vraagt het FIF het fiscale antwoord te verwerken en op te slaan.
1. De fiscale documentprovider verwerkt het fiscale antwoord. Als onderdeel van deze verwerking verwerkt de fiscale documentprovider het antwoord en worden op basis hiervan uitgebreide gegevens geëxtraheerd.
1. Het FIF slaat het antwoord en de uitgebreide gegevens in de kanaaldatabase op.
1. Het POS drukt zo nodig een ontvangstbewijs af via een normale printer voor kassabonnen die is gekoppeld aan het hardwarestation. Het ontvangstbewijs kan vereiste gegevens uit het fiscale antwoord bevatten.
 
De volgende voorbeelden laten fiscale registratie-uitvoeringsstromen zien voor typische fiscale apparaten of services.
 
### <a name="fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station"></a>Fiscale registratie wordt uitgevoerd via een apparaat dat is gekoppeld aan het hardwarestation.

Deze configuratie wordt gebruikt wanneer een fysiek fiscaal apparaat, zoals een fiscale printer, aan het hardwarestation is gekoppeld. Deze configuratie is ook van toepassing als de communicatie met een fiscaal apparaat of fiscale service wordt uitgevoerd via software die op het hardwarestation is geïnstalleerd. In dit geval bevindt de fiscale documentprovider zich in CRT en de fiscale connector op het hardwarestation.

![Fiscale registratie uitgevoerd via een apparaat dat is gekoppeld aan het hardwarestation.](media/FIF-CRT-HWS.png)

### <a name="fiscal-registration-is-done-via-an-external-service"></a>Fiscale registratie wordt via een externe service uitgevoerd

Deze configuratie wordt gebruikt wanneer fiscale registratie via een externe service wordt uitgevoerd, zoals een webservice van de belastingdienst. In dit geval bevinden zowel de fiscale documentprovider als de fiscale connector zich in CRT.

![Fiscale registratie uitgevoerd via een externe service](media/FIF-CRT-CRT.png)
 
### <a name="fiscal-registration-is-done-internally-in-the-crt"></a>Fiscale registratie wordt intern uitgevoerd in de CRT

Deze configuratie wordt gebruikt als er geen extern fiscaal apparaat of fiscale service vereist is voor fiscale registratie. De configuratie wordt bijvoorbeeld gebruikt wanneer fiscale registratie wordt uitgevoerd via het digitaal ondertekenen van verkooptransacties. In dit geval bevinden zowel de fiscale documentprovider als de fiscale connector zich in CRT.

![Fiscale registratie wordt intern uitgevoerd in de CRT.](media/FIF-CRT-CRT-SGN.png)

### <a name="fiscal-registration-is-done-via-a-device-or-service-in-the-local-network"></a>Fiscale registratie wordt uitgevoerd via een apparaat of service in het lokale netwerk

Deze configuratie wordt gebruikt wanneer een fysiek fiscaal apparaat of fiscale service aanwezig is in het lokale netwerk van de winkel en een HTTPS-API (Application Programming Interface) bevat. In dit geval bevindt de fiscale documentprovider zich in de CRT en de fiscale connector in het POS.

![Fiscale registratie wordt uitgevoerd via een apparaat of service in het lokale netwerk.](media/FIF-CRT-POS.png)

## <a name="error-handling"></a>Foutverwerking

Het fiscale integratieraamwerk biedt de volgende opties voor het afhandelen van fouten tijdens fiscale registratie:

- **Opnieuw**: operators kunnen deze optie gebruiken als de storing snel kan worden opgelost en de fiscale registratie opnieuw kan worden uitgevoerd. Deze optie kan bijvoorbeeld worden gebruikt wanneer het fiscale apparaat niet is verbonden, de fiscale printer geen papier bevat of er papier is vastgelopen in de fiscale printer.
- **Annuleren**: met deze optie kunnen operators de fiscale registratie van de huidige transactie of gebeurtenis uitstellen als deze mislukt. Nadat de registratie is uitgesteld, kan de operator blijven werken op het POS en kan elke bewerking worden voltooid waarvoor geen fiscale registratie vereist is. Wanneer een gebeurtenis de fiscale registratie vereist in het POS (er wordt bijvoorbeeld een nieuwe transactie geopend), wordt het dialoogvenster voor foutafhandeling automatisch weergegeven om de operator te informeren dat de vorige transactie niet correct is geregistreerd en om opties voor foutafhandeling te bieden.
- **Overslaan**: operators kunnen deze optie gebruiken wanneer de fiscale registratie onder bepaalde voorwaarden kan worden weggelaten en normale bewerkingen kunnen doorgaan in het POS. Deze optie kan bijvoorbeeld worden gebruikt wanneer een verkooptransactie waarvoor de fiscale registratie is mislukt, kan worden geregistreerd in een speciaal papieren journaal.
- **Markeren als geregistreerd**: operatoren kunnen deze optie gebruiken als de transactie is geregistreerd in het fiscale apparaat (er is bijvoorbeeld een fiscaal ontvangstbewijs afgedrukt), maar er een fout is opgetreden bij het opslaan van het fiscale antwoord in de afzetkanaaldatabase.
- **Uitstellen**: operatoren kunnen deze optie gebruiken als de transactie niet is geregistreerd omdat de registratieservice niet beschikbaar was. 

> [!NOTE]
> De opties **Overslaan**, **Markeren als geregistreerd** en **Uitstellen** moeten in het fiscale registratieproces worden geactiveerd voordat ze worden gebruikt. Bovendien moeten bijbehorende machtigingen worden toegekend aan operators.

De opties **Overslaan**, **Markeren als geregistreerd** en **Uitstellen** maken informatiecodes mogelijk om bepaalde specifieke informatie over een fout op te slaan, zoals de reden voor de fout of een uitleg van de reden waarom de fiscale registratie is overgeslagen of de transactie als geregistreerd is gemarkeerd. Zie voor meer informatie over het instellen van parameters voor foutafhandeling [Instellingen voor het verwerken van fouten kiezen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="optional-fiscal-registration"></a>Optionele fiscale registratie

Fiscale registratie kan verplicht zijn voor bepaalde bewerkingen, maar optioneel voor andere bewerkingen. De fiscale registratie van normale verkopen en retouren kan bijvoorbeeld verplicht zijn, maar de fiscale registratie van bewerkingen die zijn gerelateerd aan klantdeposito´s kan optioneel zijn. In dit geval wordt verdere verkoop geblokkeerd als er geen fiscale registratie van een verkoop plaatsvindt, maar als de fiscale registratie van een klantdeposito niet wordt uitgevoerd, wordt verdere verkoop niet geblokkeerd. Om een onderscheid te maken tussen verplichte en optionele bewerkingen wordt aangeraden deze af te handelen via verschillende documentproviders en afzonderlijke stappen in het proces van fiscale registratie voor deze providers in te stellen. De parameter **Doorgaan bij fout** moet worden ingeschakeld voor elke stap die is gerelateerd aan optionele fiscale registratie. Zie voor meer informatie over het instellen van parameters voor foutafhandeling [Instellingen voor het verwerken van fouten kiezen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

### <a name="manually-rerun-fiscal-registration"></a>Fiscale registratie handmatig opnieuw uitvoeren

Als de fiscale registratie van een transactie of gebeurtenis is uitgesteld na een fout (bijvoorbeeld als de operator **Annuleren** heeft geselecteerd in het dialoogvenster voor foutafhandeling), kunt u de fiscale registratie handmatig opnieuw uitvoeren door een bijbehorende bewerking aan te roepen. Zie voor meer informatie [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).

### <a name="postpone-option"></a>Optie Uitstellen

Met de optie **Uitstellen** kunt u doorgaan met het fiscale registratieproces als de huidige stap mislukt. De optie kan worden gebruikt als er een back-upoptie voor fiscale registratie is.

### <a name="fiscal-registration-health-check"></a>Statuscontrole fiscale registratie

Met de statuscontroleprocedure voor fiscale registraties wordt de beschikbaarheid van het fiscale apparaat of de fiscale service gecontroleerd wanneer bepaalde gebeurtenissen plaatsvinden. Als de fiscale registratie momenteel niet kan worden voltooid, wordt de operator vooraf in kennis gesteld.

Met het POS wordt de statuscontrole uitgevoerd wanneer de volgende gebeurtenissen plaatsvinden:

- Er wordt een nieuwe transactie geopend.
- Een uitgestelde transactie wordt teruggeroepen.
- Een verkoop- of retourtransactie wordt voltooid.

Als de statuscontrole mislukt, toont het POS het dialoogvenster voor statuscontrole. Dit dialoogvenster bevat de volgende knoppen:

- **OK**: met deze knop kan de operator een statuscontrolefout negeren en doorgaan met de bewerking. Operators kunnen deze knop alleen selecteren als de machtiging **Overslaan van statuscontrolefout toestaan** ervoor is ingeschakeld.
- **Annuleren**: als de operator deze knop selecteert, annuleert het POS de laatste actie (een artikel wordt bijvoorbeeld niet toegevoegd aan een nieuwe transactie).

> [!NOTE]
> De statuscontrole wordt alleen uitgevoerd als voor de huidige bewerking fiscale registratie is vereist en als de parameter **Doorgaan bij fout** is uitgeschakeld voor de huidige stap van het proces voor fiscale registratie. Zie voor meer informatie [Instellingen voor het verwerken van fouten kiezen](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

## <a name="storing-fiscal-response-in-fiscal-transaction"></a>Fiscaal antwoord opslaan in fiscale transactie

Wanneer fiscale registratie van een transactie of gebeurtenis geslaagd is, wordt een fiscale transactie in de afzetkanaaldatabase gemaakt en gekoppeld aan de oorspronkelijke transactie of gebeurtenis. Als de optie **Overslaan** of **Markeren als geregistreerd** wordt geselecteerd voor een mislukte fiscale registratie, wordt deze informatie ook opgeslagen in een fiscale transactie. Een fiscale transactie bevat de fiscale reactie van het fiscale apparaat of de service. Als het fiscale registratieproces uit meerdere stappen bestaat, wordt een fiscale transactie gemaakt voor elke stap van het proces dat heeft geleid tot een geslaagde of mislukte registratie.

Fiscale transacties worden overgeboekt naar Headquarters door de *P-taak* samen met transacties. Op het sneltabblad **Fiscale transacties** van de pagina **Winkeltransacties** kunt u de fiscale transacties weergeven die zijn gekoppeld aan transacties.

Een fiscale transactie wordt opgeslagen met de volgende gegevens:

- Details van fiscaal registratieproces (proces, connectorgroep, connector, enzovoort). Slaat ook het serienummer van het fiscale apparaat op in het veld **Kassanummer** als deze informatie is opgenomen in het fiscale antwoord.
- De status van de fiscale registratie: **Voltooid** voor succesvolle registratie, **Overgeslagen** als de operator de optie **Overslaan** heeft geselecteerd voor een mislukte registratie, **Gemarkeerd als geregistreerd** als de operator de optie **Markeren als geregistreerd** heeft geselecteerd of **Uitgesteld** als de operator de optie **Uitstellen** heeft geselecteerd.
- Infocodetransacties weergeven die zijn gekoppeld aan een geselecteerde fiscale transactie. Als u de infocodetransacties wilt weergeven, selecteert u op het sneltabblad **Fiscale transacties** een fiscale transactie met de status **Overgeslagen**, **Gemarkeerd als geregistreerd** of **Uitgesteld** en selecteert u vervolgens **Informatiecodetransacties**.

Als u **Uitgebreide gegevens** selecteert, kunt u ook bepaalde eigenschappen van de fiscale transactie weergeven. De lijst met eigenschappen die kunnen worden weergegeven, is specifiek voor de fiscale registratiefunctionaliteit die de fiscale transactie heeft gegenereerd. U kunt bijvoorbeeld de digitale handtekening, het opeenvolgende nummer, het certificaatsalgoritme, de hash-algoritme-id en andere eigenschappen voor fiscale transacties voor de functionaliteit voor digitale ondertekening voor Frankrijk weergeven.

## <a name="fiscal-texts-for-discounts"></a>Fiscale teksten voor kortingen

Sommige landen of regio's hebben speciale vereisten over aanvullende tekst die moeten worden afgedrukt op fiscale ontvangsten wanneer verschillende soorten kortingen worden toegepast. Met de fiscale integratiefunctionaliteit kunt u een speciale tekst instellen voor een korting die wordt afgedrukt na een kortingsregel in een fiscaal ontvangstbewijs. Voor handmatige kortingen kunt u een fiscale tekst voor de informatiecode configureren die wordt opgegeven als de **Productkorting**-infocode in het POS-functionaliteitsprofiel. Zie voor meer informatie over het instellen van fiscale teksten voor kortingen [Fiscale teksten voor kortingen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).

## <a name="printing-fiscal-x-and-fiscal-z-reports"></a>Fiscale X- en fiscale Z-rapporten afdrukken

De functionaliteit voor fiscale integratie ondersteunt het genereren van eindedagoverzichten die specifiek zijn voor het geïntegreerde fiscale apparaat of service:

- Nieuwe knoppen die corresponderende bewerkingen uitvoeren, moeten worden toegevoegd aan de POS-schermindeling. Zie voor meer informatie [X/Z-rapporten instellen vanaf het POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
- In het fiscale integratievoorbeeld moeten deze bewerkingen worden vergeleken met de bijbehorende bewerkingen van het fiscale apparaat.

## <a name="fiscal-integration-samples-in-the-commerce-sdk"></a>Fiscale integratievoorbeelden in de Commerce-SDK

De volgende fiscale integratievoorbeelden zijn momenteel beschikbaar in de Commerce-SDK:

- [Voorbeeld van integratie van fiscale printer voor Italië](./emea-ita-fpi-sample.md)
- [Voorbeeld van integratie van fiscale printer voor Polen](./emea-pol-fpi-sample.md)
- [Voorbeeld van integratie van fiscale registratieservice voor Oostenrijk](./emea-aut-fi-sample.md)
- [Voorbeeld van integratie van fiscale registratieservice voor Tsjechië](./emea-cze-fi-sample.md)
- [Regeleenheidintegratievoorbeeld voor Zweden](./emea-swe-fi-sample.md)
- [Voorbeeld van integratie van fiscale registratieservice voor Duitsland](./emea-deu-fi-sample.md)
- [Voorbeeld van integratie van fiscale printer voor Rusland](./rus-fpi-sample.md)

De volgende functionaliteit voor fiscale integratie wordt ook geïmplementeerd met behulp van het fiscale integratieraamwerk, maar is kant-en-klaar beschikbaar en is niet opgenomen in de Commerce-SDK:

- [Fiscale registratie voor Brazilië](./latam-bra-commerce-localization.md#fiscal-registration-for-brazil)
- [Digitale handtekening voor Frankrijk](./emea-fra-cash-registers.md)

De volgende fiscale Integratiefunctionaliteit is ook beschikbaar in de Commerce-SDK, maar deze maakt op het moment geen gebruik van het fiscale integratieraamwerk. Migratie van deze functionaliteit naar het fiscale integratieraamwerk is gepland voor latere updates.

- [Digitale handtekening voor Noorwegen](./emea-nor-cash-registers.md)

De volgende verouderde functionaliteit voor fiscale integratie die beschikbaar is in de Commerce-SDK maakt geen gebruik van het raamwerk voor fiscale integratie en wordt afgeschaft in latere updates:

- [Regeleenheidintegratievoorbeeld voor Zweden (verouderd)](./retail-sdk-control-unit-sample.md)
- [Digitale handtekening voor Frankrijk (verouderd)](./emea-fra-deployment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
