---
title: "CWnd::OnNcCreate"
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
ms.assetid: 7ccd61e6-a1b5-48a4-8781-85d3b5f1755d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnNcCreate
The framework calls this member function prior to the [WM_CREATE](../vs140/CWnd--OnCreate.md) message when the `CWnd` object is first created.  
  
## Syntax  
  
```  
  
      afx_msg BOOL OnNcCreate(  
   LPCREATESTRUCT lpCreateStruct   
);  
```  
  
#### Parameters  
 `lpCreateStruct`  
 Points to the [CREATESTRUCT](../vs140/CREATESTRUCT-Structure.md) data structure for `CWnd`.  
  
## Return Value  
 Nonzero if the nonclient area is created. It is 0 if an error occurs; the **Create** function will return **failure** in this case.  
  
## Remarks  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::Create](../vs140/CWnd--Create.md)   
 [CWnd::CreateEx](../vs140/CWnd--CreateEx.md)   
 [CWnd::OnNcCreate](../vs140/CWnd--OnNcCreate.md)