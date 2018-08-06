# vue-todolist
vue-todolist


## 亮点

* 渐进式的

    我认为就是可以作为一个vm数据驱动的类库来使用（实际上他也是一个类库而已）

* 可维护性、可测试的 Maintainable Testable

    关于这一点，我认为在于vue带来的数据驱动，给了我们更优雅的测试可能性

* 生态带来大型应用开发的可能

    由于vue作为一个viewModel库暴露了plugin的

* Vue2 也支持了 `渲染函数` 甚至支持 `JSX`


## 最佳实践

1. 表现类的组件用模板，逻辑类的组件用JSX

> 把组件区分为两类：一类是偏视图表现的 (presentational)，一类则是偏逻辑的 (logical)。我们推荐在前者中使用模板，在后者中使用 JSX 或渲染函数。这两类组件的比例会根据应用类型的不同有所变化，但整体来说我们发现表现类的组件远远多于逻辑类组件.
    -- from [这里](https://cn.vuejs.org/v2/guide/comparison.html)

2. 用 css-in-js 还是用 单文件组件内写 style 标签
    
    对于React来说是采用的 css-in-js方案，对于 Vue 还是建议 `单文件组件 + style 标签` 的方式

## 问题

1. 如何理解下面[这段话](https://cn.vuejs.org/v2/guide/comparison.html)? 

> 在 Vue 应用中，组件的依赖是在渲染过程中自动追踪的，所以系统能精确知晓哪个组件确实需要被重渲染。你可以理解为每一个组件都已经自动获得了 shouldComponentUpdate，并且没有上述的子树问题限制。