# 0x08. Networking basics #1

``DevOps`` ``Network`` ``SysAdmin``

![localhost](https://s3.amazonaws.com/intranet-projects-files/holbertonschool-sysadmin_devops/285/s7kpNYq.png)

In this project I learnt the following:
- ifconfig
- telnet
- nc
- cut

## TASKS

- Task 0
    - [0-change_your_home_IP](https://github.com/BrightTech10/alx-system_engineering-devops/blob/main/0x08-networking_basics_2/0-change_your_home_IP): A Bash script that configures an Ubuntu server with the below requirements.
        - localhost resolves to 127.0.0.2
        - facebook.com resolves to 8.8.8.8

    Example:

    ```Bash
    bright@BRIGHT$ ping localhost
    PING localhost (127.0.0.1) 56(84) bytes of data.
    64 bytes from localhost (127.0.0.1): icmp_seq=1 ttl=64 time=0.012 ms
    ^C
    --- localhost ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 0.012/0.012/0.012/0.000 ms
    bright@BRIGHT$
    bright@BRIGHT$ ping facebook.com
    PING facebook.com (157.240.11.35) 56(84) bytes of data.
    64 bytes from edge-star-mini-shv-02-lax3.facebook.com (157.240.11.35): icmp_seq=1 ttl=63 time=15.4 ms
    ^C
    --- facebook.com ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 15.432/15.432/15.432/0.000 ms
    bright@BRIGHT$
    bright@BRIGHT$ sudo ./0-change_your_home_IP
    bright@BRIGHT$
    bright@BRIGHT$ ping localhost
    PING localhost (127.0.0.2) 56(84) bytes of data.
    64 bytes from localhost (127.0.0.2): icmp_seq=1 ttl=64 time=0.012 ms
    64 bytes from localhost (127.0.0.2): icmp_seq=2 ttl=64 time=0.036 ms
    ^C
    --- localhost ping statistics ---
    2 packets transmitted, 2 received, 0% packet loss, time 1000ms
    rtt min/avg/max/mdev = 0.012/0.024/0.036/0.012 ms
    bright@BRIGHT$
    bright@BRIGHT$ ping facebook.com
    PING facebook.com (8.8.8.8) 56(84) bytes of data.
    64 bytes from facebook.com (8.8.8.8): icmp_seq=1 ttl=63 time=8.06 ms
    ^C
    --- facebook.com ping statistics ---
    1 packets transmitted, 1 received, 0% packet loss, time 0ms
    rtt min/avg/max/mdev = 8.065/8.065/8.065/0.000 ms
    ```

- Task 1
    - [1-show_attached_IPs](https://github.com/BrightTech10/alx-system_engineering-devops/blob/main/0x08-networking_basics_2/1-show_attached_IPs): A Bash script that displays all active IPv4 IPs on the machine it’s executed on.

    Example:

    ```Bash
    bright@BRIGHT$ ./1-show_attached_IPs | cat -e
    172.18.231.177$
    127.0.0.1$
    bright@BRIGHT$
    ```

- Task 2
    - [100-port_listening_on_localhost](https://github.com/BrightTech10/alx-system_engineering-devops/blob/main/0x08-networking_basics_2/100-port_listening_on_localhost): A Bash script that listens on port 98 on localhost.

    Example:

    <b>Terminal 0</b>

    Starting my script.
    ```Bash
    bright@BRIGHT$ sudo ./100-port_listening_on_localhost
    ```

    <b>Terminal 1</b>

    Connecting to ``localhost`` on port ``98`` using ``telnet`` and typing some text.
    ```Bash
    bright@BRIGHT$ telnet localhost 98
    Trying 127.0.0.2...
    Connected to localhost.
    Escape character is '^]'.
    Hello world
    test
    ```

    <b>Terminal 0</b>

    Receiving the text on the other side.
    ```Bash
    sylvain@ubuntu$ sudo ./100-port_listening_on_localhost
    Hello world
    test
    ```
