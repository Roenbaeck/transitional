What needs to be agreed upon

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


June 17, 2019
If we are to have a discussion about something there are a few things we first need to agree upon in order to communicate efficiently and intelligibly. A good way to test for what we need is to transcribe a discussion between two individuals and afterwards hand this over to a third non-participating individual, who should be able to unambiguously interpret the transcription.

Let's say one of the individuals in the discussion frequently talks about 'Jennifer', while the other uses 'Jen'. In order to avoid possible confusion, it should be agreed upon that 'Jen' and 'Jennifer' is the same person. This can be done by the introduction of a unique identifier, say 'J42', such that the transcript may read "I talked to Jen (J42) today." and "Oh, how is Jennifer (J42) doing?". We need to agree upon the identities of the things we talk about.

Assuming the respose is "Jen (J42) is doing good." followed by "I figured as much, new boyfriend and all, so Jennifer (J42) must be good.". In this case 'good' is a value that should mean the same thing to both individuals. However, 'good' is not scientifically precise, but there is a consensus and familiarity with the value that let's us assume that both parties have sufficiently equal definitions to understand each other. Imprecisions that would lead to confusion could of course be sorted out in the discussion itself. If "Jen (J42) is doing so so.", then "What do you mean 'so so', is something the matter?" is a natural response. We need to agree upon values, and that any imprecisions lie within the margin of error with respect to the mutual understanding of their definitions.

Now, if the transcription needs to be done efficiently, leaving out the nuances of natural language, that challenge can be used to test whether or not the two constructs above can capture the essence of any discussion. Using identities and values we can construct pairs, like (J42, Jen), (J42, Jennifer), (J42, good). Forget that you've heard anything and put yourself in the shoes of the third party. Apparently, something is missing. There is no way to tell what 'Jen', 'Jennifer', and 'good' are with respect to the thing having the identitiy J42. This can be sorted out by adding the notion of a role that an identity takes on with respect to a value. Using roles, the pairs become triples (J42, nickname, Jen), (J42, first name, Jennifer), and (J42, mood, good). We need to agree upon the roles that identities take on with respect to values.

Surely this is enough? Well, not quite, unless Jen is permanently in a good mood. The triple (J42, mood, good) is not temporally determined, so how could we tell when it applies? The third party may be reading the transcript years later, or Jen may even have broken up with her boyfriend before the discussion took place, unbeknownst to the two individuals talking about her. Using a temporal determinator, interpretable as 'since when', the triples can be extended to quadruples (J42, nickname, Jen, 1988), (J42, first name, Jennifer, 1980-02-13), and (J42, mood, good, 9.45 on Thursday morning the 20th of August 2019). The way the point in time is expressed seems to differ in precision in these quadruples. Actually, there is no way to be perfectly precise when it comes to expressing time, due to the nature of time and our way to measure it. It's not known exactly when Jennifer got her nickname Jen, but it was sometime in 1988. We need to agree upon the points in time when identities took or will take on certain roles with respect to certain values, to some degree of precision.

This is almost all we need, except that the quadruple can only express properties of an individual. What about relationships? Let B43 be the identitiy of Jen's boyfriend. We may be led to use a quadruple (J42, boyfriend, B43, 2019), but this has some issues. First, B43 is in the third position, where a value is supposed to be, not an identity. If we can overlook this, the second issue is more severe. Can we really tell if B43 is the boyfriend of J42 or if J42 is the boyfriend of B43? The way we introduced the role, as something an identity takes on with respect to a value, the latter alternative is the natural interpretation. Finally, the nail in the coffin, relationsships may involve more than two identities. Where in the quadruple would you put the third party?

The solution is to return to a triple, but where the first position contains a set of ordered pairs ({(J42, girlfriend), (B43, boyfriend)}, official, 2019). This resolves the issue of who is the boyfriend and who is the girlfriend. The second position is again a value and the third is the temporal determinator. Looking back, we can actually consolidate the quadruple used to express properties to a triple as well ({(J42, nickname)}, Jen, 1988). The only difference being that the cardinality of the set is one for properties and more than one for relationships. Triples like these are called posits in #transitional modeling.

We could leave it here and be able to represent a whole lot of information this way. But, let us return to the three individuals we have been talking about. Now that the transcript is in place, consisting of a number of posits, what if they cannot agree upon it being the single version of the truth? What if some of what was written down is not 100% certain? What if someone is of an opposite opinion? This sounds like important information, and it can actually easily be transcribed as well, but it requires another construct, the assertion. This will be the topic of the next article; "What can be disagreed upon".

---

What can be disagreed upon

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


June 17, 2019
This is a continuation of the article entitled "What must be agreed upon", in which two individuals have a discussion, whereafter a transcript appears that a third party is invited to interpret. The transcript consists of a number of posits, for example ({(J42, girlfriend), (B43, boyfriend)}, official, 2019) and ({(J42, nickname)}, Jen, 1988). The syntax of a posit is described as a triple, where the first position is occupied by a set of ordered pairs, each pair being an identity and a role. The set is followed by a value and time point, which both may be imprecise in nature. What must be agreed upon is the syntax of the posit and the semantics of what it expresses. That sums up the conclusions of the earlier article.

Given the title of this article, let us follow up by investigating disagreements, and here comes an important distinction. Even if you understand what a posit is saying, it doesn't imply that you believe in what the posit is saying. Many different opinions are certainly held towards a statement such as "We are alone in the universe". So, if we want to talk about posits in the language of #transitional modeling, the posit itself must be given an identity. To talk about ({(J42, girlfriend), (B43, boyfriend)}, official, 2019) we give it the identity P1 and ({(J42, nickname)}, Jen, 1988) will be P2. The identities make it possible to create new posits that talk about other posits; meta-posits if you like.

If posits that talk about other posits live alongside posits that talk about other things, we cannot allow for any confusion with respect to the roles. We will therefore reserve roles for our purposes, say the strings 'posit' and 'determines confidence'. An assertion is a posit exemplified by ({(P1, posit), (J42, determines confidence)}, 0.8, 2019-04-05). The interpretation is that Jennifer (J42), since 2019-04-05, expresses a confidence of 0.8 with respect to if her girlfriend/boyfriend status with B43 was official since 2019 (P1). Similarly ({(P1, posit), (B43, determines confidence)}, -1, 2019-04-05). We will see that those confidence numbers reveal a big conflict!

Confidences, at lease those found in our assertions, fall within the [-1, 1] interval. The mapping between how something is expressed in natural language and the numerical confidence is fuzzy. But, let us assume that 0.8 corresponds to "very likely". Then Jennifer is saying that it is very likely that B43 officially became her boyfriend in 2019. The twist in the plot is that the boyfriend is of a very different opinion. On the negative scale of confidences, certainty towards the opposite is expressed, and -1 is "completely certain of the opposite". More precisely, this is equivalent to being completely certain of the complement of a value. In other words, the boyfriend is completely certain, with confidence value 1, of the posit ({(J42, girlfriend), (B43, boyfriend)}, anything but official, 2019).

Tucked in between is a confidence of 0, which we call "complete uncertainty". Let us assume that the boyfriend is clueless, and instead asserted ({(P1, posit), (B43, determines confidence)}, 0, 2019-04-05). This is interpreted as the boyfriend having no clue whatsoever if P1 is a truthful posit or not. Perhaps memory is failing or the boyfriend chose to forget. Assertions with confidence give us a powerful machinery to express differences of opinon. To recap, confidence 1 means certain of one particular value, -1 certain it's a value different from one particular value, and 0 that it could be any value whatsoever. Values in between express confidence to a given degree.

