---
title: "CSacl Class"
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
ms.assetid: 8624889b-aebc-4183-9d29-a20f07837f05
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSacl Class
This class is a wrapper for a SACL (system access-control list) structure.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CSacl : public CAcl  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSacl::CSacl](../vs140/CSacl--CSacl.md)|The constructor.|  
|[CSacl::~CSacl](../vs140/CSacl--~CSacl.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSacl::AddAuditAce](../vs140/CSacl--AddAuditAce.md)|Adds an audit access-control entry (ACE) to the `CSacl` object.|  
|[CSacl::GetAceCount](../vs140/CSacl--GetAceCount.md)|Returns the number of access-control entries (ACEs) in the `CSacl` object.|  
|[CSacl::RemoveAce](../vs140/CSacl--RemoveAce.md)|Removes a specific ACE (access-control entry) from the **CSacl** object.|  
|[CSacl::RemoveAllAces](../vs140/CSacl--RemoveAllAces.md)|Removes all of the ACEs contained in the `CSacl` object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CSacl::operator =](../vs140/CSacl--operator-=.md)|Assignment operator.|  
  
## Remarks  
 A SACL contains access-control entries (ACEs) that specify the types of access attempts that generate audit records in the security event log of a domain controller. Note that a SACL generates log entries only on the domain controller where the access attempt occurred, not on every domain controller that contains a replica of the object.  
  
 To set or retrieve the SACL in an object's security descriptor, the SE_SECURITY_NAME privilege must be enabled in the access token of the requesting thread. The administrators group has this privilege granted by default, and it can be granted to other users or groups. Having the privilege granted is not all that is required: before the operation defined by the privilege can be performed, the privilege must be enabled in the security access token in order to take effect. The model allows privileges to be enabled only for specific system operations, and then disabled when they are no longer needed. See [AtlGetSacl](../vs140/AtlGetSacl.md) and [AtlSetSacl](../vs140/AtlSetSacl.md) for examples of enabling SE_SECURITY_NAME.  
  
 Use the class methods provided to add, remove, create, and delete ACEs from the **SACL** object. See also [AtlGetSacl](../vs140/AtlGetSacl.md) and [AtlSetSacl](../vs140/AtlSetSacl.md).  
  
 For an introduction to the access control model in Windows, see [Access Control](http://msdn.microsoft.com/library/windows/desktop/aa374860) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Inheritance Hierarchy  
 [CAcl](../vs140/CAcl-Class.md)  
  
 `CSacl`  
  
## Requirements  
 **Header:** atlsecurity.h  
  
##  <a name="csacl__addauditace"></a>  CSacl::AddAuditAce  
 Adds an audit access-control entry (ACE) to the `CSacl` object.  
  
```  
  
bool AddAuditAce(  
      const CSid &  rSid,  
      ACCESS_MASK  AccessMask,  
      bool  bSuccess,  
      bool  bFailure,  
      BYTE  AceFlags  
    = 0  
   ) throw(...);  
   bool AddAuditAce(  
      const CSid &  rSid,  
      ACCESS_MASK  AccessMask,  
      bool  bSuccess,  
      bool  bFailure,  
      BYTE  AceFlags,  
      const GUID *  pObjectType,  
      const GUID *  pInheritedObjectType  
   ) throw(...);  
  
```  
  
### Parameters  
 `rSid`  
 The [CSid](../vs140/CSid-Class.md) object.  
  
 `AccessMask`  
 Specifies the mask of access rights to be audited for the specified `CSid` object.  
  
 `bSuccess`  
 Specifies whether allowed access attempts are to be audited. Set this flag to true to enable auditing; otherwise, set it to false.  
  
 *bFailure*  
 Specifies whether denied access attempts are to be audited. Set this flag to true to enable auditing; otherwise, set it to false.  
  
 `AceFlags`  
 A set of bit flags that control ACE inheritance.  
  
 `pObjectType`  
 The object type.  
  
 `pInheritedObjectType`  
 The inherited object type.  
  
### Return Value  
 Returns **true** if the ACE is added to the `CSacl` object,                         **false** on failure.  
  
### Remarks  
 A `CSacl` object contains access-control entries (ACEs) that specify the types of access attempts that generate audit records in the security event log. This method adds such an ACE to the `CSacl` object. The second form of `AddAuditAce` is only available on Windows 2000 and later.  
  
 See [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) for a description of the various flags which can be set in the `AceFlags` parameter.  
  
##  <a name="csacl__csacl"></a>  CSacl::CSacl  
 The constructor.  
  
```  
  
CSacl( ) throw( );   
   CSacl(  
      const ACL &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 An existing **ACL** (access-control list) structure.  
  
### Remarks  
 The `CSacl` object can be optionally created using an existing **ACL** structure. Ensure that this parameter is a system access-control list (SACL) and not a discretionary access-control list (DACL). In debug builds, if a DACL is supplied an assertion will occur. In release builds any entries from a DACL are ignored.  
  
##  <a name="csacl___dtorcsacl"></a>  CSacl::~CSacl  
 The destructor.  
  
```  
  
~CSacl( ) throw( );  
  
```  
  
### Remarks  
 The destructor frees any resources acquired by the object, including all access-control entries (ACEs).  
  
##  <a name="csacl__getacecount"></a>  CSacl::GetAceCount  
 Returns the number of access-control entries (ACEs) in the `CSacl` object.  
  
```  
  
UINT GetAceCount( ) const throw( );  
  
```  
  
### Return Value  
 Returns the number of ACEs contained in the `CSacl` object.  
  
##  <a name="csacl__operator__eq"></a>  CSacl::operator =  
 Assignment operator.  
  
```  
  
CSacl & operator =(  
      const ACL &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The **ACL** (access-control list) to assign to the existing object.  
  
### Return Value  
 Returns a reference to the updated `CSacl` object. Ensure that the **ACL** parameter is actually a system access-control list (SACL) and not a discretionary access-control list (DACL). In debug builds an assertion will occur, and in release builds the **ACL** parameter will be ignored.  
  
##  <a name="csacl__removeace"></a>  CSacl::RemoveAce  
 Removes a specific ACE (access-control entry) from the **CSacl** object.  
  
```  
  
void RemoveAce(   
      UINT  nIndex   
   ) throw( );  
  
```  
  
### Parameters  
 `nIndex`  
 Index to the ACE entry to remove.  
  
### Remarks  
 This method is derived from [CAtlArray::RemoveAt](../vs140/CAtlArray--RemoveAt.md).  
  
##  <a name="csacl__removeallaces"></a>  CSacl::RemoveAllAces  
 Removes all of the access-control entries (ACEs) contained in the `CSacl` object.  
  
```  
  
void RemoveAllAces( ) throw( );  
  
```  
  
### Remarks  
 Removes every **ACE** structure (if any) in the `CSacl` object.  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [ACLs](http://msdn.microsoft.com/library/windows/desktop/aa374872)   
 [ACEs](http://msdn.microsoft.com/library/windows/desktop/aa374868)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Security Global Functions](../vs140/Security-Global-Functions.md)