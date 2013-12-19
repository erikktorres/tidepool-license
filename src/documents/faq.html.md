--- yaml
layout: 'default'

title: 'The Tidepool License FAQ'

---

### DRAFT

> The [draft Tidepool Open Access to Health Data Software License v1](/index.html) is currently open for public review and comment. This draft FAQ accompanies the license draft. Please email your comments on either one to our license discussion mailing list [tidepool-license-discuss@googlegroups.com](mailto:tidepool-license-discuss@googlegroups.com) or comment on the [associated blog post](http://tidepool.org/2013/09/18/2013917wheres-the-code-or-a-funny-thing-happened-while-on-the-way-to-an-open-source-license/) published September 17, 2013. Even better, feel free to fork [our GitHub repository for this license document and FAQ](https://github.com/tidepool-org/tidepool-license) and offer us an edited version as a pull request.

### Developer

Why did Tidepool choose to create a new open source license?
: We feel strongly that patients should have the right to receive all relevant data about their disease, from all of their applications, services and devices, in both human-readable and machine-accessible forms. We want anyone who chooses to use Tidepool source code in their Software to make a user&rsquo;s health data available.

Doesn’t HIPAA require access to data?
: Yes, HIPAA does require access to personal health data, but it only requires requests for such data to be released within 30 days. We believe that data should be accessible in near-real time and in both human-readable and machine-accessible forms.

Is using the Tidepool License my only choice?
: No, we&rsquo;ve chosen to release Tidepool&rsquo;s software under a dual-license approach. If you choose to use our software, you may choose to comply with either the GNU General Public License v3 or the Tidepool License.
: GPL v3 is a &ldquo;copyleft&rdquo; license that requires you release changes that you make to the software. If you are building a device, it also requires that you provide a mechanism for people to install their own software on the device.
: The Tidepool License is a &ldquo;permissive&rdquo; license, similar to Apache v2 with respect to software source code, but with the addition of a &ldquo;copyleft&rdquo; open health data requirement.

Who does the Tidepool License apply to?
: This license applies to anyone who wishes to incorporate Tidepool software or UI designs in any way, for example in a device, in a mobile app, or in a web-based service or a PC/Mac/Linux desktop application.

What data must I make available?
: The general guiding principle is &quot;it&rsquo;s my disease, so it&rsquo;s my data.&quot; The intent is that all reasonable data be made open, in both human-readable and machine-accessible forms. &quot;Reasonable data&quot; means all data that would help an engaged patient (or their designate) understand their disease or their therapy, including the safety and efficacy of that therapy.

What are examples of the kind of data you expect me to store and make accessible?
: We can&rsquo;t provide exhaustive lists of the data, because we don&rsquo;t yet know all the software that we or others will create. But here are a few examples of the data that must remain &ldquo;open&rdquo; under our license:

   * An insulin pump (as designed by today&rsquo;s standards) would need to make available all settings and all diagnostic information that could reasonably be used to understand the safety and efficacy of its therapy. This would include (but not be limited to): all settings, all &quot;events&quot; (e.g. basal and bolus deliveries, reservoir changes, etc.), bolus wizard parameters, and all useful diagnostic information like pump resistance (occlusion pressure) and battery levels.
   * A continuous glucose monitor would need to make available raw ISIG (interstitial glucose) values, all settings, and the converted blood glucose values.
   * Thinking beyond diabetes, we imagine other projects focused on other diseases might also use the Tidepool License. Data from an implanted cardioverter-defibrillator (ICD) would include things like all defibrillation events, battery charge, capacitor charge times and lead impedance.
   * Everything that is logged should include time stamps (preferably in UTC, please, and keep track of the device&rsquo;s notion of local time!).

Do I need to keep the data forever and make it accessible forever?
: Disk space is cheap so you probably should keep the data forever, but the license only requires you to make the data accessible to the data owner for three years.
: Also, although it&rsquo;s not required by the Tidepool License, you should also probably provide a mechanism for users to request that their personal data be deleted.

I am building a device and want to include Tidepool code on the device. Does this mean I need to store data on the device for three years?
: As long as your device has a protocol for getting data off of the device by the user (e.g. over USB or Bluetooth or some other wireless mechanism), and that data can be stored somewhere else (like on a PC or in the cloud), and accessed in both human-readable and machine-accessible forms, your device would be in compliance with the intent of the Tidepool License.

Am I allowed to encrypt the data?
: Yes, and you probably should on a per-user basis. But if you encrypt the data the user must be able to access it in decrypted form without specialized technical knowledge.

Is it good enough to provide access to a downloadable CSV or excel file?
: <strike>No, that&rsquo;s not good enough. You need to provide a mechanism for another application to automatically access the data, such as through a published API. This is what we mean by &ldquo;machine-accessible.&rdquo;</strike> Yes, that is acceptible, although we also encourage you to provide access to the data through a published API.

Do I need to provide both human-readable and machine-accessible formats?
: Yes.

Can I require that only a human can access the data, not other software?
: No. It should be possible for someone to build an online service for monitoring an individual patient&rsquo;s data. This is what we mean by &ldquo;machine-accessible.&rdquo;

Can I require authentication in order to access the data?
: Yes, and you should. For example, you may require registration (username and password) in order to access the data, or use Oauth, an API key or some similar authentication mechanism.

Is it required that I use an encrypted transmission protocol, e.g. https?
: It is not required by Tidepool, but highly recommended (and is required by regulations like HIPAA).

What if I violate laws by doing this, e.g. HIPAA?
: Nothing about the Tidepool license should cause you to violate laws. Do the right thing.

Do I need to make the data available to all?
: You do not need to make the data available to all, although you may choose to do so by creating an anonymized data set that is openly available. This is not required under the Tidepool License.
: We know there are many factors to consider when handling data. Our license does not attempt to sort all this out. For instance, a person&rsquo;s health data should not be inappropriately made available to others. But our license only requires that the data be available to the individual to whom it pertains, or anyone they designate. In other words, our license requires that you not withhold the data from the user; it doesn&rsquo;t lay out everything you can or cannot do with data.

Is the Tidepool License related to &#8220;Open Access&#8221; or &#8220;Open Data&#8221; ?
: Yes, the Tidepool License leverages the definition of &ldquo;open&rdquo; at opendefinition.org. However, the Tidepool License acknowledges that this health data may be private, and that the user/patient may not want the data to be openly accessible to everyone.

Can I limit the dates/times, e.g. to only 11 weeks worth of data?
: No, the user or any piece of software or person that they grant access to must be able to download all of the data and not be limited to arbitrary date ranges.

Can I throttle API access to the data? I&#8217;m worried about the scalability of our backend.
: Yes, you can throttle API access, and you don&rsquo;t need to plan for infinite API access or server capacity. But should have enough capacity that a reasonable use of your API is allowable. We highly encourage you to use an &quot;elastic&quot; scalable backend service that makes this easy.


