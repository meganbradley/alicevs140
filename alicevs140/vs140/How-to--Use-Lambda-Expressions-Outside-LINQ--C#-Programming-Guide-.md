---
title: "How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)"
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
ms.assetid: 2b519274-6ee4-4455-ab2e-aed67dbfd07c
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use Lambda Expressions Outside LINQ (C# Programming Guide)
Lambda expressions are not limited to [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] queries. You can use them anywhere a delegate value is expected, that is, wherever an anonymous method can be used. The following example shows how to use a lambda expression in a Windows Forms event handler. Notice that the types of the inputs (<xref:System.Object?qualifyHint=False> and <xref:System.Windows.Forms.MouseEventArgs?qualifyHint=False>) are inferred by the compiler and do not have to be explicitly given in the lambda input parameters.  
  
## Example  
  
```  
public partial class Form1 : Form  
{  
    public Form1()  
    {  
        InitializeComponent();  
        // Use a lambda expression to define an event handler.  
       this.Click += (s, e) => { MessageBox.Show(((MouseEventArgs)e).Location.ToString());};  
    }  
}  
```  
  
## See Also  
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Anonymous Methods (C# Programming Guide)](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)   
 [Language-Integrated Query (LINQ)](../vs140/LINQ--Language-Integrated-Query-.md)