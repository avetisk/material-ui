---
title: Text Field React component
components: FilledInput, FormControl, FormHelperText, Input, InputAdornment, InputBase, InputLabel, OutlinedInput, TextField
---
# Text Fields

<p class="description">用户可以在文本框内输入或编辑文字</p>

[文本框](https://material.io/design/components/text-fields.html)允许用户在界面中输入文本，通常，我们会在表单或者对话框中使用它们。

## TextField

` TextField `包装器组件是一个完整的表单控件，包括标签，输入和帮助文本。

{{"demo": "pages/demos/text-fields/TextFields.js"}}

## Outlined

边框样式的`文本框`

{{"demo": "pages/demos/text-fields/OutlinedTextFields.js"}}

## Filled

填充样式的`文本框`

{{"demo": "pages/demos/text-fields/FilledTextFields.js"}}

## Components

`TextField` is composed of smaller components ( [`FormControl`](/api/form-control/), [`Input`](/api/input/), [`FilledInput`](/api/filled-input/), [`InputLabel`](/api/input-label/), [`OutlinedInput`](/api/outlined-input/), and [`FormHelperText`](/api/form-helper-text/) ) that you can leverage directly to significantly customize your form inputs.

您可能注意到了， `TextField`组件相对于原生的 HTML input 组件中缺少了一些属性。 这是故意为之的， 该组件只负责处理最常用的一些属性，如果有需求，需要由用户自己使用下面 Demo 中演示的基础组件。 但是同时, 为了避免过于模版化，您仍然可以使用 `inputProps` (和 `inputProps`, `InputLabelProps` 属性) 来控制原生组件的属性。

{{"demo": "pages/demos/text-fields/ComposedTextField.js"}}

## Inputs

{{"demo": "pages/demos/text-fields/Inputs.js"}}

## Layout

`TextField`, `FormControl` 允许指定`margin`来改变输入的垂直间距。 Using `none` (default) will not apply margins to the `FormControl`, whereas `dense` and `normal` will as well as alter other styles to meet the specification.

{{"demo": "pages/demos/text-fields/TextFieldMargins.js"}}

## Input Adornments

`Input` allows the provision of `InputAdornment`. These can be used to add a prefix, a suffix or an action to an input. For instance, you can use an icon button to hide or reveal the password.

{{"demo": "pages/demos/text-fields/InputAdornments.js"}}

## Filled Input Adornments

{{"demo": "pages/demos/text-fields/FilledInputAdornments.js"}}

## Outlined Input Adornments

{{"demo": "pages/demos/text-fields/OutlinedInputAdornments.js"}}

## 格式化输入

You can use third-party libraries to format an input. You have to provide a custom implementation of the `<input>` element with the `inputComponent` property.

下面的演示使用 [react-text-mask](https://github.com/text-mask/text-mask)和 [react-number-format](https://github.com/s-yadav/react-number-format) 库。

{{"demo": "pages/demos/text-fields/FormattedInputs.js"}}

## 自定义输入

如果您有阅读[重写文档](/customization/overrides/) 但你还不是很自信能够完全掌握， 以下是如何更改一个输入的主要颜色的示例

{{"demo": "pages/demos/text-fields/CustomizedInputs.js"}}

## With icon

图标可以指定为预置或追加。

{{"demo": "pages/demos/text-fields/InputWithIcon.js"}}

## Limitations

输入标签 "shrink" 状态并不总是正确的。 输入标签应在输入显示内容时立即收缩。 在某些情况下, 我们无法确定 "shrink" 状态 (数字输入、日期时间输入、条带输入)。 您可能会注意到重叠。

![shrink](/static/images/text-fields/shrink.png)

若要解决此问题, 您可以强制标签的 "shrink" 状态。

```jsx
<TextField InputLabelProps={{ shrink: true }} />
```

或

```jsx
<InputLabel shrink>Count</InputLabel>
```