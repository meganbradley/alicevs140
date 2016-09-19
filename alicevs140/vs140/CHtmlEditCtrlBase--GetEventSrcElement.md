---
title: "CHtmlEditCtrlBase::GetEventSrcElement"
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
ms.assetid: df5d3952-4386-4517-9163-e6b887f19a77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetEventSrcElement
Retrieves the object that fired the event.  
  
## Syntax  
  
```  
  
      HRESULT GetEventSrcElement(  
   IHTMLElement ** ppSrcElement   
) const;  
```  
  
#### Parameters  
 *ppSrcElement*  
 The element that fired the event.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [IHTMLElement Interface](https://msdn.microsoft.com/en-us/library/aa752279.aspx)   
 [srcElement Property (IHTMLEventObj)](http://msdn.microsoft.com/library/aa703891)