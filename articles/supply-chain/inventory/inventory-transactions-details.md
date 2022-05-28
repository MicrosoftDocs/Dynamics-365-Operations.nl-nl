---
title: Voorraadtransactiedetails
description: Dit onderwerp biedt een overzicht van de pagina Transactiedetails met details van een geselecteerde voorraadtransactie.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735910"
---
# <a name="inventory-transaction-details"></a>Voorraadtransactiedetails

Op de pagina **Transactiedetails** kunt u details van de geselecteerde voorraadtransacties weergeven.

## <a name="open-the-transaction-details-page"></a>De pagina Transactiedetails openen

Voer de volgende stappen uit om de pagina **Transactiedetails** te openen.

1. Ga naar **Voorraadbeheer \> Query's en rapporten \> Transacties**.
1. Selecteer de transactie die u wilt inspecteren.
1. Selecteer **Transactiedetails** in het actievenster.

## <a name="fasttabs-overview"></a>Overzicht van sneltabbladen

De pagina **Transactiedetails** is opgesplitst in verschillende sneltabbladen. De volgende tabel beschrijft het doel van elk sneltabblad.

| Sneltabblad | Description |
|---|---|
| Algemeen | Op dit sneltabblad wordt basisinformatie over de geselecteerde voorraadtransactie gegeven. Naast de velden die worden weergegeven op de pagina **Voorraadtransacties**, bevat dit sneltabblad de extra velden die later in dit onderwerp worden beschreven. |
| Updates | Op dit sneltabblad wordt informatie gegeven over de fysieke, financiële en vereffeningsaspecten van de geselecteerde voorraadtransactie. Afhankelijk van de huidige status van de transactie zijn sommige velden mogelijk leeg. Deze velden worden echter automatisch ingesteld wanneer transacties worden geboekt. Naast de velden die worden weergegeven op de pagina **Voorraadtransacties**, bevat dit sneltabblad de extra velden die later in dit onderwerp worden beschreven. |
| Grootboekboekingen | Op dit sneltabblad worden het boekingstype en de grootboekrekening weergegeven die worden gebruikt voor de fysieke update, financiële update, fysieke opbrengsten, fysieke toeslagen, financiële opbrengsten en financiële toeslagen die gerelateerd zijn aan de geselecteerde voorraadtransactie. |
| Verwijzingen | Op dit sneltabblad wordt extra informatie weergegeven over de brontransactie die de geselecteerde voorraadtransactie heeft gemaakt. Deze informatie kan bijvoorbeeld details uit de inkoop- of verkooporder bevatten. |
| Verwante informatie | Op dit sneltabblad wordt extra informatie over de geselecteerde voorraadtransactie gegeven. Deze velden worden mogelijk niet ingesteld als u bepaalde functies niet gebruikt, zoals inkoopcategorieën of -projecten. |
| Financiële dimensies - fysiek | Op dit sneltabblad worden de waarden van financiële dimensies weergegeven die zijn gebruikt toen de fysieke update werd geboekt. Als de fysieke update niet is geboekt, zijn de velden leeg. |
| Financiële dimensies - financieel | Op dit sneltabblad worden de waarden van financiële dimensies weergegeven die zijn gebruikt toen de financiële update werd geboekt. Als de financiële update niet is geboekt, zijn de velden leeg. |
| Voorraaddimensies | Op dit sneltabblad worden de waarden van voorraaddimensies weergegeven die aan de geselecteerde voorraadtransactie zijn toegewezen. Deze waarden zijn onder andere de locatie, het magazijn, de grootte, de kleur, de configuratie, de locatie, het batchnummer, het serienummer, de voorraadstatus, de nummerplaat en de eigenaar. |

## <a name="fields-on-the-general-fasttab"></a>Velden op het sneltabblad Algemeen

In de volgende tabel worden de velden op het sneltabblad **Algemeen** beschreven die niet ook voorkomen op de pagina **Voorraadtransacties**.

