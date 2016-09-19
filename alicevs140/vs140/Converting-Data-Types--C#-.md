---
title: "Converting Data Types (C#)"
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
ms.assetid: 46e5682f-77a1-4302-8f93-a2b53c408808
caps.latest.revision: 5
---
# Converting Data Types (C#)
Conversion methods change the type of input objects.  
  
 Conversion operations in LINQ queries are useful in a variety of applications. Following are some examples:  
  
-   The <xref:System.Linq.Enumerable.AsEnumerable``1?qualifyHint=True> method can be used to hide a type's custom implementation of a standard query operator.  
  
-   The <xref:System.Linq.Enumerable.OfType``1?qualifyHint=True> method can be used to enable non-parameterized collections for LINQ querying.  
  
-   The <xref:System.Linq.Enumerable.ToArray``1?qualifyHint=True>, <xref:System.Linq.Enumerable.ToDictionary``2?qualifyHint=True>, <xref:System.Linq.Enumerable.ToList``1?qualifyHint=True>, and <xref:System.Linq.Enumerable.ToLookup``2?qualifyHint=True> methods can be used to force immediate query execution instead of deferring it until the query is enumerated.  
  
## Methods  
 The following table lists the standard query operator methods that perform data-type conversions.  
  
 The conversion methods in this table whose names start with "As" change the static type of the source collection but do not enumerate it. The methods whose names start with "To" enumerate the source collection and put the items into the corresponding collection type.  
  
|Method Name|Description|C# Query Expression Syntax|More Information|  
|-----------------|-----------------|---------------------------------|----------------------|  
|AsEnumerable|Returns the input typed as <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>.|Not applicable.|<xref:System.Linq.Enumerable.AsEnumerable``1?qualifyHint=True>|  
|AsQueryable|Converts a (generic) <xref:System.Collections.IEnumerable?qualifyHint=False> to a (generic) <xref:System.Linq.IQueryable?qualifyHint=False>.|Not applicable.|<xref:System.Linq.Queryable.AsQueryable?qualifyHint=True>|  
|Cast|Casts the elements of a collection to a specified type.|Use an explicitly typed range variable. For example:<br /><br /> `from string str in words`|<xref:System.Linq.Enumerable.Cast``1?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.Cast``1?qualifyHint=True>|  
|OfType|Filters values, depending on their ability to be cast to a specified type.|Not applicable.|<xref:System.Linq.Enumerable.OfType``1?qualifyHint=True><br /><br /> <xref:System.Linq.Queryable.OfType``1?qualifyHint=True>|  
|ToArray|Converts a collection to an array. This method forces query execution.|Not applicable.|<xref:System.Linq.Enumerable.ToArray``1?qualifyHint=True>|  
|ToDictionary|Puts elements into a <xref:System.Collections.Generic.Dictionary`2?qualifyHint=False> based on a key selector function. This method forces query execution.|Not applicable.|<xref:System.Linq.Enumerable.ToDictionary``2?qualifyHint=True>|  
|ToList|Converts a collection to a <xref:System.Collections.Generic.List`1?qualifyHint=False>. This method forces query execution.|Not applicable.|<xref:System.Linq.Enumerable.ToList``1?qualifyHint=True>|  
|ToLookup|Puts elements into a <xref:System.Linq.Lookup`2?qualifyHint=False> (a one-to-many dictionary) based on a key selector function. This method forces query execution.|Not applicable.|<xref:System.Linq.Enumerable.ToLookup``2?qualifyHint=True>|  
  
## Query Expression Syntax Example  
 The following code example uses an explicitly-typed range variable  to cast a type to a subtype before accessing a member that is available only on the subtype.  
  
```c#  
class Plant  
{  
    public string Name { get; set; }  
}  
  
class CarnivorousPlant : Plant  
{  
    public string TrapType { get; set; }  
}  
  
static void Cast()  
{  
    Plant[] plants = new Plant[] {  
        new CarnivorousPlant { Name = "Venus Fly Trap", TrapType = "Snap Trap" },  
        new CarnivorousPlant { Name = "Pitcher Plant", TrapType = "Pitfall Trap" },  
        new CarnivorousPlant { Name = "Sundew", TrapType = "Flypaper Trap" },  
        new CarnivorousPlant { Name = "Waterwheel Plant", TrapType = "Snap Trap" }  
    };  
  
    var query = from CarnivorousPlant cPlant in plants  
                where cPlant.TrapType == "Snap Trap"  
                select cPlant;  
  
    foreach (Plant plant in query)  
        Console.WriteLine(plant.Name);  
  
    /* This code produces the following output:  
  
        Venus Fly Trap  
        Waterwheel Plant  
    */  
}  
```  
  
## See Also  
 <xref:System.Linq?qualifyHint=False>   
 [Standard Query Operators Overview (C#)](../Topic/Standard%20Query%20Operators%20Overview%20\(C%23\).md)   
 [from clause (C# Reference)](../Topic/from%20clause%20\(C%23%20Reference\).md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [How to: Query an ArrayList with LINQ (C#)](../vs140/How-to--Query-an-ArrayList-with-LINQ--C#-.md)