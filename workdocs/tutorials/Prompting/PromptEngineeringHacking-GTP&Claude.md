
here is 6 years of prompt Engineering in just 53 minutes I started working with AI back in 2019 using gpd2 and since
then I built a number of successful service and Consulting businesses the first that did 92,000 bucks a month the
second that did $72,000 a month and my current which just did $139,000 last month so I know how to build prompts for

business purposes and the goal of this video is just to dump my brain and give it to you I want to give you everything that I know about prompt Engineering in
as quick and as compressed a format as possible if you don't know me my name is Nick and my whole thing is cut in the fluff so let's get into it so we're
going to be doing this whiteboard style I'm going to be covering both very deep foundational underpinnings of how llms
work and I'm also going to be covering some more tactical actionable advice for beginners and novices um so we're going
to have a good blend of both the very first thing that I want to cover right off the bat and this is this will immediately improve your ability to
prompt engineer is instead of using the consumer models use the playground or workbench versions of these
models so if you're unfamiliar to keep a to make a long story short this is Chachi BT this is
the consumer model this is what open aai the big artificial intelligence company is marketing to people and selling for a
monthly subscription because this is a consumer model they've made a bunch of decisions to try and optimize
performance for the widest number of people those decisions include they actually insert a bunch of stuff into
your prompt that you can't see and that you don't know about so if you really want to get good at prompt engineering you need to stop using the consumer
models okay stop using chat GPT stop using Claud and instead start using
their API playground or workbench models so this is chat GPT this is platform. open.com
playground chat and as we see here there's a lot more that we can manipulate on the right hand side we
have a variety of uh different tools we can select model types we can select
response formats we can add functions we can configure our models with Randomness

temperature max tokens stop sequences top P frequency penalty and presence penalties if you don't know what all
this stuff is don't worry too much about it right now in addition you also get to insert your own system message and then
you have the choice of being able to add user or assistant messages too so I guess the point I'm making to make a
long story short is this is really where you get into the engineering side of prompt engineering if all you're doing is communicating with the bass you know
Claude Haiku or Sonet um or the chat GPT model you're just leaving a lot on the table so right off the GetGo if you
could take one thing out of this video it's just move over to the API playground versions you're going to have a lot more juice that you could squeeze
the second thing I want to talk about is that model performance a lot of people don't fully understand this but model
performance decreases with prompt length so there's
actually a hack that you can do to immediately boost the quality of all of
your outputs and that's just make your prompt shorter this is a graph here that shows a variety of models and their
abilities to reason AKA do some task over the length of the input text input
text in this case is obviously just like your prompt okay so what are we seeing here just to break this down right most
people are probably more familiar with GPT for Gemini Pro than they are with mistol and stuff like that so maybe just focus on the green and then the purple
and I mean the Green's the highest performance maybe we'll just focus on that what we see happen basically is that when the input length is
250 accuracy is almost one one means you know it gets basically everything right so it's like 0 N9 or something okay and
then the second that we add more okay we see like basically neutral or maybe a slight elevation or something between
250 to 500 but basically everything after that we see a decrease and it just
continues decreasing the entire way through okay so in this case it's a mile decrease between 250 and 3,000 um right
I mean if I could quantify this probably be like 0.4 or something 0.04 sorry
which is probably like a 4% decrease on the Chain of Thought reasoning um but if we're using like the basic model gp4
this is the normal thing that you that you'll call Performance goes down almost 20% right which is pretty
crazy so what does this mean well a quick and easy hack that you can do to improve the quality of your outputs is
literally just make your prompts shorter now you need to also consider that um
you know the more examples you provide an a model the more context you provide an a model it also tends to perform better so what I'm what I'm not telling
you to do is to remove all of the rules and instructions that you're giving the model instead what I'm telling you to do
is take the same information and shrink it basically improve the information density of the instructions that you're
providing okay this concept in English is called
AO obfuscation espo elucidation and the reason why it's written like this is
It's supp supposed to be kind of a joke right this just means keep it simple stupid but the person that wrote it
decided to write it in an extraordinarily verbose way just to show you how silly it is to write in a way
that's more complicated than normal Al to make this actionable I'm actually going to run you guys through a real example where I pair down and break down

