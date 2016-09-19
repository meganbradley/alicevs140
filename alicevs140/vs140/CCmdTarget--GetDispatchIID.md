---
title: "CCmdTarget::GetDispatchIID"
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
ms.assetid: 52a6bc3c-add1-449b-8a3f-8794d3a083a2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCmdTarget::GetDispatchIID
Gets the primary dispatch interface ID.  
  
## Syntax  
  
```  
  
      virtual BOOL GetDispatchIID(  
   IID* pIID   
);  
```  
  
#### Parameters  
 *pIID*  
 A pointer to an interface ID (a [GUID](http://msdn.microsoft.com/library/windows/desktop/aa373931)).  
  
## Return Value  
 TRUE if successful, otherwise FALSE. If successful, **pIID* is set to the primary dispatch interface ID.  
  
## Remarks  
 Derived classes should override this member function (if not overridden, `GetDispatchIID` returns FALSE). See [COleControl](../vs140/COleControl-Class.md).  
  
 For more information, see Knowledge Base article Q185720, "HOWTO: Provide Type Information From an MFC Automation Server." Knowledge Base articles are available in the MSDN Library Visual Studio documentation or at [http://support.microsoft.com](http://support.microsoft.com/).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCmdTarget Class](../vs140/CCmdTarget-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)