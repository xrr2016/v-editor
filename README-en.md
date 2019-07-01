# V-editor

![](https://cdn.nlark.com/yuque/0/2019/svg/224563/1561712182975-f8bc4b2e-5be4-45ce-b53f-dd5195a625bf.svg#align=left&display=inline&height=20&originHeight=20&originWidth=90&size=0&status=done&width=90) [![](https://img.shields.io/npm/dm/@femessage/v-editor.svg#align=left&display=inline&height=20&originHeight=20&originWidth=140&status=done&width=140)](https://www.npmjs.com/package/@femessage/v-editor)
[![](https://img.shields.io/npm/v/@femessage/v-editor.svg#align=left&display=inline&height=20&originHeight=20&originWidth=80&status=done&width=80)](https://www.npmjs.com/package/@femessage/v-editor)
[![](https://img.shields.io/npm/l/@femessage/v-editor.svg#align=left&display=inline&height=20&originHeight=20&originWidth=78&status=done&width=78)](https://github.com/FEMessage/v-editor/blob/master/LICENSE)
[![](https://img.shields.io/badge/PRs-welcome-brightgreen.svg#align=left&display=inline&height=20&originHeight=20&originWidth=90&status=done&width=90)](https://github.com/FEMessage/v-editor/pulls) [![](https://img.shields.io/badge/%F0%9F%A4%96-release%20notes-00B2EE.svg#align=left&display=inline&height=20&originHeight=20&originWidth=104&status=done&width=104)](https://github-tools.github.io/github-release-notes/)

Lightweight rich text editor packaged according to [wang]()[Editor](https://github.com/wangfupeng1988/wangEditor) and [upload-to-ali](https://github.com/FEMessage/upload-to-ali).

![view.png](https://cdn.nlark.com/yuque/0/2019/png/224563/1561712220041-fd0c73d2-b536-4195-b87e-8e5a4f200ac5.png#align=left&display=inline&height=355&name=view.png&originHeight=355&originWidth=939&size=14023&status=done&width=939)

<a name="Idxrc"></a>

## Table of Contents

- [Introduction](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#introduction)
  - [Component size](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#%E7%BB%84%E4%BB%B6%E5%A4%A7%E5%B0%8F)
  - [OSS file Upload](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#oss-%E6%96%87%E4%BB%B6%E4%B8%8A%E4%BC%A0)
- [Feature](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#feature)
- [Demo](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#demo)
- [Install](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#install)
- [Quick start](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#quick-start)
- [Dev](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#dev)
- [License](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#license)
- [Contributors](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#contributors)

<a name="Qi3m6"></a>

## Introduction

The company's internal demand for rich text components is relatively simple: simple graphic arrangement.<br />Therefore, the selection of rich text components is mainly considered:

<a name="CdOpx"></a>

### Component size

Tend to the most lightweight rich text editor.<br />Selection and comparison of the industry's more famous (open source star is relatively high) components: quill, wangEditor, tinymce-vue, medium editor.

![diff.png](https://cdn.nlark.com/yuque/0/2019/png/224563/1561712281847-fea73ef8-4627-49ae-8e94-ae5aaee880d2.png#align=left&display=inline&height=1352&name=diff.png&originHeight=1352&originWidth=1680&size=85609&status=done&width=1680)<br />[⬆Back to Top](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#table-of-contents)

<a name="uBUTN"></a>

### OSS file Upload

Equipped with the [upload-to-ai][upload-to-ali] component, the rich text component can automatically upload the picture to oss, avoiding the image information to be stored in the content in base64 encoding, effectively compress text information.<br />[⬆Back to Top](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#table-of-contents)

<a name="sVEZZ"></a>

## Feature

- **Lightweight** : The smallest rich text editor, [Component Selection range](https://mubu.com/doc/sA3r4QKBK0) Reference (quill, tinymce-vue, medium editor)
- **Oss Upload** : Integrated upload components, just configure the basic information of OSS ([Configuration Reference][upload-to-ali]), you can upload the picture to oss, support screenshot paste upload<br />[⬆Back to Top](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#table-of-contents)

<a name="3u4Zd"></a>

## Demo

- [Doc and online demo](https://femessage.github.io/v-editor/)<br />[⬆Back to Top](https://www.yuque.com/deepexi-serverless/onx52o/ixffxl?translate=en#table-of-contents)

<a name="MF9mw"></a>

## Install

```sh
# Upload image function depends on upload-to-ali component
yarn add @femessage/upload-to-ali @femessage/v-editor
```

[⬆ Back to Top](#table-of-contents)

<a name="eFhNX"></a>

## Quick start

```html
//step1 Ensure oss config //step2 In the .vue file that needs to use the
renderer
<template>
  <v-editor v-model="content" />
</template>

<script>
  import VEditor from '@femessage/v-editor'

  export default {
    components: {
      VEditor
    },
    data() {
      return {
        content: ''
      }
    }
  }
</script>
```

[⬆ Back to Top](https://github.com/FEMessage/v-editor/blob/dev/README.md#table-of-contents)

<a name="Dev"></a>

## Dev

```sh
# install dependency
yarn
# run vue-styleguidist
yarn dev
```

[⬆ Back to Top](#table-of-contents)

<a name="License"></a>

## License

[MIT](./LICENSE)<br />[⬆ Back to Top](#table-of-contents)<br />[upload-to-ali]: [https://github.com/FEMessage/upload-to-ali](https://github.com/FEMessage/upload-to-ali) 'upload-to-ali'<br />[wangeditor]: [https://github.com/wangfupeng1988/wangEditor](https://github.com/wangfupeng1988/wangEditor) 'wangEditor'

<a name="Contributors"></a>

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

| [![](https://avatars2.githubusercontent.com/u/4848041?v=4#alt=kunzhijia&width=100)<br />**kunzhijia**](https://github.com/kunzhijia)<br />[💻](https://github.com/FEMessage/v-editor/commits?author=kunzhijia) [🐛](https://github.com/FEMessage/v-editor/issues?q=author%3Akunzhijia) [📖](https://github.com/FEMessage/v-editor/commits?author=kunzhijia) | [![](https://avatars2.githubusercontent.com/u/20613509?v=4#alt=listars&width=100)<br />**listars**](https://github.com/listars)<br />[🐛](https://github.com/FEMessage/v-editor/issues?q=author%3Alistars) [📖](https://github.com/FEMessage/v-editor/commits?author=listars) | [![](https://avatars3.githubusercontent.com/u/19591950?v=4#alt=Donald%20Shen&width=100)<br />**Donald Shen**](https://donaldshen.github.io/portfolio)<br />[🐛](https://github.com/FEMessage/v-editor/issues?q=author%3Adonaldshen) [📖](https://github.com/FEMessage/v-editor/commits?author=donaldshen) | [![](https://avatars3.githubusercontent.com/u/9384365?v=4#alt=levy&width=100)<br />**levy**](http://levy.work)<br />[👀](#review-levy9527) [🚇](#infra-levy9527) [🤔](#ideas-levy9527) |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
