---
title: "Options Page, Fonts and Colors Node Properties"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8e1ab784-5f85-4e2b-8ef9-e5d59ca4dbcb
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Options Page, Fonts and Colors Node Properties
This document describes font and color properties for a tool window that is registered to appear under **Fonts and Colors** in the **Environment** category of the **Options** dialog box. This supports the dynamic nature of groups of colorable items, which can change if VSPackages are installed or uninstalled.  
  
 The following section shows an example of a registered window type and the properties that are available for each window.  
  
## Text Editor or Printer or Dialogs and Tool Windows  
 `DTE.Properties("FontsAndColors", "TextEditor")`  
  
 -or-  
  
 `DTE.Properties("FontsAndColors", "Printer")`  
  
 -or-  
  
 `DTE.Properties("FontsAndColors", "Dialogs and Tool Windows")`  
  
|Property Item Name|Value|Description|  
|------------------------|-----------|-----------------|  
|FontFamily|Get/Set (String)|The font name to use, such as "Courier New."|  
|FontCharacterSet|Get/Set (<xref:EnvDTE.vsFontCharSet?qualifyHint=False>)|A <xref:EnvDTE.vsFontCharSet?qualifyHint=False> value, specifying the type of character set to use, such as Hebrew or Russian.|  
|FontSize|Get/Set (Short)|The size of font to use, in points. For example, 10 or 12.|  
  
## See Also  
 [Controlling Tools Options Settings](assetId:///a09ed242-7494-4cde-bbd1-7a8ec617965d)   
 [Determining Property Item Names in Tools Options Pages](assetId:///d450422d-47c7-4eeb-9f9f-3286264bc5aa)   
 [Tools Options Page - Environment Node Properties](../Topic/Options%20Page,%20Environment%20Node%20Properties.md)   
 [Tools Options Page - Text Editor Node Properties](../Topic/Options%20Page,%20Text%20Editor%20Node%20Properties.md)