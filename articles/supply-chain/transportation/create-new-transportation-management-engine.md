---
title: Een nieuwe transportbeheerengine maken
description: In dit onderwerp wordt beschreven hoe u een nieuwe engine voor transportbeheer maakt in Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSGenericEngine, TMSRateEngine, TMSMileageEngine, TMSEngineParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 51661
ms.assetid: 0473acef-755e-4b42-acf5-5e5aa902dc0e
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88661b6a974e2bd60f78e38d49a08d3290008b8b
ms.sourcegitcommit: 614d79cba238e466d445767a7d0a012e785a9861
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/19/2021
ms.locfileid: "7651968"
---
# <a name="create-a-new-transportation-management-engine"></a>Een nieuwe transportbeheerengine maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een nieuwe engine voor transportbeheer maakt in Dynamics 365 Supply Chain Management. 

Met engines voor Transportbeheer (TMS) wordt de logica gedefinieerd die wordt gebruikt om transporttarieven in Transportbeheer te genereren en te verwerken. Supply Chain Management biedt verschillende typen engines waarmee verschillende parameters worden berekend, zoals tarieven, transittijden en het aantal zones dat tijdens transit wordt doorkruist. In dit artikel wordt uitgelegd hoe u de ontwikkelomgeving Microsoft Visual Studio samen met ontwikkelprogramma's van Supply Chain Management gebruikt om een nieuwe TMS-engine te maken en te implementeren en hoe u vervolgens de engine in Operations instelt. Zie [Engines voor Transportbeheer](transportation-management-engines.md) voor meer informatie over engines.

## <a name="create-a-new-tms-engine"></a>Een nieuwe TMS-engine maken

In deze sectie wordt uitgelegd hoe u een klassebibliotheek maakt met een implementatie van een TMS-engine en hoe u ernaar verwijst vanuit een Supply Chain Management-model.

1. Om uw nieuwe engines te kunnen implementeren, moet u een model hebben dat de engines bevat. Klik in het menu **Dynamics 365** &gt; **Modelbeheer** op **Model maken** om een nieuw model te maken. Geef het model op de eerste pagina van de wizard **Model maken** de naam **TMSEngines**. 

   [![Een model maken.](./media/012.png)](./media/012.png)

2. Selecteer op de volgende pagina **Nieuw pakket maken**. 

   [![Een nieuw pakket maken.](./media/021.png)](./media/021.png)

3. Selecteer op de volgende pagina het model **ApplicationSuite** waarnaar moet worden verwezen. (Het model **ApplicationPlatform** is vooraf geselecteerd.) 

   [![Het model selecteren waarnaar moet worden verwezen.](./media/032.png)](./media/032.png)

4. Klik op de volgende pagina op **Voltooien** om het maken van het nieuwe model te bevestigen. 

   [![Het maken van het model voltooien.](./media/042.png)](./media/042.png)

5. Maak in een nieuwe oplossing een nieuw Supply Chain Management-project en geef het project de naam **TMSThirdParty**. Stel in de projecteigenschappen het model van het project in op **TMSEngines**.
6. Voeg een nieuwe C\#-klassebibliotheek aan uw oplossing toe en geef deze de naam **ThirdPartyTMSEngines**.
7. Voeg in het project ThirdPartyTMSEngines verwijzingen toe naar specifieke assembly's van Supply Chain Management:
   -   Toepassingsassembly's waarmee naar X++-typen kan worden verwezen. Deze assembly's kunt u vinden op de volgende locaties. \[Hoofdmap van pakketten\] is het pad naar de locatie waar alle geïmplementeerde assembly's worden geplaatst, zoals C:\\Pakketten.

        ```xpp
        [Packages root]\ApplicationPlatform\bin\Dynamics.AX.ApplicationPlatform.dll
        [Packages root]\ApplicationFoundation\bin\Dynamics.AX.ApplicationFoundation.dll
        [Packages root]\ApplicationSuite\bin\Dynamics.AX.ApplicationSuite.dll
        ```
        
   -   Framework-assembly's die toegang geven tot gegevens, LINQ en hulpfuncties. Al deze assembly's kunt u vinden in \[Hoofdmap pakketten\]\\bin.

        ```xpp 
        Microsoft.Dynamics.ApplicationPlatform.Environment.dll
        Microsoft.Dynamics.AX.Data.Core.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.AdoNet.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Interface.dll
        Microsoft.Dynamics.AX.Framework.Linq.Data.Msil.dll
        Microsoft.Dynamics.AX.Server.Core.dll
        Microsoft.Dynamics.AX.Xpp.AxShared.dll
        Microsoft.Dynamics.AX.Xpp.Support.dll
        ```

   -   De kern-TMS-assembly (die engines bevat) en de TMS-basis-asassembly (die onder andere helpers, constanten en klassedefinities voor gegevensoverdracht bevat). Deze assembly's kunt u vinden op de volgende locaties.

        ```xpp
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.dll
        [Packages root]\ApplicationSuite\bin\Microsoft.Dynamics.AX.Tms.Base.dll
        ```
