---
title: "&lt;map&gt; operators"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7df02b9f-701c-44ed-834a-a819badc5bd0
caps.latest.revision: 7
---
# &lt;map&gt; operators
||||  
|-|-|-|  
|[operator!= (map)](#operator_neq)|[operator&gt; (map)](#operator_gt_)|[operator&gt;= (map)](#operator_gt__eq)|  
|[operator&lt; (map)](#operator_lt_)|[operator&lt;= (map)](#operator_lt__eq)|[operator== (map)](#operator_eq_eq)|  
|[operator!= (multimap)](#operator_neq_multimap)|[operator&gt; (multimap)](#operator_gt_multimap)|[operator&gt;= (multimap)](#operator_gt__eq_multimap)|  
|[operator&lt; (multimap)](#operator_lt_multimap)|[operator&lt;= (multimap)](#operator_lt__eq_multimap)|[operator== (multimap)](#operator_eq_eq_multimap)|  
  
##  <a name="operator_neq"></a>  operator!=  
 Tests if the map object on the left side of the operator is not equal to the map object on the right side.  
  
```  
bool operator!=(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the maps are not equal; **false** if maps are equal.  
  
### Remarks  
 The comparison between map objects is based on a pairwise comparison of their elements. Two maps are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
### Example  
  
```  
// map_op_ne.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map <int, int> m1, m2, m3;  
   int i;  
   typedef pair <int, int> Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 != m2 )  
      cout << "The maps m1 and m2 are not equal." << endl;  
   else  
      cout << "The maps m1 and m2 are equal." << endl;  
  
   if ( m1 != m3 )  
      cout << "The maps m1 and m3 are not equal." << endl;  
   else  
      cout << "The maps m1 and m3 are equal." << endl;  
}  
\* Output:   
The maps m1 and m2 are not equal.  
The maps m1 and m3 are equal.  
*\  
```  
  
##  <a name="operator_lt_"></a>  operator&lt;  
 Tests if the map object on the left side of the operator is less than the map object on the right side.  
  
```  
bool operator<(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the map on the left side of the operator is strictly less than the map on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between map objects is based on a pairwise comparison of their elements. The less-than relationship between two objects is based on a comparison of the first pair of unequal elements.  
  
### Example  
  
```  
// map_op_lt.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map<int, int> m1, m2, m3;  
   int i;  
   typedef pair<int, int> Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
   }  
  
   if ( m1 < m2 )  
      cout << "The map m1 is less than the map m2." << endl;  
   else  
      cout << "The map m1 is not less than the map m2." << endl;  
  
   if ( m1 < m3 )  
      cout << "The map m1 is less than the map m3." << endl;  
   else  
      cout << "The map m1 is not less than the map m3." << endl;  
}  
\* Output:   
The map m1 is less than the map m2.  
The map m1 is not less than the map m3.  
*\  
```  
  
##  <a name="operator_lt__eq"></a>  operator&lt;=  
 Tests if the map object on the left side of the operator is less than or equal to the map object on the right side.  
  
```  
bool operator<=(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the map on the left side of the operator is less than or equal to the map on the right side of the operator; otherwise **false**.  
  
### Example  
  
```  
// map_op_le.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map <int, int> m1, m2, m3, m4;  
   int i;  
   typedef pair <int, int> Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
      m4.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 <= m2 )  
      cout << "The map m1 is less than or equal to the map m2." << endl;  
   else  
      cout << "The map m1 is greater than the map m2." << endl;  
  
   if ( m1 <= m3 )  
      cout << "The map m1 is less than or equal to the map m3." << endl;  
   else  
      cout << "The map m1 is greater than the map m3." << endl;  
  
   if ( m1 <= m4 )  
      cout << "The map m1 is less than or equal to the map m4." << endl;  
   else  
      cout << "The map m1 is greater than the map m4." << endl;  
}  
\* Output:   
The map m1 is less than or equal to the map m2.  
The map m1 is greater than the map m3.  
The map m1 is less than or equal to the map m4.  
*\  
```  
  
##  <a name="operator_eq_eq"></a>  operator==  
 Tests if the map object on the left side of the operator is equal to the map object on the right side.  
  
```  
bool operator==(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the map on the left side of the operator is equal to the map on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between map objects is based on a pairwise comparison of their elements. Two maps are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
### Example  
  
```  
// map_op_eq.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map < int, int > m1, m2, m3;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 == m2 )  
      cout << "The maps m1 and m2 are equal." << endl;  
   else  
      cout << "The maps m1 and m2 are not equal." << endl;  
  
   if ( m1 == m3 )  
      cout << "The maps m1 and m3 are equal." << endl;  
   else  
      cout << "The maps m1 and m3 are not equal." << endl;  
}  
\* Output:   
The maps m1 and m2 are not equal.  
The maps m1 and m3 are equal.  
*\  
```  
  
##  <a name="operator_gt_"></a>  operator&gt;  
 Tests if the map object on the left side of the operator is greater than the map object on the right side.  
  
```  
bool operator>(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the map on the left side of the operator is greater than the map on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between map objects is based on a pairwise comparison of their elements. The greater-than relationship between two objects is based on a comparison of the first pair of unequal elements.  
  
### Example  
  
```  
// map_op_gt.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map < int, int > m1, m2, m3;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
   }  
  
   if ( m1 > m2 )  
      cout << "The map m1 is greater than the map m2." << endl;  
   else  
      cout << "The map m1 is not greater than the map m2." << endl;  
  
   if ( m1 > m3 )  
      cout << "The map m1 is greater than the map m3." << endl;  
   else  
      cout << "The map m1 is not greater than the map m3." << endl;  
}  
\* Output:   
The map m1 is not greater than the map m2.  
The map m1 is greater than the map m3.  
*\  
```  
  
##  <a name="operator_gt__eq"></a>  operator&gt;=  
 Tests if the map object on the left side of the operator is greater than or equal to the map object on the right side.  
  
```  
bool operator>=(    const map <Key, Type, Traits, Allocator>&  _Left ,    const map <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type **map**.  
  
 `_Right`  
 An object of type **map**.  
  
### Return Value  
 **true** if the map on the left side of the operator is greater than or equal to the map on the right side of the list; otherwise **false**.  
  
### Example  
  
```  
// map_op_ge.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   map < int, int > m1, m2, m3, m4;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
      m4.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 >= m2 )  
      cout << "Map m1 is greater than or equal to map m2." << endl;  
   else  
      cout << "The map m1 is less than the map m2." << endl;  
  
   if ( m1 >= m3 )  
      cout << "Map m1 is greater than or equal to map m3." << endl;  
   else  
      cout << "The map m1 is less than the map m3." << endl;  
  
   if ( m1 >= m4 )  
      cout << "Map m1 is greater than or equal to map m4." << endl;  
   else  
      cout << "The map m1 is less than the map m4." << endl;  
}  
\* Output:   
The map m1 is less than the map m2.  
Map m1 is greater than or equal to map m3.  
Map m1 is greater than or equal to map m4.  
*\  
```  
  
##  <a name="operator_neq_multimap"></a>  operator!= (multimap)  
 Tests if the multimap object on the left side of the operator is not equal to the multimap object on the right side.  
  
```  
bool operator!=(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimaps are not equal; **false** if multimaps are equal.  
  
### Remarks  
 The comparison between multimap objects is based on a pairwise comparison of their elements. Two multimaps are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
### Example  
  
```  
// multimap_op_ne.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap <int, int> m1, m2, m3;  
   int i;  
   typedef pair <int, int> Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 != m2 )  
      cout << "The multimaps m1 and m2 are not equal." << endl;  
   else  
      cout << "The multimaps m1 and m2 are equal." << endl;  
  
   if ( m1 != m3 )  
      cout << "The multimaps m1 and m3 are not equal." << endl;  
   else  
      cout << "The multimaps m1 and m3 are equal." << endl;  
}  
\* Output:   
The multimaps m1 and m2 are not equal.  
The multimaps m1 and m3 are equal.  
*\  
```  
  
##  <a name="operator_lt_multimap"></a>  operator&lt;  
 Tests if the multimap object on the left side of the operator is less than the multimap object on the right side.  
  
```  
bool operator<(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimap on the left side of the operator is strictly less than the multimap on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between multimap objects is based on a pairwise comparison of their elements. The less-than relationship between two objects is based on a comparison of the first pair of unequal elements.  
  
### Example  
  
```  
// multimap_op_lt.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap < int, int > m1, m2, m3;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
   }  
  
   if ( m1 < m2 )  
      cout << "The multimap m1 is less than the multimap m2." << endl;  
   else  
      cout << "The multimap m1 is not less than the multimap m2." << endl;  
  
   if ( m1 < m3 )  
      cout << "The multimap m1 is less than the multimap m3." << endl;  
   else  
      cout << "The multimap m1 is not less than the multimap m3." << endl;  
}  
\* Output:   
The multimap m1 is less than the multimap m2.  
The multimap m1 is not less than the multimap m3.  
*\  
```  
  
##  <a name="operator_lt__eq_multimap"></a>  operator&lt;=  
 Tests if the multimap object on the left side of the operator is less than or equal to the multimap object on the right side.  
  
```  
bool operator<=(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimap on the left side of the operator is less than or equal to the multimap on the right side of the operator; otherwise **false**.  
  
### Example  
  
```  
// multimap_op_le.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap <int, int> m1, m2, m3, m4;  
   int i;  
   typedef pair <int, int> Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
      m4.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 <= m2 )  
      cout << "m1 is less than or equal to m2" << endl;  
   else  
      cout << "m1 is greater than m2" << endl;  
  
   if ( m1 <= m3 )  
      cout << "m1 is less than or equal to m3" << endl;  
   else  
      cout << "m1 is greater than m3" << endl;  
  
   if ( m1 <= m4 )  
      cout << "m1 is less than or equal to m4" << endl;  
   else  
      cout << "m1 is greater than m4" << endl;  
}  
\* Output:   
m1 is less than or equal to m2  
m1 is greater than m3  
m1 is less than or equal to m4  
*\  
```  
  
##  <a name="operator_eq_eq_multimap"></a>  operator==  
 Tests if the multimap object on the left side of the operator is equal to the multimap object on the right side.  
  
```  
bool operator==(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimap on the left side of the operator is equal to the multimap on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between multimap objects is based on a pairwise comparison of their elements. Two multimaps are equal if they have the same number of elements and their respective elements have the same values. Otherwise, they are unequal.  
  
### Example  
  
```  
// multimap_op_eq.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap<int, int> m1, m2, m3;  
   int i;  
   typedef pair<int, int> Int_Pair;  
  
   for (i = 0; i < 3; i++)  
   {  
      m1.insert(Int_Pair(i, i));  
      m2.insert(Int_Pair(i, i*i));  
      m3.insert(Int_Pair(i, i));  
   }  
  
   if ( m1 == m2 )  
      cout << "m1 and m2 are equal" << endl;  
   else  
      cout << "m1 and m2 are not equal" << endl;  
  
   if ( m1 == m3 )  
      cout << "m1 and m3 are equal" << endl;  
   else  
      cout << "m1 and m3 are not equal" << endl;  
}  
\* Output:   
m1 and m2 are not equal  
m1 and m3 are equal  
*\  
```  
  
##  <a name="operator_gt_multimap"></a>  operator&gt;  
 Tests if the multimap object on the left side of the operator is greater than the multimap object on the right side.  
  
```  
bool operator>(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimap on the left side of the operator is greater than the multimap on the right side of the operator; otherwise **false**.  
  
### Remarks  
 The comparison between multimap objects is based on a pairwise comparison of their elements. The greater-than relationship between two objects is based on a comparison of the first pair of unequal elements.  
  
### Example  
  
```  
// multimap_op_gt.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap < int, int > m1, m2, m3;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 0 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
   }  
  
   if ( m1 > m2 )  
      cout << "The multimap m1 is greater than the multimap m2." << endl;  
   else  
      cout << "Multimap m1 is not greater than multimap m2." << endl;  
  
   if ( m1 > m3 )  
      cout << "The multimap m1 is greater than the multimap m3." << endl;  
   else  
      cout << "The multimap m1 is not greater than the multimap m3." << endl;  
}  
\* Output:   
Multimap m1 is not greater than multimap m2.  
The multimap m1 is greater than the multimap m3.  
*\  
```  
  
##  <a name="operator_gt__eq_multimap"></a>  operator&gt;=  
 Tests if the multimap object on the left side of the operator is greater than or equal to the multimap object on the right side.  
  
```  
bool operator>=(    const multimap <Key, Type, Traits, Allocator>&  _Left ,    const multimap <Key, Type, Traits, Allocator>&  _Right );  
  
