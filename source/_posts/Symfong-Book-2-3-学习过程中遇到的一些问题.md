---
title: Symfong Book 2.3 学习过程中遇到的一些问题
tags:
  - symfony
date: 2015-05-15 21:54:30
---

*   问题一

书中P47中，4-7这处的代码：

    // src/Acme/DemoBundle/Controller/RandomController.php
    namespace Acme\DemoBundle\Controller;
    use Symfony\Component\HttpFoundation\Response;
    class RandomController
    {
    public function indexAction($limit)
    {
    return new Response(
    '&lt;html&gt;&lt;body&gt;Number: '.rand(1, $limit).'&lt;/body&gt;&lt;/html&gt;'
    );
    }
    }

应当在前后加入`&lt;?php ?&gt;`标签