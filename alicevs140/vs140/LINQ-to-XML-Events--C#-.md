---
title: "LINQ to XML Events (C#)"
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
ms.assetid: ce7de951-cba7-4870-9962-733eb01cd680
caps.latest.revision: 5
---
# LINQ to XML Events (C#)
[!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] events enable you to be notified when an XML tree is altered.  
  
 You can add events to an instance of any <xref:System.Xml.Linq.XObject?qualifyHint=False>. The event handler will then receive events for modifications to that <xref:System.Xml.Linq.XObject?qualifyHint=False> and any of its descendants. For example, you can add an event handler to the root of the tree, and handle all modifications to the tree from that event handler.  
  
 For examples of [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] events, see <xref:System.Xml.Linq.XObject.Changing?qualifyHint=False> and <xref:System.Xml.Linq.XObject.Changed?qualifyHint=False>.  
  
## Types and Events  
 You use the following types when working with events:  
  
|Type|Description|  
|----------|-----------------|  
|<xref:System.Xml.Linq.XObjectChange?qualifyHint=False>|Specifies the event type when an event is raised for an <xref:System.Xml.Linq.XObject?qualifyHint=False>.|  
|<xref:System.Xml.Linq.XObjectChangeEventArgs?qualifyHint=False>|Provides data for the <xref:System.Xml.Linq.XObject.Changing?qualifyHint=False> and <xref:System.Xml.Linq.XObject.Changed?qualifyHint=False> events.|  
  
 The following events are raised when you modify an XML tree:  
  
|Event|Description|  
|-----------|-----------------|  
|<xref:System.Xml.Linq.XObject.Changing?qualifyHint=False>|Occurs just before this <xref:System.Xml.Linq.XObject?qualifyHint=False> or any of its descendants is going to change.|  
|<xref:System.Xml.Linq.XObject.Changed?qualifyHint=False>|Occurs when an <xref:System.Xml.Linq.XObject?qualifyHint=False> has changed or any of its descendants have changed.|  
  
## Example  
  
### Description  
 Events are useful when you want to maintain some aggregate information in an XML tree. For example, you may want maintain an invoice total that is the sum of the line items of the invoice. This example uses events to maintain the total of all of the child elements under the complex element `Items`.  
  
### Code  
  
```c#  
XElement root = new XElement("Root",  
    new XElement("Total", "0"),  
    new XElement("Items")  
);  
XElement total = root.Element("Total");  
XElement items = root.Element("Items");  
items.Changed += (object sender, XObjectChangeEventArgs cea) =>  
{  
    switch (cea.ObjectChange)  
    {  
        case XObjectChange.Add:  
            if (sender is XElement)  
                total.Value = ((int)total + (int)(XElement)sender).ToString();  
            if (sender is XText)  
                total.Value = ((int)total + (int)((XText)sender).Parent).ToString();  
            break;  
        case XObjectChange.Remove:  
            if (sender is XElement)  
                total.Value = ((int)total - (int)(XElement)sender).ToString();  
            if (sender is XText)  
                total.Value = ((int)total - Int32.Parse(((XText)sender).Value)).ToString();  
            break;  
    }  
    Console.WriteLine("Changed {0} {1}",  
      sender.GetType().ToString(), cea.ObjectChange.ToString());  
};  
items.SetElementValue("Item1", 25);  
items.SetElementValue("Item2", 50);  
items.SetElementValue("Item2", 75);  
items.SetElementValue("Item3", 133);  
items.SetElementValue("Item1", null);  
items.SetElementValue("Item4", 100);  
Console.WriteLine("Total:{0}", (int)total);  
Console.WriteLine(root);  
```  
  
### Comments  
 This code produces the following output:  
  
```  
Changed System.Xml.Linq.XElement Add  
Changed System.Xml.Linq.XElement Add  
Changed System.Xml.Linq.XText Remove  
Changed System.Xml.Linq.XText Add  
Changed System.Xml.Linq.XElement Add  
Changed System.Xml.Linq.XElement Remove  
Changed System.Xml.Linq.XElement Add  
Total:308  
<Root>  
  <Total>308</Total>  
  <Items>  
    <Item2>75</Item2>  
    <Item3>133</Item3>  
    <Item4>100</Item4>  
  </Items>  
</Root>  
```  
  
## See Also  
 [Advanced LINQ to XML Programming (C#)](../Topic/Advanced%20LINQ%20to%20XML%20Programming%20\(C%23\).md)