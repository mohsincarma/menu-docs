# Usage

### To render manage menu page. It's used in admin panel.

```php
{!! manage_rv_menu() !!}
```

### To display menu in front site.

Click on "Preview" button and copy sample code to display menu. It will looks like below code.

+ PHP
```php
echo rv_render_menu('1516976222', [
    'container_id' => '',
    'container_class' => 'collapse navbar-collapse',
    'container_tag' => 'nav',
    'id' => '',
    'class' => 'nav navbar-nav navbar-right',
    'has_sub_class' => 'dropdown',
    'group_tag' => 'ul',
    'child_tag' => 'li',
    'submenu_class' => 'sub-menu',
    'item_class' => '',
    'active_class' => 'active current-menu-item',
]);
```

+ CSS
```css
.sample-menu, .sample-menu ul {
    list-style: none;
    margin: 0 !important;
    padding: 0;
}
.sample-menu {
    font-size: 12px;
    width: 100%;
    float: left;
    margin-bottom: 20px;
}
.sample-menu li {
    float: left;
    position: relative;
}
.sample-menu li a {
    display: block;
    height: 2.9em;
    line-height: 2.9em !important;
    padding: 0 1.4em !important;
}
.sample-menu ul {
    position: absolute;
    left: 0;
    top: 2.9em;
    display: none;
    z-index: 999;
    width: 160px;
}
.sample-menu ul ul {
    top: 0;
    left: 160px;
}
.sample-menu ul li {
    width: 100%;
}
.sample-menu ul li a {
    overflow: hidden;
}
.sample-menu li:hover > ul {
    display: block;
}
.sample-menu li.menu-item-has-children > a {
    background-image: url(/vendor/menu/images/arrow-right2.gif);
    background-position: right center;
    background-repeat: no-repeat;
    margin-right: 1em;
}
.sample-menu > li.menu-item-has-children > a {
    background-image: url(/vendor/menu/images/arrow-down2.gif);
}

.sample-menu, .sample-menu ul {
    -webkit-box-shadow: 2px 3px 0 rgba(150, 150, 150, 0.1);
    -moz-box-shadow: 2px 3px 0 rgba(150, 150, 150, 0.1);
    box-shadow: 2px 3px 0 rgba(150, 150, 150, 0.1);
}
.sample-menu > li > ul {
    margin-left: -1px;
}
.sample-menu ul ul {
    margin-top: -1px;
}
.sample-menu li ul li:last-child {
    border-bottom: none;
}

/* sample-menu white
-----------------------------------*/
.sample-menu, .sample-menu ul {
    border: 1px solid #ccc;
}
.sample-menu, .sample-menu li {
    background: #fff;
    background: -webkit-gradient(linear, 0 0, 0 bottom, from(#fff), to(#f1f1f1));
    background: -moz-linear-gradient(#fff, #f1f1f1);
    background: linear-gradient(#fff, #f1f1f1);
}
.sample-menu > li {
    border-right: 1px solid #ccc;
}
.sample-menu li a {
    color: #444;
    background-color: transparent !important;
    text-decoration: none !important;
}
.sample-menu li:hover {
    background: #fff;
}
.sample-menu li:hover > a {
    color: #36c6d3;
}
.sample-menu ul li {
    border-bottom: 1px solid #ddd;
}
.sample-menu li.menu-item-has-children > a {
    background-image: url(/vendor/menu/images/arrow-right1.gif);
}
.sample-menu > li.menu-item-has-children > a {
    background-image: url(/vendor/menu/images/arrow-down1.gif);
}
```