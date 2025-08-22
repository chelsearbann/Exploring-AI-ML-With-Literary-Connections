## Exploring Literary Connections Through AI, ML, and Data Visualization

Authors: Allen Wu, Chelsea Bann, Adin Handler

Original Project Presentation for Tufts University EM212 Applied Data Science: https://prezi.com/view/NUYGVJMI4kEhSDIYtwhz/ 

---

## Intro

For this project, AI was used to create tags for book reviews based on the sentiments in the review. Based on the sentiment-tag, the reviews would be matched with an image and placed in a 3D map using an open-source visualization toolkit. The primary dataset contained real reviews of "To Kill A Mockingbird" (TKAM) by Harper Lee, sourced from Goodreads (https://www.goodreads.com/). This targeted selection allows for concentrated analysis of reader feedback and thematic connections within the text. Later, the project can expand to include other datasets. It is important to note that due to the scope/timeframe of the class, the project was not completed.


## Problem Statement: 

To train AI to match photos with reactions to literature and place these matches in digital space. The inputs are images and book comments, and the output are spatial correlations on a map.  

**Goals:** 
- To understand connections in human experience
- To build a local LLM
- To create art through interactive digital visualization
 

## Key Themes:  

AI, Machine-Learning, Data Visualization, Arts & Culture, Human-centered design.  

These themes guide the design and execution of our project, ensuring a comprehensive approach to understanding connections in human experience. 

 
## Critical Questions: 

How can complex ideas be visualized?  

Can ideas be connected back to the media that influenced them?   

Do algorithms’ feature maps relate ideas similarly to humans? 


--- 

There are many platforms where text can be input to receive multimedia content, knowledge, and complex ideas as result. There are none that work in reverse – that start from an arbitrary, seldom travelled location in the space of human experience, and expand from there- how did someone get here? Where are they going next? Software that could assist people in answering these questions would facilitate better ways of communicating ideas and richer discussions.  

Various projects, like Every Noise at Once and Art Emotions Atlas, create networks of media. These focus more on content relationships rather than the commentary-derived insights which this project is pursuing. 

Every Noise at Once is an attempt at an algorithmically-generated, readability-adjusted scatter-plot of the musical genre-space, based on data tracked and analyzed for 6,291 genre-shaped distinctions at Spotify through 2023-11-19. (Mcdonald n.d.)  

Art of Emotions description: "In collaboration with Google Arts & Culture, Scientists from the University of California Berkeley, asked 1,300 people to describe how 1,500 paintings make them feel by choosing from different words, and discovering 25 different emotions that participants associated with the artworks.” (Google Arts and Culture 2021).  

In contrast this project uniquely targets the linkage between book reviews and corresponding text sections, mapping them to images. This backward tracing connects ideas to their media origins, enriching the understanding of their relationships. 

---

## Methods 

Data Cleaning:
- Isolated Book ID for To Kill a Mockingbird. 
- Wrote R code to extract the TKAM reviews into an isolated dataset (attached).
   
Tagging: 
- ChatGPT-4 was used to create tagging system for the dataset with a detailed prompt.
- For next steps, the tags need refinement for more accuracy. For example, in the first attempt, one review was clearly disappointed with the book and the LLM tagged it with “positive sentiment.” For the future, a code can be written to isolate one book review at a time, feed each individual review into our local LLM so that it can better interpret the themes, nouns, ideas, and emotional cues from the individual review. We hypothesize that isolating each quote will create a more accurate tagging index by the LLM.  

 
## Datasets 

GOODREADS DATASET: 

English review subset for spoiler detection (~1.3m book reviews about ~25k books and ~19k users, raw texts): 

goodreads_reviews_spoiler_raw.json.gz (https://mcauleylab.ucsd.edu/public_datasets/gdrive/goodreads/goodreads_reviews_spoiler_raw.json.gz)

SOURCE: 

https://cseweb.ucsd.edu/~jmcauley/datasets/goodreads.html#datasets 

IMAGE DATASET:

Undisclosed. 

---

## Works Cited 

- Glen McDonald, n.d. “Every Noise at Once.” Accessed May 8, 2025. https://everynoise.com/engenremap-austindie.html. 

- Google Arts & Culture. 2021. “Art Emotions Map.” Accessed May 8, 2025. https://artsexperiments.withgoogle.com/art-emotions-map/. 

- United Nations Environment Programme (UNEP). 2024. Artificial Intelligence (AI) end-to-end: The Environmental Impact of the Full AI Lifecycle Needs to be Comprehensively Assessed - Issue Note. https://wedocs.unep.org/20.500.11822/46288 

- Wan, Mengting. 2018. Goodreads Datasets: Code Samples. GitHub. https://github.com/MengtingWan/goodreads. 

- Mengting Wan and Julian McAuley. "Item Recommendation on Monotonic Behavior Chains." Proceedings of the 12th ACM Conference on Recommender Systems (RecSys '18), 2018. https://github.com/MengtingWan/chainRec? 

- Mengting Wan, Rishabh Misra, Ndapa Nakashole, and Julian McAuley. "Fine-Grained Spoiler Detection from Large-Scale Review Corpora." Proceedings of the 57th Annual Meeting of the Association for Computational Linguistics (ACL '19), 2019. https://github.com/MengtingWan/goodreads? 