The first article mentioned the unlikeliness of Jennifer eternally being in a good mood. There will come a time when her mood is different. Likely when she finds out what her boyfriend is asserting. At that point, maybe the recollection of her boyfriend is better, and he changes his mind. Circumstances definitely change over time, but we haven't yet seen change in action. This will be the topic of the next article, entitled "What will change and what will remain".

The observant reader will notice that assertions here are slightly different from in the paper "Modeling conflicting, uncertain, and varying information". There the assertion is an actual construct, a predicate, different from the posit. Here the assertion is a meta-posit built around a semantical reservation. The reasoning behind the different approach is that if assertions are expressed as posits, they can be talked about as well using another layer of posits; a kind of über-meta-posits.

---

What will change and what will remain

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


June 18, 2019
This is a continuation of the two articles "What needs to be agreed upon" and "What can be disagreed upon", in which two people have a discussion, after which a third party is invited to interpret a transcription of it. We have concluded that if the meaning of a posit is universally agreed upon, anyone is nevertheless at liberty to disagree or express doubt towards what it is saying. Opinions about posits are recorded in the transcript itself using assertions, a kind of meta-posit that assigns someone's confidence level with respect to a posit.

Change is everywhere, and the last article concluded that both the circumstances that posits and assertions describe may change over time. Values change and opinions change. Let us make the transcript a living document, required to capture such changes. Additionally, the transcript much be historically complete, capturing the changes in a non-destructive manner. Anything that goes into the transcript is written in stone.

Grab your chisel, because Jennifer broke up with her boyfriend. Recall that the posit P1 is ({(J42, girlfriend), (B43, boyfriend)}, official, 2019), where J42 is Jennifer and B43 her boyfriend. The posit P3 tells us what happened in 2020 and it looks like this ({(J42, girlfriend), (B43, boyfriend)}, broken up, 2020). Remember the posit P2? It is ({(J42, nickname)}, Jen, 1988). Clearly, they are all different posits, P1 ≠ P2 ≠ P3, but P1 and P3 must share something in order for them to be describing a change that they do not share with P2.

It is actually possible to precisely define change. When two posits share the same set in their first position, but have different values and one time point follows the other, they describe a change. With that in place, P3 is obviously a change from P1. Since the set in P2 differs from that in P1 and P2, it is not a change of either P1 or P3. In #transitional modeling, the set is called a dereferencing set. They remain, indefinitely, while their surroundings may change entirely. Even after J42 is gone, the dereferencing sets in which that identity is found will remain, because we can, of course, have a recollection of things that are no more.

Then how does change affect assertions? Since assertions are posits themselves it works in exactly the same way. Jennifer made the following assertion on the 5th of April in 2019 ({(P1, posit), (J42, determines confidence)}, 0.8, 2019-04-05), stating that it is very likely that she and her boyfriend officially has been an item since 2019. After learning that her "boyfriend" thought otherwise, she changed her mind. Let's say that they had a serious talk about this on the 21st of September 2019. Jennifer's revised confidence in P1 can then be expressed through another assertion ({(P1, posit), (J42, determines confidence)}, 0, 2019-09-21). This assertion changes her previous confidence level from 0.8 to 0, so after the 21st she has no clue if they actually were an item or not.

Incidentally, this is how a 'logical delete' works in a bitemporal database. Albeit, in those databases there are only two confidence values, 1 (recorded) and 0 (deleted). The database itself is also the only one allowed to have an opinion. In other words, the functionality of a bitemporal database can be described as a small subset of #transitional modeling. When confidences are extended to the continuous interval [0, 1], the functionality approaches that of probabalistic databases. If further extended to include negative confidence, [-1, 1], we approach uncertainty theory, yet to be explored in databases. The fact that anyone may have an opinion is similar to multi-tenant databases. Transitional modeling as a formal base is very powerful, despite it's simple construction.

Back in the shoes of the third party reading the transcript, we find the posit P4 as ({(S44, nickname)}, Jen, 1988). So, wait, what? There were in fact two different Jens after all, J42 and S44? What exactly is the thing with identity S44? This will be the topic of the next article, entitled "What we are".

---

What we are

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


June 18, 2019
This is a continuation of the articles "What needs to be agreed upon", "What can be disagreed upon", and "What will change and what will remain". So far we have learnt to build posits and assert these, in order to create an exhaustive transcript of a discussion. Furthermore, the transcript came alive as a stone tablet, onto which we continuously and non-destructively can capture changes of values or opinions, following the three individuals involved. We also started to glimpse the power of #transitional modeling as a formal framework.

The last article ended with the posit P4 as ({(S44, nickname)}, Jen, 1988). We had already seen a similar posit P2 as ({(J42, nickname)}, Jen, 1988). The way the story had been told, we have presumed that J42 is a female human being. Presumptions only lead to headaches. If not now, then somewhere down the road. The transcript is clearly not exhaustive enough, so we need to rectify this, and at the same time solve the mystery of identity S44.

As it turns out, an utterance about an unrelated topic was made in the discussion. Someone said "Haha, but I wonder what Jen (J42) feels about being hit by Jen (S44)? That storm is about to reach shores tomorrow." Aha, there's the person J42 and the storm S44, both nicknamed Jen. In order to tell what things are, we again need to reserve some roles. Let's reserve the strings 'thing' and 'class'. We can now create two new posits ({(J42, thing), (C1, class)}, active, 1980-02-13) and ({(S44, thing), (C2, class)}, active, 2019-08-10). These connect things to classes, but the classes themselves also need to be explained.

The classes C1 and C2 can be dressed up with a lof of their own information, but let us stay with the basics and only introduce two more posits ({(C1, named)}, Female Child, 2019-08-20) and ({(C2, named)}, Storm, 2019-08-20). But wait, Jen is not a child any longer. Let's also add ({(C3, named)}, Female Adult, 2019-08-20). If we assume that you become an adult at the age of 18, then ({(J42, thing), (C3, class)}, active, 1998-02-13). The same dereferencing set, but with a different value and a later timepoint, in other words a change. Things may change class as time goes by.

The third party reading the transcript is not much for specifics. Generics are much better. Let's help her out and add ({(C4, named)}, Person, 2019-08-20) along with ({(J42, thing), (C4, class)}, active, 1980-02-13). The third party can assert these, simultaneously as Jennifer herself asserts the other. There is a difference of opinion, leading to concurrent models, both equally valid. Thinking about it some more, it turns out that these particular classes can actually be related ({(C1, subclass), (C4, superclass)}, active, 2019-08-20) and ({(C3, subclass), (C4, superclass)}, active, 2019-08-20). Both female children and female adults are persons.

Now that we've seen some of what #transitional modeling can do, it is still only a theoretical framework. What if there was a database built using posits at its core? This is the topic of the next article, entitled "Rethinking the database".

---

Rethinking the Database

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


June 24, 2019
This is the final article in the series "What needs to be agreed upon", "What can be disagreed upon", "What will change and what will remain", and "What we are". The series has established the fundamental concepts in #transitional modeling, a theoretical framework for representing the subjectivity, uncertainty, and temporality of information. This is analog to the previously published paper "Modeling Conflicting, Unreliable, and Varying Information", but here with the assertion converted to a meta-posit. I will now be so bold as to state that all information is subjective, uncertain and temporal in nature.

Having worked with Anchor modeling for 15 years, it had evolved to the point where the old formalization from the paper "Anchor modeling — Agile information modeling in evolving data environments" was no longer valid. I had also come to the point where I started to doubt the relational model as the best way to represent Anchor. It felt as I was working against relational rather than with it as more features were added. A working theory of the beautiful constructs posits and assertions had already been formulated, albeit under other names (attributes and timeline annexes) back in 2012, "Anchor Modeling with Bitemporal Data". Thanks to these, I had started to think about what a database engine built around those concepts could do.

