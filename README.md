# Redis Custom

An enhanced version of Redis, upgrade 6 commands and add 16 new commands.

Modification based on the [Redis version 2.8.4](https://github.com/antirez/redis/releases/tag/2.8.4 "redis-2.8.4"), the [Jedis version 2.4.0](https://github.com/xetorthio/jedis/releases/tag/jedis-2.4.0 "jedis-2.4.0").

## Upgraded features

<html xmlns:v="urn:schemas-microsoft-com:vml"
xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:w="urn:schemas-microsoft-com:office:word"
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"
xmlns:m="http://schemas.microsoft.com/office/2004/12/omml"
xmlns="http://www.w3.org/TR/REC-html40">

<head>
<meta http-equiv=Content-Type content="text/html; charset=gb2312">
<meta name=ProgId content=Word.Document>
<meta name=Generator content="Microsoft Word 15">
<meta name=Originator content="Microsoft Word 15">
<link rel=File-List href="redis-custom.files/filelist.xml">
<!--[if gte mso 9]><xml>
 <o:DocumentProperties>
  <o:Author>vorfeed Chen</o:Author>
  <o:LastAuthor>vorfeed Chen</o:LastAuthor>
  <o:Revision>4</o:Revision>
  <o:TotalTime>61</o:TotalTime>
  <o:Created>2014-03-09T13:10:00Z</o:Created>
  <o:LastSaved>2014-03-09T13:11:00Z</o:LastSaved>
  <o:Pages>1</o:Pages>
  <o:Words>1454</o:Words>
  <o:Characters>8294</o:Characters>
  <o:Lines>69</o:Lines>
  <o:Paragraphs>19</o:Paragraphs>
  <o:CharactersWithSpaces>9729</o:CharactersWithSpaces>
  <o:Version>15.00</o:Version>
 </o:DocumentProperties>
 <o:OfficeDocumentSettings>
  <o:AllowPNG/>
 </o:OfficeDocumentSettings>
</xml><![endif]-->
<link rel=themeData href="redis-custom.files/themedata.thmx">
<link rel=colorSchemeMapping href="redis-custom.files/colorschememapping.xml">
<!--[if gte mso 9]><xml>
 <w:WordDocument>
  <w:TrackMoves>false</w:TrackMoves>
  <w:TrackFormatting/>
  <w:PunctuationKerning/>
  <w:DrawingGridHorizontalSpacing>5.25 磅</w:DrawingGridHorizontalSpacing>
  <w:DrawingGridVerticalSpacing>7.8 磅</w:DrawingGridVerticalSpacing>
  <w:DisplayHorizontalDrawingGridEvery>0</w:DisplayHorizontalDrawingGridEvery>
  <w:DisplayVerticalDrawingGridEvery>2</w:DisplayVerticalDrawingGridEvery>
  <w:ValidateAgainstSchemas/>
  <w:SaveIfXMLInvalid>false</w:SaveIfXMLInvalid>
  <w:IgnoreMixedContent>false</w:IgnoreMixedContent>
  <w:AlwaysShowPlaceholderText>false</w:AlwaysShowPlaceholderText>
  <w:DoNotPromoteQF/>
  <w:LidThemeOther>EN-US</w:LidThemeOther>
  <w:LidThemeAsian>ZH-CN</w:LidThemeAsian>
  <w:LidThemeComplexScript>X-NONE</w:LidThemeComplexScript>
  <w:Compatibility>
   <w:SpaceForUL/>
   <w:BalanceSingleByteDoubleByteWidth/>
   <w:DoNotLeaveBackslashAlone/>
   <w:ULTrailSpace/>
   <w:DoNotExpandShiftReturn/>
   <w:AdjustLineHeightInTable/>
   <w:BreakWrappedTables/>
   <w:SnapToGridInCell/>
   <w:WrapTextWithPunct/>
   <w:UseAsianBreakRules/>
   <w:DontGrowAutofit/>
   <w:SplitPgBreakAndParaMark/>
   <w:EnableOpenTypeKerning/>
   <w:DontFlipMirrorIndents/>
   <w:OverrideTableStyleHps/>
   <w:UseFELayout/>
  </w:Compatibility>
  <m:mathPr>
   <m:mathFont m:val="Cambria Math"/>
   <m:brkBin m:val="before"/>
   <m:brkBinSub m:val="&#45;-"/>
   <m:smallFrac m:val="off"/>
   <m:dispDef/>
   <m:lMargin m:val="0"/>
   <m:rMargin m:val="0"/>
   <m:defJc m:val="centerGroup"/>
   <m:wrapIndent m:val="1440"/>
   <m:intLim m:val="subSup"/>
   <m:naryLim m:val="undOvr"/>
  </m:mathPr></w:WordDocument>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <w:LatentStyles DefLockedState="false" DefUnhideWhenUsed="false"
  DefSemiHidden="false" DefQFormat="false" DefPriority="99"
  LatentStyleCount="371">
  <w:LsdException Locked="false" Priority="0" QFormat="true" Name="Normal"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 1"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 2"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 3"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 4"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 5"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 6"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 7"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 8"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 9"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 9"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 1"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 2"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 3"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 4"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 5"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 6"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 7"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 8"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 9"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footnote text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="header"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footer"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index heading"/>
  <w:LsdException Locked="false" Priority="35" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="caption"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="table of figures"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="envelope address"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="envelope return"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footnote reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="line number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="page number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="endnote reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="endnote text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="table of authorities"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="macro"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="toa heading"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 5"/>
  <w:LsdException Locked="false" Priority="10" QFormat="true" Name="Title"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Closing"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Signature"/>
  <w:LsdException Locked="false" Priority="1" SemiHidden="true"
   UnhideWhenUsed="true" Name="Default Paragraph Font"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Message Header"/>
  <w:LsdException Locked="false" Priority="11" QFormat="true" Name="Subtitle"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Salutation"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Date"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text First Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text First Indent 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Note Heading"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Block Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Hyperlink"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="FollowedHyperlink"/>
  <w:LsdException Locked="false" Priority="22" QFormat="true" Name="Strong"/>
  <w:LsdException Locked="false" Priority="20" QFormat="true" Name="Emphasis"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Document Map"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Plain Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="E-mail Signature"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Top of Form"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Bottom of Form"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal (Web)"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Acronym"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Address"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Cite"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Code"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Definition"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Keyboard"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Preformatted"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Sample"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Typewriter"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Variable"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal Table"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation subject"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="No List"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Contemporary"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Elegant"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Professional"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Subtle 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Subtle 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Balloon Text"/>
  <w:LsdException Locked="false" Priority="39" Name="Table Grid"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Theme"/>
  <w:LsdException Locked="false" SemiHidden="true" Name="Placeholder Text"/>
  <w:LsdException Locked="false" Priority="1" QFormat="true" Name="No Spacing"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 1"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 1"/>
  <w:LsdException Locked="false" SemiHidden="true" Name="Revision"/>
  <w:LsdException Locked="false" Priority="34" QFormat="true"
   Name="List Paragraph"/>
  <w:LsdException Locked="false" Priority="29" QFormat="true" Name="Quote"/>
  <w:LsdException Locked="false" Priority="30" QFormat="true"
   Name="Intense Quote"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 1"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 1"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 2"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 2"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 2"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 3"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 3"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 3"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 4"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 4"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 4"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 5"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 5"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 5"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 6"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 6"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 6"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="19" QFormat="true"
   Name="Subtle Emphasis"/>
  <w:LsdException Locked="false" Priority="21" QFormat="true"
   Name="Intense Emphasis"/>
  <w:LsdException Locked="false" Priority="31" QFormat="true"
   Name="Subtle Reference"/>
  <w:LsdException Locked="false" Priority="32" QFormat="true"
   Name="Intense Reference"/>
  <w:LsdException Locked="false" Priority="33" QFormat="true" Name="Book Title"/>
  <w:LsdException Locked="false" Priority="37" SemiHidden="true"
   UnhideWhenUsed="true" Name="Bibliography"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="TOC Heading"/>
  <w:LsdException Locked="false" Priority="41" Name="Plain Table 1"/>
  <w:LsdException Locked="false" Priority="42" Name="Plain Table 2"/>
  <w:LsdException Locked="false" Priority="43" Name="Plain Table 3"/>
  <w:LsdException Locked="false" Priority="44" Name="Plain Table 4"/>
  <w:LsdException Locked="false" Priority="45" Name="Plain Table 5"/>
  <w:LsdException Locked="false" Priority="40" Name="Grid Table Light"/>
  <w:LsdException Locked="false" Priority="46" Name="Grid Table 1 Light"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark"/>
  <w:LsdException Locked="false" Priority="51" Name="Grid Table 6 Colorful"/>
  <w:LsdException Locked="false" Priority="52" Name="Grid Table 7 Colorful"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 1"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 1"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 1"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 2"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 2"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 2"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 3"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 3"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 3"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 4"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 4"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 4"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 5"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 5"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 5"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 6"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 6"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 6"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="46" Name="List Table 1 Light"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark"/>
  <w:LsdException Locked="false" Priority="51" Name="List Table 6 Colorful"/>
  <w:LsdException Locked="false" Priority="52" Name="List Table 7 Colorful"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 1"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 1"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 1"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 2"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 2"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 2"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 3"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 3"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 3"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 4"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 4"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 4"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 5"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 5"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 5"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 6"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 6"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 6"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 6"/>
 </w:LatentStyles>
</xml><![endif]-->
<style>
<!--
 /* Font Definitions */
 @font-face
	{font-family:宋体;
	panose-1:2 1 6 0 3 1 1 1 1 1;
	mso-font-alt:SimSun;
	mso-font-charset:134;
	mso-generic-font-family:auto;
	mso-font-pitch:variable;
	mso-font-signature:3 680460288 22 0 262145 0;}
@font-face
	{font-family:"Cambria Math";
	panose-1:2 4 5 3 5 4 6 3 2 4;
	mso-font-charset:1;
	mso-generic-font-family:roman;
	mso-font-format:other;
	mso-font-pitch:variable;
	mso-font-signature:0 0 0 0 0 0;}
@font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;
	mso-font-charset:0;
	mso-generic-font-family:swiss;
	mso-font-pitch:variable;
	mso-font-signature:-536870145 1073786111 1 0 415 0;}
