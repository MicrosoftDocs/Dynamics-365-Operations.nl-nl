---
title: Parameters voor Vergoedingenbeheer instellen
description: Configureer parameters voor Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d6d463df08b9ae68047f09316f19e98740a8441
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229758"
---
# <a name="set-benefits-management-parameters"></a>Parameters voor Vergoedingenbeheer instellen

Voordat u verlofplannen kunt instellen in Microsoft Dynamics 365 Human Resources, moet u parameters voor Vergoedingenbeheer configureren. Met deze parameters worden standaardwaarden, redencodes en andere opties ingesteld.

## <a name="configure-general-parameters"></a>Algemene parameters configureren

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters**.

2. Geef op het tabblad **Algemeen** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Land/regio** | Het veld **Land/regio** bepaalt de weergavevolgorde van postcodes/staten. Het geselecteerde land wordt als eerste weergegeven in de vervolgkeuzelijst. |
   | **Redencode van inschrijving** | Selecteer een standaard redencode die moet worden gebruikt wanneer er plannen voor werknemers worden gemaakt tijdens de verwerking van open inschrijving. |
   | **Redencode voor annulering** | De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt geannuleerd. Tijdens het annuleringsproces wordt een dialoogvenster weergegeven. Gebruikers kunnen dit desgewenst wijzigen in de **redencodes voor annulering**. |
   | **Redencode voor opnieuw openen** | De redencode die moet worden gebruikt wanneer een vergoedingsplan voor werknemers wordt opnieuw geopend. Tijdens het annuleringsproces wordt een dialoogvenster weergegeven. Gebruikers kunnen de optie **Redencode opnieuw openen** desgewenst wijzigen. | 
   | **Redencode van levensgebeurtenis** | De redencode die wordt gebruikt wanneer een levensgebeurtenis plaatsvindt. |
   | **Redencode tariefwijziging** | De redencode die moet worden gebruikt bij het annuleren en opnieuw openen van een vergoedingsplan voor werknemers tijdens het bijwerkproces van de tariefwijziging. Het geeft aan welke records zijn gewijzigd door het wijzigingsproces voor de tariefwijziging. |
   | **Nieuwe in aanmerking komende medewerker** | Hiermee wordt opgegeven of nieuw aangestelde medewerkers in aanmerking komen. |
   | **Nieuwe inschrijvingsperiode van aanstelling** | De tijdsperiode waarin inschrijving van nieuw aangestelde medewerkers is toegestaan.</br></br>**Opmerking**: deze instelling heeft voorrang op elke nieuwe inschrijvingsperiode die u instelt voor de geschiktheidsregel voor het plan. | 
   | **Levensgebeurtenissen ingeschakeld** | Hiermee worden levensgebeurtenissen ingeschakeld. |
   | **Verouderde vergoedingsformulieren verbergen** | Hiermee kunt u verouderde vergoedingsformulieren verbergen. |

3. Selecteer **Opslaan**.

## <a name="configure-employee-self-service-parameters"></a>Parameters voor Selfservice werknemer configureren

1. Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Parameters**.

2. Geef op het tabblad **Selfservice werknemer** waarden op voor de volgende velden:

   | Veld | Beschrijving |
   | --- | --- |
   | **Vergoedingsverificatie** | De verificatietekst die moet worden gebruikt bij de afhandeling van selfservice vergoedingen. |
   | **Begunstigden automatisch selecteren** | Hiermee wordt opgegeven of er automatisch gezinsleden en begunstigden moeten worden geselecteerd op basis van hun geschiktheid voor planopties. |

3. Selecteer **Opslaan**.
