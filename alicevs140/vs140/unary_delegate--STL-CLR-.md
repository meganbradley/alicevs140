---
title: "unary_delegate (STL-CLR)"
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
H1: unary_delegate (STL/CLR)
ms.assetid: b3ee253c-98e8-466e-a272-505e47aed061
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unary_delegate (STL-CLR)
The genereic class describes a one-argument delegate. You use it specify a delegate in terms of its argument and return types.  
  
## Syntax  
  
```  
generic<typename Arg,  
    typename Result>  
    delegate Result unary_delegate(Arg);  
```  
  
#### Parameters  
 Arg  
 The type of the argument.  
  
 Result  
 The return type.  
  
## Remarks  
 The genereic delegate describes a one-argument function.  
  
 Note that for:  
  
 `unary_delegare<int, int> Fun1;`  
  
 `unary_delegare<int, int> Fun2;`  
  
 the types `Fun1` and `Fun2` are synonyms, while for:  
  
 `delegate int Fun1(int);`  
  
 `delegate int Fun2(int);`  
  
 they are not the same type.  
  
## Example  
  
```  
// cliext_unary_delegate.cpp   
// compile with: /clr   
#include <cliext/functional>   
  
int hash_val(wchar_t val)   
    {   
    return ((val * 17 + 31) % 67);   
    }   
  
typedef cliext::unary_delegate<wchar_t, int> Mydelegate;   
int main()   
    {   
    Mydelegate^ myhash = gcnew Mydelegate(&hash_val);   
  
    System::Console::WriteLine("hash(L'a') = {0}", myhash(L'a'));   
    System::Console::WriteLine("hash(L'b') = {0}", myhash(L'b'));   
    return (0);   
    }  
  
```  
  
 **hash(L'a') = 5**  
**hash(L'b') = 22**   
## Requirements  
 **Header:** <cliext/functional>  
  
 **Namespace:** cliext  
  
## See Also  
 [binary_delegate](../vs140/binary_delegate--STL-CLR-.md)   
 [binary_delegate_noreturn](../vs140/binary_delegate_noreturn--STL-CLR-.md)   
 [unary_delegate_noreturn](../vs140/unary_delegate_noreturn--STL-CLR-.md)