---
title: "Compiler Error C3345"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1dda4c79-73bb-441b-b939-746154c3afba
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3345
'identifier': invalid identifier for module name  
  
 The *identifier* for a module contains one or more unacceptable characters. An identifier is valid if the first character is an alphabetical, underscore, or high ANSI (0x80-FF) character, and any subsequent character is an alphanumeric, underscore, or high ANSI character.  
  
### To correct this error  
  
1.  Ensure that *identifier* does not contain blanks or other unacceptable characters.  
  
## Example  
 The following code example causes error message C3345 because the `name` parameter of the `module` attribute contains a blank.  
  
```  
// cpp_attr_name_module.cpp  
// compile with: /LD /link /OPT:NOREF  
#include <atlbase.h>  
#include <atlcom.h>  
#include <atlwin.h>  
#include <atltypes.h>  
#include <atlctl.h>  
#include <atlhost.h>  
#include <atlplus.h>  
  
// C3345 expected  
[module(dll, name="My Library", version="1.2", helpfile="MyHelpFile")]   
// Try the following line instead  
//[module(dll, name="MyLibrary", version="1.2", helpfile="MyHelpFile")]   
// Module attribute now applies to this class  
class CMyClass {  
public:  
BOOL WINAPI DllMain(DWORD dwReason, LPVOID lpReserved) {  
   // add your own code here  
   return __super::DllMain(dwReason, lpReserved);  
   }  
};  
```  
  
## See Also  
 [__iscsym](../vs140/iscsym--iscsymf--__iscsym--__iswcsym--__iscsymf--__iswcsymf--_iscsym_l--_iswcsym_l--_iscsymf_l--_iswcsymf_l.md)   
 [Character Classification](../vs140/Character-Classification.md)   
 [module (C++)](../vs140/module--C---.md)