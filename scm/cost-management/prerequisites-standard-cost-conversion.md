---
title: Vereisten voor een standaardkostprijsconversie
description: In dit onderwerp worden de taken besproken die moeten worden uitgevoerd voordat u een standaardkostprijsconversie kunt uitvoeren.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50891
ms.assetid: 73af66cf-c924-45be-837a-a648dbd05a31
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7a9cac200301ea58e4dd9047cd9ff42648126b8e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="prerequisites-for-a-standard-cost-conversion"></a>Vereisten voor een standaardkostprijsconversie

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de taken besproken die moeten worden uitgevoerd voordat u een standaardkostprijsconversie kunt uitvoeren. 

Voer de volgende handelingen uit voordat u een standaardkostprijsconversie uitvoert:

1.  Definieer een **artikelmodelgroep** voor standaardkosten. Gebruik de pagina Artikelmodelgroepen om een artikelmodelgroep te maken waarbij gebruik wordt gemaakt van een standaardkostenvoorraadmodel. Bij het instellen van een standaardkostprijsconversie wijst u deze artikelmodelgroep toe aan de artikelen die worden geconverteerd.
2.  Wijs een **kostengroep** toe aan elk artikel.
    -   De kostengroep die aan een ingekocht artikel is toegewezen kan fungeren als de basis voor het toewijzen van grootboekrekeningen die aan standaardkosten zijn gerelateerd. Een voorbeeld hiervan is het toewijzen van grootboekrekeningen voor inkoopprijsafwijkingen. In een productieomgeving zorgt de kostengroep die aan ingekochte onderdelen is toegewezen, voor segmentatie van de kosten in de berekende kostprijs van een gefabriceerd artikel.
    -   De kostengroep die aan een gefabriceerd artikel is toegewezen, kan fungeren als basis voor het toewijzen van grootboekrekeningen die zijn gekoppeld aan standaardkostprijzen, zoals grootboekrekeningen toewijzen voor productieafwijkingen.

3.  Wijs een **standaardorderhoeveelheid** toe aan een gefabriceerd artikel wanneer het constante kosten heeft. De standaardorderhoeveelheid voor een gefabriceerd artikel fungeert als boekhoudpartijgrootte voor het afschrijven of naar rato verdelen van constante kosten. Voorbeelden hiervan zijn instellingstijden in routebewerkingen of een constante onderdeelhoeveelheid in de stuklijst.
4.  Wijs **grootboekrekeningen** toe die aan standaardkostprijsafwijkingen zijn gekoppeld, met name de herwaarderingsafwijking. Gebruik de pagina **Boeking** (**Voorraadbeheer** &gt; **Instellingen**) om grootboekrekeningen toe te wijzen die zijn gekoppeld aan standaardkosten. Als minimum voor het standaardkostprijsconversieproces moet u de rekening voor de herwaarderingsafwijking toewijzen voor alle artikelen en alle kostengroepen. Gebruik de pagina **Rekeningschema** om de benodigde grootboekrekeningen voor standaardkosten te definiëren. Gebruik de pagina **Transactiecombinaties** om het gebruik van kostenrelaties (voor tabellen, groepen en alles) te activeren voordat u de artikelboekingsregels definieert.
5.  Definieer de voorraadparameters die aan standaardkosten zijn gekoppeld. Gebruik het tabblad **Nummerreeksen** op de pagina **Parameters voor voorraad- en magazijnbeheer** om een nummerreeks aan herwaarderingsboekstukken toe te wijzen. Een herwaarderingsboekstuk wordt gegenereerd wanneer door de standaardkostprijsconversie de voorraadwaarde van een artikel verandert. Gebruik de pagina **Parameters voor voorraad- en magazijnbeheer** om kostenbeheerparameters te definiëren (op het tabblad **Voorraadboekhouding**) waarmee u twee parameters kunt definiëren die zijn gekoppeld aan standaardkosten.
    -   Gebruik het veld **Kostenanalyse** om Nee of Subgrootboek te selecteren. De selectie van Subgrootboek is een actieve kostenanalyse. Een actieve kostenanalyse is zeer belangrijk voor het berekenen, achterhalen en weergeven van kostengroepsegmentatie over een productstructuur op meerdere niveaus voor standaardkostenartikelen. Wanneer de kostenanalyse actief is, kunt u op één niveau, meerdere niveaus of totale indeling het volgende rapporteren en analyseren:
        1.  Voorraad
        2.  Onderhanden werk (OHW)
        3.  Kosten van verkochte goederen (COGS) per kostengroep

        Bij een actieve kostenanalyse wordt de kostengroepsegmentatie door het inschakelen van de kosten van een gefabriceerd artikel in de kostenrecord van het artikel opgeslagen. Als u geen waarde in het veld **Kostenanalyse** plaatst, wordt de kostengroepsegmentatie niet onderhouden voor standaardkostenartikelen. Dit wil zeggen dat de standaardkosten van een gefabriceerd artikel worden berekend en onderhouden als één bedrag zonder kostengroepsegmentatie, en worden de kostenbijdragen van gefabriceerde onderdelen samengevoegd in het enkele bedrag.
    -   Gebruik het veld **Afwijkingen van standaard** om Samengevat of Per kostengroep te selecteren. Als u Per kostengroep selecteert, kunt u inkoopprijsafwijkingen en productieafwijkingen per kostengroep identificeren. U kunt dan ook de vier typen productieafwijkingen identificeren: partijgrootte, hoeveelheid, prijs en vervanging. Als u Samengevat selecteert, kunt u geen afwijkingen per kostengroep identificeren en kunt u niet de vier typen productieafwijkingen identificeren. U kunt alleen een samengevatte productieafwijking weergeven. Het beleid voor afwijking op standaardkosten is onafhankelijk van het kostenanalysebeleid. U kunt dus een kostenanalysebeleid van geen selecteren, en afwijkingen per kostengroep selecteren, zodat productieafwijkingen per kostengroep toch worden geregistreerd.






