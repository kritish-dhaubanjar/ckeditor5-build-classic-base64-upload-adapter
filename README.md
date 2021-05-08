# ckeditor5-build-classic-base64-upload-adapter

The classic editor build of CKEditor 5 with Base64UploadAdapter

## Quick start

1. Clone the build repository.
2. Install the plugin package.
3. Add it to the build configuration.
4. Bundle the build.

**Clone the build repository.**

```shell
git clone -b stable https://github.com/ckeditor/ckeditor5

cd ckeditor5/packages/ckeditor5-build-classic
npm install
```

**Now, install the plugin package:**
```shell
npm install --save @ckeditor/ckeditor5-upload
```
Edit the src/ckeditor.js file to add your plugin to the list of plugins which will be included in the build and to add your feature’s button to the toolbar:

```js
...
...
import Base64UploadAdapter from '@ckeditor/ckeditor5-upload/src/adapters/base64uploadadapter';

...

// Plugins to include in the build.
ClassicEditor.builtinPlugins = [
  ...
  Base64UploadAdapter,
]
```

**Finally, bundle the build:**
```
npm run build
```

If everything worked, the editor build (which is available in the `build/` directory) should be updated.
```shell
jin@death-note:~/ckeditor5-build-classic-base64-upload-adapter/build$ ls

-rw-rw-r-- 1 jin jin  719976 May  8 13:07 ckeditor.js
-rw-rw-r-- 1 jin jin 4792997 May  8 13:07 ckeditor.js.map
drwxrwxr-x 2 jin jin    4096 May  8 13:07 translations
```

## Usage

```js
/* Before */
//import ClassicEditor from '@ckeditor/ckeditor5-build-classic';

/* After */
import ClassicEditor from '@/ckeditor5-build-classic-base64-upload-adapter/build/ckeditor.js';
```

![image](https://user-images.githubusercontent.com/25634165/117547828-75324380-b051-11eb-80e9-0bf0c9bbf2dd.png)

