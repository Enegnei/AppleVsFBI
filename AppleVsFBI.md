# #AppleVsFBI
An overview of the important facts in the Apple vs. FBI case, including the main technical &amp; legal concerns
***
#### A: [What important events led to this case?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#what-important-events-led-to-this-case)
1. [Before the Attack](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#before-the-attack)
2. [After the Attack](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#after-the-attack)

#### B: [Is the FBI demanding Apple "break encryption"?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#is-the-fbi-demanding-apple-break-encryption)
1. [What 'encryption' are we dealing with here?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#1-what-encryption-are-we-dealing-with-here)
2. [Why does this distinction matter?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#2-why-does-this-distinction-matter)

#### C: [What are the technical & legal concerns involved?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#what-are-the-technical--legal-concerns-involved)
1. [Technical Concerns](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#technical-concerns)
  * [What are the limits to the use of FBiOS?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----what-are-the-limits-to-the-use-of-fbios---)
  * [Could a secure password protect against FbiOS?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----could-a-secure-password-protect-against-fbios---)
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

+ The FBI has not said this phone was used to communicate with other terrorists (Farook is believed to have used another private phone for that, which was destroyed), but rather with his *future victims* ([see lines 16-18 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)). 

![iCloudbackup](https://pbs.twimg.com/media/CbfRFpiUkAA07La.png)

+ The last date the FBI was able to obtain in the iCloud backup data was **October 9th 2015**, through Farook's account ([see top of pg 11 or line 12 of pg 22](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), as iCloud data on Apple's servers is *not* protected by the user's iPhone passcode. While the FBI states Farook had probably disabled the iCloud automatic-backup feature, [Jonathan Zdziarski](http://www.zdziarski.com/blog/?page_id=202) (iOS digital forensics expert) [argues it was unlikely to be intentional since the *Find-My-iPhone* feature was still enabled](http://www.zdziarski.com/blog/?p=5655), among other factors. 

> Find my iPhone is still active on the phone (search by serial number), so why would a terrorist use a phone he knew was tracking him? Obviously he wouldn’t. The Find-my-iPhone feature is on the same settings screen as the iCloud backup feature, so if he had disabled backups, he would have definitely known the phone was being tracked. But the argument that Farook intentionally disabled iCloud backup does not hold water, since he would have turned off Find-my-iPhone as well.


#### After the Attack

+ Zdziarski outlines amateur forensics practice mistakes that could have been made when the phone was confiscated; principle among them: [turning the iPhone off](https://twitter.com/JZdziarski/status/701172487061643265) if it was still on, which would lock it. He also raises the important question of why (or if) the victim's phones weren't searched, since they would have copies of the communications the FBI seeks ([his full take on the case here](http://www.zdziarski.com/blog/?p=5645)).

+ A "senior Apple executive" (one of many who apparently spoke with journalists on a Friday call) claimed that the Apple ID password linked to the iPhone was changed [within 24 hours of the phone being confiscated](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.fflQoRn36). This executive has only come forward now, and thus far remained anonymous, because they "[had thought it was under a confidentiality agreement with the government. Apple seems to believe this agreement is now void since the government brought it up in a public court filing](https://web.archive.org/web/20160221094419/http://arstechnica.com/tech-policy/2016/02/apple-we-tried-to-help-fbi-terror-probe-but-someone-changed-icloud-password/)." The FBI's recent motion to compel Apple confirms the passcode was reset *while in government custody* and blames it on Farook's employer in the San Bernardino Department of Health ([see footnotes on pg 18](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

![footnote](https://pbs.twimg.com/media/CbmnuFqUsAAGLm2.png)

However [San Bernardino County argues](https://web.archive.org/web/20160220180834/https://twitter.com/countywire/status/700887823482630144) they reset the password at the FBI's request.

> "The County was working cooperatively with the FBI when it reset the iCloud password at the FBI's request."

+ In an [inquiry to San Bernardino County CAO David Wert](https://web.archive.org/web/20160221170116/https://www.documentcloud.org/documents/2716811-Statement-from-the-FBI-Feb-20-2016.html), he shares a statement from [Laura Eimiller](linkedin.com/in/laura-eimiller-0595598) (FBI Press & Public Relations at U.S. Department of Justice) which confirms that the County did not "independently conduct analysis" but that "the FBI worked with [them] to reset the *iCloud password* on December 6th," which (as previously stated [in the footnotes on pg 18 here](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)) meant Apple was unable to assist with the auto-backup function on the iPhone. However, unless journalists seriously misquoted the Apple senior executives (who have yet to be personally named), this contradicts their statement that the change was made within 24 hours. This inquiry also shows that the FBI does not know "whether an additional iCloud backup to the phone after that date -- if one had been technically possible -- would have yielded any data." Their reason for pursuing Apple under the All Writs Act order is that they believe there might be "more data [on the iPhone] than an iCloud backup contains," which also contradicts [Apple's assertion that had they not reset the iCloud password/ Apple ID, this case would not be necessary](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6). No information yet on whether anyone in the San Bernardino Health Department or the FBI attempted to reset the iPhone's PIN.

![Kenn White @kennwhite](https://pbs.twimg.com/media/Cbn5nsNUcAEoKcB.png)

+ Farook's employer has consented to a law enforcement search of the device ([see lines 22-24 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

## Is the FBI demanding Apple “break encryption”?
#### 1) What 'encryption' are we dealing with here?

Based on [page 2 of the first public court order](https://web.archive.org/web/20160217152549/https://assets.documentcloud.org/documents/2714001/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf), the FBI is demanding Apple build a custom mobile iOS (which the public has nicknamed “FBiOS”) 
with two standard passcode security features disabled: the 10-try limit & time delays.

![compliance terms](https://pbs.twimg.com/media/CbYZuw7XEAAaziz.png)

The 10-try limit wipes an iPhone's data after 10 attempts. The time-delays feature will wait 1 minute after four incorrect passcode entries before it accepts another attempt, subsequently increasing to 5 minutes, 15 minutes, and finally 1 hour. Bypassing these features will allow the FBI to perform a brute-force attack, 
where they can guess the passcode as many times & as fast as the iPhone firmware will allow, without destroying the data.

However, the FBI could technically build this custom iOS on their own (though it will most likely take more time).
The one thing they actually need is for Apple to sign FBiOS using their developer software key, 
because only software signed with this key is able to work in Apple products.

So the 'encryption' we are dealing with here is a matter of *authentication*.

#### 2) Why does this distinction matter?

**Authentication** falls under one of the [three principles of information security (CIA)](http://resources.infosecinstitute.com/guiding-principles-in-information-security/): accessibility. 
Authentication deals with how you prove you hold authorization to carry out specific operations, like accessing an account. 
This is something you know (eg. a password), something you have (eg. a card), or something you are (eg. biometrics).

Authentication is also an element of cryptography, but distinct from privacy/ confidentiality 
(see the [*Purpose* section of Gary C. Kessler's "**An Overview of Cryptography**"](http://www.garykessler.net/library/crypto.html#purpose)).

The San Bernardino phone is said to be locked with a [PIN](https://en.wikipedia.org/wiki/Personal_identification_number). PINs, unlike passwords (which can be [alphanumeric](https://en.wikipedia.org/wiki/Alphanumeric) & longer), are numeric and usually very short (4-6 numbers allowed on average). Even if you had a PIN and a password of the same length, it would probably take more time to break the password with brute-force.

Therefore, if the FBI uses this FBiOS, authenticated by Apple's software key, it will be able to run on Farook's phone and the PIN will be broken within 24 hours.

What should be highlighted here is that Apple claims not to be able to, or at least not want to, access their customer's data. 
Apple customers have an expectation of **confidentiality** (the first information security principle), even from Apple itself. 
Apple claims it does not position itself as a party with access to encrypted communications on customer phones. 
If this is true, why is there a threat to encryption?

If the FBI was compelling someone who *was* a party or key-holder to encrypted communications, 
*then* it would be more accurate to say that they are “breaking encryption” 
by taking advantage of a social engineering weakness which, at the present time, exists with the majority of encryption use.

The problem here is that the *encryption is already broken*. Quoting from what a "senior Apple executive" said to **Buzzfeed**, Apple's fear that they are being asked to "[create a sort of master key](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6)" is misleading at best, because Apple is not being asked to *create* a key but rather *use the master key they already possess* in conjunction with a custom iOS that lacks two security features. Apple is being pursued because contrary to their proud claims of implimenting 'strong encryption,' they retain the ability to backdoor their products, not only through to allowing the use of PINs but because they are a centralized point of failure in regards to building proprietary firmware & software.

Taking all of this into consideration, it would be rather more accurate to say 
the FBI is demanding that Apple *take advantage of a sytem security flaw which already exists.*

## What are the technical & legal concerns involved?
#### Technical Concerns

It is now known that Apple has the ability to backdoor their own products & therefore could be compelled to use that backdoor.

##### --- What are the limits to the use of FBiOS? --

Initially some security experts argued that this backdoor wouldn't work on iPhones newer than 5C 
due to the **Secure Enclave** firmware, [a co-processor of many independently-functioning kernels within the A7 64-bit system chip which also uses secure boot to ensure that all software installed on the OS is signed by Apple](https://web.archive.org/web/20150124040556/http://www.macrumors.com/2014/02/26/touch-id-secure-enclave-document) 
(remember authentication from earlier). On February 19th, a “senior Apple executive” told journalists at **Motherboard**, [**The Guardian**](https://twitter.com/dannyyadron/status/700830922585743360) and others that this is not true – the FBiOS "[would be effective on every type of iPhone currently being sold](https://web.archive.org/web/20160221092412/http://motherboard.vice.com/read/apple-the-exploit-the-fbi-is-asking-for-would-work-on-all-iphones)."

![Motherboard, Secure Enclave](https://pbs.twimg.com/media/CbnuF7iVIAE0A76.jpg)

This detail is very important, if true, because many tech journalists (including from **Ars Technica**) also speculated 
that [FBiOS wouldn't even work on other 5C iPhones](https://web.archive.org/web/20160219203100/http://arstechnica.com/apple/2016/02/encryption-isnt-at-stake-the-fbi-knows-apple-already-has-the-desired-key/) because, since the FBI is allowing that the custom software 
be tied specifically to the phone's unique identifier, it should be limited to this *one* device. 

![FBiOS working on older phones](https://pbs.twimg.com/media/Cbl8EghUkAA5vMr.jpg)

A description of the Unique Identifier (UID) can be found on page 59 of [Apple's iOS Security Whitepaper](https://www.apple.com/business/docs/iOS_Security_Guide.pdf):

> A 256-bit AES key that’s burned into each processor at manufacture. It cannot be read by firmware or software, and is used only by the processor’s hardware AES engine. To obtain the actual key, an attacker would have to mount a highly sophisticated and expensive physical attack against the processor’s silicon. The UID is not related to any other identifier on the device 
including, but not limited to, the UDID.

Because the UID is "baked into its hardware," **Ars Technica** editor [Peter Bright](https://web.archive.org/web/20160216072035/http://arstechnica.com/author/peter-bright/) says that this request makes the assumption that the UID can be extracted -- which appears to be a difficult process.

Difficulty of extraction aside, he does offer that it *might* be possible to swap identifiers to apply to other 5C phones. 

![FBiOS tied to unique identifier](https://pbs.twimg.com/media/Cbl9ajvUcAAgJPV.jpg)

Therefore, Apple may not only be admitting that Secure Enclave is not secure enough 
but that it is possible to swap identifiers in this custom OS. This probably has something to do with the fact 
that Apple can force an update to Secure Enclave without wiping the data.

This means that, if leaked, *FBiOS could be used on any iPhone*.

##### --- Could a secure password protect against FBiOS? --

What has also not yet been confirmed by Apple is whether a strong password (not a PIN) remains a safeguard against this attack. Since it is only a brute-force attack, a long & complex password should work under normal circumstances 
(taking months to many years to break). [Micah Lee](https://theintercept.com/staff/micah-lee/), a technologist at the **The Intercept**, [says it would](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/):

> It’s true that ordering Apple to develop the backdoor will fundamentally undermine iPhone security, as Cook and other digital security advocates have argued. But it’s possible for individual iPhone users to protect themselves from government snooping by setting strong passcodes on their phones — passcodes the FBI would not be able to unlock even if it gets its iPhone backdoor.

> ...The short version: If you’re worried about governments trying to access your phone, set your iPhone up with a random, 11-digit numeric passcode.


Note that he advises even an 11-digit *numeric* (numbers only) passcode would be sufficient, though alphanumeric (numbers, characters, and symbols) is stronger because it increases the amount of possible combinations. With a "truly random" 11-digit passcode, it would take *an average of 127 years* to crack on the iPhone with FBiOS. Drawing from page 12 of [Apple's iOS Security White Paper (iOS 9.0 or later)](https://www.apple.com/business/docs/iOS_Security_Guide.pdf), this is due to limitations on how the brute-force attack can be performed:

> The passcode is entangled with the device’s UID, so brute-force attempts must be performed on the device under attack. A large iteration count is used to make each attempt slower. The iteration count is calibrated so that one attempt takes approximately 80 milliseconds. This means it would take more than 5½ years to try all combinations of a six-character alphanumeric passcode with lowercase letters and numbers.


However, these figures only apply if Secure Enclave or another aspect of the iPhone's security architecture isn't also being breached as well, the possibility of which is still up for debate.

#### Legal Concerns

##### --- What is the history behind Apple's compliance with law enforcement? --

To understand the legal history behind this case in terms of the US government ordering Apple to "unlock" iPhones, I recommend this clarifying article by **TechCrunch**'s [Matthew Panzarino](https://twitter.com/panzer): "[No, Apple Has Not Unlocked 70 iPhones For Law Enforcement](https://web.archive.org/web/20160220161959/http://techcrunch.com/2016/02/18/no-apple-has-not-unlocked-70-iphones-for-law-enforcement/)." The most important lines are about the difference between *decryption* and *extraction*:

> There are two cases involving data requests by the government which are happening at the moment. There is a case in New York [which] ...involves an iPhone running iOS 7. On devices running iOS 7 and previous, Apple actually has the capability to extract data, including (at various stages in its encryption march) contacts, photos, calls and iMessages without unlocking the phones. That last bit is key, because in the previous cases where Apple has complied with legitimate government requests for information, this is the method it has used.

> It has not unlocked these iPhones — it has extracted data that was accessible while they were still locked.

> The California case, in contrast, involves a device running iOS 9. The data that was previously accessible while a phone was locked ceased to be so as of the release of iOS 8, when Apple started securing it with encryption tied to the passcode, rather than the hardware ID of the device... So Apple is unable to extract any data including iMessages from the device because all of that data is encrypted.


##### --- What are important factors in legal precedent(s) for the future? ---

I'm seeing over and over again the comment that the legal precedent(s) this case could set carries more risk 
than the technical risk posed by FBiOS. Since I am not a lawyer, I don't know the specific statutes being considered, 
but here are some of the main points summarized:

+ This court order would force Apple to code a custom iOS 
which deliberately takes advantage of security vulnerabilities in their authentication systems. 
If “code is speech” (and there are cases which affirm this), then speech (here in the form of code) can be compelled. 
It is still an open question of who exactly at Apple can be compelled to do this.

+ If a telecommunications provider *can* be compelled to take advantage of a security flaw 
undermining encryption for its customers, then they *will* be compelled. This will put pressure on other businesses 
to either comply or build their products so that they are not a centralized authority of proprietary software.

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

***
##### Mirror Links:
+ [Order Compelling Apple, Inc. to Assist Agents in Search (Feb 16th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)
+ [Government's Motion to Compel Apple Inc. to Comply With This Court's Feb 16th Order (Feb 19th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)
+ [FBI Statement to Address Misleading Reports (Feb 20th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Statement-from-the-FBI-Feb-20-2016.pdf)

`Donations appreciated: 1PytMk24QZB147N9oW1jA6AhAoSsyqLhkB`
