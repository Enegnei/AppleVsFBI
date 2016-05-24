# #AppleVsFBI
An overview of the important facts in the Apple vs. FBI case, including post-case technical &amp; legal concerns

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
 
#### D: [How did the FBI access the iPhone & who helped them do it?](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#how-did-the-fbi-access-the-iphone--who-helped-them-do-it)
1. [The Post-Case Investigation](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#the-post-case-investigation)
2. [The Burr-Feinstein Encryption Bill](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#the-burr-feinstein-encryption-bill)
3. [Post-AppleVsFBI Encryption Panels & Committees](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#post-applevsfbi-encryption-panels--committees)

***

## What important events led to this case?

+ On December 2nd, 2015, Syed Rizwan Farook and his wife Tashfeen Malik killed 14 people and injured 22 at the Inland Regional Center in California during a San Bernardino County Department of Public Health training session/ party. They were pursued by police and died hours later in a shoot-out. The iPhone at the center of this case, a 5C with iOS9, was found by law enforcement in a Black Lexcus IS300 ([see lines 23-4 of pgs 4-5](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

![Farook & iPhone](http://cdn.images.express.co.uk/img/dynamic/1/590x/Apple01-656356.jpg)

#### Before the Attack

+ The phone was the property of Farook's employer, the **San Bernardino County Department of Public Health**. 
It had been issued to Farook for work & the County still retained official ownership of the phone at the time of the attack ([see lines 22-24 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), but for some reason *had neglected to install mobile-device management software which was standard on their government-issued work phones* & would have 
[enabled the IT department to remotely unlock the device when needed without user assistance](https://web.archive.org/web/20160220095658/http://mobile.reuters.com/article/idUSKCN0VS2QK).

> "If that particular iPhone was using MobileIron, the county's IT department could unlock it," MobileIron Vice President Ojas Rege told Reuters... If it had been, the high stakes legal battle that has pitted Apple and much of the technology industry against the U.S. government could have been avoided altogether.

+ The FBI never claimed this phone was used to communicate with other terrorists, but rather with his wife and/ or *future victims* ([see lines 16-18 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)). Farook is believed to have used other private phones for that, two of which were found destroyed behind their residence ([see lines 1-4 pg 22 or *pg 4 of Pluhar's declaration*](https://web.archive.org/web/20160401192853/http://web.cs.ucdavis.edu/~rogaway/privacy-seminar/iphone-fbi-decrypt.pdf)).

![two iPhones destroyed](https://pbs.twimg.com/media/Cbc0dtxXIAAIG8J.jpg)

+ Through accessing Farook's account, the last date the FBI had been able to obtain in the iCloud backup data was **October 19th 2015** ([see top of pg 11 or line 12 of pg 22](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)), as iCloud data on Apple's servers is *not* protected by the user's iPhone passcode. The FBI stated that Farook [changed his iCloud password & disabled the iCloud automatic-backup feature on **October 22nd**](https://camo.githubusercontent.com/f2fab381d1018fa00730b1e960a6140ac74228a0/68747470733a2f2f7062732e7477696d672e636f6d2f6d656469612f43644f5463515456414141615043502e6a7067); [Jonathan Ździarski](http://www.zdziarski.com/blog/?page_id=202) (iOS digital forensics expert) [argued it was unlikely to be intentional since the *Find-My-iPhone* feature was still enabled](http://www.zdziarski.com/blog/?p=5655), among other factors. 

![iCloudbackup](https://pbs.twimg.com/media/CbfRFpiUkAA07La.png)

> Find my iPhone is still active on the phone (search by serial number), so why would a terrorist use a phone he knew was tracking him? Obviously he wouldn’t. The Find-my-iPhone feature is on the same settings screen as the iCloud backup feature, so if he had disabled backups, he would have definitely known the phone was being tracked. But the argument that Farook intentionally disabled iCloud backup does not hold water, since he would have turned off Find-my-iPhone as well. --*Jonathan Ździarski* [@JZdziarski](https://twitter.com/JZdziarski)


#### After the Attack

> "Apple engineers saw iCloud backup auth was failing. This tells me FBI seized the phone powered up, and royally blew it turning it off." --*Jonathan Ździarski* [@JZdziarski](https://twitter.com/JZdziarski/status/701171820884525056)

+ Ździarski outlined amateur forensics practice mistakes that could have been made when, & after, the phone was confiscated; principle among them: [turning the iPhone off](https://twitter.com/JZdziarski/status/701172487061643265) if it was still on, which would lock it. He also raised the important question of why (or if) the victim's phones weren't searched, since they would have copies of the communications the FBI seeks ([his full take on the case here](http://www.zdziarski.com/blog/?p=5645)). He was among the iPhone security experts who submitted an [“amici curiae" brief](https://web.archive.org/web/20160303095429/https://cyberlaw.stanford.edu/files/blogs/CIS%20Technologists%20Apple%20Brief%20Final.pdf) through [**The Center for Internet and Society**](https://cyberlaw.stanford.edu/blog/2016/03/cis-files-amici-curiae-brief-apple-case-behalf-iphone-security-experts-and-applied) (see **Techdirt**'s [full list of *amici curiae* briefs submitted so far](https://www.techdirt.com/articles/20160303/23482933802/we-read-all-20-filings-support-apple-against-fbi-here-are-most-interesting-points.shtml), with analysis). The FBI contradicted the claim made by Apple engineers & Supervisory Special Agent Christopher Pluhar said "Farook's iPhone was found powered off" ([see pg 29 lines 7-17](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf) or [pg 2 lines 7-17](https://web.archive.org/web/20160311021811/https://assets.documentcloud.org/documents/2755240/031123088015.pdf)). Ździarksi said "[the best way to determine if the device truly was off or not is to release the carrier’s tower records showing last activity](https://web.archive.org/web/20160311002204/https://twitter.com/JZdziarski/status/708078399844171776)."

![FBI says iPhone was off](https://pbs.twimg.com/media/CdOTcQTVAAAaPCP.jpg)
![FBI says iPhone was off 2](https://pbs.twimg.com/media/CdOKlI5WwAAjiG9.jpg)


+ A "senior Apple executive" (one of many who apparently spoke with journalists on a Friday call) claimed that the Apple ID password linked to the iPhone was changed [within 24 hours of the phone being confiscated](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.fflQoRn36). This executive only came forward, and thus far remained anonymous, because they "[had thought it was under a confidentiality agreement with the government. Apple seems to believe this agreement is now void since the government brought it up in a public court filing](https://web.archive.org/web/20160221094419/http://arstechnica.com/tech-policy/2016/02/apple-we-tried-to-help-fbi-terror-probe-but-someone-changed-icloud-password/)." The FBI's motion to compel Apple confirmed the passcode was reset *while in government custody* and blamed it on Farook's employer in the **San Bernardino Department of Health** ([see footnotes on pg 18](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

![footnote](https://pbs.twimg.com/media/CbmnuFqUsAAGLm2.png)

However [San Bernardino County argued](https://web.archive.org/web/20160220180834/https://twitter.com/countywire/status/700887823482630144) they had reset the password at the FBI's request.

> "The County was working cooperatively with the FBI when it reset the iCloud password at the FBI's request."

+ In an [inquiry to San Bernardino County CAO David Wert](https://web.archive.org/web/20160221170116/https://www.documentcloud.org/documents/2716811-Statement-from-the-FBI-Feb-20-2016.html), he shared a statement from [Laura Eimiller](linkedin.com/in/laura-eimiller-0595598) (FBI Press & Public Relations at U.S. Department of Justice) which confirmed that the County did not "independently conduct analysis" but that "the FBI worked with [them] to reset the *iCloud password* on December 6th," which (as previously stated [in the footnotes on pg 18 here](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)) meant Apple was unable to assist with the auto-backup function on the iPhone. However, unless journalists seriously misquoted the Apple senior executives (who have yet to be personally named), this contradicted their statement that the change was made within 24 hours. This inquiry also showed that the FBI did not know "whether an additional iCloud backup to the phone after that date -- if one had been technically possible -- would have yielded any data." Their reason for pursuing Apple under the All Writs Act order was that they believe there might be "more data [on the iPhone] than an iCloud backup contains," which also contradicts [Apple's assertion that had they not reset the iCloud password/ Apple ID, this case would not be necessary](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6). The pieces of "device-level data" the FBI wanted to access from the phone itself included the keyboard cache ([see pg 29 line 22](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf)); the claim that there was more keyboard cache data in the device than on the iCloud backup is disputed by Ździarski [here](https://web.archive.org/web/20160313082705/https://twitter.com/jzdziarski/status/708782855409815553). Likewise, [San Bernardino Police Chief Jarrod Burguan has said](https://theintercept.com/2016/02/26/farooks-iphone-is-probably-useless-even-the-police-say-so/) "there is a reasonably good chance that there is nothing of any value on the phone."

![Kenn White @kennwhite](https://pbs.twimg.com/media/Cbn5nsNUcAEoKcB.png)

+ Farook's employer consented to a law enforcement search of the device ([see lines 22-24 of pg 6](https://web.archive.org/web/20160220002724/http://www.politico.com/f/?id=00000152-fae6-d7cd-af53-fafe53bb0002)).

+ The government filed their [*ex parte*](http://legal-dictionary.thefreedictionary.com/ex+parte) application & released [their first Order to assist](https://web.archive.org/web/20160217152549/https://assets.documentcloud.org/documents/2714001/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf) on February 16th; Apple said they were not contacted about it directly beforehand but were instead given notice through the press in conjunction with the public ([see footnotes on pg 11](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)).

![Apples says government didn't give "chance to be heard](https://prod01-cdn07.cdn.firstlook.org/wp-uploads/sites/1/2016/02/5.png)

+ On February 22nd, the [**Pew Research Center**](https://archive.is/M3eSt) released [a survey conducted Feb. 18-21](https://web.archive.org/web/20160310052849/http://www.people-press.org/files/2016/02/2-22-2016-iPhone-release.pdf) among 1,002 American adults (varying by age, education, political identity, and smartphone ownership) where they asked whether Apple should unlock the San Bernardino suspect’s iPhone to aid the FBI’s ongoing investigation. Overall, 51% of Americans said Apple should unlock the iPhone; 38% said they should not unlock it; the remaining 11% did not offer an opinion either way. When separated based on their political identity, "*almost identical shares of Republicans (56%) and Democrats (55%) say that Apple should unlock the San Bernardino suspect’s iPhone. By contrast, independents are divided: 45% say Apple should unlock the iPhone, while about as many (42%) say they should not unlock the phone*." The results were a bit more divided among non-partisan Independents, with "unlock" still being favored. When separated based on education, there was no definitive trend between less- or more-educated, though difference of opinion was greatest among those with "some college" education: 34% said Apple should not unlock the iPhone while 56% said they should. Those in the "some college" education group also had the highest percentage of them support unlocking the iPhone (56%) compared to other levels of education. When separated based on age, the older the respondent was, the more likely it was they would support unlocking the iPhone or offer no opinion. When separated based on smartphone ownership, respondents were more likely to be against Apple unlocking the iPhone if 1) they owned a smartphone 2) their smartphone was an iPhone.

![Pew Research study graph](https://pbs.twimg.com/media/Cb87udLUMAEDnVX.jpg)

+ The [US House of Representatives Committee on the Judiciary](http://judiciary.house.gov/index.cfm/hearings?ID=89431275-E911-4D5C-BD70-BFE3EF91AD86) held a session to discuss this court case on March 1st, with [FBI Director James Comey](https://web.archive.org/web/20160315071544/https://www.fbi.gov/about-us/executives/comey), Apple Senior Vice President [Bruce Sewell](https://web.archive.org/web/20160310152653/http://www.apple.com/pr/bios/bruce-sewell.html), Professor [Susan Landau]( https://web.archive.org/web/20160322052351/http://www.privacyink.org/) (co-author of "[*Privacy On The Line: The Politics of Wiretapping and Encryption*](https://web.archive.org/web/20160306014712/https://mitpress.mit.edu/books/privacy-line)"), & New York County District Attorney [Cyrus R. Vance Jr.](https://web.archive.org/web/20160316182705/http://manhattanda.org/meet-cy-vance) as witnesses. "[The Encryption Tightrope: Balancing Americans' Security & Privacy](https://youtu.be/g1GgnbN9oNw)" is available on YouTube (I also have a local .mp4 copy in case it is taken down).

+ On March 3rd, [Microsoft](https://archive.is/tEOTH) and fourteen other tech companies [filed an *amicus curiae* brief together in support of Apple](https://web.archive.org/web/20160417090812/http://mscorpmedia.azureedge.net/mscorpmedia/2016/03/smith_post.pdf). San Bernardino County District Attorney [Michael Ramos](http://www.sbcountyda.org/AboutDARamos/AboutDistrictAttorneyMichaelRamos.aspx) also filed an *amicus curiae* brief but in support of the FBI, which is still being mocked for speculating about a "lying-dormant cyber pathogen endangering San Bernardino County's infrastructure" on the iPhone ([see pg 3 or *6/40*](https://web.archive.org/web/20160305131629/https://assets.documentcloud.org/documents/2748053/Gov-Uscourts-Cacd-640468-79-0.pdf)). [Jeremiah Grossman](https://twitter.com/jeremiahg), founder of [White Hat Security](https://www.whitehatsec.com/), has created the webpage [www.cyberpathogen.com](http://www.cyberpathogen.com/) displaying the quote & linking to [Ździarski's article on the document](http://www.zdziarski.com/blog/?p=5849).

![SB DA brief statement](https://pbs.twimg.com/media/CcrIGwVW4AAipPA.jpg)

+ On March 4th, **UN High Commissioner for Human Rights** [Zeid Ra’ad Al Hussein](http://www.ohchr.org/EN/AboutUs/Pages/HighCommissioner.aspx) [released a statement on the case leaning in Apple's favor](https://web.archive.org/web/20160306001954/http://www.ohchr.org/EN/NewsEvents/Pages/DisplayNews.aspx?NewsID=17138&LangID=E), expressing concern for the safety of citizens as well as "human rights defenders, civil society, journalists, whistle-blowers and political dissidents" in authoritarian countries who would likely demand more access upon seeing the FBI successfully compel Apple.

![UN statement](https://pbs.twimg.com/media/CcsdTM3W0AAkKvr.jpg)

#### The Trial

+ On March 21st, one day before the scheduled hearing, the Department of Justice announced in a filing that it wanted to postpone or possibly cancel the hearing, claiming that "an outside party demonstrated to the FBI a possible method for unlocking Farook's iPhone" ([see pg 3](https://web.archive.org/web/20160321231145/https://assets.documentcloud.org/documents/2773489/2016-03-21-Ex-Parte-Application-Dckt-191-0.pdf)). *It was not stated who that outside party is*, though **The Intercept** says [the Department of Justice told reporters they don't work for the government](https://theintercept.com/2016/03/21/government-showdown-with-apple-delayed/). The DOJ and FBI [jointly contracted a New Jersey vendor](https://web.archive.org/web/20160323152857/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+PIID%3A%22DJF161200P0004424%22&renderer=jsp&length=1) of the Israel-based company [**Cellebrite**](http://www.cellebrite.com/) (which [manufactures data extraction & analysis devices for phones](https://web.archive.org/web/20160323225347/http://www.cellebrite.com/Pages/ios-forensics-physical-extraction-decoding-and-analysis-from-ios-devices)) [on the same day](https://web.archive.org/web/20160323152753/https://www.fpds.gov/ezsearch/fpdsportal?q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+PIID%3A%22DJF161200P0004424%22&s=FPDSNG.COM&templateName=1.4.4&indexName=awardfull&sortBy=SIGNED_DATE&desc=Y). **Reuters** says [the Tel Aviv national daily newspaper **Yedioth Ahronoth** (in Hebrew) reported two days later](https://web.archive.org/web/20160323162001/http://www.yediot.co.il/articles/0,7340,L-4781928,00.html) that [the contract was indeed part of the San Bernardino investigation](https://web.archive.org/web/20160323154820/http://www.reuters.com/article/us-apple-encryption-cellebrite-idUSKCN0WP17J). Neither the US government nor **Cellebrite** have commented on the nature of the partnership. Emily Chang, host of [**Bloomberg West**](https://en.wikipedia.org/wiki/Bloomberg_West), soon [claimed that the request was accepted by the judge](https://web.archive.org/web/20160321235306/https://twitter.com/emilychangtv/status/712060838539108352), which was confirmed by [a record of a telephonic conference](https://cryptome.org/2016/03/usg-apple-199.pdf) & subsequent filing in reply ([see the last page](https://cryptome.org/2016/03/usg-apple-191.pdf)). The government was required to file a status report on April 5th 2016 after two weeks of testing this new method, at which time either a new date would have been set or the trial cancelled altogether. The method that was being tested is believed to be [some variation of the NAND copying / mirroring technique](https://github.com/Enegnei/AppleVsFBI/blob/master/AppleVsFBI.md#----could-a-secure-password-protect-against-fbios---).

![contracting Cellebrite](https://pbs.twimg.com/media/CePaYXPVIAECN9N.jpg:large)
![postpone hearing](https://pbs.twimg.com/media/CeG3bAWUUAAAOe_.jpg:large)

+ On March 28th, the government filed a status report requesting that the order compelling Apple to assist the FBI be vacated because they had "now successfully accessed the data stored on Farook’s iPhone and therefore no longer require[d] the assistance from Apple" ([see here](https://web.archive.org/web/20160328220521/http://pdfserver.amlaw.com/nlj/FBI_apple_20160328.pdf)). [The request was accepted](https://cryptome.org/2016/03/usg-apple-210.pdf) the following day, effectively ending the case in San Bernardino; however several other cases are still ongoing and Apple used the outcome of this case to argue that the government hasn't demonstrated their assistance to be necessary ([see pg 1 or *10/55*](https://web.archive.org/web/20160418004208/https://assets.documentcloud.org/documents/2804250/FBI-Apple-EDNY-Apple-Response-04152016.pdf)). On April 22nd, that case in New York ended with the government [filing another application to vacate the order](https://web.archive.org/web/20160423143028/https://assets.documentcloud.org/documents/2811132/123111836100.pdf) since "an individual provided the passcode to the iPhone at issue in this case. Late last night, the government used that passcode by hand and gained access to the iPhone."

![preliminary statement from New York case](https://pbs.twimg.com/media/CgSNpaRUkAAmBGD.jpg:large)
![FBI vacates another assistance order](https://pbs.twimg.com/media/CgsTyl5UUAA2VLH.jpg)

+ "[The FBI is currently reviewing the information on the phone, consistent with standard investigatory procedures](https://web.archive.org/web/20160402200552/http://abcnewsradioonline.com/business-news/justice-department-withdraws-request-in-apple-iphone-encrypt.html)," said [Department of Justice public affairs director Melanie Newman](https://web.archive.org/web/20160402070810/https://www.justice.gov/opa). The method used, and the identity of the "outside party," have still not been made public. However, on the same day, the DOJ and FBI [jointly signed another purchase order contract](https://web.archive.org/web/20160331143817/https://www.fpds.gov/ezsearch/fpdsportal?q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+PRODUCT_OR_SERVICE_CODE%3A%227045%22&s=FPDSNG.COM&templateName=1.4.4&indexName=awardfull&x=16&y=11) with suspected third-party [**Cellebrite**](https://web.archive.org/web/20160402144447/http://www.cellebrite.com/Media/Default/Files/Corporate/Cellebrite-Company-Profile.pdf) for ["Information Technology Supplies" valued at $218,000](https://web.archive.org/web/20160331142249/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+PRODUCT_OR_SERVICE_CODE%3A%227045%22&renderer=jsp&length=1). Based on [contracting records from 2008-2016](https://web.archive.org/web/20160402143242/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=Cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22&renderer=jsp&length=199), where the majority are valued between $3,000-20,000, this is their most expensive contract (the second most expensive being a [Feb 21st 2014 purchase order for communications equipment at $120,000](https://web.archive.org/web/20160402145017/https://www.fpds.gov/ezsearch/fpdsportal?q=Cellebrite+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2014+PIID%3A%22DJF141200P0003847%22&s=FPDSNG.COM&templateName=1.4.4&indexName=awardfull&x=0&y=0)).

![government request to vacate](https://pbs.twimg.com/media/CeqpZnRWsAE4GRK.jpg:large)
![government request to vacate accepted](https://pbs.twimg.com/media/CewQbuXWwAAE1We.jpg:large)
![contracting with Cellebrite 2](https://pbs.twimg.com/media/CeufMi1XEAAfC4F.jpg:large)

***
## Is the FBI demanding Apple “break encryption”?
#### 1) What 'encryption' are we dealing with here?

The FBI was demanding Apple build a custom mobile iOS with two standard passcode security features disabled: the 10-try limit & escalating time delays ([see pg 2](https://web.archive.org/web/20160217152549/https://assets.documentcloud.org/documents/2714001/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)).

> *Note: Court filings & articles refer to the custom mobile iOS by different names, most commonly 'GovtOS' & 'FBiOS'. For the purposes of consistency to avoid confusion, this overview will use 'FBiOS.'*

![compliance terms](https://pbs.twimg.com/media/CbYZuw7XEAAaziz.png)

The 10-try limit wipes an iPhone's data after 10 attempts. The time-delays feature will wait 1 minute after four incorrect passcode entries before it accepts another attempt, subsequently increasing to 5 minutes, 15 minutes, and finally 1 hour. Bypassing these features would have allowed the FBI to perform a [brute-force attack](https://www.techopedia.com/definition/18091/brute-force-attack), where they could guess the passcode as many times & as fast as the iPhone firmware will allow, without destroying the data. Along with disabling these security features, the FBI also wanted the custom iOS to allow them to enter the 10,000 possible passcode combinations electronically instead of by hand (which would have been incredibly slow comparatively). This would have likely been done through [Device Firmware Upgrade (DFU) mode](https://web.archive.org/web/20160312000032/http://arstechnica.com/apple/2016/03/there-are-ways-the-fbi-can-crack-the-iphone-pin-without-apple-doing-it-for-them/), normally used for [restoration by installing a fresh iOS version when an iPhone fails to boot](https://www.theiphonewiki.com/wiki/DFU_Mode).

However, the FBI could have technically built this custom iOS on their own (though it would take more time). The one thing they actually needed was for Apple to sign FBiOS using their developer software key, because only software signed with this key will be accepted by SecureRom's signature checker (though jailbreakers have found bugs in the past which let them bypass this).

So the 'encryption' we were dealing with was a matter of *authentication*.

#### 2) Why does this distinction matter?

**Authentication** falls under one of the [three principles of information security (CIA)](http://resources.infosecinstitute.com/guiding-principles-in-information-security/): accessibility. 
Authentication deals with how you prove you hold authorization to carry out specific operations, like accessing an account. 
This is something you know (eg. a password), something you have (eg. a card), or something you are (eg. biometrics).

Authentication is also an element of cryptography, but distinct from privacy/ confidentiality 
(see the [*Purpose* section of Gary C. Kessler's "**An Overview of Cryptography**"](http://www.garykessler.net/library/crypto.html#purpose)).

The San Bernardino phone was locked with a 4-digit [PIN](https://en.wikipedia.org/wiki/Personal_identification_number). PINs, unlike passwords (which can be [alphanumeric](https://en.wikipedia.org/wiki/Alphanumeric) & longer), are numeric and usually very short (4-6 numbers allowed on average). Even if you had a PIN and a password of the same length, it would probably take more time to break the password with brute-force.

Therefore, if the FBI used FBiOS, authenticated by Apple's software key/ digital signature, it would have been able to run on Farook's phone and broken the PIN within 24 hours.

The definition of a [**backdoor**](http://www.linfo.org/backdoor.html) is *something which bypasses normal authentication*. Or, more (perhaps too) broadly:

> **backdoor:** A design fault, planned or accidental, that allows the apparent strength of the design to be easily avoided by those who know the trick -- *Newton's Telecom Dictionary: 28th Updated & Expanded Edition*

What should be highlighted here is that Apple claimed not to be able to, or at least not want to, access their customer's data. Apple customers have an expectation of **confidentiality** (the first information security principle) even from Apple itself. Apple does not position itself as a party with access to encrypted communications on customer phones. If this is true, why is there a threat to encryption?

If the FBI was compelling someone who *was* a party or key-holder to encrypted communications, *then* it would be more accurate to say that they were “breaking encryption” by taking advantage of a social engineering weakness which, at the present time, exists with the majority of encryption use.

The problem was that the 'encryption' *is already broken*. Quoting from what a "senior Apple executive" said to **Buzzfeed**, Apple's fear that they have been asked to "[create a sort of master key](https://web.archive.org/web/20160220223312/http://www.buzzfeed.com/johnpaczkowski/apple-terrorists-appleid-passcode-changed-in-government-cust?utm_term=.nvweoJwEO#.igPwBeOq6)" is misleading at best, because Apple was not asked to *create* a key but rather *use the master key they already possess* in conjunction with a custom iOS that lacked two security features. 

> [Thus, in the sense that the word is being used in the media, the ‘backdoor’ already exists. The ‘key to all locks’ is Apple’s private signing key](https://medium.com/@liamkirsh/your-iphone-already-has-a-backdoor-33f43cceefdb#.p32cuvp5t). --*Liam Kirsh* [@choicefresh](https://twitter.com/choicefresh)

**Firefox** founder [Blake Ross](https://twitter.com/blakeross) offered a very well-written & humorous take on [how security holes fail us, in both our digital & non-digital lives](https://medium.com/@blakeross/mr-fart-s-favorite-colors-3177a406c775#.wg0g6fcpu), and says this debate was about whether "a private company [should] be allowed to sell unbreakable security."

> To be clear: Contrary to a lot of shoddy reporting, and some rather “generous” language from Apple, this is not the world we’re living in yet. The fact that Apple can break into your phone demonstrates that we’re still firmly in “Coke recipe” territory.

[Leif Ryge](https://twitter.com/wiretapped) from **Ars Technica** explained why [being a single point of failure is the bigger issue *industry-wide*](https://web.archive.org/web/20160227165908/http://arstechnica.com/security/2016/02/most-software-already-has-a-golden-key-backdoor-its-called-auto-update/):

> How did we get here? How did so many well-meaning people build so many fragile systems with so many obvious single points of failure?

> I believe it was a combination of naivety and hubris. They probably thought they would be able keep the keys safe against realistic attacks, and they didn't consider the possibility that their governments would actually compel them to use their keys to sign malicious updates.

> Fortunately, there is some good news. The FBI is presently demonstrating that this was never a good assumption, which finally means that the people who have been saying for a long time that we need to remove these single points of failure can't be dismissed as unreasonably paranoid anymore.

> ... So when Apple says the FBI is trying to "force us to build a backdoor into our products," what they are really saying is that the FBI is trying to force them to use a backdoor which already exists in their products. (The fact that the FBI is also asking them to write new software is not as relevant, because they could pay somebody else to do that. The thing that Apple can provide which nobody else can is the signature.)

> Is it reasonable to describe these single points of failure as backdoors? I think many people might argue that industry-standard systems for ensuring software update authenticity do not qualify as backdoors, perhaps because their existence is not secret or hidden in any way. But in the present Apple case where they are themselves using the word "backdoor," abusing their cryptographic single point of failure is precisely what the FBI is demanding.

Todd Weaver, founder & CEO of [**Purism**](https://puri.sm/about/), says the focus of the case avoided "[the larger issue of control](https://archive.is/rlJOX#selection-403.2-403.37)."

> You don’t actually own your phone. If we truly owned our phones, court ordered warrants would be served directly to the owner of the phone. The warrants in the case of Apple v FBI were served to Apple, who actually has control of your phone.

![Purism quote](https://pbs.twimg.com/media/CiVEcevWwAAciWh.jpg)

> ... If Apple loses this legal battle, all phones, tablets, and computing devices that are under the control of a company are then legally bound to comply with a warrant to give up the key that controls your device. If Apple, or any organization, controls your device, you are giving your legal rights over to that organization.

Apple is being pursued because contrary to their commendable implimentation of 'strong encryption,' they retain the ability to backdoor their products, not only through allowing the use of PINs but because they are a centralized point of failure in regards to building proprietary firmware & software.

> "If Apple gets to call #FBiOS a 'backdoor,' I suggest we refer to 'Apple updates' as 'official backdoor only good guys are allowed to use.'" --*Pwn All The Things* [@pwnallthethings](https://twitter.com/pwnallthethings/status/702974661211119617)

`Note: iPhones can be set to manual (requires user authentication, ie. passcode) or auto-update. During the update process, iPhone updates are individually signed per-device on Apple's servers, which would prevent an attacker from downgrading to an insecure version.`

However, there can also be security *benefits* from Apple's proprietary approach -- assuming that Apple remains trustworthy. **Mashable**'s Senior Tech Correspondent [Christina Warren](https://web.archive.org/web/20160417010513/http://mashable.com/people/christina/) wrote a detailed article [outlining iPhone security and encryption features](https://web.archive.org/web/20160417002919/http://mashable.com/2016/04/16/apple-security-explained/?utm_cid=hp-hh-pri#ad9rY8H4qgqE).

> And it's here where Apple has an inarguable advantage, especially when compared to other phone makers and operating system makers.

> Apple controls the whole stack, including updates, which means that it can push out updates and bug fixes very quickly.

> This is not how the rest of the mobile industry works. Consider the situation with Stagefright, an Android vulnerability disclosed last year. Even though Google was very quick to patch the exploit, it took considerable time for those updates to get down the chain to non-Nexus devices. Millions of devices will never get an update against that vulnerability.

Consider [this point](https://theintercept.com/2016/02/26/fbi-vs-apple-post-crypto-wars/) made by [Dan Froomkin](https://theintercept.com/staff/dan-froomkin/) & [Jenna McLaughlin](https://theintercept.com/staff/jennamclaughlin/)  of **The Intercept**:

> You might say we’re entering the Post-Crypto phase of the Crypto Wars.

> Think about it: The more we learn about the FBI’s demand that Apple help it hack into a password-protected iPhone, the more it looks like part of a concerted, long-term effort by the government to find new ways *around* unbreakable encryption — rather than try to break it. [*emphasis added*]

The [**Electronic Frontier Foundation**](https://www.eff.org/about) published a few pieces on this case and offered only passing criticism of Apple on this point, even though they included passages like this:

> **Would it be easy for Apple to sign the requested cracking software?** The answer any trained security engineer will give you is "it shouldn't be."

> ... There are pros and cons to this approach, but Apple considers this signing key among the crown jewels of the entire company. There is no good revocation strategy if this key is leaked, since its corresponding verification key is hard-coded into hundreds of millions of devices around the world.

It shouldn't be easy, but it's still possible. Disabling security features in so many devices also shouldn't be easy, but it's possible and, considering Apple's response, a very real problem.

Ray Dillinger framed the FBI's court order in a rather interesting way: [as a dramatic & unfriendly bug report](https://web.archive.org/web/20160224005522/http://www.metzdowd.com/pipermail/cryptography/2016-February/028269.html).

![FBI court order as a bug report](https://pbs.twimg.com/media/Cb6-D-eXIAAA1MW.png)

Taking all of this into consideration:
+ **Was Apple being asked to "create" a "backdoor"?** Unless you consider Apple creating a custom iOS, signed with their special software key, to be outside the bounds of 'normal' in terms of software authentication powers they *already* possessed, the answer is no. Remember that Apple *could use this capability at any time*, regardless of whether it's compelled or not. If you interpret 'normal' authentication to *not* include Apple's abilities and consider that 1) Apple disabling security features in their OS is an out-of-the-ordinary procedure for them & 2) though now weakly grounded, most Apple customers did have an expectation of confidentiality... then it could be argued that this was "creating a backdoor." I think that, *whether or not this was a backdoor, a further distinction should be made on whether they were going to be 'using' one or 'creating' one -- as such a fact is very important to Apple feeling enough pressure to increase iPhone security*. You can read Jonathan Ździarski's "[*Three-Prong Backdoor Test*](http://www.zdziarski.com/blog/?p=5785)" (read the formal explanation [here](http://www.zdziarski.com/blog/wp-content/uploads/2016/05/Backdoors-A-Technical-Definition.pdf)), [EFF's thought-piece on the historical definition of backdoors](https://www.eff.org/deeplinks/2016/03/thinking-about-term-backdoor) or [another argument on this from the technical perspective by Brandon Edwards](https://medium.com/@drraid/it-s-a-backdoor-100-2460bf7f8010#.l5nwz4405) (note that I did not make my argument depend on it being limited to one device, which this article focused on & disputed).

> A **backdoor** is a component of a security mechanism, in which the component is active on a computer system without consent of the computer’s owner, performs functions that subvert purposes disclosed to the computer’s owner, and is under the control of an undisclosed actor.

+ **Was Apple being ordered to "break encryption"?** Again, this still depends on your interpretation of the previous question. The encryption system of the iOS 9 itself was not being broken; security features dealing with how authentication is proven were. [Brute-force attacks](https://www.techopedia.com/definition/18091/brute-force-attack) are a hack of security vulnerabilities, not an encryption backdoor.

Therefore, it would be rather more accurate to say the FBI was demanding that Apple *take advantage of system security vulnerabilities which already existed.* 

## What are the technical & legal concerns involved?
#### Technical Concerns

It is now known that Apple has the ability to backdoor their own products & could be compelled to use that backdoor.

##### --- What are the limits to the use of FBiOS? --

Initially some security experts argued that this backdoor wouldn't work on iPhones newer than 5C 
due to the **Secure Enclave** firmware, [a co-processor of many independently-functioning kernels within the A7 64-bit system chip which stores keys in supposedly tamper-resistant hardware & also uses secure boot to ensure that all software installed on the OS is signed by Apple](https://web.archive.org/web/20150124040556/http://www.macrumors.com/2014/02/26/touch-id-secure-enclave-document) 
(remember authentication from earlier). On February 19th, a “senior Apple executive” told journalists at **Motherboard**, [**The Guardian**](https://twitter.com/dannyyadron/status/700830922585743360) and others that this was not true – the FBiOS "[would be effective on every type of iPhone currently being sold](https://web.archive.org/web/20160221092412/http://motherboard.vice.com/read/apple-the-exploit-the-fbi-is-asking-for-would-work-on-all-iphones)."

![Motherboard, Secure Enclave](https://pbs.twimg.com/media/CbnuF7iVIAE0A76.jpg)

Apple included this warning in an [FAQ for customers](https://web.archive.org/web/20160222150037/https://www.apple.com/customer-letter/answers/):

> Law enforcement agents around the country have already said they have hundreds of iPhones they want Apple to unlock if the FBI wins this case. In the physical world, it would be the equivalent of a master key, capable of opening hundreds of millions of locks. Of course, Apple would do our best to protect that key, but in a world where all of our data is under constant threat, it would be relentlessly attacked by hackers and cybercriminals. As recent attacks on the IRS systems and countless other data breaches have shown, no one is immune to cyberattacks.

"Hundreds of millions of locks." This would have applied to most, if not all, of their customer base.

This detail is very important, if true, because many tech journalists (including from **Ars Technica**) also speculated that [FBiOS wouldn't even work on other 5C iPhones](https://web.archive.org/web/20160219203100/http://arstechnica.com/apple/2016/02/encryption-isnt-at-stake-the-fbi-knows-apple-already-has-the-desired-key/) because, since the FBI allowed that the custom software could have been tied specifically to the phone's unique identifier, it should be limited to this *one* device. 

![FBiOS working on older phones](https://pbs.twimg.com/media/Cbl8EghUkAA5vMr.jpg)

A description of the Unique Identifier (UID) can be found on page 59 of [Apple's iOS Security Whitepaper](https://www.apple.com/business/docs/iOS_Security_Guide.pdf):

> A 256-bit AES key that’s burned into each processor at manufacture. It cannot be read by firmware or software, and is used only by the processor’s hardware AES engine. To obtain the actual key, an attacker would have to mount a highly sophisticated and expensive physical attack against the processor’s silicon. The UID is not related to any other identifier on the device 
including, but not limited to, the UDID.

Because the UID is "baked into its hardware," **Ars Technica** editor [Peter Bright](https://web.archive.org/web/20160216072035/http://arstechnica.com/author/peter-bright/) said that this request made the assumption that the UID could be extracted, which appears to be a difficult process.

Difficulty of extraction aside, he did offer that it *might* be possible to swap identifiers to apply to other 5C phones. 

![FBiOS tied to unique identifier](https://pbs.twimg.com/media/Cbl9ajvUcAAgJPV.jpg:large)

Therefore, Apple may not only have admitted that Secure Enclave is not secure enough but that it would be possible to swap identifiers in this custom OS. This probably had something to do with the fact that Apple could force an update to Secure Enclave without wiping the data.

**EFF**'s [Joseph Bonneu](https://www.eff.org/about/staff/joseph-bonneau) said the following in relation to [whether Secure Enclave protects newer phones](https://www.eff.org/deeplinks/2016/02/technical-perspective-apple-iphone-case):

> (Older devices that lack the secure enclave also apply a similar delay, but apparently do so from within the operating system.) It's possible, though not completely clear from Apple's documentation, that a software update would be able to modify this behavior; if not, this would completely prevent Apple from enabling faster passcode guessing on newer devices.

> There has been further speculation that the secure enclave could refuse to accept any software update (even one signed by Apple) unless unlocked by entering the passcode, or alternately, that a software update on a locked phone would erase all of the cryptographic keys, effectively making the phone's storage unreadable. Apple's security documentation makes no such guarantees, though, and there are indications that this isn't the case. So special cracking tools from Apple could potentially still modify the secure enclave's behavior to remove both the 10-guess limit and the delays between guesses.

This means that, if leaked, *FBiOS could have been used on any iPhone*.

##### --- Could a secure password protect against FBiOS? --

What was also not confirmed by Apple was whether a strong password (not a PIN) remains a safeguard against this attack. Against a brute-force attack, a long & complex password should work under normal circumstances 
(taking months to many years to break). [Micah Lee](https://theintercept.com/staff/micah-lee/), a technologist at the **The Intercept**, [said it would](https://theintercept.com/2016/02/18/passcodes-that-can-defeat-fbi-ios-backdoor/):

> It’s true that ordering Apple to develop the backdoor will fundamentally undermine iPhone security, as Cook and other digital security advocates have argued. But it’s possible for individual iPhone users to protect themselves from government snooping by setting strong passcodes on their phones — passcodes the FBI would not be able to unlock even if it gets its iPhone backdoor.

> ...The short version: If you’re worried about governments trying to access your phone, set your iPhone up with a random, 11-digit numeric passcode.


Note that he advises even an 11-digit *numeric* (numbers only) passcode would be sufficient, though alphanumeric (numbers, characters, and symbols) is stronger because it increases the amount of possible combinations. With a "truly random" 11-digit passcode, it would have taken *an average of 127 years* to crack even with FBiOS (note: the following graphs are *maximum* time estimates, not averages).

![passcode breaking time numeric](https://d262ilb51hltx0.cloudfront.net/max/800/1*QSjgF6fnfID7N-W9Ug4fcg.png)

![passcode breaking time alphanumeric](https://d262ilb51hltx0.cloudfront.net/max/800/1*eENjTSHmHIExFrf9k1E-tw.png)

Drawing from [page 12 of Apple's iOS Security White Paper (iOS 9.0 or later)](https://www.apple.com/business/docs/iOS_Security_Guide.pdf), this is due to limitations on how the brute-force attack can be performed:

> The passcode is entangled with the device’s UID, so brute-force attempts must be performed on the device under attack. A large iteration count is used to make each attempt slower. The iteration count is calibrated so that one attempt takes approximately 80 milliseconds. This means it would take more than 5½ years to try all combinations of a six-character alphanumeric passcode with lowercase letters and numbers.


However, these figures only apply if Secure Enclave or another aspect of the iPhone's security architecture wasn't also being breached as well, such as the "Effaceable Storage" processor (contains the CPU, BootROM, RAM, crypto engines, Apple's public signing key, and the UID key). [Daniel Kahn Gillmor](https://www.aclu.org/bio/daniel-kahn-gillmor), technologist for the ACLU, wrote a piece on [how you could bypass the auto-erase security feature on an iPhone 5C](https://web.archive.org/web/20160311005401/https://www.aclu.org/blog/free-future/one-fbis-major-claims-iphone-case-fraudulent), without destroying the data, by copying the flash memory of the file system key stored in this processor:

> The FBI can simply remove this chip from the circuit board (“desolder” it), connect it to a device capable of reading and writing NAND flash, and copy all of its data. It can then replace the chip, and start testing passcodes. If it turns out that the auto-erase feature is on, and the Effaceable Storage gets erased, they can remove the chip, copy the original information back in, and replace it. If they plan to do this many times, they can attach a “test socket” to the circuit board that makes it easy and fast to do this kind of chip swapping.

> If the FBI doesn't have the equipment or expertise to do this, they can hire any one of dozens of data recovery firms that specialize in information extraction from digital devices.

> NAND flash storage is an extremely common component. It's found in USB thumb drives, mobile phones, portable music players, low-end laptops—pretty much every portable device. Desoldering a chip from the circuitboard is straightforward enough that there are many clips on YouTube showing the practice, and reading and writing a bare NAND chip requires a minor investment in hardware and training that the FBI has probably already made.

**The Washington Post** claimed an anonymous FBI official told them that "[the bureau was aware of this method early on and concluded that it wouldn’t work, for technical reasons](https://www.washingtonpost.com/world/national-security/the-fbi-is-testing-a-code-based-way-to-get-into-the-san-bernardino-iphone/2016/03/24/bc79cd14-f1dc-11e5-a61f-e9c95c06edca_story.html)." However, as [the government has classified both the third-party and the "new method" they brought forth](https://web.archive.org/web/20160326033741/http://www.theguardian.com/technology/2016/mar/22/apple-fbi-san-bernardino-iphone-method-for-cracking), this comment may have been made just to deflect attention. 

> If the government decides to regularly use its password-bypassing technique in criminal trials, it risks making the method public every time defense attorneys and courts ask questions about how it is accessing information on a locked device. 

> The law does allow the government to present sensitive sources and methods under seal – out of the view of the public and, more importantly, Apple. But that protection isn’t a guarantee. And like any secret, the more people know, the less likely it is to stay secret.

> Apple attorneys said on Monday they would push the government to reveal the nature of their tactic if it is used at trial, though it is unclear what legal mechanism they would have to do so.

Ździarski, after consulting with other tech experts, believes [the FBI is most likely using this method](http://www.zdziarski.com/blog/?p=5966), a portion of which [he demonstrated himself](https://web.archive.org/web/20160328002531/https://twitter.com/JZdziarski/status/713877288060891136) [using a jailbreak](https://youtu.be/3xHm5lktvog).

> Using a NAND copying / mirroring technique, this barrier could be overcome in iOS 9, allowing the device to write and verify the attempt, but have that change later blown away by restoring an original copy of the chip. They wouldn’t have to copy the whole NAND in this case. If they can isolate the part of the chip that is written to (even though it’s encrypted), they can just keep writing over that portion of the chip. If the methods from iOS 8 were borrowed for this, then it could be partially automated by entering the pin through the USB, as well as using a light sensor to determine which pin successfully unlocked the device

He also says that "[with the info that experts have come forward with, I am reasonably confident FBI themselves, with current talent, could get into this phone](https://web.archive.org/web/20160311015818/https://twitter.com/JZdziarski/status/708100880353071105)."

With this in mind, a very valuable & proactive thing Apple could do is **recommend that their customers upgrade their passwords**, especially by moving away from numeric PINs to alphanumeric passwords (as the level of protection provided by each is different). iPhone device passwords on iOS9 can be changed through the following steps:

> Find the `Settings` icon. Scroll to the red `Touch ID & Passcode` option. You will be prompted to enter your current passcode. Once you have done so, scroll down to `Change Passcode` (under `Turn Passcode Off`). You will be prompted to enter a new passcode. Before entering anything, select `Passcode Options` and choose `Custom Alphanumeric Code`.

Until now Apple has given their customers a false sense of security, allowing them to use short passcodes & PINs. The last line of protection should be a strong password, which is under the user's control to change, not a security feature which can apparently be disabled.

#### Legal Concerns

##### --- What is the history behind Apple's compliance with law enforcement? --

To understand the legal history behind this case in terms of the US government ordering Apple to "unlock" iPhones, I recommend this clarifying article by **TechCrunch**'s [Matthew Panzarino](https://twitter.com/panzer): "[No, Apple Has Not Unlocked 70 iPhones For Law Enforcement](https://web.archive.org/web/20160220161959/http://techcrunch.com/2016/02/18/no-apple-has-not-unlocked-70-iphones-for-law-enforcement/)." The most important lines are about the difference between *decryption* and *extraction*:

> There are two cases involving data requests by the government which are happening at the moment. There is a case in New York [which] ...involves an iPhone running iOS 7. On devices running iOS 7 and previous, Apple actually has the capability to extract data, including (at various stages in its encryption march) contacts, photos, calls and iMessages without unlocking the phones. That last bit is key, because in the previous cases where Apple has complied with legitimate government requests for information, this is the method it has used.

> It has not unlocked these iPhones — it has extracted data that was accessible while they were still locked.

> The California case, in contrast, involves a device running iOS 9. The data that was previously accessible while a phone was locked ceased to be so as of the release of iOS 8, when Apple started securing it with encryption tied to the passcode, rather than the hardware ID of the device... So Apple is unable to extract any data including iMessages from the device because all of that data is encrypted.

In short: extraction allows them to access *unencrypted* data on iOS 7 or older; because they have [implimented passcode-based encryption in iPhones running iOS 8 or iOS 9](https://web.archive.org/web/20160222150037/https://www.apple.com/customer-letter/answers/), this data is no longer accessible through extraction. Therefore this request was different compared to Apple's history of compliance, which the government's arguments never acknowledged (in fact, they argued the opposite). [*Find citation for this claim*]


##### --- What are important factors in legal precedent(s) for the future? ---

Regardless of whether this specific piece of custom software would have been useable on other devices, Apple says that they were already getting similar requests to do so now that it has been shown they have the capability. This puts them in a position where they would either save FBiOS in the event of future cases, or safely destroy it & then be forced to spend more time/ resources recreating it in the future ([see pg 3](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)).

> The government says:  “Just this once” and “Just this phone.”  But the government knows those statements are not true; indeed the government has filed multiple other applications for similar orders, some of which are pending in other courts. And as news of this Court’s order broke last week, state and local officials publicly declared their intent to use the proposed operating system to open hundreds of other seized devices—in cases having nothing to do with terrorism.

> If this order is permitted to stand, it will only be a matter of days before some other prosecutor, in some other important case, before some other judge, seeks a similar order using this case as precedent.  Once the floodgates open, they cannot be closed, and the device security that Apple has worked so tirelessly to achieve will be unwound without so much as a congressional vote.


I saw over and over again the comment that the legal precedent(s) this case could have set carries more risk than the technical risk posed by FBiOS. FBI Director James Comey already [admitted that legal prescedent would be established with this case](http://www.c-span.org/video/?c4586153/comey-admits-iphone-backdoor-legal-precedent), as happens with all cases; therefore it should not have been cast aside as hypothetical hysteria. Since I am not a lawyer, I am not familiar with the specific statutes that were being considered, but here are some of the main points summarized:

+ This court order would have forced Apple to code a custom iOS which deliberately took advantage of security vulnerabilities in their authentication systems. If “code is speech," then speech (here in the form of code) can be compelled. While this was a different form of compelled speech, [compelled speech is not at all new](http://itlaw.wikia.com/wiki/Compelled_speech). It is still an open question of who exactly at Apple could have been compelled to do this, [whether anyone would have complied at all](https://web.archive.org/web/20160318151138/http://www.nytimes.com/2016/03/18/technology/apple-encryption-engineers-if-ordered-to-unlock-iphone-might-resist.html)...

> Apple employees are already discussing what they will do if ordered to help law enforcement authorities. Some say they may balk at the work, while others may even quit their high-paying jobs rather than undermine the security of the software they have already created, according to more than a half-dozen current and former Apple employees. Among those interviewed were Apple engineers who are involved in the development of mobile products and security, as well as former security engineers and executives.

> ... The fear of losing a paycheck may not have much of an impact on security engineers whose skills are in high demand. Indeed, hiring them could be a badge of honor among other tech companies that share Apple’s skepticism of the government’s intentions. “If someone attempts to force them to work on something that’s outside their personal values, they can expect to find a position that’s a better fit somewhere else,” said Window Snyder, the chief security officer at the start-up Fastly and a former senior product manager in Apple’s security and privacy division.

> Apple said in court filings last month that it would take from six to 10 engineers up to a month to meet the government’s demands. However, because Apple is so compartmentalized, the challenge of building what the company described as “GovtOS” would be substantially complicated if key employees refused to do the work.

...and whether prior precedent of "code is speech" applied, since the case of [*Bernstein vs. US Department of Justice*](https://www.eff.org/cases/bernstein-v-us-dept-justice) was about the *publication* of code (read [Park Higgins' EFF piece on "code is speech" related to 3-D printing](https://www.eff.org/deeplinks/2015/12/3-d-printing-case-code-speech-faces-new-challenges)). Before Apple had put forth a reply outlining how their defense would argue, at least one of [Apple's objections to the court order was projected to be on First Amendment grounds](https://web.archive.org/web/20160224033346/http://www.latimes.com/local/lanow/la-me-ln-apple-legal-argument-free-speech-20160223-story.html):

> In Apple's fight to knock down a court order requiring it to help FBI agents unlock a killer’s iPhone, the tech giant plans to argue that the judge in the case has overreached in her use of an obscure law and infringed on the company’s 1st Amendment rights, an Apple attorney said Tuesday.

> Theodore J. Boutrous -- one in a pair of marquee lawyers the technology company's has hired to wage its high-stakes legal battle -- outlined the arguments Apple plans when it responds to the court order this week.

> [...] “The government here is trying to use this statute from 1789 in a way that it has never been used before. They are seeking a court order to compel Apple to write new software, to compel speech," Boutrous said in a brief interview with The Times.

> Boutrous said courts have recognized that the writing of computer code is a form of expressive activity -- speech that is protected by the 1st Amendment.

This was confirmed in Apple's first motion against the FBI's court order on February 25th, in addition to objections on Fifth Amendment due-process grounds ([see pgs 32 & 34 respectively](https://web.archive.org/web/20160225205431/https://assets.documentcloud.org/documents/2722199/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)). It is important to note with regards to passwords that [biometric methods](https://web.archive.org/web/20160331142301/https://www.eff.org/issues/biometrics) (ie. the iPhone's [Touch ID fingerprint scanner](https://archive.is/q40Pd)), unlike character passwords, is a grey area currently treated as [not protected under the Fifth Amendment](https://archive.is/dilYn#selection-567.111-567.243) and can be legally compelled.

![Apple arguing on First Amendment grounds](https://pbs.twimg.com/media/CcFn9TwXIAQRy11.png:large)

However, Neil Richards, one of the law professors supporting Apple, said [furthering the precedent of "code is speech" may carry unwanted consequences](https://www.technologyreview.com/s/600916/apples-code-speech-mistake/):

> Where does this leave us, then, when we’re considering the regulation of code by the government? The right question to ask is whether the government’s regulation of a particular kind of code (just like regulations of spending, or speaking, or writing) threatens the values of free expression. Some regulations of code will undoubtedly implicate the First Amendment. Regulations of the expressive outputs of code, like the content of websites or video games, have already been recognized by the Supreme Court as justifying full First Amendment treatment. It’s also important to recognize that as we do more and more things with code, there will be more ways that the government can threaten dissent, art, self-government, and the pursuit of knowledge.

> But on the other hand, and critically, there are many things that humans will do with code that will have nothing to do with the First Amendment (e.g., launching denial of service attacks and writing computer viruses). Code = Speech is a fallacy because it would needlessly treat writing the code for a malicious virus as equivalent to writing an editorial in the New York Times. Similarly, if companies use algorithms to discriminate on the basis of race or sex, wrapping those algorithms with the same constitutional protection we give to political novels would needlessly complicate civil rights law in the digital age.

Another [counter-point](https://archive.is/wx8WV) from [David Golumbia](https://web.archive.org/web/20160324024013/http://www.uncomputing.org/?page_id=8) (Associate Professor at Virginia Commonwealth University) to the "code is speech" argument is that, while often containing elements of speech, code more aptly fits into the category of 'action' because it *executes*.

> This is most easily seen when we think about the main use to which code is put. The reason we have and pay so much attention to code is because it is *executed*. Execution is not primarily a form of communication, not even between humans and machines. Execution is the running of instructions: it is the direct carrying out of *actions*. It is adding together two numbers, or multiplying ten of them, or looping back to perform an operation again, or incrementing a value. This is what code does. Lots of code does not even look like language at all—it looks, if anything, like giant arrays of numbers that mean very little to anyone but the most highly-trained programmer. All of it executes, or at least can be executed. That is what it is for. That is what it does. That’s what makes it different from lots of other things, like most language and expressive media, all of whose *primary* function is to convey thoughts and ideas and feelings between persons.

The Department of Justice objected to Apple's First Amendment argument for the following reasons ([see pgs 32-34](https://web.archive.org/web/20160310233407/https://assets.documentcloud.org/documents/2755202/DOJ-Apple-20160310.pdf)):

> "...it does not involve a person being compelled to speak publicly, but a for-profit corporation being asked to modify commercial software that will be seen only by Apple." [pg 32 lines 13-15]

> "[T]hat [programming] occurs at some level through expression does not elevate all such conduct to the highest levels of First Amendment protection." [pg 32 lines 19-20]

> "To the extent Apple’s software includes expressive elements — such as variable names and comments — the Order permits Apple to express whatever it wants, so long as the software functions.. the Order’s 'broad requirements' do 'not dictate any specific message.'" [pgs 32-33 lines 24-1]

> "And even assuming, *arguendo*, that the Order compels speech-like programming, there is no audience: Apple’s code will be developed in the utmost secrecy and will never be seen outside the corporation." [pg 33 lines 3-5]

> "Apple will respond that if it modifies Farook’s iPhone to allow the government access to the phone, it “could be viewed as sending the message that [it] see[s] nothing wrong with [such access], when [it] do[es]... It is extremely unlikely that anyone could understand Apple to be expressing a message of hostility to 'data security and the privacy of citizens'..." [pg 34 lines 1-11]
 
Addressing the argument that Apple's "speech" would not be protected due to lack of audience, Apple argued that the presence of an audience has never been a requirement for protected speech ([see footnotes on pg 23](https://web.archive.org/web/20160315222842/https://assets.documentcloud.org/documents/2762120/Reply-Brief-in-Support-of-Apple-s-Motion-to-Vacate.pdf)):

![audience not necessary](https://pbs.twimg.com/media/CdoliafXEAAswZO.jpg:large)

+ US Congressman Ted Lieu (D-Los Angeles County), one of the Congressmembers who put forth [a bill for the ENCRYPT ACT](https://web.archive.org/web/20160222041054/https://lieu.house.gov/media-center/press-releases/congressmembers-lieu-farenthold-delbene-and-bishop-introduce-encrypt-act) ([full text here](https://web.archive.org/web/20160222040842/https://lieu.house.gov/sites/lieu.house.gov/files/documents/LIEU_027_xml%20%28ENCRYPT%20Act%20of%202016%29.pdf)), issued [this statement regarding the Apple court order](https://web.archive.org/web/20160219182200/https://lieu.house.gov/media-center/press-releases/congressman-lieu-statement-apple-court-order) on February 17th:

> "This court order also begs the question: Where does this kind of coercion stop?  Can the government force Facebook to create software that provides analytic data on who is likely to be a criminal?  Can the government force Google to provide the names of all people who searched for the term ISIL?  Can the government force Amazon to write software that identifies who might be suspicious based on the books they ordered?"

+ If a telecommunications provider *can* be compelled to take advantage of a security flaw 
undermining encryption for its customers, then they *will* be compelled. This will put pressure on other businesses 
to either comply or build their products so that they are not a centralized authority of proprietary software (a factor which, even with end-to-end encryption, will leave them [vulnerable to shutdowns as was the case with WhatsApp](https://archive.is/b8lMN)). Security technologist [Bruce Schneier](https://www.schneier.com/blog/about/) warned the precedent may motivate the government to [limit what sorts of security features tech companies can offer customers](https://www.washingtonpost.com/posteverything/wp/2016/02/18/why-you-should-side-with-apple-not-the-fbi-in-the-san-bernardino-iphone-case/) in order to maintain the ability to compel them. Though Apple has not released public plans to do so, [the "senior executives" have indicated they want to increase encryption implimentation in their products](https://web.archive.org/web/20160221193833/http://www.nytimes.com/2016/02/22/technology/apple-still-holds-the-keys-to-its-cloud-service-but-reluctantly.html):

![Apple might pursue iCloud encryption](https://pbs.twimg.com/media/CbyM7l1WAAAr5bb.png)

+ Other countries pay attention to the US on surveillance policy. Though Apple has not said they hold this fear, lawyers and security experts say this would create a threat to foreign customers & tech businesses as well. If the U.S. government can compel Apple to take advantage of a security vulnerability, why can't others? A recent example they cite is where FBI Director James Comey called for encryption backdoors & the Chinese government introduced new counter-terrorism laws a few weeks later.

From **Reuters**, "[Obama Sharply Criticizes China's Plans for New Technology Rules](https://web.archive.org/web/20160220205359/http://www.reuters.com/article/us-usa-obama-china-idUSKBN0LY2H520150302)":

> In an interview with Reuters, Obama said he was concerned about Beijing's plans for a far-reaching counterterrorism law 
> that would require technology firms to hand over encryption keys, the passcodes that help protect data, 
> and install security 'backdoors' in their systems to give Chinese authorities surveillance access.


Sounds oddly familiar, doesn't it?

> To be sure, Western governments, including in the United States and Britain, have for years requested tech firms to disclose encryption methods, with varying degrees of success.

> Officials including FBI director James Comey and National Security Agency (NSA) director Mike Rogers publicly warned Internet companies including Apple and Google late last year against using encryption that law enforcement cannot break.

> Beijing has argued the need to quickly ratchet up its cybersecurity measures in the wake of former NSA contractor Edward Snowden's revelations of sophisticated U.S. spying techniques.

![ACLU All Writs Act map](https://www.aclu.org/sites/default/files/styles/blog_main_wide_580x384/public/field_image/web16-blog-allwritsfinal-1160x768.jpg?itok=Rzs-DQ2g)

+ The use of the **All Writs Act** is not uncommon in surveillance cases -- in fact, the ACLU [mapped more than 63 cases of law enforcement using it to compel tech companies into helping them access customer data](https://web.archive.org/web/20160331173820/https://www.aclu.org/blog/speak-freely/map-shows-how-apple-fbi-fight-was-about-much-more-one-phone); the states with the most cases are California (16) and New York (12). Jonathan Mayer's "[*Assistance for Current Surveillance: The All Writs Act*"](https://youtu.be/PoNJvmB16bQ) explains the legality of its use. However its legitimacy in retrospective surveillance is being challenged. In response to President Obama's request for "moderation" in this debate, [Susan Crawford](https://twitter.com/scrawford), professor of law & public policy, explains how [**CALEA** (Communications Assistance for Law Enforcement Act)](https://t.co/j5bKCtuxhZ) will [limit the FBI's legitimacy in compelling Apple](https://backchannel.com/the-law-is-clear-the-fbi-cannot-make-apple-rewrite-its-os-9ae60c3bbc7b#.4g9f1z23l):

> The problem for the president is that when it comes to the specific battle going on right now between Apple and the FBI, the law is clear: twenty years ago, Congress passed a statute, the Communications Assistance for Law Enforcement Act (CALEA) that does not allow the government to tell manufacturers how to design or configure a phone or software used by that phone — including security software used by that phone.

> CALEA was the subject of intense negotiation — a deal, in other words. The government won an extensive, specific list of wiretapping assistance requirements in connection with digital communications. But in exchange, in Section 1002 of that act, the Feds gave up authority to “require any specific design of equipment, facilities, services, features or system configurations” from any phone manufacturer. The government can’t require companies that build phones to come to it for clearance in advance of launching a new device. Nor can the authorities ask a manufacturer to design something new — like a back door — once that device is out.

Judge James Orenstein, in another Apple iPhone-unlocking case from the Eastern District of New York, also disputed the use of AWA in regards to whether Apple could be considered 'close' to the crime ([see pgs 1, 29 31-32, & 40 respectively](https://web.archive.org/web/20160229224454/https://epic.org/amicus/crypto/apple/Orenstein-Order-Apple-iPhone-02292016.pdf)):

> "For the reasons set forth below, I conclude thatunder the circumstances of this case,the government has failed to establish either that the AWApermits the relief it seeks or that, even if such an order is authorized, the discretionary factors I must consider weigh in favor ofgranting the motion."

![All Writs Act constitutionality](https://pbs.twimg.com/media/CcausxZVAAIwS60.jpg:large)

![All Writs Act closeness to crime factor](https://pbs.twimg.com/media/CcawNGxUYAA-Ift.jpg:large)

![All Writs Act Apple public relations](https://pbs.twimg.com/media/Cca0YfiUkAA85oD.jpg:large)

+ It was highly unlikely that the FBI did not have alternative means to access the phone or its data in conjunction with the National Security Agency (NSA) or private data forensics companies, as they have a history of mutual cooperation. Legally, alternative means would have impacted the legitimacy of using the All Writs Act, as **EFF** explained: "[This point is potentially relevant legally, as cases interpreting the All Writs Act require '*an absence of alternative remedies*.' However, we lack firm evidence that the FBI has such a capability. Apple also probably doesn't want to argue that its phone is insecure so the authorities should just break into it some other way](https://www.eff.org/deeplinks/2016/02/technical-perspective-apple-iphone-case)." Now that they have cancelled the trial, despite their prior repeated assertions that unlocking the iPhone was only possible with Apple's assistance, many are wondering whether the FBI had prior knowledge of this capability and/or only changed course for strategic reasons, such as realizing their arguments were weak. This case was valuable in promoting the 'national security vs. encryption' false dichotomy so that public pressure may make it easier to compel companies under similar circumstances in the future. 

***
## How did the FBI access the iPhone & who helped them do it?
#### The Post-Case Investigation

> FBI [[Associate Deputy Director](https://web.archive.org/web/20160402202307/http://www.executivegov.com/2016/02/david-bowdich-named-fbi-associate-deputy-director/)] David Bowdich said in a statement Monday night [March 28th] that the agency "cannot comment on the technical steps that were taken to obtain the contents of the county-issued iPhone, nor the identity of the third party that came forward as a result of the publicity generated by the court order."

> "During the past week, to include the weekend, extensive testing of the iPhone was done by highly skilled personnel to ensure that the contents of the phone would remain intact once technical methods were applied. The full exploitation of the phone and follow-up investigative steps are continuing," Bowdich added. "My law enforcement partners and I made a commitment to the victims of the 12/2 attack in San Bernardino and to the American people that no stone would be left unturned in this case. We promised to explore every investigative avenue in order to learn whether the San Bernardino suspects were working with others, were targeting others, or whether or not they were supported by others."

> "While we continue to explore the contents of the iPhone and other evidence, these questions may not be fully resolved, but I am satisfied that we have access to more answers than we did before and that the investigative process is moving forward," he said. -- [**ABC News Radio**](https://web.archive.org/web/20160402200552/http://abcnewsradioonline.com/business-news/justice-department-withdraws-request-in-apple-iphone-encrypt.html)

More than a week after they claimed to have access to the iPhone, they still claimed to be analyzing it. Ździarski says this is [beyond the normal timespan in which incriminating content is discovered on iPhones](https://web.archive.org/web/20160406132931/https://twitter.com/JZdziarski/status/717695066563878914).

> “We’re now doing an analysis of that data, as we would in any other type of criminal terrorism investigation,’’ said [James Baker, the FBI’s general counsel](https://web.archive.org/web/20160325000306/http://hls.harvard.edu/faculty/directory/10035/Baker), on [Tuesday](https://web.archive.org/web/20160415162550/http://www.cultofmac.com/421679/fbi-its-too-early-to-tell-if-gunmans-iphone-contains-useful-evidence/?utm_campaign=fbi-its-too-early-to-tell-if-gunmans-iphone-contains-useful-evidence) [April 5th [at Global Privacy Summit 2016](https://archive.is/UO9ve), a [conference](https://web.archive.org/web/20160406131116/http://www.technobuffalo.com/2016/04/06/fbi-its-too-early-to-tell-if-shooters-iphone-contains-useful-data/) of the [**International Association of Privacy Professionals**](https://archive.is/Q5Ikr)]. “That means we would follow logical leads.” As a result, he says it’s “simply too early” to know whether the iPhone at the heart of the San Bernardino investigation is going to be useful.

After [more than two weeks of analyzing the iPhone's contents](https://archive.is/2RcDm#selection-793.0-801.38), the FBI had still not released any news of whether they found important evidence.

> A law enforcement source tells CBS News that so far nothing of real significance has been found on the San Bernardino terrorist's iPhone, which was unlocked by the FBI last month without the help of Apple.

> It was stressed that the FBI continues to analyze the information on the cellphone seized in the investigation, senior investigative producer [Pat Milton](https://archive.is/bkYwx) reports.

![FBI finds nothing on iPhone](https://pbs.twimg.com/media/CgbyxWoXEAASldt.jpg)

On April 19th, the FBI finally said that they had found nothing of importance on the iPhone: [no evidence of the use of encrypted communications, no evidence of contact with another plotter or anyone associated with ISIS, and even no evidence of contact with friends or family](https://web.archive.org/web/20160419225549/http://edition.cnn.com/2016/04/19/politics/san-bernadino-iphone-data/index.html). **CNN**, [**Daily Mail**](https://web.archive.org/web/20160419232545/http://www.dailymail.co.uk/news/article-3548419/FBI-says-haul-data-San-Bernardino-iPhone-helped-answer-key-remaining-questions-terrorist-couple.html), and **Associated Press** oddly treated this news as an important revelation of *new* data, even though it is a *lack* of data and apparently only comprised an 18-minute time period which was missing from the iCloud data they had already accessed.

> Hacking the San Bernardino terrorist's iPhone has produced data the FBI didn't have before and has helped the investigators answer some remaining questions in the ongoing probe, U.S. law enforcement officials say.

They claim the FBI is still analyzing the data. However the chances of finding anything significant has long passed.

The method used to access the iPhone is still the real mystery. "According to two people with direct contact," a team of **Cellebrite** engineers led by a hacker in Seattle managed to unlock/ access the phone, and "'everyone at the company has since been forced to sign non-disclosure agreements to remain silent about the matter.'" [John McAfee claimed](https://archive.is/ppC7F) to supposedly have knowledge of a specific contract from the summer of 2013 between **Cellebrite** and the FBI for a [mobile forensics device](https://archive.is/XpPva) called [the UFED Touch](https://archive.is/zRO7c). None of the publicly available contracts specifically mention UFED Touch (they describe the cateogry of devices, not names), so McAfee's evasiveness on divulging sources is odd considering his claim is entirely possible and could have reinforced his view of why the FBI went after Apple:

> Why would the FBI bother to get caught up in a battle with Apple if they already had a solution to unlock the iPhone? McAfee says the FBI was less interested in Apple than it was in precedent. If it won against Apple, then it could go to Google and get a master key into Android — which has 91% of the world market. A software master key — which costs nothing, can be given to every agent in the DOJ for free. The Cellebrite devices costs thousands of dollars per unit — way above the DOJ budget for everyday use.

Two anonymous law enforcement officials, "speaking on condition of anonymity, [told CNN the 'outside party' was not Cellebrite](https://archive.is/xxpeX)." National security reporters from **The Washington Post** also believe **Cellebrite**'s involvement is merely "widely rumored" based on statements (from more officials refusing to give their names) responding to "[the bureau [being] peppered with inquiries from state and local law enforcement officials seeking to know whether the solution might be useful for their cases](https://archive.is/CTUVA)," which they are hesitant to answer as they don't want tech companies to fix whatever vulnerability they're exploiting. Based on talking to "people familiar with the matter," they claim the third-party helpers were just "[professional hackers](https://archive.is/wYSfV)" who [discovered an iOS 9 zero-day flaw](https://web.archive.org/web/20160414002941/http://www.wired.com/2016/04/hacker-lexicon-white-hat-gray-hat-black-hat-hackers), with no mention of any company or group affiliation. The outlet continues to chide those who think it was most likely **Cellebrite** which, based on their lack of clear sourcing, is a rather bold move. It could easily be the case that both stories are correct, that the mastermind "professional hacker" was independently contracted by **Cellebrite** to aid their team of engineers, or vice versa that the FBI hired the hacker and then the **Cellebrite** team provided him with the tools purchased through the contract with the DOJ and FBI. Ździarski said that the FBI hiring a completely independent hacker would be "[inconsistent with Comey’s past statements of purchasing from a professional company with a reputation of protecting IP](https://web.archive.org/web/20160414214745/https://twitter.com/JZdziarski/status/720230162860797952)."

> ["The people we bought this from, I know a fair amount about them, and I have a high degree of confidence that they are very good at protecting it, and their motivations align with ours," he said.](https://web.archive.org/web/20160414214213/http://www.wdsu.com/money/fbi-director-we-bought-a-tool-to-hack-terrorists-iphone/38907756)

It would also bring up the question of why the "one-time fee" contract with the independent professional hacker was not made public through the [**Federal Procurement Data System** (FPDS)](https://www.fpds.gov/fpdsng_cms/index.php/en/) like the others. About six minutes into the first [Aspen Security Forum](https://archive.is/rjs9J) [London talk](https://archive.is/9JL8X) titled "The Complexities of Today's Security Challenges" on April 21st, Comey said that the amount the FBI spent to unlock the iPhone was "[more than I will make in the remainder of this job, which is seven years and four months, for sure"](https://archive.is/DAc9T#selection-827.1-827.101)." Based on calculating the sum from public records of his executive salary (around [$183,000](https://web.archive.org/web/20160304113950/https://www.opm.gov/policy-data-oversight/pay-leave/salaries-wages/salary-tables/pdf/2015/EX.pdf) annually, though it appears to increase to $185,100 for 2016), the cost must be at least $1.3 million ([see pg 6](https://web.archive.org/web/20160331005434/https://www.opm.gov/policy-data-oversight/pay-leave/salaries-wages/pay-executive-order-2016-adjustments-of-certain-rates-of-pay.pdf)). His talk is available through [**The Aspen Institute**](https://archive.is/6SKH8) on [YouTube](https://youtu.be/4S7IKTanuxw?t=6m43s). "Several U.S. government sources" told **Reuters** that the amount was less than $1 million; their most interesting claim however was that "[not even Comey knows who it is](https://archive.is/MkXNT#selection-1535.0-1535.126)," which would again contradict his earlier claim when he said he knew "a fair amount about them" & his more recent claim that [he had a "good sense" of the identity of the the third-party contractor](https://archive.is/E74ne#selection-1523.0-1523.122).

Other companies contracted during the pre-trial period for similar products and services include [**Black Bag Technologies**](https://archive.is/2LaUX) ([purchase orders](https://web.archive.org/web/20160401170105/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=Black+Bag+Technologies+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016&renderer=jsp&length=4) [from 2016](https://web.archive.org/web/20160401164038/https://www.fpds.gov/ezsearch/fpdsportal?indexName=awardfull&templateName=1.4.4&s=FPDSNG.COM&q=Black+Bag+Technologies+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016&x=0&y=0)), [**Magnet Forensics**](https://web.archive.org/web/20160322112023/https://www.magnetforensics.com/mobile-forensics/) ([purchase orders](https://web.archive.org/web/20160401170343/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=Magnet+Forensics+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+&renderer=jsp&length=4) [from 2016](https://web.archive.org/web/20160401163950/https://www.fpds.gov/ezsearch/fpdsportal?indexName=awardfull&templateName=1.4.4&s=FPDSNG.COM&q=Magnet+Forensics+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+&x=0&y=0)) and technical support from [**Novetta**](https://archive.is/JeDGq) ([purchase orders](https://web.archive.org/web/20160401175152/https://www.fpds.gov/ezsearch/fpdsportal?s=FPDSNG.COM&indexName=awardfull&templateName=PDF&q=Novetta+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+&renderer=jsp&length=4) [from 2016](https://web.archive.org/web/20160401175050/https://www.fpds.gov/ezsearch/fpdsportal?indexName=awardfull&templateName=1.4.4&s=FPDSNG.COM&q=Novetta+CONTRACTING_AGENCY_NAME%3A%22FEDERAL+BUREAU+OF+INVESTIGATION%22+2016+&x=13&y=10)).

![contracting Black Bag Tech](https://pbs.twimg.com/media/Ce5IUWuXEAAm-98.jpg:large)
![contracting Magnet Forensics](https://pbs.twimg.com/media/Ce5MbsgXEAQIO3J.jpg:large)
![contracting Novetta Inc.](https://pbs.twimg.com/media/Ce5Li04WsAAN2mJ.jpg:large)

Besides the NAND mirroring technique, another method possibily being used by the FBI is the "IP Box" tool, which "[latches onto a susceptible iPhone's power circuitry and enters PINs over USB](https://web.archive.org/web/20160408201333/http://appleinsider.com/articles/16/04/08/apple-says-it-wont-sue-fbi-to-find-out-how-san-bernardino-iphone-5c-was-hacked)."

> The so-called "IP Box" tested by security consultancy MDSec works by entering a PIN over USB, then immediately cutting power to the iOS device before the attempt is recorded. This has the effect of eliminating the 10-try limit, at the expense of significant time lost to iOS device reboots.

> MDSec places the time per attempt at nearly 40 seconds. While this long interval may seem likely to discourage brute force attempts in all but a few scenarios, research suggests that more than 25 percent of the population use one of 20 similar PINs, potentially cutting the mean time to crack a PIN down to minutes.

> Additionally, such tools are readily available over the internet, with some models costing as little as $175.

> As the firm notes, this appears to be an automated method to exploit a flaw described last November in CVE-2014-4451. Apple patched that bug in iOS 8.1.1, but older iOS versions remain vulnerable.

So unless the FBI's third-party helper found a new vulnerability in the software, this device wouldn't work on the San Bernardino iPhone.

The **Electronic Frontier Foundation** has [challenged the government](https://web.archive.org/web/20160329003018/https://www.eff.org/deeplinks/2016/03/fbi-breaks-iphone-and-we-have-some-questions) on its [policy for hiding vs. publicly disclosing security vulnerabilities in information technologies](https://web.archive.org/web/20160122155451/https://www.eff.org/sites/all/libraries/pdf.js/web/viewer.html?file=https%3A%2F%2Fwww.eff.org%2Ffiles%2F2016%2F01%2F18%2F37-3_vep_2016.pdf) ('*Vulnerabilities Equities Process*' or VEP), so they may be required to disclose the method in the near future. Amy Hess, the witness for the FBI at the Energy and Commerce encryption panel on April 19th, [told New York Times](https://archive.is/JG9Nx) they only "purchased the method from an outside party so that we could unlock the San Bernardino device... [but] did not, however, purchase the rights to technical details about how the method functions, or the nature and extent of any vulnerability upon which the method may rely in order to operate." The FBI may be trying to avoid that disclosure process by claiming they "[don’t have sufficient knowledge of the vulnerability to implicate the process](https://archive.is/6HhoN#selection-1499.163-1499.240)."

> The government’s decision simply to hire the locksmith and ignore how that lock was opened “creates a gap in the review process” that is “not transparent and has not been set in legislation,” [Denelle Dixon-Thayer, chief legal and business officer at Mozilla], [said](https://archive.is/DlUnV#selection-2169.0-2193.380).

> The F.B.I.’s carefully worded statement reveals that law enforcement authorities have found a loophole in the vulnerability review process created by the administration— hire the hacker to extract the data, but be careful to not know how he got the job done.

> “The F.B.I. is intentionally exploiting a known vulnerability and enabling people to profit off of it,” said Alex Rice, the chief technology officer at HackerOne, a security company in San Francisco that helps coordinate vulnerability disclosure for corporations. “The collateral damage done by this lack of transparency and the possible ongoing existence of the flaw is serious.”

Though if true, by claiming they know too little about the device the FBI would be admitting that they [recklessly ignored best practices in forensic science and "created an extremely dangerous situation for all of us."](https://archive.is/ccudn):

> Best practices in forensic science would dictate that any type of forensics instrument needs to be tested and validated. It must be accepted as forensically sound before it can be put to live evidence. Such a tool must yield predictable, repeatable results and an examiner must be able to explain its process in a court of law. Our court system expects this, and allows for tools (and examiners) to face numerous challenges based on the credibility of the tool, which can only be determined by a rigorous analysis. The FBI’s admission that they have such little knowledge about how the tool works is an admission of failure to evaluate the science behind the tool; it’s core functionality to have been evaluated in any meaningful way. Knowing how the tool managed to get into the device should be the bare minimum I would expect anyone to know before shelling out over a million dollars for a solution, especially one that was going to be used on high-profile evidence.

> A tool should not make changes to a device, and any changes should be documented and repeatable. There are several other variables to consider in such an effort, especially when imaging an iOS device. Apart from changes made directly by the tool (such as overwriting unallocated space, or portions of the file system journal), simply unlocking the device can cause the operating system to make a number of changes, start background tasks which could lead to destruction of data, or cause other changes unintentionally. Without knowing how the tool works, or what portions of the operating system it affects, what vulnerabilities are exploited, what the payload looks like, where the payload is written, what parts of the operating system are disabled by the tool, or a host of other important things – there is no way to effectively measure whether or not the tool is forensically sound. Simply running it against a dozen other devices to “see if it works” is not sufficient to evaluate a forensics tool – especially one that originated from a grey hat hacking group, potentially with very little actual in-house forensics expertise.

Nonetheless they have started to [inform members of Congress](https://web.archive.org/web/20160407041534/http://www.theverge.com/2016/4/6/11380204/fbi-iphone-attack-san-bernardino-secret), beginning with [Dianne Feinstein](https://archive.is/RhFH8) & [Richard Burr](https://archive.is/VcEj6):

> According to [a new report in **National Journal**](https://www.nationaljournal.com/s/622104), the FBI has already briefed [Senator Dianne Feinstein (D-CA)](https://web.archive.org/web/20160324090115/http://www.feinstein.senate.gov/public/index.cfm/biography) on the methods used to break into the iPhone at the center of Apple's recent legal fight. [Senator Richard Burr (R-NC)](https://web.archive.org/web/20160328020654/http://www.burr.senate.gov/about/biography) is also scheduled to be briefed on the topic in the days to come. Feinstein and Burr are both working on a new bill to limit the use of encryption in consumer technology, expected to be made public in the weeks to come.

`I can't access National Journal content as a non-subscriber. Here are screenshots from those who could.`

![FBI informs Congres 1](https://pbs.twimg.com/media/CfZKZRtWQAEgdj_.jpg)
![FBI informs Congress 2](https://pbs.twimg.com/media/CfYk1SvWQAIUJ7B.jpg)

From [**C|Net**](https://web.archive.org/web/20160407033429/http://www.cnet.com/news/fbi-spills-iphone-hacking-secret-to-senators/):

> The **National Journal** said both Feinstein and Burr believe Apple shouldn't be given information on how the FBI broke into the phone, which is an obvious stance given the bill they're planning to introduce as soon as this week. 

Feinstein, among a chorus of many politicians, called encryption "[the Achilles' heel in the internet](https://web.archive.org/web/20151126142114/http://www.cbsnews.com/news/face-the-nation-transcripts-november-22-feinstein-mccaul-mcgurk-paul/)" during a **Face The Nation** broadcast following the 2015 Brussels terror attack -- despite no evidence to suggest encryption played any role in the operation. ("...[Encryption is arguably closer to Achilles' shield than his heel](https://web.archive.org/web/20160407081821/http://www.cnet.com/news/trump-not-the-first-politician-to-say-dumb-things-about-the-net/)"). Burr, a Republican senator for North Carolina, recently [announced](https://archive.is/i7rmr) that he "look[ed] forward to working with Mr. [Donald] Trump." 

#### The Burr-Feinstein Encryption Bill

Through a staff leak it was revealed that both Feinstein and Burr are drafting a bill, titled the "[**Compliance with Court Orders Act of 2016**](https://www.scribd.com/doc/307378123/Burr-Encryption-Bill-Discussion-Draft)," which would require all companies to be able to give the government any communications data in an unencrypted format, effectively banning them from offering any encryption software to users for which that service does not possess a decryption key, particularly end-to-end. **The Intercept** said the senators "[told reporters they were still working on the draft and couldn’t comment on the language of an unfinished version](https://archive.is/fyT9e)." The draft was [officially released](https://web.archive.org/web/20160414221657/https://www.burr.senate.gov/imo/media/doc/BAG16460.pdf) on [April 13th](https://web.archive.org/web/20160414222731/https://www.burr.senate.gov/press/releases/intelligence-committee-leaders-release-discussion-draft-of-encryption-legislation-) and indirectly confirmed that the leaked draft from April 7th was authentic.

Interestingly, the term "backdoor" is not used even once in the document, even though that is exactly what would need to be implemented while at the same time trying to maintain any semblance of cybersecurity. The extent of those backdoors is potentially broad, to even [involve deleted or destroyed data](https://archive.is/PSJTo).

![Bill would affect deleted data & shredders](https://pbs.twimg.com/media/CfiGJFlUIAEtysk.jpg)

The section *Design Limitations* is especially misleading, as it doesn't take into account that many systems implement encryption as a fundamental design feature ([see lines 6-9 pg 4](https://web.archive.org/web/20160408173623/https://www.justsecurity.org/wp-content/uploads/2016/04/Burr-Feinstein-Encryption-Bill-Discussion-Draft-The-Hill.pdf)).

![Design limitations section](https://pbs.twimg.com/media/CfhCIFJUYAAcG29.jpg)

The entities affected by this legislation include "a device manufacturer, a software manufacturer, an electronic communication service, a remote computing service, a provider of wire or electronic communication service, a provider of a remote computing service, or any person who provides a product or method to facilitate a communication or the processing or storage of data" ([see lines 18-25 pg 6](https://web.archive.org/web/20160408173623/https://www.justsecurity.org/wp-content/uploads/2016/04/Burr-Feinstein-Encryption-Bill-Discussion-Draft-The-Hill.pdf)). According to tweets from [**The Hill**'s cybersecurity reporter Cory Bennett](https://archive.is/Qm79I), who uploaded the bill's draft, senators were still saying as of the bill's release on April 7th that they didn't know about the FBI briefing them on the iPhone hack, implying that Feinstein and Burr may be the only ones informed. 

From [**Softpedia**](https://web.archive.org/web/20160407230025/http://news.softpedia.com/news/fbi-discloses-method-to-hack-iphones-to-us-senators-502676.shtml):

> In case you’re wondering how come Feinstein is getting access to such information, she is the vice chairman of the Senate Select Committee on Intelligence and one of the senators who backed regulations that would force phone manufacturers to install backdoors for government access on devices sold in the United States.

> In addition to Feinstein, Senator Richard Burr also got access to similar information. He’s also one of the backers of pro-backdoor bills and together with Feinstein, took FBI’s side in the case against Apple, emphasizing that the agency shouldn’t tell Cupertino how it unlocked the San Bernardino iPhone.

> “I don't believe the government has any obligation to Apple. No company or individual is above the law, and I'm dismayed that anyone would refuse to help the government in a major terrorism investigation,” Feinstein was quoted as saying.

From [**Apple Insider**](https://web.archive.org/web/20160408201333/http://appleinsider.com/articles/16/04/08/apple-says-it-wont-sue-fbi-to-find-out-how-san-bernardino-iphone-5c-was-hacked):

> Saying that whatever method was used by the FBI will have a "short shelf life," Apple on Friday [April 8th] revealed it has no intention to sue the bureau in an effort to find out how it hacked the iPhone 5c used by a terrorist in California.

The majority of security experts have already come out against the bill. [Matt Blaze](https://archive.is/MKpjs), computer scientist director for [The Distributed Systems Laboratory](https://web.archive.org/web/20160114041419/http://www.cis.upenn.edu/~dsl/) at the University of Pennsylvania (also featured in the John Oliver's [**Last Week Tonight** episode](https://youtu.be/zsjZ2r9Ygzw?t=12m7s)), is calling it "worse than [the] Clipper [chip]," [which he is credited for breaking](https://web.archive.org/web/20160322113057/http://ciphermachines.com/clipper). [Matthew Green](https://archive.is/IGtBd), cryptographer and professor at [Johns Hopkins University](https://web.archive.org/web/20160310071440/http://spar.isi.jhu.edu/~mgreen/), said it "is pretty much as clueless and unworkable as I expected it would be." [Nate Cardozo](https://archive.is/8cR9j), [Senior Staff Attorney for **EFF**](https://web.archive.org/web/20160324062651/https://www.eff.org/about/staff/nate-cardozo), said it "would outlaw secure communications & storage, endanger security, & endanger US business. And it'd be [unconstitutional](https://web.archive.org/web/20160316192008/https://www.eff.org/deeplinks/2015/08/deep-dive-crypto-exceptional-access-mandates-effective-or-constitutional-pick-one)." 

![Bill would make many NSA activities illegal](https://pbs.twimg.com/media/CgGJixuUEAEdyS2.jpg:large)

According to **The Register**, security technologist [Bruce Schneier](https://web.archive.org/web/20160310102431/https://www.schneier.com/blog/about/) says the bill is currently so broad that it would even [outlaw file compression algorithms](https://archive.is/QTxfp#selection-1303.0-1303.512). 

> He pointed out that it isn't just cryptographic code that would be affected by this poorly written legislation. Schneier, like pretty much everyone, uses lossy compression algorithms to reduce the size of images for sending via email but – as it won't work in reverse and add back the data removed – this code could be banned by the law, too. Files that can't be decrypted on demand to their original state, and files that can't be decompressed back to their exact originals, all look the same to this draft law.

[Julian Sanchez](https://web.archive.org/web/20160402050218/http://www.juliansanchez.com/about/), a policy analyst and technology journalist for the **Cato Institute**, provided a lengthy explanation of basic browser operations that would be outlawed and require change by this bill, [notably session key generation for HTTPS connections](https://archive.is/ZuhYX#selection-5883.0-5883.1037).

The Obama Administration has [declined to publicly support or oppose the bill](https://web.archive.org/web/20160408031914/http://www.reuters.com/article/us-apple-encryption-legislation-idUSKCN0X32M4?feedType=RSS&feedName=technologyNews) yet, according to unnamed sources who spoke with **Reuters**.

> Although the White House has reviewed the text and offered feedback, it is expected to provide minimal public input, if any, the sources said.

> Its stance is partly a reflection of a political calculus that any encryption bill would be controversial and is unlikely to go far in a gridlocked Congress during an election year, sources said.

> A White House spokesman declined to comment on the pending legislation, but referred to White House press secretary Josh Earnest's statements on encryption legislation. Last month Earnest said the administration is "skeptical" of lawmakers' ability to resolve the encryption debate given their difficulty in tackling "simple things."

[Senator](https://archive.is/jefG6) [Wyden](https://archive.is/2QoAm) [announced](https://archive.is/5Z85x) his intention to [oppose the bill](https://web.archive.org/web/20160414203444/https://twitter.com/RonWyden/status/720343774099017728) in committee and filibuster it on the Senate floor if necessary.

![Senator Wyden responds to bill](https://pbs.twimg.com/media/CfifeBAWwAAq1Ho.jpg)
![Senator Wyden responds to bill 2](https://pbs.twimg.com/media/Cf8sycmVIAEtRh_.png:large)

He is also [one of five senators who introduced](https://archive.is/qnAj7) the [Stopping Mass Hacking (SMH) Act](https://web.archive.org/web/20160524222953/https://www.wyden.senate.gov/download/?id=959B9967-F666-404F-B2D5-2520586107C2&download=1) in opposition to proposed changes by the Department of Justice to Rule 41 of the Federal Rules of Criminal Procedure which governs search and seizure. The bill gained popularity due to its acronym utilizing the internet meme & slang term "smh" or 'Shaking My Head.' The changes would expand the powers of magistrate judges, where they "will now have the the authority to issue a warrant to remotely search [a] device" if they don't know its location and be able to issue warrants authorizing searches for an unlimited number of deviceds (including outside the U.S.). 

> The American public should understand that these changes won’t just affect criminals: computer security experts and civil liberties advocates say the amendments would also dramatically expand the government’s ability to hack the electronic devices of law-abiding Americans if their devices were affected by a computer attack. Devices will be subject to search if their owners were victims of a botnet attack — **so the government will be treating victims of hacking the same way they treat the perpetrators.**

One this is for sure: this is not over.

> [FBI Director James Comey said on Wednesday there will be more U.S. government litigation over accessing electronic devices and said encryption is "essential tradecraft" of terrorist groups, such as Islamic State.](https://archive.is/E74ne#selection-1477.1-1477.213) (Wednesday, May 11th)

#### Post-AppleVsFBI Encryption Panels & Committees

On the morning of April 13th, the senators held a staff briefing on "[barriers to law enforcement’s ability to lawfully access the electronic evidence they need to identify suspects, solve crimes, exonerate the innocent and protect communities from further crime.](https://web.archive.org/web/20160412103920/https://www.techdirt.com/articles/20160411/13460534154/burr-feinstein-plan-one-sided-briefing-law-enforcement-to-bitch-about-going-dark.shtml)" It was immediately noticed that not one person on the panel list is referred to as a technologist. The goal was most likely to gather support for their bill, and since it was officially released on that day, it seems the response from those present at the briefing was positive.

![panel list for briefing](https://pbs.twimg.com/media/CfyhC4LXIAQzMNH.jpg)

The panel was more varied in a [hearing](https://web.archive.org/web/20160415010122/https://energycommerce.house.gov/news-center/press-releases/witnesses-announced-energy-and-commerce-encryption-hearing) on Tuesday, April 19th, overseen by the House Committee on Energy and Commerce and titled "[Deciphering the Debate Over Encryption: Industry and Law Enforcement Perspectives](https://archive.is/wb0Xv)." The [witness list](https://web.archive.org/web/20160415010922/https://energycommerce.house.gov/hearings-and-votes/hearings/deciphering-debate-over-encryption-industry-and-law-enforcement) included security experts such as [Matt Blaze](https://github.com/Enegnei/AppleVsFBI/commit/90bbb11756f40fcd03accad481ea2d26c75b157f) and industry leaders like Apple's Senior Vice President [Bruce Sewell](https://github.com/Enegnei/AppleVsFBI/commit/37b17e115aa1fbb55aed1b042ffb35589f662e3e). The hearing was livestreamed and is [available on YouTube](https://youtu.be/lafj2EXHeqQ) (again, I also have a local .mp4 copy in case it is taken down). **TechCrunch** wrote [a brief summary](https://archive.is/kq48U) of key points in the proceedings. Here is a [list](https://archive.is/FiEUD) of witness statements from each panelist:
+ Tech Industry/ Security Experts -
  * [Dr. Matthew Blaze](https://web.archive.org/web/20160419192840/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-BlazeM-20160419.pdf) - Associate Professor for the University of Pennsylvania ([witness statement](https://web.archive.org/web/20160419194046/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-BlazeM-20160419-U3.pdf))
  * [Mr. Bruce Sewell](https://web.archive.org/web/20160419192948/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-SewellB-20160419.pdf) - General Counsel, Apple, Inc ([witness statement](https://web.archive.org/web/20160419194539/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-SewellB-20160419.pdf))
  * [Mr. Daniel Weitzner](https://web.archive.org/web/20160419193101/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-WeitznerD-20160419.pdf) - Research Scientist, MIT Comp Sci & Artificial Intelligence, Internet Policy ([witness statement](https://web.archive.org/web/20160419194659/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-WeitznerD-20160419.pdf))
  * [Mr. Amit Yoran](https://web.archive.org/web/20160419193234/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-YoranA-20160419.pdf) - President, RSA Security ([witness statement](https://web.archive.org/web/20160419194844/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-YoranA-20160419.pdf))
+ Government & Law Enforcement -
  * [Capt. Charles Cohen](https://web.archive.org/web/20160419193443/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-CohenC-20160419.pdf) - Office of Intelligence & Investigative Technologies, Indiana State Police ([witness statement](https://web.archive.org/web/20160419194143/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-CohenC-20160419.pdf))
  * [Chief Thomas Galati](https://web.archive.org/web/20160419193649/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-GalatiC-20160419.pdf) - Chief, Intelligence Bureau, New York City Police Department ([witness statement](https://web.archive.org/web/20160419194243/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-GalatiC-20160419-U1.pdf))
  * [Ms. Amy Hess](https://web.archive.org/web/20160419193751/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-HessA-20160419.pdf) - Executive Assistant Director for Science and Technology, FBI ([witness statement](https://web.archive.org/web/20160419194345/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-HessA-20160419.pdf))
  * [Mr. Ron Hickman](https://web.archive.org/web/20160419193851/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-TTF-HickmanR-20160419.pdf) - Sheriff, Harris County Sheriff's Office, National Sheriff's Association ([witness statement](https://web.archive.org/web/20160419194436/http://docs.house.gov/meetings/IF/IF02/20160419/104812/HHRG-114-IF02-Wstate-HickmanR-20160419.pdf))

On May 19th, the Media Law Resource Center and the Berkeley Center for Law & Technology jointly held an evening session as part of their two-day 2016 Digital Conference to discuss the Apple vs. FBI case, titled "[Crypto-Controversy: Beyond the San Bernardino iPhone Dispute](https://archive.is/soyYs)." An [audio podcast](https://twitter.com/MediaLawMLRC/status/733729668105424896) of the session(s) will be available about three weeks from the date they were filmed.

![moderator and panelists](https://pbs.twimg.com/media/Ci2y54CVEAAwuIQ.jpg)

***
##### Mirror Links:

+ [iOS Security Whitepaper (Sept 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/iOS_Security_Guide.pdf)
+ [Transcript of Argument from another Apple iPhone case in New York (Nov 27th 2015)](https://github.com/Enegnei/AppleVsFBI/blob/master/Transcript.Order-Requiring-Apple-Inc-to-Asisst-in-the.pdf)
+ [US Government Vulnerabilities Equities Policy & Process (Jan 14th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/37-3_vep_2016.pdf)
+ [Bill of ENCRYPT (Ensuring National Constitutional Rights for Your Private Telecommunications) Act (Feb 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/LIEU_ENCRYPT.Act.of.2016.pdf)
+ [Order Compelling Apple, Inc. to Assist Agents in Search (Feb 16th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SB-Shooter-Order-Compelling-Apple-Asst-iPhone.pdf)
+ [Government's *Ex Parte* Application For Order Compelling Apple Inc. To Assist (Feb 16th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/iphone-fbi-decrypt.pdf)
+ [Government's Motion to Compel Apple Inc. to Comply With This Court's Feb 16th Order (Feb 19th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Government-Motion-To-Compel-Apple-To-Comply.pdf)
+ [FBI Statement to Address Misleading Reports (Feb 20th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Statement-from-the-FBI-Feb-20-2016.pdf)
+ [Pew Survey: More Support for Justice Department Than for Apple in Dispute Over Unlocking iPhone (Feb 22nd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/2-22-2016-iPhone-release.pdf)
+ [Apple's Motion to Vacate Order Compelling Apple Inc. to Assist Agents in Search (Feb 25th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/5-15-MJ-00451-SP-USA-v-Black-Lexus-IS300.pdf)
+ [Judge Orenstein: In Re Order Requiring Apple, Inc. To Assist In The Execution Of A Search Warrant (Feb 29th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Orenstein-Order-Apple-iPhone-02292016.pdf)
+ [Statement by Apple Lawyer Bruce Sewell: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Testimony-of-Bruce-Sewell-March-1-2016.pdf)
+ [Statement by Professor Susan Landau: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/landau-written-testimony.pdf)
+ [Statement by NY Dist Att C.R. Vance, Jr.: US House of Representatives Committee on the Judiciary (Mar 1st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/vance-written-testimony.pdf)
+ [*Amici Curiae* Brief in Apple Case on Behalf of iPhone Security Experts and Applied Cryptographers (Mar 2nd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/CIS.Technologists.Apple.Brief.Final.pdf)
+ [Brief of *Amici Curiae* EFF & 46 Technologists, Researchers, and Cryptographers (Mar 3rd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/16cm10sp_eff_apple_v_fbi_amicus_court_stamped.pdf)
+ [Brief of *Amici Curiae* from 14 Internet Technology Companies (Mar 3rd 2016](https://github.com/Enegnei/AppleVsFBI/blob/master/smith_post.pdf)
+ [San Bernardino County District Attorney *Amici Curiae* in Support of the US Government (Mar 3rd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Gov-Uscourts-Cacd-640468-79-0.pdf)
+ [Government's Reply In Support of Motion to Compel & Opposition to Apple Inc.'s Motion (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/DOJ-Apple-20160310.pdf)
+ [Declaration of Tracy L. Wilkison In Support of Government's Reply: Exhibits 1-16 (Mar 10th 2016](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088014.pdf)
+ [Declaration of Stacey Perino In Support of Government's Reply: Exhibits 17-30 (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088016.pdf)
+ [Supplemental Declaration of Christopher Pluhar In Support of Government's Reply (Mar 10th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/031123088015.pdf)
+ [Apple Inc.'s Reply To Government's Opposition To Apple Inc.'s Motion (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Reply-Brief-in-Support-of-Apple-s-Motion-to-Vacate.pdf)
+ [Declaration of Robert Ferrini In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Ferrini-Declaration-Executed.pdf)
+ [Supplemental Declaration of Nicola T. Hanna In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Supp-Hanna-Decl-Executed.pdf)
+ [Supplemental Declaration of Erik Neuenschwander In Support of Apple Inc.'s Reply (Mar 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Supp-Neuenschwander-Decl-Executed.pdf)
+ [Government's *Ex Parte* Application For A Continuance (Mar 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/2016-03-21-Ex-Parte-Application-Dckt-191-0.pdf)
+ [Conference: Order Granting Government’s *Ex Parte* Application to Vacate Hearing (Mar 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/usg-apple-199.pdf)
+ [Order Granting Government’s *Ex Parte* Application to Vacate Hearing (Mar 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/usg-apple-191.pdf)
+ [The DOJ & FBI Contract Phone Data Extraction & Analysis Company Cellebrite (Mar 21st 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/SearchResults.pdf)
+ [Government's Status Report: Vacate Order Compelling Apple Inc. to Assist (Mar 28th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/FBI_apple_20160328.pdf)
+ [Government's Status Report: Order Vacating February 16 2016 Order (Mar 29th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/usg-apple-210.pdf)
+ [LEAKED - Burr-Feinstein Encryption Bill Discussion Draft: "Compliance with Court Orders Act of 2016" (Apr 7th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/Burr-Feinstein-Encryption-Bill-Discussion-Draft-The-Hill.pdf)
+ [Burr-Feinstein Encryption Bill Discussion Draft: "Compliance with Court Orders Act of 2016" (Apr 13th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/BAG16460.pdf)
+ [**NY Case:** Apple Inc.'s Memorandum of Law In Response to the Government's Brief (Apr 15th 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/FBI-Apple-EDNY-Apple-Response-04152016.pdf)
+ [**NY Case:** In re Order Requiring Apple Inc. to Assist in the Execution of a Search Warrant (Apr 22nd 2016)](https://github.com/Enegnei/AppleVsFBI/blob/master/123111836100.pdf)

by: **@J9Roem**, keybase.io/j9roem --
Donations appreciated: `1PytMk24QZB147N9oW1jA6AhAoSsyqLhkB`
