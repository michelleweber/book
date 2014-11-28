

## 22. Speeding up the Release Cycle

Shuttle wasn’t the only project dragging on. There was more than a year between the Shuttle-inspired WordPress 2.0 and the next version, WordPress 2.1. In a [post on his blog](http://ma.tt/2010/11/one-point-oh/), Matt describes the year between 2.0 and 2.1 as “a dark time in WordPress development history, a lost year.”  

WordPress’ release cycle has often been sporadic, particularly in those early days. Sometimes releases just had a few months between them, other times longer. Between 1.2 and 1.5, for example, there was a gap of 265 days. The codebase had so many changes that it was decided to skip a few version numbers, [going straight from 1.2 to 1.5](http://wordpress.org/news/2004/12/version-skip/). This was at a time when version numbers were attached to releases in a haphazard way. The approach that the project adopts now is that the current release is the first two numbers, and each release is a major version. 1.5, 2.0, 2.9, 3.4, and 4.0, for example, all have the same weighting as each other. Patch releases have an additional decimal point - 2.0.1, for example. This is different to the approach taken by many other software projects. Drupal 6 and Drupal 7, for example, are major releases, but the releases with decimal points are not. WordPress’ approach is used to avoid version inflation. Over a period of years, the version number for a piece of software can quickly get high. Decimalisation avoids that.

Between WordPress 1.5 and 2.0, however, the project hadn’t quite settled on its approach to version numbering. 1.6 was inflated to 2.0. partly because of the number of features in it, and also of the 314 days between releases. But the delay between 2.0 (released December 31 2005) and 2.1 (released January 22 2007) was the longest so far.  

The mailing list was active, and more developers than ever were attracted to the project. WordPress itself was downloaded 1.5 million times. But while emails were being sent, no code was actually being shipped. The [release post for WordPress 2.1 with its a plethora of new features](http://wordpress.org/news/2007/01/ella-21/) demonstrates the problem. There wasn’t a rift in development or any major changes in the project, but just a constant desire to slip in just one more feature, a refusal to wait for the next release. The release may have been packed with features but it took more than a year to get there. 
	

The delay led to frustration amongst developers - not simply because the release cycle was taking so long but because commit access was still restricted to Matt and Ryan. For many developers, the delays to development could partly be attributed to the restrictive commit policy. There was a clear difference in opinion about how commit access in the project should be managed. Every free software project approaches commit access differently, and in WordPress itself there was a mixture of people who supported the Linux-style commit policy and those who didn’t. Ryan argued that the [benefit to having funnel](http://lists.automattic.com/pipermail/wp-hackers/2006-March/005192.html) was that it avoided situations in which “bridge burning arguments happen in the repository rather than in ticket comments." Discussions about approach and implementation were had before code touched the repository. When code has landed in the repository it’s harder to remove. An open commit policy brings its own challenges and some who’d been involved with open commit free software projects [supported the funnel](http://lists.automattic.com/pipermail/wp-hackers/2006-March/005195.html). "Loose control leads to spaghetti code and flame wars over inconsequential issues," wrote Douglas Daulton, in a post to wp-hackers.

In the context of these discussions, Ryan [codified elements of the project’s process that remain part of the development process today](http://lists.automattic.com/pipermail/wp-hackers/2006-March/005190.html):

- every commit must be accompanied by a ticket
- before commit, the code is reviewed by at least two people - one for a code review and the other for an integration/architecture review
- these reviews are carried out by trusted contributors.

Incremental, positive changes were happening. Ryan suggested that a #wordpress-dev channel could help facilitate discussion around development. The #wordpress channel had become a place for general chatter and support. This meant that the focus wasn’t primarily on development. Mark Jaquith [pointed out the success of the Bug Gardening scheme](http://lists.automattic.com/pipermail/wp-hackers/2006-March/005189.html) which had started the previous year during previous discussions about opening up commit. By opening up trac privileges to “bug gardeners” who were responsible for triaging tickets the workload had become distributed and led to "a whole slew of people who are autonomously fixing bugs, submitting  patches, and having them committed." Another positive change was the trac mailing list, which transformed trac from simple bug-tracking software to a locus for discussion. This kept discussion focused on specific tickets and issues, somewhat curtailing the tendency on wp-hackers for discussion to meander into rabbit holes. 

As work on WordPress 2.1 was under way, Ryan posted to wp-hackers about [getting WordPress 2.0 into Debian stable](http://lists.automattic.com/pipermail/wp-hackers/2006-October/008871.html). Debian is a free and open source operating system distribution. The stable version is the latest official version of the software. WordPress was already in the testing and unstable distributions which both contain packages that are lined up for inclusion in the stable version. To be included in the stable distribution, WordPress 2.0 would need to be maintained for 3-5 years. This involved backporting security issues to ensure that the version remained stable. Mark Jaquith took on the task of maintaining the WordPress 2.0 branch. The project committed to maintaining the version for three years, until 2010. 

Shortly after he took leadership on the legacy branch, [Mark Jaquith was given commit access.](https://core.trac.wordpress.org/changeset/4270). Mark had been involved with WordPress since 2004, coming to the project along with the exodus from Movable Type. In his two year involvement with the project he’d made a number of contributions, including to the successful bug gardening scheme. It was a sign that the funnel was starting to broaden, and the beginning of a period when, slowly but surely, more committers were added.

Commit access was given out sparing because it wasn’t just given out on the basis of coding expertise or how much work a developer had done. Adding a new committer meant trusting them to follow through with the vision of the project, to be someone sympathetic to the project’s user-first ethos. Then, and now, that’s a key factor in deciding who is given commit access. “It’s not just that you’ve shown a commitment to contributing,” says Peter Westwood ([westi](http://profiles.wordpress.org/westi)) now, “but you also have shown an understanding of the ethos of the community and their shared beliefs, and their philosophies.”

Despite adding another committer, the development cycle wasn’t significantly sped up, and the team decided to take a more serious look at how development process operated. Since WordPress’ first release, new versions had been arriving haphazardly, and as the number of users and developers grew the outside impression of the project was that it was somewhat chaotic. There was no real structure or process to development. 

A discussion was started wp-hackers about [moving to a 120 Day release cycle](http://lists.automattic.com/pipermail/wp-hackers/2006-October/008907.html). Matt wrote about what he thought a release should look like:	

> 2 months of crazy fun wild development where anything goes
> 1 month of polishing things a little bit, and performance
> Feature freeze.	
> 1 month of testing, with a public beta release at the beginning	

The community’s response was positive. This provided a concrete deadline for them to work toward. Having shorter release cycles also meant that if a feature was holding up a release it could be pushed to the next one. In theory, this should prevent there from being any more delays, in practice this often depended on what the feature was, how far along development of that feature was, and who was spearheading that feature.

When WordPress 2.1 shipped, it was the first to launch with a concrete release date for the next version: [April 23rd for WordPress 2.2](http://wordpress.org/news/2007/01/ella-21/). The publication of the release date meant that the project now had a deadline which it was beholden to. Anyone who followed WordPress’ development would be expecting to see the next version land on that date. A deadline, amongst some in the project, came to be seen as a promise to users - a promise that the next version would appear at a specific time so that users could plan around it. The project didn’t quite make the next deadline - but were only a few weeks out, with WordPress 2.2 [released on 16 May](http://wordpress.org/news/2007/05/wordpress-22/). 
