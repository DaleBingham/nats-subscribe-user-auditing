# nats-subscribe-user-auditing
An example of a consumer for the NATS message queue (not streaming) receiving user data based on auditing subjects. Works with my nats-publishing-user project.

## Running the NATS docker images
* docker run --rm --name nats-main -p 4222:4222 -p 6222:6222 -p 8222:8222 nats
* this is the default and lets you run a NATS server version 1.2.0 (as of 8/2018)
* just runs in memory and no streaming (that is separate)

## What is required
* .NET Core 2.x
* running `dotnet add package NATS.Client` to add the package
* dotnet restore to pull in all required libraries
* The C# NATS client library available at https://github.com/nats-io/csharp-nats
* The image at https://hub.docker.com/_/nats/