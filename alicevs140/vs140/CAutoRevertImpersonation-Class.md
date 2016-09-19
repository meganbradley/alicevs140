---
title: "CAutoRevertImpersonation Class"
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
ms.assetid: 43732849-1940-4bd4-9d52-7a5698bb8838
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoRevertImpersonation Class
This class reverts [CAccessToken](../vs140/CAccessToken-Class.md) objects to a nonimpersonating state when it goes out of scope.  
  
## Syntax  
  
```  
  
class CAutoRevertImpersonation  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAutoRevertImpersonation::CAutoRevertImpersonation](../vs140/CAutoRevertImpersonation--CAutoRevertImpersonation.md)|Constructs an `CAutoRevertImpersonation` object|  
|[CAutoRevertImpersonation::~CAutoRevertImpersonation](../vs140/CAutoRevertImpersonation--~CAutoRevertImpersonation.md)|Destroys the object and reverts access token impersonation.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CAutoRevertImpersonation::Attach](../vs140/CAutoRevertImpersonation--Attach.md)|Automates the impersonation reversion of an access token.|  
|[CAutoRevertImpersonation::Detach](../vs140/CAutoRevertImpersonation--Detach.md)|Cancels the automatic impersonation reversion.|  
|[CAutoRevertImpersonation::GetAccessToken](../vs140/CAutoRevertImpersonation--GetAccessToken.md)|Retrieves the access token current associated with this object.|  
  
## Remarks  
 An [access token](http://msdn.microsoft.com/library/windows/desktop/aa374909) is an object that describes the security context of a process or thread and is allocated to each user logged onto a Windows NT or Windows 2000 system. These access tokens can be represented with the `CAccessToken` class.  
  
 It is sometimes necessary to impersonate access tokens. This class is provided as a convenience, but it does not perform the impersonation of access tokens; it only performs the automatic reversion to a nonimpersonated state. This is because token access impersonation can be performed several different ways.  
  
 For an introduction to the access control model in Windows, see [Access Control](http://msdn.microsoft.com/library/windows/desktop/aa374860) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlsecurity.h  
  
##  <a name="cautorevertimpersonation__attach"></a>  CAutoRevertImpersonation::Attach  
 Automates the impersonation reversion of an access token.  
  
```  
  
void Attach(   
      const CAccessToken* pAT   
   ) throw( );  
  
```  
  
### Parameters  
 `pAT`  
 The address of the [CAccessToken](../vs140/CAccessToken-Class.md) object to be reverted automatically  
  
### Remarks  
 This method should only be used if the [CAutoRevertImpersonation](../vs140/CAutoRevertImpersonation-Class.md) object was created with a NULL `CAccessToken` pointer, or if [Detach](../vs140/CAutoRevertImpersonation--Detach.md) was called previously. For simple cases, it is not necessary to use this method.  
  
##  <a name="cautorevertimpersonation__cautorevertimpersonation"></a>  CAutoRevertImpersonation::CAutoRevertImpersonation  
 Constructs a `CAutoRevertImpersonation` object.  
  
```  
  
CAutoRevertImpersonation(   
      const CAccessToken* pAT   
   ) throw( );  
  
```  
  
### Parameters  
 `pAT`  
 The address of the [CAccessToken](../vs140/CAccessToken-Class.md) object to be reverted automatically.  
  
### Remarks  
 The actual impersonation of the access token should be performed separately from and preferably before the creation of a `CAutoRevertImpersonation` object. This impersonation will be reverted automatically when the `CAutoRevertImpersonation` object goes out of scope.  
  
##  <a name="cautorevertimpersonation___dtorcautorevertimpersonation"></a>  CAutoRevertImpersonation::~CAutoRevertImpersonation  
 Destroys the object and reverts access token impersonation.  
  
```  
  
~CAutoRevertImpersonation() throw( );  
  
```  
  
### Remarks  
 Reverts any impersonation currently in effect for the [CAccessToken](../vs140/CAccessToken-Class.md) object provided either at construction or through the [Attach](../vs140/CAutoRevertImpersonation--Attach.md) method. If no `CAccessToken` is associated, the destructor has no effect.  
  
##  <a name="cautorevertimpersonation__detach"></a>  CAutoRevertImpersonation::Detach  
 Cancels the automatic impersonation reversion.  
  
```  
  
const CAccessToken* Detach() throw( );  
  
```  
  
### Return Value  
 The address of the previously associated [CAccessToken](../vs140/CAccessToken-Class.md), or NULL if no association existed.  
  
### Remarks  
 Calling **Detach** prevents the `CAutoRevertImpersonation` object from reverting any impersonation currently in effect for the [CAccessToken](../vs140/CAccessToken-Class.md) object associated with this object. `CAutoRevertImpersonation` can then be destroyed with no effect or reassociated to the same or another `CAccessToken` object using [Attach](../vs140/CAutoRevertImpersonation--Attach.md).  
  
##  <a name="cautorevertimpersonation__getaccesstoken"></a>  CAutoRevertImpersonation::GetAccessToken  
 Retrieves the access token current associated with this object.  
  
```  
  
const CAccessToken* GetAccessToken() throw( );  
  
```  
  
### Return Value  
 The address of the previously associated [CAccessToken](../vs140/CAccessToken-Class.md), or NULL if no association existed.  
  
### Remarks  
 If this method is called for the purposes that include the reversion of an impersonation of the `CAccessToken` object, the [Detach](../vs140/CAutoRevertImpersonation--Detach.md) method should be used instead.  
  
## See Also  
 [ATLSecurity Sample](../vs140/Visual-C---Samples.md)   
 [Access Tokens](http://msdn.microsoft.com/library/windows/desktop/aa374909)   
 [Class Overview](../vs140/ATL-Class-Overview.md)