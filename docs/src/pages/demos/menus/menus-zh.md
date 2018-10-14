---
title: React 菜单组件
components: Menu, MenuItem, MenuList, ClickAwayListener, Popover, Popper
---
# 菜单

<p class="description">菜单显示在临时出现的所点击位置上的选项列表。</p>

[菜单](https://material.io/design/components/menus.html)显示临时表面上的选择列表。

## 简单菜单

默认情况下, 简单菜单会在锚点元素上打开 (此选项可通过props更改)。当靠近屏幕边缘时, 简单菜单会垂直调整以使所有菜单项完全可见。

选择一个选项后, 最好立即提交该选项并关闭菜单。

**解疑**: 与简单菜单相比, 简单对话框可以显示与列表项可用选项相关的其他详细信息, 或提供导航或正交操作与主要任务相关。 虽然它们可以显示相同的内容, 但简单的菜单比简单的对话框更可取, 因为简单的菜单对用户当前上下文的破坏性较小。

{{"演示": "pages/demos/menus/SimpleMenu.js"}}

## 选择菜单

如果用于项目选择, 则在打开时, 简单菜单将尝试将当前选定的菜单项与定位元素垂直对齐。 当前选择的菜单项使用` selected `属性（从[ListItem](/api/list-item/))。

{{"演示": "pages/demos/menus/SimpleListMenu.js"}}

如果简单菜单中的文本覆盖到第二行，则使用简单对话框代替。简单对话框可以具有不同高度的行。

## 有最大高的菜单

如果菜单的高度阻止显示所有菜单项，则菜单可以在内部滚动

{{"演示": "pages/demos/menus/LongMenu.js"}}

## 菜单列表的组成

`Menu`组件内部使用`Popver`组件 但是，您可能希望使用不同的定位策略，或者不阻塞滚动。 为了满足这些需求，我们公开了一个`MenuList`组件，您可以使用这个示例中的`Popper`来编写该组件。

`MenuList`组件的主要职责是处理焦点。

{{"演示": "pages/demos/menus/MenuListComposition.js"}}

## 定制菜单项

`MenuItem`是 `ListItem`附带的一些附加样式的包装器。 可以使用`MenuItem`组件使用相同的列表组合特性：

{{"演示": "pages/demos/menus/ListItemComposition.js"}}

## 更改过渡动画

使用不同的过渡动画。

{{"演示": "pages/demos/menus/FadeMenu.js"}}

## Render Props

这是[render props](https://reactjs.org/docs/render-props.html) 的例子。跟踪单个菜单的本地状态。

{{"演示": "pages/demos/menus/RenderPropsMenu.js"}}