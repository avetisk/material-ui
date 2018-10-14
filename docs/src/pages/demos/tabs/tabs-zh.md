---
title: React 选项卡组件
components: Tabs, Tab
---
# Tab选项卡

<p class="description">选项卡可以轻松浏览和切换不同的视图.</p>

[Tabs](https://material.io/design/components/tabs.html) organize and allow navigation between groups of content that are related and at the same level of hierarchy.

## 简单选项卡

一个简单例子

{{"demo": "pages/demos/tabs/SimpleTabs.js"}}

### Wrapped Labels

Long labels will automatically wrap on tabs. If the label is too long for the tab, it will overflow and the text will not be visible.

{{"demo": "pages/demos/tabs/TabsWrappedLabel.js"}}

### 禁用的选项卡

可以通过设置 `property` 属性来禁用选项卡>.

{{"demo": "pages/demos/tabs/DisabledTabs.js"}}

## 固定选项卡

Fixed tabs should be used with a limited number of tabs and when consistent placement will aid muscle memory.

### 100%宽度

The `fullWidth` property should be used for smaller views. This demo also uses [react-swipeable-views](https://github.com/oliviertassinari/react-swipeable-views) to animate the Tab transition, and allowing tabs to be swiped on touch devices.

{{"demo": "pages/demos/tabs/FullWidthTabs.js"}}

### 居中对齐

The `centered` property should be used for larger views.

{{"demo": "pages/demos/tabs/CenteredTabs.js"}}

## 可滚动的选项卡

### Automatic Scroll Buttons

Left and right scroll buttons will automatically be presented on desktop and hidden on mobile. (based on viewport width)

{{"demo": "pages/demos/tabs/ScrollableTabsButtonAuto.js"}}

### Forced Scroll Buttons

Left and right scroll buttons will be presented regardless of the viewport width.

{{"demo": "pages/demos/tabs/ScrollableTabsButtonForce.js"}}

### Prevent Scroll Buttons

Left and right scroll buttons will never be presented. All scrolling must be initiated through user agent scrolling mechanisms (e.g. left/right swipe, shift-mousewheel, etc.)

{{"demo": "pages/demos/tabs/ScrollableTabsButtonPrevent.js"}}

## 含图标的选项卡

Tab labels may be either all icons or all text.

{{"demo": "pages/demos/tabs/IconTabs.js"}} {{"demo": "pages/demos/tabs/IconLabelTabs.js"}}

## 自定义的选项卡

If you have read the [overrides documentation page](/customization/overrides/) but aren't confident jumping in, here's an example of how you can change the main color of the Tabs. The following demo matches the [Ant Design UI](https://ant.design/components/tabs/).

{{"demo": "pages/demos/tabs/CustomizedTabs.js"}}