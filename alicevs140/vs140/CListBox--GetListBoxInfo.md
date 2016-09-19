---
title: "CListBox::GetListBoxInfo"
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
ms.assetid: ba1e630f-d375-44ce-b5ca-b8cd42a2dc5a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::GetListBoxInfo
Retrieves the number of items per column.  
  
## Syntax  
  
```  
  
DWORD GetListBoxInfo( ) const;  
  
```  
  
## Return Value  
 Number of items per column of the `CListBox` object.  
  
## Remarks  
 This member function emulates the functionality of the [LB_GETLISTBOXINFO](http://msdn.microsoft.com/library/windows/desktop/bb775208) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)