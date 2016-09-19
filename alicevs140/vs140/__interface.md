---
title: "__interface"
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
ms.assetid: ca5d400b-d6d8-4ba2-89af-73f67e5ec056
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __interface
**Microsoft Specific**  
  
 A Visual C++ interface can be defined as follows:  
  
-   Can inherit from zero or more base interfaces.  
  
-   Cannot inherit from a base class.  
  
-   Can only contain public, pure virtual methods.  
  
-   Cannot contain constructors, destructors, or operators.  
  
-   Cannot contain static methods.  
  
-   Cannot contain data members; properties are allowed.  
  
## Syntax  
  
```  
  
modifier  
 __interface interface-name {interface-definition};  
```  
  
## Remarks  
 A C++ [class](../vs140/class--C---.md) or [struct](../vs140/struct--C---.md) could be implemented with these rules, but `__interface` enforces them.  
  
 For example, the following is a sample interface definition:  
  
```  
__interface IMyInterface {  
   HRESULT CommitX();  
   HRESULT get_X(BSTR* pbstrName);  
};  
```  
  
 For information on managed interfaces, see [interface class](../vs140/interface-class---C---Component-Extensions-.md).  
  
 Notice that you do not have to explicitly indicate that the `CommitX` and `get_X` functions are pure virtual. An equivalent declaration for the first function would be:  
  
```  
virtual HRESULT CommitX() = 0;  
```  
  
 `__interface` implies the [novtable](../vs140/novtable.md) `__declspec` modifier.  
  
## Example  
 The following sample shows how to use properties declared in an interface.  
  
```  
// deriv_interface.cpp  
#define _ATL_ATTRIBUTES 1  
#include <atlbase.h>  
#include <atlcom.h>  
#include <string.h>  
#include <comdef.h>  
#include <stdio.h>  
  
[module(name="test")];  
  
[ object, uuid("00000000-0000-0000-0000-000000000001"), library_block ]  
__interface IFace {  
   [ id(0) ] int int_data;  
   [ id(5) ] BSTR bstr_data;  
};  
  
[ coclass, uuid("00000000-0000-0000-0000-000000000002") ]  
class MyClass : public IFace {  
private:  
    int m_i;  
    BSTR m_bstr;   
  
public:  
    MyClass()  
    {  
        m_i = 0;  
        m_bstr = 0;  
    }  
  
    ~MyClass()  
    {  
        if (m_bstr)   
            ::SysFreeString(m_bstr);  
    }  
  
    int get_int_data()  
    {  
        return m_i;  
    }  
  
    void put_int_data(int _i)   
    {  
        m_i = _i;  
    }  
  
    BSTR get_bstr_data()  
    {   
        BSTR bstr = ::SysAllocString(m_bstr);  
        return bstr;   
    }  
  
    void put_bstr_data(BSTR bstr)   
    {   
        if (m_bstr)   
            ::SysFreeString(m_bstr);  
        m_bstr = ::SysAllocString(bstr);  
    }  
};  
  
int main()  
{  
    _bstr_t bstr("Testing");  
    CoInitialize(NULL);  
    CComObject<MyClass>* p;  
    CComObject<MyClass>::CreateInstance(&p);  
    p->int_data = 100;  
    printf_s("p->int_data = %d\n", p->int_data);                
    p->bstr_data = bstr;  
    printf_s("bstr_data = %S\n", p->bstr_data);  
}  
```  
  
 **p->int_data = 100**  
**bstr_data = Testing**   
## END Microsoft Specific  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [Interface Attributes](../vs140/Interface-Attributes.md)