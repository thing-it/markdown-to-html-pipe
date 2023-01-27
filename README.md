# Deprecation notice
> **Warning**
> This package is no longer actively maintained. 
> We have implemented a custom solution within our main repos. 
> This serves as an archive and may be deleted in the future.

# Markdown To HTML Pipe


Converts a Markdown string, outputs HTML.

## Usage

```typescript
// example.module.ts
import {NgModule} from '@angular/core';
import {MarkdownToHtmlModule} from 'markdown-to-html-pipe';
import {ExampleComponent} from './example.component';

@NgModule({
  imports: [MarkdownToHtmlModule],
  declarations: [ExampleComponent]
})
export class ExampleModule {}
```

```typescript
// example.component.ts
import {Component} from '@angular/core';

@Component({
  selector: 'example',
  template: `<div [innerHTML]="content|MarkdownToHtml"></div>`
})
export class ExampleComponent {
  protected content: string = 'This will render **Markdown** content!';
}
```

Will be rendered as:

```html
<div>
  <p>This will render <strong>Markdown</strong> content!</p>
</div>
```

## Installation

Run

```
npm install --save markdown-to-html-pipe
```
