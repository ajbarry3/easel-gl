# Easeljs-Next

This is the easeljs-0.8.2 "in-progress" build.

The big new feature is the StageGL.
You can find documentation with troubleshooting in a [CreateJS](http://blog.createjs.com/getting-started-with-stagegl/) blog post.

***Note vectored objects do not work with StageGL only bitmap images.

## Install

```bash
npm install easel-gl --save
```

**Angular**
```ts
import { Component, AfterViewInit } from '@angular/core';
import * as easelGL from 'easel-gl';

@Component({
  selector: 'app-root',
  template: '<canvas width="500" height=500 id="demoCanvas"></canvas>'
})
export class AppComponent implements AfterViewInit {

  ngAfterViewInit() {
    var stage = new easelGL.StageGL("demoCanvas");
    var bitmap = new easelGL.Bitmap("assets/default-user.jpg");
    bitmap.x = 50;
    bitmap.y = 50;
    stage.addChild(bitmap);
    stage.update();
  }

}
```


**Ionic**
```ts
import {Component} from '@angular/core';
import * as easelGL from 'easel-gl';

@Component({
  selector: 'project-name-app',
  template: `
    <ion-content padding>
     <canvas width="500" height=500 id="demoCanvas"></canvas>
    </ion-content>
  `
})

export class MyApp {

  ionViewDidEnter() {
    var stage = new easelGL.StageGL("demoCanvas");
    var bitmap = new easelGL.Bitmap("./assets/your-image.jpg");
    bitmap.x = 50;
    bitmap.y = 50;
    stage.addChild(bitmap);
    stage.update();
  }

  constructor(){
  }
}
```
