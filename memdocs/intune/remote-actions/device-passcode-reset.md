---
title: Wachtwoordcodes van apparaten opnieuw instellen met Microsoft Intune - Azure | Microsoft Docs
description: Verwijder de wachtwoordcode of stel deze opnieuw in met de actie Wachtwoordcode verwijderen op apparaten die u beheert of bewaakt met Intune.
keywords: ''
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 02/27/2020
ms.topic: how-to
ms.service: microsoft-intune
ms.subservice: remote-actions
ms.localizationpriority: high
ms.technology: ''
ms.assetid: 47181d19-4049-4c7a-a8de-422206c4027e
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: 9d7e5fc7d16212c40fbbe5c1486ed3be76d2738f
ms.sourcegitcommit: 302556d3b03f1a4eb9a5a9ce6138b8119d901575
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2020
ms.locfileid: "83983103"
---
# <a name="reset-or-remove-a-device-passcode-in-intune"></a>De wachtwoordcode van een apparaat opnieuw instellen of verwijderen via Intune

[!INCLUDE [azure_portal](../includes/azure_portal.md)]

In dit document bespreken we zowel het opnieuw instellen van wachtwoordcodes op apparaatniveau als het opnieuw instellen van wachtwoordcodes voor werkprofielen op zakelijke Android-apparaten (voorheen Android for Work of AfW genoemd). Het is belangrijk om u bewust te zijn van dit onderscheid, aangezien de vereisten voor beide kunnen variëren. Bij het opnieuw instellen van wachtwoordcodes op apparaatniveau wordt de wachtwoordcode voor het gehele apparaat opnieuw ingesteld. Bij het opnieuw instellen van wachtwoordcodes voor werkprofielen wordt de wachtwoordcode alleen voor het werkprofiel van de gebruiker op zakelijke Android-apparaten opnieuw ingesteld.

## <a name="supported-platforms-for-device-level-passcode-reset"></a>Ondersteunde platformen voor het opnieuw instellen van wachtwoordcodes op apparaatniveau

| Platform | Ondersteund? |
| ---- | ---- |
| Android-apparaten met versie 6.x of lager | Ja |
| Android Enterprise-apparaten die zijn ingeschreven als eigenaar van het apparaat | Ja |
| iOS-/iPadOS-apparaten | Ja |
| iOS-/iPadOS-apparaten die zijn ingeschreven met gebruikersregistratie | Nee |
| Android-apparaten die zijn ingeschreven met een werkprofiel | Nee |
| Android-apparaten met versie 7.0 of lager | Nee |
| macOS | Nee |
| Windows | Nee |

Voor Android-apparaten betekent dit dat het opnieuw instellen van wachtwoordcodes op apparaatniveau alleen wordt ondersteund op apparaten waarop 6.x of eerder wordt uitgevoerd of op Android Enterprise-apparaten die in de kioskmodus worden uitgevoerd. Dit komt doordat Google ondersteuning voor het opnieuw instellen van de wachtwoordcode/het wachtwoord van een Android 7-apparaat vanuit een door de apparaatbeheerder toegekende app heeft verwijderd. Dit is van toepassing op alle MDM-leveranciers.

## <a name="supported-platforms-for-android-enterprise-work-profile-passcode-reset"></a>Ondersteunde platformen voor het opnieuw instellen van wachtwoordcodes voor werkprofielen op zakelijke Android-apparaten

| Platform | Ondersteund? |
| ---- | ---- |
| Zakelijke Android-apparaten die met een werkprofiel zijn ingeschreven en waarop versie 8.0 of later wordt uitgevoerd | Ja |
| Zakelijke Android-apparaten die met een werkprofiel zijn ingeschreven en waarop versie 7.x of eerder wordt uitgevoerd | Nee |
| Android-apparaten waarop versie 7.x of eerder wordt uitgevoerd | Nee |

Als u een nieuwe wachtwoordcode voor het werkprofiel wilt maken, gebruikt u de actie Wachtwoordcode opnieuw instellen. Deze actie zorgt ervoor dat de wachtwoordcode opnieuw wordt ingesteld en een nieuwe, tijdelijke wachtwoordcode voor alleen het werkprofiel wordt gemaakt. 

## <a name="reset-a-passcode"></a>Een wachtwoordcode opnieuw instellen


1. Meld u met een van de volgende rollen aan bij het [Microsoft Endpoint Manager-beheercentrum](https://go.microsoft.com/fwlink/?linkid=2109431): Globale beheerder van Azure Active Directory, Azure Active Directory Intune-servicebeheerder, helpdeskmedewerker of rolbeheerder.
2. Selecteer **Apparaten** en selecteer vervolgens **Alle apparaten**.
3. Selecteer een apparaat in de lijst met apparaten die u beheert en kies **Wachtwoordcode opnieuw instellen**.

## <a name="reset-android-work-profile-and-device-owner-passcodes"></a>Wachtwoordcodes voor Android-werkprofielen en apparaateigenaars opnieuw instellen

Ondersteunde Android Enterprise-apparaten waarop een werkprofiel is ingeschreven, ontvangen een nieuw wachtwoord om het beheerde profiel te ontgrendelen of een beheerde gebruikersvraag voor eindgebruikers.

Bij Android Enterprise-apparaten met een werkprofiel waarop versie 8.x of later wordt uitgevoerd, wordt eindgebruikers gevraagd om hun wachtwoordcode opnieuw in te stellen zodra de inschrijving is voltooid. De melding wordt weergegeven als een wachtwoord voor een werkprofiel is vereist en is ingesteld. Zodra de wachtwoordcode is ingevoerd, wordt de melding verwijderd.

Bij Android Enterprise-apparaateigenaars en werkprofielapparaten met versie 8.x of hoger is het zo dat, nadat de opnieuw ingestelde wachtwoordcode wordt geselecteerd in de console, de MEM Intune-beheerder een tijdelijke wachtwoordcode te zien krijgt. De tijdelijke wachtwoordcode moet op het apparaat worden ingevoerd. De tijdelijke wachtwoordcode voor het apparaat wordt 7 dagen weergegeven in de console.


## <a name="remove-iosipados-passcodes"></a>iOS-/iPadOS-wachtwoordcodes verwijderen

In plaats van opnieuw te worden ingesteld, worden wachtwoordcodes verwijderd van iOS-/iPadOS-apparaten. Als er een nalevingsbeleid voor wachtwoordcodes is ingesteld, wordt de gebruiker gevraagd om bij Instellingen een nieuwe wachtwoordcode in te stellen.

## <a name="next-steps"></a>Volgende stappen

Als u de status wilt weergeven van de actie die u zojuist hebt uitgevoerd, kiest u in **Apparaten** de optie **Apparaatacties**.
