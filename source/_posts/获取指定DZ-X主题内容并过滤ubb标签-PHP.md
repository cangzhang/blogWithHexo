---
title: '获取指定DZ!X主题内容并过滤ubb标签[PHP]'
tags:
  - PHP
  - 代码
date: 2014-08-22 19:55:09
---

代码如下：

        <span class="php"><span class="preprocessor">&lt;?php</span>
        <span class="function"><span class="keyword">function</span> <span class="title">capword</span><span class="params">()</span></span>{
        <span class="comment">//连接数据库</span>
        <span class="variable">$mysql_server_name</span>=<span class="string">'localhost'</span>; 
        <span class="variable">$mysql_username</span>=<span class="string">'root'</span>; 
        <span class="variable">$mysql_password</span>=<span class="string">'root'</span>;
        <span class="variable">$mysql_database</span>=<span class="string">'dz'</span>;

        <span class="variable">$conn</span>=mysql_connect(<span class="variable">$mysql_server_name</span>,<span class="variable">$mysql_username</span>,<span class="variable">$mysql_password</span>) <span class="keyword">or</span> <span class="keyword">die</span>(<span class="string">"error connecting"</span>) ; 
        mysql_query(<span class="string">"set names 'utf8'"</span>); 
        mysql_select_db(<span class="variable">$mysql_database</span>); 
        <span class="variable">$sql</span> =<span class="string">"SELECT message FROM pre_forum_post WHERE tid=1 and pid=1 and fid=2 and first=1 and invisible=0 "</span>;<span class="comment">//pid tid fid确定着具体主题，first代表一楼（即主贴内容）</span>
        <span class="variable">$result</span> = mysql_query(<span class="variable">$sql</span>,<span class="variable">$conn</span>) <span class="keyword">or</span> <span class="keyword">die</span>(<span class="string">'无法连接!'</span>.mysql_error);
        <span class="variable">$str</span>;

        <span class="comment">//将读取内容赋值$str,并进行过滤</span>
        <span class="keyword">while</span>( <span class="variable">$row</span> = mysql_fetch_array(<span class="variable">$result</span>) ){
            <span class="keyword">foreach</span>(<span class="variable">$row</span> <span class="keyword">as</span> <span class="variable">$value</span>){}
            <span class="variable">$str</span>=<span class="variable">$value</span>.<span class="string">''</span>;
            <span class="comment">//echo $str;</span>
            <span class="comment">//echo "&lt;br/&gt;";</span>
            <span class="variable">$str</span>=preg_replace(<span class="string">'/\[.*?\]/is'</span>, <span class="string">''</span>, <span class="variable">$str</span>);
            <span class="keyword">echo</span> substr(<span class="variable">$str</span>,<span class="number">0</span>,<span class="number">199</span>);<span class="comment">//指定输出长度</span>
        }   
        mysql_close(<span class="variable">$conn</span>);
    }
    <span class="preprocessor">?&gt;</span></span>
    