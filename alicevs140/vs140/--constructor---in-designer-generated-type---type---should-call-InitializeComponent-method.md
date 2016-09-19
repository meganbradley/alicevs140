---
title: "&#39;&lt;constructor&gt;&#39; in designer-generated type &#39;&lt;type&gt;&#39; should call InitializeComponent method"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: beac93b0-d427-4df6-9582-fd69c7a53673
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;constructor&gt;&#39; in designer-generated type &#39;&lt;type&gt;&#39; should call InitializeComponent method
A constructor in a designer-generated type does not call the type's `InitializeComponent` method.  
  
 Each constructor in a designer-generated type should call the type's `InitializeComponent` method.  
  
 **Error ID:** BC40054  
  
### To correct this error  
  
-   Add a call to the `InitializeComponent` method in the constructor.  
  
## See Also  
 <xref:Microsoft.VisualBasic.CompilerServices.DesignerGeneratedAttribute?qualifyHint=False>   
 [NOT IN BUILD: Using Constructors and Destructors](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)