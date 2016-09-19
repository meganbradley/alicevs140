---
title: "Compiler Error CS1546"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 15fe2cdc-954f-4c67-80fd-9903c464f361
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1546
Property, indexer, or event 'property' is not supported by the language; try directly calling accessor method 'accessor'  
  
 Your code is consuming an object that has a default indexed property and tried to use the indexed syntax. To resolve this error, call the property's accessor method. For more information on indexers and properties, see [Indexers](../vs140/Indexers--C#-Programming-Guide-.md).  
  
 The following sample generates CS1546.  
  
## Example  
 This code sample consists of a .cpp file, which compiles to a .dll, and a .cs file, which uses that .dll. The following code is for the .dll file, and defines a property to be accessed by the code in the .cs file.  
  
```  
// CPP1546.cpp  
// compile with: /clr /LD  
using namespace System;  
public ref class MCPP  
{  
public:  
    property int Prop [int,int]  
    {  
        int get( int i, int b )  
        {  
            return i;  
        }  
    }  
};  
```  
  
## Example  
 This is the C# file.  
  
```  
// CS1546.cs  
// compile with: /r:CPP1546.dll   
using System;  
public class Test  
{  
    public static void Main()  
    {  
        int i = 0;  
        MCPP mcpp = new MCPP();  
        i = mcpp.Prop(1,1); // CS1546  
        // Try the following line instead:  
        // i = mcpp.get_Prop(1,1);  
    }  
}  
```