a very verbose prompt into basically something that says the same thing just in like a tenth of the words so I have
my playground open over here I've added a system message that says you're a helpful intelligent assistant this is just my goto and I have a very long and
annoying prompt over here all about content creation I'm going to run you through it but I'm going to do so using a tool called wordcounter.net I paste it
all in there and I'm also going to open up another wordcounter.net so that I can edit this in um a subsequent page you
guys could see the impact on the length so right now this prompt is 674 words
okay for informational purposes uh a word is about 1.3 tokens or so uh
meaning that uh a token is about7 words this is probably somewhere around 800 or so tokens okay if we go back to our
graph here you know 800 or so tokens is already a almost 5% reduction in
accuracy so if we can get this to around 250 tokens instead of 800 if we can cut this by a third realistically we're
gaining about 5% accuracy or quality right off the bat and that's going to be our goal all right so how would I
actually go about pairing this down well I'm going to save you guys the um bleeding eyes from reading this whole
thing essentially what I'm doing is I'm asking this thing to produce some content for me we're doing it in a very verbose way for instance it says prompt
for high quality engaging and insightful content creation we could remove that completely primary objective and overall
goal of this content request well really primary objective is a same I'm just going to say objective it delivers 99%
of the same meaning but we do it in tenth of the words and in fact we don't even need objective because we're about to tell the model what we want it to do
and it's sort of implicit in us talking to a model that obviously the objective is what I'm about to tell you okay the
overarching aim of this content generation request is to produce an exceptionally well structured highly informative deeply engaging and
action-oriented piece of content that lines perfectly with the expectations needs and desires of my specific target audience wow does that sound super deep
and well thought out well it's not good prompts don't look like this good prompts are much much simpler so remove
this all and say your task is to produce high quality content the final content
should not only provide value in the form of information but should also serve as Authority well research and compelling resource that the reader or
viewer of this video based can rely for accurate insightful and practical knowledge high
quality authoritative content the content must be structured
in a way that ensures optimal readability maximum clar in logical flow being an effortless for the audience to digest and implement the concepts being
discussed should also avoid this part's funny excessive fluff or unnecessary tangents that do not contribute to the reader's overall understanding of the
subject matter your task is to produce high quality authoritative content that is readable clear and
avoids excessive fluff awesome so we have delivered the exact same message
we've done so in about 200 or 300 fewer words okay audience understand the
people this content must resonate with let's get rid of that your
audience is entrepreneurs and business
owners it looks like individuals who active engage running businesses particularly those focus on automation so entrepreneurs and business owners who
care about automation scalability I don't know that seems kind of vague to me and operational efficiency I'll say
Automation and operations you're also writing for technical
professionals let's say Consultants because odds are they are probably technical professionals if they are
among the first group and then time conscious efficiency driven
individuals I don't really know exactly what that means but to me it sounds like fluff so I'm going to get rid of it given that the audience consists of
Highly capable intelligent professionals the tone style and depth as content must be appropriately aligned to match their expectations avoid condescending
simplifications but also ensure that even complex concepts are articulated in a way that remains accessible
so write access write in an accessible manner perfect okay
guidelines so we could actually get rid of this whole section to ensure the generated content achieves the highest possible standard of quality depth and
Clarity we just say guidelines okay use a
direct and Ampersand instead of A and D tone of voice
avoid excessive casualness well that's what direct and pragmatic means unnecessary humor well that's what direct and pragmatic means storytelling
well this actually seems kind of necessary or new so I'll say avoid storytelling unless a story serves to
reinforce a key Insight writing should be clear concise and free of unnecessary jargon well I
kind of already suggested that given my previous instruction so I can just get rid of this
completely okay the content should be defined divided into well-defined sections each marked by appropriate headings and
subheadings so use headings and subheadings that's
easy use headings subheadings and bullet points numbered lists and clear
formatting elements very cool Ur a logical progression from one section to the next well if it's high quality
authoritative content that's readable clear and avoids excessive fluff odds are we're already going to have that okay depth detail and level of technical
rigor the content must we could just get rid of that complete and just say go beyond surface level insights and generic
advice it should provide unique specific and highly actionable information that differentiates it from lower quality content available elsewhere we can just
get rid of that that is embedded this is also
embedded and this was already suggested over here so we just get rid of that
okay do you guys kind of see how this is working we've already cut this down to 250ish tokens from previously uh which
what I believe was like closer to 800 or something like that so just in me going through this prompt line by line and
removing the excessive verbosity it's called I've already improved the quality of its outputs by approximately 5%
obviously this depends on the specific model that you're using but this is one of the funnest games in prompt
engineering you're given a prompt that maybe a company has been using for their model and your whole job is just take
that thing make it 30% shorter and improve the quality of your outputs automatically by 5% so you can see you

