---
title: Markdown 문법
categories:
  - Blog
tags:
  - Markdown
thumbnail: /images/markdown.png
date: 2017-04-13 17:30:49
---
Markdown
========
Markdown은 복잡한 HTML 태그를 사용하지 않더라도 일반 텍스트만으로 문서 편집이 가능합니다. Markdown을 지원하는 환경이라면 어디서든 사용가능하고, 익숙해지면 형식화된 문서를 빠른시간에 효율적으로 작성이 가능합니다. 
<br>

<i id="index"></i>
## INDEX
***
* ** [제목 (Headers)](#headers)**
* ** [글꼴 (Text Style)](#text_style) **
* ** [인용 (Blockquotes)](#block)**
* ** [코드 블럭 (Code Blocks)](#code_block)**
* ** [인라인 코드 블럭 (Inline Code Blocks)](#inline_code_block)**
* ** [링크 (Links)](#link)**
* ** [리스트 (Lists)](#list)**
* ** [테이블 (Tables)](#table)**
* ** [이미지 (Images)](#image)**
* ** [각주 (Footnotes)](#footnote)**
***

</br>

<i id="headers"></i>
### 제목 (Headers)

-- 글자앞에 `#`을 붙이거나 글자밑에 `-`, `=` 적용
　`#`갯수에따라 H1 ~ H6까지 사이즈 조절

| Example 					| Output
| ------- 					| ------
| Headers </br> ====== 		| <h1>Headers</h1>
| Headers </br> --------- 	| <h2>Headers</h2>
| `# H1`   					| <h1>H1</h1>
| `## H2`   				| <h2>H2</h2>
| `### H3`   				| <h3>H3</h3>
| `#### H4`   				| <h4>H4</h4>
| `##### H5`   				| <h5>H5</h5>
| `###### H6`   			| <h6>H6</h6>

</br>

<i id="text_style"></i>
### 글꼴 (Text Style)
-- 글자 양옆에 적용

| Style 				| Syntax 		 | Example 						 | Output
| ----- 				| ------ 		 | ------- 						 | ------
| 굵게(Bold)			| `**` or `__`	 | `**Bold Example**` 		 	 | **Bold Example**
| 기울임(Italic) 		| `* *` or `_ _` | `_Italic Example_` 		 	 | _Italic Example_
| 취소선(Strikethrough) | `~~ ~~`		 | `~~Strikethrough Example~~` 	 | ~~Strikethrough Example~~

</br>

<i id="block"></i>
### 인용 (Blockquotes)
-- `>`를 사용하여 텍스트를 인용

| Example 					| Output
| ------- 					| ------
| `> Blockquotes Example` 	| <blockquote>Blockquotes Example</blockquote>
| `>> Blockquotes Example` 	| <blockquote>Blockquotes Example</blockquote> </br> <blockquote><blockquote>Blockquotes Example</blockquote></blockquote>

</br>

<i id="code_block"></i>
### 코드 블럭 (Code Block)
```java
echo "code block" > codeblock.log
function getCodeBlock() { return "code block"}
public class CodeBlock(){
	public CodeBlock();
}
```
| Example 								| Output
| ------- 								| ------
| \`\`\` </br> [내용] </br> \`\`\` 		| <figure class="highlight plain"><table><tbody><tr><td class="gutter"><pre><div class="line">1</div><div class="line">2</div><div class="line">3</div><div class="line">4</div><div class="line">5</div></pre></td><td class="code"><pre><div class="line">echo "code block" &gt; codeblock.log</div><div class="line">function getCodeBlock() { return "code block"}</div><div class="line">public class CodeBlock(){</div><div class="line">	public CodeBlock();</div><div class="line">}</div></pre></td></tr></tbody></table></figure>
| \~\~\~ </br> [내용] </br> \~\~\~		| <figure class="highlight plain"><table><tbody><tr><td class="gutter"><pre><div class="line">1</div><div class="line">2</div><div class="line">3</div><div class="line">4</div><div class="line">5</div></pre></td><td class="code"><pre><div class="line">echo "code block" &gt; codeblock.log</div><div class="line">function getCodeBlock() { return "code block"}</div><div class="line">public class CodeBlock(){</div><div class="line">	public CodeBlock();</div><div class="line">}</div></pre></td></tr></tbody></table></figure>
| \`\`\`bash </br> [내용] </br> \`\`\`	| <figure class="highlight bash"><table><tbody><tr><td class="gutter"><pre><div class="line">1</div><div class="line">2</div><div class="line">3</div><div class="line">4</div><div class="line">5</div></pre></td><td class="code"><pre><div class="line"><span class="built_in">echo</span> <span class="string">"code block"</span> &gt; codeblock.log</div><div class="line"><span class="keyword">function</span> <span class="function"><span class="title">getCodeBlock</span></span>() { <span class="built_in">return</span> <span class="string">"code block"</span>}</div><div class="line">public class <span class="function"><span class="title">CodeBlock</span></span>(){</div><div class="line">	public CodeBlock();</div><div class="line">}</div></pre></td></tr></tbody></table></figure>
| \`\`\`js </br> [내용] </br> \`\`\`	| <figure class="highlight js"><table><tbody><tr><td class="gutter"><pre><div class="line">1</div><div class="line">2</div><div class="line">3</div><div class="line">4</div><div class="line">5</div></pre></td><td class="code"><pre><div class="line">echo <span class="string">"code block"</span> &gt; codeblock.log</div><div class="line"><span class="function"><span class="keyword">function</span> <span class="title">getCodeBlock</span>(<span class="params"></span>) </span>{ <span class="keyword">return</span> <span class="string">"code block"</span>}</div><div class="line">public <span class="class"><span class="keyword">class</span> <span class="title">CodeBlock</span>()</span>{</div><div class="line">	public CodeBlock();</div><div class="line">}</div></pre></td></tr></tbody></table></figure>
| \`\`\`java </br> [내용] </br> \`\`\`	| <figure class="highlight java"><table><tbody><tr><td class="gutter"><pre><div class="line">1</div><div class="line">2</div><div class="line">3</div><div class="line">4</div><div class="line">5</div></pre></td><td class="code"><pre><div class="line">echo <span class="string">"code block"</span> &gt; codeblock.<span class="function">log</span></div><div class="line">function <span class="title">getCodeBlock</span><span class="params">()</span> { <span class="keyword">return</span> <span class="string">"code block"</span>}</div><div class="line"><span class="function"><span class="keyword">public</span> class <span class="title">CodeBlock</span><span class="params">()</span></span>{</div><div class="line">	<span class="function"><span class="keyword">public</span> <span class="title">CodeBlock</span><span class="params">()</span></span>;</div><div class="line">}</div></pre></td></tr></tbody></table></figure>

</br>

<i id="inline_code_block"></i>
### 인라인 코드 블럭 (Inline Code Block)

-- 글자 양옆에 ``(Block Quote)` 적용

| Example 					| Output
| ------- 					| ------
| \`inline code block\`		| `inline code block`

</br>

<i id="link"></i>
### 링크 (Link)

**1. _외부링크 (External Links)_**

| Type 			| Example 						 																			| Output
| ---- 			| ------- 						 																			| ------
| 인라인 링크	| `[인라인](http://wonmoyang.github.io "inline")` 															| [인라인](http://wonmoyang.github.io "inline")
| 참조   링크 	| `[Google][1]`</br>`[Naver][2]`</br>`[1]: http://google.com “구글”`</br>`[2]: http://naver.com "네이버”`	| <p><a href="http://google.com" title="google" target="_blank" rel="external">Google</a><br><a href="http://naver.com" title="naver" target="_blank" rel="external">Naver</a><br></p>
| URI    링크 	| `<http://wonmoyang.github.io>`</br>`<yangwm89@gmail.com>` 	 											| <http://wonmoyang.github.io></br><yangwm89@gmail.com>

**2. _내부링크 (Internal Links)_**

| Type 		| Example 					| Output
| ----	    | ------- 					| ------
| 목차 링크 | `[목차](#index)`		    | [목차](#index)

</br>

<i id="list"></i>
### 리스트 (Lists)

**1. _순서 리스트 (Ordered Lists)_**
  -- `1.`, `2.`와 같이 `숫자` + `.`을 이용하여 리스트를 구성.
　번호 순서에 상관없이 출력.

| Example 					| Output
| ------- 					| ------
| `3. 첫번째 리스트` </br> `4. 두번째 리스트` </br> `1. 세번째 리스트` </br> `2. 네번째 리스트`	|1. 첫번쨰 리스트</br>2. 두번째 리스트</br>3. 두번째 리스트</br>4. 두번째 리스트


**2. _ 글머리 리스트 (Unordered Lists)_**
  -- `*`, `+`, `-`을(를) 이용하여 리스트를 구성.
  
| Type   				    | Example 		   | Output
| ---- 					    | ------- 		   | ------
| `*`    				    | `* 글머리 리스트` | <ul><li>글머리 리스트</li></ul>
| `+`    				    | `+ 글머리 리스트` | <ul><li>글머리 리스트</li></ul>
| `-`    				    | `- 글머리 리스트` | <ul><li>글머리 리스트</li></ul>
| `-`    				    | `- 글머리 리스트` | <ul><li>글머리 리스트</li></ul>
| `응용 (다단계 리스트)`    | `* 리스트 1` </br> `+ 리스트 2` </br> 　`- 리스트 2-1` </br> 　`- 리스트 2-2` </br> 　　`- 리스트 2-2-1` </br> `* 리스트 3-1` | <ul><li>리스트 1</li><li>리스트 2<ul><li>리스트 2-1</li><li>리스트 2-2<ul><li>리스트 2-2-1</li></ul></li></ul></li><li>리스트 3</li></ul>

</br>

<i id="table"></i>
### 테이블 (Tables)
  -- `-` 와 `|` 을 사용하여 구성.
  　{% link markdown table generator http://www.tablesgenerator.com/markdown_tables# [external] [markdown table generator] %}에서 테이블 구성을 지원.

| Type   				    | Example 		   | Output
| ---- 					    | ------- 		   | ------
| `기본 테이블` 		    | &#124; column &#124; column &#124; column </br> &#124; --------- &#124; --------- &#124; --------- </br> &#124; row 1 &#124; row 1 &#124; row 1 | <table><thead><tr><th>column</th><th>column</th><th>column</th></tr></thead><tbody><tr><td>row 1</td><td>row 1</td><td>row 1 </td></tr><tr><td>row 2</td><td>row 2</td><td>row 2</td></tr></tbody></table>
| `정렬 테이블` 		    | &#124; column &#124; column &#124; column </br> &#124; :--------- &#124; :---------: &#124; ---------: </br> &#124; row 1 &#124; row 1 &#124; row 1 | <table><thead><tr><th style="text-align:left">column</th><th style="text-align:center">column</th><th style="text-align:right">column</th></tr></thead><tbody><tr><td style="text-align:left">row 1</td><td style="text-align:center">row 1</td><td style="text-align:right">row 1 </td></tr><tr><td style="text-align:left">row 2</td><td style="text-align:center">row 2</td><td style="text-align:right">row 2</td></tr></tbody></table>

</br>

<i id="image"></i>
### 이미지 (Images)

| Type   		    | Example 		   | Output
| ---- 				| ------- 		   | ------
| `인라인 이미지`	| `![alt title](/images/inline_image.jpg)` | ![inline_image](/images/inline_image.jpg)
| `링크 이미지`	    | `![alt title](https://wonmoyang.github.io/images/link_image.jpg)` | ![link_image](https://wonmoyang.github.io/images/link_image.jpg)
| `참조 이미지`	    | `![alt title][1]` </br> `[1]:/images/reference_image.png` | ![reference_image](/images/reference_image.png)

</br>