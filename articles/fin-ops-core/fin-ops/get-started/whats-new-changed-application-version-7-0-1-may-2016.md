---
title: Wat is nieuw of gewijzigd in Dynamics AX-toepassingsversie 7.0.1 (mei 2016)
description: In dit artikel worden de functies beschreven die in Microsoft Dynamics AX versie 7.0.1 nieuw of gewijzigd zijn. Deze versie werd uitgebracht in mei 2016 en heeft een buildnummer van 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 94cebad528facc5537226a3faa5ea9be8448092e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267195"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Wat is nieuw of gewijzigd in Dynamics AX-toepassingsversie 7.0.1 (mei 2016)

[!include [banner](../includes/banner.md)]

In dit artikel worden de functies beschreven die in Microsoft Dynamics AX versie 7.0.1 nieuw of gewijzigd zijn. Deze versie werd uitgebracht in mei 2016 en heeft een buildnummer van 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektronische rapportage (ER)

| Wat kunt u doen? | Waarom is dit belangrijk? |
|------------------|------------------------|
| Configureer een dialoogvenster tijdens de uitvoering voor het ontwerpen van ER-rapporten (elektronische rapportage), zodat gebruikers de financiële dimensies kunnen selecteren die ze willen gebruiken. | Tijdens de uitvoering kunnen gebruikers in het dialoogvenster voor het uitvoeren van een ER-rapport meerdere financiële dimensies selecteren. De details van de geselecteerde financiële dimensies wordt weergegeven in het elektronische document dat wordt gegenereerd. |
| Configureer toegang tot meerdere financiële dimensies bij het ontwerp van een ER-rapport, via één toewijzing voor de gewenste gegevensbron. | Dezelfde configuratie voor ER-rapporten kan worden gebruikt voor het genereren van elektronische documenten die transactiegegevens presenteren alsmede details van financiële dimensies, ongeacht het aantal financiële dimensies dat is geselecteerd door de gebruiker of geconfigureerd voor de huidige rechtspersoon of het huidige exemplaar. |
| Configureer een ER-rapport voor het invoeren van gegevens in dynamisch gegenereerde kolommen van een elektronisch document dat is gemaakt in OPENXML-werkbladindeling. | Een ER-rapport kan gegevens invoeren in een OPENXML-werkblad dat wordt gegenereerd via het horizontaal repliceren van kolommen. Daarom kan dezelfde ER-rapportconfiguratie opnieuw worden gebruikt voor het genereren van elektronische documenten met een verschillend aantal dynamisch gegenereerde kolommen. |
| Configureer ER-bestemmingen zodat het resultaat van de uitvoer van een indeling wordt omgeleid naar een specifieke bestemming: bestand, e-mailadres of archief (Microsoft SharePoint-map of Microsoft Azure-opslag). | Voorheen, wanneer u een ER-configuratie uitvoerde, werd er een bericht weergegeven waarin gebruikersactie werd vereist voor het opslaan of openen van een bestand. U kunt nu apart een bestemming vooraf configureren voor elke indelingsconfiguratie en voor elk uitvoeronderdeel (een map of een bestand). Gebruikers die over de juiste toegangsrechten beschikken, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoering. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>POS – Microsoft Dynamics AX Retail

| Wat kunt u doen? | Waarom is dit belangrijk? |
|------------------|------------------------|
| Gebruik de Google Chrome browser. | Detailhandelaren kunnen Cloud POS nu starten vanuit de browser Chrome en beschikken over alle functionaliteit die beschikbaar is in de Microsoft Edge en Internet Explorer-versie van Cloud POS. |

## <a name="financial-reporting"></a>Financiële rapportage

| Wat kunt u doen? | Waarom is dit belangrijk? |
|------------------|------------------------|
| Bouw de datamart voor financiële rapportage opnieuw op. | Wanneer u Dynamics AX-databases tussen omgevingen verplaatst of andere ingrijpende wijzigingen in de omgeving doorvoert, moet mogelijk de database voor financiële rapportage opnieuw worden opgebouwd. Er is nu een Windows PowerShell-script beschikbaar dat de database opnieuw voor u opbouwt. |
| U kunt niet langer opties voor rapportontwerper selecteren die niet geldig zijn. | Verschillende opties voor rapportontwerper die werden gebruikt in de versies van Management Reporter op de markt gelden niet voor deze versie van Dynamics AX. Deze opties waren gerelateerd aan het ontwerp, de uitvoer en de koppeling van financiële rapportage. Deze opties zijn verwijderd uit de functie voor het ontwerpen van financiële rapporten om gebruikersfouten te voorkomen. |