can get very far with just a few minutes the third tip I'm going to give you is
understand the different prompt types there are system user and assistant
prompts and these prompts are basically just the go-to for for all um large
language models at this point probably going to remain so for a while so if I go back to my chat GPT playground
example not that page this one over here and and actually if I just let's make this a little bit more Dynamic let's
grab my prompt that I've painstakingly edited over here let me just add this plus
button okay now what I'm doing is I'm embedding a system prompt which is at a
high level simply how the model identifies so this is who am I right
imagine you just turned on the IR robot
okay you just turned on this puppy and it's asking who am I all the
system prompt is is it's you answering that question oh you're a helpful intelligent assistant oh you're a an
email writing assistant oh you're a customer help desk assistant oh you are
a paperclip optimization maximizer who will certain and convert us all into aluminum right you are you are just
providing it simple straightforward instructions a very general one that you can use for most purposes you're a helpful gen uh helpful intelligence
assistant that works just fine we're saying that it's helpful because we want it to be helpful we're also saying it's intelligent because we obviously wanted
to like select an intelligent um you know an an intelligent example after that though what we have
is we have the user prompt so we always start with the system okay and I always recommend defining it
explicitly then the user prompt okay the user prompt is where you actually tell
the model what it is you want it to do and there's a specific structure within a user prompt that I will run you guys
through later but for now just know that this is where you provide the actual instruction to the model okay now the next sort of prompt is What's called the
assistant prompt if I were hypothetically just to press this button right now well it's not hypothetical because I just did it what's going to
happen is I just told the model to write me an article about birds and bees right I didn't say write it about birds and
bees you know I talked about doing it in the context of automation so let's see what it does birds and bees key insights
and analogies for business automation operations the birds and bees typically evokes blah blah blah blah okay great so
we're writing we're writing a bunch of stuff about birds and bees and how they can inform us as to how business Works what I have
now is we got the user prompt the system prompt up here the user prompt up here but now we've actually inserted an additional assistant prompt the output
of the model the thing that it just generated for us is now actually an additional part of our prompt called the
assistant and most people think well this is just the output of the model right I can't really do anything with this and here's where you're wrong well
what you can do is you can actually use this as an example to inform the model
whether or not what it just did is good and then use that as a template for future outputs okay what I mean is what
if hypothetically what if I said fantastic work now I want you to do the
same thing but do it for an article on stor delivery I don't know I'm just
making stuff up at this point what I'm doing now is I'm actually feeding in this prompt this prompt and this prompt
along with my n with my second user prompt and what I'm doing is I'm implicitly reinforcing that did a great
job on the last piece AK I wanted to do the same thing or I wanted to take a similar concept or similar approach uh
in order to do you know the next piece too and what we can see is you know we basically took the exact same structure
and format then we just copy and pasted it with this new uh you know with this new with this new idea the stor delivery
as opposed to birds and Beast now the reason why I bring this up is because this is at core at the core of all advanced prompting which I'm going to
get into now um but understanding how system user and assistant prompts work in concert and this this works across
all major large language models as the time of this video including Claude including you know uh deep seek and so
on and so forth understanding how that works under the hood is going to be critical in US developing higher level and more effective prompts the fourth

tip I want to talk about is to use one or few shot
prompting now for those of you that don't know one few zero shot all these
terms that you may may not have heard these just refer to the number of examples in the prompt if if I run you
guys through another little piece of uh of Academia here this was a study that was done a while ago on the performance
of large language models across the number of examples they were given to fulfill a specific task and what I want
you guys to see here is that there are three categories there's few shot one
shot and then zero shot zero shot is blue and it always performs the worst F
shot is orange and it always performs the best and right now I just want you guys to take a look at just the distance
in accuracy scores between this few shot and one shot if we go all the way to
175b that's about the size of um some of the simpler GPT models you know gpt3 GPT
3.5 uh because the study was in a couple years ago and technology has improved drastically my inclination is you know
we're probably I don't know if it's like 400b now this trend is probably the same
although you know a lot of these models are now totally behind closed doors you can't really see so I think that this trend is even better than it is now but
but like let's just take a look at this if we just extrapolate backwards this is somewhere around 40% accuracy right this
is almost 60% accuracy meaning that there's an accuracy gap of 20% between zero shot and few shot okay but that's
not actually the important thing what I want you guys to actually look at is notice how the dis the difference in accuracy between zero shot and one shot
is greater than the distance in accuracy or the difference in accuracy between one shot and few shot this is like
10% this is like 7% this brings to a very important point
that very few people know about that's that if you insert just one example into
your prompt you will gain a massive disproportionate Improvement in accuracy
that out Shadows if you were to add let's say 30 to your prompt I think um this F shot specific study uh was
something like 20 and N is equal to 20 examples so the distance between zero and one was like a time and a half the
distance between 1 and 20 and if you think about it considering now that we know what we know about the length of an
input and then the um accuracy Improvement as a result of shorter and shorter inputs we can actually see a
trend here if we only insert one prompt or one example in our prompt the
accuracy will be as high as humanly possible because the prompt itself will be short and then we're also going to get a massive boost in accuracy because
of how we structured our examples here okay so this takes me to an important
point about user assistant prompts which I'll run you guys through in a moment but essentially I guess what I'm trying to say is this is The Sweet Spot this is
like the gravy this is where you want to uh sorry not here this is the gravy you can tell I had to re-record this video
twice now cuz been droning on for like two hours uh my OBS incense just broke unfortunately so I I finished it now I
got to come back and do it again but whatever maybe I'm just smoother now um so so this one shot uh plus you know
what we know about keeping prompt length as short assumingly possible this is really like the goldilock zone and this
is really where you want to be as often as possible so my recommend for anything Mission critical always use
at least one prompt where at least one example to coers the model into
providing you a more accurate result the fifth tip I want to provide is this notion of conversational
engines versus knowledge engine okay what do I mean by these two