During the same period, NoSQL has seen its rise and fall, but it wouldn't have rose at all if there wasn't some circumstances in which SQL databases did not suffice. I believe it had to do with conformance. In order to get data into an SQL database it has to conform to a table, conform to a candidate key, conform to data types, conform to constraints, conform to rules of integration, conform to being truthful, conform to be free of errors, and conform to last. With this in place, data falls into three categories; non-conforming data that cannot be made to conform, non-conforming data that can be made to conform, and conforming data. From my own experience, almost all data I was working with fell into the first two categories. If it cannot conform, simply discard, BLOB, or in rare cases, find a fitting data type, such as JSON or XML. If it can be made to conform, write complex logic that molds the data until it fits. If it directly conforms, do a reality check or accept that you have a JBOT-style database.

Here, NoSQL flourished in comparison, with practically zero conformance demands. Just dump whatever into the database. For someone who is spending most of their time writing complex logic that molds the data until it fits, this sounds extraordinarily attractive. The issue here, as it turned out, is that what is no longer your problem suddenly became someone else's problem. The funny thing is, that someone else didn't even have a job description at the time, which is why it has taken far too long to realize that "inconsistent conformance on every read" is not such a nifty paradigm. However, we also want to leave the "perfectly consistent conformance on a single write" paradigm behind us.

We are currently at a point where we've visited two extremes of a scale on how to conform information in order to store it; totally and not at all. With that in mind, it's not that difficult to figure out a possible way forward. It has to be somewhere in between the two. I am not the only one who have thought of this. There is currently a plethora of database technologies out there, positioning themselves on this scale. To name a few, there are graph databases, triple stores, semantic fabrics, and the likes. In my opinion, all of these still impose too much conformance in order to store information. This is where I see a place for a transitional database, aiming to minimize conformance requirements, but still provide the mechanics for schemas, constraints, and classifications on write. Different from the others, these are subjective, evolving and possibly late-arriving schemas, constraints and classifications. Similar to "eventual consistency" in a blockchain, a transitional database has "eventual conformance".

Let's assume that we have access to a transitional database, built upon posits at its core. What type of queries could we expect to run?

Search anywhere for the unique identifier 42, NVP-like search.
Search for everything that has the girlfriend role, Graph-like search. 
Search for every time 42 was a girlfriend, Graph-like search. 
Search for everything nicknamed 'Jen', Relational-like search. 
Search for all Persons, Relational-like search.
Search for all subclasses of Person, Hierarchical-like search.
Search as it was on a given date, Temporal-like search. 
Search given what we knew on a given date, Bi-Temporal-like search. 
Search for disagreements between 42 and 43, Multi-tenant-like search. 
Search that which is at least 75% certain, Probabalistic-like search. 
Search for corrections made between two dates, Audit-like search. 
Search for all model changes made by Jen, Log-like search.
Search for how many times consensus has been reached, new feature. 
Search for how many times opposite opinions have been expressed, new feature. 
Search for individuals that have contradicted themselves, new feature.
Search for when a constraint was in place, new feature.
That sure seems like a handy database, given the things it can answer. It's a shame that it does not yet exist. Or does it? As it happens I am working on precisely such a database, written in the Rust programming language. My goal is to release a working prototype as Open Source by the end of the summer. After that I will need help, so start polishing your Rust now!

---

🅢🅗🅔 🅦🅞🅡🅔 🅐 🅑🅛🅤🅔 🅓🅡🅔🅢🅢

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


November 10, 2019
This is an article about imprecision and uncertainty, two in general poorly understood and often mixed up concepts. It's also about information, which I will define as saying something about something else¹. Information is the medium we use to convey and invoke a sense of that else; sharing our perception of it. The funny thing is, when we say something about something else, many things about the else will always get lost in translation. Information is, therefore, always imprecise and uncertain to some degree. What is perplexing, and less funny, is how we often tend to forget this and treat information as facts.

I think we have a desire to believe that information is precise and certain. The stronger the desire, the greater the willingness to interpret it as facts. Take Günther Schabowski as an example. When he, although uncertain, quite precisely stated that "As far as I know [the new regulations are] effective immediately, without delay." Those new regulations were intended to be temporary travel regulations with relaxed requirements, limited to a select number of East Germans. This later on the same day led to the fall of the Berlin wall and eventually contributed to the end of the cold war, if we are to believe Wikipedia. Even small words from the right mouths can have large consequences.

Now, in order to get a better understanding of imprecision and uncertainty, let us look at the statement 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤 in conjunction with the following photo.

She wore a blue dress (indeed)
First, we assume that whoever 𝕊𝕙𝕖 is referring to is agreed upon by everyone reading the statement. Let's say it's the woman in the center with the halterneck dress. Then 𝕨𝕠𝕣𝕖 is in the preterite tense, indicating that the occasion on which she wore the dress has come to pass. In its current form, this is highly imprecise, since all we can deduce is that it has happened, sometime in the past.

Her dress looks 𝕓𝕝𝕦𝕖, but so do many of the other dresses. If they are also 𝕓𝕝𝕦𝕖 we must conclude that 𝕓𝕝𝕦𝕖 is imprecise enough to cover different variations. One may also ask if her dress will remain the same colour forever? I am probably not the only one to have found a disastrous red sock in the (once) white wash. No, the imprecise colour 𝕓𝕝𝕦𝕖 is bound to that imprecise moment the statement is referring to. To make things worse, no piece of clothing is perfectly evenly coloured, but this dress is at least in general 𝕓𝕝𝕦𝕖.

Finally, it's a 𝕕𝕣𝕖𝕤𝕤, but there are an infinite number of ways to make a 𝕕𝕣𝕖𝕤𝕤. Regardless of how well the manufacturing runs, no two dresses come out exactly the same. The 𝕕𝕣𝕖𝕤𝕤 she wore is a unique instance, but then it also wears and tears. Maybe she has taken it to a tailor since, and it is now a completely different type of garment. In other words, what it means to be a 𝕕𝕣𝕖𝕤𝕤 is imprecise and what the 𝕕𝕣𝕖𝕤𝕤 actually looked like is imprecisely bound in time by the statement.

In fact, 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤 would have worked just as well in conjunction with any of the women in the photo². Me picking one for the sake of argument had you focusing on her, but in reality, the statement is so imprecise it could apply just as well to anyone. Imprecise information is such that it applies to a range of things. 𝕊𝕙𝕖 ranges over all females, 𝕨𝕠𝕣𝕖 ranges from now into the past, 𝕓𝕝𝕦𝕖 ranges over a spectrum of colours, 𝕕𝕣𝕖𝕤𝕤 ranges over a plethora of garments. 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤, taken combined increases the precision, since not every woman in the world has worn a blue dress. Together with context, such as the photo, the precision can even be drastically increased.

With a better understanding of imprecision, let's look at the statement anew and how: 𝗔𝗿𝗰𝗵𝗶𝗲 𝘁𝗵𝗶𝗻𝗸𝘀 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤. Regardless of its imprecision, 𝗔𝗿𝗰𝗵𝗶𝗲 is not certain that the statement is true. The word 𝘁𝗵𝗶𝗻𝗸𝘀 quantifies his uncertainty, which is less sure than 𝗰𝗲𝗿𝘁𝗮𝗶𝗻, as in: 𝗗𝗼𝗻𝗻𝗮 𝗶𝘀 𝗰𝗲𝗿𝘁𝗮𝗶𝗻 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤. Maybe 𝗗𝗼𝗻𝗻𝗮 wore the dress herself, which is why her opinion is different. Actually, 𝗔𝗿𝗰𝗵𝗶𝗲 𝘁𝗵𝗶𝗻𝗸𝘀 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤, 𝗯𝘂𝘁 𝗶𝘁 𝗺𝗮𝘆 𝗵𝗮𝘃𝗲 𝗯𝗲𝗲𝗻 𝘁𝗵𝗲 𝗰𝗮𝘀𝗲 𝘁𝗵𝗮𝘁 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕡𝕚𝕟𝕜 𝕕𝕣𝕖𝕤𝕤. From this, we can see that uncertainty is both subjective and relative a particular statement, since 𝗔𝗿𝗰𝗵𝗶𝗲 now has opinions about two possible, but mutually exclusive, statements. These are, however, only mutually exclusive if we assume that he is talking about the same occasion, which we cannot know for sure.

