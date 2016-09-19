---
title: "COleInsertDialog::GetClassID"
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
ms.assetid: 3e28e92f-3de9-40a3-a7d1-c8e149b9454e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::GetClassID
Call this function to get the **CLSID** associated with the selected item only if [DoModal](../vs140/COleInsertDialog--DoModal.md) returns **IDOK** and the selection type is **COleInsertDialog::createNewItem**.  
  
## Syntax  
  
```  
  
REFCLSID GetClassID( ) const;   
```  
  
## Return Value  
 Returns the **CLSID** associated with the selected item.  
  
## Remarks  
 For more information, see [CLSID Key](http://msdn.microsoft.com/library/windows/desktop/ms691424) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)   
 [COleInsertDialog::GetSelectionType](../vs140/COleInsertDialog--GetSelectionType.md)