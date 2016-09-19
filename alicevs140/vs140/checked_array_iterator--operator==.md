---
title: "checked_array_iterator::operator=="
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
ms.assetid: 0f8d6f0d-f452-435c-a7b5-23040423de3d
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# checked_array_iterator::operator==
Tests two `checked_array_iterator`s for equality.  
  
## Syntax  
  
```  
bool operator==(  
   const checked_array_iterator<_Iterator>& _Right  
) const;  
```  
  
#### Parameters  
 `_Right`  
 The `checked_array_iterator` against which to check for equality.  
  
## Remarks  
 For more information, see [Checked Iterators](../vs140/Checked-Iterators.md).  
  
## Example  
  
```  
// checked_array_iterators_opeq.cpp  
// compile with: /EHsc  
#include <iterator>  
#include <iostream>   
  
using namespace std;  
using namespace stdext;  
  
int main() {  
   int a[] = {0, 1, 2, 3, 4};  
   int b[5];  
   copy(a, a + 5, checked_array_iterator<int*>(b,5));  
   copy(a, a + 5, checked_array_iterator<int*>(b,5));  
  
   checked_array_iterator<int*> checked_output_iterator(b,5);  
   checked_array_iterator<int*> checked_output_iterator2(b,5);  
  
   if (checked_output_iterator2 == checked_output_iterator)  
      cout << "checked_array_iterators are equal" << endl;  
   else  
      cout << "checked_array_iterators are not equal" << endl;  
  
   copy (a, a + 5, checked_output_iterator);  
   checked_output_iterator++;  
  
   if (checked_output_iterator2 == checked_output_iterator)  
      cout << "checked_array_iterators are equal" << endl;  
   else  
      cout << "checked_array_iterators are not equal" << endl;  
}  
```  
  
 **checked_array_iterators are equal**  
**checked_array_iterators are not equal**   
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** stdext  
  
## See Also  
 [checked_array_iterator Class](../vs140/checked_array_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)