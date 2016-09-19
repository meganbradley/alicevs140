---
title: "When Element (MSBuild)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
  - CSharp
  - C++
  - jsharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb27de6f-4e71-4e87-87e2-d93f7bf5899c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# When Element (MSBuild)
Specifies a possible block of code for the `Choose` element to select.  
  
 <Project\>  
 <Choose\>  
 <When\>  
 <Choose\>  
 ...  
 <Otherwise\>  
 <Choose\>  
 ...  
  
## Syntax  
  
```  
<When Condition="'StringA'=='StringB'">  
    <PropertyGroup>... </PropertyGroup>  
    <ItemGroup>... </ItemGroup>  
    <Choose>... </Choose>  
</When>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|Condition|Required attribute.<br /><br /> Condition to evaluate. For more information, see [MSBuild Conditions](../vs140/MSBuild-Conditions.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Choose](../vs140/Choose-Element--MSBuild-.md)|Optional element.<br /><br /> Evaluates child elements to select one section of code to execute. There may be zero or more `Choose` elements in a `When` element.|  
|[ItemGroup](../vs140/ItemGroup-Element--MSBuild-.md)|Optional element.<br /><br /> Contains a set of user-defined [Item](../vs140/Item-Element--MSBuild-.md) elements. There may be zero or more `ItemGroup` elements in a `When` element.|  
|[PropertyGroup](../vs140/PropertyGroup-Element--MSBuild-.md)|Optional element.<br /><br /> Contains a set of user-defined [Property](../vs140/Property-Element--MSBuild-.md) elements. There may be zero or more `PropertyGroup` elements in an `When` element.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[Choose Element (MSBuild)](../vs140/Choose-Element--MSBuild-.md)|Evaluates child elements to select one section of code to execute.|  
  
## Remarks  
 If the `Condition` attribute evaluates to true, the child `ItemGroup` and `PropertyGroup` elements of the `When` element are executed and all subsequent `When` elements are skipped.  
  
 The `Choose`, `When`, and `Otherwise` elements are used together to provide a way to select one section of code to execute out of a number of possible alternatives. For more information, see [MSBuild Conditional Constructs](../vs140/MSBuild-Conditional-Constructs.md).  
  
## Example  
 The following project uses the `Choose` element to select which set of property values in the `When` elements to set. If the `Condition` attributes of both `When` elements evaluate to `false`, the property values in the `Otherwise` element are set.  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003" >  
    <PropertyGroup>  
        <Configuration Condition="'$(Configuration)' == ''">Debug</Configuration>  
        <OutputType>Exe</OutputType>  
        <RootNamespace>ConsoleApplication1</RootNamespace>  
        <AssemblyName>ConsoleApplication1</AssemblyName>  
        <WarningLevel>4</WarningLevel>  
    </PropertyGroup>  
    <Choose>  
        <When Condition=" '$(Configuration)'=='debug' ">  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <DebugType>full</DebugType>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\Debug\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
            <ItemGroup>  
                <Compile Include="UnitTesting\*.cs" />  
                <Reference Include="NUnit.dll" />  
            </ItemGroup>  
        </When>  
        <When Condition=" '$(Configuration)'=='retail' ">  
            <PropertyGroup>  
                <DebugSymbols>false</DebugSymbols>  
                <Optimize>true</Optimize>  
                <OutputPath>.\bin\Release\</OutputPath>  
                <DefineConstants>TRACE</DefineConstants>  
            </PropertyGroup>  
        </When>  
        <Otherwise>  
            <PropertyGroup>  
                <DebugSymbols>true</DebugSymbols>  
                <Optimize>false</Optimize>  
                <OutputPath>.\bin\$(Configuration)\</OutputPath>  
                <DefineConstants>DEBUG;TRACE</DefineConstants>  
            </PropertyGroup>  
        </Otherwise>  
    </Choose>  
    <Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />  
</Project>  
```  
  
## See Also  
 [MSBuild Conditional Constructs](../vs140/MSBuild-Conditional-Constructs.md)   
 [MSBuild Project File Schema Reference](../vs140/MSBuild-Project-File-Schema-Reference.md)