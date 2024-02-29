# NgMfm

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.2.5.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.


## Future Reference Document: Environment Configuration

### Purpose
This document serves as a future reference for understanding the environment configuration in the provided code.

### Code Overview
The provided code is written in TypeScript and represents the environment configuration for an Angular application. It sets different values for variables based on the current environment and exports an `environment` object with these values.

### Configuration
The configuration is determined by the `currentEnvironment` variable, which can have the following possible values:
- `develop`: Development environment
- `qa`: Quality Assurance environment
- `uat`: User Acceptance Testing environment
- `local`: Local development environment
- `prod`: Production environment

Based on the current environment, the code sets values for the following variables:
- `socketEndpoint`: Represents the endpoint for a socket connection.
- `apiURL`: Represents the API endpoint URL.
- `mfmLegacyUrl`: Represents a legacy URL.

The `environment` object, which is exported, also contains additional configuration options:
- `production`: A boolean value indicating whether the current environment is set to production.
- `auth`: An object containing authentication-related configuration values, including domain, client ID, and redirect URI.
- `SOCKET_ENDPOINT`: The socket endpoint value.
- `apiURL`: The API endpoint URL value.
- `mfmLegacyUrl`: The legacy URL value.

### Usage
To use this environment configuration in an Angular application, import it where needed using the following statement:

```typescript
import { environment } from './path/to/environment';
```

You can then access the configuration values as follows:

```typescript
console.log(environment.production); // true if production, false otherwise
console.log(environment.auth.domain); // the authentication domain
console.log(environment.SOCKET_ENDPOINT); // the socket endpoint URL
console.log(environment.apiURL); // the API endpoint URL
console.log(environment.mfmLegacyUrl); // the legacy URL
```

### Additional Note
To enable better error debugging during development, there is a commented import statement for `'zone.js/plugins/zone-error'`. This import is suggested to be commented out in production mode to avoid performance impact caused by error stack frames.

It is recommended to review and update the environment configuration values as needed for different deployment environments.