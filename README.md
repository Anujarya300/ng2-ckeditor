# Angular2 - CKEditor component

Use the [CKEditor (4.x)](http://ckeditor.com/) wysiwyg in your Angular2 application.

### <a name="install"></a>Installation

- Include CKEditor javascript files in your application
- Install ng2-ckeditor
  - JSPM : ```jspm install ng2-ckeditor=github:chymz/ng2-ckeditor```
  - NPM : ```npm install ng2-ckeditor```

### <a name="sample"></a>Sample (ES6)

```javascript
import {Component} from '@angular/core';
import {CKEditor} from 'ng2-ckeditor';

@Component({
  selector: 'sample',
  directives: [CKEditor],
  template: `<ckeditor [(ngModel)]="ckeditorContent" [config]="{uiColor: '#99000'}"></ckeditor>`
})
export class Sample{
  constructor(){
    this.ckeditorContent = `<p>My HTML</p>`;
  }
}
```

Other samples :
- [ES2016 and JSPM](https://github.com/chymz/angular2-jspm-seed/tree/ng2-ckeditor)
- [TypeScript and Webpack](https://github.com/chymz/angular2-seed/tree/ng2-ckeditor)

### <a name="config"></a>Configuration

* config : The configuration object for CKEditor see http://docs.ckeditor.com/#!/api/CKEDITOR.config

* ***[Deprecated : use file loader with your bundler]*** configFile : You can use a javacsript file to configure your CKEditor (Only work with SystemJS)
```javascript
export var config = {
    uiColor: '#990000'
}
```
