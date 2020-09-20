# Internal notification service RabbitMQ, Sendgrid, Slack.
The idea here is to consume events from RabbitMQ and send email via Sendgrid or add ticket to Slack channel. Let's say, there are some critical events in our business when they occure, some events are triggered
via a web endpoint and stored in RabbitMQ (please check my other repository https://github.com/mail4hafij/rabbit_event_stream ) so that we are notified by email and have tickets in our Slack channel. 


How to run locally:
This project can be debugged in Visual Studio given you have the docker support enabled. 
https://docs.microsoft.com/en-us/dotnet/standard/containerized-lifecycle-architecture/design-develop-containerized-apps/visual-studio-tools-for-docker

1. src/Dockerfile - It builds the src.
2. docker-compose.yml - It builds the servcie in 'dev' mode in the same network as rabbit_event_stream



1. Checkout the https://github.com/mail4hafij/rabbit_event_stream and run.
2. Open internal_notification_service solution in Visual Studio (in order to start fresh, delete the .vs folder and make sure the docker host is running when opening the solution. 
Then set docker-compose as startup project which will spin up the container). Hit the run button.
3. Go to the rabbit_event_stream/scenarios and run 'dummy_events.js'

