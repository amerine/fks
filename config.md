Zone configuration commands:

We have defined the following groups:

* `ZONE`:   for zone configuration
* `USER`:   for user management
* `ERROR`:  for error reporting
* `SYSTEM`: for system management?
* `...`:    ...

Better stuff then add and set

# ZONE

In zone we have:

(This will probably all change and use more consistent names)

    ZONE. TXT   "READ origin /path/to/zone"
    ZONE. TXT   "READXFR origin ip(6)-of-master [tsig-secret]"
    ZONE. TXT   "DROP origin"
    ZONE. TXT   "list"

Zones are listed in the additional section of the reply packet

    ZONE. TXT   "zonename1"
    ZONE. TXT   "zonename2"

# USER

    USER. TXT   "ADD miekg"
    USER. TXT   "DROP miekg"
    USER. TXT   "ADDTSIG miekg base64-tsig-secret"
    USER. TXT   "ADDPOWER miekg list"   // list/write/drop
    USER. TXT   "DROPPOWER miekg list"


The config is internally stored in a memory structure (not a Zone).
