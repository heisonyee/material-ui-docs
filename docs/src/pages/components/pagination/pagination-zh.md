---
title: 分页React组件
components: Pagination, PaginationItem
---

# 分页

<p class="description">分页组件使用户能够从一系列页面中选择一个特定的页面。</p>

## 基础分页

{{"demo": "pages/components/pagination/BasicPagination.js"}}

## 描边分页

{{"demo": "pages/components/pagination/PaginationOutlined.js"}}

## 圆形分页

{{"demo": "pages/components/pagination/PaginationRounded.js"}}

## 分页大小

{{"demo": "pages/components/pagination/PaginationSize.js"}}

## Buttons（按钮）

你可以选择启用第一页和最后一页按钮，或禁用上一页和下一页按钮。

{{"demo": "pages/components/pagination/PaginationButtons.js"}}

## 分页范围

你可以使用`siblingRange`属性指定当前页面两侧显示的位数，并使用`boundaryRange`属性指定在起始页和结束页数旁边显示。

{{"demo": "pages/components/pagination/PaginationRanges.js"}}

## 受控分页

{{"demo": "pages/components/pagination/PaginationControlled.js"}}

## Router集成

分页支持两种Router集成方法，`renderItem`属性：

{{"demo": "pages/components/pagination/PaginationLink.js"}}

## `usePagination`

作为一种高级定制方式，我们公开了一个 `usePagination()`hook。 它接受与分页组件几乎相同的选项，减去与JSX渲染有关的所有属性。 分页组件内部也是使用的这个hook。

```jsx
import { usePagination } from '@material-ui/lab/Pagination';
```

{{"demo": "pages/components/pagination/UsePagination.js"}}

## 可访问性

### ARIA

默认情况下，根节点具有“导航”和aria标签“分页导航”的作用。 页面项目具有一个aria-label，用于标识项目的用途（“转到首页”，“转到上一页”，“转到页面1”等）。 你可以使用 `getItemAriaLabel`属性来覆盖它们。

### 键盘

分页项目按标签顺序排列，标签索引为“0”。
