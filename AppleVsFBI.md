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

+ The last date the FBI was able to obtain in the iCloud backup data was **October 9th 2015**, through Farook's account ([see top of pg 11 or line 12 of pg 22](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), as iCloud data on Apple's servers is *not* protected by the user's iPhone passcode. While the FBI states Farook had probably disabled the iCloud automatic-backup feature, [Jonathan Zdziarski](http://www.zdziarski.com/blog/?page_id=202) (iOS digital forensics expert) [argues it was unlikely to be intentional since the *Find-My-iPhone* feature was still enabled](http://www.zdziarski.com/blog/?p=5655), among other factors. 

> Find my iPhone is still active on the phone (search by serial number), so why would a terrorist use a phone he knew was tracking him? Obviously he wouldn’t. The Find-my-iPhone feature is on the same settings screen as the iCloud backup feature, so if he had disabled backups, he would have definitely known the phone was being tracked. But the argument that Farook intentionally disabled iCloud backup does not hold water, since he would have turned off Find-my-iPhone as well.


#### After the Attack

+ Zdziarski outlines amateur forensics practice mistakes that were made when, & after, the phone was confiscated; principle among them: [turning the iPhone off](https://twitter.com/JZdziarski/status/701172487061643265) if it was still on, which would lock it. He also raises the important question of why (or if) the victim's phones weren't searched, since they would have copies of the communications the FBI seeks ([his full take on the case here](http://www.zdziarski.com/blog/?p=5645)).

> "Apple engineers saw iCloud backup auth was failing. This tells me FBI seized the phone powered up, and royally blew it turning it off." -*Jonathan Zdziarski* [@JZdziarski](https://twitter.com/JZdziarski/status/701171820884525056)

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

The 10-try limit wipes an iPhone's data after 10 attempts. The time-delays feature will wait 1 minute after four incorrect passcode entries before it accepts another attempt, subsequently increasing to 5 minutes, 15 minutes, and finally 1 hour. Bypassing these features will allow the FBI to perform a [brute-force attack](https://www.techopedia.com/definition/18091/brute-force-attack), where they can guess the passcode as many times & as fast as the iPhone firmware will allow, without destroying the data. Along with disabling these security features, the FBI also wants the custom iOS allow them to enter the passcodes electronically instead of by hand (which would be incredibly slow comparatively).

However, the FBI could technically build this custom iOS on their own (though it will most likely take more time). The one thing they actually need is for Apple to sign FBiOS using their developer software key, because only software signed with this key is able to work in Apple products.

So the 'encryption' we are dealing with here is a matter of *authentication*.

#### 2) Why does this distinction matter?

**Authentication** falls under one of the [three principles of information security (CIA)](http://resources.infosecinstitute.com/guiding-principles-in-information-security/): accessibility. 
Authentication deals with how you prove you hold authorization to carry out specific operations, like accessing an account. 
This is something you know (eg. a password), something you have (eg. a card), or something you are (eg. biometrics).

Authentication is also an element of cryptography, but distinct from privacy/ confidentiality 
(see the [*Purpose* section of Gary C. Kessler's "**An Overview of Cryptography**"](http://www.garykessler.net/library/crypto.html#purpose)).

The San Bernardino phone is said to be locked with a [PIN](https://en.wikipedia.org/wiki/Personal_identification_number). PINs, unlike passwords (which can be [alphanumeric](https://en.wikipedia.org/wiki/Alphanumeric) & longer), are numeric and usually very short (4-6 numbers allowed on average). Even if you had a PIN and a password of the same length, it would probably take more time to break the password with brute-force.

Therefore, if the FBI uses this FBiOS, authenticated by Apple's software key/ digital signature, it will be able to run on Farook's phone and the PIN will be broken within 24 hours.

The definition of a **backdoor** is *something which bypasses normal authentication*. What should be highlighted here is that Apple claims not to be able to, or at least not want to, access their customer's data. Apple customers have an expectation of **confidentiality** (the first information security principle), even from Apple itself. Apple claims it does not position itself as a party with access to encrypted communications on customer phones. If this is true, why is there a threat to encryption?

If the FBI was compelling someone who *was* a party or key-holder to encrypted communications, *then* it would be more accurate to say that they are “breaking encryption” by taking advantage of a social engineering weakness which, at the present time, exists with the majority of encryption use.

The problem here is that the 'encryption' *is already broken*. Quoting from what a "senior Apple executive" said to **Buzzfeed**, Apple's fear that they are being asked to "[create a sort of master key](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6)" is misleading at best, because Apple is not being asked to *create* a key but rather *use the master key they already possess* in conjunction with a custom iOS that lacks two security features. Apple is being pursued because contrary to their commendable implimentation of 'strong encryption,' they retain the ability to backdoor their products, not only through allowing the use of PINs but because they are a centralized point of failure in regards to building proprietary firmware & software. The [**Electronic Frontier Foundation**](https://www.eff.org/about) has published a few pieces on this case and offers only passing criticism of Apple on this point, even though they include passages like this:

> **Would it be easy for Apple to sign the requested cracking software?** The answer any trained security engineer will give you is "it shouldn't be."

> ... There are pros and cons to this approach, but Apple considers this signing key among the crown jewels of the entire company. There is no good revocation strategy if this key is leaked, since its corresponding verification key is hard-coded into hundreds of millions of devices around the world.

It shouldn't be easy, but it's still possible. Disabling security features in so many devices also shouldn't be easy, but it's possible and, considering Apple's response, a very real problem.

Ray Dillinger frames the FBI's court order in a rather interesting way: [as a dramatic & unfriendly bug report](https://web.archive.org/web/20160224005522/http://www.metzdowd.com/pipermail/cryptography/2016-February/028269.html).

![FBI court order as a bug report](https://pbs.twimg.com/media/Cb6-D-eXIAAA1MW.png)

Taking all of this into consideration:
+ Is Apple being asked to "create" a "backdoor"? Unless you consider Apple creating a custom iOS, signed with their special software key, to be outside the bounds of 'normal' in terms of software authentication powers they *already* possessed, the answer is no. Remember that Apple could use this capability at any time, regardless of whether it's compelled or not. If you interpret 'normal' authentication to *not* include Apple's abilities and consider that 1) Apple disabling security features in their OS is an out-of-the-ordinary procedure for them & 2) though now weakly grounded, most Apple customers did have an expectation of confidentiality... then it could be argued that this is "creating a backdoor." You can read [another argument on this from the technical perspective by Brandon Edwards](https://medium.com/@drraid/it-s-a-backdoor-100-2460bf7f8010#.l5nwz4405) (note that I have not made my argument depend on it being limited to one device, which this article focuses on & disputes).
+ Is Apple being told to "break encryption"? Again, it depends on your interpretion. The encryption system of the iOS9 itself is not being broken; security features dealing with how authentication is proven are. [Brute-force attacks](https://www.techopedia.com/definition/18091/brute-force-attack) are a hack of security vulnerabilities, not an encryption backdoor.

Therefore, it would be rather more accurate to say the FBI is demanding that Apple *take advantage of system security vulnerabilities which already exist.* 

## What are the technical & legal concerns involved?
#### Technical Concerns

It is now known that Apple has the ability to backdoor their own products & therefore could be compelled to use that backdoor.

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

![FBiOS tied to unique identifier](https://pbs.twimg.com/media/Cbl9ajvUcAAgJPV.jpg)

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


Note that he advises even an 11-digit *numeric* (numbers only) passcode would be sufficient, though alphanumeric (numbers, characters, and symbols) is stronger because it increases the amount of possible combinations. With a "truly random" 11-digit passcode, it would take *an average of 127 years* to crack on the iPhone with FBiOS. Drawing from page 12 of [Apple's iOS Security White Paper (iOS 9.0 or later)](https://www.apple.com/business/docs/iOS_Security_Guide.pdf), this is due to limitations on how the brute-force attack can be performed:

> The passcode is entangled with the device’s UID, so brute-force attempts must be performed on the device under attack. A large iteration count is used to make each attempt slower. The iteration count is calibrated so that one attempt takes approximately 80 milliseconds. This means it would take more than 5½ years to try all combinations of a six-character alphanumeric passcode with lowercase letters and numbers.


However, these figures only apply if Secure Enclave or another aspect of the iPhone's security architecture isn't also being breached as well, the possibility of which is still up for debate.

With this in mind, a very valuable & proactive thing Apple could do is **recommend that their customers upgrade their passwords.** Until now Apple has given their customers a false sense of security, allowing them to use short passcodes & PINs. The last line of protection should be a strong password, which is under the user's control to change, not a security feature which can apparently be disabled.

#### Legal Concerns

##### --- What is the history behind Apple's compliance with law enforcement? --

To understand the legal history behind this case in terms of the US government ordering Apple to "unlock" iPhones, I recommend this clarifying article by **TechCrunch**'s [Matthew Panzarino](https://twitter.com/panzer): "[No, Apple Has Not Unlocked 70 iPhones For Law Enforcement](https://web.archive.org/web/20160220161959/http://techcrunch.com/2016/02/18/no-apple-has-not-unlocked-70-iphones-for-law-enforcement/)." The most important lines are about the difference between *decryption* and *extraction*:

> There are two cases involving data requests by the government which are happening at the moment. There is a case in New York [which] ...involves an iPhone running iOS 7. On devices running iOS 7 and previous, Apple actually has the capability to extract data, including (at various stages in its encryption march) contacts, photos, calls and iMessages without unlocking the phones. That last bit is key, because in the previous cases where Apple has complied with legitimate government requests for information, this is the method it has used.

> It has not unlocked these iPhones — it has extracted data that was accessible while they were still locked.

> The California case, in contrast, involves a device running iOS 9. The data that was previously accessible while a phone was locked ceased to be so as of the release of iOS 8, when Apple started securing it with encryption tied to the passcode, rather than the hardware ID of the device... So Apple is unable to extract any data including iMessages from the device because all of that data is encrypted.

In short: extraction allows them to access *unencrypted* data on iOS 7 or older; because they have [implimented passcode-based encryption in iPhones running iOS 8 or iOS 9](https://web.archive.org/web/20160222150037/https://www.apple.com/customer-letter/answers/), this data is no longer accessible through extraction. Therefore this request is different compared to Apple's history of compliance, which the court orders have yet to acknowledge.

##### --- What are important factors in legal precedent(s) for the future? ---

I'm seeing over and over again the comment that the legal precedent(s) this case could set carries more risk 
than the technical risk posed by FBiOS. Since I am not a lawyer, I don't know the specific statutes being considered, 
but here are some of the main points summarized:

+ This court order would force Apple to code a custom iOS which deliberately takes advantage of security vulnerabilities in their authentication systems. If “code is speech” (and there are cases which affirm this), then speech (here in the form of code) can be compelled. It is still an open question of who exactly at Apple can be compelled to do this & whether prior precedent of "code is speech" applies (read [Park Higgins' EFF piece on "code is speech" related to 3-D printing](https://www.eff.org/deeplinks/2015/12/3-d-printing-case-code-speech-faces-new-challenges)). At least one of [Apple's objections to the court order will be on First Amendment grounds](https://web.archive.org/web/20160224033346/http://www.latimes.com/local/lanow/la-me-ln-apple-legal-argument-free-speech-20160223-story.html):

> In Apple's fight to knock down a court order requiring it to help FBI agents unlock a killer’s iPhone, the tech giant plans to argue that the judge in the case has overreached in her use of an obscure law and infringed on the company’s 1st Amendment rights, an Apple attorney said Tuesday.

> Theodore J. Boutrous -- one in a pair of marquee lawyers the technology company's has hired to wage its high-stakes legal battle -- outlined the arguments Apple plans when it responds to the court order this week.

> [...] “The government here is trying to use this statute from 1789 in a way that it has never been used before. They are seeking a court order to compel Apple to write new software, to compel speech," Boutrous said in a brief interview with The Times.

> Boutrous said courts have recognized that the writing of computer code is a form of expressive activity -- speech that is protected by the 1st Amendment.

This was confirmed in Apple's first motion against the FBI's court order on February 25th, in addition to objections on Fifth Amendment due process grounds ([see pgs 32 & 34 respectively](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)):

![Apple arguing on First Amendment grounds](https://pbs.twimg.com/media/CcFn9TwXIAQRy11.png:large)

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

+ It is highly unlikely that the FBI does not have alternative means to access the phone or its data in conjunction with the National Security Agency (NSA), as they have a history of mutual cooperation. Legally, alternative means would impact the legitimacy of usin the All Writs Act, as **EFF** explains: "[This point is potentially relevant legally, as cases interpreting the All Writs Act require '*an absence of alternative remedies*.' However, we lack firm evidence that the FBI has such a capability. Apple also probably doesn't want to argue that its phone is insecure so the authorities should just break into it some other way](https://www.eff.org/deeplinks/2016/02/technical-perspective-apple-iphone-case)." Since the FBI continues to say that they *cannot* access the phone without Apple's assistance, they may be deliberately hiding this capability so that they have enough leverage to bring about this open fight with Apple. This would be advtangeous for them in promoting the 'national security vs. encryption' false dichotomy so that public pressure will make it easier to compel companies under similar circumstances in the future. [I have not yet addressed these possible alternative methods but will do so soon.]

***
##### Mirror Links:

+ [iOS Security Whitepaper (Sept 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/iOS_Security_Guide.pdf)
+ [Transcript of Argument from another Apple iPhone case in New York (Nov 27th 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/Transcript.Order-Requiring-Apple-Inc-to-Asisst-in-the.pdf)
+ [Bill of ENCRYPT (Ensuring National Constitutional Rights for Your Private Telecommunications) Act (Feb 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/LIEU_ENCRYPT.Act.of.2016.pdf)
+ [Order Compelling Apple, Inc. to Assist Agents in Search (Feb 16th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)
+ [Government's Motion to Compel Apple Inc. to Comply With This Court's Feb 16th Order (Feb 19th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)
+ [FBI Statement to Address Misleading Reports (Feb 20th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Statement-from-the-FBI-Feb-20-2016.pdf)
+ [Apple's Motion to Vacate Order Compelling Apple Inc. to Assist Agents in Search (Feb 25th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)

by: **@J9Roem**, keybase.io/j9roem --
`Donations appreciated: 1PytMk24QZB147N9oW1jA6AhAoSsyqLhkB`
