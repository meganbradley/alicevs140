---
title: "Attribute Contexts"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 3086351f-77a8-4048-99e9-3b6b041b9437
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Attribute Contexts
C++ attributes can be described using four basic fields: the target they can be applied to (**Applies To**), if they are repeatable or not (**Repeatable**), the required presence of other attributes (**Required Attributes**), and incompatibilities with other attributes (**Invalid Attributes**). These fields are listed in an accompanying table in each attribute's reference topic. Each of these fields is described below.  
  
## Applies To  
 This field describes the different C++ language elements that are legal targets for the specified attribute. For instance, if an attribute specifies "class" in the **Applies To** field, this indicates that the attribute can only be applied to a legal C++ class. If the attribute is applied to a member function of a class, a syntax error would result.  
  
 For more information, see [Attributes by Usage](../vs140/Attributes-by-Usage.md).  
  
## Repeatable  
 This field states whether the attribute can be repeatedly applied to the same target. The majority of attributes are not repeatable.  
  
## Required Attributes  
 This field lists other attributes that need to be present (that is, applied to the same target) for the specified attribute to function properly. It is uncommon for an attribute to have any entries for this field.  
  
## Invalid Attributes  
 This field lists other attributes that are incompatible with the specified attribute. It is uncommon for an attribute to have any entries for this field.  
  
## See Also  
 [C++ Attributes Reference](../vs140/C---Attributes-Reference.md)