# Convert PDF file to Text file in C# - Step by Step
## Requires
- Visual Studio 2012
## License
- MS-LPL
## Technologies
- C#
- Silverlight
- ASP.NET
- Windows Forms
- Microsoft Azure
- .NET Framework
- VB.Net
- .NET Framework 4.0
- SharePoint Server 2010
- Silverlight 5
- Visual C#
## Topics
- Controls
- C#
- ASP.NET
- Windows Forms
- Microsoft Azure
- .NET 4
- How to
## Updated
- 03/22/2016
## Description

<h1>Introduction</h1>
<p><em>This is a C# example to convert PDF file to Text via a free C# PDF library.</em></p>
<p><em><br>
If you are searching for a solution to convert PDF documents into Text-format in C#, stop the searching - you're in the right place! The PDF Focus .Net is only the one library designed for this purpose.</em></p>
<p><em><br>
Only the .Net platform and nothing else, 32 and 64-bit support, Medium Trust level, converting of all types of PDF documents, works under Windows, Mac, Linux and a lot of other nuances</em><em>.</em></p>
<h1><strong>Main Functions</strong></h1>
<p><em><img id="149924" src="149924-pdf_to_text.png" alt="" width="800" height="473"></em></p>
<h1>How to do it:</h1>
<p><em>So, here we'll show you in details how to convert a PDF document to Text file in C#.</em></p>
<p><em><strong><span class="blue12b">Very simple example.</span></strong>&nbsp;For example, we've the PDF file: Sample.pdf (please see in att. file) and we need to create an Text document from Sample.pdf</em></p>
<p><em><span class="blue12b"><strong>Step 1</strong>:</span>&nbsp;Launch Visual Studio 2010 (2013). Click File-&gt;New Project-&gt;Visual C# Console Application.</em></p>
<p><em>Type the application name and location, for example &quot;pdf to text&quot; and &quot;c:\samples&quot;.</em></p>
<p><em><span class="blue12b"><strong>Step 2</strong>:</span>&nbsp;In the Solution Explorer right-click on &quot;References&quot; and select &quot;Add Reference&quot;. Next add a reference to the &quot;SautinSoft.PdfFocus.dll&quot;</em><em>.</em></p>
<p><em><span class="blue12b"><strong>Step 3</strong>:</span>&nbsp;So, we've created an empty C# console application. Now type the C# code to convert our Sample.pdf into Sample.txt</em></p>
<p><em><strong>Step 4</strong>: Please insert c# code in your console application.&nbsp;Now build the application and launch it.</em></p>
<p><em><strong><span class="blue12b">Well done!</span>&nbsp;</strong>Our congratulations, with help of the PDF Focus .Net library we've created an editable Word document.</em></p>
<p>&nbsp;</p>
<div class="scriptcode">
<div class="pluginEditHolder" pluginCommand="mceScriptCode">
<div class="title"><span>C#</span></div>
<div class="pluginLinkHolder"><span class="pluginEditHolderLink">Edit</span>|<span class="pluginRemoveHolderLink">Remove</span></div>
<span class="hidden">csharp</span>

<div class="preview">
<pre class="csharp"><span class="cs__keyword">using</span>&nbsp;System;&nbsp;
<span class="cs__keyword">using</span>&nbsp;<a class="libraryLink" href="https://msdn.microsoft.com/en-US/library/System.IO.aspx" target="_blank" title="Auto generated link to System.IO">System.IO</a>;&nbsp;
<span class="cs__keyword">using</span>&nbsp;SautinSoft;&nbsp;
&nbsp;
<span class="cs__keyword">namespace</span>&nbsp;Sample&nbsp;
{&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">class</span>&nbsp;Sample&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">static</span>&nbsp;<span class="cs__keyword">void</span>&nbsp;Main(<span class="cs__keyword">string</span>[]&nbsp;args)&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">string</span>&nbsp;pathToPdf&nbsp;=&nbsp;@<span class="cs__string">&quot;D:\Tempos\Sample.pdf&quot;</span>;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">string</span>&nbsp;pathToText&nbsp;=&nbsp;@<span class="cs__string">&quot;D:\Tempos\Sample.txt&quot;</span>;&nbsp;
&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__com">//Convert&nbsp;PDF&nbsp;file&nbsp;to&nbsp;Text&nbsp;file</span>&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;SautinSoft.PdfFocus&nbsp;f&nbsp;=&nbsp;<span class="cs__keyword">new</span>&nbsp;SautinSoft.PdfFocus();&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__com">//&nbsp;You&nbsp;may&nbsp;download&nbsp;the&nbsp;latest&nbsp;version&nbsp;of&nbsp;SDK&nbsp;here:&nbsp;&nbsp;</span>&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__com">//&nbsp;www.sautinsoft.com/products/pdf-focus/download.php&nbsp;&nbsp;</span>&nbsp;
&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;f.OpenPdf(pathToPdf);&nbsp;
&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">if</span>&nbsp;(f.PageCount&nbsp;&gt;&nbsp;<span class="cs__number">0</span>)&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">int</span>&nbsp;result&nbsp;=&nbsp;f.ToText(pathToText);&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__com">//Show&nbsp;Text&nbsp;document</span>&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="cs__keyword">if</span>&nbsp;(result==<span class="cs__number">0</span>)&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a class="libraryLink" href="https://msdn.microsoft.com/en-US/library/System.Diagnostics.Process.Start.aspx" target="_blank" title="Auto generated link to System.Diagnostics.Process.Start">System.Diagnostics.Process.Start</a>(pathToText);&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}&nbsp;
&nbsp;&nbsp;&nbsp;&nbsp;}&nbsp;
}</pre>
</div>
</div>
</div>
<h1>Source Code Files</h1>
<p>&nbsp;<em>Related Links:</em></p>
<div><em><br>
Website:&nbsp;<a href="http://www.sautinsoft.com/">www.sautinsoft.com</a><br>
Product Home:&nbsp;<a href="http://sautinsoft.com/products/pdf-focus/index.php">PDF Focus .NET</a><br>
Download:&nbsp;<a href="http://sautinsoft.com/thankyou.php?download=pdf_focus_net.zip">PDF Focus .NET</a></em></div>
<p>&nbsp;</p>
<h2 class="H2Text">Requrements and Technical Information</h2>
<p class="CommonText"><em>Requires only .Net 2.0 or above. Our product is compatible with all .Net languages and supports all Operating Systems where .Net Framework can be used. Note that PDF Focus .Net is entirely written in managed C#, which makes it absolutely
 standalone and an independent library</em></p>
