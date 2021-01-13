---
title: How to Customize the Blog Style
author: Panpan
categories: [Blogging, Tutorial]
tags: [CSS, writing]
---

**Everything is in file main.css, module.css or home.css**. 

We just need to find the CSS key by using "Inspect Elements" in browser and look it up in the three CSS files.

## Side bar


- Sidebar background: 

  **In assets/css/_colors/light-typography.scss**

  ```css
  --sidebar-bg: radial-gradient(circle, #696969 0%, rgba(35, 37, 46, 1) 100%);
  ```

- side bar cursor

  **In assets/css/_colors/light-typography.scss**

  ```css
  --nav-cursor-color: rgba(38,12,12,1);
  ```

- change side bar link text color

  **In assets/css/_addon/module.scss**
  
  ```css
  @mixin sidebar-links($color:rgba(255,0,0,0.3)) {
  color: $color;
  transition: color 0.35s ease-in-out;
  user-select: none;
  margin: 0 .25rem;
  ```
- Side bar text color hover

  **In assets/css/_addon/main/scss**
  ```css
    .nav-item {
      height: $tab-height;
      &:hover {
        .nav-link {
          color: red;
        }
      }
      &.active {
        .nav-link {
          color: #000000; 
        }
      }
    }
  ```
  

## Home page

**In assets/css/_colors/light-typography.scss**

```css 
  --btn-active-bg: #696969;
```



## Post list page

**In assets/css/_colors/light-typography.scss**

- change the color of post titles:
  ```css
  --link-color: #696969;
  ```
- change post title hover color:

  **In assets/css/_addon/module.scss**

  ```css
%link-hover {
  color: #000000!important;
  border-bottom: 1px solid #000000;
  text-decoration: none;
}
  ```
- change the color of post list content

  **In assets/css/_colors/light-typography.scss**
  
  ```css
  --post-list-text-color: #000000;
  ```