```  
  
### Parameters  
 `_Left`  
 An object of type `multimap`.  
  
 `_Right`  
 An object of type `multimap`.  
  
### Return Value  
 **true** if the multimap on the left side of the operator is greater than or equal to the multimap on the right side of the list; otherwise **false**.  
  
### Example  
  
```  
// multimap_op_ge.cpp  
// compile with: /EHsc  
#include <map>  
#include <iostream>  
  
int main( )  
{  
   using namespace std;  
   multimap < int, int > m1, m2, m3, m4;  
   int i;  
   typedef pair < int, int > Int_Pair;  
  
   for ( i = 1 ; i < 3 ; i++ )  
   {  
      m1.insert ( Int_Pair ( i, i ) );  
      m2.insert ( Int_Pair ( i, i * i ) );  
      m3.insert ( Int_Pair ( i, i - 1 ) );  
      m4.insert ( Int_Pair ( i, i ) );  
   }  
  
   if ( m1 >= m2 )  
      cout << "The multimap m1 is greater than or equal to the multimap m2." << endl;  
   else  
      cout << "The multimap m1 is less than the multimap m2." << endl;  
  
   if ( m1 >= m3 )  
      cout << "The multimap m1 is greater than or equal to the multimap m3." << endl;  
   else  
      cout << "The multimap m1 is less than the multimap m3." << endl;  
  
   if ( m1 >= m4 )  
      cout << "The multimap m1 is greater than or equal to the multimap m4." << endl;  
   else  
      cout << "The multimap m1 is less than the multimap m4." << endl;  
}  
\* Output:   
The multimap m1 is less than the multimap m2.  
The multimap m1 is greater than or equal to the multimap m3.  
The multimap m1 is greater than or equal to the multimap m4.  
*\  
```  
  
## See Also  
 [&lt;map&gt;](../vs140/-map-.md)