# Results

The `classes.tsv` file contains all the classes that have instances in the input domain subgraph on music, with their number of instances.

The `classes_95_7.tsv` file contains the 7 classes that have been selected based on the 0.95 threshold, with their number of instances.

The folder `all_subgraphs` contains all the subgraphs, one for each pattern, by selecting from the whole domain subgraph only the triples with an instance of the given class - or one of its subclasses - as subject.  E.g., for the class _album_, we will build a subgraph containing all the triples about instances of album or subclasses of album.

The folder `patterns` contains the actual results of the patterns extraction method applied to the music Wikidata subgraph. There is one subfolder for each pattern. In each subfolder, the relevant files are the following:
- the file `[CLASS]-properties.tsv` contains the list of properties involved in at least one triple, with the number of distinct instances that have at least one triple involving that property
- the file `[CLASS]-properties_85_[NUMBER-OF-PROPERTIES].tsv` contains the properties that have been selected for that pattern based on the 0.85 threshold, with their number of occurrences
- the file `[CLASS]-dr-pairs-frequent-properties_85.tsv` contains all the triplets (domain, property, range) involving the most frequent properties and instantiated in the subgraph, with their number of occurrences
- the file `[CLASS]-dr-pairs-frequent-properties_85_50_[NUMBER-OF-TRIPLETS].tsv` contains the triplets that have been selected based on the 0.50 threshold, with their number of occurrences
