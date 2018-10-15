---
title: Circular Progress, Linear Progress React component
components: CircularProgress, LinearProgress
---
# 进度

<p class="description">进度指示器用以表示一个不确定的等待时间或显示一个处理过程的时间长短。</p>

[进度指示器](https://material.io/design/components/progress-indicators.html) 通知用户当前处理过程的状态，例如加载一个应用，提交一个表单或保存一些更新。 它们与应用程序状态进行通信并指示可用的操作，例如用户是否可从当前页面离开。

**确定的** 指示器显示一个操作消耗多长时间。

**未确定**指示器可视化一个不确定的操作等待时间。

#### 进度指示器组

当显示一系列过程的进度时，表示全部的过程而不是每个单独活动的进度。

## 环形的

[圆形进度指示器](https://material.io/design/components/progress-indicators.html#circular-progress-indicators)支持确定过程和不确定过程。

- **确定的** 环形指示器填充不可见区域，以颜色环形追踪，作为指示器从0至360度移动。
- **不确定** 环形指示器在沿着不可见轨道移动时，随之变大变小。

### 不确定环形

{{"demo": "pages/demos/progress/CircularIndeterminate.js"}}

### 交互集成

{{"demo": "pages/demos/progress/CircularIntegration.js"}}

### 确定环形

{{"demo": "pages/demos/progress/CircularDeterminate.js"}}

### 静态环形

{{"demo": "pages/demos/progress/CircularStatic.js"}}

## 线状

[线状进度](https://material.io/design/components/progress-indicators.html#linear-progress-indicators) 指示器.

### 不确定线状

{{"demo": "pages/demos/progress/LinearIndeterminate.js"}}

### 确定线状

{{"demo": "pages/demos/progress/LinearDeterminate.js"}}

### 缓冲线状

{{"demo": "pages/demos/progress/LinearBuffer.js"}}

### 查询线状

{{"demo": "pages/demos/progress/LinearQuery.js"}}

## 非标准范围

进度组件接受一个0 - 100范围的值。 作为默认的最小 / 最大值，这简化了屏幕阅读用户的使用。 但是有时，你可能会使用值超出这个范围的数据源。 Here's how you can easily transform a value in any range to a scale of 0 - 100:

```jsx
// MIN = Minimum expected value
// MAX = Maximium expected value

// Function to normalise the values (MIN / MAX could be integrated)
const normalise = value => (value - MIN) * 100 / (MAX - MIN);

// Example component that utilizes the `normalise` function at the point of render.
function Progress(props) {
  return (
    <React.Fragment>
      <CircularProgress variant="determinate" value={normalise(props.value)} />
      <LinearProgress variant="determinate" value={normalise(props.value)} />
    </React.Fragment>
  )
}
```

## Delaying appearance

There are [3 important limits](https://www.nngroup.com/articles/response-times-3-important-limits/) to know around response time. The ripple effect of the `ButtonBase` component ensures that the user feels that the system is reacting instantaneously. Normally, no special feedback is necessary during delays of more than 0.1 but less than 1.0 second. After 1.0 second, you can display a loader to keep user's flow of thought uninterrupted.

{{"demo": "pages/demos/progress/DelayingAppearance.js"}}

## Limitations

Under heavy load, you might lose the stroke dash animation or see random CircularProgress ring widths. You should run processor intensive operations in a web worker or by batch in order not to block the main rendering thread.

![heavy load](/static/images/progress/heavy-load.gif)

See https://github.com/mui-org/material-ui/issues/10327