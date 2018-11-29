# Web Development Checklist for Go-Live

## About

This page is designed to provide a list of questions and actions that should have been considered before launching a web site. It isn't designed to provide _all_ the answers and it isn't necessarily geared towards any specific role (although there are a lot of technical tasks on the list), but if you're trying to launch a website you should at least have an _opinion_ on the things listed here. Even if that opinion is, "No, that's not relevant to our particular endeavour".

## Content Dependent Questions

*   [Has a sitemap been generated?](#sitemap)
*   [Has the spelling for all content been checked?](#spelling)
*   [Is punctuation and capitalisation consistent across pages?](#punctuation)
*   [Have we made sure there is no filler text on any of the pages?](#filler-text)
*   [Have we made sure there are no filler images?](#filler-img)
*   [Have we made sure there no inline css or javascript?](#inline)
*   [Is the markup and css valid? Or is the reason it's invalid acceptable?](#validator)
*   [Is there a print css file?](#print)
*   [Have we tested any required plugins in a browser without plugins installed?](#plugins)
*   [Have we made sure no content has been copied in with extra formatting?](#formatting)
*   [Is all content rendered as appropriate charset?](#charset)
*   [Have images been saved as appropriate extensions and quality?](#extensions)
*   [Are all the links valid and go to correct locations?](#links)
*   [Have we made sure any downloadable files have been uploaded to the server?](#downloads)
*   [Has a 404 page been created?](#page404)
*   [Has a 500 page been created?](#page500)
*   [Has a favicon been created?](#favicon)
*   [Do all images have proper alt text atributes?](#alt)
*   [Do all links have descriptive text and proper title attributes?](#titles)
*   [Does all text fall back to being rendered in a web font?](#web-font)
*   [Have we made sure there is only one level one heading on each page?](#heading)
*   [Has micro-content been created for all user interaction messages?](#micro-content)
*   [Are css and javascript files minimised?](#minimised)
*   [Have we added appropriate page analytics?](#analytics)
*   [Have we removed any debug messages?](#debugging)
*   [Does the site match the design](#design)
*   [Have we tested the content at expanded text size?](#resize)
*   [Have we tested the pages at the most common screen resolutions?](#resolution)
*   [Have we varied content quantity in content panes to make sure the design fidelity is maintained?](#content-quantity)
*   [Have we tested javascript form validation?](#validation)
*   [Have we tested other javascript functionality?](#functionality)
*   [Does the site functionality work with javascript turned off?](#progressive)
*   [Confirm media plays (audio, video)](#media)
*   [Utilise canonical urls where appropriate](#canonical)
*   [Confirm responsive breakpoints and usability](#responsive)
*   [Run automated performance tests on primary pages](#performance)
*   [Confirm all standard HTML5 elements have appropriate stylings](#elements)
*   [Implement social media meta tags (twitter cards, open graph) for shareable content](#sharing)
*   [Confirm appropriate entities (recipes, events, people, etc) have been marked up with associated schema.org ontologies](#schema)
*   [Confirm Client owns and publishes to associated social media accounts](#social-accounts)
*   [Have we created legal and privacy pages and do they contain correct content?](#legal)

## Server Dependent Questions

*   [Do we have required account details details?](#accounts)
*   [Do we have database details?](#database)
*   [Have we made a backup of the live site and the live database?](#backup-live)
*   [Do we have a sql file for generating any databases and content?](#db-schema)
*   [Do we know the DNS and hosting provider have details for a contact for each?](#hosting)
*   [Do we know the exact URL the site is to exist on?](#url)
*   [Have we enabled CORS if required for cross domain frontend queries?](#cors)
*   [Have we enabled monitoring on application and infrastructure?](#monitoring)
*   [Do we have an automated deployment pipeline or understand the steps needed to move the application into Production?](#deployment)
*   [Do we know how to easily and gracefully rollback to a previous depoyment?](#rollback)
*   [Do we know how to migrate the DB and any DB changes?](#migration)
*   [Do we know what caching we need to enable?](#caching)
*   [Have we published an RSS feed? Has it been tested in an RSS Reader?](#rss)
*   [Do we have a plan for how we will handle future updates to plugins, modules, core frameworks or CMS?](#updates)
*   [Does the client have ownership of the accounts used for third party integrations and licensing? Have we confirmed we're using those accounts and associated secrets/keys in our calls?](#ownership)
*   [Have we made sure there are no keys, secrets, API credentials, passwords, usernames or similar commited to our source control?](#privacy)
*   [Have we tested user creation lifecycle? As both an Admin as a user signing up?](#lifecycle)
*   [Have we confirmed emails are being sent by the system appropriately?](#email)
*   [Have we removed all debug messages?](#debug-server)
*   [Have we set up logging of critical errors?](#logging)
*   [Do we have any dependencies or classes that need to be installed on the server?](#dependencies)
*   [Are we using appropriate versions of all the technology we have used?](#versions)
*   [Do we have access to any third party APIs or external dependencies that we use?](#external)
*   [Have we made sure the database doesn't have any test data in it?](#test-data)
*   [Have we set appropriate permissions on any directories that users can upload to?](#permissions)
*   [Have we confirmed that users can't upload malicious files?](#file-security)
*   [Have we made sure that uploaded files are renamed to prevent overwriting?](#rename-files)
*   [Are css and javascript files gzipped?](#gzip)
*   [Have we tested any forms for server validation?](#server-validation)
*   [Have we cleaned all data received from the user?](#clean)
*   [Are we certain any mail functionality is protected from spammers?](#email-spam)
*   [Have we made sure that any mails from the server are not being sent to spam folders?](#spam)
*   [Have we set up any appropriate 3** redirects?](#redirects)
*   [Have we set up any required server analytics?](#sever-analytics)
*   [Has a robots.txt file been generated?](#robots)
*   [Have we run load and stress tests?](#stress)
*   [Have we checked the slow query log for the database?](#slow)
*   [Are private urls appropriately protected?](#private)
*   [Have any required administrators or users been created?](#user-creation)
*   [Have we purchased and installed any required SSL certificates?](#ssl)
*   [Is there a backup procedure in place?](#backup)
*   [Have we successfully restored from backup?](#restore)
    *   [Really?](#really)

## Content Dependent Question Details

### Has a sitemap been generated?

Google has produced excellent documentation on [sitemap generation](https://support.google.com/webmasters/answer/183668?hl=en) which can be used to produce a sitemap that allows easy crawling for spiders as well as easy navigation for some users.

### Has the spelling for all content been checked?

Check all written content for spelling and grammatical errors. There are a few online apps that are available

*   [Online spellchecker app](http://www.spellchecker.net/spellcheck/)
*   [Typosaur.us](https://typosaur.us/)

### Is punctuation and capitalisation consistent across pages?

Check content for consistency across all pages. Written style and voice should remain consistent as well as capitalisation of any specific terms or proper nouns used on the site.

### Have we made sure there is no filler text on any of the pages?

Go through each page of the site and confirm that no filler or 'Lorem Ipsum' text exists anywhere, especially watch out for footer text, image descriptions or text designed to appear on user specified actions such as help text that appears on rollover.

### Have we made sure there are no filler images?

Many backend and frontend developers will use standardised images such the [Dynamic Dummy Image Generator](http://dummyimage.com/) when they are coding up designs. Go through each of the pages and make sure that the images in place are ones specified by the client for that position.

### Have we made sure there no inline css or javascript?

Make sure that CSS and javascript are not attached explicity to the markup and elements of the page. Firefox has an extension that allows us to easily check this per page - [Inline Code Finder](https://addons.mozilla.org/en-US/firefox/addon/9640). There is also a [Chrome extension](https://chrome.google.com/extensions/detail/lfllandeffkmadbndfckhdbkekdfahom/) which does the same thing.

### Is the markup and css valid? Or is the reason it's invalid acceptable?

Run the pages through the [W3C validtor](http://validator.w3.org/) or install the [Firefox validator add-on](https://addons.mozilla.org/en-US/firefox/addon/249) to test the page code and css of the site. Be aware however that there may be valid reasons for markup and css to fail an automated checker. For example:

*   WAI-ARIA attributes will not validate on the majority of X/HTML validators but it is recommended that ARIA is used despite this for the increased usability it gives screenreaders.
*   Browser specific css properties will cause the css to not validate but it's generally better to use them anyway for designs that require them.

### Is there a print css file?

It's important to provide users with a print version of important content that strips out any extraneous content and design. Make sure a print stylesheet exists on pages that users are more likely to print.

`<link rel="stylesheet" type="text/css" media="print" href="print.css" />`

### Have we tested any required plugins in a browser without plugins installed?

There should be alternative or fallback content for anything content that requires plugins or at the very least instructions on what the user has to do in order to access the plugin required content.

### Have we made sure no content has been copied in with extra formatting?

Pasting from word docs for example adds garbage xml code to the markup. It doesn't always show up from a content or design perspective but it can break the site in unexpected and unusual ways. Avoid it by first pasting any content we've copied from word into a plain .txt file such as that created bu 'notepad' before copying it from the text file and pasting it into the site. Make sure other content hasn't been copied in from other sources with associated HTML elements or formatting.

### Is all content rendered as appropriate charset?

Often a byproduct of pasting content from word is that strange characters sometimes appear in the content. We may get these from other sources as well so it is important to always check the content is encoded to the appropriate characterset. It's fairly easy to find more indepth [information on charactersets](http://www.w3.org/International/getting-started/characters) . In general sites and content should be saved and encoded to the UTF-8 charset.

### Have images been saved as appropriate extensions and quality?

Make sure any background images or images used in content are of the appropriate filetype and size. Filesizes should be kept as small as possible for ease of user bandwidth and server load.

### Are all the links valid and go to correct locations?

Run the page through the [W3C link validator](http://validator.w3.org/checklink) or through a [site-wide linkchecker](http://www.dead-links.com/) ; remembering that the site-wide versions can often hammer the hosting server.

### Have we made sure any downloadable files have been uploaded to the server?

If the site has any files that users can download, make sure that the appropriate files are uploaded to the correct locations and named appropriately.

### Has a 404 page been created?

Creating a custom 404 page helps usability enormously. We can assign the location of a custom 404 page with the following line in an .htaccess file on the server:

`ErrorDocument 404 http://www.yoursite.com/custom_page.html`

### Has a 500 page been created?

Users should never be exposed to server or internal error messages so a custom page for server errors should be generated. We can assign the location of a custom 500 page with the following line in an .htaccess file on the server:

`ErrorDocument 500 http://www.yoursite.com/custom_page.html`

### Has a favicon been created?

A Favicon is a little custom icon that appears next to a website's URL in the address bar of a web browser. Create a 16*16px .ico file (modern browsers can handle .gif and .png as well) called favicon and plac it in the root directory of the site.

### Do all images have proper alt text atributes?

Any image that isn't a spacer should have a descriptive alt text for screenreaders. We can also use the WAI-ARIA role 'presentation' to indicate to screenreaders that the should ignore that element. For example:

`<div role="presentation" class="clear" ></div>`

### Do all links have descriptive text and proper title attributes?

Screenreader users often get a list of all links on a page so they can navigate sites quickly rather than have to listen through all the content to find what they want. When they are searching through a list of links titles and descriptions like 'click here' and 'read more' are not very useful and can be very confusing. Make sure that all links on a page are described properly for understanding where they go when read away from their surrounding context.

### Does all text fall back to being rendered in a web font?

If possible, all text on a page should be marked up as text in a [web safe font](http://en.wikipedia.org/wiki/Core_fonts_for_the_Web) . If the design utilises a custom font make sure we have the appropriate licensing for it and that it downloads correctly for the user.

### Have we made sure there is only one level one heading (h1) on each page?

Mostly useful for SEO purposes; it's important that each page only has a single h1 element, additionally subsequent headings should follow the correct order (h2 should come before h3). This recommendation can be ignored if we're using HTML5 which takes into account heading number and how many levels of `section` surround it.

### Has micro-content been created for all user interaction messages?

Make sure that all small pieces of content that might not have been recognised during IA have been approved and spellchecked. The following situations should be considered as a minimum to check for:

*   Error messages
*   Welcome messages
*   Login messages
*   Logout messages
*   Zero results search messages
*   Action success messages
*   Action confirmation messages
*   Action failure messages

### Are css and javascript files minimised?

Make sure css files and javascript files have been run through a production build script that provides a minimised version of both.

### Have we added appropriate page analytics?

Make sure any required [google analytics](http://www.google.com/analytics/) or any other javascript tracking has been added to the pages.

### Have we removed any debug messages?

Any javascript console.log or alert messages should be removed from the code.

### Does the site match the design?

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from a graded browser support list.</span>

### Have we tested the content at expanded text size?

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from a graded browser support list.</span>

### Have we tested the pages at the most common screen resolutions?

We can use the browser developer toolbar to resize the browser to the most common screen resolutions. Try to check in at least 800*600, 1024*768, 1280*1024 and 1600*1200.

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from a graded browser support list.</span>

### Have we varied content quantity in content panes to make sure the design fidelity is maintained?

Different amounts of text in boxes of a fixed height or width may break the layout of the page, so test varied content amount in any element that will hold text.

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from a graded browser support list.</span>

### Have we tested javascript form validation?

Check any forms for client-side validation. Some, but not all, things to check for include:

*   Email confirmation boxes match.
*   Password confirmation boxes match.
*   Required fields are filled out.

Client-side javascript validation should be very 'soft' (as in it shouldn't do any complex validation of data - this should be resereved for server-side validation).

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from graded browser support list.</span>

### Have we tested other javascript functionality?

Javascript functionality such as tabs, image carousels, accordions, datepickers, show/hide scripts and other such usability additions need to checked on eahc page to make sure they for a variety of content.

<span class="warning">This is a browser dependent issue and needs to be checked across the browsers listed in our contract or from a graded browser support list.</span>

### Does the site functionality work with javascript turned off?

Any additional javascript usability functionality needs to provide alternative and equivalent functionality for users with javascript turned off. This doesn't mean the experience has to be the same, just that there has to be some way for everyone to access the same content. For example an image carousel with javascript turned off may just load a single image and then provide a link through to a seperate page that allows access to any extra images.

### Confirm media plays (audio, video)

Test real content, especially in cases where files are uploaded in order to make sure correct filepaths and loading of media occurs.

### Utilise canonical urls where appropriate

In instances of multiple pages on the site having duplicate content, make sure that there is a single, master page that can be designated as 'canonical' for the purposes of search engines. Read more about canonical usage as [Moz](https://moz.com/learn/seo/canonicalization) or [Goggle support](https://support.google.com/webmasters/answer/139066?hl=en)

### Confirm responsive breakpoints and usability

Ideally the site utilised a [mobile first design/development process](https://www.uxpin.com/studio/blog/a-hands-on-guide-to-mobile-first-design/) and we have a clear matrix of mobile/browser versions to test against.

### Run automated performance tests on primary pages

There are a number of automated tools that can be used to help target specific issues that of worth focusing on.

Some tools include:

*   [Google Lighthouse](https://developers.google.com/web/tools/lighthouse/) [General overview]
*   [Google structured data validation](https://search.google.com/structured-data/testing-tool/u/0/) [Schema validation]
*   [Observatory](https://observatory.mozilla.org/) by Mozilla [Security]
*   [Sizzy](https://sizzy.co/) [Responsive design]
*   [AChecker](https://achecker.ca/checker/index.php) [Accessibility]
*   [Tenon](https://tenon.io/) [Accessibility]

### Confirm all standard HTML5 elements have appropriate stylings

It's a good idea to have a standard content page that contains instances of every possible element that we can use to validate designs and functionality. Check each element has been considered within the design and has an appropriate treatment. [This is agood example page detailing HTML5 elements](https://github.com/cbracco/html5-test-page), and [here is a hosted version](https://www.webdevelopmentchecklist.com/content.html)<a>.</a>

<a>

### Implement social media meta tags (twitter cards, open graph) for shareable content

</a>

<a>Include</a> [appropriate meta tags](https://yoast.com/advanced-technical-seo-social-image-ogimage-tags/) within the head of the page to facilitate sharing across social sites.

### Confirm appropriate entities (recipes, events, people, etc) have been marked up with associated schema.org ontologies

Certain schema entities are currently actively used by Google and others to improve search results and others are in the process of being implemented into other pieces of functionality. It's worth implementing schema.org entities even on schemas that aren't currently implemented in search functionlity as it's likely they will be used in the future and they help search engines clearly identify our content.

### Confirm Client owns and publishes to associated social media accounts

If we have icons on the site that are intended to point to company assets, make sure the company< owns the account in question and actively publishes to it and checks it.

### Have we created legal and privacy pages and do they contain correct content?

Pages that contain important legal and privacy related information should be created and kept up-to-date.

## Server Dependent Question Details

### Do we have required accounts details?

Have we confirmed what we need to be able to log in and upload to the host server? Have firewalls been configured? Do we need to set up a secure tunnel before we can ssh in? Do we have accounts, passwords and appropriate permissions for the actual services we need to use to deploy (SFTP, ssh, source control)

### Do we have database details?

Make sure we have database username and password and any extra details we need to set up and utilise the live database; including who is responsible for it, how it can be accessed by developers and any extra issues that may be involved.

### Have we made a backup of the live site and the live database?

Zip up the live site and associated database and data in a safe location, formally and named on proper naming conventions.

### Do we have a sql file for generating any databases and content?

Make a .sql file from phpmyadmin or from the mysql command line.

### Do we know the DNS and hosting provider have details for a contact for each?

Is hosting being managed internally or externally? Has it been configured and are we able to access the required infrastrcuture? Do we have an account and permissions to create other infrastructure or configure domain redirects if required?

### Do we know the exact URL the site is to exist on?

Do we know if mutiple urls need to be configured? Has the URL been purchased? Do we know account details for how to access the domain registrar and when and how the domain may need to be renewed?

### Have we enabled CORS if required for cross domain frontend queries?

If we have an API that is designed to be accessed by javascript on a separate domain (including subdomain) we need to [enable CORS](https://enable-cors.org/) to allow frontend code to access the required data.

### Have we enabled monitoring on application and infrastructure?

Make sure there is appropriate monitoring to determine issues in advance for each layer. There's no point only monitoring at a server layer if our application is serving endless 500 errors to anyone trying to access it. Make sure any automated alerts are being sent to someone who can action them.

### Do we have an automated deployment pipeline or understand the steps needed to move the application into Production?

We should endeavour to automate as much of deployment as possible so we can minimise likely human error. Do we know how our pipeline works? What needs to be configured? Who is responsible for activating the build?

### Do we know how to easily and gracefully rollback to a previous depoyment?

If a critical error occurs in deployment we need to be able to easily fall back to the previous version that worked. If possible this should be part of our automated delivery pipeline.

### Do we know how to migrate the DB and any DB changes?

Do we have an automated way to deply changes or updates to our DB to minimise human error and to ensure that nothing is missed?

### Do we know what caching we need to enable?

Do we have a clear picture of caching layers used by application, database and infrastrcuture? Do we know how to configure them and how they might affect testing and updates?

### Have we published an RSS feed? Has it been tested in an RSS Reader?

Certain content suits delivery via RSS andshould be supplied for those people who wish to subscribe. Make sure the output of the RSS feed is correct by testing it in a third party RSS reader as content is published.

### Do we have a plan for how we will handle future updates to plugins, modules, core frameworks or CMS?

If we are using third party code we need to have a plan for being able to update it as required. This includes potential critical security updates. We also need to make sure we sign up for any available notifications of updates from those third parties so we know the roadmap of their releases and can plan accordingly.

### Does the client have ownership of the accounts used for third party integrations and licensing? Have we confirmed we're using those accounts and associated secrets/keys in our calls?

Make sure that we aren't using test accounts for third parties and APIs in production. Make sure that we have licensing in place that covers our expected usage of APIs or paid services.

### Have we made sure there are no keys, secrets, API credentials, passwords, usernames or similar commited to our source control?

Confirm that we are storing account and password information used to access services and APIs appropriately and accessing it only through variables in configuration files - never hard coded.

### Have we tested user creation lifecycle? As both an Admin as a user signing up?>

Make sure we run basic functionality tests against high value tasks. Create a user as an Administrator in the system to confirm it works. Complete the same as a user of the system to make sure that all aprts of the user journey function. This includes confirmation and change password journeys.

### Have we confirmed emails are being sent by the system appropriately?

Make sure we are receiving confirmation or automated emails from the application. This includes both user journey emails that are part of the customer lifecycle as well as notification emails that may be sent by monitoring or automated processes.

### Have we removed all debug messages?

Make sure we have removed any print or echo statements from server scripts and turned off any debug variables.

### Have we set up logging of critical errors?

Add logging for any raised errors that need to be captured. Make sure none of the critical error messages are raised to the client.

### Do we have any dependencies or classes that need to be installed on the server?

Make sure that any extra functionality that we need is installed on the live site (image manipulation, pdf makers, batabase servers, etc, etc).

### Are we using appropriate versions of all the technology we have used?

Make sure we've been developing to the correct technology versions. Nothing like developing locally in PHP5 and discovering the live server only has PHP4, for example.

### Do we have access to any third party APIs or external dependencies that we use?

Make sure any application keys we use to access external APIs are set up with a live version rather than a developer one. Any live firewalls may need to be configured to allow access to third parties.

### Have we made sure the database doesn't have any test data in it?

Try to start with a totally clean database if possible, otherwise make sure that any test data in it has been deleted before the client sees it.

### Have we set appropriate permissions on any directories that users can upload to?

Make sure directories that are supposed to allow file uploads can actually write the files to the system. See [this answer on SuperUser Stackexchange](https://superuser.com/questions/581194/setting-correct-permissions-for-uploading-files)

### Have we confirmed that users can't upload malicious files?

Check for explicit mime type rather than relying on file extensions before allowing users to upload files to the server.

### Have we made sure that uploaded files are renamed to prevent overwriting?

Rename any user uploaded files to remove non-alphanumeric characters, spaces and then rename the file with the current datetime before writing it to disk to prevent two files with the same name from being overwritten.

### Are css and javascript files gzipped?

Compress any client served files if possible.

### Have we tested any forms for server validation?

Server validation should be more robust than client-side validation and we may need to test complex business rules within the form.

### Have we cleaned all data received from the user?

Never trust any data that could have come from the client.

### Are we certain any mail functionality is protected from spammers?

If there is any 'send to friend' or 'contact us' email functionality in the site, make sure that the sending of email is protected from hacking attempts such as adding extra addresses through the form or writing a script to send multiple emails very quickly.

### Have we made sure that any mails from the server are not being sent to spam folders?

Confirm the correct headers are being sent on any automated emails so that they are not regulated to the receiver's spam folder.

### Have we set up any appropriate 300 redirects?

Ensure any old links redirect to new pages.

### Have we set up any required server analytics?

Configured DB logs, web and server traffic tracking and any extra packages needed to monitor the server and database.

### Has a robots.txt file been generated?

Place a robots.txt file in the root directory indicating which areas of the site crawlers should ignore

### Have we run load and stress tests?

Run a server stress test such as [flood](http://httpd.apache.org/test/flood/) to check the server performs under load.

### Have we checked the slow query log for the database?

Check the slow query log for any queries that can be cleaned up to improve performace and to prevent massive site slowdown.

### Are private urls appropriately protected?

Make sure any url that is supposed to be private requires login or redirects to somewhere else.

### Have any required administrators or users been created?

Any database additions that need to be added so the client can login and view/use administration or cms functionality should be created.

### Have we purchased and installed any required SSL certificates?

Ensure any required security is protected by https and an associated SSL certificate. Test the validity of installed SSL with [a verification tool](https://www.digicert.com/help/)

### Is there a backup procedure in place?

Make sure periodic, automatic backups of the server and database work correctly.

### Have we successfully restored from backup? Of both the application and the database?

Make sure we have successfully restored the entire system from an existing backup to confirm the backup and restore procedure work.

#### Really?

No, really. Make sure this has been confirmed. We do not want to see a [situation like this](http://superuser.com/questions/82036/recovering-a-lost-website-with-no-backup).