## <a name="financial-management"></a>Financieel beheer

| Wat kunt u doen? | Waarom is dit belangrijk? |
|------------------|------------------------|
| Genereer positieve betalingsbestanden voor leveranciersbetalingen. | Positieve betalingsbestanden kunnen worden gegenereerd om fraude met cheques te helpen voorkomen. |

## <a name="warehouse-and-production"></a>Magazijn en productie

<table>
<thead>
<tr>
<th>Wat kunt u doen?</th>
<th>Waarom is dit belangrijk?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Definieer een werkbeleid voor magazijnen dat het maken van werk voor een reeks van producten op specifieke locaties regelt.</td>
<td>Magazijnprocessen omvatten niet altijd werk. Met behulp van het nieuwe magazijnwerkbeleid kunt u voorkomen dat werk wordt gemaakt voor het verzamelen en wegzetten van grondstoffen voor afgewerkte goederen voor een reeks producten op specifieke locaties.</td>
</tr>
<tr>
<td>Geef op dat op een locatie voor productie-uitvoer niet worden gecontroleerd op nummerplaat.</td>
<td>U kunt nu opgeven dat een locatie voor productuitvoer niet wordt gecontroleerd op nummerplaat. Deze functie is bijvoorbeeld handig als een upstream productieorder artikelen rechtstreeks gereedmeldt op een locatie die als productie-invoerlocatie voor een downstream productieorder fungeert.</td>
</tr>
<tr>
<td>Ondersteun stuklijsten die artikelen met verschillende productafmetingen van hetzelfde artikel bevatten.</td>
<td>Wanneer u een of meerdere van de productafmetingen in productie gebruikt, kunt u situaties hebben waarin u een artikel wilt produceren op basis van een andere variant van hetzelfde artikel. Zie <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">deze blog</a> voor meer informatie.</td>
</tr>
<tr>
<td>Productieorders met circulaire structuren op het eerste niveau van de stuklijsten zijn uitgesloten van berekening op stuklijstniveau voor de planning van materiaalresources.</td>
<td>Het is niet mogelijk correcte stuklijstniveaus toe te wijzen aan productvarianten voor productieorders die correctheid in de stuklijsthiërarchie veroorzaken.</td>
</tr>
<tr>
<td>Bereken afzonderlijke stuklijstniveaus voor de planning van materiaalresources en kostenberekening:
<ul>
<li>Voor de planning van materiaalresources worden stuklijstniveaus berekend in de nieuwe tabel <strong>ReqItemLevel</strong>. Beëindigde productieorders worden genegeerd in de berekening.</li>
<li>Voor de berekening van de productiekosten worden stuklijstniveaus berekend in de tabel <strong>InventTable</strong>. Beëindigde productieorders worden opgenomen in de berekening.</li>
</ul>
</td>
<td>
<ul>
<li>Bij het uitvoeren van de planning van materiaalresources, bijvoorbeeld planning en explosie van de hoofdplanning, hoeven alleen stuklijstniveaus die worden gebruikt voor de planning van de materiaalresources opnieuw te worden berekend. Met andere woorden, er hoeven geen stuklijstniveaus te worden berekend die worden gebruikt voor de berekening van de productiekostprijs.</li>
<li>Bij het uitvoeren van bewerkingen voor kostprijsberekening, bijvoorbeeld de afsluiting van voorraad, hoeven alleen stuklijstniveaus die worden gebruikt voor kostprijsberekening voor de productie opnieuw te worden berekend.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Aanvullende bronnen

[Startpagina Nieuw of gewijzigd in apps voor financiën en bedrijfsactiviteiten](whats-new-changed.md)

[Nieuwe of bijgewerkte taakbegeleidingen (mei 2016)](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
