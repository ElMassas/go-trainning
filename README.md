# Trainning

Base repo to train languagues, skills and specific technologies like protobuffers.

To test out a new languague and understand it I implement the following service:

- A client-server program in which:
    - There is a simple defined **protocol buffer** schema defined for communication.
    - The **client** sends a request with a random string
    - The server recieves said string and analyzes it in order to see the percentage of consonants and vowels. Per each group on consonants and vowels it applies a cypher:
        - If it receives the following string: 'The president of sissy town is ludicrous, but no ludacris'.
        - Remove any special chars and blank spaces.
        - For each sequence of consonants it will perform an increment of 69 x the ammount of consonants. For example: 'Th' would become: 'Þò'
        - For each value change it with the next vowel. For example: 'a' would become 'e' and 'A' would also become 'e'.
        - After the whole string has been altered, apply the md5 hash to it.
    - The **server stores** the computed value in a file with the name of the date in which it was computed.
    - The **server returns** said value to the client
    - Both the **client** and **server** must have proper logging, as well as metrics endpoints to export metrics.
    - The **server** must use gRPC
    - The connection between the client and the server is established using HTTP/2 and SSL/TLS
    - For **observability** the services should make sure to be using OpenTelemetry


**Note**: All the programs must be properly packaged and containerized and deployed, using a simple docker-compose and in a simple kubernetes cluster. 

## Objectives

- Learn how to create a service using the language that:
    - Performs string operations
    - Learn a decent lvl of networking on said language
    - Learn how observability is done in the languague
    - Learn how to package and manage deployment caveats for said language
