---
title: EUR-00015 Een btw-id instellen
description: Deze procedure beschrijft de vereisten voor het registreren van de btw-id, zoals het instellen van een registratietype en het toewijzen ervan aan een registratiecategorie.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
ms.openlocfilehash: 26120765b61a27cab544c37163a34a0ef18da30a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283783"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 Een btw-id instellen

[!include [banner](../../includes/banner.md)]

Deze procedure beschrijft de vereisten voor het registreren van de btw-id, zoals het instellen van een registratietype en het toewijzen ervan aan een registratiecategorie. U kunt extra informatie over registratie-id's en de verwerking van registratie-id, waaronder de vereisten, vinden in het Help-artikel Registratie-id's. 

Deze informatie is van toepassing op alle Europese landen/regio's. De taak werd gemaakt met het demobedrijf DEMF met een primair adres van een rechtspersoon in Duitsland. Deze taak is bedoeld voor systeembeheerders. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.

1. Ga naar Organisatiebeheer > Globaal adresboek > Registratietypen > Registratietypen.
2. Klik op Nieuw om het verwijderdialoogvenster te openen.
3. Typ Btw-id in het veld Naam.
4. Typ Btw-nummer in het Veld Omschrijving
5. Typ of selecteer een waarde DEU in het veld Land/regio
6. Selecteer Ja in het veld Uniek.
    * Schakel dit selectievakje in om te verifiëren of de btw-id uniek is.  
7. Selecteer Ja in het veld Primair voor land/regio.
    * Schakel dit selectievakje in als de btw-id geldig moet zijn voor alle adressen die tot het opgegeven land/regio behoren.  
8. Klik op Maken.
9. Klik op Toevoegen.
10. Typ of selecteer een waarde ITA in het veld Land/regio
11. Typ ########### in het veld Indeling.
    * Wanneer u een registratie-id van dit type voor het geselecteerde land of de regio invoert, wordt de registratie-id aan de hand van deze indeling gecontroleerd.  
12. Schakel het selectievakje Uniek in.
    * Schakel dit selectievakje in om te verifiëren of de btw-id uniek is.  
13. Schakel het selectievakje Primair voor land/regio in.
    * Schakel dit selectievakje in als de btw-id geldig moet zijn voor alle adressen die tot het opgegeven land/regio behoren.  
14. Klik op Opslaan.
15. Ga naar Organisatiebeheer > Globaal adresboek > Registratietypen > Registratiecategorieën.
16. Klik op Nieuw.
17. Typ of selecteer een waarde Btw-id, DEU in het veld Land/regio
18. Selecteer Btw-id in het veld Registratiecategorie.
    * Wijs het registratietype dat u eerder hebt gemaakt toe aan een vooraf gedefinieerde registratiecategorie.  
19. Klik op Nieuw.
20. Typ of selecteer een waarde Btw-id, ITA in het veld Land/regio
21. Selecteer Btw-id in het veld Registratiecategorie.
    * Wijs het registratietype dat u hebt gemaakt toe aan een vooraf gedefinieerde registratiecategorie.  
22. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
