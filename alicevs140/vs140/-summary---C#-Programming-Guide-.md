---
title: "&lt;summary&gt; (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4c43d92-2067-4eac-a59a-d32f5248c08b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;summary&gt; (C# Programming Guide)
## Syntax  
  
```  
<summary>description</summary>  
```  
  
#### Parameters  
 `description`  
 A summary of the object.  
  
## Remarks  
 The <summary\> tag should be used to describe a type or a type member. Use [<remarks\>](../vs140/-remarks---C#-Programming-Guide-.md) to add supplemental information to a type description. Use the [cref Attribute](../vs140/cref-Attribute--C#-Programming-Guide-.md) to enable documentation tools such as [Sandcastle](http://go.microsoft.com/fwlink/?LinkId=124061) to create internal hyperlinks to documentation pages for code elements.  
  
 The text for the <summary\> tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser Window.  
  
 Compile with [/doc](../Topic/-doc%20\(C%23%20Compiler%20Options\).md) to process documentation comments to a file. To create the final documentation based on the compiler-generated file, you can create a custom tool, or use a tool such as [Sandcastle](http://go.microsoft.com/fwlink/?LinkId=124061).  
  
## Example  
 [!CODE [csProgGuideDocComments#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#12)]  
  
 The previous example produces the following XML file.  
  
```  
<?xml version="1.0"?>  
<doc>  
    <assembly>  
        <name>YourNamespace</name>  
    </assembly>  
    <members>  
        <member name="T:DotNetEvents.TestClass">  
            text for class TestClass  
        </member>  
        <member name="M:DotNetEvents.TestClass.DoWork(System.Int32)">  
            <summary>DoWork is a method in the TestClass class.  
            <para>Here's how you could make a second paragraph in a description. <see cref="M:System.Console.WriteLine(System.String)"/> for information about output statements.</para>  
            <seealso cref="M:DotNetEvents.TestClass.Main"/>  
            </summary>  
        </member>  
        <member name="M:DotNetEvents.TestClass.Main">  
            text for Main  
        </member>  
    </members>  
</doc>  
```  
  
## Example  
 The following example shows how to make a `cref` reference to a generic type.  
  
 [!CODE [csProgGuideDocComments#11](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideDocComments#11)]  
  
 The previous example produces the following XML file.  
  
```  
<?xml version="1.0"?>  
<doc>  
    <assembly>  
        <name>YourNamespace</name>  
    </assembly>  
    <members>  
        <member name="T:ExtensionMethodsDemo1.A">  
            <summary cref="T:ExtensionMethodsDemo1.C`1">  
            </summary>  
        </member>  
        <member name="T:ExtensionMethodsDemo1.B">  
            <summary cref="T:C`1">  
            </summary>  
        </member>  
        <member name="T:ExtensionMethodsDemo1.C`1">  
            <summary cref="T:ExtensionMethodsDemo1.A">  
            </summary>  
            <typeparam name="T"></typeparam>  
        </member>  
    </members>  
</doc>  
  
```  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Recommended Tags for Documentation Comments](../vs140/Recommended-Tags-for-Documentation-Comments--C#-Programming-Guide-.md)