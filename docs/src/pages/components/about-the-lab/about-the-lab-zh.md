# 关于 lab

<p class="description">此依赖包包含了一些还在开发中的组件，它们还不能移到 core（核心）库中。</p>

核心库（core）和实验室（lab）之间的主要差别就是组件是如何版本化的 拥有独立的实验室版本，我们就可以在必要的时候发布一些会影响原本代码的改动，并且核心库遵循 [slower-moving policy](https://material-ui.com/versions/#release-frequency)

程序员在使用和测试组件后向项目报漏洞，维护者就知道更多关于组件的缺点：如缺少功能，能不能访问的问题、漏洞，API设计等等的问题 The older and more used a component is, the less likely it is that new issues will be found and subsequently need to introduce breaking changes.

那些准备搬到核心库的组件，需要考虑以下几点：

* 它需要**被使用过** Material-UI 团队使用谷歌分析的方法去估计每个组件的使用情况 如果一个实验室组件使用量太少，意味着它并不能全部正常工作，或者需求量比较小
* 它需要和核心组件的**代码质量**相似 作为核心代码的一部分，它不需要很完美，但是这个组件应该要很可靠，要另其他开发者可以依赖它 
    * 每个组件需要**类型定义** 就目前来说，实验室组件不需要定义类型，但是当搬到核心代码之后就需要定义好类型了
    * 需要一个好的**测试覆盖率**。 有一些实验室组件目前并没有进行综合的测试。
* Can it be used as **leverage** to incentivize users to upgrade to the latest major release? The less fragmented the community is, the better.
* It needs to have a low probability of a **breaking change** in the short/medium future. For instance, if it needs a new feature that will likely require a breaking change, it may be preferable to delay its promotion to the core.

## 安装

请在您的项目目录中用以下方式安装依赖包：

```sh
// 用 npm 安装
npm install @material-ui/lab

// 用 yarn 安装
yarn add @material-ui/lab
```

该 lab 和那些核心组件是对等依赖的。 若您还未在项目中使用 Material-UI，那可以按如下方式安装：

```sh
// 用 npm 安装
npm install @material-ui/core

// 用 yarn 安装
yarn add @material-ui/core
```