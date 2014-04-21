<p>TrueTOC is a Javascript application that produces dynamically generated outline-numbered Tables of Content (TOC). The TOC can be based on heading levels or ordered list levels. For example, using headings:</p>
<pre><code>
H1 Heading A     =>  1. Heading A
H1 Heading B     =>  2. Heading B
H2 Heading B.A   =>    2.1 Heading B.A
H2 Heading B.B   =>    2.2 Heading B.B
H1 Heading C     =>  3. Heading C
</code></pre>
<p>TrueTOC is designed to be used with most HTML pages. It requires a minimum of 2 lines of Javascript inserted into your HEAD section of a HTML page . You can also determine where the Table of Contents (TOC) is to appear in your page and which part of your page should be numbered. TrueTOC includes its own CSS file that can be overridden by the page designer.</p>
<p>A default of 5 levels are included in the generated TOC. Up to 9 levels can be numbered.</p>
<p>Addition options include selecting which symbols represent expanded and collapsed levels. Toggling a symbol marker in the TOC will expand and collapse its content.</p>
<p>The TrueTOC.js library is developed by <a href="http://almende.com">MariusL</a>.</p>
<h2><a name="user-content-install" class="anchor" href="#install">
<span class="octicon octicon-link"></span></a>Install</h2>
<p>Install via npm:</p>
<pre><code>npm install TrueTOC</code></pre>

<p>Or download the library from the github project:
<a href="https://github.com/rcharney/TrueTOC">https://github.com/rcharney/TrueTOC</a>.</p>

<h2><a name="user-content-load" class="anchor" href="#load"><span class="octicon octicon-link"></span></a>Load</h2>

<p>To use a component, include the javascript and css files of TrueTOC in your web page:</p>

<div class="highlight highlight-html"><pre><span class="cp">&lt;!DOCTYPE HTML&gt;</span>
<span class="nt">&lt;html&gt;</span>
<span class="nt">&lt;head&gt;</span>
  <span class="nt">&lt;script </span><span class="na">src=</span><span class="s">"TrueTOC.js"</span><span class="nt">&gt;&lt;/script&gt;</span>
  <span class="nt">&lt;link</span> <span class="na">href=</span><span class="s">"TrueTOC.css"</span><span class="nt">&gt;&lt;/script&gt;</span>
<span class="nt">&lt;/head&gt;</span>
<span class="nt">&lt;body&gt;</span>
<span class="nt">&lt;div</span> <span class="na">id=</span><span class="s">...content of page...</span><span class="nt">&gt;&lt;/div&gt;</span>
<span class="nt">&lt;/body&gt;</span>
<span class="nt">&lt;/html&gt;</span>
</pre></div>

<h2>
<a name="user-content-example" class="anchor" href="#example"><span class="octicon octicon-link"></span></a>Example</h2>

<p>A basic example using TrueTOC is shown below.</p>

<div class="highlight highlight-html"><pre><span class="cp">&lt;!DOCTYPE HTML&gt;</span>
<span class="nt">&lt;html&gt;</span>
<span class="nt">&lt;head&gt;</span>
  <span class="nt">&lt;title&gt;</span>TrueTOC basic demo<span class="nt">&lt;/title&gt;&lt;</span>
  <span class="nt">&lt;script </span><span class="na">src=</span><span class="s">"jquery-2.0.3.min.js"</span> <span class="na">type="text/javascript"&gt;&lt;/script&gt;</span>
  <span class="nt">&lt;link</span> <span class="na">href=</span><span class="s">"TrueTOC.css"</span> <span class="na">rel=</span><span class="s">"stylesheet"</span> <span class="na">type=</span><span class="s">"text/css"</span><span class="nt">/&gt;</span>
  <span class="nt">&lt;style </span><span class="na">type=</span><span class="s">"text/css"</span><span class="nt">&gt;</span>
  <span class="nt">&nbsp;&nbsp;#TrueTOC-placeholder</span> <span class="p">{</span><span class="k"> background</span><span class="o">:</span><span class="k">lightgray</span><span class="p">;</span><span class="p"> }</span>
  <span class="nt">&lt;/style&gt;</span>
<span class="nt">&lt;/head&gt;</span>
<span class="nt">&lt;body&gt;</span>
  &lt;div id="TrueTOC-placeholder"&gt;&nbsp;&lt;/div&gt;
  &lt;div id="TrueTOC-content"&gt;
  &lt;h1&gt;L1 a level 1 heading&lt;/h1&gt;
  &lt;p&gt;Text at level 1.&lt;/p&gt;
