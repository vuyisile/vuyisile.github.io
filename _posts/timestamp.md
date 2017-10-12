

The timestamp read-only property of the Notification interface returns a DOMTimeStamp, as specified in the timestamp option of the Notification() constructor.

The notification's timestamp can represent the time, in milliseconds since 00:00:00 UTC on 1 January 1970, of the event for which the notification was created, or it can be an arbitrary timestamp that you want associated with the notification. For example, a timestamp for an upcoming meeting could be set in the future, whereas a timestamp for a missed message could be set in the past.

Note: This feature is available in Web Workers.

Syntax

var timestamp = Notification.timestamp;

Value

A DOMTimeStamp.
Examples

The following snippet fires a notification; a simple options object is created, then the notification is fired using the Notification() constructor.

var dts = Math.floor(Date.now());

var options = {
  body: 'Do you like my body?',
  timestamp: dts
}

var n = new Notification('Test notification',options);

n.timestamp // should return original timestamp




4.4. DOMTimeStamp

typedef unsigned long long DOMTimeStamp;

The DOMTimeStamp type is used for representing a number of milliseconds, either as an absolute time (relative to some epoch) or as a relative amount of time. Specifications that use this type will need to define how the number of milliseconds is to be interpreted.
4.5. Function

callback Function = any (any... arguments
);

The Function callback function type is used for representing function values with no restriction on what arguments are passed to it or what kind of value is returned from it.
4.6. VoidFunction

callback VoidFunction = void ();

The VoidFunction callback function type is used for representing function values that take no arguments and do not return any value.
5. Extensibility

This section is informative.

Extensions to language binding requirements can be specified using extended attributes that do not conflict with those defined in this document. Extensions for private, project-specific use should not be included in IDL fragments appearing in other specifications. It is recommended that extensions that are required for use in other specifications be coordinated with the group responsible for work on Web IDL, which at the time of writing is the W3C Web Platform Working Group, for possible inclusion in a future version of this document.

Extensions to any other aspect of the IDL language are strongly discouraged.
6. Referencing this specification

This section is informative.

It is expected that other specifications that define Web platform interfaces using one or more IDL fragments will reference this specification. It is suggested that those specifications include a sentence such as the following, to indicate that the IDL is to be interpreted as described in this specification:

    The IDL fragment in Appendix A of this specification must, in conjunction with the IDL fragments defined in this specification’s normative references, be interpreted as required for conforming sets of IDL fragments, as described in the “Web IDL” specification. [WEBIDL]

In addition, it is suggested that the conformance class for user agents in referencing specifications be linked to the conforming implementation class from this specification:

    A conforming FooML user agent must also be a conforming implementation of the IDL fragment in Appendix A of this specification, as described in the “Web IDL” specification. [WEBIDL]

7. Acknowledgements

This section is informative.

The editor would like to thank the following people for contributing to this specification: Glenn Adams, David Andersson, L. David Baron, Art Barstow, Nils Barth, Robin Berjon, David Bruant, Jan-Ivar Bruaroey, Marcos Cáceres, Giovanni Campagna, Domenic Denicola, Chris Dumez, Michael Dyck, Brendan Eich, João Eiras, Gorm Haug Eriksen, Sigbjorn Finne, David Flanagan, Aryeh Gregor, Dimitry Golubovsky, James Graham, Aryeh Gregor, Tiancheng “Timothy” Gu, Kartikaya Gupta, Marcin Hanclik, Jed Hartman, Stefan Haustein, Dominique Hazaël-Massieux, Ian Hickson, Björn Höhrmann, Kyle Huey, Lachlan Hunt, Oliver Hunt, Jim Jewett, Wolfgang Keller, Anne van Kesteren, Olav Junker Kjær, Magnus Kristiansen, Takeshi Kurosawa, Yves Lafon, Travis Leithead, Jim Ley, Kevin Lindsey, Jens Lindström, Peter Linss, 呂康豪 (Kang-Hao Lu), Kyle Machulis, Mark Miller, Ms2ger, Andrew Oakley, 岡坂 史紀 (Shiki Okasaka), Jason Orendorff, Olli Pettay, Simon Pieters, Andrei Popescu, François Remy, Tim Renouf, Alex Russell, Takashi Sakamoto, Doug Schepers, Jonas Sicking, Garrett Smith, Geoffrey Sneddon, Jungkee Song, Josh Soref, Maciej Stachowiak, Anton Tayanovskyy, Peter Van der Beken, Jeff Walden, Allen Wirfs-Brock, Jeffrey Yasskin and, Collin Xu.

Special thanks also go to Sam Weinig for maintaining this document while the editor was unavailable to do so.
