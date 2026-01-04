# layout off file:
~~~
1: shabang
2: run app
~~~

# code
recommended locations for komands
~~~
/usr/bin/<application name>
~~~
files conntent
~~~
#!/usr/bin/bash
flatpak run <appilaciton id> "$@"
~~~
commments:
<application name> : name to use in terminal

<application id> : flatpak id, ex: org.mozilla.firefox

*"$@"* : retuns file *commands* to flatpak, ex : firefox *--private-window op.se* => flatpak run org.mozzila.firefox *--private-window op.se*

# exampel
~~~
# tee /usr/bin/firefox <<EOF
#!/bin/bash
flatpak run org.mozilla.firefox "\$@"
EOF

# chmod +x /usr/bin/firefox
~~~
