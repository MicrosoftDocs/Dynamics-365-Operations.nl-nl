---
title: Aangepaste X++-scripts uitvoeren met nul downtime
description: In dit artikel wordt beschreven hoe u implementeerbare pakketten met aangepaste X++-scripts kunt uploaden en uitvoeren zonder uw systeem te onderbreken.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 3d00f842da69f889738fbcb293c7489bb018e810
ms.sourcegitcommit: f62c9b24c2205d03e2fd6e7c67f7b5c316233b12
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2022
ms.locfileid: "9598077"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Aangepaste X++-scripts uitvoeren met nul downtime

[!include [banner](../includes/banner.md)]

Met deze functie kunt u implementeerbare pakketten met aangepaste X++-scripts uploaden en uitvoeren zonder dat u Microsoft Dynamics Lifecycle Services (LCS) moet gebruiken of uw systeem moet onderbreken. U kunt kleine inconsistenties in gegevens daarom corrigeren zonder downtime te veroorzaken.

Het voordeel van het gebruik van een X++-script om inconsistenties in kleine gegevens te corrigeren, is dat alle gerelateerde tabellen indien nodig automatisch worden aangepast wanneer het script wordt uitgevoerd. Door deze benadering wordt de integriteit van de correctie gegarandeerd en wordt het risico op nieuwe inconsistenties beperkt.

> [!IMPORTANT]
> Deze functie is alleen bedoeld voor het corrigeren van kleine inconsistenties in gegevens. De functie mag niet worden gebruikt voor de volgende doeleinden of voor een ander doel:
>
> - Gegevensverzameling
> - Schemawijzigingen
> - Gegevensmigratie of andere langlopende processen
> - Correctie van gegevens die op andere wijze kunnen worden gecorrigeerd, zoals normale bedrijfsprocessen, consistentieprogramma's voor gegevens of andere selfserviceprogramma's
>
> Met deze functie kunnen geautoriseerde gebruikers entiteiten en bijbehorende records rechtstreeks wijzigen, zonder dat de bedrijfslogica moet worden uitgevoerd die aan deze entiteiten is gekoppeld. Deze wijzigingen kunnen leiden tot integriteitsproblemen met betrekking tot gegevens. Daarom kan uw organisatie vereisen dat u voor en/of na het uitvoeren van een script goedkeuring en aanmelding krijgt van interne en externe auditoren (of andere equivalente belanghebbenden). Om nalevingsredenen moeten wijzigingen die invloed hebben op sommige kenmerken ook openbaar worden gemaakt in externe rapporten (zoals financiële overzichten) of aan overheidsinstanties worden gerapporteerd. Uw organisatie is alleen verantwoordelijk voor wijzigingen die in de gegevens worden aangebracht via deze functie, goedkeuring en aanmelding of openbaarmaking van deze wijzigingen en naleving van toepasselijke wetten. U draagt alle risico's van het gebruik van deze functie.

Alle implementeerbare pakketten die naar het systeem worden geüpload, gaan via een verplichte werkstroom. Als veiligheidsmaatregel en om de scheiding van taken te garanderen, mag de gebruiker die een implementeerbaar pakket uploadt, het niet goedkeuren voor de volgende stappen in de werkstroom. Een andere gebruiker moet het goedkeuren. Nadat het pakket echter is goedgekeurd, kan de gebruiker die het heeft geüpload, de resterende stappen voltooien.

Het systeem vereist dat voor alle implementeerbare pakketten een testuitvoering wordt uitgevoerd. Voordat het script mag worden uitgevoerd op productiegegevens, moet een gebruiker valideren dat de uitvoer juist is door **Testlogboek accepteren** te selecteren. Als de uitvoer niet juist is, moet de gebruiker het pakket markeren als mislukt door **Verlaten** te selecteren. In dit geval mag het script niet worden uitgevoerd op productiegegevens.

Elk geüpload pakket wordt opgeslagen in het systeem en doorloopt een gedefinieerde werkstroom van gebeurtenissen. Voor elke gebeurtenis houdt het systeem een logboek bij met een tijdstempel en de identiteit van de persoon die de gebeurtenis heeft uitgevoerd. Op deze manier zorgt het systeem ervoor dat er een audittrail is.

Zoals in de volgende afbeelding wordt getoond, bevat het systeem details over de manier waarop elk implementeerbaar pakket in X++ is uitgevoerd en welke entiteiten betrokken waren.

![Pagina Scriptdetails.](media/script-details.png "Pagina Scriptdetails")

