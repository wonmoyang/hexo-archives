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
=======
Markdown은 복잡한 HTML 태그를 사용하지 않더라도 일반 텍스트만으로 문서 편집이 가능합니다. Markdown을 지원하는 환경이라면 어디서든 사용가능하고, 익숙해지면 형식화된 문서를 빠른시간에 효율적으로 작성이 가능합니다. 
<br>

***
* ** [제목 (Headers)](#headers)**
* ** [글꼴 (Text Style)](#text_style) **
* ** [인용 (Blockquotes)](#block)**
* ** [코드 블럭 (Code Blocks)](#code_block)**
* ** [인라인 코드 블럭 (Inline Code Blocks)](#inline_code_block)**
* ** [링크 (Links)](#link)**
***

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

-- 외부링크 (External Links)

[Google][1]</br>[Naver][2]</br>
[1]: http://example.com/ "링크제목1"
[2]: http://example.org/ "링크제목2"


| Type 			| Example 						 																			| Output
| ---- 			| ------- 						 																			| ------
| 인라인 링크	| `[인라인](http://wonmoyang.github.io "inline")` 															| [인라인](http://wonmoyang.github.io "inline")
| 참조   링크 	| `[Google][1]`</br>`[Naver][2]`</br>`[1]: http://google.com “구글”`</br>`[2]: http://naver.com "네이버”`	| <p><a href="http://google.com" title="google" target="_blank" rel="external">Google</a><br><a href="http://naver.com" title="naver" target="_blank" rel="external">Naver</a><br></p>
| URI    링크 	| `<http://wonmoyang.github.io>`</br>`<yangwm89@gmail.com>` 	 											| <http://wonmoyang.github.io></br><yangwm89@gmail.com>