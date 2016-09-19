---
title: "IDiaLoadCallback2::RestrictReferencePathAccess"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e20cb45c-0360-4ff0-a92c-b1b6f76d6e85
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDiaLoadCallback2::RestrictReferencePathAccess
Determines if looking for a .pdb file is allowed in the path where the .exe file is located.  
  
## Syntax  
  
```cpp#  
HRESULT RestrictReferencePathAccess();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Any return code other than `S_OK` to prevent looking for a .pdb file in the path where the .exe file is located.  
  
## See Also  
 [IDiaLoadCallback2](../vs140/IDiaLoadCallback2.md)