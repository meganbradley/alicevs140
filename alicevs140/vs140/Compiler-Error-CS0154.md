---
title: "Compiler Error CS0154"
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
ms.topic: article
ms.assetid: 815150da-09b4-4593-825f-1dd435c92da8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0154
The property or indexer 'property' cannot be used in this context because it lacks the get accessor  
  
 An attempt to use a [property](../vs140/Using-Properties--C#-Programming-Guide-.md) failed because no get accessor method was defined in the property. For more information, see [Properties and Fields (C# Programmer's Reference)](../vs140/Fields--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0154:  
  
```  
// CS0154.cs  
public class MyClass2  
{  
    public int i  
    {  
        set  
        {  
        }  
        // uncomment the get method to resolve this error  
        /*  
        get  
        {  
            return 0;  
        }  
        */  
    }  
}  
  
public class MyClass  
{  
    public static void Main()  
    {  
        MyClass2 myClass2 = new MyClass2();  
        int j = myClass2.i;   // CS0154, no get method  
    }  
}  
```