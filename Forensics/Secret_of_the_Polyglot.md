If you open the file as pdf, you will get
```
1n_pn9_&_pdf_1f991f77}
```

It seems no more information, but we can download it first and then check it.
```sh
wget https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf
```

Cat it forst
```
% cat flag2of2-final.pdf
```
result
```
�PNG

IHDR2?���iCCPICC profile(�}�=H�@�_S��;f�bAT�Q�P�
�Vh����/hҐ��8
�?�.κ:�
�����������"փ�~����"Ӭ�q@�m3����xE�bC2��9I��������w���ܟ�[�X
��M��ObyY%>'3�ď\W<~�sY�!3��'��&V���M�x�8�j:�              �ĳ�0m�
                                            )�U�[��b����_��+�\�9��	"�Q@6"��XH�~����K�R�U#�J� �~�?�ݭ����Q���q>���.P�8����N�3p�7�*0�Iz������m�⺡){����dȦ�J~�B6
  ���7���[�s�뭾�� I]�o��C`$G��-����ۿg���r�r���b�	pHYs.#.#x�?vtIME�
                                                                         9�O��tEXtCommentCreated with GIMPW�{IDATh��YA���LO&�"�b��n�CW�
                                                       0Z@DL<E3	RJ)ya��"���% ;@��@��w�}�� ��/uZ��[�����(���u�^��^�Fqc��w�5�4ײ� o.��Nv�f�\i�'���TvI~�
�Z��]��)ZFd{B�f25����L1��^Y��=j{��2v�bV`���V�9y�::nM/�\�����Z⽢iܡ"�<�3"RJE���%v48�K�_s�������=�E8ő�5�$r���a���h���cz������D	����@�����f�IEND�B`�%PDF-1.4
%�쏢
%%Invocation: path/gs -P- -dSAFER -dCompatibilityLevel=1.4 -q -P- -dNOPAUSE -dBATCH -sDEVICE=pdfwrite -sstdout=? -sOutputFile=? -P- -dSAFER -dCompatibilityLevel=1.4 ?
5 0 obj
<</Length 6 0 R/Filter /FlateDecode>>
stream
x�+T0�3T0A(���e���U�U�Rɹ
N!\�A�
�f
!i\ņ
�
F@�˥a�_�g�_��o�fii�fn^�����ʦendstream
endobj
6 0 obj
93
endobj
4 0 obj
<</Type/Page/MediaBox [0 0 595 842]
/Rotate 0/Parent 3 0 R
/Resources<</ProcSet[/PDF /Text]
/Font 8 0 R
>>
/Contents 5 0 R
>>
endobj
3 0 obj
<< /Type /Pages /Kids [
4 0 R
] /Count 1
>>
endobj
1 0 obj
<</Type /Catalog /Pages 3 0 R
/Metadata 9 0 R
>>
endobj
8 0 obj
<</R7
7 0 R>>
endobj
7 0 obj
<</BaseFont/Helvetica/Type/Font
/Subtype/Type1>>
endobj
9 0 obj
<</Type/Metadata
/Subtype/XML/Length 1173>>stream
<?xpacket begin='' id='W5M0MpCehiHzreSzNTczkc9d'?>
<?adobe-xap-filters esc="CRLF"?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='XMP toolkit 2.9.1-13, framework 1.6'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#' xmlns:iX='http://ns.adobe.com/iX/1.0/'>
<rdf:Description rdf:about="" xmlns:pdf='http://ns.adobe.com/pdf/1.3/' pdf:Producer='GPL Ghostscript 10.01.2'/>
<rdf:Description rdf:about="" xmlns:xmp='http://ns.adobe.com/xap/1.0/'><xmp:ModifyDate>2024-03-12T00:04:33Z</xmp:ModifyDate>
<xmp:CreateDate>2024-03-12T00:04:33Z</xmp:CreateDate>
<xmp:CreatorTool>UnknownApplication</xmp:CreatorTool></rdf:Description>
<rdf:Description rdf:about="" xmlns:xapMM='http://ns.adobe.com/xap/1.0/mm/' xapMM:DocumentID='uuid:a7b27342-1820-11fa-0000-69698921356b'/>
<rdf:Description rdf:about="" xmlns:dc='http://purl.org/dc/elements/1.1/' dc:format='application/pdf'><dc:title><rdf:Alt><rdf:li xml:lang='x-default'>Untitled</rdf:li></rdf:Alt></dc:title></rdf:Description>
</rdf:RDF>
</x:xmpmeta>


<?xpacket end='w'?>
endstream
endobj
2 0 obj
<</Producer(GPL Ghostscript 10.01.2)
/CreationDate(D:20240312000433Z00'00')
/ModDate(D:20240312000433Z00'00')>>endobj
xref
0 10
0000000000 65535 f
0000000563 00000 n
0000001969 00000 n
0000000504 00000 n
0000000363 00000 n
0000000182 00000 n
0000000345 00000 n
0000000656 00000 n
0000000627 00000 n
0000000720 00000 n
trailer
<< /Size 10 /Root 1 0 R /Info 2 0 R
/ID [<58A499EFA8F9E47E6655F3DCF619573D><58A499EFA8F9E47E6655F3DCF619573D>]
>>
startxref
2095
%%EOF
```
From the first line of the result, we can know that this is a PNG file. We can also use the following command to get information about type.
```sh
file <FILE_PATH>
```
for example:
```
% file flag2of2-final.pdf
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced
```

Then we change its extension
```sh
mv flag2of2-final.pdf flag2of2-final.png
```
result
```
picoCTF{f1u3n7_
```
<img width="249" alt="截圖 2024-07-21 上午10 06 37" src="https://github.com/user-attachments/assets/9290a4a2-2c0a-409b-90ec-426ec77f2c67">

The flag is `picoCTF{f1u3n7_1n_pn9_&_pdf_1f991f77}`. BTW, there is a little hint "pn9_&_pdf" in the last part of flag XD

