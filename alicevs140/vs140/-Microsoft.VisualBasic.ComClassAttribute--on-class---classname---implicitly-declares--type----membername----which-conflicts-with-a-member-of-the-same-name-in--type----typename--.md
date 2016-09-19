---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; on class &#39;&lt;classname&gt;&#39; implicitly declares &lt;type&gt; &#39;&lt;membername&gt;&#39;, which conflicts with a member of the same name in &lt;type&gt; &#39;&lt;typename&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 001c8eaa-19b6-44fa-8056-4186ecffbda8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; on class &#39;&lt;classname&gt;&#39; implicitly declares &lt;type&gt; &#39;&lt;membername&gt;&#39;, which conflicts with a member of the same name in &lt;type&gt; &#39;&lt;typename&gt;&#39;
'Microsoft.VisualBasic.ComClassAttribute' on class '<classname\>' implicitly declares <type\> '<membername\>', which conflicts with a member of the same name in <type\> '<typename\>'. Use 'Microsoft.VisualBasic.ComClassAttribute(InterfaceShadows:=True)' if you want to hide the name on the base '<typename\>'.  
  
 A class using a `COMClassAttribute` attribute block implicitly defines an interface with the same name as a member of the base class. In this situation, the interface name should shadow the base class member.  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42101  
  
### To correct this error  
  
1.  If you intend to hide the base class member, set `InterfaceShadows:=True` in the `ComClassAttribute` attribute block.  
  
2.  If you do not intend to hide the base class member, change the name of the class.  
  
## See Also  
 [NOT IN BUILD: Attributes Used in Visual Basic](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NOT IN BUILD: Application of Attributes](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute Class](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)   
 [ComClassAttribute.InterfaceShadows Property](assetId:///0fae25bd-e0ba-4755-a76c-3b526b1ac795)