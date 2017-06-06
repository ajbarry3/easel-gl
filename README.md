# Easeljs-Next

This is the easeljs-0.8.2 "in-progress" build.

The big new feature is the StageGL.
You can find documentation with troubleshooting in a [CreateJS](http://blog.createjs.com/getting-started-with-stagegl/) blog post.

***Note vectored objects do not work with StageGL only bitmap images.

## Install

```bash
npm install easel-gl --save
```

```ts
import {Component} from '@angular/core';
import { * as easel-gl } from 'easel-gl';

@Component({
  selector: 'project-name-app',
  template: `
    <ion-content padding>
     <canvas width="500" height=500 id="demoCanvas"></canvas>
    </ion-content>
  `
})
export class MyApp {
    var stage = new easel-gl.Stage("demoCanvas");
    var bitmap = new easel-gl.Bitmap("assets/your-image.jpg");
    stage.addChild(bitmap);
    stage.update();
}
```


