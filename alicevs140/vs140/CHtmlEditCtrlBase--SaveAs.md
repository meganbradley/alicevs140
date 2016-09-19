---
title: "CHtmlEditCtrlBase::SaveAs"
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
ms.assetid: 42019b88-8718-423f-89f4-bee544105b40
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlEditCtrlBase::SaveAs
Saves the current Web page to a file.  
  
## Syntax  
  
```  
  
      HRESULT SaveAs(  
   LPCTSTR szPath = NULL   
) const;  
```  
  
#### Parameters  
 `szPath`  
 The path and file name to which to save the Web page.  
  
## Return Value  
 Returns S_OK on success, or an error HRESULT on failure.  
  
## Remarks  
 This method sends the [IDM_SAVEAS command ID](https://msdn.microsoft.com/en-us/library/aa770024.aspx) to the WebBrowser control.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlEditCtrlBase Class](../vs140/CHtmlEditCtrlBase-Class.md)