@font-face
	{font-family:Monaco;
	panose-1:2 11 5 9 3 4 4 4 2 4;
	mso-font-charset:0;
	mso-generic-font-family:modern;
	mso-font-pitch:fixed;
	mso-font-signature:7 0 0 0 147 0;}
@font-face
	{font-family:"\@宋体";
	panose-1:2 1 6 0 3 1 1 1 1 1;
	mso-font-charset:134;
	mso-generic-font-family:auto;
	mso-font-pitch:variable;
	mso-font-signature:3 680460288 22 0 262145 0;}
 /* Style Definitions */
 p.MsoNormal, li.MsoNormal, div.MsoNormal
	{mso-style-unhide:no;
	mso-style-qformat:yes;
	mso-style-parent:"";
	margin:0cm;
	margin-bottom:.0001pt;
	text-align:justify;
	text-justify:inter-ideograph;
	mso-pagination:none;
	font-size:10.5pt;
	mso-bidi-font-size:11.0pt;
	font-family:"Calibri","sans-serif";
	mso-ascii-font-family:Calibri;
	mso-ascii-theme-font:minor-latin;
	mso-fareast-font-family:宋体;
	mso-fareast-theme-font:minor-fareast;
	mso-hansi-font-family:Calibri;
	mso-hansi-theme-font:minor-latin;
	mso-bidi-font-family:"Times New Roman";
	mso-bidi-theme-font:minor-bidi;
	mso-font-kerning:1.0pt;}
