import { Component } from '@angular/core';
import { RouterOutlet } from '@angular/router';

import {
  CdkDragDrop, 
  moveItemInArray, 
  CdkDrag, 
  CdkDropList
} from '@angular/cdk/drag-drop';

import {MatChipsModule} from '@angular/material/chips';

export interface Vegetable {
  name: string;
}


@Component({
  selector: 'app-root',
  standalone: true,
  imports: [
    RouterOutlet,

    MatChipsModule, 
    CdkDropList, 
    CdkDrag
  ],
  templateUrl: './app.component.html',
  styleUrl: './app.component.scss'
})
export class AppComponent {

  title = 'ag_material_demo';

  vegetables: Vegetable[] = [
    {name: 'apple'},
    {name: 'banana'},
    {name: 'strawberry'},
    {name: 'orange'},
    {name: 'kiwi'},
    {name: 'cherry'},
  ];

  drop(event: CdkDragDrop<Vegetable[]>) {
    moveItemInArray(this.vegetables, event.previousIndex, event.currentIndex);
  }

}