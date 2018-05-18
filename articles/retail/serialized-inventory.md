---
title: POS-verbeteringen voor geserialiseerde producten
description: Dit onderwerp bevat een overzicht van verbeteringen die zijn aangebracht in geserialiseerde producten om u tijd te laten besparen en productiever te laten werken.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 74a27761c065e475fa7c10c5812f0307df9f570e
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---

# <a name="pos-improvements-for-serialized-products"></a>POS-verbeteringen voor geserialiseerde producten

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Overzicht 
Op basis van de instellingen in Detailhandel Hoofdkantoor kunnen producten als geserialiseerde producten of niet-geserialiseerde producten worden geclassificeerd. Wanneer producten geserialiseerd worden, kan aan elk artikel een uniek nummer worden toegewezen waarmee garanties worden bijgehouden, artikelen worden getraceerd en eigendom wordt bevestigd. Hoewel de mogelijkheid om serienummers voor geserialiseerde producten op te geven, bestond in MPOS (Modern Point of Sale) en CPOS (Cloud Point of Sale), zijn enkele verbeteringen doorgevoerd om kassamedewerkers tijd te laten besparen en hun productiviteit te verhogen.  

## <a name="pos-improvements"></a>POS-verbeteringen

- **Serienummers zijn pas bij het uitchecken vereist** : voorheen moest een kassamedewerker bij het toevoegen van een geserialiseerd product aan de transactie een serienummer opgeven. Deze vereiste werd een probleem in clientelingscenario's als kassamedewerkers en verkoopmedewerkers mogelijkheden voor meerverkoop hadden. Tot de betalingsstap werden de producten vaak bijgewerkt in de winkelwagen. Elke keer dat een kassamedewerker een nieuw product toevoegde, werd hij of zij gevraagd om het serienummer. Het dialoogvenster voor serienummers bevat nu een knop **Later toevoegen**. Verkoopmedewerkers kunnen nu dus het artikel toevoegen aan de transactie en later het serienummer opgeven. Verkoopmedewerkers kunnen geserialiseerde artikelen snel toevoegen aan en vervangen in de winkelwagen en vervolgens vlak voor het uitchecken het serienummer opgeven. Als het serienummer niet wordt opgegeven voor een geserialiseerde product, ontvangt een kassamedewerker die de transactie probeert af te handelen een foutbericht. In dit bericht wordt aangegeven dat de kassamedewerker de ontbrekende serienummers moet opgeven voordat hij of zij kan doorgaan.

    Voor elk geserialiseerd artikel waarvoor het serienummer is overgeslagen, verschijnt een opmerking onder de transactieregel. Dit commentaar geeft aan dat het serienummer voor het artikel nog niet is opgegeven. De kassamedewerker kan dus snel de artikelen vinden waarvoor een serienummer ontbreekt.

    Met een nieuwe bewerking **Serienummer toevoegen** wordt ook het serienummer opgegeven voor artikelen waarvoor een serienummer ontbreekt. Nadat het serienummer is opgegeven, kan het niet meer worden bewerkt. De kassamedewerker moet de regel annuleren en het product opnieuw toevoegen. 
    
- **Serienummers zijn niet vereist om klantorders plaatsen**: klantorders kunnen worden geplaatst in de ene winkel en worden afgehandeld in een andere winkel. Een kassamedewerker die een klantorder plaatst, hoeft het serienummer niet op te geven. Het serienummer wordt opgegeven tijdens de orderverzameling of het ophalen. Er moet echter een serienummer worden opgegeven voor alle regelartikelen waarvoor het leveringstype **Uitvoeren** is geselecteerd. Anders kan de transactie niet worden voltooid.    
- **Geserialiseerde producten worden niet samengevoegd in het transactiescherm**: via de instelling **Producten samenvoegen** in de veldgroep **Terminal** op de pagina **Functionaliteitsprofiel** kunt u dezelfde niet-geserialiseerde producten samenvoegen in het transactiescherm. Wanneer dezelfde producten worden samengevoegd, zijn ze gemakkelijker te zien in het transactieraster. Omdat serienummers doorgaans uniek zijn en verkoopmedewerkers pas serienummers hoeven in te voeren bij het uitchecken, is de instelling **Producten samenvoegen** niet van toepassing op geserialiseerde producten. Geserialiseerde producten worden dus niet samengevoegd in het transactiescherm als de instelling **Producten samenvoegen** is geselecteerd.
- **Mogelijkheid om de journalen te doorzoeken op serienummer**: de journalen kunnen nu ook worden doorzocht op serienummers. Hiervoor opent u de bewerking Journalen en kiest u de knop Geavanceerd zoeken op de appbalk. Met de knop Filter toevoegen kunt u ook een filter toepassen om op de serienummers te zoeken.

