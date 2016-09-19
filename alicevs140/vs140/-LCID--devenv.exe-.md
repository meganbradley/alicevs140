---
title: "-LCID (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /LCID (devenv.exe)
ms.assetid: 3a3f4e70-ea66-4351-9d62-acb1dec30e8e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -LCID (devenv.exe)
Sets the default language used for text, currency, and other values within the integrated development environment (IDE).  
  
## Syntax  
  
```  
devenv {/LCID|/l} LocaleID  
```  
  
## Arguments  
 `LocaleID`  
 Required. The LCID (locale ID) of the language you specify.  
  
## Remarks  
 Loads the IDE and sets the default natural language for the environment. This change is persisted between sessions and reflected on the **International Settings** pane of the **Environment** options in the **Options** dialog box in the IDE.  
  
 If the specified language is not available on the user's system, the /LCID switch is ignored.  
  
 The following table lists the LCIDs of the languages supported by [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
|Language|LCID|  
|--------------|----------|  
|Chinese (Simplified)|2052|  
|Chinese (Traditional)|1028|  
|English|1033|  
|French|1036|  
|German|1031|  
|Italian|1040|  
|Japanese|1041|  
|Korean|1042|  
|Spanish|3082|  
  
## Example  
 This example loads the IDE with English resources strings.  
  
```  
devenv /LCID 1033  
```  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)   
 [International Settings, Environment, Options Dialog Box](../vs140/International-Settings--Environment--Options-Dialog-Box.md)   
 [Customizing window layouts](../vs140/Customizing-window-layouts-in-Visual-Studio.md)