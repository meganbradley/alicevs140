---
title: "CMFCKeyMapDialog::FormatItem"
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
ms.assetid: 411b75f4-30b7-4ca7-92af-f970b61efb27
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog::FormatItem
Called by the framework to build a string that describes a key mapping. By default, the string contains the command name, the shortcut keys used, and the shortcut key description.  
  
## Syntax  
  
```  
virtual CString FormatItem(  
   int nItem   
) const;  
```  
  
#### Parameters  
 [in] `nItem`  
 The zero-based index of an item in the internal list of key mappings.  
  
## Return Value  
 A `CString` object that contains the formatted item text.  
  
## Remarks  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
## See Also  
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)