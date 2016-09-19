---
title: "CPathT::BuildRoot"
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
ms.assetid: 3579d163-4dbb-4273-9bbe-13073d3b48ef
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPathT::BuildRoot
Call this method to create a root path from a given drive number.  
  
## Syntax  
  
```  
  
      void BuildRoot(  
   int iDrive   
);  
```  
  
#### Parameters  
 *iDrive*  
 The drive number (0 is A:, 1 is B:, and so on).  
  
## Remarks  
 For more information, see [PathBuildRoot](http://msdn.microsoft.com/library/windows/desktop/bb773567).  
  
## Requirements  
 **Header:** atlpath.h  
  
## See Also  
 [CPathT Class](../vs140/CPathT-Class.md)   
 [CPathT::GetDriveNumber](../vs140/CPathT--GetDriveNumber.md)