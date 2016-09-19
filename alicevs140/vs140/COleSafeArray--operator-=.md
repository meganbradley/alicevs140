---
title: "COleSafeArray::operator ="
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
ms.assetid: 4c638c1e-f07f-4ae2-9db6-11de8da85120
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::operator =
These overloaded assignment operators copy the source value into this `COleSafeArray` object.  
  
## Syntax  
  
```  
  
      COleSafeArray& operator =(  
   const COleSafeArray& saSrc   
);  
COleSafeArray& operator =(  
   const VARIANT& varSrc   
);  
COleSafeArray& operator =(  
   LPCVARIANT pSrc   
);  
COleSafeArray& operator =(  
   const COleVariant& varSrc   
);  
```  
  
## Remarks  
 A brief description of each operator follows:  
  
-   **operator =(** *saSrc* **)** Copies an existing `COleSafeArray` object into this object.  
  
-   **operator =(** *varSrc* **)** Copies an existing **VARIANT** or `COleVariant` array into this object.  
  
-   **operator =(** `pSrc` **)** Copies the **VARIANT** array object accessed by `pSrc` into this object.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)