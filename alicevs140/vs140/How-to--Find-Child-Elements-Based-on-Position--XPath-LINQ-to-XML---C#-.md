---
title: "How to: Find Child Elements Based on Position (XPath-LINQ to XML) (C#)"
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
ms.assetid: e35bb269-ec86-4c96-8321-12491a0eb2c3
caps.latest.revision: 5
---
# How to: Find Child Elements Based on Position (XPath-LINQ to XML) (C#)
Sometimes you want to find elements based on their position. You might want to find the second element, or you might want to find the third through the fifth element.  
  
 The XPath expression is:  
  
 `Test[position() >= 2 and position() <= 4]`  
  
 There are two approaches to writing this [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] query in a lazy way. You can use the <xref:System.Linq.Enumerable.Skip``1?qualifyHint=False> and <xref:System.Linq.Enumerable.Take``1?qualifyHint=False> operators, or you can use the <xref:System.Linq.Enumerable.Where?qualifyHint=False> overload that takes an index. When you use the <xref:System.Linq.Enumerable.Where?qualifyHint=False> overload, you use a lambda expression that takes two arguments. The following example shows both methods of selecting based on position.  
  
## Example  
 This example finds the second through the fourth `Test` element. The result is a collection of elements.  
  
 This example uses the following XML document: [Sample XML File: Test Configuration (LINQ to XML)](../vs140/Sample-XML-File--Test-Configuration--LINQ-to-XML-1.md).  
  
```c#  
XElement testCfg = XElement.Load("TestConfig.xml");  
  
// LINQ to XML query  
IEnumerable<XElement> list1 =  
    testCfg  
    .Elements("Test")  
    .Skip(1)  
    .Take(3);  
  
// LINQ to XML query  
IEnumerable<XElement> list2 =  
    testCfg  
    .Elements("Test")  
    .Where((el, idx) => idx >= 1 && idx <= 3);  
  
// XPath expression  
IEnumerable<XElement> list3 =  
  testCfg.XPathSelectElements("Test[position() >= 2 and position() <= 4]");  
  
if (list1.Count() == list2.Count() &&  
    list1.Count() == list3.Count() &&  
    list1.Intersect(list2).Count() == list1.Count() &&  
    list1.Intersect(list3).Count() == list1.Count())  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
foreach (XElement el in list1)  
    Console.WriteLine(el);  
```  
  
 This example produces the following output:  
  
```  
Results are identical  
<Test TestId="0002" TestType="CMD">  
  <Name>Find succeeding characters</Name>  
  <CommandLine>Examp2.EXE</CommandLine>  
  <Input>abc</Input>  
  <Output>def</Output>  
</Test>  
<Test TestId="0003" TestType="GUI">  
  <Name>Convert multiple numbers to strings</Name>  
  <CommandLine>Examp2.EXE /Verbose</CommandLine>  
  <Input>123</Input>  
  <Output>One Two Three</Output>  
</Test>  
<Test TestId="0004" TestType="GUI">  
  <Name>Find correlated key</Name>  
  <CommandLine>Examp3.EXE</CommandLine>  
  <Input>a1</Input>  
  <Output>b1</Output>  
</Test>  
```  
  
## See Also  
 [LINQ to XML for XPath Users (C#)](../vs140/LINQ-to-XML-for-XPath-Users--C#-.md)