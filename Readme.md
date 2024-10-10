
# Distributed Tokenization and Embeddings Generation with Hadoop
## Created by: Yashvardhan Udia, yudia2@uic.edu
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

1. **Clone this repository**: ```[My Repo](https://github.com/messicode/CloudLLM/)```

2. **Navigate to the root directory**:
~~~
cd /path/to/root/folder/
~~~
3. **Build the Application**: ``` sbt clean compile assembly ```
4. **Run the Application**: ```hadoop <Jar file name.jar> <Main class name>```

## Result

A sample output of the default execution with a distributed system of 50 processes should look like this:
```
appoint, 11933	3
appointed, 71216	4
appointment, 52201	2
appointments, 11933, 1392	2
bears, 391, 15750, 291	1

```


## Contributing
Contributions are welcome! Please fork the repository and submit pull requests with any enhancements. Ensure to add unit tests for new features.

## License

This project is licensed under the [MIT License](https://github.com/messicode/Distributed_Systems/blob/master/LICENSE.txt). Feel free to use, modify, and distribute it as per the license terms.

## YOUTUBE DEMO
[My video](https://youtu.be/Yp4X_gxDO-Y)
## NOTE

- This project was successfully run on Windows 10 using command line
