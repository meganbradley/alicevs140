---
title: "CHtmlEditCtrlBase::GetFrameZone"
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
ms.assetid: 1add9514-3a7c-4e8f-b978-b6ee462f3c2b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::GetFrameZone
Returns the security zone of the current page in the web browser.  
  
## Syntax  
  
```  
  
      HRESULT GetFrameZone(  
   short& nZone   
) const;  
```  
  
#### Parameters  
 *nZone*  
 The security zone.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_GETFRAMEZONE command ID](https://msdn.microsoft.com/en-us/library/aa769916.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)