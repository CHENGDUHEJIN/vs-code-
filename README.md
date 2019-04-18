# vs-code-
###vscode 使用格式化配置

### 1、插件安装

#####Eslint、Prettier - Code formatter、Vetur

#### 2、.prettierrc.js配置
文件夹根目录新建.prettierrc.js文件，文件配置如下 
```
module.exports = {
  eslintIntegration: true,
  // 使用单引号
  singleQuote: true,
  // 结尾不加分号
  semi: false,
  // js代码中超出后换行
  printWidth: 100
}
```

####3、vs code  setting 配置

```
{
  //.vue文件template格式化支持，并使用js-beautify-html插件
  "vetur.format.defaultFormatter.html": "prettyhtml",
  //js-beautify-html格式化配置，属性强制换行
  //文档：https://github.com/beautify-web/js-beautify#css--html
  "vetur.format.defaultFormatterOptions": {
    "js-beautify-html": {
      "wrap_attributes": "force",
      "singleQuote": true,
      "semi": false
    },
    "prettyhtml": {
      "printWidth": 100,
      "singleQuote": true,
      "wrapAttributes": false,
      "sortAttributes": false,
      "semi": false
    },
    "prettier": {
      "singleQuote": true,
      "semi": false,
      "eslintIntegration": true
    },
    "wrap_attributes": "force-aligned"
  },
  //根据文件后缀名定义vue文件类型
  "files.associations": {
    "*.vue": "vue"
  },
  //保存时eslint自动修复错误
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    {
      "language": "vue",
      "autoFix": true
    }
  ],
  "eslint.autoFixOnSave": true,
  "[jsonc]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "vetur.validation.template": false,
  "[html]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}

JS使用规范为文尾不要空格、分号、使用单引号
```

#### 4、编辑规范
class命名使用 a-b-c书写方式
函数命名  使用驼峰命名  

