---
title: "CObject::GetRuntimeClass"
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
ms.assetid: fee38b64-bde1-4086-9fa6-bc72940748ab
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CObject::GetRuntimeClass
Returns the `CRuntimeClass` structure corresponding to this object's class.  
  
## Syntax  
  
```  
  
virtual CRuntimeClass* GetRuntimeClass( ) const;  
```  
  
## Return Value  
 A pointer to the [CRuntimeClass](../vs140/CRuntimeClass-Structure.md) structure corresponding to this object's class; never **NULL**.  
  
## Remarks  
 There is one `CRuntimeClass` structure for each `CObject`-derived class. The structure members are as follows:  
  
-   **LPCSTR m_lpszClassName** A null-terminated string containing the ASCII class name.  
  
-   **int m_nObjectSize** The size of the object, in bytes. If the object has data members that point to allocated memory, the size of that memory is not included.  
  
-   **UINT m_wSchema** The schema number ( – 1 for nonserializable classes). See the [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro for a description of schema number.  
  
-   **CObject\* ( PASCAL\* m_pfnCreateObject )( )** A function pointer to the default constructor that creates an object of your class (valid only if the class supports dynamic creation; otherwise, returns **NULL**).  
  
-   **CRuntimeClass\* ( PASCAL\* m_pfn_GetBaseClass )( )** If your application is dynamically linked to the AFXDLL version of MFC, a pointer to a function that returns the `CRuntimeClass` structure of the base class.  
  
-   **CRuntimeClass\* m_pBaseClass** If your application is statically linked to MFC, a pointer to the `CRuntimeClass` structure of the base class.  
  
 This function requires use of the [IMPLEMENT_DYNAMIC](../vs140/IMPLEMENT_DYNAMIC.md), [IMPLEMENT_DYNCREATE](../vs140/IMPLEMENT_DYNCREATE.md), or [IMPLEMENT_SERIAL](../vs140/IMPLEMENT_SERIAL.md) macro in the class implementation. You will get incorrect results otherwise.  
  
## Example  
 See [CObList::CObList](../vs140/CObList--CObList.md) for a listing of the `CAge` class used in all `CObject` examples.  
  
 [!CODE [NVC_MFCCObjectSample#10](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#10)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CObject Class](../vs140/CObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CObject::IsKindOf](../vs140/CObject--IsKindOf.md)   
 [RUNTIME_CLASS](../vs140/RUNTIME_CLASS.md)