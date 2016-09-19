---
title: "CFixedStringT::CFixedStringT"
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
ms.assetid: 6477bb9c-4cd8-4af3-a392-3f5907258799
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFixedStringT::CFixedStringT
Constructs a `CFixedStringT` object.  
  
## Syntax  
  
```  
  
      CFixedStringT( ) throw( );   
explicit CFixedStringT(  
   IAtlStringMgr* pStringMgr   
) throw( );  
CFixedStringT(  
   const CFixedStringT< StringType, t_nChars >& str   
);  
CFixedStringT(  
   const StringType& str   
);  
CFixedStringT(  
   const StringType::XCHAR* psz   
);  
explicit CFixedStringT(  
   const StringType::YCHAR* psz   
);  
explicit CFixedStringT(  
   const unsigned char* psz   
);  
```  
  
#### Parameters  
 `psz`  
 A null-terminated string to be copied into this `CFixedStringT` object.  
  
 `str`  
 An existing `CFixedStringT` object to be copied into this `CFixedStringT` object.  
  
 `pStringMgr`  
 A pointer to the memory manager of the `CFixedStringT` object. For more information on `IAtlStringMgr` and memory management for `CFixedStringT`, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Remarks  
 Because the constructors copy the input data into new allocated storage, you should be aware that memory exceptions may result. Note that some of these constructors act as conversion functions.  
  
## Requirements  
 **Header:** cstringt.h  
  
## See Also  
 [CFixedStringT Class](../vs140/CFixedStringT-Class.md)