terms well llms like Chachi BT and Claude
are almost like a human being that's read a quadrillion Books
Okay so if we got a book here this is my fantastic super detailed and amazing
drawing of a book so we could see here I'm quite the artist I'm like the Pao Picasso kind I think um not saying that
Pablo Picasso wasn't amazing he is for those the guys that know art don't scw me uh okay so an llm is just like a
person that's read like a million books and just like a person that's read a million books if you went up to that you're like hey tell me the boiling
point of X oxy pyc Benzene or something
that person may roughly know what the boiling point is of things that are in a similar class but they're not going to
know exactly what that is 99.9% of the time just like a human being llms often
know roughly approximately what a right answer is just because they've read so many books they've picked up so many
patterns between Concepts but they don't know exact facts so llms okay are not
knowledge engines what they are are conversational engines you don't use llms to extract
knowledge for the most part unless that knowledge is very old and very commonly
known instead what you do is use them to talk use them to have conversations use them to reason or something introductory
level reasoning still but still reasoning now contrast this with something like a database if you you
know I think most of us would probably use Google Sheets here right so you know in Google Sheets you
have some sort of column heading so XYZ a and then you have like the data for the headings so maybe X is like name or
something to make this a little clearer and then you know the value here is Nick um tables and and databases and
encyclopedias okay these are knowledge
engines they essentially know facts but you can't have conversations with them
right can't have a conversation with an encyclopedia the cool part about llms really is when you hook up an
llm to a knowledge engine and then you basically have
it query that knowledge engine for some facts or some information okay so llms
on their own like the GPT whatever series of models these are conversational engines they don't know
facts and you shouldn't really rely on them for facts they're going to be very comp ident because it's just like I don't know the some dude at the bar
that's like absolutely man I know all about medieval history from 1864 to 1899
right medieval history good God uh that's definitely not medieval history folks clearly I am a conversational
engine but they're not going to know the specific facts they're going to be very confident in explaining these things to
you but unless you actually hook them up to some sort of external knowledge base you use something like you know rag which stands for retrieval augmented
generation which is where you query some data set using an llm you you ask it to
find you some data return that data and then have the llm produce the response
okay um you're not actually going to get like any usable information for the most part and even if you do you know I I
wouldn't trust it maybe it's right like 70% of the time for most queries but that 30% um that means a lot in business
applications right you're never really going to get somebody to pay you a lot of money for some sort of business application if you're wrong 30% of the

time okay speaking of being wrong the sixth tip I want to give you is to use completely UNAM uous
language what do I mean by unambiguous language well unfortunately or
fortunately AI is extraordinarily creative okay because it's very creative that means that when you ask AI
something the first time it'll give you a different answer than if you ask it the second time and that'll be a
different answer than if you ask it the third time and a fourth time and a fifth time and a sixth time okay if I could
just give you guys a quick little example here if this was like um if you played one of those games where like I
don't know you have some Zone that you need to hit or something okay I don't know maybe you guys have play this at the arcade or whatever and and basically
there's this little cursor and it goes ding ding ding and you're supposed to just like stop it right when it's in the
middle of some little goldilock Zone well large language models are are very similar if we have like this little
goldilock Zone here I want you guys to hypothetically just think about this as this is the zone of responses that you
want okay this is you know the perfect output of your prompt it's the the best
ice breaker it's you know the the perfect report or or whatever basically the way that large language models work
are you know if you query it the first time maybe you get a response over here okay quer it the second time maybe you
get a response over here quer it a third time maybe you get a response over here maybe it's only when you query it like the fourth time that you actually get
the response that you want what you want to do is you want to you want to you want to minimize this as much as humanly possible okay you want to get all of
these as close to that little green zone as humanly possible and I'll show you a
practical way to do this in just a few tips um but essentially one of the simplest ways for you to do this is to
be extraordinarily unambiguous with what you want okay so to make this practical
um you know a big a big thing a lot of people will use AI for is it'll you know
you'll ask it to do something like produce me a report based on this
data this is what I would call a bad prompt okay do not do this instead
say list our five most popular
products and write me a one line or one paragraph let's say
description this is a better prompt and you get even better if you say here's an example of a
one paragraph description for another product okay so why is the first bad and
the second good well I guess it's good so let's do a check mark the first is bad because we're just saying producer
report produce is extraordinarily ambiguous a report is extraordinarily
ambiguous based on this data is also extraordinarily ambiguous okay ideally
you'd say here is the data you don't just like make your own inferences about what to use of this data why is this
good because it's specifically saying what we want we want you to list five most popular products like if you produce a report on some reports it'll
it'll do 10 products and other ones it'll do two okay it's just kind of up to like how the model is feeling at the time but if you hardcode it in and say
you're doing five products in addition you're writing me a one paragraph description of each and in addition here's an example of the formatting well
now what you've done is you've constrained all possible outputs so that even if they're not perfect okay what
they are is they're probably a lot closer to that goldilock zone of responses that you want instead of being

