---
title: "Modifying XML Trees (LINQ to XML) (C#)"
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
ms.assetid: 8ec47e6d-2363-4694-be46-8d5ca4d15fc9
caps.latest.revision: 5
---
# Modifying XML Trees (LINQ to XML) (C#)
[!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] is an in-memory store for an XML tree. After you load or parse an XML tree from a source, [!INCLUDE[sqltecxlinq](../vs140/includes/sqltecxlinq_md.md)] lets you modify that tree in place, and then serialize the tree, perhaps saving it to a file or sending it to a remote server.  
  
 When you modify a tree in place, you use certain methods, such as <xref:System.Xml.Linq.XContainer.Add?qualifyHint=False>.  
  
 However, there is another approach, which is to use functional construction to generate a new tree with a different shape. Depending on the types of changes that you need to make to your XML tree, and depending on the size of the tree, this approach can be more robust and easier to develop. The first topic in this section compares these two approaches.  
  
## In This Section  
  
|Topic|Description|  
|-----------|-----------------|  
|[In-Memory XML Tree Modification vs. Functional Construction (LINQ to XML) (C#)](../Topic/In-Memory%20XML%20Tree%20Modification%20vs.%20Functional%20Construction%20\(LINQ%20to%20XML\)%20\(C%23\).md)|Compares modifying an XML tree in memory to functional construction.|  
|[Adding Elements, Attributes, and Nodes to an XML Tree (C#)](../Topic/Adding%20Elements,%20Attributes,%20and%20Nodes%20to%20an%20XML%20Tree%20\(C%23\).md)|Provides information about adding elements, attributes, or nodes to an XML tree.|  
|[Modifying Elements, Attributes, and Nodes in an XML Tree](../Topic/Modifying%20Elements,%20Attributes,%20and%20Nodes%20in%20an%20XML%20Tree3.md)|Provides information about modifying existing elements, attributes, or nodes.|  
|[Removing Elements, Attributes, and Nodes from an XML Tree (C#)](../vs140/Removing-Elements--Attributes--and-Nodes-from-an-XML-Tree--C#-.md)|Provides information about removing elements, attributes, or nodes from the XML tree.|  
|[Maintaining Name/Value Pairs (C#)](../vs140/Maintaining-Name-Value-Pairs--C#-.md)|Describes how to maintain application information that is best kept as name/value pairs, such as configuration information or global settings.|  
|[How to: Change the Namespace for an Entire XML Tree (C#)](../Topic/How%20to:%20Change%20the%20Namespace%20for%20an%20Entire%20XML%20Tree%20\(C%23\).md)|Shows how to move an XML tree from one namespace into another.|  
  
## See Also  
 [Programming Guide (LINQ to XML) (C#)](../Topic/Programming%20Guide%20\(LINQ%20to%20XML\)%20\(C%23\).md)