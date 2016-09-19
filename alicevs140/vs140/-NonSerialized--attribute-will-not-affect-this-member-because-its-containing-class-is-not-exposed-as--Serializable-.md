---
title: "&#39;NonSerialized&#39; attribute will not affect this member because its containing class is not exposed as &#39;Serializable&#39;"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1014e944-40c1-4078-8a38-139736ef89da
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;NonSerialized&#39; attribute will not affect this member because its containing class is not exposed as &#39;Serializable&#39;
By default, classes and their members are non-serializable. The <xref:System.NonSerializedAttribute?qualifyHint=False> attribute is only needed if a member of a serializable class should not be serialized.  
  
 **Error ID:** BC30772  
  
### To correct this error  
  
-   Add the <xref:System.SerializableAttribute?qualifyHint=False> attribute to the class.  
  
     —or—  
  
-   Remove the <xref:System.NonSerializedAttribute?qualifyHint=False> attribute from the member.  
  
## See Also  
 <xref:System.NonSerializedAttribute?qualifyHint=False>   
 <xref:System.SerializableAttribute?qualifyHint=False>   
 [NOT IN BUILD: Attributes in Visual Basic](assetId:///620bfc0e-4582-4c8b-8432-ebc5c3dccc22)