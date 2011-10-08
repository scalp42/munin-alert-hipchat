Send Munin alerts to HipChat.
-----------------------------

This script converts Munin alerts into messages in a HipChat room.

Put this script somewhere on your Munin master and make it executable. Then
add it as a contact in your Munin configuration like so:

    contact.hipchat.command | [THIS] [THIS] --room=[ROOM] --token=[TOKEN]
    contact.hipchat.always_send warning critical

Replace [THIS] with the full path to this script (yes, it is supposed to be
there twice). Replace [ROOM] with the name or ID of the room where you want
the messages to arrive and replace [TOKEN] with your HipChat token.

Don't forget to add it to your contacts list.

If you want to change the name associated with the message, pass a value for
the --from argument. If you'd like the messages to link back to your Munin
web interface then use --munin-prefix.
