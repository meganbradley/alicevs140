---
title: "CSid Class"
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
ms.assetid: be58b7ca-5958-49c3-a833-ca341aaaf753
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSid Class
This class is a wrapper for a `SID` (security identifier) structure.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
  
class CSid  
  
```  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|[CSid::CSidArray](../vs140/CSid--CSidArray.md)|An array of `CSid` objects.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CSid::CSid](../vs140/CSid--CSid.md)|The constructor.|  
|[CSid::~CSid](../vs140/CSid--~CSid.md)|The destructor.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CSid::AccountName](../vs140/CSid--AccountName.md)|Returns the name of the account associated with the `CSid` object.|  
|[CSid::Domain](../vs140/CSid--Domain.md)|Returns the name of the domain associated with the `CSid` object.|  
|[CSid::EqualPrefix](../vs140/CSid--EqualPrefix.md)|Tests `SID` (security identifier) prefixes for equality.|  
|[CSid::GetLength](../vs140/CSid--GetLength.md)|Returns the length of the `CSid` object.|  
|[CSid::GetPSID](../vs140/CSid--GetPSID.md)|Returns a pointer to a `SID` structure.|  
|[CSid::GetPSID_IDENTIFIER_AUTHORITY](../vs140/CSid--GetPSID_IDENTIFIER_AUTHORITY.md)|Returns a pointer to the **SID_IDENTIFIER_AUTHORITY** structure.|  
|[CSid::GetSubAuthority](../vs140/CSid--GetSubAuthority.md)|Returns a specified subauthority in a **SID** structure.|  
|[CSid::GetSubAuthorityCount](../vs140/CSid--GetSubAuthorityCount.md)|Returns the subauthority count.|  
|[CSid::IsValid](../vs140/CSid--IsValid.md)|Tests the `CSid` object for validity.|  
|[CSid::LoadAccount](../vs140/CSid--LoadAccount.md)|Updates the `CSid` object given the account name and domain, or an existing `SID` structure.|  
|[CSid::Sid](../vs140/CSid--Sid.md)|Returns the ID string.|  
|[CSid::SidNameUse](../vs140/CSid--SidNameUse.md)|Returns a description of the state of the `CSid` object.|  
  
### Operators  
  
|||  
|-|-|  
|[operator =](../vs140/CSid--operator-=.md)|Assignment operator.|  
|[operator const SID *](../vs140/CSid--operator-const-SID--.md)|Casts a `CSid` object to a pointer to a `SID` structure.|  
  
### Global Operators  
  
|||  
|-|-|  
|[operator ==](../vs140/CSid--operator-==.md)|Tests two security descriptor objects for equality|  
|[operator !=](../vs140/CSid--operator-!=.md)|Tests two security descriptor objects for inequality|  
|[operator <](../vs140/CSid--operator--.md)|Compares relative value of two security descriptor objects.|  
|[operator >](../vs140/CSid--operator--.md)|Compares relative value of two security descriptor objects.|  
|[operator <=](../vs140/CSid--operator--=.md)|Compares relative value of two security descriptor objects.|  
|[operator >=](../vs140/CSid--operator--=.md)|Compares relative value of two security descriptor objects.|  
  
## Remarks  
 The `SID` structure is a variable-length structure used to uniquely identify users or groups.  
  
 Applications should not modify the `SID` structure directly, but instead use the methods provided in this wrapper class. See also [AtlGetOwnerSid](../vs140/AtlGetOwnerSid.md), [AtlSetGroupSid](../vs140/AtlSetGroupSid.md), [AtlGetGroupSid](../vs140/AtlGetGroupSid.md), and [AtlSetOwnerSid](../vs140/AtlSetOwnerSid.md).  
  
 For an introduction to the access control model in Windows, see [Access Control](http://msdn.microsoft.com/library/windows/desktop/aa374860) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlsecurity.h  
  
##  <a name="csid__accountname"></a>  CSid::AccountName  
 Returns the name of the account associated with the `CSid` object.  
  
```  
  
LPCTSTR AccountName( ) const throw(...);  
  
```  
  
### Return Value  
 Returns the `LPCTSTR` pointing to the name of the account.  
  
### Remarks  
 This method attempts to find a name for the specified `SID` (security identifier). For full details, see [LookupAccountSid](http://msdn.microsoft.com/library/windows/desktop/aa379166).  
  
 If no account name for the `SID` can be found, `AccountName` returns an empty string. This can occur if a network timeout prevents this method from finding the name. It also occurs for security identifiers with no corresponding account name, such as a logon `SID` that identifies a logon session.  
  
##  <a name="csid__csid"></a>  CSid::CSid  
 The constructor.  
  
```  
  
