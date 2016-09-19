---
title: "CFixedStringT::operator ="
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
ms.assetid: deeea72e-be54-4ba1-9cd5-f9054458c5a6
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFixedStringT::operator =
Reinitializes an existing `CFixedStringT` object with new data.  
  
## Syntax  
  
```  
  
      CFixedStringT< StringType, t_nChars >& operator =(  
   const CFixedStringT< StringType, t_nChars >& str  
);  
CFixedStringT< StringType, t_nChars >& operator =(  
   const char* psz  
);  
CFixedStringT< StringType, t_nChars >& operator =(  
   const wchar_t* psz  
);  
CFixedStringT< StringType, t_nChars >& operator =(  
   const unsigned char* psz  
);  
CFixedStringT< StringType, t_nChars >& operator =(  
   const StringType& str  
);  
```  
  
#### Parameters  
 `str`  
 A null-terminated string to be copied into this `CFixedStringT` object.  
  
 `psz`  
 An existing `CFixedStringT` to be copied into this `CFixedStringT` object.  
  
## Remarks  
 You should be aware that memory exceptions may occur whenever you use the assignment operator because new storage is often allocated to hold the resulting `CFixedStringT` object.  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CFixedStringT Class](../vs140/CFixedStringT-Class.md)