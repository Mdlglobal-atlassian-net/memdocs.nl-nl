---
title: Een macOS-apparaat wissen
titleSuffix: Microsoft Intune
description: Lees hoe u alle gegevens van een macOS-apparaat kunt wissen, inclusief het besturingssysteem.
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
ms.assetid: ab396092-907a-44b7-a157-aabee62176a9
ms.reviewer: coferro
ms.suite: ems
search.appverid: MET150
ms.custom: intune-azure
ms.collection: M365-identity-device-management
ms.openlocfilehash: 50575b1a4b19a6fbebb3fd904a471e19b070860e
ms.sourcegitcommit: 302556d3b03f1a4eb9a5a9ce6138b8119d901575
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2020
ms.locfileid: "83989957"
---
# <a name="erase-all-data-from-a-macos-device"></a>Alle gegevens van een macOS-apparaat wissen

[!INCLUDE [azure_portal](../includes/azure_portal.md)]

U kunt alle gegevens van een macOS-apparaat wissen, inclusief het besturingssysteem. Het apparaat wordt ook uit Intune-beheer verwijderd. De eindgebruiker wordt hier niet over gewaarschuwd.

1. Kies in het [Microsoft Endpoint Manager-beheercentrum](https://go.microsoft.com/fwlink/?linkid=2109431) de opties **Apparaten** > **Alle apparaten** > kies het apparaat dat u wilt wissen.
2. Klik op **Meer** > **Wissen** en geef een zescijferig nummer op voor de **Herstelpincode**. Dit is de pincode die u aan de gebruiker moet geven zodat ze het besturingssysteem weer op hun apparaat kunnen installeren. Noteer deze pincode; de pincode is niet meer zichtbaar nadat de wisactie is voltooid.
![Schermopname](./media/device-erase/providepin.png)
3. Klik op **OK** om het apparaat te wissen.
