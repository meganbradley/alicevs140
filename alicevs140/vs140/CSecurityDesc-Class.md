---
title: "CSecurityDesc Class"
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
ms.assetid: 3767a327-378f-4690-ba40-4d9f6a1f5ee4
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc Class
This class is a wrapper for the **SECURITY_DESCRIPTOR** structure.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CSecurityDesc  
  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSecurityDesc::CSecurityDesc](../vs140/CSecurityDesc--CSecurityDesc.md)|The constructor.|  
|[CSecurityDesc::~CSecurityDesc](../vs140/CSecurityDesc--~CSecurityDesc.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSecurityDesc::FromString](../vs140/CSecurityDesc--FromString.md)|Converts a string-format security descriptor into a valid, functional security descriptor.|  
|[CSecurityDesc::GetControl](../vs140/CSecurityDesc--GetControl.md)|Retrieves control information from the security descriptor.|  
|[CSecurityDesc::GetDacl](../vs140/CSecurityDesc--GetDacl.md)|Retrieves discretionary access-control list (DACL) information from the security descriptor.|  
|[CSecurityDesc::GetGroup](../vs140/CSecurityDesc--GetGroup.md)|Retrieves the primary group information from the security descriptor.|  
|[CSecurityDesc::GetOwner](../vs140/CSecurityDesc--GetOwner.md)|Retrieves owner informaton from the security descriptor.|  
|[CSecurityDesc::GetPSECURITY_DESCRIPTOR](../vs140/CSecurityDesc--GetPSECURITY_DESCRIPTOR.md)|Returns a pointer to the **SECURITY_DESCRIPTOR** structure.|  
|[CSecurityDesc::GetSacl](../vs140/CSecurityDesc--GetSacl.md)|Retrieves system access-control list (SACL) information from the security descriptor.|  
|[CSecurityDesc::IsDaclAutoInherited](../vs140/CSecurityDesc--IsDaclAutoInherited.md)|Determines if the DACL is configured to support automatic propagation.|  
|[CSecurityDesc::IsDaclDefaulted](../vs140/CSecurityDesc--IsDaclDefaulted.md)|Determines if the security descriptor is configured with a default DACL.|  
|[CSecurityDesc::IsDaclPresent](../vs140/CSecurityDesc--IsDaclPresent.md)|Determines if the security descriptor contains a DACL.|  
|[CSecurityDesc::IsDaclProtected](../vs140/CSecurityDesc--IsDaclProtected.md)|Determines if the DACL is configured to prevent modifications.|  
|[CSecurityDesc::IsGroupDefaulted](../vs140/CSecurityDesc--IsGroupDefaulted.md)|Determines if the security descriptor's group security identifier (SID) was set by default.|  
|[CSecurityDesc::IsOwnerDefaulted](../vs140/CSecurityDesc--IsOwnerDefaulted.md)|Determines if the security descriptor's owner SID was set by default.|  
|[CSecurityDesc::IsSaclAutoInherited](../vs140/CSecurityDesc--IsSaclAutoInherited.md)|Determines if the SACL is configured to support automatic propagation.|  
|[CSecurityDesc::IsSaclDefaulted](../vs140/CSecurityDesc--IsSaclDefaulted.md)|Determines if the security descriptor is configured with a default SACL.|  
|[CSecurityDesc::IsSaclPresent](../vs140/CSecurityDesc--IsSaclPresent.md)|Determines if the security descriptor contains a SACL.|  
|[CSecurityDesc::IsSaclProtected](../vs140/CSecurityDesc--IsSaclProtected.md)|Determines if the SACL is configured to prevent modifications.|  
|[CSecurityDesc::IsSelfRelative](../vs140/CSecurityDesc--IsSelfRelative.md)|Determines if the security descriptor is in self-relative format.|  
|[CSecurityDesc::MakeAbsolute](../vs140/CSecurityDesc--MakeAbsolute.md)|Call this method to convert the security descriptor to absolute format.|  
|[CSecurityDesc::MakeSelfRelative](../vs140/CSecurityDesc--MakeSelfRelative.md)|Call this method to convert the security descriptor to self-relative format.|  
|[CSecurityDesc::SetControl](../vs140/CSecurityDesc--SetControl.md)|Sets the control bits of a security descriptor.|  
|[CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md)|Sets information in a DACL. If a DACL is already present in the security descriptor, it is replaced.|  
|[CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md)|Sets the primary group information of an absolute format security descriptor, replacing any primary group information already present.|  
|[CSecurityDesc::SetOwner](../vs140/CSecurityDesc--SetOwner.md)|Sets the owner information of an absolute format security descriptor, replacing any owner information already present.|  
|[CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md)|Sets information in a SACL. If a SACL is already present in the security descriptor, it is replaced.|  
|[CSecurityDesc::ToString](../vs140/CSecurityDesc--ToString.md)|Converts a security descriptor to a string format.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[CSecurityDesc::operator const SECURITY_DESCRIPTOR *](../vs140/CSecurityDesc--operator-const-SECURITY_DESCRIPTOR--.md)|Returns a pointer to the **SECURITY_DESCRIPTOR** structure.|  
|[CSecurityDesc::operator =](../vs140/CSecurityDesc--operator-=.md)|Assignment operator.|  
  
