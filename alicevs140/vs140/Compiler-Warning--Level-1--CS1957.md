---
title: "Compiler Warning (Level 1) CS1957"
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
ms.assetid: a4823211-52ce-4ffa-b19b-ee874069409f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (Level 1) CS1957
Member 'name' overrides 'method'. There are multiple override candidates at run-time. It is implementation dependent which method will be called.  
  
 Method parameters that vary only by whether they are `ref` or `out` cannot be differentiated at run-time.  
  
### To avoid this warning  
  
1.  Give one of the methods a different name or different number of parameters.  
  
## Example  
 The following code generates CS1957:  
  
```  
// cs1957.cs  
class Base<T, S>  
{  
    public virtual string Test(out T x) // CS1957  
    {  
        x = default(T);  
        return "Base.Test";  
    }  
    public virtual void Test(ref S x) { }  
}  
  
class Derived : Base<int, int>  
{  
    public override string Test(out int x)  
    {  
        x = 0;  
        return "Derived.Test";  
    }  
  
    static int Main()  
    {  
        int x;  
        if (new Derived().Test(out x) == "Derived.Test")  
            return 0;  
        return 1;  
    }  
}  
```