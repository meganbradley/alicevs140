---
title: "CSize::CSize"
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
ms.assetid: 85e88e37-259c-4858-823f-98d545c7c51e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSize::CSize
Constructs a `CSize` object.  
  
## Syntax  
  
```  
  
      CSize( ) throw( );   
CSize(   
   int initCX,   
   int initCY    
) throw( );  
CSize(   
   SIZE initSize    
) throw( );  
CSize(   
   POINT initPt    
) throw( );  
CSize(   
   DWORD dwSize    
) throw( );  
```  
  
#### Parameters  
 *initCX*  
 Sets the **cx** member for the `CSize`.  
  
 *initCY*  
 Sets the **cy** member for the `CSize`.  
  
 `initSize`  
 [SIZE](http://msdn.microsoft.com/library/windows/desktop/dd145106) structure or `CSize` object used to initialize `CSize`.  
  
 `initPt`  
 [POINT](../vs140/POINT-Structure.md) structure or `CPoint` object used to initialize `CSize`.  
  
 `dwSize`  
 `DWORD` used to initialize `CSize`. The low-order word is the **cx** member and the high-order word is the **cy** member.  
  
## Remarks  
 If no arguments are given, **cx** and **cy** are initialized to zero.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#97](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#97)]  
  
## Requirements  
 **Header:** atltypes.h  
  
## See Also  
 [CSize Class](../vs140/CSize-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)