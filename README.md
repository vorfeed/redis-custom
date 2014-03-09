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