p
	{mso-style-noshow:yes;
	mso-style-priority:99;
	mso-margin-top-alt:auto;
	margin-right:0cm;
	mso-margin-bottom-alt:auto;
	margin-left:0cm;
	mso-pagination:widow-orphan;
	font-size:12.0pt;
	font-family:宋体;
	mso-bidi-font-family:宋体;}
.MsoChpDefault
	{mso-style-type:export-only;
	mso-default-props:yes;
	mso-bidi-font-family:"Times New Roman";
	mso-bidi-theme-font:minor-bidi;}
 /* Page Definitions */
 @page
	{mso-page-border-surround-header:no;
	mso-page-border-surround-footer:no;}
@page WordSection1
	{size:595.3pt 841.9pt;
	margin:36.0pt 36.0pt 36.0pt 36.0pt;
	mso-header-margin:42.55pt;
	mso-footer-margin:49.6pt;
	mso-paper-source:0;
	layout-grid:15.6pt;}
div.WordSection1
	{page:WordSection1;}
 /* List Definitions */
 @list l0
	{mso-list-id:363138322;
	mso-list-template-ids:1562291880;}
@list l0:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l0:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1
	{mso-list-id:417365376;
	mso-list-template-ids:-603172832;}
@list l1:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l1:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2
	{mso-list-id:533730974;
	mso-list-template-ids:-1012211606;}
