---
title: "Compiler Error CS1917"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 05688706-e4b4-4273-9244-48cce1f7f9b9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1917
Members of read-only field 'name' of type 'struct name' cannot be assigned with an object initializer because it is of a value type.  
  
 Read-only fields that are value types can only be assigned in a constructor.  
  
### To correct this error  
  
-   Change the struct to a class type.  
  
-   Initialize the struct with a constructor.  
  
## Example  
 The following code generates CS1917:  
  
```  
// cs1917.cs  
class CS1917  
{  
    public struct TestStruct  
    {  
        public int i;  
    }  
    public class C  
    {  
        public readonly TestStruct str = new TestStruct();  
        public static int Main()  
        {  
            C c = new C { str = { i = 1 } }; // CS1917  
            return 0;  
        }  
    }  
}  
```