---
title: "COleControlContainer::GetDlgItemText"
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
ms.assetid: 1f5c1cd9-9222-48d7-92a9-63cf7e49f877
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::GetDlgItemText
Retrieves the text of the given control.  
  
## Syntax  
  
```  
  
      virtual int GetDlgItemText(  
   int nID,  
   LPTSTR lpStr,  
   int nMaxCount   
) const;  
```  
  
#### Parameters  
 `nID`  
 The identifier of the control.  
  
 `lpStr`  
 Pointer to the text of the control.  
  
 `nMaxCount`  
 Specifies the maximum length, in characters, of the string to be copied to the buffer pointed to by `lpStr`. If the length of the string exceeds the limit, the string is truncated.  
  
## Return Value  
 If the function succeeds, the return value specifies the number of characters copied to the buffer, not including the terminating null character.  
  
 If the function fails, the return value is zero. To get extended error information, call [GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360).  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)