Somewhat more formally, uncertainty consists of subjective probabilistic opinions about imprecise statements. Paradoxically, increasing the precision may make someone less certain, such as in: 𝗔𝗿𝗰𝗵𝗶𝗲 𝗶𝘀 𝗻𝗼𝘁 𝘀𝗼 𝘀𝘂𝗿𝗲 𝘁𝗵𝗮𝘁 𝔻𝕠𝕟𝕟𝕒 𝕨𝕠𝕣𝕖 𝕒 𝕟𝕒𝕧𝕪 𝕓𝕝𝕦𝕖 𝕙𝕒𝕝𝕥𝕖𝕣𝕟𝕖𝕔𝕜 𝕕𝕣𝕖𝕤𝕤 𝕥𝕠 𝕙𝕖𝕣 𝕡𝕣𝕠𝕞. This hints that there may be a need for some imprecision in order to maintain an acceptable level of certainty towards the statements we make. It is almost as if this is an information theoretical analog to the uncertainty principle in quantum mechanics.

But is this important? Well, let me tell you that there are a number of companies out there that claim to use statistical methods, machine learning, or some other fancy artificial intelligence³, in order to provide you with must-have business-leading thingamajigs. Trust me that a large portion of them are selling you the production of 𝕊𝕙𝕖 𝕨𝕠𝕣𝕖 𝕒 𝕓𝕝𝕦𝕖 𝕕𝕣𝕖𝕤𝕤-type of statements rather than fact-machines. Imprecise results, towards which uncertainty can be held. Such companies fall into four categories:

Those that do not know they aren't selling facts. [stupid]
Those that know they aren't selling facts, but say they do anyway. [deceptive]
Those that say they aren't selling facts, but cannot say exactly why. [honest]
Those that say they aren't selling facts, and tell you exactly why. [smart]
Unfortunately I've met very few smart companies. Thankfully, there are some honest companies, but there is also an abundance of stupid and deceptive companies. Next time, put them to the test. Never buy anything that doesn't come with a specified margin of error, a confusion matrix, or some other measure indicating the imprecision. If the thingamajig is predicting something, make sure it tells you how certain it is of those predictions, then evaluate these against actual outcomes and form your own opinion as well.

Above all, do not take information for granted. Always apply critical thinking and evaluate its imprecision and the certainty with which and by whom it is stated.

﻿

¹ 𝘐𝘯𝘧𝘰𝘳𝘮𝘢𝘵𝘪𝘰𝘯 𝘵𝘩𝘢𝘵 𝘵𝘢𝘭𝘬𝘴 𝘢𝘣𝘰𝘶𝘵 𝘪𝘵𝘴𝘦𝘭𝘧 𝘪𝘴 𝘶𝘴𝘶𝘢𝘭𝘭𝘺 𝘤𝘢𝘭𝘭𝘦𝘥 𝘮𝘦𝘵𝘢-𝘪𝘯𝘧𝘰𝘳𝘮𝘢𝘵𝘪𝘰𝘯.

² 𝘈𝘵 𝘭𝘦𝘢𝘴𝘵 𝘧𝘰𝘳 𝘴𝘰𝘮𝘦𝘰𝘯𝘦 𝘸𝘪𝘵𝘩 𝘮𝘺 𝘭𝘦𝘷𝘦𝘭 𝘰𝘧 𝘬𝘯𝘰𝘸𝘭𝘦𝘥𝘨𝘦 𝘢𝘣𝘰𝘶𝘵 𝘨𝘢𝘳𝘮𝘦𝘯𝘵𝘴.

³ 𝘙𝘰𝘣𝘣𝘦𝘥 𝘰𝘧 𝘪𝘵𝘴 𝘰𝘳𝘪𝘨𝘪𝘯𝘢𝘭 𝘮𝘦𝘢𝘯𝘪𝘯𝘨, 𝘴𝘪𝘯𝘤𝘦 𝘸𝘦 𝘢𝘳𝘦 𝘧𝘢𝘳 𝘧𝘳𝘰𝘮 𝘩𝘢𝘷𝘪𝘯𝘨 𝘤𝘰𝘯𝘴𝘤𝘪𝘰𝘶𝘴 𝘮𝘢𝘤𝘩𝘪𝘯𝘦𝘴.

----

Rescuing the Excluded Middle

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


April 13, 2020
This is a continuation of "She wore a blue dress", in which we introduced to the concepts of imprecision and uncertainty. I will now turn the focus back on the imprecise value 'blue' and make that imprecision a bit more formal. In the works of Brouwer related to intuitionism an imprecise value can be thought of as a mapping. I will introduce the notation >blue< for such a mapping of the imprecise value 'blue'. The mapping >blue< would then be:

>blue< : x ⟶ [0,1]

In other words, for any color x it evaluates to either 1 for it being fully considered as blue or 0 if it cannot be considered blue. However, according to Brouwer any value in between is also allowed. It could be 0.5 for half blue, which is also known as a fuzzy imprecise value. Allowing these will confuse the with imprecision codependent concept of uncertainty. I will therefore restrict imprecise values, such as blue to:

>blue< : x ⟶ {true, false}

The reasoning is that subjectivity enters already in the evaluation of this mapping. In the terminology of transitional modeling, it is when asserting the statement "She wore a blue dress" that the asserter evaluates the actual color x of the dress against the value 'blue'. As such, the posit will be crisp from the asserter's point of view. Given that the dress was acceptably 'blue' enough, the asserter can determine their certainty towards the posit. Values can therefore be said to be crisp imprecise values, but only relative a subject.

If we assume that the occasion when she wore a dress took place on the 1st of April 2020 and this is used as the appearance time in the posit, then it is also an imprecise value. Most of us will take this as the precise interval from midnight to midnight on the following day. At some point in that crisp interval, the dress was put on. Even so, putting on a dress is not an instantaneous event and time cannot be measured with infinite precision, so regardless of how precisely that time is presented, appearance time will remain imprecise.

With finer detail, the appearance time could, for example have been expressed as at two minutes to midnight on the 1st of April 2020. But, here we start to see the fallacy of taking some time range for granted though. With the same reasoning as before we would assume that to refer to the interval between two minutes and one minute to midnight. However, there is no way of knowing that a subject will always interpret it this way. So, we need the mapping once again:

>two minutes to midnight on the 1st of April 2020< : x ⟶ {true, false}

It seems as if the evaluation of this mapping is not only subjective, but also contextual. If we know that it could have taken more than a minute to put on the dress in question, then maybe this allows for both tree and one minute to midnight evaluating to true. Even when such a range is possible to specify it is almost never available in the information we consume, so we often have to deal with evaluations like these. We have, however, become so used to evaluating the imprecision that we do so more or less subconsciously.

