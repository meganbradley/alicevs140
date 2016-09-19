---
title: "IDebugProperty3::CreateObjectID"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f2fa81e7-822f-456e-8729-a96a18eea771
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProperty3::CreateObjectID
Creates a unique ID for this property to ensure that it is unique among all other properties.  
  
## Syntax  
  
```cpp  
HRESULT CreateObjectID(  
   void  
);  
```  
  
```c#  
int CreateObjectID();  
```  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 This method is called when the session debug manager wants to make sure that this property is uniquely identified among all other properties. The debug engine (DE) supports this method unless the properties it deals with are already uniquely identified. If the DE does not support this method, it returns `E_NOTIMPL`.  
  
 Any unique ID created with `CreateObjectID` is destroyed when the [IDebugProperty3::DestroyObjectID](../vs140/IDebugProperty3--DestroyObjectID.md) method is called; this also signals the end of the need for uniquely identifying this property.  
  
> [!NOTE]
>  There is no method to retrieve this unique ID, so the DE can do whatever it wants for unique IDs when the `CreateObjectID` method is called.  
  
## See Also  
 [IDebugProperty3](../vs140/IDebugProperty3.md)   
 [IDebugProperty3::DestroyObjectID](../vs140/IDebugProperty3--DestroyObjectID.md)