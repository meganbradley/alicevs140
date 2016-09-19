---
title: "COlePasteSpecialDialog::AddLinkEntry"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: fd439bf7-4ebc-4e5c-8363-469202e4cf92
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::AddLinkEntry
Adds a new entry to the list of supported Clipboard formats.  
  
## Syntax  
  
```  
  
      OLEUIPASTEFLAG AddLinkEntry(  
   UINT cf  
);  
```  
  
#### Parameters  
 `cf`  
 The clipboard format to add.  
  
## Return Value  
 An [OLEUIPASTEFLAG](http://msdn.microsoft.com/library/windows/desktop/ms682172) structure containing the information for the new link entry.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)