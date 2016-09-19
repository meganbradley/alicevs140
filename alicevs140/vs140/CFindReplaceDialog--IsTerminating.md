---
title: "CFindReplaceDialog::IsTerminating"
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
ms.assetid: 0c6352ec-884f-4662-a089-e8fd21df5db5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::IsTerminating
Call this function within your callback function to determine whether the user has decided to terminate the dialog box.  
  
## Syntax  
  
```  
  
BOOL IsTerminating( ) const;  
```  
  
## Return Value  
 Nonzero if the user has decided to terminate the dialog box; otherwise 0.  
  
## Remarks  
 If this function returns nonzero, you should call the `DestroyWindow` member function of the current dialog box and set any dialog box pointer variable to **NULL**. Optionally, you can also store the find/replace text last entered and use it to initialize the next find/replace dialog box.  
  
## Example  
 See the example for [CFindReplaceDialog::GetFindString](../vs140/CFindReplaceDialog--GetFindString.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)