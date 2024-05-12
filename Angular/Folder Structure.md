```
.
└── example
    ├── example.app.js
    ├── index.html
    ├── less
    │   └── example.less
    └── app
        ├── common
        │   ├── components
        │   ├── filters
        │   └── services
        └── components
            ├── home
            │   ├── home.module.js
            │   ├── home.routes.js
            │   ├── first.controller.js
            │   ├── second.controller.js
            │   ├── functionality-1.directive.js
            │   ├── functionality-1.tpl.html
            │   ├── bar.filter.js
            │   ├── model.service.js
            │   ├── model.spec.js
            │   └── home.less
            └── about
                ├── about.module.js
                ├── about.routes.js
                ├── third.controller.js
                ├── functionality-2.directive.js
                ├── functionality-3.directive.js
                ├── localize.filter.js
                ├── helper.service.js
                └── about.less
```
###### `Angular.json`
Main focus should be on architect section 


`serve` - To run the project locally 
`build` - Contains the build information
`configuration` - Contains the production budget (e.g size of the final webpack bundle and limit of CSS files etc)


#### `main.ts`

```
import { bootstrapApplication } from '@angular/platform-browser';

import { appConfig } from './app/app.config';

import { AppComponent } from './app/app.component';

  

bootstrapApplication(AppComponent, appConfig)

  .catch((err) => console.error(err));
```

In this file we are stacking the main component `AppComponent` along with its configuration `appConfig`
