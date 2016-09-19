---
title: "CDocument::PreCloseFrame"
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
ms.assetid: 10a056d9-ea5e-4fc7-888c-f026297390a5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::PreCloseFrame
This member function is called by the framework before the frame window is destroyed.  
  
## Syntax  
  
```  
  
      virtual void PreCloseFrame(  
   CFrameWnd* pFrame   
);  
```  
  
#### Parameters  
 `pFrame`  
 Pointer to the [CFrameWnd](../vs140/CFrameWnd-Class.md) that holds the associated **CDocument** object.  
  
## Remarks  
 It can be overridden to provide custom cleanup, but be sure to call the base class as well.  
  
 The default of `PreCloseFrame` does nothing in **CDocument**. The **CDocument**-derived classes [COleDocument](../vs140/COleDocument-Class.md) and [CRichEditDoc](../vs140/CRichEditDoc-Class.md) use this member function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)