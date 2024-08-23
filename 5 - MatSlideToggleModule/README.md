# 5 - MatSlideToggleModule
 
1. open `app.component.ts`

```
import { Component } from '@angular/core';
import { CommonModule } from '@angular/common';
import { RouterOutlet } from '@angular/router';

import { MatSlideToggleModule } from '@angular/material/slide-toggle';

@Component({
  selector: 'app-root',
  standalone: true,
  imports: [
    CommonModule, 
    RouterOutlet,
    MatSlideToggleModule
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
<mat-slide-toggle>Toggle me!</mat-slide-toggle>
```

3. open `app.component.scss`

```
* {
    margin: 40px;
}
```

![Image](4.PNG)

![Image](5.PNG)