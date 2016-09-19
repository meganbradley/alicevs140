---
title: "Programming Visual Studio Tools for Unity"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - tgt-pltfrm-cross-plat
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a5758cb0-e73b-45f5-8cae-c0eb40491026
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Programming Visual Studio Tools for Unity
In this section, you'll find examples for using the Visual Studio Tools for Unity API.  
  
## Examples  
 Here are some examples that show how you can use the Visual Studio Tools for Unity APIs.  
  
### Customize project files created by VSTU  
 Visual Studio Tools for Unity provides a Unity-style callback during project file generation. To learn how you can modify the project file whenever it's regenerated, see [Example: Project File Generation](../vs140/Customize-Project-Files-Created-by-VSTU.md).  
  
### Share the Unity log callback with VSTU  
 Visual Studio Tools for Unity registers a log callback with Unity to be able to stream its console to Visual Studio. If your editor scripts also register a log callback with Unity, the VSTU callback might interfere with it. To learn how you can share the Unity log callback with VSTU, see [Example: Log Callback](../vs140/Share-the-Unity-Log-Callback-with-VSTU.md).