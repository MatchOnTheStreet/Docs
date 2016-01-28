# Software Design Specification

## System Architecture
### Modules
### Interfaces
### Data
The primary type of data in our system is event information. Each event item will
have the following fields: Title, Time, Location, Description, and a list of
users who have promised to attend the event. In addition we will also keep
user information. Initially user data will consist of name, and a unique identifier.
Later we may expand the user information to include more fields, such as
previous events attended, user rating, and skills.

The data will be stored using Firebase. The format of the event and user data will
be a JSON tree.

We will be using Facebook for identification, so we won't have to care about user
identification information.

### Alternatives
#### Backend
We decide to use Firebase as our backend because of it's simplicity. However we
could have used a different infrastructure. Primarily, we considered using
App Engine as our backend. We decided not to pursue this route because it would
have increased the complexity of our backend. One drawback to Firebase, is that
it lacks flexibility. For example, it can't perform complex backend computations.
At this point in our application's life, we don't need a lot of backend services,
and since we will be abstracting the backned away in our applications, we should
be able to change it later if we need to.

### Assumptions
Since we are are relying of the Facebook API for user identification, we assume
that 1) the user is connected to the internet and 2) the user has a Facebook
account. This may not always prove to be true. Individuals that do not have
a Facebook account will not be able to use our site.

## Process
### Risk Assesment



