---
title: Automatisering van incassoproces
description: In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit vereist is of een aanmaningsbrief naar de klant moet worden verzonden.
author: JodiChristiansen
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 59db852024faf457db7ac145b67619b31555aaf2
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486864"
---
# <a name="collections-process-automation"></a>Automatisering van incassoproces

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u strategieën voor het incassoproces instelt waarmee automatisch klantfacturen worden geïdentificeerd waarvoor een e-mailherinnering of incasso-activiteit (zoals een telefoongesprek) vereist is of een aanmaningsbrief naar de klant moet worden verzonden. 

Organisaties besteden vaak veel tijd aan het doorzoeken van verouderde balansrapporten, klantrekeningen en openstaande facturen om te bepalen met welke klanten contact moet worden opgenomen over een openstaande factuur of een openstaand rekeningsaldo. Dit onderzoek kost tijd die de incassomedewerker ook had kunnen besteden aan het communiceren met klanten om achterstallige saldi te innen of factuurgeschillen te verhelpen. Door het incassoproces te automatiseren, kunt u een strategie instellen voor uw incassoproces. Zo kunt u incasso-activiteiten consistent toepassen door aangepaste e-mailherinneringen of een geprogrammeerd proces voor het verzenden van aanmaningen te bieden. 

## <a name="collections-process-setup"></a>Instelling van incassoproces
U kunt de pagina **Instelling van incassoproces** (**Crediteringen en aanmaningen > Instellingen > Instelling van incassoproces**) gebruiken om een automatisch incassoproces te maken waarmee activiteiten worden gepland, e-mailberichten worden verzonden en klantaanmaningen worden gemaakt en geboekt. De processtappen zijn gebaseerd op de leidende of oudste openstaande factuur. In elke stap wordt deze factuur gebruikt om te bepalen welke communicatie of activiteit voor een bepaalde klant moet plaatsvinden.  

Incassoteams verzenden doorgaans een vroege kennisgeving met betrekking tot elke openstaande factuur, zodat een klant op de hoogte wordt gebracht van het moment waarop de factuur moet worden betaald. U kunt de selectie **Voor de aanmaning** instellen om één stap in elke proceshiërarchie toe te staan voor elke factuur wanneer de timing van de factuur die stap bereikt.

### <a name="process-hierarchy"></a>Proceshiërarchie
Elke klantverzameling kan slechts aan één proceshiërarchie worden toegewezen. De hiërarchiepositie van deze stap geeft aan welk proces prioriteit krijgt als een klant is opgenomen in meerdere verzamelingen waaraan een proceshiërarchie is toegewezen. De verzameling-id bepaalt welke klanten worden toegewezen aan het proces. Een hiërarchie die is ingesteld, kan slechts aan één automatisering worden toegewezen.

De stille dagen worden gebruikt om ervoor te zorgen dat niet te vaak contact met een klant wordt opgenomen door het geautomatiseerde proces. Als het aantal stille dagen bijvoorbeeld op twee is ingesteld, wordt door het geautomatiseerde proces gedurende ten minste twee dagen geen contact met de klant gemaakt, ook niet als de oorspronkelijke leidende factuur volledig is vereffend. 

Als u klanten wilt uitsluiten van de procesautomatisering als het naar ouderdom gerangschikt saldo van klantouderdomssaldo van de klant of het factuurbedrag lager is dan een gedefinieerde waarde, selecteert **Ouderdomssaldo van de klant kleiner dan** of **Factuurbedrag lager dan** in het veld **Uitsluiten van proces** en voert u de bedragwaarde in.

Markeer **Voorspelling gebruiken** incassoactiviteiten te maken met behulp van voorspellingen van klantbetalingen. De gemaakte activiteiten maken gebruik van de activiteitssjabloon van **Betalingsvoorspellingen** op de pagina **Parameters van module klanten**, tabblad **Automatisering van incassoproces**. 

### <a name="process-details"></a>Procesgegevens
Klik op **Nieuw** om een nieuw procesdetail aan de hiërarchie toe te voegen. De **Beschrijving** wordt gebruikt om het doel of de naam van de stap in de hiërarchie aan te duiden. Selecteer het **Actietype** om vast te leggen in welke stap een activiteit wordt gemaakt, een e-mailbericht wordt verzonden of een aanmaning wordt gemaakt. 

