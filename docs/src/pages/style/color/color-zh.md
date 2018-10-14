# 颜色

<p class="description">通过颜色传达意义。 开箱即用，您可以访问Material Design规范中的所有颜色。</p>

material design中的 [ 颜色 ](https://material.io/design/color/) 灵感源自与静音环境、深阴影和明亮亮点并列的粗色调。

## 颜色系统

Material Design 颜色系统可用于创建反映您的品牌或风格的颜色主题。

### Important Terms

#### "Palette"

调色板是颜色的集合, 即色调和它们的阴影. Material-UI 提供Material Design 指南中的所有颜色.

#### "Hue" & "Shade"

调色板中的单一颜色由色相如 "red" 和阴影如 "500"组成。 "rad 50" 是红色的最浅的阴影 (* 粉红色! *), 而 "red 900" 是最暗的。 此外, 大多数色调都带有强调色调, 以 ` A ` 为前缀。

### Examples

Material Design调色板包括主要和强调颜色, 可用于插图或开发您的品牌颜色. 他们被设计成彼此和谐地工作.

例如, 您可以参考互补的主要和强调颜色 (例如 "red 500" & "purple A200"), 如下所示:

```js
import purple from '@material-ui/core/colors/purple';
import red from '@material-ui/core/colors/red';

const primary = red[500]; // #F44336
const accent = purple['A200']; // #E040FB
const accent2 = purple.A200; // #E040FB (代替方法)
```

## Color tool

To test a [material.io/color](https://material.io/design/color/) color scheme with the Material-UI documentation, simply select colors using the palette and sliders below. Alternatively, you can enter hex values in the Primary and Secondary text fields.

{{"demo": "pages/style/color/ColorTool.js", "hideHeader": true}}

The output shown in the color sample can be pasted directly into a [`createMuiTheme()`](/customization/themes/#createmuitheme-options-theme) function (to be used with [`MuiThemeProvider`](/customization/themes/#theme-provider)):

```jsx
import { createMuiTheme } from '@material-ui/core/styles';
import purple from '@material-ui/core/colors/purple';

const theme = createMuiTheme({
  palette: {
    primary: purple,
    secondary: {
      main: '#f44336',
    },
  },
});
```

Only the `main` shades need be provided (unless you wish to further customise `light`, `dark` or `contrastText`), as the other colors will be calculated by `createMuiTheme()`, as described in the [Theme customization](/customization/themes/#palette) section.

If you are using the default primary and / or secondary shades then by providing the color object, `createMuiTheme()` will use the appropriate shades from the material color for main, light and dark.

### Official color tool

The Material Design team has also built an awesome palette configuration tool: [material.io/tools/color](https://material.io/tools/color/). This can help you create a color palette for your UI, as well as measure the accessibility level of any color combination.

<a href="https://material.io/tools/color/#!/?view.left=0&view.right=0&primary.color=3F51B5&secondary.color=F44336">
  <img src="/static/images/color/colorTool.png" alt="Official color tool" style="width: 574px" />
</a>

The output can be fed into `createMuiTheme()` function:

```jsx
import { createMuiTheme } from '@material-ui/core/styles';

const theme = createMuiTheme({
  palette: {
    primary: {
      light: '#757ce8',
      main: '#3f50b5',
      dark: '#002884',
      contrastText: '#fff',
    },
    secondary: {
      light: '#ff7961',
      main: '#f44336',
      dark: '#ba000d',
      contrastText: '#000',
    },
  },
});
```

### Tools by the community

- [create-mui-theme](https://react-theming.github.io/create-mui-theme/) Is an online tool for creating Material-UI themes via Material Design Color Tool.
- [material-ui-theme-editor](https://in-your-saas.github.io/material-ui-theme-editor/) A tool to generate themes for your Material-UI applications by just selecting the colors and having a live preview.

## Color palette

This color palette comprises primary and accent colors that can be used for illustration or to develop your brand colors. 他们被设计成彼此和谐地工作.

{{"demo": "pages/style/color/Color.js", "hideHeader": true}}