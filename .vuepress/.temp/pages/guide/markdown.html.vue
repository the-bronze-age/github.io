<template><div><p>VuePress 的每个文档页面都是由 Markdown 渲染而成。所以你需要通过在相应路径创建编写 Markdown 建立你的文档或博客页面。</p>
<!-- more -->
<h2 id="markdown-介绍" tabindex="-1"><a class="header-anchor" href="#markdown-介绍" aria-hidden="true">#</a> Markdown 介绍</h2>
<p>如果你是一个新手，还不会编写 Markdown，请先阅读 <a href="https://vuepress-theme-hope.github.io/v2/zh/basic/markdown/README.html" target="_blank" rel="noopener noreferrer">Markdown 介绍<ExternalLinkIcon/></a> 和 <a href="https://vuepress-theme-hope.github.io/v2/zh/basic/markdown/demo.html" target="_blank" rel="noopener noreferrer">Markdown 演示<ExternalLinkIcon/></a>。</p>
<div class="custom-container info"><p class="custom-container-title">Frontmatter</p>
<p>Frontmatter 是 VuePress 中很重要的一个概念，如果你不了解它，你需要阅读 <a href="https://vuepress-theme-hope.github.io/v2/zh/basic/vuepress/page.html#front-matter" target="_blank" rel="noopener noreferrer">Frontmatter 介绍<ExternalLinkIcon/></a>。</p>
</div>
<h2 id="vuepress-扩展" tabindex="-1"><a class="header-anchor" href="#vuepress-扩展" aria-hidden="true">#</a> VuePress 扩展</h2>
<p>为了丰富文档写作，VuePress 对 Markdown 语法进行了扩展。</p>
<p>关于这些扩展，请阅读 <a href="https://vuepress-theme-hope.github.io/v2/zh/basic/vuepress/markdown.html" target="_blank" rel="noopener noreferrer">VuePress 中的 Markdown 扩展<ExternalLinkIcon/></a>。</p>
<h2 id="主题扩展" tabindex="-1"><a class="header-anchor" href="#主题扩展" aria-hidden="true">#</a> 主题扩展</h2>
<h3 id="一键启用" tabindex="-1"><a class="header-anchor" href="#一键启用" aria-hidden="true">#</a> 一键启用</h3>
<p>你可以设置在主题选项中设置 <code v-pre>plugins.mdEnhance.enableAll: true</code> 启用 <a href="https://vuepress-theme-hope.github.io/v2/md-enhance" target="_blank" rel="noopener noreferrer">md-enhance<ExternalLinkIcon/></a> 插件的所有功能。</p>
<div class="language-javascript ext-js line-numbers-mode"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> <span class="token punctuation">{</span> hopeTheme <span class="token punctuation">}</span> <span class="token operator">=</span> <span class="token function">require</span><span class="token punctuation">(</span><span class="token string">"vuepress-theme-hope"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>

module<span class="token punctuation">.</span>exports <span class="token operator">=</span> <span class="token punctuation">{</span>
  <span class="token literal-property property">theme</span><span class="token operator">:</span> <span class="token function">hopeTheme</span><span class="token punctuation">(</span><span class="token punctuation">{</span>
    <span class="token literal-property property">plugins</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token literal-property property">mdEnhance</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token literal-property property">enableAll</span><span class="token operator">:</span> <span class="token boolean">true</span><span class="token punctuation">,</span>
      <span class="token punctuation">}</span><span class="token punctuation">,</span>
    <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">,</span>
<span class="token punctuation">}</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><h3 id="自定义容器" tabindex="-1"><a class="header-anchor" href="#自定义容器" aria-hidden="true">#</a> 自定义容器</h3>
<p>::: v-pre</p>
<p>安全的在 Markdown 中使用 {{ variable }}。</p>
<p>:::</p>
<div class="custom-container info"><p class="custom-container-title">自定义标题</p>
<p>信息容器，包含 <code v-pre>代码</code> 与 <a href="#markdown">链接</a>。</p>
<div class="language-javascript ext-js line-numbers-mode"><pre v-pre class="language-javascript"><code><span class="token keyword">const</span> a <span class="token operator">=</span> <span class="token number">1</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div></div>
<div class="custom-container tip"><p class="custom-container-title">自定义标题</p>
<p>提示容器</p>
</div>
<div class="custom-container warning"><p class="custom-container-title">自定义标题</p>
<p>警告容器</p>
</div>
<div class="custom-container danger"><p class="custom-container-title">自定义标题</p>
<p>危险容器</p>
</div>
<details class="custom-container details"><summary>自定义标题</summary>
<p>详情容器</p>
</details>
<details class="custom-container details"><summary>代码</summary>
<div class="language-markdown ext-md line-numbers-mode"><pre v-pre class="language-markdown"><code>::: v-pre

安全的在 Markdown 中使用 {{ variable }}。

:::

::: info 自定义标题

信息容器

:::

::: tip 自定义标题

提示容器

:::

::: warning 自定义标题

警告容器

:::

::: danger 自定义标题

危险容器

:::

::: details 自定义标题

详情容器

:::
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div></details>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/container.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="代码块" tabindex="-1"><a class="header-anchor" href="#代码块" aria-hidden="true">#</a> 代码块</h3>
<p>::: code-tabs</p>
<p>@tab pnpm</p>
<div class="language-bash ext-sh line-numbers-mode"><pre v-pre class="language-bash"><code><span class="token function">pnpm</span> <span class="token function">add</span> -D vuepress-theme-hope
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>@tab yarn</p>
<div class="language-bash ext-sh line-numbers-mode"><pre v-pre class="language-bash"><code><span class="token function">yarn</span> <span class="token function">add</span> -D vuepress-theme-hope
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>@tab:active npm</p>
<div class="language-bash ext-sh line-numbers-mode"><pre v-pre class="language-bash"><code><span class="token function">npm</span> i -D vuepress-theme-hope
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div></div></div><p>:::</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/code-tabs.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="自定义对齐" tabindex="-1"><a class="header-anchor" href="#自定义对齐" aria-hidden="true">#</a> 自定义对齐</h3>
<p>::: center</p>
<p>我是居中的</p>
<p>:::</p>
<p>::: right</p>
<p>我在右对齐</p>
<p>:::</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/align.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="上下角标" tabindex="-1"><a class="header-anchor" href="#上下角标" aria-hidden="true">#</a> 上下角标</h3>
<p>19<sup>th</sup> H<sub>2</sub>O</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/sup-sub.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="脚注" tabindex="-1"><a class="header-anchor" href="#脚注" aria-hidden="true">#</a> 脚注</h3>
<p>此文字有脚注<sup class="footnote-ref"><a href="#footnote1">[1]</a><a class="footnote-anchor" id="footnote-ref1" /></sup>.</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/footnote.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="标记" tabindex="-1"><a class="header-anchor" href="#标记" aria-hidden="true">#</a> 标记</h3>
<p>你可以标记 <mark>重要的内容</mark> 。</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/mark.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="任务列表" tabindex="-1"><a class="header-anchor" href="#任务列表" aria-hidden="true">#</a> 任务列表</h3>
<ul>
<li>
<p>[x] 计划 1</p>
</li>
<li>
<p>[ ] 计划 2</p>
</li>
<li>
<p><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/tasklist.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></p>
</li>
</ul>
<h3 id="图表" tabindex="-1"><a class="header-anchor" href="#图表" aria-hidden="true">#</a> 图表</h3>
<p>::: chart 一个散点图案例</p>
<div class="language-json ext-json line-numbers-mode"><pre v-pre class="language-json"><code><span class="token punctuation">{</span>
  <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"scatter"</span><span class="token punctuation">,</span>
  <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"datasets"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
      <span class="token punctuation">{</span>
        <span class="token property">"label"</span><span class="token operator">:</span> <span class="token string">"散点数据集"</span><span class="token punctuation">,</span>
        <span class="token property">"data"</span><span class="token operator">:</span> <span class="token punctuation">[</span>
          <span class="token punctuation">{</span> <span class="token property">"x"</span><span class="token operator">:</span> <span class="token number">-10</span><span class="token punctuation">,</span> <span class="token property">"y"</span><span class="token operator">:</span> <span class="token number">0</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token punctuation">{</span> <span class="token property">"x"</span><span class="token operator">:</span> <span class="token number">0</span><span class="token punctuation">,</span> <span class="token property">"y"</span><span class="token operator">:</span> <span class="token number">10</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token punctuation">{</span> <span class="token property">"x"</span><span class="token operator">:</span> <span class="token number">10</span><span class="token punctuation">,</span> <span class="token property">"y"</span><span class="token operator">:</span> <span class="token number">5</span> <span class="token punctuation">}</span><span class="token punctuation">,</span>
          <span class="token punctuation">{</span> <span class="token property">"x"</span><span class="token operator">:</span> <span class="token number">0.5</span><span class="token punctuation">,</span> <span class="token property">"y"</span><span class="token operator">:</span> <span class="token number">5.5</span> <span class="token punctuation">}</span>
        <span class="token punctuation">]</span><span class="token punctuation">,</span>
        <span class="token property">"backgroundColor"</span><span class="token operator">:</span> <span class="token string">"rgb(255, 99, 132)"</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">]</span>
  <span class="token punctuation">}</span><span class="token punctuation">,</span>
  <span class="token property">"options"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
    <span class="token property">"scales"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
      <span class="token property">"x"</span><span class="token operator">:</span> <span class="token punctuation">{</span>
        <span class="token property">"type"</span><span class="token operator">:</span> <span class="token string">"linear"</span><span class="token punctuation">,</span>
        <span class="token property">"position"</span><span class="token operator">:</span> <span class="token string">"bottom"</span>
      <span class="token punctuation">}</span>
    <span class="token punctuation">}</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>:::</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/chart.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="流程图" tabindex="-1"><a class="header-anchor" href="#流程图" aria-hidden="true">#</a> 流程图</h3>
<div class="language-flow ext-flow line-numbers-mode"><pre v-pre class="language-flow"><code>cond<span class="token operator">=></span>condition<span class="token operator">:</span> 是否执行操作<span class="token operator">?</span>
process<span class="token operator">=></span>operation<span class="token operator">:</span> 操作
e<span class="token operator">=></span>end<span class="token operator">:</span> 结束

<span class="token function">cond</span><span class="token punctuation">(</span>yes<span class="token punctuation">)</span><span class="token operator">-</span><span class="token operator">></span>process<span class="token operator">-</span><span class="token operator">></span>e
<span class="token function">cond</span><span class="token punctuation">(</span>no<span class="token punctuation">)</span><span class="token operator">-</span><span class="token operator">></span>e
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/flowchart.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="mermaid" tabindex="-1"><a class="header-anchor" href="#mermaid" aria-hidden="true">#</a> Mermaid</h3>
<div class="language-mermaid ext-mermaid line-numbers-mode"><pre v-pre class="language-mermaid"><code><span class="token keyword">flowchart</span> TB
    c1<span class="token arrow operator">--></span>a2
    <span class="token keyword">subgraph</span> one
    a1<span class="token arrow operator">--></span>a2
    <span class="token keyword">end</span>
    <span class="token keyword">subgraph</span> two
    b1<span class="token arrow operator">--></span>b2
    <span class="token keyword">end</span>
    <span class="token keyword">subgraph</span> three
    c1<span class="token arrow operator">--></span>c2
    <span class="token keyword">end</span>
    one <span class="token arrow operator">--></span> two
    three <span class="token arrow operator">--></span> two
    two <span class="token arrow operator">--></span> c2
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/mermaid.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="tex-语法" tabindex="-1"><a class="header-anchor" href="#tex-语法" aria-hidden="true">#</a> Tex 语法</h3>
<p>$$
\frac {\partial^r} {\partial \omega^r} \left(\frac {y^{\omega}} {\omega}\right)
= \left(\frac {y^{\omega}} {\omega}\right) \left{(\log y)^r + \sum_{i=1}^r \frac {(-1)^i r \cdots (r-i+1) (\log y)^{r-i}} {\omega^i} \right}
$$</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/tex.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="代码演示" tabindex="-1"><a class="header-anchor" href="#代码演示" aria-hidden="true">#</a> 代码演示</h3>
<p>::: normal-demo 一个普通 Demo</p>
<div class="language-html ext-html line-numbers-mode"><pre v-pre class="language-html"><code><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>h1</span><span class="token punctuation">></span></span>VuePress Theme Hope<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>h1</span><span class="token punctuation">></span></span>
<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>p</span><span class="token punctuation">></span></span><span class="token tag"><span class="token tag"><span class="token punctuation">&lt;</span>span</span> <span class="token attr-name">id</span><span class="token attr-value"><span class="token punctuation attr-equals">=</span><span class="token punctuation">"</span>very<span class="token punctuation">"</span></span><span class="token punctuation">></span></span>非常<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>span</span><span class="token punctuation">></span></span>强大!<span class="token tag"><span class="token tag"><span class="token punctuation">&lt;/</span>p</span><span class="token punctuation">></span></span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div></div></div><div class="language-javascript ext-js line-numbers-mode"><pre v-pre class="language-javascript"><code>document<span class="token punctuation">.</span><span class="token function">querySelector</span><span class="token punctuation">(</span><span class="token string">"#very"</span><span class="token punctuation">)</span><span class="token punctuation">.</span><span class="token function">addEventListener</span><span class="token punctuation">(</span><span class="token string">"click"</span><span class="token punctuation">,</span> <span class="token punctuation">(</span><span class="token punctuation">)</span> <span class="token operator">=></span> <span class="token punctuation">{</span>
  <span class="token function">alert</span><span class="token punctuation">(</span><span class="token string">"非常强大"</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token punctuation">}</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><div class="language-css ext-css line-numbers-mode"><pre v-pre class="language-css"><code><span class="token selector">span</span> <span class="token punctuation">{</span>
  <span class="token property">color</span><span class="token punctuation">:</span> red<span class="token punctuation">;</span>
<span class="token punctuation">}</span>
</code></pre><div class="line-numbers" aria-hidden="true"><div class="line-number"></div><div class="line-number"></div><div class="line-number"></div></div></div><p>:::</p>
<ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/demo.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<h3 id="幻灯片" tabindex="-1"><a class="header-anchor" href="#幻灯片" aria-hidden="true">#</a> 幻灯片</h3>
<Presentation id="presentation-64a567b4" data-code="%0A%23%23%20%E5%B9%BB%E7%81%AF%E7%89%87%201%0A%0A%E4%B8%80%E4%B8%AA%E6%9C%89%E6%96%87%E5%AD%97%E5%92%8C%20%5B%E9%93%BE%E6%8E%A5%5D(https%3A%2F%2Fmrhope.site)%20%E7%9A%84%E6%AE%B5%E8%90%BD%0A%0A---%0A%0A%23%23%20%E5%B9%BB%E7%81%AF%E7%89%87%202%0A%0A-%20%E9%A1%B9%E7%9B%AE%201%0A-%20%E9%A1%B9%E7%9B%AE%202%0A%0A---%0A%0A%23%23%20%E5%B9%BB%E7%81%AF%E7%89%87%203.1%0A%0A%60%60%60js%0Aconst%20a%20%3D%201%3B%0A%60%60%60%0A%0A--%0A%0A%23%23%20%E5%B9%BB%E7%81%AF%E7%89%87%203.2%0A%0A%24%24%0AJ(%5Ctheta_0%2C%5Ctheta_1)%20%3D%20%5Csum_%7Bi%3D0%7D%0A%24%24%0A" theme="auto"></Presentation><ul>
<li><a href="https://vuepress-theme-hope.github.io/v2/zh/guide/markdown/presentation.html" target="_blank" rel="noopener noreferrer">查看详情<ExternalLinkIcon/></a></li>
</ul>
<hr class="footnotes-sep">
<section class="footnotes">
<ol class="footnotes-list">
<li id="footnote1" class="footnote-item"><p>这是脚注内容 <a href="#footnote-ref1" class="footnote-backref">↩︎</a></p>
</li>
</ol>
</section>
</div></template>
