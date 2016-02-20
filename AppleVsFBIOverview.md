# #AppleVsFBI
An overview of the important facts in the Apple vs. FBI case, including the main technical &amp; legal concerns
***
## What important events led to this case?
1. Farook's employer at the San Bernardino Department of Health provided him with a work phone, an iPhone 5C. 
Farook's employer still retained official ownership of the phone.

2. The FBI has not said this phone was used to communicate with any other terrorists 
(Farook is believed to have used another private phone(s) for that, which was destroyed), but rather with his future victims. 
Communications from October 9th 2015 is the last date available in the iCloud data the FBI
was able to obtain through Farook's account. Farook likely disabled the iCloud backup feature at this day.

3. On December 2nd, 2015, Farook and his wife Malik killed 14 people and injured 22 at the Inland Regional Center 
during a San Bernardino County Department of Public Health training session/ party. 
The iPhone now in question (a 5C with iOS9) was found in one of the cars law enforcement searched.

4. Within 24 hours of the phone being confiscated, someone reset the passcode on the phone. 
The FBI's recent motion to compel Apple confirms the passcode was reset while in government custody 
and blames it on Farook's employer in the San Bernardino Department of Health, 
but it is possible it was the fault of law enforcement or FBI forensics. 
It is unknown whether anyone in any of these agencies still knows the passcode. 
If that someone had not reset the passcode & (apparently) forgotten it, the FBI would have been able to access the phone, 
and this case against Apple would not be necessary.

5. Farook's employer (the official owner of the iPhone) has consented to a law enforcement search of the device.

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
(see the Purpose section of Gary C. Kessler's An Overview of Cryptography).

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
due to the Secure Enclave firmware, a co-processor of many independently-functioning kernels within the A7 64-bit system chip
which also uses secure boot to ensure that all software installed on the OS is signed by Apple 
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

From Reuters:

> “In an interview with Reuters, Obama said he was concerned about Beijing's plans for a far-reaching counterterrorism law 
> that would require technology firms to hand over encryption keys, the passcodes that help protect data, 
> and install security 'backdoors' in their systems to give Chinese authorities surveillance access.”


Sounds oddly familiar, doesn't it?
