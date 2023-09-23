# Ethiopian-cultural-heritage-semantic-search-engine
. Introduction 
The Cultural Heritage Search Engine is a web-based application that allows users to search for and 
discover cultural heritage objects and locations in Ethiopia. The system aims to provide an intuitive 
search experience for users, facilitating access to information about cultural heritage. The system 
will conduct semantic searches based on a region/location, and retrieve cultural heritage 
information related to that region/location. Additionally, the search engine will retrieve results 
based on the keywords entered by the user, and the results will be recovered by matching the 
keywords to the database of cultural heritage information. 
2. Objective 
2.1. General Objective 
The general objective of this project is to design and implement a cultural heritage search engine. 
2.2. Specific Objective 
To achieve the general objective of this project, the specific objectives are specified as follows -
Create ontology that defines and categorizes cultural heritage entities. 
- Develop a semantic search function that enables users to find cultural heritage information 
based on a region/location. 
- Develop a keyword search function that enables users to find cultural heritage information 
based on a match of the search keyword. 
- Develop a search filter that refines search results.

  4.1 Classes 
4.1.1. Intangible Heritage 
Intangible Heritage encompasses non-physical manifestations of culture and includes the 
following subclasses: 
1. History: Deals with the study of past events, locations, and time periods. 
- Events: Significant occurrences in the past. 
- Locations: Geographical places associated with historical events. 
3
- Periods: Timeframes that define particular eras in history. 
2. Music: Encompasses various aspects of musical expressions and traditions. 
- Genres: Different styles and categories of music. 
- Instruments: Tools used to create musical sounds. 
- Performances: Live or recorded presentations of musical compositions. 
3. Oral Traditions: Focuses on cultural expressions passed down through generations via spoken 
word. 
- Drama: Theatrical performances and plays. 
- Expressions: Sayings, proverbs, and other forms of oral communication. 
- Folklore and Performing Arts: Traditional stories, legends, and performance-based art forms. 
4. Personalities: Individuals who have contributed to or influenced cultural heritage. 
- Architects: Professionals who design and oversee the construction of buildings and structures. 
- Artists: Individuals who create visual, auditory, or performing arts. 
- Historians: Scholars who study and interpret past events and societies. 
- Poets: Writers who craft compositions in verse. 
- Society: People who have shaped social, political, or economic aspects of culture. 
5. Religion: Encompasses various aspects of belief systems and spiritual practices. 
- Deity: Divine beings or supreme beings in different religious traditions. 
- Practices: Rituals, customs, and traditions followed by believers. 
- Rituals: Ceremonies and rites performed as part of religious observance. 
- Scriptures: Sacred texts containing religious teachings and narratives. 
- Symbols: Icons, images, or objects that represent religious concepts or beliefs. 
4.1.2. Tangible Heritage 
Tangible Heritage refers to the physical manifestations of cultural heritage and includes the 
following subclasses: 
1. Archaeology: The study of past human activity through the recovery and analysis of material 
culture. 
- Artifacts: Objects created or modified by humans in the past. 
4
- Excavations: Sites where archaeological investigation has taken place. 
- Ruins: Remnants of ancient structures or settlements. 
2. Architecture: Encompasses various aspects of the design and construction of buildings and 
structures. 
- Buildings: Constructed edifices with specific functions. 
- Landscapes: Designed or modified outdoor spaces. 
- Monuments: Structures erected to commemorate a person, event, or idea. 
3. Art: Diverse forms of human expression and creativity in visual and tactile media. 
- Manuscripts: Handwritten texts, often adorned with illustrations or decorations. 
- Paintings: Artworks created using pigments on various surfaces. 
- Photographs: Images captured through the use of a camera. 
- Sculptures: Three-dimensional artworks created by shaping materials. 
- Wall Cravings: Artistic designs or texts carved or etched onto walls. 
4. Cuisine: Culinary traditions and practices related to the preparation and consumption of food. 
- Foods: Edible items used to create dishes and meals. 
- Ingredients: Components used in the preparation of foods. 
5. Written Media: Text-based works that convey information, ideas, or stories. 
- Books: Collections of written or printed works. 
- Poetry: Creative compositions in verse. 
4.2. Object Properties 
- Represent relationships between two classes. 
- Have a domain and range defined, which are the two classes the property relates. 
- Can have inverse properties defined. 
Are represented as arrows between two classes in the Protege interface. 
- Created_by: 
Domain: Art , Range: Artist 
5
Domain: Cuisine , Range: Society 
- Designed_by 
Domain: Architecture , Range: Architects 
- Originated_from 
Domain: Oral traditions , Range: Society 
Domain: Cuisine , Range: Society 
- Part_of 
Domain: Art , Range: Artist 
Domain: Cuisine , Range: Society 
- Practiced_by 
Domain: Religion , Range: Society 
- Subclass_of 
Domain : Buildings, Foods, Artist, Ingredients, Poetry, Poets, locations, expressions, 
Historians, Paintings, Artifacts, folklore, Excavations, Practices, Diety, Scriptures, Rituals, 
Monuments, Genres, Landscapes, Sculptures, Books, performing_arts, Periods, 
Photographs, Performances, Instruments, Community leaders, Symbols, Events, Drama, 
Architects, Wall_cravings
Range: Cuisine, Music, Architecture, OralTraditions, Religion, Art, Personalities, 
Religion, Art, Personalities, History, WrittenMedia, Archaeology 
Domain: Archaeology Architecture, Art, Cuisine, WrittenMedia 
Range: Tangible heritage 
4.3 Data properties 
- Represent attributes of a single class. 
- Have a domain defined which is the class the property belongs to. The range is a data 
type like String, Integer, etc. 
- Do not have inverses. 
- Are represented as labels on the class node in the Protege interface. 
- Have predefined characteristics based on their data type. For example, a "String" data 
property can have max length defined.
- The data properties we have are the following: 
6
• Date 
• Description 
• Total Description
• Author
• Region
• Location 
• Name 
• Accession number
• Artist
• Classifications
• Coordinates
• CreditLine
• Description
• Date
• Narrator
• Video
5. RDF triplets
RDF triplets are the basic building blocks of Resource Description Framework (RDF) data. They 
are made up of a subject, predicate and object. RDF data is represented as a graph of these triplets.
For the cultural search engine data was collected from sources like UNESCO and MethMuseum. 
The individual values for each class and subclass were input and rdf triples were created. 
6. Apache Jena
Apache Jena is a Java framework that provides a variety of tools for working with RDF data. It 
can be used to create, store, and query RDF data, as well as to convert RDF data to and from other 
formats.
In our semantic cultural search engine, we used Apache Jena to store the RDF data that we had 
collected. We also used Apache Jena to execute test queries on the data. To store the RDF data, 
we created a Jena model. A Jena model is a collection of RDF statements. We added RDF 
statements to the model by using the Jena API. To execute test queries, we used the Jena query 
engine. The Jena query engine can be used to execute a variety of queries on RDF data. We used 
the Jena query engine to execute SELECT queries. 
7. Apache Solr
Preparing and Indexing the RDF data in Apache Solr was done by several steps: First, Solr was 
configured to handle RDF data. The ManageSchema.xml file was edited to enable the RDF plugin 
7
and specify an RDF configuration. This RDF configuration defined fields to index that mapped to 
properties in the ontology, as well as datatype mappings and options for indexing literals and URIs. 
Next, the RDF data was prepared by adding rdf:about attributes to identify each resource and using 
an appropriate RDF format. This has allowed Solr to index each resource separately. The data was 
then indexed by uploading the RDF file using Solr's URL upload handler. This POSTed the entire 
RDF data at once to Solr for indexing. In the RDF configuration, fields were mapped to the 
ontology properties that needed to be made searchable. This allowed Solr to extract the relevant 
values from the RDF data and index them. By following these steps of configuring Solr for RDF, 
preparing the RDF data, and then indexing and optimizing the data, a searchable cultural heritage 
dataset was created from the RDF data leveraging Apache Solr. Even though an indexed file was 
prepared, it was not included in the project since the dataset was too small and it was working very 
well without it. It can be included as the data gets more vast. 
8. SPARQL queries
StringqueryString="PREFIXuntitled-ontology-5: 
<http://www.semanticweb.org/feven/ontologies/2023/4/untitled-ontology-5#>\r\n"
 + "PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>\r\n"
 + "\r\n"
 + "SELECT DISTINCT ?subject ?name ?desc ?totalDesc ?region (SUM(?score) AS 