CSid( ) throw( );   
   CSid(  
      const SID &  rhs  
   ) throw(...);  
   CSid(  
      const CSid &  rhs  
   ) throw(...);  
   CSid(  
      const SID_IDENTIFIER_AUTHORITY &  IdentifierAuthority,  
      BYTE  nSubAuthorityCount,  
      ...   
   ) throw(...);  
   explicit CSid(  
      LPCTSTR  pszAccountName,  
      LPCTSTR  pszSystem  
    = NULL   
   ) throw(...);  
   explicit CSid(  
      const SID *  pSid,  
      LPCTSTR  pszSystem  
    = NULL   
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 An existing `CSid` object or `SID` (security identifier) structure.  
  
 *IdentifierAuthority*  
 The authority.  
  
 *nSubAuthorityCount*  
 The subauthority count.  
  
 `pszAccountName`  
 The account name.  
  
 `pszSystem`  
 The system name. This string can be the name of a remote computer. If this string is NULL, the local system is used instead.  
  
 `pSid`  
 A pointer to a `SID` structure.  
  
### Remarks  
 The constructor initializes the `CSid` object, setting an internal data member to *SidTypeInvalid*, or by copying the settings from an existing `CSid`, `SID`, or existing account.  
  
 If initialization fails, the constructor will throw a [CAtlException Class](../vs140/CAtlException-Class.md).  
  
##  <a name="csid___dtorcsid"></a>  CSid::~CSid  
 The destructor.  
  
```  
  
virtual ~CSid( ) throw( );  
  
```  
  
### Remarks  
 The destructor frees any resources acquired by the object.  
  
##  <a name="csid__csidarray"></a>  CSid::CSidArray  
 An array of [CSid](../vs140/CSid-Class.md) objects.  
  
```  
  
typedef CAtlArray<CSid> CSidArray;  
  
```  
  
### Remarks  
 This typedef specifies the array type that can be used to retrieve security identifiers from an ACL (access-control list). See [CAcl::GetAclEntries](../vs140/CAcl--GetAclEntries.md).  
  
##  <a name="csid__domain"></a>  CSid::Domain  
 Returns the name of the domain associated with the `CSid` object.  
  
```  
  
LPCTSTR Domain( ) const throw(...);  
  
```  
  
### Return Value  
 Returns the `LPCTSTR` pointing to the domain.  
  
### Remarks  
 This method attempts to find a name for the specified `SID` (security identifier). For full details, see [LookupAccountSid](http://msdn.microsoft.com/library/windows/desktop/aa379166).  
  
 If no account name for the `SID` can be found,                         **Domain** returns the domain as an empty string. This can occur if a network timeout prevents this method from finding the name. It also occurs for security identifiers with no corresponding account name, such as a logon `SID` that identifies a logon session.  
  
##  <a name="csid__equalprefix"></a>  CSid::EqualPrefix  
 Tests `SID` (security identifier) prefixes for equality.  
  
```  
  
bool EqualPrefix(  
      const SID &  rhs  
   ) const throw();  
   bool EqualPrefix(  
      const CSid &  rhs  
   ) const throw();  
  
```  
  
### Parameters  
 `rhs`  
 The `SID` (security identifier) structure or `CSid` object to compare.  
  
### Return Value  
 Returns **true** on success,                         **false** on failure.  
  
### Remarks  
 See [EqualPrefixSid](http://msdn.microsoft.com/library/windows/desktop/aa446621) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more details.  
  
##  <a name="csid__getlength"></a>  CSid::GetLength  
 Returns the length of the `CSid` object.  
  
```  
  
UINT GetLength( ) const throw( );  
  
```  
  
### Return Value  
 Returns the length in bytes of the `CSid` object.  
  
### Remarks  
 If the `CSid` structure is not valid, the return value is undefined. Before calling `GetLength`, use the [CSid::IsValid](../vs140/CSid--IsValid.md) member function to verify that `CSid` is valid.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
##  <a name="csid__getpsid"></a>  CSid::GetPSID  
 Returns a pointer to a `SID` (security identifier) structure.  
  
```  
  
const SID * GetPSID( ) const throw(...);  
  
```  
  
### Return Value  
 Returns the address of the `CSid` object's underlying `SID` structure.  
  
##  <a name="csid__getpsid_identifier_authority"></a>  CSid::GetPSID_IDENTIFIER_AUTHORITY  
 Returns a pointer to the **SID_IDENTIFIER_AUTHORITY** structure.  
  
```  
  
const SID_IDENTIFIER_AUTHORITY * GetPSID_IDENTIFIER_AUTHORITY( ) const throw();  
  
```  
  
### Return Value  
 If the method succeeds, it returns the address of the **SID_IDENTIFIER_AUTHORITY** structure. If it fails, the return value is undefined. Failure may occur if the `CSid` object is not valid, in which case the [CSid::IsValid](../vs140/CSid--IsValid.md) method returns **false**. The function `GetLastError` can be called for extended error information.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
##  <a name="csid__getsubauthority"></a>  CSid::GetSubAuthority  
 Returns a specified subauthority in a `SID` (security identifier) structure.  
  
```  
  
DWORD GetSubAuthority(  
      DWORD  nSubAuthority  
   ) const throw( );  
  
```  
  
### Parameters  
 *nSubAuthority*  
 The subauthority.  
  
### Return Value  
 Returns the subauthority referenced by *nSubAuthority.* The subauthority value is a relative identifier (RID).  
  
### Remarks  
 The *nSubAuthority* parameter specifies an index value identifying the subauthority array element the method will return. The method performs no validation tests on this value. An application can call [CSid::GetSubAuthorityCount](../vs140/CSid--GetSubAuthorityCount.md) to discover the range of acceptable values.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
##  <a name="csid__getsubauthoritycount"></a>  CSid::GetSubAuthorityCount  
 Returns the subauthority count.  
  
```  
  
UCHAR GetSubAuthorityCount( ) const throw( );  
  
```  
  
### Return Value  
 If the method succeeds, the return value is the subauthority count.  
  
 If the method fails, the return value is undefined. The method fails if the `CSid` object is invalid. To get extended error information, call `GetLastError`.  
  
> [!NOTE]
>  Under debug builds the function will cause an ASSERT if the `CSid` object is not valid.  
  
##  <a name="csid__isvalid"></a>  CSid::IsValid  
 Tests the `CSid` object for validity.  
  
```  
  
bool IsValid( ) const throw();  
  
```  
  
### Return Value  
 Returns **true** if the `CSid` object is valid,                         **false** if not. There is no extended error information for this method; do not call `GetLastError`.  
  
### Remarks  
 The `IsValid` method validates the `CSid` object by verifying that the revision number is within a known range and that the number of subauthorities is less than the maximum.  
  
##  <a name="csid__loadaccount"></a>  CSid::LoadAccount  
 Updates the `CSid` object given the account name and domain, or an existing SID (security identifier) structure.  
  
```  
bool LoadAccount(  
   LPCTSTR pszAccountName,  
   LPCTSTR pszSystem = NULL   
) throw(...);  
bool LoadAccount(  
   const SID * pSid,  
   LPCTSTR pszSystem = NULL   
) throw(...);  
```  
  
### Parameters  
 `pszAccountName`  
 The account name.  
  
 `pszSystem`  
 The system name. This string can be the name of a remote computer. If this string is NULL, the local system is used instead.  
  
 `pSid`  
 A pointer to a [SID](http://msdn.microsoft.com/library/windows/desktop/aa379594\(v=vs.85\).aspx) structure.  
  
### Return Value  
 Returns **true** on success,                         **false** on failure. To get extended error information, call `GetLastError`.  
  
### Remarks  
 `LoadAccount` attempts to find a security identifier for the specified name. See [LookupAccountSid](http://msdn.microsoft.com/library/windows/desktop/aa379166\(v=vs.85\).aspx) for more details.  
  
##  <a name="csid__operator__eq"></a>  CSid::operator =  
 Assignment operator.  
  
```  
  
CSid & operator =(  
      const CSid &  rhs  
   ) throw(...);  
   CSid & operator =(  
      const SID &  rhs  
   ) throw(...);  
  
```  
  
### Parameters  
 `rhs`  
 The `SID` (security identifier) or `CSid` to assign to the `CSid` object.  
  
### Return Value  
 Returns a reference to the updated `CSid` object.  
  
##  <a name="csid__operator__eq_eq"></a>  CSid::operator ==  
 Tests two security descriptor objects for equality.  
  
```  
  
bool operator==(   
      const CSid & lhs,   
      const CSid & rhs   
   ) throw(   );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the == operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the == operator.  
  
### Return Value  
 **true** if the security descriptors are equal, otherwise **false**.  
  
##  <a name="csid__operator__neq"></a>  CSid::operator !=  
 Tests two security descriptor objects for inequality.  
  
```  
  
bool operator!=(   
      const CSid & lhs,   
      const CSid & rhs   
   ) throw(   );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the != operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the != operator.  
  
### Return Value  
 **true** if the security descriptors are not equal, otherwise **false**.  
  
##  <a name="csid__operator__lt_"></a>  CSid::operator &lt;  
 Compares relative value of two security descriptor objects.  
  
```  
  
bool operator<(   
      const CSid & lhs,   
      const CSid & rhs   
   ) throw(   );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the != operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the != operator.  
  
### Return Value  
 **true** if `lhs` is less than `rhs`, otherwise **false**.  
  
##  <a name="csid__operator__lt__eq"></a>  CSid::operator &lt;=  
 Compares relative value of two security descriptor objects.  
  
```  
  
bool operator<(   
      const CSid & lhs,   
      const CSid & rhs   
   ) throw( );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the != operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the != operator.  
  
### Return Value  
 **true** if `lhs` is less than or equal to `rhs`, otherwise **false**.  
  
##  <a name="csid__operator__gt_"></a>  CSid::operator &gt;  
 Compares relative value of two security descriptor objects.  
  
```  
  
bool operator<(   
      const CSid & lhs,   
      const CSid & rhs   
   ) throw(   );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the != operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the != operator.  
  
### Return Value  
 **true** if `lhs` is greater than `rhs`, otherwise **false**.  
  
##  <a name="csid__operator__gt__eq"></a>  CSid::operator &gt;=  
 Compares relative value of two security descriptor objects.  
  
```  
  
bool operator<(   
      const CSid & lhs,   
      const CSid & rhs  
   ) throw( )   
   );  
  
```  
  
### Parameters  
 `lhs`  
 The `SID` (security identifier) or `CSid` that appears on the left side of the != operator.  
  
 `rhs`  
 The `SID` (security identifier) or `CSid` that appears on the right side of the != operator.  
  
### Return Value  
 **true** if `lhs` is greater than or equal to `rhs`, otherwise **false**.  
  
##  <a name="csid__operator_const_sid__star"></a>  CSid::operator const SID *  
 Casts a `CSid` object to a pointer to a `SID` (security identifier) structure.  
  
```  
  
operator const SID *( ) const throw(...);  
  
```  
  
### Remarks  
 Returns the address of the `SID` structure.  
  
##  <a name="csid__sid"></a>  CSid::Sid  
 Returns the `SID` (security identifier) structure as a string.  
  
```  
  
LPCTSTR Sid( ) const throw(...);  
  
```  
  
### Return Value  
 Returns the `SID` structure as a string in a format suitable for display, storage, or transmission. Equivalent to [ConvertSidToStringSid](http://msdn.microsoft.com/library/windows/desktop/aa376399), although this function is only available on Windows 2000 or later and so is emulated for earlier operating systems.  
  
##  <a name="csid__sidnameuse"></a>  CSid::SidNameUse  
 Returns a description of the state of the `CSid` object.  
  
```  
  
SID_NAME_USE SidNameUse( ) const throw( );  
  
```  
  
### Return Value  
 Returns the value of the data member that stores a value describing the state of the `CSid` object.  
  
|Value|Description|  
|-----------|-----------------|  
|SidTypeUser|Indicates a user `SID` (security identifier).|  
|SidTypeGroup|Indicates a group `SID`.|  
|SidTypeDomain|Indicates a domain `SID`.|  
|SidTypeAlias|Indicates an alias `SID`.|  
|SidTypeWellKnownGroup|Indicates a `SID` for a well-known group.|  
|SidTypeDeletedAccount|Indicates a `SID` for a deleted account.|  
|SidTypeInvalid|Indicates an invalid `SID`.|  
|SidTypeUnknown|Indicates an unknown `SID` type.|  
|SidTypeComputer|Indicates a `SID` for a computer.|  
  
### Remarks  
 Call [CSid::LoadAccount](../vs140/CSid--LoadAccount.md) to update the `CSid` object before calling `SidNameUse` to return its state. `SidNameUse` does not change the state of the object (by calling to **LookupAccountName** or **LookupAccountSid**), but only returns the current state.  
  
## See Also  
 [Security Sample](../vs140/Visual-C---Samples.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Security Global Functions](../vs140/Security-Global-Functions.md)   
 [Operators Alphabetical Reference](../vs140/ATL-Operators-Alphabetical-Reference.md)