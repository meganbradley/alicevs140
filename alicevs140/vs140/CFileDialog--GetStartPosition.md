---
title: "CFileDialog::GetStartPosition"
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
ms.assetid: 6907b77f-884e-4951-b8b7-af438b166647
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::GetStartPosition
Call this member function to retrieve the position of the first file pathname in the list, if `m_ofn.Flags` has the `OFN_ALLOWMULTISELECT` flag set.  
  
## Syntax  
  
```  
  
POSITION GetStartPosition( ) const;  
  
```  
  
## Return Value  
 A **POSITION** value that can be used for iteration; **NULL** if the list is empty.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFileDialog::GetFileName](../vs140/CFileDialog--GetFileName.md)   
 [CFileDialog::GetNextPathName](../vs140/CFileDialog--GetNextPathName.md)