## <a name="assign-duties-to-users-to-control-access"></a>Taken aan gebruikers toewijzen om toegang te beheren

Deze functie biedt de volgende taken. Beheerders kunnen deze taken gebruiken om de toegang tot de functie te beheren.

- **Aangepaste scripts onderhouden**: deze taak biedt de mogelijkheid om aangepaste X++-scripts in omgevingen (acceptatietests door gebruiker \[UAT\] en productie) te uploaden, te testen, te controleren en uit te voeren.
- **Aangepaste scripts goedkeuren**: deze taak biedt de mogelijkheid om een geüpload aangepast X++-script goed te keuren. Goedkeuring is een verplichte stap voordat een script kan worden getest, geverifieerd en uitgevoerd.

Om het risico op kwaadwillende acties te minimaliseren, moet elk script expliciet worden goedgekeurd door een andere gebruiker dan de gebruiker die het heeft geüpload. Voordat u deze functie in uw organisatie kunt gebruiken, moet een beheerder de voorafgaande taken aan ten minste twee relevante en betrouwbare gebruikers toewijzen. Hoewel één gebruiker beide taken kan hebben, kan die gebruiker eigen scripts nog steeds niet goedkeuren.

## <a name="create-a-deployable-package"></a>Een implementeerbaar pakket maken

Voor de functie is een regelmatig implementeerbaar pakket nodig dat kan worden gemaakt in Visual Studio. Zie [Implementeerbare pakketten van modellen maken](../deployment/create-apply-deployable-package.md) voor instructies.

Uw implementeerbare pakket mag precies één uitvoerbare X++-klasse bevatten. Dit houdt in dat het pakket één klasse moet hebben die een methode bevat met de volgende handtekening.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> De naam van de hoofdmethode moet in kleine letters zijn.

## <a name="code-example"></a>Codevoorbeeld

In het volgende codevoorbeeld ziet u hoe een implementeerbaar pakket kan worden gestructureerd.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Best practices

De volgende lijst beschrijft enkele best practices voor het succesvol schrijven, implementeren en uitvoeren van een script. De lijst is niet volledig en dient slechts als richtlijn.

- **Schrijf** een succesbericht aan het einde van het script. Op deze manier kunt u zien dat het script zonder uitzonderingen is uitgevoerd.
- **Voeg** expliciete verwerking van het transactiebereik toe.
- **Gebruik** bestaande bedrijfslogica, zoals `update()`-methoden, maar omzeil bedrijfslogica **niet** door de methoden `doUpdate()`, `doInsert()` en `doDelete()` te gebruiken. Door deze benadering zorgt u ervoor dat afhankelijke gegevens op de juiste manier worden verwerkt. Bovendien neemt het risico op inconsistenties in gegevens aanzienlijk af.
- **Bevestig** de bedrijfscontext. Door deze benadering worden veelvoorkomende fouten tijdens een scriptuitvoering getoond. Zo wordt bijvoorbeeld aangegeven of het script wordt uitgevoerd in het verkeerde bedrijf.
- **Bevestig** dat het aantal beïnvloede records overeenkomt met uw verwachtingen. Door deze benadering wordt duidelijk of gegevens onverwacht in het systeem zijn verplaatst terwijl het script werd voorbereid.
- **Gebruik** voor elk script unieke klassenamen (bijvoorbeeld door een verwijzing naar een werkitem in de naam op te nemen). Zo voorkomt u problemen met namen wanneer u het script uploadt. Als een nieuwe iteratie van een script vereist is, moet u er een nieuwe naam aan geven.
- **Test** elk script eerst in een niet-productieomgeving. Test op het bedoelde effect en op onbedoelde neveneffecten op gerelateerde gegevens. Controleer of alle betrokken bedrijfsprocessen later succesvol en volledig kunnen worden voltooid.

## <a name="upload-and-run-a-deployable-package"></a>Een implementeerbaar pakket uploaden en uitvoeren

Gebruik de volgende procedure om een script te uploaden en uit te voeren.

