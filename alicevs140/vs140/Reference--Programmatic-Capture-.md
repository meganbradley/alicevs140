---
title: "Reference (Programmatic Capture)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ef60eb8d-1ac2-4e3a-9b4b-f6da0bdd9da8
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference (Programmatic Capture)
Graphics Diagnostics supports programmatic control over its capture features, through the programmatic capture API. You can use this API to toggle and add messages to the graphics diagnostics HUD (Head-Up Display), initialize and create graphics log files, and capture graphics information.  
  
## Programmatic Capture APIs  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[VsgDbg Class](../vs140/VsgDbg-Class.md)|Represents the interface through which the in-app component of graphics diagnostics is controlled programmatically.|  
  
### Preprocessor Symbols  
  
|Name|Description|  
|----------|-----------------|  
|[DONT_SAVE_VSG_LOG_TO_TEMP](../vs140/DONT_SAVE_VSGLOG_TO_TEMP.md)|Defines by its presence whether the graphics log file is saved to the user's temporary files directory.|  
|[VSG_DEFAULT_RUN_FILENAME](../vs140/VSG_DEFAULT_RUN_FILENAME.md)|Defines the default file name of the graphics log file.|  
|[VSG_NODEFAULT_INSTANCE](../vs140/VSG_NODEFAULT_INSTANCE.md)|Defines by its presence whether a default instance of the `VsgDbg` class is provided.|  
  
## Related Articles  
  
|Title|Description|  
|-----------|-----------------|  
|[Capturing Graphics Information](../vs140/Capturing-Graphics-Information.md)|Shows how to capture graphics information from your DirectX-based app so that you can use [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] Graphics Diagnostics tools to diagnose rendering problems.|  
|[Graphics Diagnostics Overview](../vs140/Overview-of-Visual-Studio-Graphics-Diagnostics.md)|Shows how Graphics Diagnostics can help you debug rendering errors in DirectX games and apps.|