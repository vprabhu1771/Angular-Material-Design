# 10 - MatSliderModule - Formatting the thumb label
 
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

  formatLabel(value: number): string {
    if (value >= 1000) {
      return Math.round(value / 1000) + 'k';
    }

    return `${value}`;
  }

}
```

2. open `app.component.html`

```
<mat-slider 
min="0" 
max="100000" 
step="1000" 
showTickMarks 
discrete 
[displayWith]="formatLabel" 
class="custom">

  <input matSliderThumb>
  
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

![Image](5.PNG)

![Image](6.PNG)