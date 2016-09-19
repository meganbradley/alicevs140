---
title: "CStrBufT::SetLength"
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
ms.assetid: 3a4c99aa-d2df-4878-aa78-b3b50dd34981
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStrBufT::SetLength
Sets the length of the character buffer.  
  
## Syntax  
  
```  
  
      void SetLength(  
   int nLength  
);  
```  
  
#### Parameters  
 `nLength`  
 The new length of the character buffer of the string object.  
  
> [!NOTE]
>  Must be less than or equal to the minimum buffer length specified in the constructor of `CStrBufT`.  
  
## Remarks  
 Call this function to set the length of the string represented by the buffer object.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStrBufT Class](../vs140/CStrBufT-Class.md)