super crazy spread out now they're at least like somewhere in the realm of what you constitute a good response
somewhere in the realm of what a business might want my seventh tip is a very quick and easy hack it's just use the term
Spartan in your tone of voice this is just one of those extraordinarily simple
things that you can just do in in every prompt um I just find the term Spartan is the perfect middle ground in terms of
like being direct and being pragmatic and then you know offering the model a little bit of flexibility so for
instance this guideline here I would I would write use a Spartan tone of voice I I think before I had um something different use a direct or or assertive
tone of voice just always say use a Spartan tone of voice your answers are just going to be way way better and way easier all right let's make this data
driven my eighth point is to iterate your prompts with

data now this is something of a more nuanced point but it's how you get the
highest quality prompts I see lots of people in my communities like maker school which is a day-by-day accountability program for people that
want to start an automation business it's something I've been running for uh quite a few months now a lot of people in maker School the way that they'll do
their prompt engineering is they'll spend all night coming up with some amazing prompt they think it's amazing anyway and then they'll run it once and
it'll deliver the most amazing output ever and they're like oh my God I finally figured it out I found the most amazing prompt I'm just going to use
this prompt for my business now okay the thing is do you remember earlier when I said that we have a range of possible
responses in the model sometimes it's going to respond over here other times it's going to respond over here other
times going to respond over here right odds are when you get a really good response in a model like 70% of the time
it's just because the model happened to produce something that was in line with your expectations but it wasn't
guaranteed to do so it just happened to do so so if you want to get prompts that
reliably and consistently produce outputs that are more in line with what you want what you have to do is you have to test them and then it's not enough
just to test them once you actually have to test them using what's called a Monte Carlo approach where you throw a bunch of stuff at the wall okay and then
progressively make changes to get it closer and closer and closer to where you want so I mean I don't if you guys
ever play darts okay but usually you have some like dart board and it looks like this and it's usually different colors and stuff and they're nice points
and you know like your your goal I think is you want to throw it like kind of over here all right so this is ideal
what usually happens is you know you're drunk as hell you start off playing darts you never played darts bar you throw one over here throw another one
over there throw another one over there throw one over there and you throw another one over there at the wall and hit the back of St you know Stacy's head
or something um every time that you iterate your prompt what you want to
happen is you just want the I guess total size of this to get smaller and more constrained so that's
that's route number two this is route number three and then ultimately what you want
is you want like a very accurate model that just consistently delivers you results in this perfect Zone how you
actually get there is you got to test and throw a bunch of stuff at the wall practically what this usually means is
you're going to do something like a Google sheet okay just like this you're going to have a prompt on the left hand
side you're going to have the output in the middle and then you're going to have another column that I just always call good
enough and then basically what you do is okay you grab your um chat gbt
playground in this case and then what you do is you generate 10 examples of what you want it
to do okay so for example this was one on birds and bees let me just delete
this other one so this is this is my my first article on birds andb so what I do is I actually paste it in here okay so I
pasted in the entire thing then I delete it all and then I do it again and usually
what I'll do is I'll use a no code model or no code tool something that just does things way faster um and then I'll just
like do it in the background but you know this is now like route number two so I'm going to wait for it to finish
its second output just for the purpose of this demonstration I won't do any more but basically after it's done with
number two I will copy all of this into another row okay uh that's not right
let's actually enter this and then what I'll do is I grab my prompt okay then I'll just stick
it on the left hand side on this prompt column and just because this isn't very viewable I'm just going to make this way
smaller so we could actually like see and maybe interpret this okay so I have two rows on my sheet
here right what I'll do after that is I'll do like I'll do another um I don't know I'll do like another 10 or
something like that uh and you know in my case I'm just going to do two but um in your case do
do 10 okay and what you do is you will read through every row and you'll say
hey is this good enough for my business is this good enough for the thing that I was hard to do this this good enough for the use case that I'm building my
automation for maybe this article is good enough maybe this one isn't okay so
we have one good enough out of two mathematically one out of two is equal to 50% %. realistically if I had like 20
of these or something like that you know what I would do is I would output 20 and then I'd go through and I'd read each of these and I'd ask myself hey this is
good enough and maybe 18 out of 20 are so if you know 18 out of 20 are then that's a total of 90% And then what I
would do is I would just test this against a different prompt so now instead of me just using my gut feeling
instead of me just having it generate one thing and me being okay with that one thing I have to do 20 and now I have
like statistics I basically have like some some science or some data behind my answer I'm like oh you know what that prompt actually beats the other prompt
19 times out of 20 that prompt actually beats the first prompt 13 times out of 20 that prompt actually beats the other
prompt 18 times out of 20 so what am I going to do I'm going to pick the one that's 19 times out of 20 and in this way you get more data driven and every
time you make a change and you run this test again you actually know hey I'm not just like throwing the most lucky bullseye on planet Earth okay I'm
actually statistically testing a big set of all of these outputs and then I'm finding which ones have higher accuracy
scores which ones are like more statistically correlated to the center of that Circle the ninth tip I want to

