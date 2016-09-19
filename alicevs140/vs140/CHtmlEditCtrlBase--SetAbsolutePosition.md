---
title: "CHtmlEditCtrlBase::SetAbsolutePosition"
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
ms.assetid: 2ddf4b6f-a946-472d-a31a-0d6fced4c3b2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetAbsolutePosition
Sets an element's position property to "absolute" or "static."  
  
## Syntax  
  
```  
  
      HRESULT SetAbsolutePosition(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, the element's position property is "absolute"; if false, it is "static."  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_ABSOLUTE_POSITION command ID](https://msdn.microsoft.com/en-us/library/aa769889.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::GetAbsolutePosition](../vs140/CHtmlEditCtrlBase--GetAbsolutePosition.md)