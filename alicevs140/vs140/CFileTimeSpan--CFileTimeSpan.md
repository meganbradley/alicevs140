---
title: "CFileTimeSpan::CFileTimeSpan"
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
ms.assetid: af7c9870-d758-4195-99fc-8c0c345ea7be
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileTimeSpan::CFileTimeSpan
The constructor.  
  
## Syntax  
  
```  
  
      CFileTimeSpan( ) throw( );   
CFileTimeSpan(  
   const CFileTimeSpan& span   
) throw( );  
CFileTimeSpan(  
   LONGLONG nSpan   
) throw( );  
```  
  
#### Parameters  
 `span`  
 An existing `CFileTimeSpan` object.  
  
 `nSpan`  
 A period of time in milliseconds.  
  
## Remarks  
 The `CFileTimeSpan` object can be created using an existing `CFileTimeSpan` object, or expressed as a 64-bit value. The default constructor sets the time span to 0.  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CFileTimeSpan Class](../vs140/CFileTimeSpan-Class.md)