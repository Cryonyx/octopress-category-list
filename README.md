Tag Cloud for Octopress
=======================

Fixed Problem
-------------
最新版的Octopress已经支持中文tag与category

修复了在最新版的Octopress下使用本插件导致的中文category链接无法正常被转换为拼音的bug



Description:
------------
Easy output tag cloud and category list.

Files:
------

    .
    ├─ plugins/
    │  └── category_list.rb
    └─ source/
       └─ _includes/
          └─ custom/
             └─ asides/
                ├─ category_list.html
                └─ category_cloud.html

Syntax:
-------

    {% category_cloud [counter:true] %}
    {% category_list [counter:true] %}

Example:
--------

In some template files, you can add the following markups.

### source/_includes/custom/asides/category_cloud.html ###

    <section>
      <h1>Tag Cloud</h1>
        <span id="tag-cloud">{% category_cloud %}</span>
    </section>

### source/_includes/custom/asides/category_list.html ###

    <section>
      <h1>Categories</h1>
        <ul id="category-list">{% category_list counter:true %}</ul>
    </section>

alswl 的改进
---------

支持 utf-8，使用 `category_cloud` 替换 `tag_cloud` ，
以避免和 [真正的标签云](https://github.com/robbyedwards/octopress-tag-cloud) 冲突。

Notes:
------
Be sure to insert above template files into `default_asides` array in `_config.yml`.
And also you can define styles for 'tag-cloud' or 'category-list' in a `.scss` file.
(ex: `sass/custom/_styles.scss`)

Licence:
--------
Distributed under the [MIT License][MIT].

[MIT]: http://www.opensource.org/licenses/mit-license.php