@list l2:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l2:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3
	{mso-list-id:619577927;
	mso-list-template-ids:414513796;}
@list l3:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l3:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4
	{mso-list-id:655884659;
	mso-list-template-ids:-1508727380;}
@list l4:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l4:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5
	{mso-list-id:762186659;
	mso-list-template-ids:1388379302;}
@list l5:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l5:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6
	{mso-list-id:917132897;
	mso-list-template-ids:315624802;}
@list l6:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l6:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7
	{mso-list-id:957951575;
	mso-list-template-ids:339225410;}
@list l7:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l7:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8
	{mso-list-id:961302800;
	mso-list-template-ids:902435924;}
@list l8:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l8:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9
	{mso-list-id:1733188492;
	mso-list-template-ids:-888094832;}
@list l9:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l9:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10
	{mso-list-id:1755589692;
	mso-list-template-ids:-1885065560;}
@list l10:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l10:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11
	{mso-list-id:1886134232;
	mso-list-template-ids:-1592906378;}
@list l11:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l11:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12
	{mso-list-id:1937206618;
	mso-list-template-ids:-1160508960;}
@list l12:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l12:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13
	{mso-list-id:1950702467;
	mso-list-template-ids:-541805786;}
@list l13:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l13:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14
	{mso-list-id:1998801527;
	mso-list-template-ids:-495946270;}
@list l14:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l14:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15
	{mso-list-id:2143306385;
	mso-list-template-ids:177794752;}
@list l15:level1
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:36.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level2
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:72.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level3
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:108.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level4
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:144.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level5
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:180.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level6
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:216.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level7
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:252.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level8
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:288.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
@list l15:level9
	{mso-level-number-format:bullet;
	mso-level-text:\F0B7;
	mso-level-tab-stop:324.0pt;
	mso-level-number-position:left;
	text-indent:-18.0pt;
	mso-ansi-font-size:10.0pt;
	font-family:Symbol;}
ol
	{margin-bottom:0cm;}
ul
	{margin-bottom:0cm;}
-->
</style>
<!--[if gte mso 10]>
<style>
 /* Style Definitions */
 table.MsoNormalTable
	{mso-style-name:普通表格;
	mso-tstyle-rowband-size:0;
	mso-tstyle-colband-size:0;
	mso-style-noshow:yes;
	mso-style-priority:99;
	mso-style-parent:"";
	mso-padding-alt:0cm 5.4pt 0cm 5.4pt;
	mso-para-margin:0cm;
	mso-para-margin-bottom:.0001pt;
	mso-pagination:widow-orphan;
	font-size:10.5pt;
	mso-bidi-font-size:11.0pt;
	font-family:"Calibri","sans-serif";
	mso-ascii-font-family:Calibri;
	mso-ascii-theme-font:minor-latin;
	mso-hansi-font-family:Calibri;
	mso-hansi-theme-font:minor-latin;
	mso-font-kerning:1.0pt;}
</style>
<![endif]--><!--[if gte mso 9]><xml>
 <o:shapedefaults v:ext="edit" spidmax="1026"/>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <o:shapelayout v:ext="edit">
  <o:idmap v:ext="edit" data="1"/>
 </o:shapelayout></xml><![endif]-->
