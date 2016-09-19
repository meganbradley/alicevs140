---
title: "How to: Project a New Type (LINQ to XML) (C#)"
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
ms.assetid: 48145cf9-1e0b-4e73-bbfd-28fc04800dc4
caps.latest.revision: 3
---
# How to: Project a New Type (LINQ to XML) (C#)
Other examples in this section have shown queries that return results as <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of <xref:System.Xml.Linq.XElement?qualifyHint=False>, <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of `string`, and <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of `int`. These are common result types, but they are not appropriate for every scenario. In many cases you will want your queries to return an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> of some other type.  
  
## Example  
 This example shows how to instantiate objects in the `select` clause. The code first defines a new class with a constructor, and then modifies the `select` statement so that the expression is a new instance of the new class.  
  
 This example uses the following XML document: [Sample XML File: Typical Purchase Order (LINQ to XML)](../vs140/Sample-XML-File--Typical-Purchase-Order--LINQ-to-XML-1.md).  
  
```c#  
class NameQty {  
    public string name;  
    public int qty;  
    public NameQty(string n, int q)  
    {  
        name = n;  
        qty = q;  
    }  
};  
  
class Program {  
    public static void Main() {  
        XElement po = XElement.Load("PurchaseOrder.xml");  
  
        IEnumerable<NameQty> nqList =  
            from n in po.Descendants("Item")  
            select new NameQty(  
                    (string)n.Element("ProductName"),  
                    (int)n.Element("Quantity")  
                );  
  
        foreach (NameQty n in nqList)  
            Console.WriteLine(n.name + ":" + n.qty);  
    }  
}  
```  
  
 This example uses the `M:System.Xml.Linq.XElement.Element` method that was introduced in the topic [How to: Retrieve a Single Child Element (LINQ to XML) (C#)](../vs140/How-to--Retrieve-a-Single-Child-Element--LINQ-to-XML---C#-.md). It also uses casts to retrieve the values of the elements that are returned by the `M:System.Xml.Linq.XElement.Element` method.  
  
 This example produces the following output:  
  
```  
Lawnmower:1  
Baby Monitor:2  
```  
  
## See Also  
 [Projections and Transformations (LINQ to XML) (C#)](../vs140/Projections-and-Transformations--LINQ-to-XML---C#-.md)