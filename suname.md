[return](switching)

:suname:

difference between su - username and su username if <-> or
<-l> is specified, su simulates a real login_the environment
is cleared except for a few select variables (TERM notably,
DISPLAY and XAUTHORITY on some systems)_otherwise the
environment is left as it is except for PATH that is reset.

for <su -> compared to <su - root>, the difference between
passing no user name and specifying root this might be
system-dependent. On Linux with shadow as the package
providing su, if no username is specified, then su first
tries to see if user root has a passwd entry_if it does, it
uses that. If it doesn't, it tries uid 0

not sure about other unix-like operating systems.