</head>

<body lang=ZH-CN style='tab-interval:21.0pt;text-justify-trim:punctuation'>

<div class=WordSection1 style='layout-grid:15.6pt'>

<p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan'><span
lang=EN-US style='font-size:12.0pt;font-family:Monaco;mso-fareast-font-family:
宋体;mso-bidi-font-family:宋体;color:black;mso-font-kerning:0pt'><o:p>&nbsp;</o:p></span></p>

<table class=MsoNormalTable border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid #A3A3A3 1.0pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 0cm 0cm 0cm'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=94 style='width:70.7pt;border:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border:solid #A3A3A3 1.0pt;border-left:
  none;mso-border-left-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Command<o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border:solid #A3A3A3 1.0pt;
  border-left:none;mso-border-left-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Description<o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border:solid #A3A3A3 1.0pt;border-left:
  none;mso-border-left-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>May affect<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=94 rowspan=5 style='width:70.7pt;border:solid #A3A3A3 1.0pt;
  border-top:none;mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>String<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCR</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>modified to<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCR</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key <span style='color:#C00000'>[EX seconds] [PX
  milliseconds] [XX]</span></i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Increments the number stored at <i>key</i> by one. If
  the <i>key</i> does not exist, no operation is performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Options<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>EX <i>seconds</i> -- Set the specified expire time, in
  seconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PX <i>millisecond</i> -- Set the specified expire time,
  in milliseconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>XX -- Only increase the key if it already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value of <i>key</i> after
  the increment if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if the <i>key</i>
  was not set.</span><span lang=EN-US style='font-size:11.5pt;font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=4 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCR<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECR<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCRBY<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECRBY<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECR</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>modified to<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECR</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key <span style='color:#C00000'>[EX seconds] [PX
  milliseconds] [XX]</span></i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Decrements the number stored at <i>key</i> by one. If
  the <i>key</i> does not exist, no operation is performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Options<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>EX <i>seconds</i> -- Set the specified expire time, in
  seconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PX <i>millisecond</i> -- Set the specified expire time,
  in milliseconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>XX -- Only decrease the key if it already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value of <i>key</i> after
  the decrement if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if the <i>key</i>
  was not set.</span><span lang=EN-US style='font-size:11.5pt;font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCRBY</span></b><span lang=EN-US style='font-size:
  11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:
  宋体;mso-font-kerning:0pt'> <i>key increment</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>modified to<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>INCRBY</span></b><span lang=EN-US style='font-size:
  11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:
  宋体;mso-font-kerning:0pt'> <i>key increment <span style='color:#C00000'>[EX
  seconds] [PX milliseconds] [XX]</span></i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Increments the number stored at <i>key</i> by <i>increment</i>.
  If the <i>key</i> does not exist, no operation is performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Options<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>EX <i>seconds</i> -- Set the specified expire time, in
  seconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PX <i>millisecond</i> -- Set the specified expire time,
  in milliseconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>XX -- Only increase the key if it already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value of <i>key</i> after
  the increment if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if the <i>key</i>
  was not set.</span><span lang=EN-US style='font-size:11.5pt;font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECRBY</span></b><span lang=EN-US style='font-size:
  11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:
  宋体;mso-font-kerning:0pt'> <i>key decrement</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>modified to<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>DECRBY</span></b><span lang=EN-US style='font-size:
  11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:
  宋体;mso-font-kerning:0pt'> <i>key decrement <span style='color:#C00000'>[EX
  seconds] [PX milliseconds] [XX]</span></i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Decrements the number stored at <i>key</i> by <i>increment</i>.
  If the <i>key</i> does not exist, no operation is performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Options<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>EX <i>seconds</i> -- Set the specified expire time, in
  seconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PX <i>millisecond</i> -- Set the specified expire time,
  in milliseconds.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>XX -- Only decrease the key if it already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value of <i>key</i> after
  the decrement if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if the <i>key</i>
  was not set.</span><span lang=EN-US style='font-size:11.5pt;font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SET</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key value [EX seconds] [PX milliseconds] [NX|XX]</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>modified to<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SET</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> <i>key value [EX seconds] [PX milliseconds] [NX|XX<span
  style='color:#C00000'>|EQ</span>]</i><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>SETEQ</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key value</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set <i>key</i> to hold the string <i>value</i>.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Options<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>EQ -- Determine whether the set value and the given <i>value</i>
  are equal if <i>key</i> exists, otherwise set <i>key</i> to hold the <i>value</i>.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value</span><span
  lang=EN-US style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>(for EQ)<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Simple string reply</span><span
  lang=EN-US style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <i>OK</i> if <i>key</i> does
  not exist.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if the set value and
  the given <i>value</i> are equal under the condition of <i>key</i> existing.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if the set value and
  the given <i>value</i> are not equal under the condition of <i>key</i>
  existing.</span><span lang=EN-US style='font-size:11.5pt;font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SET<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SETNX<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SETEX<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PSETEX<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6'>
  <td width=94 rowspan=6 style='width:70.7pt;border:solid #A3A3A3 1.0pt;
  border-top:none;mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>List<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>LFIND</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key value
  number</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Get <i>number</i> successor elements of the given <i>value</i>,
  including itself, in a list stored at <i>key</i>.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Array reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: the <i>number</i> successor
  elements of the given value, including itself, in the list.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Bulk string reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <i>nil</i> if <i>key</i> or <i>value</i>
  does not yet exist.<o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=2 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>无<span lang=EN-US><o:p></o:p></span></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>RFIND</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key value
  number</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Get <i>number</i> predecessor elements of the given <i>value</i>,
  including itself, in a list stored at <i>key</i>.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Array reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: the <i>number</i> predecessor
  elements of the given value, including itself, in the list.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Bulk string reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <i>nil</i> if <i>key</i> or <i>value</i>
  does not yet exist.<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>LPUSHNX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key value
  [value ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Insert all the specified <i>values</i> at the head of
  the list stored at <i>key</i>, only if <i>key</i> does not yet exist. In
  contrary to <span style='color:#0070C0'>LPUSH</span>, no operation will be
  performed when <i>key</i> already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i>
  already exists.</span><span lang=EN-US style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist.</span><span lang=EN-US style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=2 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>LPUSH<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>RPUSH<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>PUSHX<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>RPUSHNX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key value
  [value ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Insert all the specified <i>values</i> at the tail of
  the list stored at <i>key</i>, only if <i>key</i> does not yet exist. In contrary
  to <span style='color:#0070C0'>RPUSH</span>, no operation will be performed
  when <i>key</i> already exists.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i>
  already exists.</span><span lang=EN-US style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist.</span><span lang=EN-US style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>LPUSHXLTRIM</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>Key value
  start stop</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Insert <i>value</i> at the head of the list stored at <i>key</i>,
  only if <i>key</i> already exists, then trim the list to make it contain only
  the specified range of elements specified. <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Both <i>start</i> and <i>stop</i> are zero-based
  indexes, where <i>0</i> is the first element of the list (the head), <i>1</i>
  the next element and so on.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><i><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>start</span></i><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> and <i>stop</i> can also be negative numbers
  indicating offsets from the end of the list, where <i>-1</i> is the last
  element of the list, <i>-2</i> the penultimate element and so on.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Out of range indexes will not produce an error: if <i>start</i>
  is larger than the end of the list, or <i>start</i> &gt; <i>stop</i>, the
  result will be an empty list (which causes key to be removed). If end is
  larger than the end of the list, Redis will treat it like the last element of
  the list.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Simple string reply</span><span
  lang=EN-US style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <i>OK</i>.<o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=2 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>LTRIM<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>LPUSHLTRIM</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>Key value
  [value ...] start stop</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Insert all the specified <i>values</i> at the head of
  the list stored at <i>key</i>, only if <i>key</i> already exists, then trim the
  list to make it contain only the specified range of elements specified. <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Both <i>start</i> and <i>stop</i> are zero-based indexes,
  where <i>0</i> is the first element of the list (the head), <i>1</i> the next
  element and so on.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><i><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>start</span></i><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'> and <i>stop</i> can also be negative numbers
  indicating offsets from the end of the list, where <i>-1</i> is the last
  element of the list, <i>-2</i> the penultimate element and so on.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Out of range indexes will not produce an error: if <i>start</i>
  is larger than the end of the list, or <i>start</i> &gt; <i>stop</i>, the
  result will be an empty list (which causes key to be removed). If end is
  larger than the end of the list, Redis will treat it like the last element of
  the list.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Simple string reply</span><span
  lang=EN-US style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <i>OK</i>.<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12'>
  <td width=94 rowspan=7 style='width:70.7pt;border:solid #A3A3A3 1.0pt;
  border-top:none;mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Hash<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HMSETNX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  value [field value ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set the specified <i>fields</i> to their respective <i>values</i>
  in the hash stored at <i>key</i>, only if <i>key</i> does not yet exist. If <i>key</i>
  already exists, this operation has no effect.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i> does
  not yet exist in the hash and <i>values</i> were set.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i>
  already exists in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=2 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>HMSET<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HMSETEX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  value [field value ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set the specified <i>fields</i> to their respective <i>values</i>
  in the hash stored at <i>key</i>, only if <i>key</i> already exists. If <i>key</i>
  does not yet exist, this operation has no effect. If <i>fields</i> already
  exist in the hash, they are overwritten.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i>
  already in the hash and <i>values</i> were set or updated.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HINCRBYEX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  increment</i></span><span lang=EN-US style='font-size:11.5pt;font-family:
  Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'> <o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Increment the number stored at <i>field</i> in the hash
  stored at <i>key</i> by <i>increment</i>, only if <i>key</i> already exists. If
  <i>key</i> does not yet exist, this operation has no effect. If <i>field</i>
  does not yet exist the value is set to <i>0</i> before the operation is
  performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value at <i>field</i> after
  the increment operation if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>HINCRBY<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:15'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HMINCRBYEX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  increment [field increment ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Increment the numbers stored at <i>fields</i> in the
  hash stored at <i>keys</i> by each <i>increment</i>, only if <i>key</i>
  already exists. If <i>key</i> does not yet exist, this operation has no
  effect. If any <i>field</i> does not yet exist the value is set to <i>0</i>
  before the operation is performed.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the value at <i>field</i> after
  the increment operation if <i>key</i> already exists.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span style='font-size:11.5pt;font-family:
  宋体;mso-bidi-font-family:宋体;mso-font-kerning:0pt'>无<span lang=EN-US><o:p></o:p></span></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:16'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HSETEX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  value</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set <i>field</i> in the hash stored at <i>key</i> to <i>value</i>,
  only if <i>field</i> already exists. If <i>key</i> does not yet exist, this
  operation has no effect.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if both <i>key</i>
  and <i>field</i> already exist in the hash and <i>value</i> was set.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> or <i>field</i>
  does not yet exist in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 rowspan=3 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>HSET<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>HSETNX<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:17'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HSETKEX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  value</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set <i>field</i> in the hash stored at <i>key</i> to <i>value</i>,
  only if <i>key</i> already exists. If <i>key</i> does not yet exist, this
  operation has no effect. If <i>field</i> already exists in the hash, it is
  overwritten.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i>
  already in the hash and <i>value</i> was set or updated.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:18'>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>HSETKNX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key field
  value</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set <i>field</i> in the hash stored at <i>key</i> to <i>value</i>,
  only if <i>key</i> does not yet exist. If <i>key</i> already exists, this
  operation has no effect.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>1</i> if <i>key</i> does
  not yet exist in the hash and <i>value</i> was set.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i>
  already exists in the hash and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:19'>
  <td width=94 style='width:70.7pt;border:solid #A3A3A3 1.0pt;border-top:none;
  mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Set<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>SADDX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key member
  [member ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Add the specified <i>members</i> to the set stored at <i>key</i>,
  only if <i>key</i> already exists. Specified <i>members</i> that are already
  a member of this set are ignored. If <i>key</i> does not yet exist, this
  operation has no effect.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- the number of elements that
  were added to the set if <i>key</i> already exists, not including all the
  elements already present into the set.</span><span lang=EN-US
  style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;mso-font-kerning:
  0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the set and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SADD<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:20'>
  <td width=94 style='width:70.7pt;border:solid #A3A3A3 1.0pt;border-top:none;
  mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Sorted Set<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>newly added<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#C00000;mso-font-kerning:0pt'>ZADDX</span></b><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;color:#C00000;mso-font-kerning:0pt'> <i>key score
  member [score member ...]</i><o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Add all the specified <i>members</i> with the specified
  <i>scores</i> to the sorted set stored at <i>key</i>, only if <i>key</i>
  already exists. If a specified <i>member</i> is already a member of the
  sorted set, the <i>score</i> is updated and the element reinserted at the
  right position to ensure the correct ordering. If <i>key</i> does not yet
  exist, this operation has no effect.<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>&nbsp;<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:14.0pt;
  mso-bidi-font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>Return Value<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  color:#0070C0;mso-font-kerning:0pt'>Integer reply</span><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>: <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- The number of elements added
  to the sorted sets if <i>key</i> already exists, not including elements
  already existing for which the score was updated. <o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan;vertical-align:middle'><span lang=EN-US
  style='font-size:11.5pt;font-family:Monaco;mso-fareast-font-family:宋体;
  mso-bidi-font-family:宋体;mso-font-kerning:0pt'>- <i>0</i> if <i>key</i> does
  not yet exist in the sorted set and no operation was performed.</span><span
  lang=EN-US style='font-size:11.5pt;font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>ZADD<o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>ZINCRBY<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:21;mso-yfti-lastrow:yes'>
  <td width=94 style='width:70.7pt;border:solid #A3A3A3 1.0pt;border-top:none;
  mso-border-top-alt:solid #A3A3A3 1.0pt;padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Key<o:p></o:p></span></p>
  </td>
  <td width=327 style='width:245.5pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SORT</span></b><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'><o:p></o:p></span></p>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>add support for Hash<o:p></o:p></span></p>
  </td>
  <td width=627 valign=top style='width:470.15pt;border-top:none;border-left:
  none;border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>Format the entire hash map into JSON and display to the
  client.<o:p></o:p></span></p>
  </td>
  <td width=123 style='width:92.1pt;border-top:none;border-left:none;
  border-bottom:solid #A3A3A3 1.0pt;border-right:solid #A3A3A3 1.0pt;
  mso-border-top-alt:solid #A3A3A3 1.0pt;mso-border-left-alt:solid #A3A3A3 1.0pt;
  padding:4.0pt 4.0pt 4.0pt 4.0pt'>
  <p class=MsoNormal align=left style='text-align:left;mso-line-height-alt:
  0pt;mso-pagination:widow-orphan'><span lang=EN-US style='font-size:11.5pt;
  font-family:Monaco;mso-fareast-font-family:宋体;mso-bidi-font-family:宋体;
  mso-font-kerning:0pt'>SORT<o:p></o:p></span></p>
  </td>
 </tr>
</table>

<p class=MsoNormal align=left style='text-align:left;mso-pagination:widow-orphan'><span
lang=EN-US style='font-size:12.0pt;font-family:Monaco;mso-fareast-font-family:
宋体;mso-bidi-font-family:宋体;color:black;mso-font-kerning:0pt'><o:p>&nbsp;</o:p></span></p>

<p class=MsoNormal><span lang=EN-US><o:p>&nbsp;</o:p></span></p>

</div>

</body>

</html>

## Usage

Patch Redis

* download [Redis-2.8.4](https://github.com/antirez/redis/archive/2.8.4.tar.gz "Redis-2.8.4")

* cd into root directory

* patch -p1 < redis-2.8.4-custom.patch

Patch Jedis

* download [Jedis-2.4.0](https://github.com/xetorthio/jedis/archive/jedis-2.4.0.tar.gz "Jedis-2.4.0")

* cd into root directory

* patch -p1 < jedis-2.4.0-custom.patch


================================
by chenxiaojie(swly@live.com)

