---
title: "CStatic::GetEnhMetaFile"
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
ms.assetid: 69ffa376-2b17-4e4c-bf19-548a5a01efda
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatic::GetEnhMetaFile
Gets the handle of the enhanced metafile, previously set with [SetEnhMetafile](../vs140/CStatic--SetEnhMetaFile.md), that is associated with `CStatic`.  
  
## Syntax  
  
```  
  
HENHMETAFILE GetEnhMetaFile( ) const;  
  
```  
  
## Return Value  
 A handle to the current enhanced metafile, or **NULL** if no enhanced metafile has been set.  
  
## Example  
 [!CODE [NVC_MFC_CStatic#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CStatic#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CStatic Class](../vs140/CStatic-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatic::SetEnhMetaFile](../vs140/CStatic--SetEnhMetaFile.md)   
 [STM_GETIMAGE](http://msdn.microsoft.com/library/windows/desktop/bb760778)