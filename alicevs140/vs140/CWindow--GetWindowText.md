---
title: "CWindow::GetWindowText"
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
ms.assetid: 340f1ca3-08c5-45bb-8f95-5020b363e68c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWindow::GetWindowText
Retrieves the window's text.  
  
## Syntax  
  
```  
  
      int GetWindowText(  
   LPTSTR lpszStringBuf,  
   int nMaxCount   
) const throw();  
BOOL GetWindowText(  
   BSTR& bstrText   
) throw();  
int GetWindowText(   CSimpleString& strText) const;  
```  
  
#### Parameters  
 `lpszStringBuf`  
 A buffer to which to write the window text.  
  
 `nMaxCount`  
 The size of the buffer in characters; also the maximum number of characters to write.  
  
 `bstrText`  
 A `BSTR` in which to store the window text.  
  
 `strText`  
 A `CString` in which to store the window text.  
  
## Return Value  
 If the text is successfully copied, the return value is **TRUE**; otherwise, the return value is **FALSE**.  
  
## Remarks  
 See [GetWindowText](http://msdn.microsoft.com/library/windows/desktop/ms633520) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The second version of this method allows you to store the text in a `BSTR`; the third version allows you to store the result in a [CString](../vs140/CStringT-Class.md), since `CSimpleString` is the base class of `CString`.  
  
## Requirements  
 **Header:** atlwin.h  
  
## See Also  
 [CWindow Class](../vs140/CWindow-Class.md)   
 [CWindow::GetWindowTextLength](../vs140/CWindow--GetWindowTextLength.md)   
 [CWindow::SetWindowText](../vs140/CWindow--SetWindowText.md)