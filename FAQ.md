# What's is the status of libjingle? #

We just released a new version, 0.5, with many updates.  There is now support for video, and the "jingle" standard (XEP-166 and XEP-167).  Also, the license has been changed from GPL to BSD.  There are also lots of bug fixes and performance improvements.

# How does libjingle compare to other XMPP stacks? #

libjingle isn't just an XMPP stack.  It's more a P2P (peer-to-peer) and RTC (real-time communication) stack that builds on XMPP.  If you don't need any P2P or RTC, you can use any XMPP stack.  If you do, then you might want to use libjingle.  In fact, you can even use libjingle on top of another XMPP stack.

For example, if you are building an application that synchronizes data between devices, you can use any XMPP stack to send small chunks of XML through an XMPP server.  But if the data is large, then you'll need a direct socket between the peers.  You'll want libjingle for that.

libjingle is also obviously well suited to interop with Google Talk and other XMPP chat clients that work with the Jingle protocol (http://xmpp.org/extensions/xep-0166.html).

# How does the build of 0.5 differ from 0.4? #

See the README for details.  Basically, you'll need to download one tool and two libraries:

swtoolkit: http://code.google.com/p/swtoolkit/
libsrtp: http://sourceforge.net/projects/srtp/develop
expat: http://sourceforge.net/projects/expat/

# What XEPs does libjingle support? #

Libjingle has basic support for XEP-166 and XEP-167.  It also supports the pre-standard versions of those protocols that Google Talk currently uses (web-based Google Talk will be updated to speak jingle soon).

Libjingle does not yet have support for XEP-176 because it uses a pre-standard version of ICE-UDP.  We're looking at how we can fully implement XEP-176 and ICE-UDP.


# What about the "nextsnap" branch? #

The "nextsnap" branch was temporary, but will be left as-is for those depending on it.  Please move to trunk.