---
title: "CHtmlEditCtrlBase::SetAtomicSelection"
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
ms.assetid: 2b752115-746f-4df2-a320-7c7b6baf5683
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SetAtomicSelection
Set atomic selection mode.  
  
## Syntax  
  
```  
  
      HRESULT SetAtomicSelection(  
   bool bNewValue   
) const;  
```  
  
#### Parameters  
 `bNewValue`  
 If true, any element that has an ATOMICSELECTION attribute set to TRUE will be selectable only as a unit.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_ATOMICSELECTION command ID](https://msdn.microsoft.com/en-us/library/aa769892.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)