1. Ga in uw app voor financiën en bedrijfsactiviteiten naar **Systeembeheer \> Periodieke taken \> Database \> Aangepaste scripts**.
1. Selecteer **Uploaden**.
1. Selecteer het implementeerbare pakket dat u hebt gemaakt, zoals eerder in dit artikel is beschreven. U wordt gevraagd het doel van het script op te geven.
1. Het script moet nu worden goedgekeurd door een andere gebruiker dan de gebruiker die het heeft geüpload. De fiatteur moet de volgende stappen uitvoeren:

    1. Ga naar **Systeembeheer \> Periodiek \> Database \> Aangepaste scripts**.
    1. Selecteer het script dat u wilt goedkeuren en selecteer vervolgens **Details**.
    1. Selecteer in het actievenster op het tabblad **Proceswerkstroom** in de groep **Start** **Goedkeuren** of **Afwijzen**. Als u **Goedkeuren** selecteert, wordt het script gemarkeerd als goedgekeurd en ontgrendeld voor testen. Als u **Afwijzen** selecteert, wordt het script vergrendeld. In beide gevallen wordt de gebeurtenis geregistreerd en wordt een kopie van het script in het systeem bewaard.

1. Het script moet worden getest om ervoor te zorgen dat het doet waarvoor het bedoeld is. De tester kan dezelfde zijn als de uploader of de fiatteur of kan een derde gebruiker zijn die de vereiste machtigingen heeft. De tester moet de volgende stappen uitvoeren:

    1. Ga naar **Systeembeheer \> Periodiek \> Database \> Aangepaste scripts**.
    1. Selecteer het script dat u wilt testen en selecteer vervolgens **Details**.
    1. Selecteer in het actievenster op het tabblad **Proceswerkstroom** in de groep **Test** de optie **Test uitvoeren**. Het script wordt uitgevoerd binnen een tijdelijke transactie die automatisch wordt afgebroken terwijl het verschillende logboeken en SQL-instructies verzamelt.
    1. Wanneer de uitvoering van het script gereed is, bekijkt u de logboeken en controleert u of de resultaten aan uw verwachtingen voldoen. Volg één van deze stappen:

        - Als u tevreden bent met het testresultaat, selecteert u **Testlogboek accepteren** in de groep **Test** op het tabblad **Proceswerkstroom** van het actievenster, zodat het script kan worden uitgevoerd. In het gebeurtenislogboek wordt aangegeven dat het script is getest en wie het heeft getest en wanneer.
        - Als u tevreden bent met het testresultaat, selecteert u **Verlaten** in de groep **Einde** op het tabblad **Proceswerkstroom** van het actievenster om te voorkomen dat het script wordt uitgevoerd. Het systeem houdt een kopie van het script samen met een logboek van de historie bij.

1. Wanneer u zeker weet dat het script aan uw verwachtingen voldoet, selecteert u **Uitvoeren** in de groep **Uitvoeren** op het tabblad **Proceswerkstroom** van het actievenster om het script uit te voeren. Deze opdracht doet hetzelfde als de vorige testuitvoering, maar de transactie wordt aan het einde vastgelegd.
1. Als de uitvoering van het script gereed is, controleert u het resultaat en bevestigt u dat het script werkte zoals bedoeld. Volg één van deze stappen:

    - Als u tevreden bent met het resultaat, selecteert u **Doel opgelost** in de groep **Einde** op het tabblad **Proceswerkstroom** van het actievenster. In het gebeurtenislogboek wordt aangegeven dat het script succesvol is uitgevoerd en wie het script heeft gecontroleerd en wanneer. Het script wordt opgeslagen, maar is nu vergrendeld en kan niet meer worden uitgevoerd.
    - Als u tevreden bent met het resultaat, selecteert u **Doel niet opgelost** in de groep **Einde** op het tabblad **Proceswerkstroom** van het actievenster. In het gebeurtenislogboek wordt aangegeven dat het script niet heeft gedaan waarvoor het bedoeld is en wie het script heeft uitgevoerd en wanneer. Het script wordt opgeslagen, maar is nu vergrendeld en kan niet meer worden uitgevoerd. De scriptactie wordt echter niet automatisch ongedaan gemaakt. U moet mogelijk een nieuw script schrijven, importeren en uitvoeren om het effect van het mislukte script op uw systeem ongedaan te maken.

Uw selectie in de laatste stap bepaalt de definitieve status voor het script. U kunt het proces indien nodig herhalen.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Een implementeerbaar pakket via LCS uploaden en uitvoeren

In plaats van uw implementeerbare pakket te implementeren via de gebruikersinterface voor uw app voor financiën en bedrijfsactiviteiten, zoals in het vorige gedeelte is beschreven, kunt u het naar LCS uploaden en de normale procedure gebruiken om het te implementeren. Zie voor meer informatie [Implementeerbare pakketten installeren vanaf de opdrachtregel](../deployment/install-deployable-package.md).

Deze benadering brengt minder beperkingen met zich mee, maar levert ook minder beveiliging tegen fouten op. Aangezien alle servers opnieuw moeten worden opgestart, leidt dit ook tot downtime.

