
# Distributed Tokenization and Embeddings Generation with Hadoop
### Created by: Yashvardhan Udia
### Email: yudia2@uic.edu
### NET ID: 656090513

This Scala project implements a distributed system for tokenization and embeddings generation using Hadoop's MapReduce framework. 
It processes huge text corpus to create tokens and subsequently generates word embeddings using advanced techniques (like sliding window).

## Overview

- This Scala project leverages the Hadoop MapReduce framework to process text data efficiently. 
- The primary focus is on tokenization and the generation of word embeddings from input text. 
- The project consists of mappers and reducers that handle the tasks of breaking down text into manageable pieces (shards) and creating numerical representations (embeddings) for further analysis. 
- This approach is particularly useful in natural language processing (NLP) applications, where large volumes of text data need to be processed and analyzed.

## Project Structure
The main files are listed in below structure
```plaintext
project-root/
├── build.sbt                   # Build configuration
├── src/
│   ├── main/
│   │   ├── scala/
│   │   │   ├── MainApp.scala    # Main entry point for the Hadoop jobs
│   │   │   ├── TokenizationMapper.scala # Mapper for tokenization logic
│   │   │   ├── TokenizationReducer.scala # Reducer for aggregating tokens
│   │   │   ├── EmbeddingMapper.scala     # Mapper for generating embeddings
│   │   │   └── EmbeddingReducer.scala     # Reducer for finalizing embeddings
│   │   └── resources/
│   │       └── application.conf         # Configuration settings for the application
│   ├── test/
│   │   └── scala/
│   │       ├── TokenizationMapperTest.scala # Test suite for TokenizationMapper
│   │       ├── TokenizationReducerTest.scala # Test suite for TokenizationReducer
│   │       ├── EmbeddingMapperTest.scala     # Test suite for EmbeddingMapper
│   │       └── EmbeddingReducerTest.scala     # Test suite for EmbeddingReducer
```
## Features


## Building and Running

### Requirements

- Scala 3.5 
- Hadoop 3.3.6
- Java SE Development Kit 11
- SBT (Scala Build Tool) version (1.10.1)


## Getting Started

### Running the Application locally

1. **Clone this repository**: [My Repo](https://github.com/messicode/CloudLLM/)

2. **Navigate to the root directory**:
~~~
cd /path/to/root/folder/
~~~
3. **Update paths**: ```Update the corresponding paths in application.conf (Will be updated to input from command line arguments later on) ```
4. **Build the Application**: ``` sbt clean compile assembly ```
5. **Run Hadoop**: ```Use commands start-dfs.cmd and start-yarn.cmd to start hadoop processes.```
6. **Run the Application**: ```hadoop <Jar file name.jar> <Main class name>```
   
NOTE: Make sure the output path does not exist.


## Result

A sample output for the tokenization should look like this:
```
appoint, 11933	3
appointed, 71216	4
appointment, 52201	2
appointments, 11933, 1392	2
bears, 391, 15750, 291	1

```
For the embeddings:
```
Token	Embedding																																																																																																			
3305	-0.326765239	-0.063227907	-0.006134826	-0.598145783	0.42487523	-0.386558831	-1.039467812	0.606797338	0.660481393  ... 100 embeddings
791	0.7912516	0.299544364	0.941945672	-0.766571105	0.176163837	0.292200118	0.327613533	0.482545078	0.073925711	-0.226988479	...  100 embeddings
5907	0.115294464	-0.541093946	-0.160247117	-0.486180395	0.405101955	0.529536664	0.244080856	0.480882555	-0.473731011	... 100 embeddings
52686	0.184256598	-0.366833448	0.159912243	-0.189438492	0.320423007	0.269936919	0.421694756	0.311885566	-0.804217994	... 100 embeddings
58610	-0.464945167	0.01696438	0.293394834	0.460091263	-0.151001737	-0.205581665	-0.987886131	0.139263034	-0.232811913	... 100 embeddings
315	-0.254555047	-0.19791688	-0.170502663	-0.073417582	0.264686793	0.641144693	0.489721864	0.196015283	-0.650536776 ... 100 embeddings
```

![image](https://github.com/user-attachments/assets/c9a3fafd-08f5-46ff-8e7b-8bc3d0b6101c)



## Contributing
Contributions are welcome! Please fork the repository and submit pull requests with any enhancements. Ensure to add unit tests for new features.

## License

This project is licensed under the [MIT License](https://github.com/messicode/Distributed_Systems/blob/master/LICENSE.txt). Feel free to use, modify, and distribute it as per the license terms.

## YOUTUBE DEMO
[My video](https://youtu.be/Yp4X_gxDO-Y)
## NOTE

- This project was successfully run on Windows 10 using command line
