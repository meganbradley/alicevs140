---
title: "Debugging Preparation: Windows Services"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - VB
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac0a99f7-ec3d-4a20-b17f-698a817fdcc2
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debugging Preparation: Windows Services
A Windows service is a program that runs in the background under Microsoft Windows. Examples include the Telnet service and the Windows time service, which updates your computer's visible clock. A Windows service cannot be run from within [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]; it must run within the context of the Services Control Manager. For more information, see [Creating Windows Services](assetId:///0f5e2cbb-d95d-477c-b2b5-4b990e6b86ff), [Debugging Windows Service Applications](assetId:///63ab0800-0f05-4f1e-88e6-94c73fd920a2), and [Windows Service Applications](assetId:///ba72d648-9553-4849-b829-069ad5ea014b).  
  
## See Also  
 [Debugging Managed Code](../Topic/Debugging%20Managed%20Code.md)   
 [C#, F#, and Visual Basic Project Types](../vs140/Debugging-Preparation--C#--F#--and-Visual-Basic-Project-Types.md)   
 [Project Settings for  C# Debug Configurations](../vs140/Project-Settings-for--C#-Debug-Configurations.md)   
 [Project Settings for a Visual Basic Debug Configuration](../vs140/Project-Settings-for-a-Visual-Basic-Debug-Configuration.md)   
 [How to: Debug the OnStart Method](../Topic/How%20to:%20Debug%20the%20OnStart%20Method.md)