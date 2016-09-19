---
title: "vector::emplace_back"
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
ms.topic: article
ms.assetid: c2d38929-04b0-4e4d-8663-82810d8aa9aa
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# vector::emplace_back
Adds an element constructed in place to the end of the vector.  
  
## Syntax  
  
```  
template <class... Types>    void emplace_back(        Types&&... _Args);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Args`|Constructor arguments. The function infers which constructor overload to invoke based on the arguments provided.|  
  
## Example  
  
```cpp  
  
#include <vector>  
struct obj  
{  
   obj(int, double) {}  
};  
  
int main()  
{  
   std::vector<obj> v;  
   v.emplace_back(1, 3.14); // obj in created in place in the vector  
}  
  
```  
  
## Requirements  
 **Header:** <vector\>  
  
 **Namespace:** std  
  
## See Also  
 [vector Class](../vs140/vector-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)