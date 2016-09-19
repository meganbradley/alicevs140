---
title: "ASSERT_KINDOF"
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
ms.topic: article
ms.assetid: 94b62f7c-ba07-46b7-b90b-734f31ef134f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ASSERT_KINDOF
This macro asserts that the object pointed to is an object of the specified class, or is an object of a class derived from the specified class.  
  
## Syntax  
  
```  
  
ASSERT_KINDOF(  
classname  
,   
pobject )  
```  
  
#### Parameters  
 *classname*  
 The name of a `CObject`-derived class.  
  
 *pobject*  
 A pointer to a class object.  
  
## Remarks  
 The *pobject* parameter should be a pointer to an object and can be **const**. The object pointed to and the class must support `CObject` run-time class information. As an example, to ensure that `pDocument` is a pointer to an object of the `CMyDoc` class, or any of its derivatives, you could code:  
  
 [!CODE [NVC_MFCDocView#194](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#194)]  
  
 Using the `ASSERT_KINDOF` macro is exactly the same as coding:  
  
 [!CODE [NVC_MFCDocView#195](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#195)]  
  
 This function works only for classes declared with the [DECLARE_DYNAMIC](../vs140/DECLARE_DYNAMIC.md) or [DECLARE_SERIAL](../vs140/DECLARE_SERIAL.md) macro.  
  
> [!NOTE]
>  This function is available only in the Debug version of MFC.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ASSERT](../vs140/ASSERT--MFC-.md)