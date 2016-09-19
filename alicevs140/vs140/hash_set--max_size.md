---
title: "hash_set::max_size"
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
ms.assetid: 7ab102b2-613d-4aad-b0c8-6822715581f0
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_set::max_size
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_set Class](../vs140/unordered_set-Class.md).  
  
 Returns the maximum length of the hash_set.  
  
## Syntax  
  
```  
  
size_type max_size( ) const;  
  
```  
  
## Return Value  
 The maximum possible length of the hash_set.  
  
## Remarks  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_set_max_size.cpp  
// compile with: /EHsc  
#include <hash_set>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   hash_set <int> hs1;  
   hash_set <int>::size_type i;  
  
   i = hs1.max_size( );  
   cout << "The maximum possible length "  
        << "of the hash_set is " << i << "." << endl;  
}  
```  
  
## Sample Output  
 The following output is for x86.  
  
```  
The maximum possible length of the hash_set is 1073741823.  
```  
  
## Requirements  
 **Header:** <hash_set>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_set Class](../vs140/hash_set-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)