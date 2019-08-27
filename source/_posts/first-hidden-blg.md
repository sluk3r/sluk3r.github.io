---
title: first_hidden_blg
date: 2019-08-26 08:28:54
tags:
sage: true
---
****
总有些不想公开的文章。 这些文章想写出来， 但不想着让别人看到。 
这方面的典型内容有： 日记
至于不想公开的原因， 最概括的说，是时机还不到，未到需要公开的时候。后面某种机缘到位后， 就可以不再隐藏，公开出来请大家批判。 

这个功能，在Wordpress下已有。 本来嘛， 像Wordpress这样的动态博客管理工具，博客的隐藏与否，实现起来太简单了， 也太正常了。 

那么在Hexo中， 怎么实现呢？ 一顿搜索后， 找到下这样[插件](https://github.com/printempw/hexo-sage-posts). 接下来的这篇文章中，就作为一个使用体验， 记录下这个插件使用过程的经验和教训。 

注：下面的使用要点， 是本着精简的方式记录下， 没有配图， 如果大家有缘看到这篇文章的话， 在照方抓药使用过程中， 如有什么问题， 请移步这个[插件的官方文档](https://github.com/printempw/hexo-sage-posts), 那里有最权威的解释。 


1. 安装： 
   
   安装很简单， 使用命令“npm install hexo-sage-posts --save”. 即可安装。 

2. 使用： 

    新建一篇博客时， 在博客的开头设置；sage: true，

3. 配置：

    博客的全局配置文件_config.yml中， 添加如下内容： 
    ``` java
    # hexo-sage-posts
    sage_posts: 
        filter: hidden    # Change the filter name to fit your need
    ```

    上面的配置后， 博客首页和归档中，都看不到这篇被隐藏的文章了。 
    
    不赖。

4. 问题： 
   
   - 怎么列出隐藏的博客， 在这个插件的Github上， 给作者反馈了[Issue](https://github.com/printempw/hexo-sage-posts/issues/6), 后续再更进这个功能实现。 
   - 在使用中也发现，期望被隐藏的文章， 在“上一篇”和“下一篇”中， 会被露出。 针对这个问题， 看[Issue](https://github.com/printempw/hexo-sage-posts/issues/1)中有列到， 不过， 从Issue提到，到现在7个月过去了， 还没见到修复的动静。 可能需要大家先凑合着使用了。 接着再往下想一步， 自己是不是可以帮修复下这个问题， 然后提交给作者审核。 也算是参与开源的一个实际行动。 也借这个实际行动来感受下开源世界里协作方式。 
   - 隐藏文章的Toc不再显示。关于这点， 不知是正常的功能，还是Bug，也给作者提了[Issue](https://github.com/printempw/hexo-sage-posts/issues/7), 后续如有的更新后， 也会在这里同步出来。 
   - 能不能彻底隐藏某篇文章？ 即当隐藏的文章，被知道URL后，在浏览器里访问时， 也会给一个恰当的反馈， 而不是像现在一样，可以正常查看？ 这个问题也以[Issue](https://github.com/printempw/hexo-sage-posts/issues/8)方式反馈给作者。 

至此，安装使用过程记录完毕，虽有些小瑕疵， 但最核心的功能，还是完成了。 