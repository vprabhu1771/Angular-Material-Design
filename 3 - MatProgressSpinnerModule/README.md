# 2 - MatIconModule
 
1. open `app.component.ts`

```
import { Component } from '@angular/core';
import { CommonModule } from '@angular/common';
import { RouterOutlet } from '@angular/router';

import {MatProgressSpinnerModule} from '@angular/material/progress-spinner';


@Component({
  selector: 'app-root',
  standalone: true,
  imports: [
    CommonModule, 
    RouterOutlet,
    MatProgressSpinnerModule,
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
<mat-spinner></mat-spinner>
```

3. open `app.component.scss`

```
* {
    margin: 40px;
}
```

![Image](4.PNG)