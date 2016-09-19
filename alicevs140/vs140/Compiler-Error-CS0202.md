---
title: "Compiler Error CS0202"
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
ms.assetid: 7088850f-c206-4b95-9586-a0fa3d876c0c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0202
foreach requires that the return type 'type' of 'type.GetEnumerator()' must have a suitable public MoveNext method and public Current property  
  
 A <xref:System.Collections.IEnumerable.GetEnumerator?qualifyHint=False> function, used to enable the use of foreach statements, cannot return a pointer or array; it must return an instance of a class that is able to act as an enumerator. The proper requirements to serve as an enumerator include a public Current property and a public MoveNext method.  
  
> [!NOTE]
>  In C# 2.0, the compiler will automatically generate Current and MoveNext for you. For more information, see the code example in [Generic Interfaces (C# Programmers Reference)](../vs140/Generic-Interfaces--C#-Programming-Guide-.md).  
  
 The following sample generates CS0202:  
  
```  
// CS0202.cs  
  
public class C1  
{  
   public int Current  
   {  
      get  
      {  
         return 0;  
      }  
   }  
  
   public bool MoveNext ()  
   {  
      return false;  
   }  
  
   public static implicit operator C1 (int c1)  
   {  
      return 0;  
   }  
}  
  
public class C2  
{  
   public int Current  
   {  
      get  
      {  
         return 0;  
      }  
   }  
  
   public bool MoveNext ()  
   {  
      return false;  
   }  
  
   public C1[] GetEnumerator ()  
   // try the following line instead  
   // public C1 GetEnumerator ()  
   {  
      return null;  
   }  
}  
  
public class MainClass  
{  
   public static void Main ()  
   {  
      C2 c2 = new C2();  
  
      foreach (C1 x in c2)   // CS0202  
      {  
         System.Console.WriteLine(x.Current);  
      }  
   }  
}  
```