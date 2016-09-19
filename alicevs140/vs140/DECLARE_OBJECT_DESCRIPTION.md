---
title: "DECLARE_OBJECT_DESCRIPTION"
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
ms.topic: reference
ms.assetid: 32ac881c-97b1-44e2-a017-0e23eb99ac93
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_OBJECT_DESCRIPTION
Allows you to specify a text description for your class object.  
  
## Syntax  
  
```  
  
      DECLARE_OBJECT_DESCRIPTION(   
   x    
)  
```  
  
#### Parameters  
 *x*  
 [in] The class object's description.  
  
## Remarks  
 ATL enters this description into the object map through the [OBJECT_ENTRY](assetId:///abd10ee2-54f0-4f94-9ec2-ddf8f4c8c8cd) macro.  
  
 `DECLARE_OBJECT_DESCRIPTION` implements a `GetObjectDescription` function, which you can use to override the [CComCoClass::GetObjectDescription](../vs140/CComCoClass--GetObjectDescription.md) method.  
  
 The `GetObjectDescription` function is called by **IComponentRegistrar::GetComponents**. **IComponentRegistrar** is an Automation interface that allows you to register and unregister individual components in a DLL. When you create a Component Registrar object with the ATL Project Wizard, the wizard will automatically implement the **IComponentRegistrar** interface. **IComponentRegistrar** is typically used by Microsoft Transaction Server.  
  
 For more information about the ATL Project Wizard, see the article [Creating an ATL Project](../vs140/Creating-an-ATL-Project.md).  
  
## Example  
 [!CODE [NVC_ATL_Windowing#123](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#123)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Object Map Macros](../vs140/Object-Map-Macros.md)   
 [Macros](../vs140/ATL-Macros.md)