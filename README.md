              __       __    __
    .--.--.--|__.-----|  |--|  |--.-----.-----.-----.
    |  |  |  |  |__ --|     |  _  |  _  |     |  -__|
    |________|__|_____|__|__|_____|_____|__|__|_____|
                                       version 3.1.1

    Build composable event pipeline servers with minimal effort.


    ======================
    wishbone.module.input.zmqpull
    ======================

    Version: 0.2.0

    Pulls events from one or more ZeroMQ push modules.
    --------------------------------------------------


        Expects to connect with one or more wishbone.input.push modules.  This
        module can be started in client or server mode.  In server mode, it waits
        for incoming connections.  In client mode it connects to the defined
        servers.  Events are spread in a round robin pattern over all connections.

        Parameters:

            - mode(str)("server")
               |  The mode to run in.  Possible options are:
               |  - server: Binds to a port and listens.
               |  - client: Connects to a port.

            - interface(string)("0.0.0.0")
               |  The interface to bind to in server <mode>.

            - port(int)(19283)
               |  The port to bind to in server <mode>.


        Queues:

            - outbox
               |  Events arriving from the outside.


