# 9 - MatSliderModule - Selecting a range
 
1. open `app.component.ts`

```
import { Component } from '@angular/core';
import { CommonModule } from '@angular/common';
import { RouterOutlet } from '@angular/router';

import {MatSliderModule} from '@angular/material/slider';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [
    CommonModule, 
    RouterOutlet,
    MatSliderModule
  ],
  templateUrl: './app.component.html',
  styleUrl: './app.component.scss'
})
export class AppComponent {

  title = 'ag_material_demo';

}
```

2. open `app.component.html`

```
<mat-slider min="200" max="500" class="custom">

  <input value="300" matSliderStartThumb>

  <input value="400" matSliderEndThumb>

</mat-slider>
```

3. open `app.component.scss`

```
.custom {
  margin: 40px;
}

mat-slider {
  width: 300px;
}
```

![Image](4.PNG)