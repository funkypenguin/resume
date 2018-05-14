{
    "title":"Bandersnatch - Jabber Conversation Logger",
    "date": "2001-02-11T12:41:05-05:00",
    "link":"https://www.funkypenguin.co.nz/project/bandersnatch/",
    "image":"/img/deploysonly.gif",
    "description":"Jabber server conversation logger with search, sort, and privacy masking",
    "featured":true,
    "tags":["MySQL","PHP","XMPP"],
    "fact":"Reduce page load time from minutes to instantaneous.",
    "sitemap": {"priority" : "0.8"}
}

In 2003, when I wanted to implement a Jabber server at my [first employer](/#experience), management were afraid that the platform would be abused, and wanted a means to archive all conversations. (_I'd included transports to MSN, ICQ, and Yahoo Messenger_)

To meet this requirement, I developed **[Bandersnatch](https://www.funkypenguin.co.nz/project/bandersnatch/)**, a perl/PHP/MySQL-based conversation logger, named after the nonsensical reference in Lewis Carroll's "[Jabberwocky](https://en.wikipedia.org/wiki/Jabberwocky)".

The perl code was adapted from other code I'd found, the PHP/MySQL interface was developed from scratch. For a while, Bandersnatch was famous - it was even included in Debian/Ubuntu ports, but was abandoned when perl modules it depended upon became deprecated, and jabberd2 introduced native logging capabilities.

(_I also wrote a tutorial re [implementing Bandersnatch](https://www.funkypenguin.co.nz/how-to/generate-logs-from-your-jabberd2-server-using-bandersnatch/)_)
