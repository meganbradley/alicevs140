---
title: "set::operator="
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
ms.assetid: 20183766-3575-430a-aee2-84f2bb647a3e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# set::operator=
Replaces the elements of this `set` using elements from another `set`.  
  
## Syntax  
  
```  
set& operator=(  
   const set& _Right  
);  
set& operator=(  
   set&& _Right  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`_Right`|The `set` providing new elements to be assigned to this `set`.|  
  
## Remarks  
 The first version of `operator=` uses an [lvalue reference](../vs140/Lvalue-Reference-Declarator---.md) for `_Right`, to copy elements from `_Right` to this `set`.  
  
 The second version uses an [rvalue reference](../vs140/Rvalue-Reference-Declarator----.md) for _Right. It moves elements from `_Right` to this `set`.  
  
 Any elements in this `set` before the operator function executes are discarded.  
  
## Example  
  
```  
// set_operator_as.cpp  
// compile with: /EHsc  
#include <set>  
#include <iostream>  
  
int main( )  
   {  
   using namespace std;  
   set<int> v1, v2, v3;  
   set<int>::iterator iter;  
  
   v1.insert(10);  
  
   cout << "v1 = " ;  
   for (iter = v1.begin(); iter != v1.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
  
   v2 = v1;  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
  
// move v1 into v2  
   v2.clear();  
   v2 = move(v1);  
   cout << "v2 = ";  
   for (iter = v2.begin(); iter != v2.end(); iter++)  
      cout << *iter << " ";  
   cout << endl;  
   }  
```  
  
## Output  
  
```  
v1 = 10   
v2 = 10   
v2 = 10   
```  
  
## Requirements  
 **Header:** <set\>  
  
 **Namespace:** std  
  
## See Also  
 [set Class](../vs140/set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)   
 [Lvalues and Rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)