But, didn't we lose a whole field of applicability in the restriction of Brouwer's mapping? That fuzziness is actually not all lost. I believe that what assertions do in transitional modeling is to fill that gap, while paying respect to subjectivity and contextuality. It is not possible to capture the exact reasoning behind the assertion, but we can at least capture its result. Recall that an assertion is someone expressing a degree of certainty towards a posit, here exemplified by "She wore a blue dress". An example of an assertion is: "Archie thinks it likely that she wore a blue dress". With time involved this becomes: "On the 2nd of April Archie thinks it likely that she wore a blue dress two minutes to midnight on the 1st of April". Even more precisely and closer to a formal assertion: "Since the >2nd of April< the value >likely< appears for (Archie, certainty) in relation to 'since the >1st of April< the value >blue< appears for (she, dress color)'".

As can be seen, assertions can themselves be formulated as posits. Given the example assertion, it's value is also imprecise, with a mapping:

>likely< : x ⟶ {true, false}

We have however, in transitional modeling, decided that certainty is better expressed using a numerical value. Certainty is taken from the range [-1, 1], with 1 being 100% certain, -1 being 100% certain of the opposite, and 0 for complete uncertainty. Certainties in between represent beliefs to some degree. We have to ask Archie, when you say 'likely', how certain is that given as a percentage? Let's assume it is 80%. That means the corresponding mapping becomes:

>0.8< : x ⟶ {true, false}

Certainty is just another crisp imprecise value, but relative a subject who has performed a contextual evaluation of the imprecise values present in a posit with the purpose of judging their certainty towards it. An asserter (the subject) made an assertion (the evaluation and judgement), in transitional modeling terminology.

The interesting aspect of crisp imprecise values are that they respect "tertium non datur", which is Latin for "no third is given", more commonly known as the law of the excluded middle. In propositional logic it can be written as (P ∨ ¬P), basically saying that no statement can be both true and not true. An asserter making an assertion, evaluating whether the actual color of the dress can be said to be blue, obeys this law. It can either be said to be blue or it cannot. This law does not hold for fuzzy imprecise values. If something can be half blue, then neither "the dress was blue" nor "the dress was not blue" is fully true.

Fuzziness is not lost in transitional modeling though. Since certainty is expressed in the interval [-1, 1], it encompasses that of fuzzy values. The difference is that fuzziness comes from uncertainty and not from imprecision. Uncertainty is subjective and contextual, whereas fuzzy imprecise values are assumed objective and universal. I believe that this makes for a richer and truer to life, albeit more complex, foundation. It also rescues the excluded middle. Statements are either true or false with respect to crispness, but it is possible to express subjective doubt. Thanks to the subjectivity of doubt, contradicting opinions can be expressed, but that is the story of my previous articles, starting with "What needs to be agreed upon".

As a consequence of the reasoning above, a posit is open for evaluation with respect to its imprecisions. Such imprecisions are evaluated in the act of performing an assertion, but an assertion is also a posit. In other words, the assertion is open for evaluation with respect to its imprecisions (the >certainty< and >since when< this certainty was stated). This can be remedied by someone asserting the assertion, but then those assertions will remain open, so someone has to assert the new assertions asserting the first assertions. But then those remain open, so someone has to assert the third level assertions asserting the second level assertions asserting the first level assertions, and so on...

Rather than having "turtles all the way down", in transitional modeling there are posits all the way down, but for practical purposes it's likely impossible to capture more than a few levels. The law of the excluded middle holds, within a posit and even if imprecise, but only in the light of subjective asserters performing contextual evaluations resulting in their judgments of certainty. To some extent, the excluded middle has been rescued!


---

She'll wear a grue dress

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


April 14, 2020
This is a continuation of the articles "She wore a blue dress" and "Rescuing the Excluded Middle", which introduced crisp imprecision and fuzzy uncertainty. The former being evaluative and the latter both subjective and contextual. The articles discuss, relate, and sometimes further the formalization of transitional modeling, so they are best read with some previous knowledge of this technique. An introduction can be found starting with the article "What needs to be agreed upon" or by reading the scientific paper "Modeling Conflicting, Unreliable, and Varying Information". In this article I will discuss the effect of a chosen language upon the modeling of posits, with particular homage to the new riddle of induction and Goodman's predicate 'grue'.

In order to look at the intricacies of using language to convey information about the real world, we will focus on the statement "She'll wear a grue dress". First, this refers to a future event, as opposed to the previously investigated statement "She wore a blue dress", which obviously happened in the past. There are no issues talking about future events in transitional modeling. Let's say Donna is holding the dress and is just about to put it on. She would then, with absolute certainty, assert the posit "She'll wear a grue dress". It may be the case that the longer time before the dress will be put on, the less certain Donna will be, but not necessarily. If she just after New Year's Eve is thinking of what to wear at the next, she could still be certain. Donna could have made it a tradition to always wear the same dress.

There is a difference between certainty and probability. If Donna is certain she will wear that dress at the next New Year's Eve, she is saying her decision has already been made to wear it, should nothing prevent her from doing so. From a probabilistic viewpoint, lots of things can happen between now and New Year preventing that from ever happening. The probability that she will wear the dress at next New Year's Eve is therefore always less than 1, and will be so for any prediction. Assuming the probability could be determined, it would also be objective. Everyone should be able to come up with the same number. Bella, on the other hand, could be certain that Donna will not wear the dress at the next New Year's Eve, since she intends to ruin Donna's moment by destroying the dress. Certainty is subjective and circumstantial. I believe this distinction between certainty and probability is widely overlooked and the concepts confused. "Are you certain? Yes. Is it probable? No" is a completely valid and non-contradictory situation.

With no problems of talking about future events, let's turn our attention to 'grue'. Make note of the fact that you would not have reacted in the same way if the statement had been "She'll wear a blue dress", unless you happen to be among the minority already familiar with the color grue. If you belong to that minority, having studied philosophy perhaps, then forget for a minute what you know about grue. I will look at the word 'grue' from a number of different possibilities, of only the last will be Goodman's grue.

What is grue?

It is a color universally and objectively distinguishable from blue.
It is a color selectively and subjectively indistinguishable from blue.
It is a synonym of blue.
It is an at the current time widely known color.
It is an at the current time little known color.
It is an at the current time unknown color that will become known.
It is an at the current time known color synonymous with blue that at some point in the future will be considered different from blue (Goodman).
In (1) there will likely be no issues whatsoever. Perhaps there is a scientific definition of 'grue' as a range of wavelengths in between green and blue. On a side note and right now, the color greige is quite popular and a mix between grey and beige. Using that definition of 'grue' anyone should be able to reach the same conclusion whether an actual color can be said to be grue or not. Of course most of us do not possess spectrophotometers or colorimeters, so we will judge the similarity on sight. If enough reach the same conclusion, we may say it's as close to an objectively determinable color as we will get. This is good, and not much thought has to go into using >grue< in a posit.

In (2) there may be potential issues. Perhaps grue and blue become indistinguishable under certain conditions, such as lighting, or let's assume that 50% of the population cannot distinguish between grue and blue because of color blindness. Given two otherwise identical dresses of actual different colors, grue and blue, they may assert that she wore or will wear both of these, simultaneously. Such assertions can be made in transitional modeling and possible contradictions found using a formula over sums of certainty (see the scientific paper). To resolve this, non-contradiction either needs to be enforced at write time or periodically analyzed. Unknown types of color blindness could even be discovered this way, through statistically significant contradictory opinions. That being said, one should document already known facts and new findings with respect to effects that may disturb the objectivity of the values used.

