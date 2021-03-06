---
title: Virtuele Windows 10-machines gebruiken met Microsoft Intune
titleSuffix: ''
description: Richtlijnen voor het gebruik van virtuele Windows 10-machines met Microsoft Intune
keywords: ''
author: ErikjeMS
ms.author: erikje
manager: dougeby
ms.date: 11/20/2019
ms.topic: conceptual
ms.service: microsoft-intune
ms.subservice: fundamentals
ms.localizationpriority: high
ms.technology: ''
ms.assetid: ''
ms.reviewer: dougeby
ms.suite: ems
search.appverid: MET150
ms.custom: intune-classic; get-started
ms.collection: M365-identity-device-management
ms.openlocfilehash: 944b3d98dc59dcae69f72fef5dfdb1793701f67a
ms.sourcegitcommit: 2871a17e43b2625a5850a41a9aff447c8ca44820
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/24/2020
ms.locfileid: "82126167"
---
# <a name="using-windows-10-virtual-machines-with-intune"></a>Virtuele Windows 10-machines gebruiken met Intune

Intune biedt ondersteuning voor het beheer van virtuele machines met Windows 10 Enterprise maar met bepaalde beperkingen. Intune-beheer is niet afhankelijk van en hindert het beheer van Windows Virtual Desktop van dezelfde virtuele machine niet.

Houd bij het beheren van virtuele Windows 10-machines met Intune rekening met de volgende punten:

- Windows 10 Enterprise Multi Session (Enterprise for Virtual Devices) zoals wordt gebruikt in Windows Virtual Desktop, biedt momenteel geen ondersteuning voor Intune-beheer.

## <a name="enrollment"></a>Inschrijving
- Het is niet raadzaam virtuele machines op aanvraag te beheren en virtuele machinesessies met Intune te hosten. Elke VM moet worden ingeschreven als deze wordt gemaakt. Als u regelmatig virtuele machines verwijdert, blijven er zwevende apparaatrecords in Intune achter totdat deze worden [opgeschoond](../remote-actions/devices-wipe.md#automatically-delete-devices-with-cleanup-rules). 
- Automatische implementatie van Windows Autopilot en nauwkeurige implementatietypen worden niet ondersteund omdat hiervoor een fysieke TPM (Trusted Platform Module) is vereist. 
- De OOBE-inschrijving (Out-Of-Box Experience) wordt niet ondersteund op VM's die alleen toegankelijk zijn via RDP (zoals VM's die worden gehost op Azure). Deze beperking betekent het volgende:
    - Windows Autopilot en Commercial OOBE worden niet ondersteund.
    - Opties voor de inschrijvingsstatuspagina voor beleid voor apparaatcontext worden niet ondersteund.


## <a name="configuration"></a>Configuration
Intune biedt geen ondersteuning voor een configuratie die gebruikmaakt van een Trusted Platform Module of hardwarebeheer, waaronder:
- [BitLocker-instellingen](../configuration/device-profiles.md#endpoint-protection)
- [Instellingen voor de configuratie-interface voor apparaatfirmware](../configuration/device-profiles.md#device-firmware-configuration-interface)

## <a name="reporting"></a>Rapporten
Intune detecteert automatisch virtuele machines en rapporteert deze als 'virtuele machine' in het veld **Apparaten** > **Alle apparaten** > kies een apparaat > **Overzicht** > **Model**. 

Virtuele machines waarvan de toewijzing ongedaan is gemaakt, kunnen als niet-compatibele apparaten worden gerapporteerd, omdat deze niet kunnen worden [ingecheckt bij de Intune-service](../configuration/device-profile-troubleshoot.md#how-long-does-it-take-for-devices-to-get-a-policy-profile-or-app-after-they-are-assigned).

## <a name="retirement"></a>Buiten gebruik stellen
Als u alleen RDP-toegang hebt, moet u de [actie om te wissen](../remote-actions/devices-wipe.md#wipe) niet gebruiken. Met de actie om te wissen worden de RDP-instellingen van de virtuele machine verwijderd en wordt voorkomen dat u ooit nog verbinding kunt maken.


