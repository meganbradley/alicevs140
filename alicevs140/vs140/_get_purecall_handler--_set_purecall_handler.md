---
title: "_get_purecall_handler, _set_purecall_handler"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _set_purecall_handler
  - _set_purecall_handler_m
  - _get_purecall_handler
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr120_clr0400.dll
  - api-ms-win-core-crt-l2-1-0.dll
  - ntoskrnl.exe
apitype: DLLExport
ms.assetid: 2759b878-8afa-4129-86e7-72afc2153d9c
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _get_purecall_handler, _set_purecall_handler
Gets or sets the error handler for a pure virtual function call.  
  
## Syntax  
  
```  
typedef void (__cdecl* _purecall_handler)(void);  
  
_purecall_handler __cdecl _get_purecall_handler(void);  
  
_purecall_handler __cdecl _set_purecall_handler(   
   _purecall_handler function  
);  
```  
  
#### Parameters  
 `function`  
 The function to be called when a pure virtual function is called. A `_purecall_handler` function must have a void return type.  
  
## Return Value  
 The previous `_purecall_handler`. Returns `nullptr` if there was no previous handler.  
  
## Remarks  
 The `_get_purecall_handler` and `_set_purecall_handler` functions are Microsoft-specific and apply only to C++ code.  
  
 A call to a pure virtual function is an error because it has no implementation. By default, the compiler generates code to invoke an error handler function when a pure virtual function is called, which terminates the program. You can install your own error handler function for pure virtual function calls, to catch them for debugging or reporting purposes. To use your own error handler, create a function that has the `_purecall_handler` signature, then use `_set_purecall_handler` to make it the current handler.  
  
 Because there is only one `_purecall_handler` for each process, when you call `_set_purecall_handler` it immediately impacts all threads. The last caller on any thread sets the handler.  
  
 To restore the default behavior, call `_set_purecall_handler` by using a `nullptr` argument.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_get_purecall_handler`, `_set_purecall_handler`|<cstdlib\> or <stdlib.h>|  
  
 For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// _set_purecall_handler.cpp  
// compile with: /W1  
#include <tchar.h>  
#include <stdio.h>  
#include <stdlib.h>  
  
class CDerived;  
class CBase  
{  
public:  
   CBase(CDerived *derived): m_pDerived(derived) {};  
   ~CBase();  
   virtual void function(void) = 0;  
  
   CDerived * m_pDerived;  
};  
  
class CDerived : public CBase  
{  
public:  
   CDerived() : CBase(this) {};   // C4355  
   virtual void function(void) {};  
};  
  
CBase::~CBase()  
{  
   m_pDerived -> function();  
}  
  
void myPurecallHandler(void)  
{  
   printf("In _purecall_handler.");  
   exit(0);  
}  
  
int _tmain(int argc, _TCHAR* argv[])  
{  
   _set_purecall_handler(myPurecallHandler);  
   CDerived myDerived;  
}  
```  
  
 **In _purecall_handler.**   
## See Also  
 [Error Handling](../vs140/Error-Handling--CRT-.md)   
 [_purecall](../vs140/_purecall.md)