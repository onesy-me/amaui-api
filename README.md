
</br>
</br>

<p align='center'>
  <a target='_blank' rel='noopener noreferrer' href='#'>
    <img src='utils/images/logo.svg' alt='onesy logo' />
  </a>
</p>

<h1 align='center'>onesy API</h1>

<p align='center'>
  API
</p>

<br />

<h3 align='center'>
  <sub>MIT license&nbsp;&nbsp;&nbsp;&nbsp;</sub>
  <sub>Production ready&nbsp;&nbsp;&nbsp;&nbsp;</sub>
  <sub>100% test cov&nbsp;&nbsp;&nbsp;&nbsp;</sub>
  <sub>Nodejs</sub>
</h3>

<p align='center'>
    <sub>Very simple code&nbsp;&nbsp;&nbsp;&nbsp;</sub>
    <sub>Modern code&nbsp;&nbsp;&nbsp;&nbsp;</sub>
    <sub>Junior friendly&nbsp;&nbsp;&nbsp;&nbsp;</sub>
    <sub>Typescript&nbsp;&nbsp;&nbsp;&nbsp;</sub>
    <sub>Made with :yellow_heart:</sub>
</p>

<br />

## Getting started

### Add

```sh
yarn add @onesy/api
```

### Use

```javascript
  import express from 'express';
  import { Route, Method, IRouteClassInstance, Routes } from '@onesy/api';

  class Base implements IRouteClassInstance {

    public response(req: express.Request, response: express.Response, options: { method: 'json' | 'send', type: 'application/json', }) { return ...; }

    public error(req: express.Request, error: Error) { return ...; }

  }

  // Add decorator to a class representing a route
  @Route(
    '/a',
    method
  )
  class A extends Base {

    @Method(
      'get',
      '/a',
      method1
    )
    public a() { }

  }

  // Create an express app
  const app = express();

  // Register all classes as app routes
  Routes([A], app);

  // app routes:
  // GET /a/a, middlewares: method, method1

  // etc.
```

### Dev

Install

```sh
yarn
```

Test

```sh
yarn test
```

### Prod

Build

```sh
yarn build
```
