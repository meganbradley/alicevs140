---
title: "ASSERT_VALID"
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
ms.assetid: 105f788e-d3ce-42c5-b125-1f121ce34427
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ASSERT_VALID
Use to test your assumptions about the validity of an object's internal state.  
  
## Syntax  
  
```  
  
ASSERT_VALID(  
pObject )  
```  
  
#### Parameters  
 `pObject`  
 Specifies an object of a class derived from `CObject` that has an overriding version of the `AssertValid` member function.  
  
## Remarks  
 `ASSERT_VALID` calls the `AssertValid` member function of the object passed as its argument.  
  
 In the Release version of MFC, `ASSERT_VALID` does nothing. In the Debug version, it validates the pointer, checks against **NULL**, and calls the object's own `AssertValid` member functions. If any of these tests fails, an alert message is displayed in the same manner as [ASSERT](../vs140/ASSERT--MFC-.md).  
  
> [!NOTE]
>  This function is available only in the Debug version of MFC.  
  
 For more information and examples, see [Debugging MFC Applications](../vs140/MFC-Debugging-Techniques.md).  
  
## Example  
 [!CODE [NVC_MFCCObjectSample#19](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#19)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [ASSERT](../vs140/ASSERT--MFC-.md)   
 [VERIFY](../vs140/VERIFY.md)   
 [CObject Class](../vs140/CObject-Class.md)   
 [CObject::AssertValid](../vs140/CObject--AssertValid.md)