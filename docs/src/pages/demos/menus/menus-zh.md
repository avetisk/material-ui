---
title: React 菜单组件
components: 菜单, 菜单项, 菜单列表, 点击监听器, 弹出框, Popper
---
# 菜单

<p class="description">菜单显示在临时出现的所点击位置上的选项列表。</p>

[菜单](https://material.io/design/components/menus.html)显示临时表面上的选择列表。

## 简单菜单

默认情况下, 简单菜单会在锚点元素上打开 (此选项可通过props更改)。当靠近屏幕边缘时, 简单菜单会垂直调整以使所有菜单项完全可见。

选择一个选项后, 最好立即提交该选项并关闭菜单。

**解疑**: 与简单菜单相比, 简单对话框可以显示与列表项可用选项相关的其他详细信息, 或提供导航或正交操作与主要任务相关。 虽然它们可以显示相同的内容, 但简单的菜单比简单的对话框更可取, 因为简单的菜单对用户当前上下文的破坏性较小。

{{"演示": "pages/demos/menus/SimpleMenu.js"}}

## Selected menus

If used for item selection, when opened, simple menus attempt to vertically align the currently selected menu item with the anchor element. The currently selected menu item is set using the `selected` property (from [ListItem](/api/list-item/)).

{{"demo": "pages/demos/menus/SimpleListMenu.js"}}

If text in a simple menu wraps to a second line, use a simple dialog instead. Simple dialogs can have rows with varying heights.

## Max height menus

If the height of a menu prevents all menu items from being displayed, the menu can scroll internally.

{{"demo": "pages/demos/menus/LongMenu.js"}}

## MenuList composition

The `Menu` component uses the `Popover` component internally. However, you might want to use a different positioning strategy, or not blocking the scroll. For answering those needs, we expose a `MenuList` component that you can compose, with `Popper` in this example.

The primary responsibility of the `MenuList` component is to handle the focus.

{{"demo": "pages/demos/menus/MenuListComposition.js"}}

## Customized MenuItem

The `MenuItem` is a wrapper around `ListItem` with some additional styles. You can use the same list composition features with the `MenuItem` component:

{{"demo": "pages/demos/menus/ListItemComposition.js"}}

## Change Transition

Use a different transition altogether.

{{"demo": "pages/demos/menus/FadeMenu.js"}}

## Render Props

It is a [render props](https://reactjs.org/docs/render-props.html) demo that keeps track of the local state for a single menu.

{{"demo": "pages/demos/menus/RenderPropsMenu.js"}}