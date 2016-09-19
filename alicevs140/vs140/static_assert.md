---
title: "static_assert"
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
ms.assetid: 28dd3668-e78c-4de8-ba68-552084743426
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# static_assert
Tests a software assertion at compile time. If the specified constant expression is `false`, the compiler displays the specified message and the compilation fails with error C2338; otherwise, the declaration has no effect.  
  
## Syntax  
  
```  
static_assert(   
    constant-expression,   
    string-literal   
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`constant-expression`|An integral constant expression that can be converted to a Boolean.<br /><br /> If the evaluated expression is zero (false), the `string-literal` parameter is displayed and the compilation fails with an error. If the expression is nonzero (true), the `static_assert` declaration has no effect.|  
|`string-literal`|An message that is displayed if the `constant-expression` parameter is zero. The message is a string of characters in the [base character set](../vs140/ASCII-Character-Set.md) of the compiler; that is, not [multibyte or wide characters](../vs140/Multibyte-and-Wide-Characters.md).|  
  
## Remarks  
 The `constant-expression` parameter of a `static_assert` declaration represents a *software assertion*. A software assertion specifies a condition that you expect to be true at a particular point in your program. If the condition is true, the `static_assert` declaration has no effect. If the condition is false, the assertion fails, the compiler displays the message in `string-literal` parameter, and the compilation fails with an error.  
  
 The `static_assert` declaration tests a software assertion at compile time. In contrast, the [assert (CRT)](../vs140/assert-Macro--_assert--_wassert.md) macro tests a software assertion at run time and incurs a run time cost in space or time. The `static_assert` declaration is especially useful for debugging templates because template arguments can be included in the `constant-expression` parameter.  
  
 The compiler examines the `static_assert` declaration for syntax errors when the declaration is encountered. The compiler evaluates the `constant-expression` parameter immediately if it does not depend on a template parameter. Otherwise, the compiler evaluates the `constant-expression` parameter when the template is instantiated. Consequently, the compiler might issue a diagnostic message once when the declaration is encountered, and again when the template is instantiated.  
  
 You can use the `static_assert` keyword at namespace, class, or block scope. (The `static_assert` keyword is technically a declaration, even though it does not introduce new name into your program, because it can be used at namespace scope.)  
  
## Description  
 In the following example, the `static_assert` declaration has namespace scope. Because the compiler knows the size of type `void *`, the expression is evaluated immediately.  
  
## Example  
  
```  
static_assert(sizeof(void *) == 4, "64-bit code generation is not supported.");  
```  
  
## Description  
 In the following example, the `static_assert` declaration has class scope. The `static_assert` verifies that a template parameter is a *plain old data* (POD) type. The compiler examines the `static_assert` declaration when it is declared, but does not evaluate the `constant-expression` parameter until the `basic_string` class template is instantiated in `main()`.  
  
## Example  
  
```  
#include <type_traits>  
#include <iosfwd>  
namespace std {  
template <class CharT, class Traits = std::char_traits<CharT> >  
class basic_string {  
    static_assert(tr1::is_pod<CharT>::value,  
                  "Template argument CharT must be a POD type in class template basic_string");  
    // ...  
    };  
}  
struct NonPOD {  
    NonPOD(const NonPOD &) {}  
    virtual ~NonPOD() {}  
};  
int main()  
{  
    std::basic_string<char> bs;  
}  
```  
  
## Description  
 In the following example, the `static_assert` declaration has block scope. The `static_assert` verifies that the size of the VMPage structure is equal to the virtual memory pagesize of the system.  
  
## Example  
  
```  
#include <sys/param.h> // defines PAGESIZE  
class VMMClient {  
public:  
    struct VMPage { // ...   
           };  
    int check_pagesize() {  
    static_assert(sizeof(VMPage) == PAGESIZE,  
        "Struct VMPage must be the same size as a system virtual memory page.");  
    // ...  
    }  
// ...  
};  
```  
  
## See Also  
 [Error Handling (C++)](../vs140/Assertion-and-User-Supplied-Messages--C---.md)   
 [The #error Directive](../vs140/#error-Directive--C-C---.md)   
 [assert (CRT)](../vs140/assert-Macro--_assert--_wassert.md)   
 [Templates](../vs140/Templates--C---.md)   
 [The ASCII Character Set](../vs140/ASCII-Character-Set.md)   
 [Declarations](../vs140/Declarations.md)