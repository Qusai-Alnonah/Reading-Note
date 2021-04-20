# Reading Summary
today we will take and read bout THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS
ersistent local storage is one of the areas where native client applications have held an advantage over web applications. For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state. These values may be stored in the registry, INI files, XML files, or some other place according to platform convention. If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

What we really want is
<ul>
a lot of storage space
on the client
that persists beyond a page refresh
and isn’t transmitted to the server
</ul>

HISTORY OF LOCAL STORAGE HACKS
they all expose radically different interfaces, have different storage limitations, and present different user experiences. So this is the problem that HTML5 set out to solve: to provide a standardized API, implemented natively and consistently in multiple browsers, without having to rely on third-party plugins.

INTRODUCING HTML5 
HTML5 STORAGE SUPPORT
IE	FIREFOX	SAFARI	CHROME	OPERA	IPHONE	ANDROID
8.0+	3.5+	4.0+	4.0+	10.5+	2.0+	2.0+

*/function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
/*}

USING HTML5 STORAGE.

TRACKING CHANGES TO THE HTML5 
jQuery or some other JavaScript library to register your event handlers, you can do that with the storage event, too.)

BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS
While the past is littered with hacks and workarounds, the present condition of HTML5 Storage is surprisingly rosy. A new API has been standardized and implemented across all major browsers, platforms, and devices. As a web developer, that’s just not something you see every day, is it? But there is more to life than “5 megabytes of named key/value pairs,” and the future of persistent local storage is… how shall I put it… well, there are competing visions.
 do things like this from JavaScript:
 ↶ actual working code in 4 browsers

openDatabase('documents', '1.0', 'Local document storage', 5*1024*1024,
 */function (db) {
  db.changeVersion('', '1.0', function (t) {
    t.executeSql('CREATE TABLE docids (id, name)');
  }, error);
/*});
The Web SQL Database specification has been implemented by four browsers and platforms like:
WEB SQL DATABASE SUPPORT
IE	FIREFOX	SAFARI	CHROME	OPERA	IPHONE	ANDROID
·	·	4.0+	4.0+	10.5+	3.0+	2.0+

# FURTHER READING
http://diveinto.html5doctor.com/storage.html
referance:
HTML5 Storage specification
Introduction to DOM Storage on MSDN
Web Storage: easier, more powerful client-side data storage on Opera Developer Community
DOM Storage on Mozilla Developer Center. (Note: most of this page is devoted to Firefox’s prototype implementation of a globalStorage object, a non-standard precursor to localStorage. Mozilla added support for the standard localStorage interface in Firefox 3.5.)
Unlock local storage for mobile Web applications with HTML5, a tutorial on IBM DeveloperWorks
Early work by Brad Neuberg et. al. (pre-HTML5):

Internet Explorer Has Native Support for Persistence?!?! (about the userData object in IE)
Dojo Storage, part of a larger tutorial about the (now-defunct) Dojo Offline library
dojox.storage.manager API reference
dojox.storage Subversion repository
Web SQL Database:

Web SQL Database specification
Introducing Web SQL Databases
Web Database demonstration
persistence.js, an “asynchronous JavaScript ORM” built on top of Web SQL Database and Gears
IndexedDB:

Indexed Database API specification
Beyond HTML5: Database APIs and the Road to IndexedDB
Firefox 4: An early walk-through of IndexedDB