give you guys is to define the output format explicitly okay what do I mean by
explicitly well I mean like there are a lot of use cases where you're going to want something like a bulleted list so actually like say output a bulleted list
that's pretty easy right but there's a lot more than you can do than that um you know in instead
what we see a lot of people do nowadays is we output code blocks so output Json if you don't know what Json is it's
basically like a um specific JavaScript
notation where you will generate some curly braces a quote inside of this uh
thing that's encapsulated by quotes you have the variable or key name then you have a colon then you have some quotes around a value then you have another
curly bracket this is a very specific format that now allows you to integrate your large language model with code
servers scripts that that sort of stuff um you know like csvs okay if you want a
a a Google sheet and you want the Google sheet to say something like uh I don't
know like month um
Revenue uh profit you can actually have ai generate this don't just ask remember how earlier
I I told you guys um that don't just tell it to produce a report so don't just say produce
a sheet about
financial data or something that is bad instead what you wanted to do is you
want to say generate a
CSV with month
revenue and profit headings based off of the below
data and now like when it gives you an output it's actually going to give you an output that you can just copy and paste directly into Google uh Google
Sheets or or Excel or something you know you're going to have data that looks like this month Revenue profit then
it'll say like I don't know January okay it'll say like 13,000 it'll say you know 3,000 it's not
going to have any commas cuz it's comma separated but I'll get into that later maybe February it'll say 14,500
then it'll pull from some spreadsheet and grab this much for you right like your data is going to be a lot structured so if you want data in a
format don't just have it generate a thing and then have you have to go copy and paste it into a spreadsheet or into
your app or into your program later like actually just ask it to do the exact thing that you want it to do right off the Geto I'll show you the exact
structure you need in order to get this to Output reliably in a moment the 10th tip is to remove conflicting

instructions now this may sound pretty simple but it's a lot bigger of an
issue then I think a lot of people realize okay what do I mean by conflicting instructions well like a lot
of the words that we use we don't really think of but they have directly opposed
meanings I'll give you a quick example remember how earlier we went through and we made our whole thing really short our
whole prompt really short to take advantage of better accuracy well a word I always see and I've seen very often in
maker School my my 0 to1 community and then also make money with make.com which is a higher level Community um like a
lot of prompt engineering threads I see stuff like this detailed summary I want you to think about this logically like
if you produce a summary of something you are necessarily producing something that is simpler and smaller and and
lighter and and easier it's a it's a compressed form of you know the thing that you are doing you're basically
going you know from something like complex to simple right that's what a
summary is but if you ask for something detailed basically going from something simple to complex so then if you're
asking for a detailed summary what you're basically doing is you're it's like mathematically it's like it's like this equals zero okay it equals nothing
these two cancel each other out and what you end up doing is you just end up needlessly increasing token count for no reason so like when you say stuff like

produce an engaging article that is also very simple and straightforward or produce like a very comprehensive article that's still easy for newcomers
to understand right you're giving it conflicting instructions do you want it to produce something detailed or do you want it to produce something that's
that's not okay um just eliminate that it'll substantially reduce your token length and then it'll also allow you to
uh you know just get get a little bit better at defining things and and being simple and treating llms as I think that
you know they realistically should be treated which are tools that enable you to generate things not like at our
current level some super nuanced being that's able to like really fully understand the full gradient of the
decision that you've tasked it with the 11th tip I have for you is to learn JavaScript object notation XML then CSV
let's actually start with XML XML stands for
extensible markup language okay to make a long story
short all XML basically is it's just a way to structure data you remember how
like back in grade school um you know you would write a story and you write your name in the top left hand corner
you write the date over here you'd write the title over
here and then underneath here maybe you write the story right and then you hand
it in well all XML Json and csvr are just formats that allow you to embed
what all of these different things are in a simple and easy and standardized way um for computers to understand so
that you can do cool things with them like run you know cool programs and whatnot so you know if this is my big paper okay this is a big paper that I
wrote One me first place in school I got a $25 discard discard um a $25 gift card
to uh Denny's or something okay this is equivalent to this I have a little author
tag where it says Nick s then I have a closing author tag all
right this is now like universally understood that the author is Nick surve right maybe the date okay the date was
February the 19th and I close that tag off with date um title right well the title was
birds and bees right and I close out the title I could
go on and on but I think you guys understand this is a very particular formatting convention that allows you to
Define things okay if I go uh this one this one's pretty cool because I
actually used to um live and work in Sur so building ID Siri head office address
this is an address variable city city variable Province uh Province VAR country um country variable location
right you can embed data if I were to instead write a paper I'd say the sir
head office is located at 7445 132 Street which is in Siri BC
Canada I just want you guys to like see how much more every time I say Siri it
activates my Siri isn't that funny um I just want you guys to see how much more compressed this data is and how much
more immediately understandable this data is too so that's one reason why XML is awesome
um Json stands for JavaScript object notation it's very similar okay the only difference is instead of the tags the
less than and greater than symbols that we used along with some of those backs slashes um all this is is this is Curly
braces quotes characters um colons and then more curly
braces okay exact same thing right uh this would say
author and then this would say Nick sarf right exact same data if you could see
um Jason example you'll see data that looks just like this so instead of me saying hey
this guy's name is Richard he's a 33-year-old man who loves biking gaming squash and lives in Port space land he's
friends with Joe and Sarah and Michelle who are all you know 30ish somethings that live across the continent of the
United States like instead of me saying that I just create a little JavaScript object where the name variables equal to
Richard the age variables to 33 and so on and so forth and then CSV the reason
I bring this up is because this is a little bit more of a Nuance Point CSV is actually just the hyper compressed version of all of this where you don't
have to use these tag characters and you only have to mention the Thing Once okay so what I mean is okay remember this
author date and title a CSV file would actually just look like this author comma no space date comma no space
title and you'd have a little new line then here it would say Nick SV then it would say Feb 19 then it
would go birds and bees now this if you just like
count up the number of characters this is actually way less than all of this and the cool thing is when you do a new row you don't have to repeat the key
names what you can do is you can actually just you know um write the I don't know write everything in what's
called comma separated value format the comma here is the delimiter character the issue with using this in large
language models um is unfortunately large language models often lose their sense of place especially in longfall so
if you're producing a CSV that has I don't know like several hundred um inputs the large language model's
ability to like remember that the date column always comes second on I don't know like row number 1,00 and three or
something its ability to know that like date corresponds to Y it just tends to get muddled down which is why you typically only use csrees for for
smaller applications with large language models all right the 12th tip I want to give you guys is what I call my key

