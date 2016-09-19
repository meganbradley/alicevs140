---
title: "_set_com_error_handler"
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
ms.assetid: 49fe4fca-5e37-4d83-abaf-15be5ce37f94
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _set_com_error_handler
**Microsoft Specific**  
  
 Replaces the default function that is used for COM error-handling.  
  
## Syntax  
  
```  
void __stdcall _set_com_error_handler(  
   void (__stdcall *pHandler)(  
      HRESULT hr,   
      IErrorInfo* perrinfo  
   )  
);  
```  
  
#### Parameters  
 `pHandler`  
 Pointer to the replacement function.  
  
 `hr`  
 `HRESULT` information.  
  
 `perrinfo`  
 `IErrorInfo` object.  
  
## Remarks  
 By default, [_com_raise_error](../vs140/_com_raise_error.md) handles all COM errors. You can change this behavior by using `_set_com_error_handler` to call your own error-handling function.  
  
 The replacement function must have a signature that is equivalent to that of `_com_raise_error`.  
  
## Example  
  
```  
// _set_com_error_handler.cpp  
// compile with /EHsc  
#include <stdio.h>  
#include <comdef.h>  
#include <comutil.h>  
  
// Importing ado dll to attempt to establish an ado connection.  
// Not related to _set_com_error_handler   
#import "C:\Program Files\Common Files\System\ado\msado15.dll" no_namespace rename("EOF", "adoEOF")  
  
void __stdcall _My_com_raise_error(HRESULT hr, IErrorInfo* perrinfo)  
{  
   throw "Unable to establish the connection!";  
}  
  
int main()  
{  
   _set_com_error_handler(_My_com_raise_error);  
   _bstr_t bstrEmpty(L"");  
   _ConnectionPtr Connection = NULL;  
   try  
   {  
      Connection.CreateInstance(__uuidof(Connection));  
      Connection->Open(bstrEmpty, bstrEmpty, bstrEmpty, 0);   
   }  
   catch(char* errorMessage)  
   {  
      printf("Exception raised: %s\n", errorMessage);  
   }  
  
   return 0;  
}  
```  
  
 **Exception raised: Unable to establish the connection!**   
## Requirements  
 **Header:** comdef.h  
  
 **Lib:** If the “wchar_t is Native Type” compiler option is on, use comsuppw.lib or comsuppwd.lib. If “wchar_t is Native Type” is off, use comsupp.lib. For more information, see [/Zc:wchar_t (wchar_t Is Native Type)](../Topic/-Zc:wchar_t%20\(wchar_t%20Is%20Native%20Type\).md).  
  
## See Also  
 [Compiler COM Global Functions](../vs140/Compiler-COM-Global-Functions.md)