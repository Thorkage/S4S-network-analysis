# Community network analysis of the Science for Sustainability theme of Utrecht University🧑‍🧑‍🧒

This project was initiated in early 2024 as a student assistant project. It shall serve as a demo to test a network driven approach to **get a better understanding of what a community of researcheres is made up of**. The analysis has been performed on a set of researchers and their publications who are to some extent involved in the Science for Sustainability (S4S) community of Utrecht University (find more info here: https://www.uu.nl/en/research/sustainability/science-for-sustainability). More extensive documentation about the project can be found in the *docs* folder, along with 2 presentations held at an advisory board and board meeting, respectively. Additionally, there is a article on the S4S website (https://www.uu.nl/en/research/sustainability/science-for-sustainability/collaboration/exploring-the-s4s-community) which also includes a short video presenting the project: https://vimeo.com/973065588.

The workflow generated for this project can be roughly seperated into three steps: (1) 💾 Data collection, (2) 🐍 Data processing and (3) 📊 Visualization. 


### (1) 💾 Data collection:
We start the project with 2 given list of names: the mailinglist of S4S and the list of people who have the S4S tag on the 'UU medewerker' website. We need to merge the lists (*merge_lists_of_people.ipynb*) and see which of those people are reseachers. This is done by performing a check against the PURE database where researchers are noted (*lookup_pure.ipynb*). With the names of researchers we can now go ahead and try to find them on both Scopus (https://www.scopus.com) and OpenAlex (https://openalex.org/) via their API services (*retrieve_ids.ipynb*). Now we finally collect all the publications since 2020, when S4S came to life (*retrieve_authorsAndPaper.ipynb*). 

### (2) 🐍 Data processing:
With all the data in place, we want to find and build connections between researchers and their topics. For this we use the keywords of the publications and find those that are used by different authors. If that is the case, the keyword will be linked to those authors. We repeat for all authors and keywords that are part of our dataset and construct a network (*build_keywordAuthor_network.ipynb*).

### (3) 📊 Visualization
The visualisation can be 

 