- Het **Bedrijfsdocument** bepaalt welke sjabloon wordt gebruikt om het actietype te maken. Dit document kan een sjabloon voor een activiteit, een e-mailsjabloon of een aanmaning die naar iedere klant worden gezonden, zijn. De automatisering van het incassoproces maakt alleen incassobrieven per klant, ongeacht de instellingen van andere incassoparameters.
- **Wanneer** legt de de processtap vast die vóór of na de relevante (oudste) factuurvervaldatum wordt uitgevoerd, en wordt gebruikt samen met het getal dat wordt weergegeven in de kolom **Dagen in relatie tot vervaldatum factuur**. 
- Markeer de optie **Vóór aanmaning** om een actie te maken voor elke factuur in één stap in een proceshiërarchie. Acties vóór aanmaning zijn meestal een vroege kennisgeving met betrekking tot openstaande facturen, zodat een klant op de hoogte kan worden gebracht van het moment waarop de factuur moet worden betaald. Er kan per hiërarchie slechts één activiteit vóór aanmaning worden gemarkeerd. Wanneer u een actietype voor e-mail selecteert, wordt de ontvanger gebruikt om te bepalen of het e-mailberichten wordt verstuurd naar een klant, verkoopgroep of incassomedewerker. 
- De waarde in het veld **Contactpersoon voor zakelijk doel** bepaalt vervolgens welke contactpersoon van de account van die klant de communicatie ontvangt.

### <a name="business-document-details"></a>Bedrijfsdocumentdetails
De details van bedrijfsdocumenten zijn afhankelijk van het actietype dat is geselecteerd in de procesdetails. Wanneer het actietype een activiteit is, worden de details van de activiteitsjabloon weergegeven. Deze gegevens omvatten de naam van de activiteitsjabloon, het type activiteit dat wordt gemaakt, het doel van de activiteit, het aantal dagen dat is gepland om de activiteit te voltooien en de details van de activiteit. Deze activiteit wordt vervolgens gekoppeld aan de leidende factuur die de ontvanger vertelt over de actie die nodig is om de activiteit te voltooien.

Als het actietype een e-mailbericht in de procesgegevens is, bevat deze sectie twee sneltabbladen. Het eerste wordt gebruikt voor het definiëren van de sjabloon-id, e-mailbeschrijving, standaardtaal, de gebruikersnaam die wordt toegewezen aan e-mailberichten die automatisch worden verzonden en het e-mailadres van de gekoppelde afzenders. Op het tweede sneltabblad kan de hoofdtekst van het e-mailbericht worden gemaakt nadat de waarden in de velden **Taal** en **Onderwerp** zijn opgeslagen via **Bewerken**. Hierdoor wordt een venster geopend waarin HTML-inhoud kan worden geüpload. 

> [!Note]
> U kunt een Outlook-e-mailbericht opslaan met de tekst van de communicatie in HTML-indeling. U kunt de berichtinhoud vervolgens uploaden om de sjabloon te implementeren. <br> <br> Als het actietype Aanmaning is geselecteerd, bevat d instellingenpagina geen sectie voor bedrijfsdocumentdetails.

Met de knop **Historie incassoproces** kunt u de recente historie voor de geselecteerde proceshiërarchie weergeven. 

Klik op de actie **Toewijzing van incassoproces** om klanten weer te geven die aan een incassoproces zijn toegewezen. Gebruik **Preview van klanttoewijzing** om de hiërarchie weer te geven waaraan een bepaalde klant is toegewezen. Gebruik op de actie **Preview van klanttoewijzing** om de klanten te bekijken die bij uitvoering worden toegewezen aan een hiërarchie. Klik op **Handmatige toewijzing** om klanten weer te geven die handmatig aan een proces zijn toegewezen of om klanten te selecteren die aan een proces moeten worden toegewezen.

Klik op de actie **Processimulatie** om een voorbeeld weer van de acties die worden gemaakt als de geselecteerde procesautomatisering op dit moment wordt uitgevoerd. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
