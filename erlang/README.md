# Erlang code for RabbitMQ tutorials #

Here you can find a Erlang code examples from [RabbitMQ
tutorials](https://www.rabbitmq.com/getstarted.html).

This code is using [RabbitMQ Erlang
Client](https://github.com/rabbitmq/rabbitmq-server/tree/main/deps/amqp_client) ([User
Guide](https://www.rabbitmq.com/erlang-client-user-guide.html)).

## Requirements

To run this code you need at least [Erlang
R13B03](https://www.erlang.org/downloads), on Ubuntu you can get it
using apt:

    sudo apt-get install erlang

You also need rebar3: https://www.rebar3.org/docs/getting-started/

You need Erlang Client binaries:

    make all

## Code

[Tutorial one: "Hello World!"](https://www.rabbitmq.com/tutorials/tutorial-one-python.html):

    ./send.erl
    ./receive.erl

[Tutorial two: Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html):

    ./new_task.erl "A very hard task which takes two seconds.."
    ./worker.erl

[Tutorial three: Publish/Subscribe](https://www.rabbitmq.com/tutorials/tutorial-three-python.html):

    ./receive_logs.erl
    ./emit_log.erl "info: This is the log message"

[Tutorial four: Routing](https://www.rabbitmq.com/tutorials/tutorial-four-python.html):

    ./receive_logs_direct.erl info
    ./emit_log_direct.erl info Hello

[Tutorial five: Topics](https://www.rabbitmq.com/tutorials/tutorial-five-python.html):

    ./receive_logs_topic.erl "*.rabbit"
    ./emit_log_topic.erl red.rabbit Hello