## Remarks  
 The **SECURITY_DESCRIPTOR** structure contains the security information associated with an object. Applications use this structure to set and query an object's security status. See also [AtlGetSecurityDescriptor](../vs140/AtlGetSecurityDescriptor.md).  
  
 Applications should not modify the **SECURITY_DESCRIPTOR** structure directly, and instead should use the class methods provided.  
  
 For an introduction to the access control model in Windows, see [Access Control](http://msdn.microsoft.com/library/windows/desktop/aa374860) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlsecurity.h  
  
##  <a name="csecuritydesc__csecuritydesc"></a>  CSecurityDesc::CSecurityDesc  
 The constructor.  
  
```  
  
CSecurityDesc( ) throw( );   
   CSecurityDesc(  
      const CSecurityDesc &  rhs  
   ) throw(...);  
   CSecurityDesc(  
      const SECURITY_DESCRIPTOR &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The `CSecurityDesc` object or **SECURITY_DESCRIPTOR** structure to assign to the new `CSecurityDesc` object.  
  
### Remarks  
 The `CSecurityDesc` object can optionally be created using a **SECURITY_DESCRIPTOR** structure or a previously defined `CSecurityDesc` object.  
  
##  <a name="csecuritydesc___dtorcsecuritydesc"></a>  CSecurityDesc::~CSecurityDesc  
 The destructor.  
  
```  
  
virtual ~CSecurityDesc( ) throw( );  
  
```  
  
### Remarks  
 The destructor frees all allocated resources.  
  
##  <a name="csecuritydesc__fromstring"></a>  CSecurityDesc::FromString  
 Converts a string-format security descriptor into a valid, functional security descriptor.  
  
```  
  
bool FromString(  
      LPCTSTR  pstr  
   ) throw(...);  
  
```  
  
### Parameters  
 `pstr`  
 Pointer to a null-terminated string that contains the [string-format security descriptor](http://msdn.microsoft.com/library/windows/desktop/aa379570) to be converted.  
  
### Return Value  
 Returns true on success. Throws an exception on failure.  
  
### Remarks  
 The string can be created by using [CSecurityDesc::ToString](../vs140/CSecurityDesc--ToString.md). Converting the security descriptor into a string makes it easier to store and transmit.  
  
 This method is only available with Windows 2000 and later because it calls [ConvertStringSecurityDescriptorToSecurityDescriptor](http://msdn.microsoft.com/library/windows/desktop/aa376401).  
  
##  <a name="csecuritydesc__getcontrol"></a>  CSecurityDesc::GetControl  
 Retrieves control information from the security descriptor.  
  
```  
  
bool GetControl(  
      SECURITY_DESCRIPTOR_CONTROL *  psdc  
   ) const throw( );  
  
```  
  
### Parameters  
 *psdc*  
 Pointer to a **SECURITY_DESCRIPTOR_CONTROL** structure that receives the security descriptor's control information.  
  
### Return Value  
 Returns true if the method succeeds, false if it fails.  
  
### Remarks  
 This method is only meaningful when using Windows 2000 or later, as it calls [GetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa446647).  
  
##  <a name="csecuritydesc__getdacl"></a>  CSecurityDesc::GetDacl  
 Retrieves discretionary access-control list (DACL) information from the security descriptor.  
  
```  
  
bool GetDacl(  
      CDacl *  pDacl,  
      bool *  pbPresent  
    = NULL,  
      bool *  pbDefaulted  
    = NULL   
   ) const throw(...);  
  
```  
  
### Parameters  
 `pDacl`  
 Pointer to an `CDacl` structure in which to store a copy of the security descriptor's DACL. If a discretionary **ACL** exists, the method sets `pDacl` to the address of the security descriptor's discretionary **ACL**. If a discretionary **ACL** does not exist, no value is stored.  
  
 `pbPresent`  
 Pointer to a value that indicates the presence of a discretionary **ACL** in the specified security descriptor. If the security descriptor contains a discretionary **ACL**, this parameter is set to true. If the security descriptor does not contain a discretionary **ACL**, this parameter is set to false.  
  
 `pbDefaulted`  
 Pointer to a flag set to the value of the SE_DACL_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure if a discretionary **ACL** exists for the security descriptor. If this flag is true, the discretionary **ACL** was retrieved by a default mechanism; if false, the discretionary **ACL** was explicitly specified by a user.  
  
### Return Value  
 Returns true if the method succeeds, false if it fails.  
  
##  <a name="csecuritydesc__getgroup"></a>  CSecurityDesc::GetGroup  
 Retrieves the primary group information from the security descriptor.  
  
```  
  
bool GetGroup(  
      CSid *  pSid,  
      bool *  pbDefaulted  
    = NULL   
   ) const throw(...);  
  
```  
  
### Parameters  
 `pSid`  
 Pointer to a [CSid](../vs140/CSid-Class.md) (security identifier) that receives a copy of the group stored in the CDacl.  
  
 `pbDefaulted`  
 Pointer to a flag set to the value of the SE_GROUP_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure when the method returns.  
  
### Return Value  
 Returns true if the method succeeds, false if it fails.  
  
##  <a name="csecuritydesc__getowner"></a>  CSecurityDesc::GetOwner  
 Retrieves owner informaton from the security descriptor.  
  
```  
  
bool GetOwner(  
      CSid *  pSid,  
      bool *  pbDefaulted  
    = NULL   
   ) const throw(...);  
  
```  
  
### Parameters  
 `pSid`  
 Pointer to a [CSid](../vs140/CSid-Class.md) (security identifier) that receives a copy of the group stored in the CDacl.  
  
 `pbDefaulted`  
 Pointer to a flag set to the value of the SE_OWNER_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure when the method returns.  
  
### Return Value  
 Returns true if the method succeeds, false if it fails.  
  
##  <a name="csecuritydesc__getpsecurity_descriptor"></a>  CSecurityDesc::GetPSECURITY_DESCRIPTOR  
 Returns a pointer to the **SECURITY_DESCRIPTOR** structure.  
  
```  
  
const SECURITY_DESCRIPTOR * GetPSECURITY_DESCRIPTOR( ) const throw( );  
  
```  
  
### Return Value  
 Returns a pointer to the [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561) structure.  
  
##  <a name="csecuritydesc__getsacl"></a>  CSecurityDesc::GetSacl  
 Retrieves system access-control list (SACL) information from the security descriptor.  
  
```  
  
bool GetSacl(  
      CSacl *  pSacl,  
      bool *  pbPresent  
    = NULL,  
      bool *  pbDefaulted  
    = NULL   
   ) const throw(...);  
  
```  
  
### Parameters  
 `pSacl`  
 Pointer to an `CSacl` structure in which to store a copy of the security descriptor's SACL. If a system **ACL** exists, the method sets `pSacl` to the address of the security descriptor's system **ACL**. If a system **ACL** does not exist, no value is stored.  
  
 `pbPresent`  
 Pointer to a flag the method sets to indicate the presence of a system **ACL** in the specified security descriptor. If the security descriptor contains a system **ACL**, this parameter is set to true. If the security descriptor does not contain a system **ACL**, this parameter is set to false.  
  
 `pbDefaulted`  
 Pointer to a flag set to the value of the SE_SACL_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure if a system **ACL** exists for the security descriptor.  
  
### Return Value  
 Returns true if the method succeeds, false if it fails.  
  
##  <a name="csecuritydesc__isdaclautoinherited"></a>  CSecurityDesc::IsDaclAutoInherited  
 Determines if the discretionary access-control list (DACL) is configured to support automatic propagation.  
  
```  
  
bool IsDaclAutoInherited( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a DACL which is set up to support automatic propagation of inheritable access-control entries (ACEs) to existing child objects. Returns false otherwise.  
  
### Remarks  
 The system sets this bit when it performs the automatic inheritance algorithm for the object and its existing child objects.  
  
##  <a name="csecuritydesc__isdacldefaulted"></a>  CSecurityDesc::IsDaclDefaulted  
 Determines if the security descriptor is configured with a default discretionary access-control list (DACL).  
  
```  
  
bool IsDaclDefaulted( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a default DACL, false otherwise.  
  
### Remarks  
 This flag can affect how the system treats the DACL, with respect to access-control entry (ACE) inheritance. For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token. The system ignores this flag if the SE_DACL_PRESENT flag is not set.  
  
 This flag is used to determine how the final DACL on the object is to be computed and is not stored physically in the security descriptor control of the securable object.  
  
 To set this flag, use the [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md) method.  
  
##  <a name="csecuritydesc__isdaclpresent"></a>  CSecurityDesc::IsDaclPresent  
 Determines if the security descriptor contains a discretionary access-control list (DACL).  
  
```  
  
bool IsDaclPresent( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a DACL, false otherwise.  
  
### Remarks  
 If this flag is not set, or if this flag is set and the DACL is NULL, the security descriptor allows full access to everyone.  
  
 This flag is used to hold the security information specified by a caller until the security descriptor is associated with a securable object. Once the security descriptor is associated with a securable object, the SE_DACL_PRESENT flag is always set in the security descriptor control.  
  
 To set this flag, use the [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md) method.  
  
##  <a name="csecuritydesc__isdaclprotected"></a>  CSecurityDesc::IsDaclProtected  
 Determines if the discretionary access-control list (DACL) is configured to prevent modifications.  
  
```  
  
bool IsDaclProtected( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the DACL is configured to prevent the security descriptor from being modified by inheritable access-control entries (ACEs). Returns false otherwise.  
  
### Remarks  
 To set this flag, use the [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md) method.  
  
 This method is only meaningful for Windows 2000 or later, as only Windows 2000 supports automatic propagation of inheritable ACEs.  
  
##  <a name="csecuritydesc__isgroupdefaulted"></a>  CSecurityDesc::IsGroupDefaulted  
 Determines if the security descriptor's group security identifier (SID) was set by default.  
  
```  
  
bool IsGroupDefaulted( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if a default mechanism, rather than the original provider of the security descriptor, provided the security descriptor's group SID. Returns false otherwise.  
  
### Remarks  
 To set this flag, use the [CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md) method.  
  
##  <a name="csecuritydesc__isownerdefaulted"></a>  CSecurityDesc::IsOwnerDefaulted  
 Determines if the security descriptor's owner security identifier (SID) was set by default.  
  
```  
  
bool IsOwnerDefaulted( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if a default mechanism, rather than the original provider of the security descriptor, provided the security descriptor's owner SID. Returns false otherwise.  
  
### Remarks  
 To set this flag, use the [CSecurityDesc::SetOwner](../vs140/CSecurityDesc--SetOwner.md) method.  
  
##  <a name="csecuritydesc__issaclautoinherited"></a>  CSecurityDesc::IsSaclAutoInherited  
 Determines if the system access-control list (SACL) is configured to support automatic propagation.  
  
```  
  
bool IsSaclAutoInherited( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a SACL which is set up to support automatic propagation of inheritable access-control entries (ACEs) to existing child objects. Returns false otherwise.  
  
### Remarks  
 The system sets this bit when it performs the automatic inheritance algorithm for the object and its existing child objects.  
  
##  <a name="csecuritydesc__issacldefaulted"></a>  CSecurityDesc::IsSaclDefaulted  
 Determines if the security descriptor is configured with a default system access-control list (SACL).  
  
```  
  
bool IsSaclDefaulted( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a default SACL, false otherwise.  
  
### Remarks  
 This flag can affect how the system treats the SACL, with respect to access-control entry (ACE) inheritance. The system ignores this flag if the SE_SACL_PRESENT flag is not set.  
  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
##  <a name="csecuritydesc__issaclpresent"></a>  CSecurityDesc::IsSaclPresent  
 Determines if the security descriptor contains a system access-control list (SACL).  
  
```  
  
bool IsSaclPresent( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor contains a SACL, false otherwise.  
  
### Remarks  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
##  <a name="csecuritydesc__issaclprotected"></a>  CSecurityDesc::IsSaclProtected  
 Determines if the system access-control list (SACL) is configured to prevent modifications.  
  
```  
  
bool IsSaclProtected( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the SACL is configured to prevent the security descriptor from being modified by inheritable access-control entries (ACEs). Returns false otherwise.  
  
### Remarks  
 To set this flag, use the [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md) method.  
  
 This method is only meaningful for Windows 2000 or later, as only Windows 2000 supports automatic propagation of inheritable ACEs.  
  
##  <a name="csecuritydesc__isselfrelative"></a>  CSecurityDesc::IsSelfRelative  
 Determines if the security descriptor is in self-relative format.  
  
```  
  
bool IsSelfRelative( ) const throw( );  
  
```  
  
### Return Value  
 Returns true if the security descriptor is in self-relative format with all the security information in a contiguous block of memory. Returns false if the security descriptor is in absolute format. For more information, see [Absolute and Self-Relative Security Descriptors](http://msdn.microsoft.com/library/windows/desktop/aa374807).  
  
##  <a name="csecuritydesc__makeabsolute"></a>  CSecurityDesc::MakeAbsolute  
 Call this method to convert the security descriptor to absolute format.  
  
```  
  
bool MakeAbsolute( ) throw(...);  
  
```  
  
### Return Value  
 Returns true if the method succeeds, false otherwise.  
  
### Remarks  
 A security descriptor in absolute format contains pointers to the information it contains, rather than the information itself. A security descriptor in self-relative format contains the information in a contiguous block of memory. In a self-relative security descriptor, a **SECURITY_DESCRIPTOR** structure always starts the information, but the security descriptor's other components can follow the structure in any order. Instead of using memory addresses, the components of the self-relative security descriptor are identified by offsets from the beginning of the security descriptor. This format is useful when a security descriptor must be stored on a disk or transmitted by means of a communications protocol. For more information, see [Absolute and Self-Relative Security Descriptors](http://msdn.microsoft.com/library/windows/desktop/aa374807).  
  
##  <a name="csecuritydesc__makeselfrelative"></a>  CSecurityDesc::MakeSelfRelative  
 Call this method to convert the security descriptor to self-relative format.  
  
```  
  
bool MakeSelfRelative( ) throw(...);  
  
```  
  
### Return Value  
 Returns true if the method succeeds, false otherwise.  
  
### Remarks  
 A security descriptor in absolute format contains pointers to the information it contains, rather than containing the information itself. A security descriptor in self-relative format contains the information in a contiguous block of memory. In a self-relative security descriptor, a **SECURITY_DESCRIPTOR** structure always starts the information, but the security descriptor's other components can follow the structure in any order. Instead of using memory addresses, the components of the security descriptor are identified by offsets from the beginning of the security descriptor. This format is useful when a security descriptor must be stored on a disk or transmitted by means of a communications protocol. For more information, see [Absolute and Self-Relative Security Descriptors](http://msdn.microsoft.com/library/windows/desktop/aa374807).  
  
##  <a name="csecuritydesc__operator__eq"></a>  CSecurityDesc::operator =  
 Assignment operator.  
  
```  
  
CSecurityDesc & operator =(  
      const SECURITY_DESCRIPTOR &  rhs  
   ) throw(...);  
   CSecurityDesc & operator =(  
      const CSecurityDesc &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The **SECURITY_DESCRIPTOR** structure or `CSecurityDesc` object to assign to the `CSecurityDesc` object.  
  
### Return Value  
 Returns the updated `CSecurityDesc` object.  
  
##  <a name="csecuritydesc__operator_const_security_descriptor__star"></a>  CSecurityDesc::operator const SECURITY_DESCRIPTOR *  
 Casts a value to a pointer to the **SECURITY_DESCRIPTOR** structure.  
  
```  
  
operator const SECURITY_DESCRIPTOR *( ) const throw( );  
  
```  
  
##  <a name="csecuritydesc__setcontrol"></a>  CSecurityDesc::SetControl  
 Sets the control bits of a security descriptor.  
  
```  
bool SetControl(  
   SECURITY_DESCRIPTOR_CONTROL ControlBitsOfInterest,  
   SECURITY_DESCRIPTOR_CONTROL ControlBitsToSet   
) throw( );  
```  
  
### Parameters  
 `ControlBitsOfInterest`  
 A **SECURITY_DESCRIPTOR_CONTROL** mask that indicates the control bits to set. For a list of the flags which can be set, see [SetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa379582\(v=vs.85\).aspx).  
  
 `ControlBitsToSe`t  
 A `SECURITY_DESCRIPTOR_CONTROL` mask that indicates the new values for the control bits specified by the `ControlBitsOfInterest` mask. This parameter can be a combination of the flags listed for the `ControlBitsOfInterest` parameter.  
  
### Return Value  
 Returns true on success, false on failure.  
  
### Remarks  
 This method is available only on Windows 2000 and later, as it calls [SetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa379582\(v=vs.85\).aspx).  
  
##  <a name="csecuritydesc__setdacl"></a>  CSecurityDesc::SetDacl  
 Sets information in a discretionary access-control list (DACL). If a DACL is already present in the security descriptor, it is replaced.  
  
```  
  
inline void SetDacl(  
      bool  bPresent  
    = true,  
      bool  bDefaulted  
    = false   
   ) throw(...);  
   inline void SetDacl(  
      const CDacl &  Dacl,  
      bool  bDefaulted  
    = false   
   ) throw(...);  
  
```  
  
### Parameters  
 *Dacl*  
 Reference to a `CDacl` object specifying the DACL for the security descriptor. This parameter must not be NULL. To set a NULL DACL in the security descriptor, the first form of the method should be used with `bPresent` set to false.  
  
 `bPresent`  
 Specifies a flag indicating the presence of a DACL in the security descriptor. If this parameter is true, the method sets the SE_DACL_PRESENT flag in the **SECURITY_DESCRIPTOR_CONTROL** structure and uses the values in the *Dacl* and `bDefaulted` parameters. If it is false, the method clears the SE_DACL_PRESENT flag, and `bDefaulted` is ignored.  
  
 `bDefaulted`  
 Specifies a flag indicating the source of the DACL. If this flag is true, the DACL has been retrieved by some default mechanism. If false, the DACL has been explicitly specified by a user. The method stores this value in the SE_DACL_DEFAULTED flag of the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is not specified, the SE_DACL_DEFAULTED flag is cleared.  
  
### Return Value  
 Returns true on success, false on failure.  
  
### Remarks  
 There is an important difference between an empty and a nonexistent DACL. When a DACL is empty, it contains no access-control entries and no access rights have been explicitly granted. As a result, access to the object is implicitly denied. When an object has no DACL, on the other hand, no protection is assigned to the object, and any access request is granted.  
  
##  <a name="csecuritydesc__setgroup"></a>  CSecurityDesc::SetGroup  
 Sets the primary group information of an absolute format security descriptor, replacing any primary group information already present.  
  
```  
  
bool SetGroup(  
      const CSid &  Sid,  
      bool  bDefaulted  
    = false   
   ) throw(...);  
  
```  
  
### Parameters  
 `Sid`  
 Reference to a [CSid](../vs140/CSid-Class.md) object for the security descriptor's new primary group. This parameter must not be NULL. A security descriptor can be marked as not having a DACL or a SACL, but it must have a group and an owner, even it these are the NULL SID (which is a built-in SID with a special meaning).  
  
 `bDefaulted`  
 Indicates whether the primary group information was derived from a default mechanism. If this value is true, it is default information, and the method stores this value as the SE_GROUP_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is zero, the SE_GROUP_DEFAULTED flag is cleared.  
  
### Return Value  
 Returns true on success, false on failure.  
  
##  <a name="csecuritydesc__setowner"></a>  CSecurityDesc::SetOwner  
 Sets the owner information of an absolute format security descriptor. It replaces any owner information already present.  
  
```  
  
bool SetOwner(  
      const CSid &  Sid,  
      bool  bDefaulted  
    = false   
   ) throw(...);  
  
```  
  
### Parameters  
 `Sid`  
 The [CSid](../vs140/CSid-Class.md) object for the security descriptor's new primary owner. This parameter must not be NULL.  
  
 `bDefaulted`  
 Indicates whether the owner information is derived from a default mechanism. If this value is true, it is default information. The method stores this value as the SE_OWNER_DEFAULTED flag in the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is zero, the SE_OWNER_DEFAULTED flag is cleared.  
  
### Return Value  
 Returns true on success, false on failure.  
  
##  <a name="csecuritydesc__setsacl"></a>  CSecurityDesc::SetSacl  
 Sets information in a system access-control list (SACL). If a SACL is already present in the security descriptor, it is replaced.  
  
```  
  
bool SetSacl(  
      const CSacl &  Sacl,  
      bool  bDefaulted  
    = false   
   ) throw(...);  
  
```  
  
### Parameters  
 *Sacl*  
 Pointer to an `CSacl` object specifying the SACL for the security descriptor. This parameter must not be NULL, and must be a CSacl object. Unlike DACLs, there is no difference between NULL and an empty SACL, as SACL objects do not specify access rights, only auditing information.  
  
 `bDefaulted`  
 Specifies a flag indicating the source of the SACL. If this flag is true, the SACL has been retrieved by some default mechanism. If false, the SACL has been explicitly specified by a user. The method stores this value in the SE_SACL_DEFAULTED flag of the **SECURITY_DESCRIPTOR_CONTROL** structure. If this parameter is not specified, the SE_SACL_DEFAULTED flag is cleared.  
  
### Return Value  
 Returns true on success, false on failure.  
  
##  <a name="csecuritydesc__tostring"></a>  CSecurityDesc::ToString  
 Converts a security descriptor to a string format.  
  
```  
  
bool ToString(  
      CString *  pstr,  
      SECURITY_INFORMATION  si  
    = OWNER_SECURITY_INFORMATION |   
         GROUP_SECURITY_INFORMATION | DACL_SECURITY_INFORMATION |   
         SACL_SECURITY_INFORMATION   
   ) const throw(...);  
  
```  
  
### Parameters  
 `pstr`  
 Pointer to a null-terminated string which will receive the [string-format security descriptor](http://msdn.microsoft.com/library/windows/desktop/aa379570).  
  
 `si`  
 Specifies a combination of SECURITY_INFORMATION bit flags to indicate the components of the security descriptor to include in the output string.  
  
### Return Value  
 Returns true on success, false on failure.  
  
### Remarks  
 Once the security descriptor is in string format, it can more easily be stored or transmitted. Use the `CSecurityDesc::FromString` method to convert the string back into a security descriptor.  
  
 The `si` parameter can contain the following SECURITY_INFORMATION flags:  
  
|Value|Meaning|  
|-----------|-------------|  
|OWNER_SECURITY_INFORMATION|Include the owner.|  
|GROUP_SECURITY_INFORMATION|Include the primary group.|  
|DACL_SECURITY_INFORMATION|Include the DACL.|  
|SACL_SECURITY_INFORMATION|Include the SACL.|  
  
 If the DACL is NULL and the SE_DACL_PRESENT control bit is set in the input security descriptor, the method fails.  
  
 If the DACL is NULL and the SE_DACL_PRESENT control bit is not set in the input security descriptor, the resulting security descriptor string does not have a D: component. See [Security Descriptor String Format](http://msdn.microsoft.com/library/windows/desktop/aa379570) for more details.  
  
 This method is only available with Windows 2000 and later, as it calls [ConvertStringSecurityDescriptorToSecurityDescriptor](http://msdn.microsoft.com/library/windows/desktop/aa376401).  
  
## See Also  
 [Security Sample](../vs140/Visual-C---Samples.md)   
 [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Security Global Functions](../vs140/Security-Global-Functions.md)