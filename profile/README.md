## Hidden Voices: Biographies of women achievers that are hidden no more!

Hidden Voices is an open source project managed by Robert Bosch Center for Data Science and Artificial Intelligence (RBCDSAI) and SuperBloom Studios in collaboration with the IITMAA. The project is created to reduce the gender data gap in Wikipedia and to build an inclusive internet. The objective of Hidden Voices is to develop information theoretical approaches, ML assisted auto identification and validation of external sources of data and generative AI methods to auto-generate a first draft of Wikipedia-style biography for notable women in STEMM.

### Motivation:
As a technically skilled woman in the STEMM field, try answering the following questions, honestly.
- Do you wish you had ways to find experts that look like you in your domain? 
- Were you frustrated that LinkedIn won't allow you to search for people by gender? 
- Do you not see any news about anyone who looks like you in the media or press? 
- Do you wish your women colleagues would get more recognition for the work they do within your community and outside your community?

Most of you would have answered yes to almost all of the questions above. Search engines generally use data scraped from publicly available websites and forums. There is an inherent gender gap existing in digital data in some of the most used websites and Wikipedia is one among them which is the only not-for-profit organisation. The issue is not the absence of women achievers in STEMM field; instead, it is the reduced representation of such women in public sources like Wikipedia. In fact, a 2021 study found that, in April 2017, 41% of biographies nominated for deletion on Wikipedia were women, despite only 17% of published biographies being women. Of the roughly 1.5 million biographical articles on the English Wikipedia in 2021, only 19% were about women.
A few years back, when you searched for a woman achievers’ full name in search engines like Google Search, it used to pull up the Wikipedia biographies of male counterparts who had similar last names instead. The visibility and reachability of women on Wikipedia is limited, with a 2015 report finding that female pages generally "tend to be more linked to men". 

People generally refer to the biographies of accomplished personalities on Wikipedia, since the data for Wikipedia is manually curated and validated by human editors. These editors are volunteers who do free labour. Also, Wikipedia has a set of rules called [notability](https://en.wikipedia.org/wiki/Wikipedia:Notability) ccriteria which allow the editors to determine if a person or a topic deserves its own article. Some potential issues with how Wikipedia curates data are the following:

- There is a greater chance that the editors may not be even experts in their fields and will come up with some inherent societal biases.
- Who decides the notability of a person or a topic?
- How many of the Wikipedia editors are actually women? There are some official numbers that can be found here: [Gender Bias on Wikipedia](https://en.wikipedia.org/wiki/Gender_bias_on_Wikipedia).

### Why has Hidden Voices started?
Contributing to Wikipedia is a labour-intensive process and it is completely manual. What if we could make the process of contribution easier for the editors or anyone who wants to add biographies of notable women in their respective fields with the assistance of artificial intelligence and machine learning tools?

The Hidden Voices project has been started to address the ever-widening critical data gap that exists, build tools to systematically reduce the gap at scale and to reduce the cost of participation in curating reliable biographies. The project will be an instance of a human-allied AI execution. While state-of-the-art automated language processing has significantly advanced, there are situations when the AI will make errors. This is especially true when processing documents about underrepresented populations, the very fact that this project is trying to address. Building products and services that are inclusive at the core is the mission of Hidden Voices. 

### The Approach:
The proposed system has three stages or pipelines, 

**1. Gathering and compiling pre-existing information:**

The first and foremost step in the wiki bio generation is curating quality data that includes women in STEMM who have done notable things in their respective fields but do not have representation on Wikipedia. Multiple reliable sources need to be identified and publicly available information must be curated. This can be accomplished by scraping the information published in the media, the public domain or asking people in different domains to provide details about accomplished women in their respective fields.
  - Dataset Curation: In order to collect information on such notable women, the following approaches are being used:
    - Obtain a list of past PhD graduates from academic institutions in India (specifically women who have graduated in the past) and get their publicly available social information by scraping the web.
    - Scrape existing biographies of women in STEMM from Wikipedia and leverage large language models to extract relationships and label them. Using the extracted relationships, regenerate the original wiki bio. The original bio, the extracted relationships, and the regenerated wiki bio can be quality checked through a hackathon and then used for fine-tuning instruction-based models. Using appropriate large language models as few-shot learners will help in generating data faster.
    - A google form has been designed with relevant fields that can be circulated to academic institutions, organisations and the public to collect more information on notable women they personally know in their respective fields.

**2. Distil knowledge into human-verifiable Intermediate Knowledge Representation (IKR):**

Once relevant data is obtained either through manual data curation or using the user interface built to collect it, information theoretical constructs (with or without ML) are used to extract relationships, label and sort information. Both rule-based and ML approaches have been tried to extract relationships but most of the methods failed to capture complex relationships and provided inaccurate results.

Large language models (LLM) are leveraged here to extract complex and almost accurate relationships and the extracted IKR is termed as factoids here. At this stage, the factoids are subjected to human validation and corrected for any misinformation by validating it against the data obtained at the first stage of data curation. A back reference is always maintained to the original data source from which the factoids are extracted.

**3. Wiki-like text generation from intermediate data:**

The extracted factoids along with reference to sources are used in generating Wikipedia-style biographies. Generative large language models are leveraged here. Hallucinations are a common problem when using large language models. To mitigate it, human validation is done in the IKR pipeline and only the accurate information is passed to the wiki text generation phase. Once the wiki style biography is generated, the user interface allows for editing the presented biography for inconsistencies or adding additional verified information about the women.

At each stage, human evaluation is done to check the quality of the data before it is passed on to the next stage. This helps in mitigating the hallucinations of the large language models and improving the data quality at all levels. 

![alt text](https://github.com/hiddenvoices/.github/blob/main/resources/architecture_simple.png?raw=true)


### How can you make a difference?

If you consider yourself an ally to improving diversity and inclusion in the tech world, specifically in the STEMM field, you can contribute to the Hidden Voices initiative by doing the following:

- Be an advocate. Spread the word about the initiative in your network.
- Conduct a bio-hackathon to collect data as part of the events you organise (the HV project team will support you with all the necessary kits and share the how-tos).
- Nominate female achievers who have contributed to your field through this [form](https://forms.gle/jyfbwUYYKCvyZ9JEA) or our UI (work in progress).
- Be an informed digital citizen and ally of women in your domain of knowledge and professional sphere.
- If you are a content creator, media person, or event organiser, then use our directory to find experts to deliver talks, be part of panel discussions, etc.
- Do cite us if you’re using our tool.



<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
