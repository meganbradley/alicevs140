---
title: "CPen::GetExtLogPen"
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
ms.assetid: c620b0ec-02b8-48cf-a6db-f9b6b817af91
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPen::GetExtLogPen
Gets an **EXTLOGPEN** underlying structure.  
  
## Syntax  
  
```  
  
      int GetExtLogPen(  
   EXTLOGPEN* pLogPen   
);  
```  
  
#### Parameters  
 `pLogPen`  
 Points to an [EXTLOGPEN](http://msdn.microsoft.com/library/windows/desktop/dd162711) structure that contains information about the pen.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 The **EXTLOGPEN** structure defines the style, width, and brush attributes of a pen. For example, call `GetExtLogPen` to match the particular style of a pen.  
  
 See the following topics in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for information about pen attributes:  
  
-   [GetObject](http://msdn.microsoft.com/library/windows/desktop/dd144904)  
  
-   [EXTLOGPEN](http://msdn.microsoft.com/library/windows/desktop/dd162711)  
  
-   [LOGPEN](http://msdn.microsoft.com/library/windows/desktop/dd145041)  
  
-   [ExtCreatePen](http://msdn.microsoft.com/library/windows/desktop/dd162705)  
  
## Example  
 The following code example demonstrates calling `GetExtLogPen` to retrieve a pen's attributes, and then create a new, cosmetic pen with the same color.  
  
 [!CODE [NVC_MFCDocView#102](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#102)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPen Class](../vs140/CPen-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPen::GetLogPen](../vs140/CPen--GetLogPen.md)   
 [CPen::CreatePen](../vs140/CPen--CreatePen.md)