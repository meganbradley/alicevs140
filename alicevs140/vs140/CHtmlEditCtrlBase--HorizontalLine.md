---
title: "CHtmlEditCtrlBase::HorizontalLine"
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
ms.assetid: 075c0c67-4327-4fbe-bc5b-22bc3efb5479
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::HorizontalLine
Overwrites a horizontal line on the current selection.  
  
## Syntax  
  
```  
  
      HRESULT HorizontalLine(  
   LPCTSTR szId = NULL   
) const;  
```  
  
#### Parameters  
 *szID*  
 The ID for the horizontal line.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_HORIZONTALLINE command ID](https://msdn.microsoft.com/en-us/library/aa769968.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)