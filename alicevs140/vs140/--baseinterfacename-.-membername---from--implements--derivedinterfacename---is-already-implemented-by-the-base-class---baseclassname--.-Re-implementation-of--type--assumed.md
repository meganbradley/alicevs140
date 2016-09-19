---
title: "&#39;&lt;baseinterfacename&gt;.&lt;membername&gt;&#39; from &#39;implements &lt;derivedinterfacename&gt;&#39; is already implemented by the base class &#39;&lt;baseclassname&gt;&#39;. Re-implementation of &lt;type&gt; assumed"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 95fff622-5d54-4ec8-90f0-477de1d58687
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;baseinterfacename&gt;.&lt;membername&gt;&#39; from &#39;implements &lt;derivedinterfacename&gt;&#39; is already implemented by the base class &#39;&lt;baseclassname&gt;&#39;. Re-implementation of &lt;type&gt; assumed
A property, procedure, or event in a derived class uses an `Implements` clause specifying a derived interface member that is already implemented on the base interface in the base class.  
  
 The member being implemented is defined by the base interface and inherited by the derived interface. The base class directly implements the base interface. The derived class implements the derived interface and can easily miss the fact that the base class has already implemented the member.  
  
 A derived class can reimplement an interface member that is implemented by its base class. This is not the same as overriding the base class implementation. For more information, see [Implements (Visual Basic)](../vs140/Implements-Clause--Visual-Basic-.md).  
  
 By default, this message is a warning. For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42014  
  
### To correct this error  
  
-   If you intend to reimplement the interface member, you do not need to take any action. Code in your derived class accesses the reimplemented member unless you use the [MyBase - delete](assetId:///52491d06-6451-4f6f-9aa6-8fab59bbc2b9) keyword to access the base class implementation.  
  
-   If you do not intend to reimplement the interface member, remove the `Implements` clause from the property, procedure, or event declaration.  
  
## See Also  
 [Interfaces in Visual Basic](../vs140/Interfaces--Visual-Basic-.md)   
 [NOT IN BUILD: Implements Keyword and Implements Statement](assetId:///b96560f7-6413-480f-a1e2-f80253bab5be)