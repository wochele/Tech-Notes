# Routing

- [Routing in depth plunkr](https://angular.io/resources/live-examples/router/ts/plnkr.html)
- [Router Book](https://leanpub.com/router/)
- "Like a mini application encapsulating the features inside that route (Component, Service, Pipe, Directive)"
- [Routing and Navigation Docs](https://angular.io/docs/ts/latest/guide/router.html)

- The Angular router is an external, optional Angular NgModule called RouterModule. The router is a combination of multiple provided services (RouterModule), multiple directives (RouterOutlet, RouterLink, RouterLinkActive), and a configuration (Routes). 
- The Angular Router enables navigation from one view to the next as users perform application tasks.

```
import { Routes, RouterModule } from '@angular/router';
```

### `<base href>`

- Most routing applications should add a <base> element to the index.html as the first child in the <head> tag to tell the router how to compose navigation URLs. If the app folder is the application root, set the href value exactly as shown here.

```
<base href="/">
```

A router has no routes until we configure it. We bootstrap our application with an array of routes that we'll provide to our RouterModule.forRoot function.

```
import { ModuleWithProviders } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const appRoutes: Routes = [
  { path: 'hero/:id', component: HeroDetailComponent },
  { path: 'crisis-center', component: CrisisCenterComponent },
  {
    path: 'heroes',
    component: HeroListComponent,
    data: {
      title: 'Heroes List'
    }
  },
  { path: '', component: HomeComponent },
  { path: '**', component: PageNotFoundComponent }
];

export const appRoutingProviders: any[] = [

];

export const routing: ModuleWithProviders = RouterModule.forRoot(appRoutes);
```

- The Routes is an array of routes that describe how to navigate. Each Route maps a URL path to a component.
- There are no leading slashes in our path. The router parses and builds the URL for us, allowing us to use relative and absolute paths when navigating between application views.
- The :id in the first route is a token for a route parameter. In a URL such as /hero/42, "42" is the value of the id parameter. The corresponding HeroDetailComponent will use that value to find and present the hero whose id is 42. 
- The data property in the third route is a place to store arbitrary data associated with each specific route. This data is accessible within each activated route and can be used to store items such as page titles, breadcrumb text and other read-only data.
- The empty path in the fourth route matches as the default path for each level of routing. It also allows for adding routes without extending the URL path.
- The ** in the last route denotes a wildcard path for our route. The router will match this route if the URL requested doesn't match any paths for routes defined in our configuration. This is useful for displaying a 404 page or redirecting to another route.
- The order of the routes in the configuration matters and this is by design. The router uses a first-match wins strategy when matching routes, so more specific routes should be placed above less specific routes. In our configuration above, the routes with a static path are listed first, followed by an empty path route, that matches as the default route. The wildcard route is listed last as it's the most generic route and should be matched only if no other routes are matched first.
