---
title: "CHtmlEditCtrlBase::GetAbsolutePosition"
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
ms.assetid: c181ac2a-9eab-4076-8251-17ce4ebc8147
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetAbsolutePosition
Returns whether an element's position property is "absolute."  
  
## Syntax  
  
```  
  
      HRESULT GetAbsolutePosition(  
   bool& bCurValue   
) const;  
```  
  
#### Parameters  
 `bCurValue`  
 True if the element's position property is set to "absolute."  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 For more information, see [IDM_ABSOLUTE_POSITION Command ID](https://msdn.microsoft.com/en-us/library/aa769889.aspx).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::SetAbsolutePosition](../vs140/CHtmlEditCtrlBase--SetAbsolutePosition.md)