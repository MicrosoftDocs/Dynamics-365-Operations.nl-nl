---
title: Parameters voor Vergoedingenbeheer en Werknemerselfservice instellen voor alle bedrijven
description: Parameters voor Vergoedingenbeheer en Werknemerselfservice configureren in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2021
ms.locfileid: "4962435"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Parameters voor Vergoedingenbeheer en Werknemerselfservice instellen voor alle bedrijven

Voordat u vergoedingsplannen kunt instellen in Microsoft Dynamics 365 Human Resources, moet u parameters voor Vergoedingenbeheer configureren. Met deze parameters worden standaardwaarden, redencodes en andere opties ingesteld. 

## <a name="configure-general-parameters"></a>Algemene parameters configureren

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Gedeelde parameters voor Human Resources**.

2. Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Land/regio** | Het veld **Land/regio** bepaalt de weergavevolgorde van postcodes/staten. Het geselecteerde land wordt als eerste weergegeven in de vervolgkeuzelijst. |
   | **Redencode van inschrijving** | Selecteer een standaard redencode die moet worden gebruikt wanneer er plannen voor werknemers worden gemaakt tijdens de verwerking van open inschrijving. |
   | **Redencode voor annulering** | De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt geannuleerd. Tijdens het annuleringsproces wordt een dialoogvenster weergegeven. Gebruikers kunnen dit desgewenst wijzigen in de **redencodes voor annulering**. |
   | **Redencode voor opnieuw openen** | De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt opnieuw geopend. Tijdens het annuleringsproces wordt een dialoogvenster weergegeven. Gebruikers kunnen de optie **Redencode opnieuw openen** desgewenst wijzigen. | 
   | **Redencode van levensgebeurtenis** | De redencode die wordt gebruikt wanneer een levensgebeurtenis plaatsvindt. |
   | **Redencode tariefwijziging** | De redencode die moet worden gebruikt bij het annuleren en opnieuw openen van een vergoedingsplan voor werknemers tijdens het bijwerkproces van de tariefwijziging. Het geeft aan welke records zijn gewijzigd door het wijzigingsproces voor de tariefwijziging. |
   | **Vergoedingen jaarsalaris** | Hiermee kunt u een **Jaarlijks salarisbedrag voor vergoedingen** voor een werknemer instellen. Human Resources gebruikt **het jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het vaste jaarlijkse compensatiebedrag. |
   | **Nieuwe in aanmerking komende medewerker** | Hiermee wordt opgegeven of nieuw aangestelde medewerkers in aanmerking komen. |
   | **Nieuwe inschrijvingsperiode van aanstelling** | De tijdsperiode waarin inschrijving van nieuw aangestelde medewerkers is toegestaan.</br></br>**Opmerking**: deze instelling heeft voorrang op elke nieuwe inschrijvingsperiode die u instelt voor de geschiktheidsregel voor het plan. |
   | **Standaard betalingsfrequentie** | De standaardbetalingsfrequentie die wordt gebruikt wanneer nieuwe werknemers worden toegevoegd. |
   | **Levensgebeurtenissen ingeschakeld** | Hiermee worden levensgebeurtenissen ingeschakeld. |
   | **Verouderde vergoedingsformulieren verbergen** | Hiermee kunt u verouderde vergoedingsformulieren verbergen. |
   | **Vergoedingsverificatie** | De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen. |
   | **Begunstigden automatisch selecteren** | Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd, op basis van hun geschiktheid voor planopties. |

3. Selecteer **Opslaan**.

## <a name="configure-employee-self-service-parameters"></a>Parameters voor Werknemerselfservice configureren

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters voor Human Resources**.

2. Geef op het tabblad **Vergoedingenbeheer** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Vergoedingsverificatie** | De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen. |
   | **Begunstigden automatisch selecteren** | Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd op basis van hun geschiktheid voor planopties. |

3. Selecteer **Opslaan**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]