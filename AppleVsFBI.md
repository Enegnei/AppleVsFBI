# #AppleVsFBI
An overview of the important facts in the Apple vs. FBI case, including the main technical &amp; legal concerns
***
## What important events led to this case?
+ Farook's employer, the **San Bernardino County Department of Public Health**, provided him with an iPhone 5C. 
Farook's employer still retained official ownership of the phone ([see lines 22-24 of pg 6](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)), but for some reason *did not install mobile-device management software which was standard on their government-issued work phones* & would have 
[enabled the IT department to remotely unlock the device without user assistance](https://web.archive.org/web/20160220095658/http://mobile.reuters.com/article/idUSKCN0VS2QK).

> "If that particular iPhone was using MobileIron, the county's IT department could unlock it," MobileIron Vice President Ojas Rege told Reuters... If it had been, the high stakes legal battle that has pitted Apple and much of the technology industry against the U.S. government could have been avoided altogether.

+ The FBI has not said this phone was used to communicate with other terrorists 
(Farook is believed to have used another private phone for that, which was destroyed), but rather with his *future victims* ([see lines 16-18 of pg 6](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)). The last date the FBI was able to obtain in the iCloud backup data was **October 9th 2015**, through Farook's account ([see top of pg 11 or line 12 of pg 22](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)). While the FBI states Farook had probably disabled the iCloud automatic-backup feature, [Jonathan Zdziarski](http://www.zdziarski.com/blog/?page_id=202) (iOS digital forensics expert) [argues it was unlikely to be intentional since the *Find-My-iPhone* feature was still enabled](http://www.zdziarski.com/blog/?p=5655), among other factors. He also points out amateur forensics practice mistakes that must have been made when the phone was confiscated (principle among them: [turning the iPhone off](https://twitter.com/JZdziarski/status/701172487061643265)) and raises the important question of why (or if) the victim's phones weren't searched, since they would have copies of the communications the FBI seeks (his full take on the case [here](http://www.zdziarski.com/blog/?p=5645)).

> Find my iPhone is still active on the phone (search by serial number), so why would a terrorist use a phone he knew was tracking him? Obviously he wouldn’t. The Find-my-iPhone feature is on the same settings screen as the iCloud backup feature, so if he had disabled backups, he would have definitely known the phone was being tracked. But the argument that Farook intentionally disabled iCloud backup does not hold water, since he would have turned off Find-my-iPhone as well.

![iCloudbackup](https://pbs.twimg.com/media/CbfRFpiUkAA07La.png)

+ On December 2nd, 2015, Farook and his wife Malik killed 14 people and injured 22 at the Inland Regional Center in California 
during a San Bernardino County Department of Public Health training session/ party. They were pursued by police and died hours later in a shoot-out. The iPhone now in question (a 5C with iOS9) was found by law enforcement in a Black Lexcus IS300.

+ [Within 24 hours of the phone being confiscated](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.fflQoRn36), someone reset the passcode on the phone. 
The FBI's recent motion to compel Apple confirms the passcode was reset *while in government custody* 
and blames it on Farook's employer in the San Bernardino Department of Health ([see footnotes on pg 18](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)).

![footnote](https://pbs.twimg.com/media/CbmnuFqUsAAGLm2.png)

However [San Bernardino County argues](https://web.archive.org/web/20160220180834/https://twitter.com/countywire/status/700887823482630144) they reset the password at the FBI's request.

> "The County was working cooperatively with the FBI when it reset the iCloud password at the FBI's request."

It is unknown whether anyone still knows the passcode. 
If that someone had not reset the passcode & (apparently) forgotten it, the FBI would have been able to access the phone, 
and *this case against Apple would not be necessary*.

![Kenn White @kennwhite](https://pbs.twimg.com/media/Cbn5nsNUcAEoKcB.png)

+ Farook's employer has consented to a law enforcement search of the device ([see lines 22-24 of pg 6](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)).

## Is the FBI demanding Apple “break encryption”?
#### 1) What 'encryption' are we dealing with here?

Based on public court orders, the FBI is demanding Apple build a custom mobile iOS (nicknamed “FBiOS”) 
with two standard passcode security features disabled: the 10-try limit & delayed attempts. 
The 10-try limit wipes an iPhone's data after 10 attempts. This will allow the FBI to perform a brute-force attack, 
where they can guess the passcode as many times & as fast as a computer will allow, without destroying the data.

However, the FBI could technically build this custom iOS on their own (though it will most likely take more time).
The one thing they actually need is for Apple to sign FBiOS using their developer software key, 
because only software signed with this key is able to work in Apple products.

So the 'encryption' we are dealing with here is a matter of authentication.

#### 2) Why does this distinction matter?

Authentication falls under one of the three principles of cybersecurity (CIA), accessibility. 
Authentication deals with anything to prove you hold authorization to carry out specific operations. 
This is something you know (eg. a password), something you have (eg. a card), or something you are (eg. Biometrics).

Authentication is also an element of cryptography, but distinct from privacy/ confidentiality 
(see the [*Purpose* section of Gary C. Kessler's "*An Overview of Cryptography*"](http://www.garykessler.net/library/crypto.html#purpose)).

The San Bernardino phone is said to be locked with a PIN. 
PINs, unlike passwords (which are alphanumeric & can be longer), are numeric and usually very short (4-6 numbers). 
Even if you had a PIN and a password of the same length, it would take you much longer to break the password with brute-force.

Therefore, if the FBI uses this FBiOS, authenticated by Apple's software key, 
it will be able to run on the phone and will most certainly break the PIN.

What should be highlighted here is that Apple claims not to be able to, or at least not want to, access their customer's data. 
Apple customers have an expectation of confidentiality (the first cybersecurity principle), even from Apple itself. 
Apple claims it does not position itself as a party with access to encrypted communications on customer phones. 
If this is true, why is there a threat to encryption?

If the FBI was compelling someone who was a party or key-holder to encrypted communications, 
then it would be more accurate to say that they are “breaking encryption” 
by taking advantage of a social engineering weakness which, at the present time, exists with the majority of encryption use.

The problem here is that the encryption is already broken. 
It has been undermined by Apple's deficient security features, not only due to allowing the use of PINs 
but because they are a centralized point of failure with the ability to backdoor their products.

Taking all of this into consideration, it would be rather more accurate to say 
the FBI is demanding that Apple take advantage of a security flaw which already exists.

## What are the technical & legal concerns involved?
#### Technical Concerns

It is now known that Apple has the ability to backdoor their own products & therefore could be compelled to use that backdoor.

Initially some security experts argued that this backdoor wouldn't work on iPhones newer than 5C 
due to the **Secure Enclave** firmware, [a co-processor of many independently-functioning kernels within the A7 64-bit system chip which also uses secure boot to ensure that all software installed on the OS is signed by Apple](https://web.archive.org/web/20150124040556/http://www.macrumors.com/2014/02/26/touch-id-secure-enclave-document) 
(remember authentication from earlier). Last night, a “senior Apple executive” told journalists at Motherboard & The Guardian
that this is not true – the FBiOS would work with any iPhone currently on the market.

This detail is very important, if true, because many tech journalists (including from Ars Technica) also speculated 
that FBiOS wouldn't even work on other 5C iPhones because, since the FBI is allowing that the custom software 
be tied specifically to the phone's unique identifier, it should be limited to one device. 
They did offer that it might be possible to swap identifiers to apply to any phone. 
Therefore, Apple may not only be admitting that Secure Enclave is not secure enough 
but that it is possible to swap identifiers in this custom OS. This probably has something to do with the fact 
that Apple can force an update to Secure Enclave without wiping the data.

This means that, if leaked, FBiOS could be used on any iPhone.

What has also not yet been confirmed is whether a strong password (not a PIN) remains a safeguard against this attack. 
Since it is only a brute-force attack, a long & complex password should work under normal circumstances 
(taking months to many years to break).

#### Legal Concerns

To understand the legal history behind this case in terms of the US government ordering Apple to "unlock" iPhones, I recommend this clarifying article by **TechCrunch**'s [Matthew Panzarino](https://twitter.com/panzer): "[No, Apple Has Not Unlocked 70 iPhones For Law Enforcement](https://web.archive.org/web/20160220161959/http://techcrunch.com/2016/02/18/no-apple-has-not-unlocked-70-iphones-for-law-enforcement/)." The most important lines are about the difference between *decryption* and *extraction*:

> There are two cases involving data requests by the government which are happening at the moment. There is a case in New York [which] ...involves an iPhone running iOS 7. On devices running iOS 7 and previous, Apple actually has the capability to extract data, including (at various stages in its encryption march) contacts, photos, calls and iMessages without unlocking the phones. That last bit is key, because in the previous cases where Apple has complied with legitimate government requests for information, this is the method it has used.

> It has not unlocked these iPhones — it has extracted data that was accessible while they were still locked.

> The California case, in contrast, involves a device running iOS 9. The data that was previously accessible while a phone was locked ceased to be so as of the release of iOS 8, when Apple started securing it with encryption tied to the passcode, rather than the hardware ID of the device... So Apple is unable to extract any data including iMessages from the device because all of that data is encrypted.


I'm seeing over and over again the comment that the legal precedent(s) this case could set carries more risk 
than the technical risk posed by FBiOS. Since I am not a lawyer, I do not known the specific statutes being considered, 
but here are some of the main points summarized:

+ This court order would force Apple to code a custom iOS 
which deliberately takes advantage of security vulnerabilities in their authentication systems. 
If “code is speech” (and there are cases which affirm this), then speech (here in the form of code) can be compelled. 
It is still an open question of who exactly at Apple can be compelled to do this.

+ If a telecommunications provider can be compelled to take advantage of a security flaw 
undermining encryption for its customers, then they will be compelled. This will put pressure on other businesses 
to either comply or build their products so that they are not a centralized authority of proprietary software.

+ Other countries pay attention to the US on surveillance policy. Though Apple has not said they hold this fear, 
lawyers and security experts say this presents a threat to foreign customers & tech businesses as well.
If the U.S. government can compel Apple to take advantage of a security vulnerability, why not others?
A recent example they cite is where FBI Director James Comey called for encryption backdoors 
& the Chinese government introduced new counter-terrorism laws a few weeks later.

From [*Reuters*](http://www.reuters.com/article/us-usa-obama-china-idUSKBN0LY2H520150302) ("Obama Sharply Criticizes China's Plans for New Technology Rules"):

> “In an interview with Reuters, Obama said he was concerned about Beijing's plans for a far-reaching counterterrorism law 
> that would require technology firms to hand over encryption keys, the passcodes that help protect data, 
> and install security 'backdoors' in their systems to give Chinese authorities surveillance access.”


Sounds oddly familiar, doesn't it?

> To be sure, Western governments, including in the United States and Britain, have for years requested tech firms to disclose encryption methods, with varying degrees of success.

> Officials including FBI director James Comey and National Security Agency (NSA) director Mike Rogers publicly warned Internet companies including Apple and Google late last year against using encryption that law enforcement cannot break.

> Beijing has argued the need to quickly ratchet up its cybersecurity measures in the wake of former NSA contractor Edward Snowden's revelations of sophisticated U.S. spying techniques.
