---
title: "CHtmlEditCtrlBase::Is2DElement"
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
ms.assetid: c6a81e5a-7769-4456-a66c-df1111ea9e23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::Is2DElement
Determines if an element is absolutely positioned.  
  
## Syntax  
  
```  
  
      HRESULT Is2DElement(  
   bool& bValue   
) const;  
```  
  
#### Parameters  
 `bValue`  
 True if the element is absolutely positioned, false otherwise.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_2D_ELEMENT command ID](https://msdn.microsoft.com/en-us/library/aa769886.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)   
 [CHtmlEditCtrlBase::Is1DElement](../vs140/CHtmlEditCtrlBase--Is1DElement.md)