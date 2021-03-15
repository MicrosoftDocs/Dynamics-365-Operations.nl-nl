---
title: Regels en beleid van de vergoedingsgeschiktheid definiëren
description: In dit artikel leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: cc80549eaffa72a22dec51829c86d04a763de96a
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112045"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Regels en beleid van de vergoedingsgeschiktheid definiëren

In dit onderwerp leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.  

## <a name="create-benefit-eligibility-policy-rule-type"></a>Regeltype van beleid om in aanmerking te komen voor een vergoeding maken

1. Ga naar **Human Resources > Vergoedingen > Geschiktheid > Regeltypen van beleid om in aanmerking te komen voor een vergoeding**.
2. Selecteer **Nieuw**.
3. Voer een waarde in het veld **Regelnaam** in.
4. Voer een waarde in het veld **Beschrijving** in.
5. Klik in het veld **Querynaam** op de vervolgkeuzeknop om het opzoekveld te openen.
6. Selecteer in de lijst de koppeling in de geselecteerde rij.
7. Selecteer **Opslaan**.
8. Sluit de pagina.

## <a name="benefit-eligibility-policy"></a>Beleid om in aanmerking te komen voor een vergoeding

1. Ga naar **Human resources > Vergoedingen > Geschiktheid > Beleid voor geschiktheid vergoedingen**.
2. Selecteer een bestaand vergoedingsbeleid.
3. Selecteer in de lijst de koppeling in de geselecteerde rij.
4. Schakel het uitvouwen van de secties **Beleidsorganisaties** om. U kunt organisaties toevoegen of verwijderen die u wilt opnemen in het beleid.
5. Vouw de sectie **Beleidsregels** uit of samen.
6. Zoek in de lijst de beleidsregel die u eerder hebt gemaakt.
7. Selecteer **Beleidsregel maken**.
8. Voer in het veld **Ingangsdatum** de datum in waarop u het beleid van kracht wilt laten worden.
    * Door ingangsdatums en einddatums in te stellen, kunt u in de toekomst wijzigingen aanbrengen in beleidsregels zodat u niet terug hoeft te gaan naar het beleid als u die wijzigingen van kracht wilt laten worden.  
9. Voeg zo nodig een clausule toe aan het veld **Voorwaarde toevoegen**.
    * Als u bijvoorbeeld wilt dat de regel alleen van toepassing is op verkoopmanagers, kunt u de WHERE-clausule gebruiken om te zeggen: Waar de positieomschrijving gelijk is aan Verkoopmanager. U kunt meerdere Where-instructies opnemen in de regel.  
10. Selecteer **OK**.
11. Sluit de pagina.

## <a name="assign-rule-to-benefit"></a>Regel toewijzen aan vergoeding

1. Ga naar **Human Resources > Vergoedingen > Vergoedingen**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Selecteer in de lijst de koppeling in de geselecteerde rij.
4. Vouw de sectie **Geschiktheidsregels** uit of samen.
5. Selecteer **Bewerken**.
6. Selecteer de regel in het veld **Geschiktheid**.
7. Selecteer in het veld **Regeltype** de regel die u eerder hebt gemaakt.
9. Selecteer in de lijst de koppeling in de geselecteerde rij.
10. Selecteer **Opslaan**.
11. Het formulier sluiten.



[!INCLUDE[footer-include](../includes/footer-banner.md)]