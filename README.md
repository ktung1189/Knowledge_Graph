# Knowledge Graph To Mine Information from Text

## Objective

To create a knowledge graph from text using Natural Language Processing techniques.  

- 1st step: Split the text documents into sentences, then create a dataframe for the sentences.

- 2rd step: Entities Extraction using parts of speech(POS) tags to parse the sentences for a single word entity.  The nouns and proper nouns will be the entities.

- 3rd step: Extract Edges(relations) between nodes(entities) to one another.

<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/enitites.PNG" alt='entities'>

From the example above, the nsubpass is the entity and the pobj is the object, root is the relations.  So in the above example the word process would be the subject, d823 would be the object, and governed would be the root that connects the subject and object together.

## Purpose

To scape a text file and using nlp to parse and graph the knowledge graph nodes.  The text file link to imported is   https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2019/10/wiki_sentences_v2.csv that has only 1 subject and 1 object that has 4,300 sentences from over 500 Wikipedia articles.  The knowledge graph will be parsed and a knowledge graph will be created.

## Technologies Used

- Python
- Jupyter Notebook

## Modules Used

- Regex
- Pandas
- BeautifulSoup
- Urllib
- Requests
- Spacy
- Networkx
- Matplotlib
- Tqdm

## Graphs

- ***Top 30 Relations***
<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/relations.PNG" alt='relations'>

- ***Knowledge Graph with All Relation***
<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/Knowledge_Graph.png" alt='knowledge graph'>

The knowledge graph before any filtering for edges.  This graph is too gumbled gain any intelligence from the information.

- ***Knowledge Graph that has edge node filtered by "Released In"***
<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/Released%20In.png" alt='released in'>

By filtering the edge nodes by "released in" the graph becomes more interesting where the movies and released can be seen more clearly.

- ***Knowledge Graph that has edge node filtered by "Written By"***
<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/Written%20By.png" alt='written by'>

Filtering for "written by" it is clearly visible where authors and types are graphed.

- ***Knowledge Graph that has edge node filtered by "Composed By"***
<img src="https://github.com/ktung1189/Knowledge_Graph/blob/master/Images/composed_by.png" alt='composed by'>

Filtering for "composed by" it can be seen that music is connected by all the composers.