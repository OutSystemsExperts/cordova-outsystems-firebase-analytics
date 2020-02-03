# API

The list of available methods for this plugin is described below.
The tag for calls to the plugin is "window.Analytics.".
A normal call would look like:
```
window.Analytics.forceCrashlytics(function(data){},function(error){})
```
### Anaylics

##### **`logEvent(name, params, success, error): void`**
Logs events that provide insight on what is happening in your app, such as user actions, system events, or errors.

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `name`      | `String`                         | Event Name                  |
| `params`    | `JSONObject`                     | Parameters that can be registered for reporting in your Analytics reports. They can also be used as filters in audience definitions that can be applied to every report.|

##### **`setScreenName(name, success, error): void`**

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `name`      | `String`                         | Screen name                 |

##### **`setUserId(id, success, error): void`**
Allows you to store a user ID for the individual using your app.

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `id`        | `String`                         | user ID                     |

##### **`setUserProperty(name, value, success, error): void`**
Set user properties which are attributes you define to describe segments of your user base, such as language preference or geographic location.

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `name`      | `String`                         | Property name               |
| `value`     | `String`                         | Value to be attributed to the property |

##### **`setAnalyticsCollectionEnabled(enabled, success, error): void`**
Enable or temporarily disable Analytics Collection

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `enabled`   | `Bool`                           | If Analytics Collection is going to be enabled |

### Crashlytics

##### **`logError(message, success, error): void`**
Log non-fatal exceptions.

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `message`   | `String`                         | Exception Message           |

##### **`forceCrashlytics(success, error): void`**
Force a crash in your app

##### **`setCrashlyticsUserId(userId, success, error): void`**
Assign each user a unique identifier in the form of an ID number, token, or hashed value for more information click [here](https://firebase.google.com/docs/crashlytics/customize-crash-reports?authuser=0#set_user_ids)

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `userId`    | `String`                         | User identifier             |

### Performance

##### **`startTrace(name, success, error): void`**
Initialize a new Tracing

| parameter   | type                             | description      |
| ----------- |----------------------------------|------------------|
| `name`      | `String`                         | Trace name       |

##### **`incrementCounter(name, counterNamed, success, error): void`**
Increment local metric of a given Trace

| parameter   | type                             | description      |
| ----------- |----------------------------------|------------------|
| `name`      | `String`                         | Trace name       |
| `counterNamed` | `String`                         | Metric name      |


##### **`stopTrace(name, success, error): void`**
Stop a Tracing

| parameter   | type                             | description      |
| ----------- |----------------------------------|------------------|
| `name`      | `String`                         | Trace name       |

##### **`addTraceAttribute(name, attribute, value, success, error): void`**
Add a metric to a Trace

| parameter   | type                             | description      |
| ----------- |----------------------------------|------------------|
| `name`      | `String`                         | Trace name       |
| `attribute` | `String`                         | Metric name      |
| `value`     | `String`                         | Value for the metric |

##### **`setPerformanceCollectionEnabled(enabled, success, error): void`**
Enable or temporarily disable Performance Collection

| parameter   | type                             | description                 |
| ----------- |----------------------------------|-----------------------------|
| `enabled`   | `Bool`                           | If Performance Collection is going to be enabled |
