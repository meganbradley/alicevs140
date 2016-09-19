---
title: "CFont::FromHandle"
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
ms.assetid: 38d452e2-079a-4fd4-a921-4e90bfa57dc7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFont::FromHandle
Returns a pointer to a `CFont` object when given an **HFONT** handle to a Windows GDI font object.  
  
## Syntax  
  
```  
  
      static CFont* PASCAL FromHandle(  
   HFONT hFont   
);  
```  
  
#### Parameters  
 `hFont`  
 An **HFONT** handle to a Windows font.  
  
## Return Value  
 A pointer to a `CFont` object if successful; otherwise **NULL**.  
  
## Remarks  
 If a `CFont` object is not already attached to the handle, a temporary `CFont` object is created and attached. This temporary `CFont` object is valid only until the next time the application has idle time in its event loop, at which time all temporary graphic objects are deleted. Another way of saying this is that the temporary object is valid only during the processing of one window message.  
  
## Example  
 [!CODE [NVC_MFCDocView#75](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#75)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CFont Class](../vs140/CFont-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)