prompt structure so I have developed probably over a thousand prompts now for
businesses my own businesses other businesses I work with people that I consult with and so on and so forth and
this is what I do um on basically all of them okay so feel free to copy this on your own um use this for all your own
promps I'm going to show you what this looks like first we start with context then I give it instructions okay after
that I give it my output format you guys just use this to scaffold your own
then I give it rules and then finally I wrap it up with an example so let me show you guys a quick
actual look at what a real prompt that has made me almost um $500,000 looks like I'm going to show you guys this in
a no code tool it's called make.com it's what I personally use and I teach a lot about it as well um it is for a specific
tool called upwork upwork is a tool uh upwork is a freelancing platform or basically you
can bid on jobs and stuff like that and this prompt was written to allow me to take as input an upwork job
description uh and then have ai automatically process it filter it tell me if it's relevant to me and then write
me a oneline Icebreaker that's customized to that job so how this actually looks I start off with a system
prompt that says you're an intelligent admin that filters jobs that's pretty simple right no real rocket science here
then I have my user prompt and the way that I want you guys to look at this is through that lens that I provided you earlier okay with context first then
instructions then output format then rules and then some examples so let me break this down for you this
up here this is all my context okay so what do I mean I say hey I'm an
automation engineer that builds Outreach systems CRM systems project management systems no code systems and Integrations
right I'm sure I could cut this down in hindsite now that I know a little bit more about prompt engineering I built this thing out um I believe over a year
ago now uh it was one of the videos that actually made me go viral on YouTube then I say below is a job description filter it for relevance true or false in
Json some of the platforms include use air table clickup chat TBT make Monday zap here LinkedIn Google Sheets if
relevant write a short introductory Icebreaker okay but I'm not actually done yet I then give it some example
client projects these are things that I've done and then I tell it my format okay so let's just be abundantly clear
here I provided a context over here then I gave it some instructions over here so
sorry I think I misspoke earlier this is my context this is my
instructions okay after my context and instructions what I do is I give it my output format which is right over
here and then at the end I also have some rules now in this case I wrote them as notes but these are essentially my
rules then finally I actually give it some examples and the way that you do this in make.com and any other no code
tool is you will have your user prompt up here with all of those four bits that I showed you a moment ago and then you
have another user prompt with your first example then another assistant prompt with your first result and in my case I
did I think three or four shots so then I have a user with an example this is an actual job description from upw workk
then I have an assistant response with a result then another user prompt assistant prompt another user prompt
assistant prompt another user prompt assistant prompt another user prompt assistant prompt I think in this case looks like I had like seven or six or
something like that uh in hindsight probably too much and I was probably forced to do this just because models were a little bit less intelligent when
I built this out nowadays I might do like two maybe okay I also also wanted to show like a wide range of possible jobs which um
obviously helped to perform and this is why I have almost $500,000 in posted earnings on my profile because I use
systems like this to be able to apply to large volumes of jobs I've also helped a lot of other people and build out processes that involve things like this
so um in a nutshell I almost always use this key prompt structure with some slight variations context is where you
tell it what you want like who you are and what you want instructions are where you outline specifically and say your
task is to do XY Z output format is where you say something like return your results in Json using this format rules
where you say hey here's a quick list I want you you know don't do this do this don't do this do this then examples
where you actually give it those user prompt or user assistant prompt pairs okay the next thing I want to talk

