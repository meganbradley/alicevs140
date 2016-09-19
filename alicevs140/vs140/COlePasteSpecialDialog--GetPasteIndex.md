---
title: "COlePasteSpecialDialog::GetPasteIndex"
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
ms.assetid: a0cd8e77-13e9-406b-a263-83b394038d13
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::GetPasteIndex
Gets the index value associated with the entry the user selected.  
  
## Syntax  
  
```  
  
int GetPasteIndex( ) const;  
```  
  
## Return Value  
 The index into the array of **OLEUIPASTEENTRY** structures that was selected by the user. The format that corresponds to the selected index should be used when performing the paste operation.  
  
## Remarks  
 For more information, see the [OLEUIPASTEENTRY](http://msdn.microsoft.com/library/windows/desktop/ms690165) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)