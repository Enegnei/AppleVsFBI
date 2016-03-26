# #AppleVsFBI
An overview of the important facts in the Apple vs. FBI case, including the main technical &amp; legal concerns

***
#### A: [What important events led to this case?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#what-important-events-led-to-this-case)
1. [Before the Attack](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#before-the-attack)
2. [After the Attack](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#after-the-attack)
3. [The Trial](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#the-trial)

#### B: [Is the FBI demanding Apple "break encryption"?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#is-the-fbi-demanding-apple-break-encryption)
1. [What 'encryption' are we dealing with here?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#1-what-encryption-are-we-dealing-with-here)
2. [Why does this distinction matter?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#2-why-does-this-distinction-matter)

#### C: [What are the technical & legal concerns involved?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#what-are-the-technical--legal-concerns-involved)
1. [Technical Concerns](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#technical-concerns)
  * [What are the limits to the use of FBiOS?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----what-are-the-limits-to-the-use-of-fbios---)
  * [Could a secure password protect against FBiOS?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----could-a-secure-password-protect-against-fbios---)
2. [Legal Concerns](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#legal-concerns)
  * [What is the history behind Apple's compliance with law enforcement?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----what-is-the-history-behind-apples-compliance-with-law-enforcement---)
  * [What are important factors in legal precedent(s) for the future?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----what-are-important-factors-in-legal-precedents-for-the-future----)

***

## What important events led to this case?

+ On December 2nd, 2015, Farook and his wife Malik killed 14 people and injured 22 at the Inland Regional Center in California 
during a San Bernardino County Department of Public Health training session/ party. They were pursued by police and died hours later in a shoot-out. The iPhone now in question (a 5C with iOS9) was found by law enforcement in a Black Lexcus IS300 ([see lines 23-4 of pgs 4-5](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

#### Before the Attack

+ The phone was the property of Farook's employer, the **San Bernardino County Department of Public Health**. 
It had been issued to Farook for work & the County still retained official ownership of the phone at the time of the attack ([see lines 22-24 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), but for some reason *had neglected to install mobile-device management software which was standard on their government-issued work phones* & would have 
[enabled the IT department to remotely unlock the device without user assistance](https://web.archive.org/web/20160220095658/http://mobile.reuters.com/article/idUSKCN0VS2QK).

> "If that particular iPhone was using MobileIron, the county's IT department could unlock it," MobileIron Vice President Ojas Rege told Reuters... If it had been, the high stakes legal battle that has pitted Apple and much of the technology industry against the U.S. government could have been avoided altogether.

+ The FBI has not said this phone was used to communicate with other terrorists (Farook is believed to have used another private phone for that, which was destroyed), but rather with his wife and/ or *future victims* ([see lines 16-18 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)). 

![iCloudbackup](https://pbs.twimg.com/media/CbfRFpiUkAA07La.png)

+ The last date the FBI was able to obtain in the iCloud backup data was **October 9th 2015**, through Farook's account ([see top of pg 11 or line 12 of pg 22](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), as iCloud data on Apple's servers is *not* protected by the user's iPhone passcode. The FBI states that Farook [changed his iCloud password & disabled the iCloud automatic-backup feature on **October 22nd**](https://camo.githubusercontent.com/f2fab381d1018fa00730b1e960a6140ac74228a0/68747470733a2f2f7062732e7477696d672e636f6d2f6d656469612f43644f5463515456414141615043502e6a7067); [Jonathan Zdziarski](http://www.zdziarski.com/blog/?page_id=202) (iOS digital forensics expert) [argues it was unlikely to be intentional since the *Find-My-iPhone* feature was still enabled](http://www.zdziarski.com/blog/?p=5655), among other factors. 

> Find my iPhone is still active on the phone (search by serial number), so why would a terrorist use a phone he knew was tracking him? Obviously he wouldn’t. The Find-my-iPhone feature is on the same settings screen as the iCloud backup feature, so if he had disabled backups, he would have definitely known the phone was being tracked. But the argument that Farook intentionally disabled iCloud backup does not hold water, since he would have turned off Find-my-iPhone as well.


#### After the Attack

> "Apple engineers saw iCloud backup auth was failing. This tells me FBI seized the phone powered up, and royally blew it turning it off." --*Jonathan Zdziarski* [@JZdziarski](https://twitter.com/JZdziarski/status/701171820884525056)

+ Zdziarski outlines amateur forensics practice mistakes that were made when, & after, the phone was confiscated; principle among them: [turning the iPhone off](https://twitter.com/JZdziarski/status/701172487061643265) if it was still on, which would lock it. He also raises the important question of why (or if) the victim's phones weren't searched, since they would have copies of the communications the FBI seeks ([his full take on the case here](http://www.zdziarski.com/blog/?p=5645)). He is among the iPhone security experts who submitted an [“amici curiae" brief](https://web.archive.org/web/20160303095429/https://cyberlaw.stanford.edu/files/blogs/CIS%20Technologists%20Apple%20Brief%20Final.pdf) through [**The Center for Internet and Society**](https://cyberlaw.stanford.edu/blog/2016/03/cis-files-amici-curiae-brief-apple-case-behalf-iphone-security-experts-and-applied) (see **Techdirt**'s [full list of *amici curiae* briefs submitted so far](https://www.techdirt.com/articles/20160303/23482933802/we-read-all-20-filings-support-apple-against-fbi-here-are-most-interesting-points.shtml), with analysis). The FBI contradicts the claim made by Apple engineers & Supervisory Special Agent Christopher Pluhar says "Farook's iPhone was found powered off" ([see pg 29 lines 7-17](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf) or [pg 2 lines 7-17](https://web.archive.org/web/20160311021811/https://assets.documentcloud.org/documents/2755240/031123088015.pdf)). Zdziarksi says "[the best way to determine if the device truly was off or not is to release the carrier’s tower records showing last activity](https://web.archive.org/web/20160311002204/https://twitter.com/JZdziarski/status/708078399844171776)."

![FBI says iPhone was off](https://pbs.twimg.com/media/CdOTcQTVAAAaPCP.jpg)
![FBI says iPhone was off 2](https://pbs.twimg.com/media/CdOKlI5WwAAjiG9.jpg)


+ A "senior Apple executive" (one of many who apparently spoke with journalists on a Friday call) claimed that the Apple ID password linked to the iPhone was changed [within 24 hours of the phone being confiscated](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.fflQoRn36). This executive only came forward, and thus far remained anonymous, because they "[had thought it was under a confidentiality agreement with the government. Apple seems to believe this agreement is now void since the government brought it up in a public court filing](https://web.archive.org/web/20160221094419/http://arstechnica.com/tech-policy/2016/02/apple-we-tried-to-help-fbi-terror-probe-but-someone-changed-icloud-password/)." The FBI's motion to compel Apple confirms the passcode was reset *while in government custody* and blames it on Farook's employer in the San Bernardino Department of Health ([see footnotes on pg 18](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

![footnote](https://pbs.twimg.com/media/CbmnuFqUsAAGLm2.png)

However [San Bernardino County argued](https://web.archive.org/web/20160220180834/https://twitter.com/countywire/status/700887823482630144) they had reset the password at the FBI's request.

> "The County was working cooperatively with the FBI when it reset the iCloud password at the FBI's request."

+ In an [inquiry to San Bernardino County CAO David Wert](https://web.archive.org/web/20160221170116/https://www.documentcloud.org/documents/2716811-Statement-from-the-FBI-Feb-20-2016.html), he shared a statement from [Laura Eimiller](linkedin.com/in/laura-eimiller-0595598) (FBI Press & Public Relations at U.S. Department of Justice) which confirms that the County did not "independently conduct analysis" but that "the FBI worked with [them] to reset the *iCloud password* on December 6th," which (as previously stated [in the footnotes on pg 18 here](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)) meant Apple was unable to assist with the auto-backup function on the iPhone. However, unless journalists seriously misquoted the Apple senior executives (who have yet to be personally named), this contradicts their statement that the change was made within 24 hours. This inquiry also shows that the FBI does not know "whether an additional iCloud backup to the phone after that date -- if one had been technically possible -- would have yielded any data." Their reason for pursuing Apple under the All Writs Act order is that they believe there might be "more data [on the iPhone] than an iCloud backup contains," which also contradicts [Apple's assertion that had they not reset the iCloud password/ Apple ID, this case would not be necessary](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6). The pieces of "device-level data" the FBI wants to access from the phone itself includes the keyboard cache ([see pg 29 line 22](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf)); the claim that there is more keyboard cache data in the device than on the iCloud backup is disputed by Zdziarski [here](https://web.archive.org/web/20160313082705/https://twitter.com/jzdziarski/status/708782855409815553). Likewise, [San Bernardino Police Chief Jarrod Burguan has said](https://theintercept.com/2016/02/26/farooks-iphone-is-probably-useless-even-the-police-say-so/) "there is a reasonably good chance that there is nothing of any value on the phone."

![Kenn White @kennwhite](https://pbs.twimg.com/media/Cbn5nsNUcAEoKcB.png)

+ Farook's employer consented to a law enforcement search of the device ([see lines 22-24 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

+ The government filed their [*ex parte*](http://legal-dictionary.thefreedictionary.com/ex+parte) application & released [their first Order to assist](https://web.archive.org/web/20160217152549/https://assets.documentcloud.org/documents/2714001/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf) on February 16th; Apple says they were not contacted about it directly beforehand but were instead given notice through the press in conjunction with the public ([see footnotes on pg 11](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)).

![Apples says government didn't give "chance to be heard](https://prod01-cdn07.cdn.firstlook.org/wp-uploads/sites/1/2016/02/5.png)

+ The [US House of Representatives Committee on the Judiciary](http://judiciary.house.gov/index.cfm/hearings?ID=89431275-E911-4D5C-BD70-BFE3EF91AD86) held a session to discuss this court case on March 1st, with [FBI Director James Comey](https://web.archive.org/web/20160315071544/https://www.fbi.gov/about-us/executives/comey), Apple Senior Vice President [Bruce Sewell](https://web.archive.org/web/20160310152653/http://www.apple.com/pr/bios/bruce-sewell.html), Professor [Susan Landau]( https://web.archive.org/web/20160322052351/http://www.privacyink.org/) (co-author of "[*Privacy On The Line: The Politics of Wiretapping and Encryption*](https://web.archive.org/web/20160306014712/https://mitpress.mit.edu/books/privacy-line)"), & New York County District Attorney [Cyrus R. Vance Jr.](https://web.archive.org/web/20160316182705/http://manhattanda.org/meet-cy-vance) as witnesses. "[The Encryption Tightrope: Balancing Americans' Security & Privacy](https://youtu.be/g1GgnbN9oNw)" is available on YouTube (I also have a local .mp4 copy in case it is taken down).

+ On March 3rd, San Bernardino County District Attorney [Michael Ramos](http://www.sbcountyda.org/AboutDARamos/AboutDistrictAttorneyMichaelRamos.aspx) filed an *amicus curiae* brief in support of the FBI, which is being mocked for speculating about a "lying-dormant cyber pathogen endangering San Bernardino County's infrastructure" on the iPhone ([see pg 3 or *6/40*](https://web.archive.org/web/20160305131629/https://assets.documentcloud.org/documents/2748053/Gov-Uscourts-Cacd-640468-79-0.pdf)). [Jeremiah Grossman](https://twitter.com/jeremiahg), founder of [White Hat Security](https://www.whitehatsec.com/), has created the webpage [www.cyberpathogen.com](http://www.cyberpathogen.com/) displaying the quote & linking to [Zdziarski's artcle on the document](http://www.zdziarski.com/blog/?p=5849).

![SB DA brief statement](https://pbs.twimg.com/media/CcrIGwVW4AAipPA.jpg)

+ On March 4th, **UN High Commissioner for Human Rights** [Zeid Ra’ad Al Hussein](http://www.ohchr.org/EN/AboutUs/Pages/HighCommissioner.aspx) [released a statement on the case leaning in Apple's favor](https://web.archive.org/web/20160306001954/http://www.ohchr.org/EN/NewsEvents/Pages/DisplayNews.aspx?NewsID=17138&LangID=E), expressing concern for the safety of citizens as well as "human rights defenders, civil society, journalists, whistle-blowers and political dissidents" in authoritarian countries who would likely demand more access upon seeing the FBI successfully compel Apple.

![UN statement](https://pbs.twimg.com/media/CcsdTM3W0AAkKvr.jpg)

#### The Trial

+ On March 21st, one day before the scheduled hearing, the Department of Justice announced in a filing that it wanted to postpone or possibly cancel the hearing, claiming that "an outside party demonstrated to the FBI a possible method for unlocking Farook's iPhone" ([see pg 3](https://web.archive.org/web/20160321231145/https://assets.documentcloud.org/documents/2773489/2016-03-21-Ex-Parte-Application-Dckt-191-0.pdf)). *It was not stated who that outside party is*, though **The Intercept** says [the Department of Justice told reporters they don't work for the government](https://theintercept.com/2016/03/21/government-showdown-with-apple-delayed/). The DOJ and FBI [jointly contracted a New Jersey vendor](https://web.archive.org/web/20160323152857/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+PIID%3A%22DJF161200P0004424%22&renderer=jsp&length=1) of the Israel-based company [**Cellebrite**](http://www.cellebrite.com/) (which manufactures data extraction & analysis devices for phones) [on the same day](https://web.archive.org/web/20160323152753/https://www.fpds.gov/ezsearch/fpdsportal?q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+PIID%3A%22DJF161200P0004424%22&s=FPDSNG.COM&templateName=1.4.4&indexName=awardfull&sortBy=SIGNED_DATE&desc=Y). **Reuters** says [the Tel Aviv national daily newspaper **Yedioth Ahronoth** (in Hebrew) reported two days later](https://web.archive.org/web/20160323162001/http://www.yediot.co.il/articles/0,7340,L-4781928,00.html) that [the contract was indeed part of the San Bernardino investigation](https://web.archive.org/web/20160323154820/http://www.reuters.com/article/us-apple-encryption-cellebrite-idUSKCN0WP17J). Neither the US government nor **Cellebrite** have commented on the nature of the partnership. Emily Chang, host of [**Bloomberg West**](https://en.wikipedia.org/wiki/Bloomberg_West), soon [claimed that the request was accepted by the judge](https://web.archive.org/web/20160321235306/https://twitter.com/emilychangtv/status/712060838539108352), which was confirmed by [a record of a telephonic conference](https://cryptome.org/2016/03/usg-apple-199.pdf) & subsequent filing in reply ([see the last page](https://cryptome.org/2016/03/usg-apple-191.pdf)). The government is required to file a status report on April 5th 2016 after two weeks of testing this new method, at which time either a new date will be set or the trial will be cancelled altogether. The method being tested is believed to be [some variation of the NAND copying / mirroring technique](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----could-a-secure-password-protect-against-fbios---).

![contracting Cellebrite](https://pbs.twimg.com/media/CePaYXPVIAECN9N.jpg:large)
![postpone hearing](https://pbs.twimg.com/media/CeG3bAWUUAAAOe_.jpg:large)

## Is the FBI demanding Apple “break encryption”?
#### 1) What 'encryption' are we dealing with here?

The FBI is demanding Apple build a custom mobile iOS with two standard passcode security features disabled: the 10-try limit & escalating time delays ([see pg 2](https://web.archive.org/web/20160217152549/https://assets.documentcloud.org/documents/2714001/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)).

> *Note: Court filings & articles refer to the custom mobile iOS by different names, most commonly 'GovtOS' & 'FBiOS'. For the purposes of consistency to avoid confusion, this overview will use 'FBiOS.'*

![compliance terms](https://pbs.twimg.com/media/CbYZuw7XEAAaziz.png)

The 10-try limit wipes an iPhone's data after 10 attempts. The time-delays feature will wait 1 minute after four incorrect passcode entries before it accepts another attempt, subsequently increasing to 5 minutes, 15 minutes, and finally 1 hour. Bypassing these features will allow the FBI to perform a [brute-force attack](https://www.techopedia.com/definition/18091/brute-force-attack), where they can guess the passcode as many times & as fast as the iPhone firmware will allow, without destroying the data. Along with disabling these security features, the FBI also wants the custom iOS allow them to enter the 10,000 possible passcode combinations electronically instead of by hand (which would be incredibly slow comparatively). This would likely be done through [Device Firmware Upgrade (DFU) mode](https://web.archive.org/web/20160312000032/http://arstechnica.com/apple/2016/03/there-are-ways-the-fbi-can-crack-the-iphone-pin-without-apple-doing-it-for-them/), normally used for [restoration by installing a fresh iOS version when an iPhone fails to boot](https://www.theiphonewiki.com/wiki/DFU_Mode).

However, the FBI could technically build this custom iOS on their own (though it will take more time). The one thing they actually need is for Apple to sign FBiOS using their developer software key, because only software signed with this key will be accepted by SecureRom's signature checker (though jailbreakers have found bugs in the past which let them bypass this).

So the 'encryption' we are dealing with here is a matter of *authentication*.

#### 2) Why does this distinction matter?

**Authentication** falls under one of the [three principles of information security (CIA)](http://resources.infosecinstitute.com/guiding-principles-in-information-security/): accessibility. 
Authentication deals with how you prove you hold authorization to carry out specific operations, like accessing an account. 
This is something you know (eg. a password), something you have (eg. a card), or something you are (eg. biometrics).

Authentication is also an element of cryptography, but distinct from privacy/ confidentiality 
(see the [*Purpose* section of Gary C. Kessler's "**An Overview of Cryptography**"](http://www.garykessler.net/library/crypto.html#purpose)).

The San Bernardino phone is said to be locked with a 4-digit [PIN](https://en.wikipedia.org/wiki/Personal_identification_number). PINs, unlike passwords (which can be [alphanumeric](https://en.wikipedia.org/wiki/Alphanumeric) & longer), are numeric and usually very short (4-6 numbers allowed on average). Even if you had a PIN and a password of the same length, it would probably take more time to break the password with brute-force.

Therefore, if the FBI uses this FBiOS, authenticated by Apple's software key/ digital signature, it will be able to run on Farook's phone and the PIN will be broken within 24 hours.

The definition of a [**backdoor**](http://www.linfo.org/backdoor.html) is *something which bypasses normal authentication*. Or, more (perhaps too) broadly:

> **backdoor:** A design fault, planned or accidental, that allows the apparent strength of the design to be easily avoided by those who know the trick -- *Newton's Telecom Dictionary: 28th Updated & Expanded Edition*

What should be highlighted here is that Apple claims not to be able to, or at least not want to, access their customer's data. Apple customers have an expectation of **confidentiality** (the first information security principle) even from Apple itself. Apple claims it does not position itself as a party with access to encrypted communications on customer phones. If this is true, why is there a threat to encryption?

If the FBI was compelling someone who *was* a party or key-holder to encrypted communications, *then* it would be more accurate to say that they are “breaking encryption” by taking advantage of a social engineering weakness which, at the present time, exists with the majority of encryption use.

The problem here is that the 'encryption' *is already broken*. Quoting from what a "senior Apple executive" said to **Buzzfeed**, Apple's fear that they are being asked to "[create a sort of master key](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6)" is misleading at best, because Apple is not being asked to *create* a key but rather *use the master key they already possess* in conjunction with a custom iOS that lacks two security features. 

> [Thus, in the sense that the word is being used in the media, the ‘backdoor’ already exists. The ‘key to all locks’ is Apple’s private signing key](https://medium.com/@liamkirsh/your-iphone-already-has-a-backdoor-33f43cceefdb#.p32cuvp5t). --*Liam Kirsh* [@choicefresh](https://twitter.com/choicefresh)

**Firefox** founder [Blake Ross](https://twitter.com/blakeross) offered a very well-written & humorous take on [how security holes fail us, in both our digital & non-digital lives](https://medium.com/@blakeross/mr-fart-s-favorite-colors-3177a406c775#.wg0g6fcpu), and says this debate is about whether "a private company [should] be allowed to sell unbreakable security."

> To be clear: Contrary to a lot of shoddy reporting, and some rather “generous” language from Apple, this is not the world we’re living in yet. The fact that Apple can break into your phone demonstrates that we’re still firmly in “Coke recipe” territory.

[Leif Ryge](https://twitter.com/wiretapped) from **Ars Technica** explains why [being a single point of failure is the bigger issue *industry-wide*](https://web.archive.org/web/20160227165908/http://arstechnica.com/security/2016/02/most-software-already-has-a-golden-key-backdoor-its-called-auto-update/):

> How did we get here? How did so many well-meaning people build so many fragile systems with so many obvious single points of failure?

> I believe it was a combination of naivety and hubris. They probably thought they would be able keep the keys safe against realistic attacks, and they didn't consider the possibility that their governments would actually compel them to use their keys to sign malicious updates.

> Fortunately, there is some good news. The FBI is presently demonstrating that this was never a good assumption, which finally means that the people who have been saying for a long time that we need to remove these single points of failure can't be dismissed as unreasonably paranoid anymore.

> ... So when Apple says the FBI is trying to "force us to build a backdoor into our products," what they are really saying is that the FBI is trying to force them to use a backdoor which already exists in their products. (The fact that the FBI is also asking them to write new software is not as relevant, because they could pay somebody else to do that. The thing that Apple can provide which nobody else can is the signature.)

> Is it reasonable to describe these single points of failure as backdoors? I think many people might argue that industry-standard systems for ensuring software update authenticity do not qualify as backdoors, perhaps because their existence is not secret or hidden in any way. But in the present Apple case where they are themselves using the word "backdoor," abusing their cryptographic single point of failure is precisely what the FBI is demanding.

Apple is being pursued because contrary to their commendable implimentation of 'strong encryption,' they retain the ability to backdoor their products, not only through allowing the use of PINs but because they are a centralized point of failure in regards to building proprietary firmware & software.

> "If Apple gets to call #FBiOS a 'backdoor,' I suggest we refer to 'Apple updates' as 'official backdoor only good guys are allowed to use.'" --*Pwn All The Things* [@pwnallthethings](https://twitter.com/pwnallthethings/status/702974661211119617)

`Note: iPhones can be set to manual (requires user authentication, ie. passcode) or auto-update. During the update process, iPhone updates are individually signed per-device on Apple's servers, which would prevent an attacker from downgrading to an insecure version.`

Consider [this point](https://theintercept.com/2016/02/26/fbi-vs-apple-post-crypto-wars/) made by [Dan Froomkin](https://theintercept.com/staff/dan-froomkin/) & [Jenna McLaughlin](https://theintercept.com/staff/jennamclaughlin/)  of **The Intercept**:

> You might say we’re entering the Post-Crypto phase of the Crypto Wars.

> Think about it: The more we learn about the FBI’s demand that Apple help it hack into a password-protected iPhone, the more it looks like part of a concerted, long-term effort by the government to find new ways *around* unbreakable encryption — rather than try to break it. [*emphasis added*]

The [**Electronic Frontier Foundation**](https://www.eff.org/about) has published a few pieces on this case and offers only passing criticism of Apple on this point, even though they include passages like this:

> **Would it be easy for Apple to sign the requested cracking software?** The answer any trained security engineer will give you is "it shouldn't be."

> ... There are pros and cons to this approach, but Apple considers this signing key among the crown jewels of the entire company. There is no good revocation strategy if this key is leaked, since its corresponding verification key is hard-coded into hundreds of millions of devices around the world.

It shouldn't be easy, but it's still possible. Disabling security features in so many devices also shouldn't be easy, but it's possible and, considering Apple's response, a very real problem.

Ray Dillinger frames the FBI's court order in a rather interesting way: [as a dramatic & unfriendly bug report](https://web.archive.org/web/20160224005522/http://www.metzdowd.com/pipermail/cryptography/2016-February/028269.html).

![FBI court order as a bug report](https://pbs.twimg.com/media/Cb6-D-eXIAAA1MW.png)

Taking all of this into consideration:
+ **Is Apple being asked to "create" a "backdoor"?** Unless you consider Apple creating a custom iOS, signed with their special software key, to be outside the bounds of 'normal' in terms of software authentication powers they *already* possessed, the answer is no. Remember that Apple *could use this capability at any time*, regardless of whether it's compelled or not. If you interpret 'normal' authentication to *not* include Apple's abilities and consider that 1) Apple disabling security features in their OS is an out-of-the-ordinary procedure for them & 2) though now weakly grounded, most Apple customers did have an expectation of confidentiality... then it could be argued that this is "creating a backdoor"; yes, I think that *whether or not this is a backdoor, a further distinction should be made on whether they are merely 'using' one or 'creating' one -- as such a fact is very important to Apple feeling enough pressure to increase iPhone security*. You can read Jonathan Zdziarski's "[*Three-Prong Backdoor Test*](http://www.zdziarski.com/blog/?p=5785)" (see definition below), [EFF's thought-piece on the historical definition of backdoors](https://www.eff.org/deeplinks/2016/03/thinking-about-term-backdoor) or [another argument on this from the technical perspective by Brandon Edwards](https://medium.com/@drraid/it-s-a-backdoor-100-2460bf7f8010#.l5nwz4405) (note that I have not made my argument depend on it being limited to one device, which this article focuses on & disputes).

> A **backdoor** is a component of a security mechanism, in which the component is active on a computer system without consent of the computer’s owner, performs functions that subvert purposes disclosed to the computer’s owner, and is under the control of an undisclosed actor.

+ **Is Apple being told to "break encryption"?** Again, this still depends on your interpretation of the previous question. The encryption system of the iOS 9 itself is not being broken; security features dealing with how authentication is proven are. [Brute-force attacks](https://www.techopedia.com/definition/18091/brute-force-attack) are a hack of security vulnerabilities, not an encryption backdoor.

Therefore, it would be rather more accurate to say the FBI is demanding that Apple *take advantage of system security vulnerabilities which already exist.* 

## What are the technical & legal concerns involved?
#### Technical Concerns

It is now known that Apple has the ability to backdoor their own products & could be compelled to use that backdoor.

##### --- What are the limits to the use of FBiOS? --

Initially some security experts argued that this backdoor wouldn't work on iPhones newer than 5C 
due to the **Secure Enclave** firmware, [a co-processor of many independently-functioning kernels within the A7 64-bit system chip which stores keys in supposedly tamper-resistant hardware & also uses secure boot to ensure that all software installed on the OS is signed by Apple](https://web.archive.org/web/20150124040556/http://www.macrumors.com/2014/02/26/touch-id-secure-enclave-document) 
(remember authentication from earlier). On February 19th, a “senior Apple executive” told journalists at **Motherboard**, [**The Guardian**](https://twitter.com/dannyyadron/status/700830922585743360) and others that this is not true – the FBiOS "[would be effective on every type of iPhone currently being sold](https://web.archive.org/web/20160221092412/http://motherboard.vice.com/read/apple-the-exploit-the-fbi-is-asking-for-would-work-on-all-iphones)."

![Motherboard, Secure Enclave](https://pbs.twimg.com/media/CbnuF7iVIAE0A76.jpg)

Apple has now included this warning in an [FAQ for customers](https://web.archive.org/web/20160222150037/https://www.apple.com/customer-letter/answers/):

> Law enforcement agents around the country have already said they have hundreds of iPhones they want Apple to unlock if the FBI wins this case. In the physical world, it would be the equivalent of a master key, capable of opening hundreds of millions of locks. Of course, Apple would do our best to protect that key, but in a world where all of our data is under constant threat, it would be relentlessly attacked by hackers and cybercriminals. As recent attacks on the IRS systems and countless other data breaches have shown, no one is immune to cyberattacks.

"Hundreds of millions of locks." This would apply to most, if not all of their customer base.

This detail is very important, if true, because many tech journalists (including from **Ars Technica**) also speculated 
that [FBiOS wouldn't even work on other 5C iPhones](https://web.archive.org/web/20160219203100/http://arstechnica.com/apple/2016/02/encryption-isnt-at-stake-the-fbi-knows-apple-already-has-the-desired-key/) because, since the FBI is allowing that the custom software 
be tied specifically to the phone's unique identifier, it should be limited to this *one* device. 

![FBiOS working on older phones](https://pbs.twimg.com/media/Cbl8EghUkAA5vMr.jpg)

A description of the Unique Identifier (UID) can be found on page 59 of [Apple's iOS Security Whitepaper](https://www.apple.com/business/docs/iOS_Security_Guide.pdf):

> A 256-bit AES key that’s burned into each processor at manufacture. It cannot be read by firmware or software, and is used only by the processor’s hardware AES engine. To obtain the actual key, an attacker would have to mount a highly sophisticated and expensive physical attack against the processor’s silicon. The UID is not related to any other identifier on the device 
including, but not limited to, the UDID.

Because the UID is "baked into its hardware," **Ars Technica** editor [Peter Bright](https://web.archive.org/web/20160216072035/http://arstechnica.com/author/peter-bright/) says that this request makes the assumption that the UID can be extracted -- which appears to be a difficult process.

Difficulty of extraction aside, he does offer that it *might* be possible to swap identifiers to apply to other 5C phones. 

![FBiOS tied to unique identifier](https://pbs.twimg.com/media/Cbl9ajvUcAAgJPV.jpg:large)

Therefore, Apple may not only be admitting that Secure Enclave is not secure enough but that it is possible to swap identifiers in this custom OS. This probably has something to do with the fact that Apple could force an update to Secure Enclave without wiping the data.

**EFF**'s [Joseph Bonneu](https://www.eff.org/about/staff/joseph-bonneau) says the following in relation to [whether Secure Enclave protects newer phones](https://www.eff.org/deeplinks/2016/02/technical-perspective-apple-iphone-case):

> (Older devices that lack the secure enclave also apply a similar delay, but apparently do so from within the operating system.) It's possible, though not completely clear from Apple's documentation, that a software update would be able to modify this behavior; if not, this would completely prevent Apple from enabling faster passcode guessing on newer devices.

> There has been further speculation that the secure enclave could refuse to accept any software update (even one signed by Apple) unless unlocked by entering the passcode, or alternately, that a software update on a locked phone would erase all of the cryptographic keys, effectively making the phone's storage unreadable. Apple's security documentation makes no such guarantees, though, and there are indications that this isn't the case. So special cracking tools from Apple could potentially still modify the secure enclave's behavior to remove both the 10-guess limit and the delays between guesses.

This means that, if leaked, *FBiOS could be used on any iPhone*.

##### --- Could a secure password protect against FBiOS? --

What has also not yet been confirmed by Apple is whether a strong password (not a PIN) remains a safeguard against this attack. Since it is only a brute-force attack, a long & complex password should work under normal circumstances 
(taking months to many years to break). [Micah Lee](https://theintercept.com/staff/micah-lee/), a technologist at the **The Intercept**, [says it would](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/):

> It’s true that ordering Apple to develop the backdoor will fundamentally undermine iPhone security, as Cook and other digital security advocates have argued. But it’s possible for individual iPhone users to protect themselves from government snooping by setting strong passcodes on their phones — passcodes the FBI would not be able to unlock even if it gets its iPhone backdoor.

> ...The short version: If you’re worried about governments trying to access your phone, set your iPhone up with a random, 11-digit numeric passcode.


Note that he advises even an 11-digit *numeric* (numbers only) passcode would be sufficient, though alphanumeric (numbers, characters, and symbols) is stronger because it increases the amount of possible combinations. With a "truly random" 11-digit passcode, it would take *an average of 127 years* to crack on the iPhone with FBiOS (note: the following graphs are *maximum* time estimates, not averages).

![passcode breaking time numeric](https://d262ilb51hltx0.cloudfront.net/max/800/1*QSjgF6fnfID7N-W9Ug4fcg.png)

![passcode breaking time alphanumeric](https://d262ilb51hltx0.cloudfront.net/max/800/1*eENjTSHmHIExFrf9k1E-tw.png)

Drawing from [page 12 of Apple's iOS Security White Paper (iOS 9.0 or later)](https://www.apple.com/business/docs/iOS_Security_Guide.pdf), this is due to limitations on how the brute-force attack can be performed:

> The passcode is entangled with the device’s UID, so brute-force attempts must be performed on the device under attack. A large iteration count is used to make each attempt slower. The iteration count is calibrated so that one attempt takes approximately 80 milliseconds. This means it would take more than 5½ years to try all combinations of a six-character alphanumeric passcode with lowercase letters and numbers.


However, these figures only apply if Secure Enclave or another aspect of the iPhone's security architecture isn't also being breached as well, such as the "Effaceable Storage" processor (contains the CPU, BootROM, RAM, crypto engines, Apple's public signing key, and the UID key). [Daniel Kahn Gillmor](https://www.aclu.org/bio/daniel-kahn-gillmor), technologist for the ACLU, [explains how you could bypass the auto-erase security feature on an iPhone 5C](https://web.archive.org/web/20160311005401/https://www.aclu.org/blog/free-future/one-fbis-major-claims-iphone-case-fraudulent), without destroying the data, by copying the flash memory of the file system key stored in this processor:

> The FBI can simply remove this chip from the circuit board (“desolder” it), connect it to a device capable of reading and writing NAND flash, and copy all of its data. It can then replace the chip, and start testing passcodes. If it turns out that the auto-erase feature is on, and the Effaceable Storage gets erased, they can remove the chip, copy the original information back in, and replace it. If they plan to do this many times, they can attach a “test socket” to the circuit board that makes it easy and fast to do this kind of chip swapping.

> If the FBI doesn't have the equipment or expertise to do this, they can hire any one of dozens of data recovery firms that specialize in information extraction from digital devices.

> NAND flash storage is an extremely common component. It's found in USB thumb drives, mobile phones, portable music players, low-end laptops—pretty much every portable device. Desoldering a chip from the circuitboard is straightforward enough that there are many clips on YouTube showing the practice, and reading and writing a bare NAND chip requires a minor investment in hardware and training that the FBI has probably already made.

Zdziarski, after consulting with other tech experts, believes [the FBI is most likely using this method](http://www.zdziarski.com/blog/?p=5966).

> Using a NAND copying / mirroring technique, this barrier could be overcome in iOS 9, allowing the device to write and verify the attempt, but have that change later blown away by restoring an original copy of the chip. They wouldn’t have to copy the whole NAND in this case. If they can isolate the part of the chip that is written to (even though it’s encrypted), they can just keep writing over that portion of the chip. If the methods from iOS 8 were borrowed for this, then it could be partially automated by entering the pin through the USB, as well as using a light sensor to determine which pin successfully unlocked the device

He also says that "[with the info that experts have come forward with, I am reasonably confident FBI themselves, with current talent, could get into this phone](https://web.archive.org/web/20160311015818/https://twitter.com/JZdziarski/status/708100880353071105)."

With this in mind, a very valuable & proactive thing Apple could do is **recommend that their customers upgrade their passwords.** Until now Apple has given their customers a false sense of security, allowing them to use short passcodes & PINs. The last line of protection should be a strong password, which is under the user's control to change, not a security feature which can apparently be disabled.

#### Legal Concerns

##### --- What is the history behind Apple's compliance with law enforcement? --

To understand the legal history behind this case in terms of the US government ordering Apple to "unlock" iPhones, I recommend this clarifying article by **TechCrunch**'s [Matthew Panzarino](https://twitter.com/panzer): "[No, Apple Has Not Unlocked 70 iPhones For Law Enforcement](https://web.archive.org/web/20160220161959/http://techcrunch.com/2016/02/18/no-apple-has-not-unlocked-70-iphones-for-law-enforcement/)." The most important lines are about the difference between *decryption* and *extraction*:

> There are two cases involving data requests by the government which are happening at the moment. There is a case in New York [which] ...involves an iPhone running iOS 7. On devices running iOS 7 and previous, Apple actually has the capability to extract data, including (at various stages in its encryption march) contacts, photos, calls and iMessages without unlocking the phones. That last bit is key, because in the previous cases where Apple has complied with legitimate government requests for information, this is the method it has used.

> It has not unlocked these iPhones — it has extracted data that was accessible while they were still locked.

> The California case, in contrast, involves a device running iOS 9. The data that was previously accessible while a phone was locked ceased to be so as of the release of iOS 8, when Apple started securing it with encryption tied to the passcode, rather than the hardware ID of the device... So Apple is unable to extract any data including iMessages from the device because all of that data is encrypted.

In short: extraction allows them to access *unencrypted* data on iOS 7 or older; because they have [implimented passcode-based encryption in iPhones running iOS 8 or iOS 9](https://web.archive.org/web/20160222150037/https://www.apple.com/customer-letter/answers/), this data is no longer accessible through extraction. Therefore this request is different compared to Apple's history of compliance, which the court orders have yet to acknowledge.


##### --- What are important factors in legal precedent(s) for the future? ---

Regardless of whether this specific piece of custom software will be useable on other devices, Apple claims that they are already getting similar requests to do so now that it has been shown they have the capability. This would put them in a position where they either save FBiOS in the event of future cases, or safely destroy it & then be forced to spend more time/ resources recreating it in the future ([see pg 3](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)).

> The government says:  “Just this once” and “Just this phone.”  But the government knows those statements are not true; indeed the government has filed multiple other applications for similar orders, some of which are pending in other courts. And as news of this Court’s order broke last week, state and local officials publicly declared their intent to use the proposed operating system to open hundreds of other seized devices—in cases having nothing to do with terrorism.

> If this order is permitted to stand, it will only be a matter of days before some other prosecutor, in some other important case, before some other judge, seeks a similar order using this case as precedent.  Once the floodgates open, they cannot be closed, and the device security that Apple has worked so tirelessly to achieve will be unwound without so much as a congressional vote.


I'm seeing over and over again the comment that the legal precedent(s) this case could set carries more risk than the technical risk posed by FBiOS. FBI Director James Comey has already [admitted that legal prescedent will be established with this case](http://www.c-span.org/video/?c4586153/comey-admits-iphone-backdoor-legal-precedent) and therefore it should not be cast aside as hypothetical hysteria. Since I am not a lawyer, I am not familiar with the specific statutes being considered,but here are some of the main points summarized:

+ This court order would force Apple to code a custom iOS which deliberately takes advantage of security vulnerabilities in their authentication systems. If “code is speech," then speech (here in the form of code) can be compelled. While this would be a different form of compelled speech, [compelled speech is not at all new](http://itlaw.wikia.com/wiki/Compelled_speech). It is still an open question of who exactly at Apple can be compelled to do this, and [whether anyone will comply at all](https://web.archive.org/web/20160318151138/http://www.nytimes.com/2016/03/18/technology/apple-encryption-engineers-if-ordered-to-unlock-iphone-might-resist.html)...

> Apple employees are already discussing what they will do if ordered to help law enforcement authorities. Some say they may balk at the work, while others may even quit their high-paying jobs rather than undermine the security of the software they have already created, according to more than a half-dozen current and former Apple employees. Among those interviewed were Apple engineers who are involved in the development of mobile products and security, as well as former security engineers and executives.

> ... The fear of losing a paycheck may not have much of an impact on security engineers whose skills are in high demand. Indeed, hiring them could be a badge of honor among other tech companies that share Apple’s skepticism of the government’s intentions. “If someone attempts to force them to work on something that’s outside their personal values, they can expect to find a position that’s a better fit somewhere else,” said Window Snyder, the chief security officer at the start-up Fastly and a former senior product manager in Apple’s security and privacy division.

> Apple said in court filings last month that it would take from six to 10 engineers up to a month to meet the government’s demands. However, because Apple is so compartmentalized, the challenge of building what the company described as “GovtOS” would be substantially complicated if key employees refused to do the work.

...and whether prior precedent of "code is speech" applies, since the case of [*Bernstein vs. US Department of Justice*](https://www.eff.org/cases/bernstein-v-us-dept-justice) was about the *publication* of code (read [Park Higgins' EFF piece on "code is speech" related to 3-D printing](https://www.eff.org/deeplinks/2015/12/3-d-printing-case-code-speech-faces-new-challenges)). Before Apple had put forth a reply outlining how their defense would argue, at least one of [Apple's objections to the court order was projected to be on First Amendment grounds](https://web.archive.org/web/20160224033346/http://www.latimes.com/local/lanow/la-me-ln-apple-legal-argument-free-speech-20160223-story.html):

> In Apple's fight to knock down a court order requiring it to help FBI agents unlock a killer’s iPhone, the tech giant plans to argue that the judge in the case has overreached in her use of an obscure law and infringed on the company’s 1st Amendment rights, an Apple attorney said Tuesday.

> Theodore J. Boutrous -- one in a pair of marquee lawyers the technology company's has hired to wage its high-stakes legal battle -- outlined the arguments Apple plans when it responds to the court order this week.

> [...] “The government here is trying to use this statute from 1789 in a way that it has never been used before. They are seeking a court order to compel Apple to write new software, to compel speech," Boutrous said in a brief interview with The Times.

> Boutrous said courts have recognized that the writing of computer code is a form of expressive activity -- speech that is protected by the 1st Amendment.

This was confirmed in Apple's first motion against the FBI's court order on February 25th, in addition to objections on Fifth Amendment due process grounds ([see pgs 32 & 34 respectively](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)):

![Apple arguing on First Amendment grounds](https://pbs.twimg.com/media/CcFn9TwXIAQRy11.png:large)

However, Neil Richards, one of the law professors supporting Apple, says [furthering the precedent of "code is speech" may carry unwanted consequences](https://www.technologyreview.com/s/600916/apples-code-speech-mistake/):

> Where does this leave us, then, when we’re considering the regulation of code by the government? The right question to ask is whether the government’s regulation of a particular kind of code (just like regulations of spending, or speaking, or writing) threatens the values of free expression. Some regulations of code will undoubtedly implicate the First Amendment. Regulations of the expressive outputs of code, like the content of websites or video games, have already been recognized by the Supreme Court as justifying full First Amendment treatment. It’s also important to recognize that as we do more and more things with code, there will be more ways that the government can threaten dissent, art, self-government, and the pursuit of knowledge.

> But on the other hand, and critically, there are many things that humans will do with code that will have nothing to do with the First Amendment (e.g., launching denial of service attacks and writing computer viruses). Code = Speech is a fallacy because it would needlessly treat writing the code for a malicious virus as equivalent to writing an editorial in the New York Times. Similarly, if companies use algorithms to discriminate on the basis of race or sex, wrapping those algorithms with the same constitutional protection we give to political novels would needlessly complicate civil rights law in the digital age.

The Department of Justice has objected to Apple's First Amendment argument for the following reasons ([see pgs 32-34](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf)):

> "...it does not involve a person being compelled to speak publicly, but a for-profit corporation being asked to modify commercial software that will be seen only by Apple." [pg 32 lines 13-15]

> "[T]hat [programming] occurs at some level through expression does not elevate all such conduct to the highest levels of First Amendment protection." [pg 32 lines 19-20]

> "To the extent Apple’s software includes expressive elements — such as variable names and comments — the Order permits Apple to express whatever it wants, so long as the software functions.. the Order’s 'broad requirements' do 'not dictate any specific message.'" [pgs 32-33 lines 24-1]

> "And even assuming, *arguendo*, that the Order compels speech-like programming, there is no audience: Apple’s code will be developed in the utmost secrecy and will never be seen outside the corporation." [pg 33 lines 3-5]

> "Apple will respond that if it modifies Farook’s iPhone to allow the government access to the phone, it “could be viewed as sending the message that [it] see[s] nothing wrong with [such access], when [it] do[es]... It is extremely unlikely that anyone could understand Apple to be expressing a message of hostility to 'data security and the privacy of citizens'..." [pg 34 lines 1-11]
 
Addressing the argument that Apple's "speech" would not be protected due to lack of audience, Apple argues that the presence of an audience has never been a requirement for protected speech ([see footnotes on pg 23](https://web.archive.org/web/20160315222842/https://assets.documentcloud.org/documents/2762120/Reply-Brief-in-Support-of-Apple-s-Motion-to-Vacate.pdf)):

![audience not necessary](https://pbs.twimg.com/media/CdoliafXEAAswZO.jpg:large)

+ US Congressman Ted Lieu (D-Los Angeles County), one of the Congressmembers who recently put forth [a bill for the ENCRYPT ACT](https://web.archive.org/web/20160222041054/https://lieu.house.gov/media-center/press-releases/congressmembers-lieu-farenthold-delbene-and-bishop-introduce-encrypt-act) ([full text here](https://web.archive.org/web/20160222040842/https://lieu.house.gov/sites/lieu.house.gov/files/documents/LIEU_027_xml%20%28ENCRYPT%20Act%20of%202016%29.pdf)), issued [this statement regarding the Apple court order](https://web.archive.org/web/20160219182200/https://lieu.house.gov/media-center/press-releases/congressman-lieu-statement-apple-court-order) on February 17th:

> "This court order also begs the question: Where does this kind of coercion stop?  Can the government force Facebook to create software that provides analytic data on who is likely to be a criminal?  Can the government force Google to provide the names of all people who searched for the term ISIL?  Can the government force Amazon to write software that identifies who might be suspicious based on the books they ordered?"

+ If a telecommunications provider *can* be compelled to take advantage of a security flaw 
undermining encryption for its customers, then they *will* be compelled. This will put pressure on other businesses 
to either comply or build their products so that they are not a centralized authority of proprietary software. Security technologist [Bruce Schneier](https://www.schneier.com/blog/about/) says the precent may motivate the government to [limit what sorts of security features tech companies can offer customers](https://www.washingtonpost.com/posteverything/wp/2016/02/18/why-you-should-side-with-apple-not-the-fbi-in-the-san-bernardino-iphone-case/) in order to maintain the ability to compel them. Though Apple has not released public plans to do so, [the "senior executives" have indicated they want to increase encryption implimentation in their products](https://web.archive.org/web/20160221193833/http://www.nytimes.com/2016/02/22/technology/apple-still-holds-the-keys-to-its-cloud-service-but-reluctantly.html):

![Apple might pursue iCloud encryption](https://pbs.twimg.com/media/CbyM7l1WAAAr5bb.png)

+ Other countries pay attention to the US on surveillance policy. Though Apple has not said they hold this fear, 
lawyers and security experts say this presents a threat to foreign customers & tech businesses as well.
If the U.S. government can compel Apple to take advantage of a security vulnerability, why not others?
A recent example they cite is where FBI Director James Comey called for encryption backdoors 
& the Chinese government introduced new counter-terrorism laws a few weeks later.

From [*Reuters*](http://www.reuters.com/article/us-usa-obama-china-idUSKBN0LY2H520150302) ("Obama Sharply Criticizes China's Plans for New Technology Rules"):

> In an interview with Reuters, Obama said he was concerned about Beijing's plans for a far-reaching counterterrorism law 
> that would require technology firms to hand over encryption keys, the passcodes that help protect data, 
> and install security 'backdoors' in their systems to give Chinese authorities surveillance access.


Sounds oddly familiar, doesn't it?

> To be sure, Western governments, including in the United States and Britain, have for years requested tech firms to disclose encryption methods, with varying degrees of success.

> Officials including FBI director James Comey and National Security Agency (NSA) director Mike Rogers publicly warned Internet companies including Apple and Google late last year against using encryption that law enforcement cannot break.

> Beijing has argued the need to quickly ratchet up its cybersecurity measures in the wake of former NSA contractor Edward Snowden's revelations of sophisticated U.S. spying techniques.

+ The use of the **All Writs Act** is not uncommon in surveillance cases -- listen to Jonathan Mayer's "[*Assistance for Current Surveillance: The All Writs Act*"](https://youtu.be/PoNJvmB16bQ); however its legitimacy in retrospective surveillance is being challenged. In response to President Obama's request for "moderation" in this debate, [Susan Crawford](https://twitter.com/scrawford), professor of law & public policy, explains how [**CALEA** (Communications Assistance for Law Enforcement Act)](https://t.co/j5bKCtuxhZ) will [limit the FBI's legitimacy in compelling Apple](https://backchannel.com/the-law-is-clear-the-fbi-cannot-make-apple-rewrite-its-os-9ae60c3bbc7b#.4g9f1z23l):

> The problem for the president is that when it comes to the specific battle going on right now between Apple and the FBI, the law is clear: twenty years ago, Congress passed a statute, the Communications Assistance for Law Enforcement Act (CALEA) that does not allow the government to tell manufacturers how to design or configure a phone or software used by that phone — including security software used by that phone.

> CALEA was the subject of intense negotiation — a deal, in other words. The government won an extensive, specific list of wiretapping assistance requirements in connection with digital communications. But in exchange, in Section 1002 of that act, the Feds gave up authority to “require any specific design of equipment, facilities, services, features or system configurations” from any phone manufacturer. The government can’t require companies that build phones to come to it for clearance in advance of launching a new device. Nor can the authorities ask a manufacturer to design something new — like a back door — once that device is out.

Judge James Orenstein, in another Apple iPhone-unlocking case from the Eastern District of New York, also disputed the use of AWA as to whether Apple could be considered 'close' to the crime ([see pgs 1, 29 31-32, & 40 respectively](https://web.archive.org/web/20160229224454/https://epic.org/amicus/crypto/apple/Orenstein-Order-Apple-iPhone-02292016.pdf)):

> "For the reasons set forth below, I conclude thatunder the circumstances of this case,the government has failed to establish either that the AWApermits the relief it seeks or that, even if such an order is authorized, the discretionary factors I must consider weigh in favor ofgranting the motion."

![All Writs Act constitutionality](https://pbs.twimg.com/media/CcausxZVAAIwS60.jpg:large)

![All Writs Act closeness to crime factor](https://pbs.twimg.com/media/CcawNGxUYAA-Ift.jpg:large)

![All Writs Act Apple public relations](https://pbs.twimg.com/media/Cca0YfiUkAA85oD.jpg:large)

+ It is highly unlikely that the FBI does not have alternative means to access the phone or its data in conjunction with the National Security Agency (NSA), as they have a history of mutual cooperation. Legally, alternative means would impact the legitimacy of using the All Writs Act, as **EFF** explains: "[This point is potentially relevant legally, as cases interpreting the All Writs Act require '*an absence of alternative remedies*.' However, we lack firm evidence that the FBI has such a capability. Apple also probably doesn't want to argue that its phone is insecure so the authorities should just break into it some other way](https://www.eff.org/deeplinks/2016/02/technical-perspective-apple-iphone-case)." Now that they have requested to [postpone the trial](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#the-trial) despite their prior repeated assertions that unlocking the iPhone was only possible with Apple's assistance, many are wondering whether the FBI had prior knowledge of this capability and may only be changing course for strategic legal reasons, such as promoting the 'national security vs. encryption' false dichotomy so that public pressure will make it easier to compel companies under similar circumstances in the future. 

***
##### Mirror Links:

+ [iOS Security Whitepaper (Sept 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/iOS_Security_Guide.pdf)
+ [Transcript of Argument from another Apple iPhone case in New York (Nov 27th 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/Transcript.Order-Requiring-Apple-Inc-to-Asisst-in-the.pdf)
+ [Bill of ENCRYPT (Ensuring National Constitutional Rights for Your Private Telecommunications) Act (Feb 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/LIEU_ENCRYPT.Act.of.2016.pdf)
+ [Order Compelling Apple, Inc. to Assist Agents in Search (Feb 16th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)
+ [Government's Motion to Compel Apple Inc. to Comply With This Court's Feb 16th Order (Feb 19th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)
+ [FBI Statement to Address Misleading Reports (Feb 20th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Statement-from-the-FBI-Feb-20-2016.pdf)
+ [Apple's Motion to Vacate Order Compelling Apple Inc. to Assist Agents in Search (Feb 25th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)
+ [Judge Orenstein: In Re Order Requiring Apple, Inc. To Assist In The Execution Of A Search Warrant (Feb 29th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Orenstein-Order-Apple-iPhone-02292016.pdf)
+ [Statement by Apple Lawyer Bruce Sewell: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Testimony-of-Bruce-Sewell-March-1-2016.pdf)
+ [Statement by Professor Susan Landau: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/landau-written-testimony.pdf)
+ [Statement by NY Dist Att C.R. Vance, Jr.: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/vance-written-testimony.pdf)
+ [*Amici Curiae* Brief in Apple Case on Behalf of iPhone Security Experts and Applied Cryptographers (Mar 2nd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/CIS.Technologists.Apple.Brief.Final.pdf)
+ [Brief of *Amici Curiae* EFF & 46 Technologists, Researchers, and Cryptographers (Mar 3rd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/16cm10sp_eff_apple_v_fbi_amicus_court_stamped.pdf)
+ [San Bernardino County District Attorney *Amici Curiae* in Support of the US Government (Mar 3rd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Gov-Uscourts-Cacd-640468-79-0.pdf)
+ [Government's Reply In Support of Motion to Compel & Opposition to Apple Inc.'s Motion (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/DOJ-Apple-20160310.pdf)
+ [Declaration of Tracy L. Wilkison In Support of Government's Reply: Exhibits 1-16 (Mar 10th 2016](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088014.pdf)
+ [Declaration of Stacey Perino In Support of Government's Reply: Exhibits 17-30 (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088016.pdf)
+ [Supplemental Declaration of Christopher Pluhar In Support of Government's Reply (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088015.pdf)
+ [Apple Inc.'s Reply To Government's Opposition To Apple Inc.'s Motion (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Reply-Brief-in-Support-of-Apple-s-Motion-to-Vacate.pdf)
+ [Declaration of Robert Ferrini In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Ferrini-Declaration-Executed.pdf)
+ [Supplemental Declaration of Nicola T. Hanna In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Supp-Hanna-Decl-Executed.pdf)
+ [Supplemental Declaration of Erik Neuenschwander In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Supp-Neuenschwander-Decl-Executed.pdf)
+ [Government's *Ex Parte* Application For A Continuance (March 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/2016-03-21-Ex-Parte-Application-Dckt-191-0.pdf)
+ [Conference: Order Granting Government’s *Ex Parte* Application to Vacate Hearing (March 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/usg-apple-199.pdf)
+ [Order Granting Government’s *Ex Parte* Application to Vacate Hearing (March 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/usg-apple-191.pdf)
+ [The DOJ & FBI Contract Phone Data Extraction & Analysis Company Cellebrite (March 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SearchResults.pdf)

by: **@J9Roem**, keybase.io/j9roem --
`Donations appreciated: 1PytMk24QZB147N9oW1jA6AhAoSsyqLhkB`
