---
title: "How to: Query an ArrayList with LINQ (C#)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2bfb471c-6e9a-4e60-bd83-4a1778abde11
caps.latest.revision: 5
---
# How to: Query an ArrayList with LINQ (C#)
When using LINQ to query non-generic <xref:System.Collections.IEnumerable?qualifyHint=False> collections such as <xref:System.Collections.ArrayList?qualifyHint=False>, you must explicitly declare the type of the range variable to reflect the specific type of the objects in the collection. For example, if you have an <xref:System.Collections.ArrayList?qualifyHint=False> of `Student` objects, your [from clause](../Topic/from%20clause%20\(C%23%20Reference\).md)should look like this:  
  
```  
  
var query = from Student s in arrList  
...  
  
```  
  
 By specifying the type of the range variable, you are casting each item in the <xref:System.Collections.ArrayList?qualifyHint=False> to a `Student`.  
  
 The use of an explicitly typed range variable in a query expression is equivalent to calling the <xref:System.Linq.Enumerable.Cast``1?qualifyHint=False> method. <xref:System.Linq.Enumerable.Cast``1?qualifyHint=False> throws an exception if the specified cast cannot be performed. <xref:System.Linq.Enumerable.Cast``1?qualifyHint=False> and <xref:System.Linq.Enumerable.OfType``1?qualifyHint=False> are the two Standard Query Operator methods that operate on non-generic <xref:System.Collections.IEnumerable?qualifyHint=False> types. For more information, see[Type Relationships in LINQ Query Operations (C#)](../vs140/Type-Relationships-in-LINQ-Query-Operations--C#-.md).  
  
## Example  
 The following example shows a simple query over an <xref:System.Collections.ArrayList?qualifyHint=False>. Note that this example uses object initializers when the code calls the <xref:System.Collections.ArrayList.Add?qualifyHint=False> method, but this is not a requirement.  
  
```c#  
using System;  
using System.Collections;  
using System.Linq;  
  
namespace NonGenericLINQ  
{  
    public class Student  
    {  
        public string FirstName { get; set; }  
        public string LastName { get; set; }  
        public int[] Scores { get; set; }  
    }  
  
    class Program  
    {  
        static void Main(string[] args)  
        {  
            ArrayList arrList = new ArrayList();  
            arrList.Add(  
                new Student  
                    {  
                        FirstName = "Svetlana", LastName = "Omelchenko", Scores = new int[] { 98, 92, 81, 60 }  
                    });  
            arrList.Add(  
                new Student  
                    {  
                        FirstName = "Claire", LastName = "O’Donnell", Scores = new int[] { 75, 84, 91, 39 }  
                    });  
            arrList.Add(  
                new Student  
                    {  
                        FirstName = "Sven", LastName = "Mortensen", Scores = new int[] { 88, 94, 65, 91 }  
                    });  
            arrList.Add(  
                new Student  
                    {  
                        FirstName = "Cesar", LastName = "Garcia", Scores = new int[] { 97, 89, 85, 82 }  
                    });  
  
            var query = from Student student in arrList  
                        where student.Scores[0] > 95  
                        select student;  
  
            foreach (Student s in query)  
                Console.WriteLine(s.LastName + ": " + s.Scores[0]);  
  
            // Keep the console window open in debug mode.  
            Console.WriteLine("Press any key to exit.");  
            Console.ReadKey();  
        }  
    }  
}  
/* Output:   
    Omelchenko: 98  
    Garcia: 97  
*/  
```  
  
## See Also  
 [LINQ to Objects (C#)](../Topic/LINQ%20to%20Objects%20\(C%23\).md)