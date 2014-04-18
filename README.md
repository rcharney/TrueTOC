TrueTOC is a Javascript application that produces dynamically generated outline-numbered Tables of Content (TOC). The TOC can be based on heading levels or ordered list levels. For example, using headings:

<pre>
H1 Heading A     =>  1. Heading A
H1 Heading B     =>  2. Heading B
H2 Heading B.A   =>    2.1 Heading B.A
H2 Heading B.B   =>    2.2 Heading B.B
H1 Heading C     =>  3. Heading C
</pre>

TrueTOC is designed to be used with most HTML pages. It requires a minimum of 2 lines of Javascript inserted into your HEAD section of a HTML page . You can also determine where the Table of Contents (TOC) is to appear in your page and which part of your page should be numbered. TrueTOC includes its own CSS file that can be overridden by the page designer.

A default of 5 levels are included in the generated TOC. Up to 9 levels can be numbered.

Addition options include selecting which symbols represent expanded and collapsed levels. Toggling a symbol marker in the TOC will expand and collapse its content.
