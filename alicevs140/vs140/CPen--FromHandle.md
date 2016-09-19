---
title: "CPen::FromHandle"
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
ms.assetid: 4c9ce849-8fed-4e7c-b8ab-e94e750d4a38
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPen::FromHandle
Returns a pointer to a `CPen` object given a handle to a Windows GDI pen object.  
  
## Syntax  
  
```  
  
      static CPen* PASCAL FromHandle(  
   HPEN hPen   
);  
```  
  
#### Parameters  
 *hPen*  
 `HPEN` handle to Windows GDI pen.  
  
## Return Value  
 A pointer to a `CPen` object if successful; otherwise **NULL**.  
  
## Remarks  
 If a `CPen` object is not attached to the handle, a temporary `CPen` object is created and attached. This temporary `CPen` object is valid only until the next time the application has idle time in its event loop, at which time all temporary graphic objects are deleted. In other words, the temporary object is only valid during the processing of one window message.  
  
## Example  
 [!CODE [NVC_MFCDocView#105](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#105)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CPen Class](../vs140/CPen-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)