&lt;h2&gt;L2 a level 2 heading&lt;/h2&gt; 
&lt;p&gt;Some text at level 2.&lt;/p&gt;

&lt;h1&gt;L1 a level 1 heading&lt;/h1&gt;
&lt;p&gt;More level 1 text. &lt;/p&gt;
&lt;h2&gt;L2 a level 2 heading&lt;/h2&gt; 
&lt;ol&gt;
	&lt;li&gt;Item 1 at level 2.&lt;/li&gt; 
	&lt;li&gt;Item 2 at level 2.&lt;/li&gt; 
	&lt;li&gt;Item 3 at level 2.&lt;/li&gt;
&lt;/ol&gt;
&lt;p&gt;Additional text at level 2.&lt;/p&gt;
&lt;h2&gt;L2 a level 2 heading&lt;/h2&gt; 
&lt;p&gt;More text at level 2.&lt;/p&gt;
&lt;h3&gt;L3 a level 3 heading&lt;/h3&gt;
&lt;p&gt;Text at level 3&lt;/p&gt;
&lt;h3&gt;L3 a level 3 heading&lt;/h3&gt; &lt;p&gt;More text at level 3.&lt;/p&gt;
&lt;h3&gt;L3 a level 3 heading&lt;/h3&gt; 
&lt;h4&gt;L4 a level 4 heading&lt;/h4&gt;
&lt;h4&gt;L4 a level 4 heading&lt;/h4&gt;
&lt;h4&gt;L4 a level 4 heading&lt;/h4&gt; 
&lt;p&gt;Text at level 4.&lt;/p&gt;
&lt;h5&gt;L5 a level 5 heading&lt;/h5&gt;
&lt;p&gt;Some more text at level 5.&lt;/p&gt; 
&lt;h5&gt;L5 a level 5 heading&lt;/h5&gt;
&lt;p&gt;Additional text a level 5.&lt;/p&gt;
&lt;ol&gt;
	&lt;li&gt;Item 1 at level 5.&lt;/li&gt;
	&lt;li&gt;Item 2 at level 5.&lt;/li&gt;
	&lt;li&gt;Item 3 at level 5.&lt;/li&gt;
&lt;/ol&gt;
&lt;h2&gt;L2 a level 2 heading&lt;/h2&gt;
&lt;p&gt;Text at level 2.&lt;/p&gt; 
&lt;h5&gt;This heading should be at level 3&lt;/h5&gt;
&lt;p&gt;Text at level 3.&lt;/p&gt;
&lt;h5&gt;This heading should be at level 3 &lt;/h5&gt;
&lt;p&gt;More text a level 3.&lt;/p&gt;
  &lt;h1&gt;L1 a heading at level 1&lt;/h1&gt;
  &lt;p&gt;Text at level 1.&lt;/p&gt;
  &lt;h2 style="background-color:silver;height:22px" title="Empty heading"&gt;&lt;/h2&gt;
&lt;/div&gt;
&lt;/div&gt;</span>
<span class="nt">&lt;/body&gt;</span>
<span class="nt">&lt;/html&gt;</span>
</pre></div>

<h2>
<a name="user-content-build" class="anchor" href="#build"><span class="octicon octicon-link"></span></a>Build</h2>

<p>To build the library from source, clone the project from github</p>

<pre><code>git clone git://github.com/TrueTOC/TrueTOC.git
</code></pre>

<p>The project uses <a href="https://github.com/mde/jake">jake</a> as build tool.
The build script uses <a href="http://browserify.org/">Browserify</a> to
bundle the source code into a library,
and uses <a href="http://lisperator.net/uglifyjs/">UglifyJS</a> to minify the code.
The source code uses the module style of node (require and module.exports) to
organize dependencies.</p>

<p>To install all dependencies and build the library, run <code>npm install</code> in the
root of the project.</p>

<pre><code>cd TrueTOC
npm install
</code></pre>

<p>Then, the project can be build running:</p>

<pre><code>npm run build
</code></pre>

<h2><a name="user-content-test" class="anchor" href="#test"><span class="octicon octicon-link"></span></a>Test</h2>
span class="na">
<p>To test this library, install the project dependencies once:</p>

<pre><code>npm install</code></pre>

<p>Then run the tests:</p>

<pre><code>npm tests</code></pre>

<h2><a name="user-content-license" class="anchor" href="#license"><span class="octicon octicon-link"></span></a>License</h2>

<p>Copyright (C) 2014 WizOf.Biz</p>

<p>Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at</p>

<p><a href="http://www.apache.org/licenses/LICENSE-2.0">http://www.apache.org/licenses/LICENSE-2.0</a></p>

<p>Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.</p></article>