8. Wijzig de naam van de C\#-klasse die automatisch wordt gegenereerd in het project ThirdPartyTMSEngines in **SampleRatingEngine**.
9. De engine implementeren. Omdat we in dit voorbeeld een tariefengine maken, nemen we de basisklasse over voor tariefengines. Met de basisklasse wordt het grootste deel van de interface van de tariefengine **(TMSFwkIRateEngine)** geïmplementeerd. We hoeven alleen maar de tariefmethode te implementeren. Om dit voorbeeld eenvoudig te houden, registreren we met deze methode een in code opgenomen tarief van 100. U kunt engines maken waarmee alle engine-interfaces worden geïmplementeerd, zoals **TMSFwkIAccessorialEngine**. Alle engine-interfaces worden in X++ gedefinieerd.

    ```xpp
    namespace ThirdPartyTMSEngines
    {
        using Dynamics.AX.Application;
        using Microsoft.Dynamics.Ax.Tms.Base.Data;
        using Microsoft.Dynamics.Ax.Tms.Base.Utility;
        using Microsoft.Dynamics.Ax.Tms.Bll;
        using System.Xml.Linq;
        public class SampleRatingEngine : BaseRateEngine
        {
            public override RatingDto rate(TmsTransactionFacade transactionFacade, XElement shipment, TMSRateMasterCode rateMasterCode)
            {
               XElement re = shipment.RetrieveOrCreateRatingEntity(this.RatingDto);
               re.AddRate(TmsRateType.Rate, 100);
               return this.RatingDto;
            }
        }
    }
    ```

10. Bouw de oplossing.
11. Voeg een nieuwe verwijzing naar het project TMSThirdParty toe. De verwijzing moet verwijzen naar het project ThirdPartyTMSEngines. Als u klaar bent, moet uw oplossing er als volgt uitzien. 

    [![De oplossing, die een verwijzing naar het project TMSThirdParty bevat.](./media/052.png)](./media/052.png)

12. Bouw de oplossing. Controleer of de nieuwe bibliotheek wordt weergegeven in het knooppunt **Verwijzingen** in Toepassingsverkenner. 

    [![De nieuwe bibliotheek in het knooppunt Verwijzingen van Toepassingsverkenner.](./media/061.png)](./media/061.png)

## <a name="deploy-the-tms-engine-as-a-package"></a>De TMS-engine als een pakket implementeren

Een manier om TMS-engines van derden te implementeren is via een implementatiepakket. Deze benadering wordt aangeraden in een productieomgeving. In een ontwikkelomgeving kunt u de assembly's handmatig kopiëren, zoals wordt beschreven in de volgende sectie, 'Een TMS-engine instellen in Supply Chain Management.' Ga als volgt te werk om de engine als een pakket te implementeren:

1. Klik in het menu **Dynamics 365** &gt; **Implementeren** op <strong>Implementatiepakket maken</strong>.
2. Selecteer in het dialoogvenster **Implementatiepakket maken** het TMSEngines-model en voer het pad in waar u de pakketbestanden wilt opslaan. 

   [![Het TMSEngines-model selecteren.](./media/071.png)](./media/071.png)

