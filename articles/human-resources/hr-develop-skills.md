---
title: Vaardigheden configureren
description: U kunt de vaardigheden van uw werknemer bijhouden in Dynamics 365 Human Resources. U kunt ook opgeven welke vaardigheden voor een bepaalde functie zijn vereist.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076554"
---
# <a name="configure-skills"></a>Vaardigheden configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt de vaardigheden van uw werknemer bijhouden in Dynamics 365 Human Resources. U kunt ook opgeven welke vaardigheden voor een bepaalde functie zijn vereist.

Voorbeelden van de vaardigheden die u kunt bijhouden zijn:

- Supervisie - vermogen om toe te zien op het werk van anderen.
- Leiderschap - vermogen om leiding te geven aan medewerkers en bedrijfseenheden.
- Planning: mogelijkheid om vooruit te kijken, visies te ontwikkelen en uit te voeren.
- HTML - vermogen om HTML-code te schrijven.

Als u nog geen vaardigheidstypen en beoordelingsmodellen hebt ingesteld, moet u er een aantal toevoegen voordat u vaardigheden kunt maken.

De volgende personen kunnen vaardigheden voor een werknemer invoeren:

- Werknemers kunnen vaardigheden voor zichzelf invoeren in Selfservice werknemer. Voor deze vaardigheden is goedkeuring van de manager vereist.
- Managers kunnen vaardigheden voor hun werknemers invoeren. U kunt een werkstroom maken waarmee deze vaardigheden automatisch worden goedgekeurd.

## <a name="create-a-skill-type"></a>Een vaardigheidstype maken

Vaardigheidstypen zijn categorieën waaronder afzonderlijke vaardigheden vallen, zoals Administratie of Verkoop.

1. Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.

2. Selecteer **Vaardigheidstypen** onder **Competentie-instellingen**.

3. Selecteer **Nieuw**.

4. Vul de volgende velden in:

   - **Vaardigheidstype**: voer een unieke naam voor het vaardigheidstype in.
   - **Omschrijving**: voer een omschrijving voor het vaardigheidstype in.

5. Selecteer **Opslaan**.

## <a name="create-a-rating-model"></a>Een beoordelingsmodel maken

Beoordelingsmodellen helpen te beoordelen wat het werkelijke vaardigheidsniveau van een persoon is, het niveau dat ze moeten zien te bereiken of het vaardigheidsniveau dat ze voor een taak moeten hebben. Aan elk niveau in een beoordelingsmodel wordt een factor toegewezen.

1. Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.

2. Selecteer **Beoordelingsmodellen** onder **Competentie-instellingen**.

3. Selecteer **Nieuw**.

4. Vul de volgende velden in:

   - **Beoordeling**: voer een naam in voor het beoordelingsmodel, zoals **Vaardigheden**.
   - **Omschrijving**: voer een omschrijving in voor het beoordelingsmodel, zoals **Vaardigheidsbeoordelingen**.

5. Selecteer **Nieuw** in de sectie **Niveaus**. Vul de volgende velden in voor elk niveau dat u wilt toevoegen:

   - **Niveau**: voer een naam voor het niveau in.
   - **Omschrijving**: voer een omschrijving in voor het niveau.
   - **Factor**: voer een factorwaarde in van 0-9. Factorwaarden worden gebruikt om scores te normaliseren van vaardigheden die verschillende beoordelingsmodellen gebruiken. Elk niveau moet een unieke factor hebben. Niveaus met een hogere factorwaarden zijn belangrijker in een beoordelingsmodel.

   Ga indien nodig door met het toevoegen van niveaus. U kunt tot maximaal 10 niveaus invoeren voor elk beoordelingsmodel.

6. Selecteer **Opslaan**.

## <a name="create-a-skill"></a>Een vaardigheid maken

Voordat u een vaardigheid kunt toewijzen, een zoekopdracht voor vaardigheidstoewijzingen of een vaardigheidsprofiel kunt maken, moet u informatie over de vaardigheden op de pagina **Vaardigheden** invoeren. Voor elke vaardigheid kunt u een vaardigheidstype en een beoordelingsmodel selecteren.

1. Selecteer **Koppelingen** in het werkgebied **Werknemersontwikkeling**.

2. Selecteer **Vaardigheden** onder **Competentie-instellingen**.

3. Selecteer **Nieuw**.

4. Vul de volgende velden in:

   - **Vaardigheid**: voer een naam voor de vaardigheid in.
   - **Omschrijving**: voer een omschrijving voor de vaardigheid in.
   - **Beoordeling**: selecteer het beoordelingsmodel dat u voor deze vaardigheid wilt gebruiken.
   - **Vaardigheidstype**: selecteer een vaardigheidstype in de lijst met vaardigheidstypen.

5. Selecteer **Opslaan**.

## <a name="see-also"></a>Zie ook

[Vaardigheden invoeren](hr-develop-enter-skills.md)<br>
[Vaardigheden toewijzen](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]