In (3) there is a choice or a need for documentation. Either one of 'blue' and 'grue' is chosen and used consistently as the value or both are used but the fact that they are synonymous is documented. This may be a more common situation than one first may think, since 'grue' could be the word for 'blue' in a different language. This then raises the question of synonymy. What if there are language-specific differences between the interpretations of 'grue' and 'blue', so that they nearly but not entirely overlap? If grue allows a bit more bluegreenish tones than blue then they are only close to synonymous. This speaks for keeping values as they were stated, but that values themselves then may need their own model.

With those out of the way, let us look at how well known of a color grue is. In (4) almost everyone has heard of and use grue when describing that color. This is good, both those who are about to assert a posit containing >grue< will know how to evaluate it, and those later consuming information stored in posits will understand what grue is. With (5) difficulties may arise. In the extreme, I have invented the word 'grue' myself and nobody else knows about it. However, when interrogated by the police to describe the dress of the woman I saw at the scene of the crime, I insist on it being grue. No other color comes close to the one I actually saw. Rare values, like these, that likely can be explained in more common terms need translation. If done prescriptively the original statement is lost, but if not, it must be done descriptively at the cost of the one consuming posits first digesting translation logic. This is a very common scenario when reading information from some system, in which you almost inevitably find their own coding schemes, like "CR", "LF", "TX", and "RX" turning out to have elaborate meanings.

Now (6) may at first glance seem impossible, but it is not. Let us assume that we believe the dress is blue and the posit temporally more qualified to "She'll wear a blue dress on the evening of December 31st 2020". Donna asserts this with 100% certainty the day after the preceding New Year's Eve. When looking at the dress on December 31st 2020, Donna has learnt that there is a new color named grue, and there is nothing more fitting to describe this dress. Given this new knowledge, that the dress is and always has been grue, she retracts her previous posit, produce a new posit, and asserts this new one instead. The process can be schematically described as:

posit_1     = She'll wear a blue dress on the evening of December 31st 2020

assertion_1 = Donna, posit_1, 100% certainty, sometime on January 1st 2020

assertion_2 = Donna, posit_1, 0% certainty, earlier on December 31st 2020

posit_2     = She'll wear a grue dress on the evening of December 31st 2020

assertion_3 = Donna, posit_2, 100% certainty, earlier on December 31st 2020

Given new knowledge, you may need to correct yourself. This is precisely how corrections are managed in transitional modeling, in a bi-temporal solution, where it is possible to deduce who knew what when. This works for rewriting history as well:

posit_3     = The dress is blue since it was made on August 20th 2018

assertion_4 = Donna, posit_3, 100% certainty, sometime on August 20th 2018

assertion_5 = Donna, posit_3, 0% certainty, earlier on December 31st 2020

posit_4     = The dress is grue since it was made on August 20th 2018

assertion_6 = Donna, posit_4, 100% certainty, earlier on December 31st 2020

The dress is and always has been grue, even if grue was unheard of as a color in 2018. Nowhere do the posits and assertions indicate when grue started to be used though. This would, again be a documentation detail or alternatively warrant explicit modeling of values.

Finally there is (7), in which there is a point in time, t, before which we believe everything blue to be grue and vice versa. Due to some new knowledge, say some yet to be discovered quantum property of light, those things are now split into either blue or grue to some proportions. This is really troublesome. If some asserters were certain "She wore a blue dress" and others were certain "She wore a grue dress", in assertions made before t, that was not a problem. They were all correct. After that point in time, though, there is no way of knowing if the dress was actually blue or grue from those assertions alone. If we are lucky enough to get hold of the dress and figure out it is blue, things start to look up a bit. We would know which asserters were wrong. Their assertions could be invalidated, while we make new ones in their place. In the less fortunate event that the dress is nowhere to be found, previous assertions could perhaps be downgraded to certainties in accordance with the discovered proportions of blue versus grue.

The overarching issue here, which Goodman eloquently points out, is that this really messes up our ability to infer conclusions from inductive reasoning. How do we know if we are in a blue-is-grue situation soon to become a blue-versus-grue nightmare? To me, the problem seems to be a linguistic one. If blue and grue have been used arbitrarily before t, but after t signify a meaningful difference between measurable properties, then reusing blue and grue is a poor choice. If, on the other hand, blue and grue were actually onto something all along, then this measurable property must have been present and in some way sensed, and many assertions likely to be valid nevertheless. This reasoning is along the lines of philosopher Mark Sainsbury, who stated that:

A generalization that all A’s are B’s is confirmed by instances unless we have good reason to believe that there is some property, O, such that every A-instance is O, and if those A-instances had not been O, they would not have been B.
In other words, some additional property is always hiding behind issue number (7).

With all that said, there are a lot of subtleties concerning values, but most, if not all of them can be sorted out using posits and assertions, with the optional addition of an explicit model of values, together with prescriptive or descriptive measures. That being said, if language is used with proper care and with the seven types of 'grue' mentioned above in mind, you will likely save yourself a lot of headaches. We also learnt that people normally think in certainties rather than probabilities.

----

Time in Databases

 Lars Rönnbäck
Lars Rönnbäck

Ardent data dissector | AI-assisted author | Open source adherent


January 25, 2021
Is something in your database dependent on time? If you think not, think again. I can assure you there are plenty of such things. But, as plentiful as your time-dependent objects are, as plentiful are the creative ways I've seen them handled. Trust me, when you screw up time, the failures of your implementation will be felt, painfully. This is, however, understandable given the complexity of time and its limited treatment in commonplace database literature. This article aims to introduce a terminology together with some best practices and considerations that should be addressed before implementing time in a database. It is inspired by the article "Kinds of Time" by Christian Kaul, and likely has significant overlaps, but provides my slightly different view.

Primary and Documentary Times

In essence there are two purposes time can serve in a database. Time can be of a primary nature or of a documentary nature. Time of a primary nature is part of your primary keys, and your database engine will, if modeled accordingly, automatically ensure temporal integrity with respect to it. Time of a documentary nature are data points that are of a time type, like a date, but that are not part of your primary keys. If you need any constraints imposed over your documentary time, you will have to build and maintain them yourself.

For integrity reasons, any primary time values must be comparable in such a way that they form a total order. Time of day, such as 12:59, cannot be used as it will repeat itself daily, giving you no option to determine if two instances of 12:59 coincided or happened in some succession. Because of this requirement, primary times are often expressed through some calendar convention, such as Julian day, Unix time, or perhaps most commonly ISO 8601, which even accommodates for leap seconds. It is worth noting that any time that is affected by daylight saving is not totally ordered. In Sweden the hour between 02:00 and 03:00 on the last Sunday of October is repeated every year. Even so and unfortunately, I see many databases here use local time as primary time.

A decent choice for a primary time would therefore be coordinated universal time (UTC). Expressed in ISO 8601, such a time looks like 2021-01-25T07:23:47.534Z. While this may look satisfactory, there is an additional concern. The precision of the data type used to store this time in the database may debilitate the total ordering. Somewhat surprisingly, and often nastily discovered, the precision of a datetime in SQL Server is 3 milliseconds. The final digit in a time expressed as above can only be 0, 3 or 7 in the database. While this particular choice is unintuitive, there is always a shortest time span that can be represented through a data type, called its chronon. For primary times, a data type with a chronon shorter than anything happening in succession is necessary to preserve the total ordering.

Given that primary times are parts of primary keys in the database and altering primary keys is normally time-consuming, the choice of data types should be made with care. Always picking the data type with the smallest chronon, such as datetime2(7) in SQL Server with a 100 nanosecond chronon, may affect performance. While it can store a time like 2007-05-02T19:58:47.1234567 it will use 8 bytes, compared to 3 bytes for the date type, if daily changes are sufficient. Keeping primary keys small should be paramount for any database designer, since smaller keys lowers total storage and increase insert and join performance.

