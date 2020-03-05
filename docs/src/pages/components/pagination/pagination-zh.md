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

## 圆角分页

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

Pagination supports two approaches for Router integration, the `renderItem` prop:

{{"demo": "pages/components/pagination/PaginationLink.js"}}

## `usePagination`

For advanced customization use cases, we expose a `usePagination()` hook. It accepts almost the same options as the Pagination component minus all the props related to the rendering of JSX. The Pagination component uses this hook internally.

```jsx
import { usePagination } from '@material-ui/lab/Pagination';
```

{{"demo": "pages/components/pagination/UsePagination.js"}}

## 可访问性

### ARIA

The root node has a role of "navigation" and aria-label "pagination navigation" by default. The page items have an aria-label that identifies the purpose of the item ("go to first page", "go to previous page", "go to page 1" etc.). You can override these using the `getItemAriaLabel` prop.

### Keyboard

The pagination items are in tab order, with a tabindex of "0".