3. U kunt het pakket nu in de doelomgeving implementeren. Zie [Een implementeerbaar pakket installeren](../../fin-ops-core/dev-itpro/deployment/install-deployable-package.md) voor een zelfstudie.

## <a name="set-up-the-tms-engine-in-supply-chain-management"></a>De TMS-engine instellen in Supply Chain Management

In deze sectie wordt uitgelegd hoe u Supply Chain Management instelt om een TMS-engine te gebruiken en wordt getoond hoe de nieuwe engine die we hebben gemaakt, wordt gebruikt bij tarieven zoeken. In het voorbeeld in deze sectie wordt het demogegevensbedrijf USMF gebruikt.

1. Maak een nieuwe engine zoals beschreven in de sectie 'Een nieuwe TMS-engine maken'.
2. Bouw uw oplossing.
3. Kopieer de resulterende assembly naar de binaire locatie van de Supply Chain Management-server, \[AOSWebRoot\]bin. **Let op:** deze stap is alleen relevant in een ontwikkelomgeving. In een productieomgeving moet u de implementatie uitvoeren via een implementatiepakket. Zie de vorige sectie 'De TMS-engine als een pakket implementeren' voor instructies.
4. Maak in Supply Chain Management op de pagina **Tariefengine** een nieuwe tariefengine. De engine moet naar de engine-assembly verwijzen die wordt geproduceerd door de engineklassebibliotheek en de engineklasse te bouwen die u hebt geïmplementeerd. 

   [![Een nieuwe tariefengine maken op de pagina Tariefengines.](./media/081.png)](./media/081.png)

5. Maak een vervoerder die gebruikmaakt van de tariefengine Voorbeeld. Omdat onze engine geen gegevens gebruikt, hoeft u geen tariefmodel toe te wijzen. 

   [![Een nieuwe vervoerder maken.](./media/092.png)](./media/092.png)

6. Klik op de pagina **Workbench tariefroute** op **Tariefwinkel**. U moet een tarief van 100,00 zien van SampleCarrier, zoals wordt weergegeven in de volgende schermopname. In dit voorbeeld zoeken we naar tarieven voor een route van magazijn 24 naar klant US-004. Omdat het tarief echter is gecodeerd, wordt altijd een tarief van 100,00 weergegeven.

   [![Workbench tariefroute.](./media/101.png)](./media/101.png)

## <a name="tips-and-tricks"></a>Tips en trucs

- Als u ontwikkelprogramma's voor Supply Chain Management gebruikt, is het handig om een nieuw project aan uw oplossing toe te voegen. Als u dit project instelt als uw opstartproject en een foutopsporingssessie start, kunt u in zowel X++- als C\#-code fouten opsporen in dezelfde foutopsporingssessie.
- Telkens wanneer u uw ThirdPartyTMSEngines-project wijzigt en opnieuw compileert, moet u de resulterende assembly handmatig naar de binaire locatie kopiëren of via een implementatiepakket implementeren. Anders wordt er voor de uitvoering mogelijk een verouderde assembly gebruikt.
- Nadat u TMS-specifieke bewerkingen in Supply Chain Management hebt uitgevoerd, kan het IIS-werknemersproces (Internet Information Services) de ThirdPartyTMSEngines-assembly mogelijk vergrendelen, zodat de assembly niet kan worden bijgewerkt. Start in dat geval het w3svc-proces opnieuw op.

### <a name="whitepaper"></a>Whitepaper

Download de volgende whitepaper (geschreven ter ondersteuning van AX2012, maar is nog steeds van toepassing op Dynamics 365 Supply Chain Management) voor meer informatie.

- [Engines voor Transportbeheer implementeren en gebruiken](https://download.microsoft.com/download/b/5/f/b5ff8fef-3918-4c1d-92d5-b67eb0971684/ImplementingAndDeployingTransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]