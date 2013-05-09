DSizerListView
==========================

It adds a items-per-page size switcher in CListView widget in Yii

Readme
------------

[README RUS](http://www.elisdn.ru/blog/43/various-pagesize-for-clistview)

Installation
------------

Extract to `protected/components`.

Usage example
-------------

Use `DSizerListView` instead of `zii.widgets.CListView` and add a placeholder `{sizer}` into a template string:

~~~
[php]
<?php $this->widget('DSizerListView', array(
    'dataProvider'=>$dataProvider,
    'itemView'=>'_view',
    'template'=>"{sizer}\n{summary}\n{items}\n{pager}",
    'sizerVariants'=>array(10, 20, 30),
    'sizerAttribute'=>'size',
    'sizerCssClass'=>'sorter',
    'sizerHeader'=>'Show per page: ',
)); ?>
~~~

We deliberately use a CSS class 'sorter', because the sizer HTML code and the sorter HTML code are some.