about tip number 13 is to use AI to generate
examples for AI okay what do I mean by that well if we
go back to that prompt that I showed you guys a moment ago right we have a lot of examples here what you can do instead of
you actually finding an examp examples you get you can actually like create one yourself right so I can actually go and
I can create one so what do I mean by this I could say um I'm actually going to go all the way down to the bottom and
I actually want to generate my own little assistant prompt right so maybe
what I'm going to do now is uh I don't know I'm just going to go into AI paste this
and say I'm using this for training write me a similar training example as
the above this is just using a simple hotkey um option space on Mac where I
can launch a chat GPT instance I should know that this is not the same as the um
API that I'm using right now but does a pretty good job right so now I have this and what am I going to do I'm just going
to right click run this module only and it's actually going to go through and generate me a result using AI right
pretty simple and easy now this was back in the day when you could not parse uh
the Json in the make Doom module anybody that is a little bit more experienced with make.com is probably looking at
this and being like hey why aren't you parsing this directly inside of the prompt that's just because the gbd 40613 model just didn't have access to do it
as you could see there's no there's no tool for me to do so but basically what we've done is we've outputed some Json JavaScript object notation which I can
then feed into this module here to parse automatically then produce me a variable that I can access that looks kind of
like this reason result Icebreaker the last tip I want to provide you guys is a pretty simple one but it's to use the
right model for the task okay I see a lot of people nowadays

using very simple models so here's how it basically Works
simple models are cheap complex models are more expensive so this is a
gradient between simple and cheap complex and expensive the unfortunate thing is like 99% of people that I see
in in maker School make money with make a comment on YouTube they're way too far on the simple and the cheap side of
things as of the time of this video there there a bunch of models available I don't really want to date this too much but you know a bunch of these are like mini models and so what a lot of
people will do is they'll just use the mini models because they think that it's saving them a lot of money well unless you're running something like that is
doing 5 million operations or executions a day like unless you're running some serious backend infra
token costs are so little that it doesn't actually make any sense not to just use like smart models
most of the time obviously there's some exceptions but let me just run you through what the gbt 40 family models
looks like okay this $250 cents per million tokens of input $10 per 1
million tokens of output if we just like average them and say I don't know for the purposes of this I'm just going to say it's five bucks per 1 million tokens
combined okay this upwork RSS feed thing that I just did if we look at the usage
okay combin it was 1,169 I would have to use one I would have to do this 1,000
times to use $5 that's crazy how many do I actually do a day like 15 okay if we
do the math on this $5 divided by 1,000 means that for every run I use
0.5 this is equivalent to uh
55.5 C so basically every two times I run this it's 1 cent it's it's a it's a
penny every four times I run this it's two every eight times I run this it's four
right it's such a marginal small amount of money that there's no reason and this is by the way this is using a GPT 40613
and this is also using like a very very under optimized Pro well maybe not very under optimized but pretty under optimized prompt with what I know now
the reality is you know like uh any case that you could use GPT 40 mini which you
know is understandably much cheaper but basically any use case you could use GPT 4 a mini for unless you're sending
Millions of tokens on a daily basis just use the smarter model the smarter model will eliminate like half of the problems
that you didn't even know you had and I recommend always just starting with a smarter model and then working your way down as opposed to starting with a
dumber model and then trying to work your way up just way easier to do that way so I mean you know 75 bucks per a
million tokens for 4.5 or 150 bucks for a million tokens like like yeah that's pretty expensive and I could see that
being a limiter but the vast majority of these o based multimodal models anyway
um as of the time of this recording are hyper cheap and usually recommend Just DE buying yourself debiasing yourself
and just trying to use the more expensive ones wherever possible because at the end of the day they're not really that expensive my company um which is
called one second copy we still use a lot of tokens on a daily basis I think we spent like I don't know five bucks
last month that's that's a company right makes several tens of thousands of
dollars still so if you think about like the the return on investment of these tokens it it's crazy so just make sure
you use the right model for the task most of the time that involves using a little bit smarter model all right

that's it for this video had a lot of fun recording it and re-recording it for all yall if you guys have any questions about this just drop them down below if
you guys want me to make videos on a specific topic then please I love getting ideas and I'm inspired for the
most part by people like you that actually take the time to leave comments down below saying Nick can you do a video x1z Nick can you do a master class
on prompt engineering so this video is because somebody earlier on in my comments a few weeks ago asked me to do this and I'm more than happy to do what
you what you want me to do as well otherwise if you guys do me a big solid anybody that's on the cusp of you know
starting an automation agency or getting up and running with their own business that hasn't had a lot of experience in
service companies or in any sort of automation scenario before I'd highly recommend that you check out maker
school it's my day-by-day accountability program and you can get the link just in the description I guide you through setting up essentially your own
automation outfit um from complete scratch and bootstrap in the hell out of it while you're at it and for anybody
that maybe knows a little bit more about business that already has an automation business for instance or somebody that runs uh a business in a very similar
domain to automation maybe a marketing agency maybe some sort of advertising or creative business check out make money
with make.com it's my mid-level community that helps people that run businesses over5 to $10,000 a month
scale using my own products systems templates and so on and so forth both of these communities have me and them every
single day coaching and guiding you guys through I'm a very friendly and familiar face you can hopefully tell from now um
and yeah I'd be I'd be more than than happy to see you in there and then help you out if you guys could do me a solid like subscribe do all the fun YouTube
stuff I'll catch you on the next one cheers
- Generated with https://kome.ai