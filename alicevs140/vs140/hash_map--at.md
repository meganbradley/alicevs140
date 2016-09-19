---
title: "hash_map::at"
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
ms.assetid: 56881eba-3936-4072-80a7-3f03c734c376
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hash_map::at
> [!NOTE]
>  This API is obsolete. The alternative is [unordered_map Class](../vs140/unordered_map-Class.md).  
  
 Finds an element in a hash_map with a specified key value.  
  
## Syntax  
  
```  
  
      Type& at(  
   const Key& _Key  
);  
const Type& at(  
   const Key& _Key  
) const;  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|`_Key`|The key value of the element that is to be found.|  
  
## Return Value  
 A reference to the data value of the element found.  
  
## Remarks  
 If the argument key value is not found, then the function throws an object of class [out_of_range](../vs140/out_of_range-Class.md).  
  
 In Visual C++ .NET 2003, members of the [<hash_map>](../vs140/-hash_map-.md) and [<hash_set>](../vs140/-hash_set-.md) header files are no longer in the std namespace, but rather have been moved into the stdext namespace. See [The stdext Namespace](../vs140/stdext-Namespace.md) for more information.  
  
## Example  
  
```  
// hash_map_at.cpp  
// compile with: /EHsc  
#include <hash_map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   using namespace stdext;  
   typedef pair <const int, int> cInt2Int;  
   hash_map <int, int> hm1;  
  
   // Insert data values  
   hm1.insert ( cInt2Int ( 1, 10 ) );  
   hm1.insert ( cInt2Int ( 2, 20 ) );  
   hm1.insert ( cInt2Int ( 3, 30 ) );  
  
   cout  << "The values of the mapped elements are:";  
   for ( int i = 1 ; i <= hm1.size() ; i++ )  
      cout << " " << hm1.at(i);  
   cout << "." << endl;  
}  
```  
  
## Output  
  
```  
The values of the mapped elements are: 10 20 30.  
```  
  
## Requirements  
 **Header:** <hash_map>  
  
 **Namespace:** stdext  
  
## See Also  
 [hash_map Class](../vs140/hash_map-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)