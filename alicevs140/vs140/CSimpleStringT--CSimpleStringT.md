---
title: "CSimpleStringT::CSimpleStringT"
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
ms.assetid: 97999818-a7ec-42f4-b8b5-946eff498559
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::CSimpleStringT
Constructs a `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      CSimpleStringT(  
   const XCHAR* pchSrc,  
   int nLength,  
   IAtlStringMgr* pStringMgr  
);  
CSimpleStringT(  
   PCXSTR pszSrc,  
   IAtlStringMgr* pStringMgr  
);  
CSimpleStringT(  
   const CSimpleStringT& strSrc   
);  
explicit CSimpleStringT(  
   IAtlStringMgr* pStringMgr  
) throw( );  
```  
  
#### Parameters  
 `strSrc`  
 An existing `CSimpleStringT` object to be copied into this `CSimpleStringT` object.  
  
 `pchSrc`  
 A pointer to an array of characters of length `nLength`, not null terminated.  
  
 `pszSrc`  
 A null-terminated string to be copied into this `CSimpleStringT` object.  
  
 `nLength`  
 A count of the number of characters in `pch`.  
  
 `pStringMgr`  
 A pointer to the memory manager of the `CSimpleStringT` object. For more information about `IAtlStringMgr` and memory management for `CSimpleStringT`, see [Memory Management and CStringT](../vs140/Memory-Management-with-CStringT.md).  
  
## Remarks  
 Construct a new `CSimpleStringT` object. Because the constructors copy the input data into new allocated storage, memory exceptions may result.  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::CSimpleStringT` by using the ATL `typedef``CSimpleString`. `CSimpleString` is a commonly used specialization of the class template `CSimpleStringT`.  
  
 A specialization defines a class by putting specific type parameters into a class template. For more information, see [Class Template Instantiation](../vs140/Class-Template-Instantiation.md).  
  
 [!CODE [NVC_ATLMFC_Utilities#77](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#77)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)