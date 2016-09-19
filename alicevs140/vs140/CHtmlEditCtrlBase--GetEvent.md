---
title: "CHtmlEditCtrlBase::GetEvent"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 38c04a1c-c98d-4065-a708-daa0b999ee2a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetEvent
Retrieves an interface pointer to the event object that contains information relevant to the most recent event.  
  
## Syntax  
  
```  
  
      HRESULT GetEvent(  
   IHTMLEventObj ** ppEventObj   
) const;  
```  
  
#### Parameters  
 `ppEventObj`  
 The event object.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [IHTMLEventObj Interface](https://msdn.microsoft.com/en-us/library/aa703876.aspx)   
 [event Property (IHTMLWindow2)](https://msdn.microsoft.com/en-us/library/aa741461.aspx)