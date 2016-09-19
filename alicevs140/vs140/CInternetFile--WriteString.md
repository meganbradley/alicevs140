---
title: "CInternetFile::WriteString"
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
ms.assetid: b425fe84-a468-48df-819c-288a142f46f8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CInternetFile::WriteString
This function writes a null-terminated string to the associated file.  
  
## Syntax  
  
```  
  
      virtual void WriteString(   
   LPCTSTR pstr    
);  
```  
  
#### Parameters  
 `pstr`  
 A pointer to a string containing the contents to be written.  
  
## Remarks  
 If any error occurs while writing the data, the function throws a [CInternetException](../vs140/CInternetException-Class.md) object describing the error.  
  
## Exceptions  
 This method can throw exceptions of type `CInternetException*`.  
  
## Requirements  
 **Header:** afxinet.h  
  
## See Also  
 [CInternetFile Class](../vs140/CInternetFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)