Documentary times are not required to have a total ordering or even be temporally consistent, making it possible for versions overlapping in time. With so much leniency choices can be made with much less consideration. Naturally, there are cases when you want to impose the same restrictions to documentary times, particularly if you intend for them to behave as primary times at some point.

Particular Recurring Timepoints

There are some particular recurring timepoints of interest, and for some reason beyond my understanding there is no standardised way to express these. Some common ones are:

The end of time.
The beginning of time.
Indefinitely.
At an unknown time.
The end of time is what it sounds like, the infinite extension of time into the future. An application for this would be if you want to express a fact such as 'I will love you forever'. Similarly, the beginning of time is the longest possible extension of time into the past. It could be applied in an expression such as 'gravity has always been present in the universe'. Indefinitely is similar to these, but in this case we expect an actual point in time will come to pass after which a time interval is no longer open-ended. An application, with the slight but important difference from 'forever' is 'I will cherish rock music until the day I die' or 'my hair will turn gray one day'. Finally, there is the unknown time. It can be used both for past and future events, such as 'The price was raised, but nobody remembers when that happened' and 'We will raise the price the next time crops fail'.

From a storage perspective, databases normally provide one special value; NULL, that is (somewhat horrifyingly) often used for all purposes above. Practically one could possibly reason that unknown time could be used in place of indefinitely, which in turn could be used in place of the beginning and end of time. Semantically, some important nuances will then be lost. For example, the nuance lost by stating 'I will love you until an unknown time' may yield an entirely different outcome.

Ideally, and if your database permits user-defined types, data types which includes and separates these particular timepoints should be implemented. ISO 8601 should also be extended with ways to express these notions. There is an interesting discussion on how to express these by shema.org here, for anyone who wants to dive deeper, which suggests that standards may be coming. Regardless, you should consider how you intend to manage particular timepoints like these.

Named Timelines

Even if there is just one single time, there are many timelines. A timeline can be thought of as an interval of time (finite or infinite) over which events happen in a temporally consistent sequence. If two events can mess up each others bonds in time, such as one moving the other in time, then they definitely do not belong on the same timeline. For example, if I have an appointment in my calendar between 9:00 and 10:00 today it lives on a different timeline from the action of me, at 08:00, rescheduling it to the afternoon. Timelines can also be separated by the fact that the events they track pertain to completely different things, and it would only decrease readability and understandability to keep them together.

Borrowing the terminology of transitional modeling, following are some examples of timelines commonly discussed in computer science and database literature. There is so little consensus on the naming of these so understanding what they represent is what matters.

Edit: Thanks to Maarten van der Heijden for making me realize that a consistent use of the word timeline for these, eg appearance timeline instead of appearance time, avoids confusion.

The Appearance Timeline

The appearance timeline contain points in time when some value was observed, became valid, or will come into effect in real life. It tracks the natural progression between values or states, both for attributes and relationships. Note that appearance timepoints may lie in the future, such as an already known price cut coming into effect on Black Friday.

In literature it is known by many different names: Valid time [Snodgrass], Effective time [Johnston], Application time [ANSI SQL:2011], and Changing time [Anchor modeling]. I also recall hearing these synonyms from forgotten sources: Utterance time, State time, Business time, Versioning time, and Statement time.

The Assertion Timeline

The assertion timeline contains points in time when some statement is subjectively assessed with respect to its certainty. In the simple case this is done by some system acting as the asserter and statements evaluating to either true or false. It is commonly used to track the correction or deletion of values or states, both for attributes and relationships. Note that assertion timepoints cannot lie in the future. If someone corrects the rebate for the upcoming price cut on Black Friday, this correction necessarily happens in the present.

In literature it is also known by many different names: Transaction time [Snodgrass], Assertion time [Johnston], System versioning time [ANSI SQL:2011], and Positing time [Anchor modeling]. I have heard less synonyms here from forgotten sources, only Falsification time and Evaluation time comes to mind.

For further reading on how to make uncertain assertions, to even being sure of the opposite, there is more information on transitional modeling in this series of articles.

The Recording Timeline

The recording timeline contains points in time at which information is stored in some kind of memory, typically when the data entered the database. This is very useful from a logging and later maintenance perspective. With it you can keep track of how quickly your database is growing on a per object basis, or revert to previous states of the database, perhaps after an erroneous load. It could have been the case that I sent all the price cuts for Black Friday into the production database but associated with the wrong products due to a faulty join.

In literature there are a couple of other names: Inscription time [Johnston] and Load date [Data Vault]. A very poor synonym I've seen used is Transaction time, which should be reserved for the assertion timeline alone.

The Structuring Timeline

The structuring timeline contains points in time at which the information had a certain structure and constraints. Yes, structure and constraints change over time too. This process is referred to as schema versioning in literature, but few mention keeping a named time line for tracking when structural changes happened. If someone comes asking why there were no price cuts for Black Friday last year, you can safely assure them that 'price cut' was not part of your information structure at the time.

The only other name I have seen is Schema Versioning Time, but it has a too technical ring to it, in my opinion.

Unnamed Timelines

Unnamed timelines are all the points in time that do not fall within any of your named timelines. There will be values in your database that are of a time type, but that are not immediately put onto named timelines, even if the attributes themselves are named. These may be assembled onto timelines for ad-hoc purposes or they may just be used as any other descriptive attribute. A typical example would be the point of time the receipt for the stuff I bought on Black Friday was printed. You are not likely to name the timeline on which birth dates occur either.

In literature there are a couple of other names: User defined time [Snodgrass] and Happening time [Anchor]. Again, I've seen Transaction time used for unnamed times when the timepoint represents some event in which a transaction took place. Again, an unfortunate confusion of terminology.

Time Tracking Scope

Before implementing time in your database, you need to consider which of the timelines above and possibly others you will need, since they need to be separable in your database, possibly as different columns in the same or adjoined tables. Along with that you will also need to determine your time tracking scope. For example, is it sufficient to track changes to any part of an address or do you need to track changes of the individual parts of an address?

If tracking any change is sufficient, you can use a single point in time for the entire address. Essentially, you will be viewing a changed address, regardless of which part changed, as a new address. If you track the individual parts you will need several points in time, one for the street, one for the postal code, one for the state, and so on. In this case the same address can have different postal codes over time.

The latter approach, tracking time for every single object (attribute and relationship) can be achieved through modeling in the sixth normal form, henceforth 6NF. With it change is visible without having to make comparisons with previous rows and no data is duplicated when only a part of something is changing.

Even if you do not go as far as 6NF your time tracking scope has to be decided, since the amount of timepoints you will store depend on it. Unfortunately, in many of the source systems I regularly fetch data from, there is usually just one column named "modified date" which is documentary. In other words you can only tell something has changed and when, but not exactly what or what came before it. In these situations you can, with a proper data warehouse, provide the history the sources lost.

Orthogonality

If you have an implementation that keeps track of both appearance and assertion timepoints, this is usually referred to as a bi-temporal implementation. The reason is that events on the appearance timeline are in a sense orthogonal to events on the assertion timeline. It is possible for the same value to appear and to be asserted simultaneously, but also at different times, so a single timepoint is not sufficient to describe both events. Furthermore, what value appears may be retroactively corrected by a later assertion. When a value appears may be also modified by an assertion. Keeping both of these on the same timeline, if you think of it as storing the date and time in a single column in a table, would cause collisions and ambiguities.

When appearances and assertions are easy to tell apart, using two different timepoints to describe these may be complex but straightforward. Problems usually arise when you are faced with a different value but nobody can tell whether it is a correction of the existing value or supposed to replace it from some point in time. This may lead to corrupt data if the wrong assumptions are made. Another issue is the fact that if you want a bi-temporal implementation with both appearance and assertion timelines treated as primary, a single table with a single primary key cannot guarantee temporal integrity. This requires careful modeling, and only a few modeling techniques have this as a "built-in" feature.

