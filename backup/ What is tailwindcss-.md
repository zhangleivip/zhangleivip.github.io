> Tailwind CSS is a utility-first CSS framework. Tailwind CSS works by scanning all of your HTML files, JavaScript components, and any other templates for class names, generating the corresponding styles and then writing them to a static CSS file.
>
> 一个实用程序优先的 CSS 框架 Tailwind CSS 的工作原理是扫描所有 HTML 文件、JavaScript 组件和任何其他模板的类名，生成相应的样式，然后将它们写入静态 CSS 文件。

# Documentation

## Installation

1. Create tailwind.config.js file
   `npx tailwindcss init`
2. Configure your template paths

- Add the paths to all of your template files in your `tailwind.config.js`file.(在 tailwind.config.js 文件中添加所有模板文件的路径。)

3. Add tailwind directives to CSS

- Add the `@tailwind` directives for each of Tailwind's layers to your main CSS file.(将 Tailwind 每个图层的 @tailwind 指令添加到主 CSS 文件中。)

```
/src/input.css

@tailwind base;
@tailwind components;
@tailwind utilities;
```

4. Start the Tailwind CLI build process(启动 Tailwind CLI 构建过程)

- Run the CLI tool to scan your template files for classes and build your CSS.
  (运行 CLI 工具以扫描模板文件中的类并构建 CSS。)
  `npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

## NOTE

1. `min-h-screen`: 最小高度;`.min-h-screen {min-height: 100vh;}`
2. `vh(viewport height)`: 视口高度;100vh=100%;
3. `sm:hidden`:窗口宽度大于等于 640px 时，应用下面的样式，将元素的显示设置为无，即隐藏元素。

```css
@media (min-width: 640px) {
  .sm\:hidden {
    display: none;
  }
}
```

4. ` scroll-mt-40`:设置滚动边距，根据 id(#)标签定位位置时用到。
5. `<script src="js/main.js" defer></script>`<br>
   **defer**:
   > This Boolean attribute is set to indicate to a browser that the script is > meant to be executed after the document has been parsed, but before firing DOMContentLoaded.
   >
   > Scripts with the defer attribute will prevent the DOMContentLoaded event from firing until the script has loaded and finished evaluating.
   >
   > This attribute must not be used if the src attribute is absent (i.e. for inline scripts), in this case it would have no effect.
   >
   > To achieve a similar effect for dynamically inserted scripts use async="false" instead. Scripts with the defer attribute will execute in the order in which they appear in the document.
   >
   > 设置此布尔属性是为了向浏览器表明，脚本应在文档解析完成后，但在触发 DOMContentLoaded 之前执行。
   > 带有 defer 属性的脚本将阻止 DOMContentLoaded 事件触发，直到脚本加载并完成评估。
   > 如果没有 src 属性（即内联脚本），则不得使用此属性，否则将没有任何效果。
   > 要使动态插入的脚本达到类似效果，请使用 async="false" 代替。带有 defer 属性的脚本将按照它们在文档中出现的顺序执行。

6. [Adding Custom Styles](https://tailwindcss.com/docs/adding-custom-styles#using-arbitrary-values)
7. [Reusing Styles&重用样式](https://tailwindcss.com/docs/reusing-styles#extracting-classes-with-apply)