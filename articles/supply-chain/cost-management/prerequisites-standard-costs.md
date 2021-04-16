---
title: Overzicht van Vereisten voor standaardkosten
description: In dit onderwerp worden de basisstappen voor het gebruik van standaardkosten besproken.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f80ecc611e68210e24e59b696724e1bc9c3a06
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809657"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Overzicht van Vereisten voor standaardkosten

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de basisstappen voor het gebruik van standaardkosten besproken. Volgende stappen zijn afhankelijk van de bedrijfsactiviteiten. De stappen verschillen bijvoorbeeld voor een niet-productieomgeving, een productieomgeving waarin routeringen niet worden gebruikt en een productieomgeving met routeringen. 

Voer de onderstaande stappen uit om standaardkosten in te stellen.

**1. Maak een artikelmodelgroep voor standaardkosten.**

Gebruik de pagina **Artikelmodelgroepen** om een nieuwe groep voor standaardkosten te maken en om een voorraadmodel van **Standaardkosten** toe te wijzen. De artikelmodelgroep moet een duidelijke id hebben, zoals **Stdkosten**. Schakel de selectievakjes in om aan te geven dat de groep financiële negatieve voorraad moet toestaan en dat deze fysieke voorraad en financiële voorraad moet boeken. Deze standaardkostengroep wordt aan artikelen toegewezen.

**2. Definieer grootboekrekeningen die aan standaardkostprijsafwijkingen zijn gekoppeld.** 

Gebruik de pagina **Rekeningschema** om grootboekrekeningen te definiëren die zijn gekoppeld aan standaardkostprijsafwijkingen. Deze grootboekrekeningen moeten worden gedefinieerd voordat ze kunnen worden toegewezen op de pagina **Boeking**. De grootboekrekeningen kunnen artikelgroepen en kostengroepen reflecteren.

**3. Wijs grootboekrekeningen toe aan artikelboekingen die zijn gekoppeld aan standaardkostprijsafwijkingen.** 

Gebruik de pagina **Boeking** om de grootboekrekeningen toe te wijzen die zijn gekoppeld aan standaardkostprijsafwijkingen. U kunt een grootboekrekening van een afwijking per artikel (of artikelgroep) en per kostengroep (of kostengroeptype) opgeven of u kunt opgeven dat de grootboekrekening van toepassing is op alle artikelen en kostengroepen. Deze opties komen overeen met de kostenrelaties voor tabellen, groepen en alles. 

Voordat u artikelboekingsregels definieert, gebruikt u de pagina **Transactiecombinaties** om kostenrelaties (voor tabellen, groepen en alles) te activeren.

**4. Definieer voorraadparameters die aan standaardkosten zijn gekoppeld.** 

-  Gebruik het tabblad **Voorraadboekhouding** op de pagina **Instelling voor boekhoudingbeleid voorraad > Parameters** voor het definiëren van twee kostenbeheerparameters die aan standaardkosten zijn gerelateerd.

    -  Selecteer in het veld **Kostenanalyse** **Geen** of **Subgrootboek**. Als u **Subgrootboek** selecteert, is de kostenanalyse een *actieve* kostenanalyse. Een actieve kostenanalyse is cruciaal voor het berekenen, achterhalen en weergeven van kostengroepsegmentatie over een productstructuur op meerdere niveaus voor standaardkostenartikelen. Wanneer de kostenanalyse actief is, kunt u voorraad, OHW (onderhanden werk) en kosten van verkochte goederen rapporteren en analyseren per kostengroep op één niveau, meerdere niveaus of totale indeling. Wanneer de kostenanalyse actief is en u kosten van een gefabriceerd artikel activeert, wordt de kostengroepsegmentatie opgeslagen in de kostenrecord van het artikel. 

    -  Als u **Geen** selecteert wordt geen kostengroepsegmentatie onderhouden voor standaardkostenartikelen. Met andere woorden: de standaardkosten van een gefabriceerd artikel worden berekend en onderhouden als één bedrag zonder kostengroepsegmentatie. De kostenbijdragen van gefabriceerde onderdelen worden samengevoegd tot het ene bedrag.

-  Selecteer in het veld **Afwijkingen van standaard** **Samengevat** of **Per kostengroep**. Als u **Per kostengroep** selecteert, kunt u inkoopprijsafwijkingen en productieafwijkingen per kostengroep identificeren. U kunt ook de vier typen productieafwijkingen identificeren: partijgrootte, hoeveelheid, prijs en vervanging. Als u **Samengevat** selecteert, kunt u geen afwijkingen per kostengroep identificeren en kunt u niet de vier typen productieafwijkingen identificeren. U kunt alleen een samengevatte productieafwijking weergeven.

-  Het beleid voor afwijking op standaardkosten werkt onafhankelijk van het kostenanalysebeleid. Met andere woorden: u kunt een kostenanalysebeleid van **geen** selecteren en afwijkingen per kostengroep selecteren, zodat productieafwijkingen per kostengroep toch worden geregistreerd.

**5. Maak kostprijsberekeningsversies voor standaardkosten.** 

Gebruik de pagina **Instellingen kostprijsberekeningsversie** om een of meer kostprijsberekeningsversies voor standaardkosten te maken. Elke kostprijsberekeningsversie moet worden aangegeven door een kostprijsberekeningstype van **standaardkosten** en moet kostengegevens in de inhoud toestaan.

**6. Bereid een bestaande klant voor om standaardkosten te gebruiken.** 

Klanten die hun bestaande artikelen naar een standaardkostenvoorraadmodel willen wijzigen, moeten de pagina **Standaardkostprijsconversies** gebruiken.


<a name="related-topics"></a>Verwante onderwerpen
--------

[Overzicht van standaardkostprijsconversie](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Weblogs

#### <a name="community-blogs"></a>Community-blogs

- [Hoe u standaardkosten instelt voor directe materialen in Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Standaard directe arbeidskosten in Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]