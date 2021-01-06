## change color instruction



### Side bar

- change side bar link text color

  **In Module.scss**

  `@mixin sidebar-links($color:rgba(255,0,0,0.3)) {`
  `color: $color;`
  `transition: color 0.35s ease-in-out;`
  `user-select: none;`
  `margin: 0 .25rem;`



- Sidebar background: 

  **In assets/css/_colors/light-typography.scss**

  `--sidebar-bg: radial-gradient(circle, #696969 0%, rgba(35, 37, 46, 1) 100%);`

- side bar cursor

  **In assets/css/_colors/light-typography.scss**

  ```--nav-cursor-color: rgba(38,12,12,1);```

- Side bar text color hover

  **In assets/css/_addon/main/scss**

    `.nav-item {`
      `height: $tab-height;`
      `&:hover {`
        `.nav-link {`
          `color: red;`
        `}`
      `}`
      `&.active {`
        `.nav-link {`
          `color: #000000; //???`
        `}`
      `}`
   ` }`

  

### Home page

**In assets/css/_colors/light-typography.scss**

  `--btn-active-bg: #696969;`



### Post list page

**In assets/css/_colors/light-typography.scss**

- change the color of post titles:

  `--link-color: #696969;`

- change post title hover color:

**In Module.scss**

`%link-hover {`
  `color: #000000!important;`
  `border-bottom: 1px solid #000000;`
  `text-decoration: none;`
`}`

- change the color of post list content

  **In assets/css/_colors/light-typography.scss**

  `  --post-list-text-color: black;`



  ==Everything is in main.css, module.css or home.css==

