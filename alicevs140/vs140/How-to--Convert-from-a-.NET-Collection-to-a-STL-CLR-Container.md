---
title: "How to: Convert from a .NET Collection to a STL-CLR Container"
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
H1: How to: Convert from a .NET Collection to a STL/CLR Container
ms.assetid: bb927c48-78e8-4150-bd0b-787c651f4a87
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert from a .NET Collection to a STL-CLR Container
This topic shows how to convert .NET collections to their equivalent STL/CLR containers. As an example we show how to convert a .NET <xref:System.Collections.Generic.List`1?qualifyHint=False> to a STL/CLR [vector](../Topic/vector%20\(STL-CLR\).md) and how to convert a .NET <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> to a STL/CLR [map](../Topic/map%20\(STL-CLR\).md), but the procedure is similar for all collections and containers.  
  
### To create a container from a collection  
  
1.  To convert an entire collection, create a STL/CLR container and pass the collection to the constructor.  
  
     The first example demonstrates this procedure.  
  
 -OR-  
  
1.  Create a generic STL/CLR container by creating a [collection_adapter](../vs140/collection_adapter--STL-CLR-.md) object. This template class takes a .NET collection interface as an argument. To verify which interfaces are supported, see [collection_adapter (STL/CLR)](../vs140/collection_adapter--STL-CLR-.md).  
  
2.  Copy the contents of the .NET collection to the container. This can be done by using a STL/CLR [algorithm](../vs140/algorithm--STL-CLR-.md), or by iterating over the .NET collection and inserting a copy of each element into the STL/CLR container.  
  
     The second example demonstrates this procedure.  
  
## Example  
 In this example, we create a generic <xref:System.Collections.Generic.List`1?qualifyHint=False> and add 5 elements to it. Then, we create a `vector` using the constructor that takes a <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> as an argument.  
  
```  
// cliext_convert_list_to_vector.cpp  
// compile with: /clr  
  
#include <cliext/adapter>  
#include <cliext/algorithm>  
#include <cliext/vector>  
  
using namespace System;  
using namespace System::Collections;  
using namespace System::Collections::Generic;  
  
int main(array<System::String ^> ^args)  
{  
    List<int> ^primeNumbersColl = gcnew List<int>();  
    primeNumbersColl->Add(2);  
    primeNumbersColl->Add(3);  
    primeNumbersColl->Add(5);  
    primeNumbersColl->Add(7);  
    primeNumbersColl->Add(11);  
  
    cliext::vector<int> ^primeNumbersCont =  
        gcnew cliext::vector<int>(primeNumbersColl);  
  
    Console::WriteLine("The contents of the cliext::vector are:");  
    cliext::vector<int>::const_iterator it;  
    for (it = primeNumbersCont->begin(); it != primeNumbersCont->end(); it++)  
    {  
        Console::WriteLine(*it);  
    }  
}  
```  
  
 **The contents of the cliext::vector are:**  
**2**  
**3**  
**5**  
**7**  
**11**   
## Example  
 In this example, we create a generic <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> and add 5 elements to it. Then, we create a `collection_adapter` to wrap the <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> as a simple STL/CLR container. Finally, we create a `map` and copy the contents of the <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> to the `map` by iterating over the `collection_adapter`. During this process, we create a new pair by using the `make_pair` function, and insert the new pair directly into the `map`.  
  
```  
// cliext_convert_dictionary_to_map.cpp  
// compile with: /clr  
  
#include <cliext/adapter>  
#include <cliext/algorithm>  
#include <cliext/map>  
  
using namespace System;  
using namespace System::Collections;  
using namespace System::Collections::Generic;  
  
int main(array<System::String ^> ^args)  
{  
    System::Collections::Generic::Dictionary<float, int> ^dict =  
        gcnew System::Collections::Generic::Dictionary<float, int>();  
    dict->Add(42.0, 42);  
    dict->Add(13.0, 13);  
    dict->Add(74.0, 74);  
    dict->Add(22.0, 22);  
    dict->Add(0.0, 0);  
  
    cliext::collection_adapter<System::Collections::Generic::IDictionary<float, int>> dictAdapter(dict);  
    cliext::map<float, int> aMap;  
    for each (KeyValuePair<float, int> ^kvp in dictAdapter)  
    {  
        cliext::pair<float, int> aPair = cliext::make_pair(kvp->Key, kvp->Value);  
        aMap.insert(aPair);  
    }  
  
    Console::WriteLine("The contents of the cliext::map are:");  
    cliext::map<float, int>::const_iterator it;  
    for (it = aMap.begin(); it != aMap.end(); it++)  
    {  
        Console::WriteLine("Key: {0:F} Value: {1}", it->first, it->second);  
    }  
}  
```  
  
 **The contents of the cliext::map are:**  
**Key: 0.00 Value: 0**  
**Key: 13.00 Value: 13**  
**Key: 22.00 Value: 22**  
**Key: 42.00 Value: 42**  
**Key: 74.00 Value: 74**   
## See Also  
 [STL/CLR Library Reference](../vs140/STL-CLR-Library-Reference.md)   
 [adapter (STL/CLR)](../vs140/adapter--STL-CLR-.md)   
 [How to: Convert from a STL/CLR Container to a .NET Collection](../Topic/How%20to:%20Convert%20from%20a%20STL-CLR%20Container%20to%20a%20.NET%20Collection.md)