?relevanceScore) WHERE {\r\n"
 + " ?subject a/rdfs:subClassOf* untitled-ontology-5:" + classType + " .\r\n"
 + " ?subject untitled-ontology-5:Name ?name .\r\n"
 + " ?subject untitled-ontology-5:Description ?desc .\r\n"
 + " ?subject untitled-ontology-5:TotalDescription ?totalDesc .\r\n"
 + " ?subject untitled-ontology-5:Region ?region .\r\n"
 
 + " \r\n"
 + " # Calculate relevance score based on search term matches in properties\r\n"
 + " BIND(IF(regex(?name, \"" + searchTerm + "\", \"i\"), 4, 0) +\r\n"
 + " IF(regex(?desc, \"" + searchTerm + "\", \"i\"), 3, 0) +\r\n"
 + " IF(regex(?totalDesc, \"" + searchTerm + "\", \"i\"), 2, 0) +\r\n"
 + " IF(regex(?region, \"" + searchTerm + "\", \"i\"), 1, 0)\r\n"
 + " AS ?score)\r\n"
 + "} \r\n"
 + "GROUP BY ?subject ?name ?desc ?totalDesc ?region\r\n"
 + "HAVING(?relevanceScore > 0)\r\n"
 + "ORDER BY DESC(?relevanceScore)";


 
The SPARQL query will search for the cultural heritage and its data based on a given class type 
and search term. It will return: 
- The resource URI (?subject)
- The Name (?name) 
- The Description (?desc)
- The Total Description (?totalDesc)
- The Region (?region)
- A calculated relevance score based on how many times the search term matches in each property
The query performs the following:
1. Finds all resources that are of the given class type or a subclass 
2. Extracts the relevant properties: Name, Description, TotalDescription, Region
3. Calculates a relevance score by checking for regex matches of the search term in each property 
and summing the scores
4. Only returns results with a relevance score greater than 0
5. Groups the results by resource, and orders them by descending relevance score
The key parts are:
- Filtering by class type:
?subject a/rdfs:subClassOf* untitled-ontology-5:" + classType + " .
- Calculating the relevance score:
BIND(IF(regex(?name, \"" + searchTerm + "\", \"i\"), 4, 0) + ... AS ?score) 
- Filtering by score:
HAVING(?relevanceScore > 0)
- Ordering by score:
ORDER BY DESC(?relevanceScore)

9. UI
The UI was done using JavaFX sim builder.