Proxying

Some of the most confusing aspects of time in databases come from the use of proxying, whether deliberate or unknowingly. If we assume that I have decided to keep track of appearance, assertion, recording, and structuring timelines in my database, with 6NF time tracking scope, then I am very much all set for anything thrown at me from a querying perspective. However, that is under the assumption that all of those timepoints will be available to me when I put data into my database.

Sadly, this is often not the case. This is true both for operational systems and data warehouses. Getting information like [Using the Megastore structure as of January 5th (The database recorded on Monday 10:12:42 that 'The manager asserted with 95% certainty on Monday at 09:15 that "The price cut will be 25% starting at midnight on Black Friday"')], actually never happens, yet. We do get some of the information some of the time though.

If we are in control of the database, we will always know when data is entering it. This opens up an opportunity. In the case that we do not know the assertion timepoint, say we only get "The price cut will be 25% starting at midnight on Black Friday", we can approximate it with the recording timepoint. In this example that means missing the mark by almost an hour. As unfortunate as this is, sometimes it is the only option.

Somewhat more dangerous, but also doable, is approximating appearance timepoints with recording timepoints. Let's say we only get "The price cut will be 25%" and we approximate it with the recording timepoint we will be dropping the price several days too early. Since recording timepoints always "happen" in the present when they come into existence, take utmost care when using it as an approximation for appearance timepoints. Still, this may sometimes also be the only option available.

Here within lies the big fallacy though. When enough approximations have been done, the different timelines become hard to distinguish, and it seems like you can use these timepoints interchangeably. This is not the case. You should always strive to get hold of the times when they are available and if proxying is necessary, and only as a last resort, then structure your loading intervals accordingly, to minimise the damage done.

Comparing Data Vault and Anchor

So far we have talked about time in databases from a theoretical perspective. There are two modeling techniques I would like to take a practical look at, taking diametrically different approaches to which timelines serve what purposes. The two techniques Anchor modeling and Data Vault are related, both being forms of Ensemble modeling, but still have many differences.

Edit: Thanks to Christian Kaul for pointing out a misconception I had about links in Data Vault, which has now been corrected.

Anchor modeling utilises 6NF to provide as granular time tracking scope as possible. It designates the appearance and assertion timelines as primary for both attributes and relationships (called ties) around a concept (called anchor), while the recording timeline is documentary. Ties are attribute-like since they have a primary timeline and in that they have no identity of their own, making tie-to-tie and tie-to-attribute connections impossible, and tie-to-anchors the only option. Anchor also maintains separate metadata for the information structure in which structuring time is primary. By treating appearance and assertion timelines as primary, the database engine will ensure bi-temporal integrity. However, that needs both to be present and have functionally adequate approximations when necessary. Anchor also makes the assumption that values are exhaustive, such that an existing value cannot become NULL, and must instead be explicitly marked as “Unknown”. There no NULL values in an Anchor model.

Data Vault is similar to Anchor, but is not 6NF and instead groups attributes together (called satellites) around a concept (called hub). A single point of time is used to track all changes within a satellite, regardless of which particular attribute changed. The big difference is that Data Vault uses the recording timeline as primary for satellites. Relationships (called links) have no primary, but include a recording timepoint as documentary. Links are hub-like since they lack a primary, and can therefore have their own identities. Theoretically link-to-link and link-to-satellite connections then become possible. The implication is that relationships that change over time must be managed through other connected objects. Figuring out that some change occurred requires you to look outside of the link. Links are also, opposed to ties, always many to many, so any additional constraints have to be managed by the application layer. If appearance and assertion timelines are present in satellites or elsewhere pertain to links, they are always documentary. I do not believe Data Vault has a notion of a structuring timeline in its standard.

The advantage of Anchor is that you do not have to worry about temporal integrity after the data has entered the database. Integrity is also practically a requirement if you want to use the technique outside of data warehousing. Anchor was designed to be a general modeling technique and it is applied in several operational systems. The downside is that you need trustworthy timepoints, which can require a lot of effort and digging in the sources. Values in a source that once existed and suddenly are NULL could pose a problem if they are indeed suddenly “Unknown” and your data type does not support it to be explicitly specified. This has, in my experience, very rarely happened, and almost always the NULL means ‘deleted’, as in asserting the statement as false, which is a different thing and handled without problems. Analysts find it easy to work directly with Anchor models, thanks to it being able to serve data as it appears at or as it was asserted at without any additional work than finding the correct bitemporal time slice.

The advantage of Data Vault is that you do not have to worry at all about temporal integrity at load time. For auditing purposes, it will reproduce inconsistencies in the sources perfectly, so if you need to provide auditing and validation reports it is an excellent choice. Since Data Vault focuses specifically on data warehousing, it is also less restricted in its choice of primary timelines. However, using the recording timeline, the temporal integrity of the now documentary appearance and assertion timelines will likely have to be taken care of later. I do believe that if any business users are going to be using the data, this must be done at some point. Pushing constraints on links to the application layer has advantages if you, for example, want to prevent bigamous weddings for Christians, but allow polygamy for Mormons. The downside is that keeping consistency in a link requires more work than for a tie. In the end about the same amount of work will likely have to be done both in Anchor and Data Vault, but with additional layers in the latter. Looking at Data Vault and its choice of recording time as primary it looks like an excellent choice for a persistent staging layer, with the usually recommended Dimensional model on top as the presentable part of the data warehouse.

In my opinion both are valid options. If you like many layers, using different modeling techniques, distributing a fixed total amount of work over them, then Data Vault is a good choice. If you do not want layers, and stick to a single modeling technique, doing a fixed total amount of work for that single layer, then Anchor is a good choice. Both have been proven in practice, also for Big Data, but Data Vault has many more implementations to date.

Imprecision and Uncertainty

Going forward I am doing active research on transitional modeling, in which two other aspects of time is also considered. First there is imprecision. There is no way to measure time with perfect accuracy, so all timepoints are imprecise to some degree. In an atomic clock this imprecision is minuscule, but not insignificant. Regardless, there are events whose boundaries are hard to determine. Like when I got married. When exactly did that happen?By using fuzzy data types, intervals, or margins of error, we can actually express imprecision in databases. There are open questions on how to address the total ordering if we allow imprecise points of time in our primary timelines. Is it possible to maintain temporal integrity with imprecise values, or will we have to treat everything as documentary, and later apply some heuristics with best guesses?

The other aspect of time is uncertainty, which is not the same thing as imprecision. Certainty is a subjective measure, in which a statement is assessed with a "probability to be true", loosely speaking. Using certainty it is actually possible to assert that you are certain of the opposite of a statement. This takes away a hard problem of storing 'opposite values' in a database by instead storing a negative certainty. Taking my marriage, if I look at "Lars was married on the 19th of June 2004" I can assert with 100% certainty that it is true, even if the time is imprecise enough to pin it down to a whole day. Looking at "Lars was married between 15:00 and 16:00 on the 19th of June 2004" I may actually be less certain, and assert it with 50% certainty, since I don't exactly remember if it was one hour earlier or not. There are some open questions on when you contradict yourself if values are imprecise and you make several (vague) assertions. If values are precise, there is an exact formula by which you can calculate exactly when you contradict yourself.

Conclusions

Hopefully I have not made time all too confusing compared to the post of Christian that inspired me. I do believe that time in databases is a complex matter, but that should be digestible for everyone, given that we can put ourselves on some common ground. All the different terminology and poor implementations out there definitely does not help.

It's time to treat time more seriously.