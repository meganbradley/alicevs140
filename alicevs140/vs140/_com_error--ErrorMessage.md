---
title: "_com_error::ErrorMessage"
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
ms.topic: language-reference
ms.assetid: e47335b6-01af-4975-a841-121597479eb7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _com_error::ErrorMessage
**Microsoft Specific**  
  
 Retrieves the string message for `HRESULT` stored in the `_com_error` object.  
  
## Syntax  
  
```  
  
const TCHAR * ErrorMessage( ) const throw( );  
  
```  
  
## Return Value  
 Returns the string message for the `HRESULT` recorded within the `_com_error` object. If the `HRESULT` is a mapped 16-bit [wCode](../vs140/_com_error--WCode.md), then a generic message "`IDispatch error #<wCode>`" is returned. If no message is found, then a generic message "`Unknown error #<hresult>`" is returned. The returned string is either a Unicode or multibyte string, depending on the state of the **_UNICODE** macro.  
  
## Remarks  
 Retrieves the appropriate system message text for `HRESULT` recorded within the `_com_error` object. The system message text is obtained by calling the Win32 [FormatMessage](http://msdn.microsoft.com/library/windows/desktop/ms679351) function. The string returned is allocated by the `FormatMessage` API, and it is released when the `_com_error` object is destroyed.  
  
 **END Microsoft Specific**  
  
## See Also  
 [_com_error Class](../vs140/_com_error-Class.md)