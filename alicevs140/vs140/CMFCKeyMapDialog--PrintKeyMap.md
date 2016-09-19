---
title: "CMFCKeyMapDialog::PrintKeyMap"
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
ms.assetid: 308e00a7-f86a-446d-adea-4c039625220a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog::PrintKeyMap
Called by the framework when a user clicks the **Print** button.  
  
## Syntax  
  
```  
virtual void PrintKeyMap();  
```  
  
## Remarks  
 The `PrintKeyMap` method prints the key map. It initiates a new print job and then repeatedly calls the [CMFCKeyMapDialog::OnPrintHeader](../vs140/CMFCKeyMapDialog--OnPrintHeader.md) and [CMFCKeyMapDialog::OnPrintItem](../vs140/CMFCKeyMapDialog--OnPrintItem.md) methods until all the key mappings are printed.  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
## See Also  
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC Class](../vs140/CDC-Class.md)