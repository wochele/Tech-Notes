# Providers

- A provider is a recipe for creating a service.
- A provider is something that can create or return a service, typically the service class itself.
- You can register providers in modules or in components.
- In general, add providers to the root module so that the same instance of a service is available everywhere.
- Registering at a component level means you get a new instance of the service with each new instance of that component.

