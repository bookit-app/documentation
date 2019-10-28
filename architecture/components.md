# Components

The Book-it app is broken down into a client app and a set of micro-services running on Google Cloud Platform. The below likes are references to the details of the individual components and their respective designs.

## API Gateway

- [API Gateway](https://github.com/bookit-app/api-gateway)

## Cloud Run Services

- [Profile Services](https://github.com/bookit-app/profile-services): Set of services related to a users profile
- [Provider Services](https://github.com/bookit-app/profile-services): Set of services related to Service Providers
- [Calendar Services](https://github.com/bookit-app/profile-services): Set of services related to calendar and appointment management

## Cloud Functions

- [Service Offering Notification Publisher](https://github.com/bookit-app/service-offering-notification-publisher)
- [Welcome Email Generator](https://github.com/bookit-app/welcome-email-function)
- [Profile Creation Notification Publisher](https://github.com/bookit-app/profile-create-event-publisher)
