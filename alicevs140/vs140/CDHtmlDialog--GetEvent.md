---
title: "CDHtmlDialog::GetEvent"
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
ms.assetid: 53c0052d-f783-4461-ade2-aeeb814461f2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::GetEvent
Returns the **IHTMLEventObj** pointer to the current event object.  
  
## Syntax  
  
```  
  
      HRESULT GetEvent(  
   IHTMLEventObj **ppEventObj   
);  
```  
  
#### Parameters  
 `ppEventObj`  
 Address of a pointer that will be filled with the **IHTMLEventObj** interface pointer.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 This function should only be called from within a DHTML event handler.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)