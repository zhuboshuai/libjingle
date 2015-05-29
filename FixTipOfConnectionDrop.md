## Introduction ##

Some users have reported that if a connected client has been set idle for sometime, it'll be disconnected (put to offline) without any log-out request from libjingle.

There is a small workaround to resolve this issue which is to keep sending "keepalives" request to the server periodically.
What you need to do is to set up a timer to call this "keepalives" function at regular intervals, for example 110 seconds in the Google Talk application.

## Details ##

The following is the sample code:

```
void
YourClientUIClass::DoKeepAlive() {
  buzz::XmppClient* client = YourLibjingleApp->GetClient();
  if (client) {
    client->SendRaw(" "); // Just send a space.
  }
}
```