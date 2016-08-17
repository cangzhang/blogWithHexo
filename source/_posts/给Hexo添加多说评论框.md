---
title: 给Hexo添加多说评论框
tags:
  - hexo
  - 折腾
date: 2014-08-22 21:17:17
---

在\themes\landscape\layout_partial\article.ejs添加如下代码

    <span class="vbscript">&lt;% <span class="keyword">if</span> (!index &amp;&amp; post.comments){ %&gt;</span>
    <span class="tag">&lt;<span class="title">section</span> <span class="attribute">id</span>=<span class="value">"comments"</span>&gt;</span>
      <span class="comment">&lt;!-- Duoshuo Comment BEGIN --&gt;</span>
      <span class="tag">&lt;<span class="title">div</span> <span class="attribute">class</span>=<span class="value">"ds-thread"</span>&gt;</span><span class="tag">&lt;/<span class="title">div</span>&gt;</span>
        <span class="tag">&lt;<span class="title">script</span> <span class="attribute">type</span>=<span class="value">"text/javascript"</span>&gt;</span><span class="javascript">
          <span class="keyword">var</span> duoshuoQuery = {short_name:<span class="string">"your_shortname"</span>};
            (<span class="function"><span class="keyword">function</span><span class="params">()</span> </span>{
              <span class="keyword">var</span> ds = <span class="built_in">document</span>.createElement(<span class="string">'script'</span>);
              ds.type = <span class="string">'text/javascript'</span>;ds.async = <span class="literal">true</span>;
              ds.src = <span class="string">'http://static.duoshuo.com/embed.js'</span>;
              ds.charset = <span class="string">'UTF-8'</span>;
              (<span class="built_in">document</span>.getElementsByTagName(<span class="string">'head'</span>)[<span class="number">0</span>]
              || <span class="built_in">document</span>.getElementsByTagName(<span class="string">'body'</span>)[<span class="number">0</span>]).appendChild(ds);
            })();
      </span><span class="tag">&lt;/<span class="title">script</span>&gt;</span>
    <span class="comment">&lt;!-- Duoshuo Comment END --&gt;</span>
    <span class="tag">&lt;/<span class="title">section</span>&gt;</span>
    <span class="vbscript">&lt;% } %&gt;</span>
    