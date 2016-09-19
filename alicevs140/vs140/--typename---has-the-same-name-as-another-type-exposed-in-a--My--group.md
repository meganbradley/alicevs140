---
title: "&#39;&lt;typename&gt;&#39; has the same name as another type exposed in a &#39;My&#39; group"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cd2286da-49be-461f-bec9-58e9c53e250b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;&lt;typename&gt;&#39; has the same name as another type exposed in a &#39;My&#39; group
'<typename\>' has the same name as another type exposed in a 'My' group. Rename the form or its enclosing namespace.  
  
 A class or structure is declared with the same name as a class or structure in one of the `My` objects.  
  
 A name collision could not be avoided between two classes that can be accessed through a `My` object, such as `My.Forms`.  
  
 If there is a potential name collision between classes in a `My` object, the compiler changes the property name for the type from *ClassName* to *RootNamespace*_*Namespace*\_*ClassName*. For example, consider two forms named `Form1`. If one of these forms is in the root namespace `WindowsApplication1` and in the namespace `Namespace1`, you would access that form through `My.Forms.WindowsApplication1_Namespace1_Form1`.  
  
 This error can occur if two classes have the same name and are in nested namespaces with underscores in their names. When the compiler constructs the new property names for the classes, there is still a name collision.  
  
 **Error ID:** BC36015  
  
### To correct this error  
  
1.  Rename the new form.  
  
2.  Rename the namespaces.  
  
     Avoid naming any class or structure with the same name as an existing one.  
  
## See Also  
 <xref:System.Windows.Forms.Form?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.MyGroupCollectionAttribute?qualifyHint=False>   
 [NOTINBUILD: Resolving a Reference When Multiple Variables Have the Same Name](assetId:///9601e39f-1911-44e1-ace5-3f6e090408b9)   
 [My.Forms Object](../Topic/My.Forms%20Object.md)