| Veld | Description |
|---|---|
| Partij | De naam van de relevante partij voor de geselecteerde voorraadtransactie. In een inkoopordertransactie wordt bijvoorbeeld de naam van de leverancier op de inkooporder weergegeven en in een verkoopordertransactie wordt de naam van de klant weergegeven. Dit veld is niet beschikbaar voor alle typen voorraadtransacties. |
| Voorraadverwijzing | Als een andere voorraadtransactie is gerelateerd aan de geselecteerde voorraadtransactie, is dit het type van de andere transactie. Als bijvoorbeeld een inkooporder voor een verkooporder is gemarkeerd, wordt het veld **Voorraadverwijzing** voor de verkoopordertransactie ingesteld op *Verkooporder*. Markering wordt automatisch gedaan voor rechtstreekse leveringsorders en intercompany-orders. Wanneer u markeren gebruikt met andere kostprijsmethoden dan *standaardkosten* en *zwevend gemiddelde*, worden er vereffeningen en correcties gemaakt voor de exacte gemarkeerde transacties. Op deze manier kunt u 'werkelijke' kostprijs maken die voorrang heeft boven de logica voor FIFO (First In First Out); last in, first out (LIFO); of gewogen gemiddelde. |
| Voorraadnummer | De specifieke transactie die betrekking heeft op de geselecteerde voorraadtransactie. Als bijvoorbeeld een inkooporder voor een verkooporder is gemarkeerd, wordt het veld **Voorraadnummer** van de verkoopordertransactie ingesteld op het verkoopordernummer. |
| Project-ID | Als de geselecteerde voorraadtransactie betrekking heeft op een project, wordt dit veld ingesteld op het projectnummer. |
| Partij-ID | De unieke partij-id die het systeem heeft toegewezen aan de geselecteerde voorraadtransactie. |
| Verwijzingspartij | Als een andere voorraadtransactie is gerelateerd aan de geselecteerde voorraadtransactie, is dit de partij-id van die andere transactie. Als bijvoorbeeld een inkooporder voor een verkooporder is gemarkeerd, wordt het veld **Verwijzingspartij** voor de verkoopordertransactie ingesteld op de waarde voor **Partij-id** van de voorraadtransactie voor de verkooporderregel. |
| Dimensienummer | Een unieke id die de combinatie vertegenwoordigt van alle voorraaddimensiewaarden die aan de geselecteerde voorraadtransactie zijn toegewezen. |
| Openstaande waarde | Een waarde die aangeeft of de geselecteerde voorraadtransactie is vereffend door het voorraadsluitingsproces. Als het veld is ingesteld op *Ja*, is de transactie niet vereffend. |
| Verw. datum | Voor ontvangsttransacties is dit de datum waarop de voorraadontvangst naar verwachting plaatsvindt. Dit veld kan bijvoorbeeld de verwachte ontvangstdatum voor een voorraadblokkeringsorder of de leveringsdatum voor een inkooporderregel bevatten. |
| Voorraaddatum | Dit veld wordt ingesteld wanneer een registratietransactie is uitgevoerd op de ontvangstorder voordat een fysieke ontvangst werd geboekt. |
| Niet-financiële overdracht | Een waarde die aangeeft of de geselecteerde voorraadtransactie een niet-financiële overdracht is. Een niet-financiële overdracht wordt uitgevoerd wanneer een wijziging in voorraaddimensie niet financieel wordt bijgehouden op de pagina **Artikelmodelgroep**. |
| Overdrachtpartij-ID | Als de geselecteerde voorraadtransactie een niet-financiële overdracht is, wordt dit veld ingesteld op de waarde **Partij-ID** van de andere voorraadtransactie waarmee de geselecteerde transactie wordt vereffend. |

## <a name="fields-on-the-updates-fasttab"></a>Velden op het sneltabblad Updates

In de volgende tabel worden de velden op het sneltabblad **Updates** beschreven die niet ook voorkomen op de pagina **Voorraadtransacties**.

| Veld | Description |
|---|---|
| Fysiek boekstuk | Het boekstuknummer in het grootboek waar de fysieke boeking voor de geselecteerde voorraadtransactie is gegenereerd. |
| Route | De route die betrekking heeft op de geselecteerde voorraadtransactie. Dit veld wordt alleen ingesteld voor productieverzamellijsttransacties waarbij de stuklijst- of formuleregel aan een specifiek artikel is gerelateerd. |
| Pakbon | Het pakbonnummer dat is ingevoerd voor een productontvangstbontransactie voor een inkooporder. |
| Fysieke kostprijs | Het bedrag dat is geboekt naar het grootboek voor de fysieke update. Voor een standaardkostenproduct vertegenwoordigt dit bedrag de standaardkosten. Voor andere kostprijsmethoden vertegenwoordigt dit het gewogen gemiddelde voor het product ten tijde van de boeking. |
| Fysieke opbrengst | Het bedrag aan uitgestelde opbrengst dat naar het grootboek is geboekt voor de fysieke update. |
| Lading-id | Als de huidige transactie betrekking heeft op een lading in Transportbeheer, wordt in dit veld het unieke nummer weergegeven van de lading die het artikel bevatte. |
| Fysiek geboekt | Een waarde die aangeeft of de geselecteerde voorraadtransactie fysiek is geboekt. Als de huidige transactie naar het grootboek wordt geboekt, is er ook een fysiek boekstuk. |
| Financieel geboekt | Een waarde die aangeeft of de geselecteerde voorraadtransactie financieel is geboekt. Als de huidige transactie naar het grootboek wordt geboekt, is er ook een financieel boekstuk. |
| Fysieke kostprijs geboekt | Een waarde die aangeeft of de fysieke kostprijzen met betrekking tot de geselecteerde voorraadtransactie zijn geboekt. |
| Financiële kostprijs geboekt | Een waarde die aangeeft of de financiële kostprijzen met betrekking tot de geselecteerde voorraadtransactie zijn geboekt. |
| Financieel boekstuk | Het boekstuknummer in het grootboek waar de financiële boeking is gegenereerd. |
| Factuur | Het factuurnummer dat is gegenereerd, bijvoorbeeld voor een inkoop- of verkooporder. |
| Correctie | Het bedrag dat is gecorrigeerd voor de geselecteerde voorraadtransactie uit het proces voor voorraadafsluiting en -correctie. |
| Verlies en winst, geboekt bedrag | Het bedrag van de geselecteerde voorraadtransactie dat is geboekt naar de winst- en verliesrekening. |
| Niet-geboekte factuur | Het factuurnummer van een verwante inkooporder die wordt weergegeven op de pagina **Leveranciersfactuur in behandeling**. |
| Financieel afgesloten | De datum waarop de transactie volledig is vereffend. |
| Gedekte variabel gewicht-hoeveelheid | De hoeveelheid catch weight die wordt gedekt door de vereffening. |
| Vereffende hoeveelheid | De hoeveelheid die is vereffend voor de geselecteerde voorraadtransactie. |
| Vereffend bedrag | De waarde die is vereffend voor de geselecteerde voorraadtransactie. |
